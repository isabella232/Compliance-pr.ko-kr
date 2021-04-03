---
title: Microsoft 365의 SharePoint 및 OneDrive 데이터 복원력
description: 이 문서에서는 Microsoft 365의 SharePoint 및 OneDrive 데이터 탄력성에 대한 개요를 제공합니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c267551f26b4dd96e3762b0edc2942a3cb22eb5c
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496758"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Microsoft 365의 SharePoint 및 OneDrive 데이터 복원력

Microsoft 365 내에서 OneDrive는 SharePoint 파일 플랫폼을 토로합니다. 이 문서에서는 두 제품을 모두 참조하는 데 SharePoint만 사용됩니다. 이 문서의 내용은 Microsoft 365와 관련이 있으며 소비자 서비스에는 적용되지 않습니다.

SharePoint의 핵심 콘텐츠 저장소를 만드는 두 가지 기본 자산이 있습니다.

- **메타데이터:** 각 파일에 대한 메타데이터는 Azure SQL 데이터베이스에 저장됩니다. Azure SQL SharePoint에서 사용하는 완전한 비즈니스 연속성 스토리와 자세한 내용은 이 문서 의 부분에 설명되어 있습니다.
- **Blob Storage:** SharePoint에 업로드되는 사용자 콘텐츠는 Azure Storage에 저장됩니다. SharePoint는 사용자 콘텐츠와 실제 활성/활성 시스템을 거의 실시간으로 복제할 수 있도록 Azure Storage에 사용자 지정 탄력성 계획을 구축했습니다.

데이터 탄력성 보장을 위한 전체 컨트롤 집합은 추가 섹션에서 설명합니다.

## <a name="blob-storage-resilience"></a>Blob 저장소 탄력성

SharePoint에는 Azure Storage에 고객 데이터를 저장하기 위한 사용자 지정 솔루션이 있습니다. 모든 파일은 기본 및 보조 데이터 센터 지역에 동시에 기록됩니다. 두 Azure 지역에 대한 쓰기가 실패하면 파일 저장이 실패합니다. Azure Storage에 콘텐츠를 작성하고 나면 체크 체크 인이 메타데이터와 별도로 저장되고 이후의 모든 읽기 중에 커밋된 쓰기가 SharePoint로 전송된 원본 파일과 동일한지 확인할 수 있습니다. 모든 워크플로에서 이와 동일한 기술을 사용하여 발생해야 하는 손상이 전파되지 않도록 합니다. 각 지역 내에서 Azure LRS(Locally Redundant Storage)는 높은 수준의 안정성을 제공합니다. 자세한 내용은 [Azure Storage 중복성](/azure/storage/common/storage-redundancy-lrs) 문서를 참조하세요.

SharePoint는 저장소 Append-Only 사용 합니다. 이 프로세스를 통해 초기 저장 후 파일을 변경하거나 손상할 수 있지만 제품 내 버전 관리 기능을 사용하여 이전 버전의 파일 콘텐츠를 검색할 수 있습니다.

![Blob 저장소 탄력성](../media/assurance-blob-storage-resiliency-diagram.png)

두 데이터 센터의 SharePoint 환경은 두 Azure 지역의 저장소 컨테이너에 액세스할 수 있습니다. 성능상의 이유로 동일한 로컬 데이터 센터의 저장소 컨테이너가 항상 선호됩니다. 그러나 원하는 임계값 내에서 결과를 볼 수 없는 읽기 요청에는 데이터가 항상 사용 가능하도록 원격 데이터 센터에서 요청한 콘텐츠가 동일하게 설정됩니다.

## <a name="metadata-resilience"></a>메타데이터 탄력성

SharePoint 메타데이터는 Azure Storage에 저장된 콘텐츠에 대한 선택키 및 위치가 저장되어 있는 사용자 콘텐츠에 액세스하는 데도 중요합니다. 이러한 데이터베이스는 광범위한 비즈니스 연속성 SQL Azure 2013에 [저장됩니다.](/azure/sql-database/sql-database-business-continuity)

SharePoint는 Azure SQL 제공하는 복제 모델을 사용하며 장애 조치(failover)가 필요한지 결정하고 필요한 경우 작업을 시작하는 독점 자동화 기술을 구축했습니다. 따라서 Azure 데이터베이스 관점에서 '수동 데이터베이스 장애 조치(failover)' 범주에 SQL 있습니다. Azure SQL 복구 가능성에 대한 최신 메트릭은 에서 사용할 수 [있습니다.](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)

![메타데이터 탄력성](../media/assurance-metadata-resiliency-diagram.png)

SharePoint는 Azure SQL 백업 시스템을 사용하여 최대 14일 동안 PITR(Point in Time Restores)을 사용하도록 설정할 수 있습니다. PITR에 대한 자세한 내용은 이후 [섹션에서 설명합니다.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>자동화된 장애 조치(failover)

SharePoint는 사용자 지정 자동 장애 조치(failover)를 사용하여 위치별 이벤트가 발생할 때 고객 환경에 미치는 영향을 최소화합니다. 모니터링 기반 자동화는 특정 임계값을 초과하는 단일 또는 다중 구성 요소 실패를 감지하면 문제가 있는 환경에서 웜 보조로 모든 사용자의 활동이 자동으로 리디렉션됩니다. 장애 조치(failover)를 통해 메타데이터 및 컴퓨팅 저장소가 완전히 새 데이터 센터에서 처리됩니다. Blob 저장소는 항상 완전히 활성/활성 상태이기 위해 장애 조치(failover)를 변경할 필요는 없습니다. 계산 계층은 가장 가까운 Blob 컨테이너를 선호하지만 항상 로컬 및 원격 Blob 저장소 위치를 모두 사용하여 가용성을 보장합니다.

SharePoint는 Azure Front Door 서비스를 사용하여 Microsoft 네트워크 내부에 라우팅을 제공합니다. 이 구성은 DNS에 독립적인 장애 조치(failover) 리디렉션을 허용하고 로컬 컴퓨터 캐싱의 영향을 줄입니다. 대부분의 장애 조치(failover) 작업은 최종 사용자에게 투명합니다. 장애 조치(failover)가 있는 경우 고객은 서비스에 대한 액세스를 유지 관리하기 위해 변경할 필요가 없습니다.

## <a name="versioning-and-files-restore"></a>버전 및 파일 복원

새로 만든 문서 라이브러리의 경우 SharePoint는 기본적으로 모든 파일에 대해 500개 버전으로 기본 설정되어 있으며 필요한 경우 더 많은 버전을 유지하도록 구성할 수 있습니다. UI는 100개 미만의 버전을 설정할 수 없지만 공용 API를 사용하여 더 적은 수의 버전을 저장하도록 시스템을 설정할 수 있습니다. 안정성의 경우 100보다 작은 값은 권장되지 않는 것이 며 사용자 작업으로 인해 부적절한 데이터 손실을 야기할 수 있습니다.

버전에 대한 자세한 내용은 [Versioning in SharePoint을 참조하세요.](/microsoft-365/community/versioning-basics-best-practices)

파일 복원은 SharePoint의 문서 라이브러리에서 지난 30일 동안의 두 번째 시간으로 '뒤로'로 이동하는 능력입니다. 이 프로세스를 사용하여 랜섬웨어, 대량의 지우기, 손상 또는 기타 이벤트를 복구할 수 있습니다. 이 기능은 기본 버전을 줄이면 이 복원의 효율성을 줄일 수 있도록 파일 버전을 사용 합니다.

파일 복원 기능은 [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) 및 SharePoint 둘 다에 대해 [문서화되어 있습니다.](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)

## <a name="deletion-backup-and-point-in-time-restore"></a>Deletion, backup, and Point in Time Restore

SharePoint에서 삭제된 사용자 콘텐츠는 다음과 같은 삭제 흐름을 통과합니다.

삭제된 항목은 일정 기간 동안 재활용 보관에 보관됩니다. SharePoint의 경우 보존 시간은 93일입니다. 원래 위치에서 항목을 삭제할 때 시작됩니다. 사이트 재활용 모음에서 항목을 삭제하면 사이트 모음 재활용 모음으로 [들어갑니다.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) 남은 93일 동안 이 곳을 유지한 다음 영구적으로 삭제됩니다. 재활용 쓰레기 수거란 사용 방법에 대한 자세한 내용은 다음 링크를 참조하십시오.

- [Recycle Bin의 항목 복원](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- 사이트 모음 재활용 모음에서 삭제된 [항목을 복원합니다.](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)

이 프로세스는 기본 삭제 흐름으로, 보존 정책 또는 레이블을 고려하지 않습니다. 자세한 내용은 SharePoint 및 [OneDrive의 보존에 대해 자세히를 참조하세요.](/microsoft-365/compliance/retention-policies-sharepoint)

93일 재순환 파이프라인이 완료되면 메타데이터 및 Blob Storage에 대해 독립적으로 폐기됩니다. 메타데이터는 데이터베이스에서 즉시 제거되어 백업에서 메타데이터를 복원하지 않으면 콘텐츠를 읽을 수 없습니다. SharePoint는 14일 동안의 메타데이터 백업을 유지 관리합니다. 이러한 백업은 거의 실시간으로 로컬로 수행된 다음 이 게시 당시 설명서에 따라 [](/azure/sql-database/sql-database-automated-backups) 5~10분 일정에 따라 중복 Azure Storage 컨테이너의 저장소로 푸시됩니다.

Blob Storage 콘텐츠를 삭제할 때 SharePoint는 Azure Blob Storage의 소프트 삭제 기능을 사용하여 실수로 또는 악의적인 삭제로부터 보호합니다. 이 기능을 사용하면 콘텐츠를 영구적으로 삭제하기 전까지 총 14일 동안 복원할 수 있습니다.

>[!Note]
>Microsoft 응용 프로그램에서 표준 프로세스에 대한 콘텐츠를 재활용 쓰레기통으로 보내지만 SharePoint는 재활용 쓰레기 수거통을 건너뛰고 즉시 삭제하도록 허용하는 API를 제공합니다. 응용 프로그램을 검토하여 규정 준수를 위해 필요한 경우만 이행되도록 합니다.

## <a name="integrity-checks"></a>무결성 검사

SharePoint는 다양한 방법을 사용하여 데이터 수명 주기의 모든 단계에서 Blob 및 메타데이터의 무결성을 보장합니다.

- **메타데이터에 저장된** 파일 해시: 전체 파일의 해시가 파일 메타데이터와 함께 저장되어 모든 작업 중에 문서 수준 데이터 무결성이 유지 관리됩니다.
- **메타데이터에** 저장된 Blob 해시: 각 Blob 항목은 암호화된 콘텐츠의 해시를 저장하여 Azure 저장소의 손상으로부터 보호합니다.
- **데이터 무결성 작업:** 14일마다 데이터베이스의 항목을 나열하고 Azure Storage에 나열된 Blob과 일치하여 각 사이트가 무결성을 검색합니다. 이 작업은 누락된 저장소 Blob을 보고하고 필요한 경우 [Azure 저장소](/azure/storage/blobs/soft-delete-blob-overview) 소프트 삭제 기능을 통해 해당 Blob을 검색할 수 있습니다.
