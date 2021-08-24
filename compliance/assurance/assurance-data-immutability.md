---
title: 데이터 몰입도 Microsoft 365
description: 규정 준수Microsoft 365 내부 거버넌스 요구 사항 및 소송 위험을 해결하기 위해 검색 가능한 형태로 데이터를 보존하는 방법을 확인합니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e17685c7d927ab8188abe1ef4dae4d2cdf0f3764
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482121"
---
# <a name="data-immutability-in-microsoft-365"></a>데이터 몰입도 Microsoft 365

규정 준수, 내부 거버넌스 요구 사항 또는 소송 위험은 조직에서 전자 메일 및 관련 데이터를 검색 가능한 형태로 보존해야 합니다. 시스템의 모든 데이터는 검색할 수 있어야 합니다. 삭제하거나 변경할 수 없습니다. 이 용어에 대한 업계 표준 용어는 "몰입성"입니다.

일반적으로 전자 메일 메시지를 별도의 읽기 전용 저장소 위치로 이동하여 변경하는 방법으로는 변경 작업을 할 수 있습니다. 이러한 시스템은 검색을 위해 사서함 항목을 보존하기 위한 용도로 사용하나, 사용자 지정 일별 워크플로에서 보존된 항목을 제거하여 사용자 경험에 영향을 주는 경우가 종종 있습니다. IT 전문가의 경우 이러한 몰입형 접근 방식을 사용하려면 별도의 서버 및 저장소 인프라를 배포하고 지속적인 유지 관리해야 합니다. 검색은 메일 시스템 외부의 도구를 사용하여 수행하며 관련 배포 및 유지 관리 비용을 포함합니다.

사용자 및 해당 서비스에 있는 보관의 현재 Microsoft 365 보존 및 보존 정책 기능을 통해 많은 클래스의 들어오는, 내부 및 외부 데이터를 보존하고 유지할 수 있습니다. 여기에는 다음이 포함됩니다.

- 인바운드 및 아웃바운드 전자 메일 통신
- 전자 메일 양식 또는 공유 온라인 문서에 포함된 책 및 레코드
- 모임 요청
- 팩스
- 인스턴트 메시지
- 온라인 모임 중에 공유된 문서
- 음성

또한 Microsoft는 타사 데이터 캡처 및 [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) 관리 솔루션과의 통합을 통해 다른 원본의 데이터를 보관할 수 있도록 추가 기능 기능을 개발했습니다. 타사 데이터를 가져온 후 다음을 비롯한 Microsoft 365 준수 기능을 데이터에 적용할 수 있습니다.

- [소송 대기](/microsoft-365/compliance/create-a-litigation-hold)
- [원본 위치 eDiscovery 및 유지](/microsoft-365/compliance/manage-legal-investigations)
- [규격 검색](/microsoft-365/compliance/search-for-content)
- [원본 위치 보관](/microsoft-365/compliance/enable-archive-mailboxes)
- [사서함 감사](/microsoft-365/compliance/enable-mailbox-auditing)
- [보존 정책](/microsoft-365/compliance/retention-policies)

예를 들어 사서함에 소송 보존이 설정되어 있는 경우 타사 데이터가 보존됩니다. eDiscovery 또는 준수 검색을 사용하여 타사 In-Place 검색할 수 있습니다. 또는 Microsoft 데이터에 대해와 마찬가지로 타사 데이터에 보관 및 보존 정책을 적용할 수 있습니다. 타사 데이터를 보관하는 Microsoft 365 조직은 정부 및 규제 정책을 준수하는 데 도움이 됩니다.

Microsoft 365 보관은 SEC(Securities and Exchange Commission) 규칙 17a-4 규격 저장소를 제공합니다. Microsoft 365 보존 정책 및 보존 정책(보존 잠금 포함)을 사용하여 다시 사용할 수 없는, 지울 수 없는 형식으로 수집된 모든 데이터의 영구 파일을 보존합니다.

특히 다음 사항에 유의합니다.

- 위에서 언급한 보존 정책을 사용하여 저장된 모든 레코드는 일반 사용자의 전용 저장소 영역에 보존됩니다. 권한이 부여된 사용자만 이러한 레코드에 액세스하고 검색할 수 있지만 해당 레코드를 변경하거나 지울 수는 없습니다.
- 각 항목에 대한 메타데이터에는 보존 기간 계산에 사용되는 타임스탬프가 포함됩니다. 타임스탬프는 새 항목을 수신하거나 만들 때 적용되고 메타데이터에서 수정하거나 제거할 수 없습니다.
- 보관을 Microsoft 365 여러 보존 정책을 결합하고 작업을 보존하여 세부적인 보존 정책을 만들 수 있습니다. 이러한 정책은 보존된 항목의 유형 또는 위치와 보존 기간을 정의합니다.
- 보존 잠금 기능을 사용하면 정책을 제한적인 정책으로 만들지 여부를 선택할 수 있습니다. 제한적인 정책은 모든 사용자가 보존 정책을 제거, 비활성화 또는 변경할 수 없습니다. 즉, 일단 보존 잠금을 사용하도록 설정하면 사용하지 않도록 설정할 수 없습니다. 보존 정책에 의해 수집된 기존 보유자로부터의 데이터가 보존 기간 동안 덮어되거나 수정, 삭제 또는 삭제될 수 있는 메커니즘은 존재하지 않습니다. 또한 보존 잠금에 의해 설정된 보존 기간이 단축되거나 줄어들지 않을 수 있습니다. 그러나 위에서 언급한 대로 저장된 데이터의 보존을 계속해야 하는 법적 요구 사항이 있는 경우 기간이 길어도 됩니다. 보존 잠금은 관리자나 특정 제어 권한이 있는 사용자도 설정을 변경하거나 저장된 데이터를 덮어 Microsoft 365 수 있도록 하여 2003 SEC 규칙 17a-4 릴리스에 규정된 지침에 따라 보관을 Microsoft 365 수 있도록 합니다.

규칙 Microsoft 365 특히 규칙 17a-4 요구 사항을 충족하는 데 도움이 되는 방법을 이해하기 위해 Exchange Online Archiving, SharePoint Online, 비즈니스용 OneDrive 및 비즈니스용 Skype. [](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) 또한 백서에서는 SEC 규칙 17a-4에 따라 각 요구 사항에 대해 Microsoft 365 보관 기능을 심층 분석하고 규제 대상 고객에게 Microsoft 365 보관을 통해 이러한 요구 사항을 충족할 수 있는 방법을 보여줄 수 있습니다.
