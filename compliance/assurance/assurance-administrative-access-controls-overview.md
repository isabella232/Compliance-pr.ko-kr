---
title: 2016의 관리 액세스 Microsoft 365
description: 이 문서에서는 관리 액세스 제어 및 데이터 분류에 대한 개요를 Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06bdd239e2845d3495a40fc83bd33cbb0e43dbdb3d025bd8fa77b5d5451a680c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289266"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>2016의 관리 액세스 Microsoft 365 

Microsoft는 Microsoft의 고객 콘텐츠에 대한 액세스를 의도적으로 제한하면서 대부분의 Microsoft 365 작업을 자동화하는 시스템 및 제어에 많은 투자를 했습니다. 인간은 서비스를 관리하고 소프트웨어는 서비스를 운영합니다. 이 구조를 통해 Microsoft는 대규모로 Microsoft 365 관리하고 고객 콘텐츠에 대한 내부 위협 위험을 관리할 수 있습니다.

기본적으로 Microsoft 엔지니어는 0인치 관리 권한과 고객 콘텐츠에 대한 액세스 권한이 Microsoft 365. Microsoft 엔지니어는 제한된 기간 동안 고객 콘텐츠에 대한 액세스 권한을 제한, 감사 및 보호할 수 있습니다. 액세스는 서비스 작업에 필요한 경우와 Microsoft 고위 관리 구성원이 승인한 경우만 해당됩니다. 고객 Lockbox 사용이 허가된 고객의 경우 고객은 고객이 라이선스를 통해 호스팅되는 콘텐츠에 대한 액세스 승인을 Microsoft 365.

Microsoft는 여러 형태의 클라우드 배달을 사용하여 온라인 서비스를 제공합니다.

- **공용 클라우드:** 북미, Microsoft 365, 유럽, 아시아, 오스트레일리아 등에서 호스트되는 기타 서비스, Azure의 다중 테넌트 버전을 포함합니다.
- **국가 클라우드:** 중국의 Microsoft 365(21Vianet에서 운영) 및 독일의 Microsoft 365(Microsoft에서 운영하지만 독일 데이터 수탁자인 독일어 데이터 수탁자인 독일어 Telekom)는 고객 데이터를 포함하는 고객 데이터 및 시스템에 대한 Microsoft의 액세스를 제어하고 모니터링하는 모델에 따라 이전에 언급한 클라우드를 제외한 모든 주권자 및 타사 운영 클라우드를 포함합니다.
- **정부 클라우드:** 미국 Microsoft 365 사용할 수 있는 Microsoft 365 Azure 서비스가 포함됩니다.

이 문서에서는 다음과 같은 Microsoft 365 서비스를 제공합니다.

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [비즈니스용 OneDrive](/OneDrive/onedrive)
- [비즈니스용 Skype](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365 액세스 제어

액세스 제어를 위해 Microsoft는 고객 Microsoft 365 다른 유형의 데이터로 분류합니다.

### <a name="customer-data"></a>고객 데이터

고객 데이터는 고객 서비스를 사용할 때 고객이 제공하거나 고객을 Microsoft 365 데이터입니다. 이 데이터는 다음을 포함하여 Microsoft 365 사용자가 직접 만들거나 업로드하는 고객 콘텐츠입니다.

- 전자 메일
- SharePoint 온라인 콘텐츠
- 인스턴트 메시지
- 일정 항목
- 문서
- 대화 상대
- EUII(최종 사용자 식별 정보)(사용자에게 고유하거나 개별 사용자에게 연결 가능하지만 고객 콘텐츠는 포함하지 않는 데이터)

### <a name="other-types-of-data"></a>기타 데이터 형식

기타 데이터 형식은 다음과 같습니다.

- **계정 데이터:** 관리 데이터(관리자가 서비스를 등록하거나 구매할 때 제공한 정보) 및 결제 데이터(신용 카드 세부 정보 등 결제 수단에 대한 정보)가 포함됩니다.
- **조직 식별이 가능한 정보:** 테넌트, 사용 현황 데이터를 식별하는 데 사용되는 데이터를 포함하며 개별 사용자 또는 고객 콘텐츠에 포함될 수 없습니다.
- **시스템 메타데이터:** 구성 설정, 시스템 상태, Microsoft IP 주소 및 구독 및 테넌트에 대한 기술 정보를 포함하는 서비스 로그를 포함합니다.

Microsoft는 고객 데이터 또는 액세스 제어 데이터에 대한 승인되지 않은 액세스 권한을 아무도 가지지 않도록 액세스 제어 메커니즘을 설정했습니다. 액세스 제어 데이터는 고객 콘텐츠 또는 EUII, Microsoft 암호, 보안 인증서 및 기타 인증 관련 데이터에 대한 액세스를 포함하여 환경 내의 다른 유형의 데이터 또는 기능에 대한 액세스를 관리합니다. 또한 액세스 제어 메커니즘은 프로덕션 환경에 대한 승인되지 않은 물리적, 논리적 또는 원격 액세스를 Microsoft 365 보호합니다.

Microsoft에서 운영 체제를 운영하는 데 사용하는 액세스 제어에는 다음 세 가지 범주가 Microsoft 365.

- 격리 제어
- 직원 제어
- 기술 제어

이러한 컨트롤을 결합하면 이러한 컨트롤이 통합된 작업에서 악의적인 작업을 방지하고 감지하는 데 Microsoft 365. Microsoft에서 사용하는 통제, 직원 및 기술 컨트롤 외에도 네 번째 범주의 제어가 있습니다. 즉, 고객이 구현하는 컨트롤입니다.

Microsoft 365 사용하여 데이터를 관리할 수 있는 방법은 데이터 관리 방식과 동일합니다. 조직에 등록하는 Microsoft 365 자동으로 전역 관리자가 됩니다. 전역 관리자는 관리 포털의 모든 기능에 액세스할 수 있으며 다음을 할 수 있습니다.

- 사용자 만들기 또는 편집
- 다른 사용자에게 관리자 역할 할당
- 사용자 암호 다시 설정
- 사용자 라이선스 관리
- 도메인 관리
- 고객 Lockbox 요청 승인

각 조직에서는 관리자 계정을 두 개 이상 구성하는 것이 좋습니다. 대기업 조직의 경우 다양한 기능을 하는 특수한 관리자 계정을 추천합니다.

관리자 역할 및 사용 권한을 할당하는 데 대한 자세한 내용은 [관리자](/microsoft-365/admin/add-users/assign-admin-roles) 역할 할당 및 관리자 역할 [정보를 참조하세요.](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>관련 링크

- [Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft 사전 고용 차단](assurance-pre-employment-screening.md)
- [Microsoft 클라우드 백그라운드 검사](assurance-cloud-background-check.md)
- [액세스 제어 모니터링 및 감사](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise 액세스 제어](assurance-yammer-enterprise-access-controls.md)
