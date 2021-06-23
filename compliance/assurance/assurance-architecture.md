---
title: 아키텍처 개요
description: 2013의 아키텍처에 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9af5296cce34db6362638f025f38315f2e1d7b05
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088537"
---
# <a name="architecture-overview"></a>아키텍처 개요

## <a name="what-is-microsoft-365"></a>Microsoft 365란 무엇인가요?

Microsoft 365 클라우드 기반 구독 기반 버전의 Office, Windows 10, Enterprise Mobility + Security 준수입니다. Microsoft 365 고객은 Outlook 및 Windows 같은 클라이언트를 사용할 수 있으며 Exchange Online, Microsoft Teams 및 SharePoint Online과 같이 Microsoft가 Exchange Online 호스트하는 서비스도 SharePoint. 서비스의 모든 구성 요소는 구독 모델의 일부로 정기적으로 업데이트되어 고객이 '에버그리엔' 제품을 사용할 수 있도록 합니다. Microsoft는 고객을 대신하여 서비스 인프라를 관리합니다. 즉, Microsoft는 고객 데이터를 저장하는 인프라의 보호를 담당합니다.

규모 면에서 현재는 1백만 대에 가까운 컴퓨터를 사용하여 서비스를 Microsoft 365 있습니다. 이러한 서비스를 제공하는 인프라는 Azure, Windows 및 Linux, 다중 테넌트 및 전용 플랫폼의 서비스별 하드웨어 및 가상화된 환경에 따라 크게 다릅니다. Microsoft 365 글로벌 비즈니스로, 인프라는 전 세계 데이터 센터에 배포되어 고객이 데이터 상주 및 주권 요구 사항을 충족할 수 있도록 합니다.

즉, 서비스는 복잡하고 놀라운 규모로 실행하며 수천 명의 Microsoft 엔지니어가 빌드 및 유지 관리해야 합니다. 이 모든 인프라를 안전하게 유지하는 것이 최우선 과제입니다.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>고객 Microsoft 365 어떻게 하나요?

Microsoft의 클라우드 서비스는 모든 테넌트가 다른 모든 테넌트에 잠재적으로 적대적일 수 있는 것으로 가정하여 구축됩니다. 테넌트를 적절히 격리하기 위해 Microsoft는 다양한 격리 기술 및 제어를 구현합니다. 이러한 컨트롤은 테넌트 전체의 고객 데이터에 대한 정보 누출 또는 무단 액세스로부터 보호하고 한 테넌트의 작업이 다른 테넌트의 서비스에 부정적인 영향을 주지 않도록 방지하도록 디자인됩니다.

고객 콘텐츠는 Azure AD(Microsoft 365 사용하여 Azure Active Directory 격리됩니다. Microsoft 365 사용자 인증은 사용자 ID뿐만 아니라 사용자 계정이 있는 테넌트 ID도 확인하여 사용자가 테넌트 환경 외부의 데이터에 액세스할 수 없습니다. Azure AD의 논리적 고지를 보완하기 위해 고객 콘텐츠는 항상 미사용 및 전송 중으로 암호화됩니다. 개별 서비스는 또한 별도의 암호화된 데이터베이스에서 테넌트 데이터의 SharePoint 분리하는 등의 추가적인 테넌트 분리 계층을 제공할 수 있습니다.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>단일 Microsoft 365 방지하는 복구 서비스를 엔지니어는 어떻게 하나요?

Microsoft는 클라우드 서비스를 설계 및 구축하여 안정성을 극대화하고 정상적인 운영에 대한 장애 및 문제로 고객에게 부정적인 영향을 최소화합니다. 이 전략은 지리적으로 분산된 데이터 센터를 연결하는 네트워크 디자인에서 시작됩니다. Microsoft의 네트워크 아키텍처에는 직접 상호 연결 및 여러 네트워크 경로가 포함되어 있습니다. Microsoft 365 서비스는 이러한 중복성을 활용하여 오류와 관련한 트래픽을 자동으로 라우팅하여 서비스 품질을 향상합니다.

서비스 수준에서는 Microsoft 365 전략에 따라 소프트웨어 탄력성에 우선 순위를 지정합니다. 가능한 경우 서비스가 자동화된 서비스 상태 모니터링을 통해 활성/활성 구성에 배포되므로 사용자가 개입하지 않고도 많은 일반적인 오류 및 실패를 감지하고 복구할 수 있습니다. 활성/활성 구성 외에도 Microsoft 365 서비스가 별도의 장애 영역으로 배포되어 한 영역의 장애가 다른 영역의 가용성에 영향을 주지 않도록 하여 내결함성을 향상합니다.

데이터 탄력성은 서비스에서 데이터의 무결성과 가용성을 보호하여 서비스 Microsoft 365 보완합니다. 당사의 서비스는 로컬 저장소 중복성 및 지리적 중복을 사용하여 고객 데이터의 복사본을 다른 장애 영역으로 복제합니다. 한 장애 영역의 데이터가 손상되거나 손실된 경우 가용성 손실 없이 다른 장애 영역의 데이터에 액세스할 수 있습니다. 자동화된 무결성 검사는 다양한 종류의 물리적 또는 논리적 손상에 영향을 미치는 데이터를 자동으로 복원합니다. Microsoft 365 온라인 및 온라인에서 고객이 실수로 삭제하거나 수정한 데이터를 복원하는 Exchange Online SharePoint 제공합니다.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>어떻게 Microsoft 365 추적하고 권한이 없는 외부 시스템 연결을 방지하나요?

Microsoft 365 서비스 팀은 비즈니스 연속성 관리의 일부로 중요한 시스템 구성 요소 및 해당 종속성을 식별합니다. 또한 Microsoft 365 구성에서 권한이 부여된 연결만 허용되도록 모든 외부 시스템 연결을 문서화하고 추적합니다. Microsoft 365, 종속성 및 외부 연결은 Microsoft 365 보안 아키텍처에 설명되어 있습니다. 정보 보안 아키텍처와 해당 데이터 흐름 다이어그램은 최소한 매년 검토 및 업데이트될 뿐만 아니라 시스템이 크게 변경될 때마다 검토 및 업데이트됩니다.

Microsoft 365 아키텍처는 클라우드 기반 도구를 사용하여 정기적으로 자동으로 유효성을 검사하여 보안 원칙에 부합하는지 확인하고 지속적으로 고리 및 탄력성 기능을 테스트합니다. 아키텍처 유효성 검사는 서비스의 현재 상태가 원하는 상태로부터 밝아진 인스턴스를 자동으로 식별하여 검토 및 완화를 위해 모든 이진에 을 표시하는 작업입니다. 아키텍처 유효성 검사의 목표는 서비스 인프라의 보안 기능이 예상대로 계속 작동하도록 하는 것입니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 다음 표에서 데이터 아키텍처와 관련된 컨트롤의 유효성을 Microsoft 365.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: 정보 흐름 적용 <br> CP-9: 정보 시스템 백업 <br> PL-8: 정보 보안 아키텍처 <br> SC-7: 경계 보호 <br> SC-22: 아키텍처 및 프로비전 | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 정보 보안 구성 <br> A.13.1: 네트워크 보안 관리 <br> A.17.2: 중복 | 2021년 4월 20일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: 정보 보안 구성 <br> A.13.1: 네트워크 보안 관리 | 2021년 4월 20일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: 테넌트 고리 <br> CA-49: 백업 정책 <br> CA-51: 데이터 복제 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: 데이터 흐름 다이어그램 <br> CA-37: 테넌트 고리 <br> CA-49: 백업 정책 <br> CA-51: 데이터 복제 | 2020년 12월 24일 |