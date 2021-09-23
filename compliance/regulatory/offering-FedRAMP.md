---
title: FedRAMP(Federal Risk and Authorization Management Program)
description: Microsoft는 미국 연방 위험 및 권한 부여 관리 프로그램 P-ATOS 및 ATOS를 부여했습니다.
keywords: Microsoft 365, 규정 준수, 제안
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 36e3ddb58a61bc3a0a14a300e15f22262027fc92
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486345"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>FedRAMP(Federal Risk and Authorization Management Program)

## <a name="fedramp-overview"></a>FedRAMP 개요

미국 FedRAMP(Federal Risk and Authorization Management Program)는 FISMA(Federal Information Security Management Act)에 따라 클라우드 컴퓨팅 제품 및 서비스를 평가, 모니터링 및 인증하기 위한 표준화된 접근 방식을 제공하고 연방 기관의 보안 클라우드 솔루션 채택을 가속화하기 위해 설립되었습니다.

이제 Office 및 예산을 관리하고 예산을 세우려면 모든 정부 기관이 FedRAMP를 사용하여 클라우드 서비스의 보안 유효성을 검사해야 합니다. (다른 기관에서도 채택하고 있으므로 공공 부문의 다른 영역에서도 유용합니다.) NIST(National Institute of Standards and Technology) SP 800-53은 필수 표준을 설정하고, 정보 시스템의 보안 범주(기밀성, 무결성 및 가용성)를 설정하여 정보 및 정보 시스템이 손상된 경우 조직에 미칠 수 있는 영향을 평가합니다. FedRAMP는 클라우드 서비스 공급자(CSP)가 해당 표준을 충족하는지 인증하는 프로그램입니다.

연방 기관에 서비스를 판매하기를 원하는 CSP는 FedRAMP 규정 준수를 입증하기 위해 세 가지 경로를 사용할 수 있습니다.

- JAB(합동 인증 위원회)에서 P-ATO(Provisional Authority to Operate)를 획득합니다. JAB는 FedRAMP의 기본 거버넌스 및 의사 결정 본문입니다. 국방부, 국토안보부 및 일반 서비스 관리 담당자가 보드에서 일합니다. 이 보드는 FedRAMP 규정 준수를 입증한 CSP에 P-ATO를 부여합니다.
- 연방 기관에서 ATO(운영 권한)를 받을 수 있습니다.
- 또는 독립적으로 프로그램 요구 사항을 충족하는 CSP 제공 패키지를 개발합니다.

이러한 각 경로를 사용하려면 FedRAMP PMO(프로그램 관리 Office)에서 엄격한 기술 검토를 수행하고 프로그램에 의해 인증된 독립적인 타사 조직의 평가가 필요합니다.

FedRAMP 권한 부여는 NIST 지침(낮음, 보통, 높음)에 따라 세 가지 영향 수준에서 부여됩니다. 이러한 수준은 기밀성, 무결성 또는 가용성 손실이 조직에 미칠 수 있는 영향의 순위를 낮음(제한된 효과), 보통(심각한 부정적인 영향) 및 높음(심각한 또는 재난적 효과)으로 순위를 높입니다.

## <a name="microsoft-and-fedramp"></a>Microsoft 및 FedRAMP

Azure Government, Dynamics 365 Government 및 Office 365 미국 정부를 비롯한 Microsoft의 정부 클라우드 서비스는 미국 연방 위험 및 권한 부여 관리 프로그램(FedRAMP)의 요구 사항을 충족하여 미국 연방 기관이 Microsoft 클라우드의 비용 절감 및 엄격한 보안을 활용하는 데 도움이 됩니다.

Microsoft 정부 클라우드 서비스는 공공 부문 고객에게 FedRAMP를 준수하는 다양한 서비스와 [FedRAMP High Blueprint를](https://aka.ms/fedrampblueprint)비롯한 강력한 지침 및 구현 도구를 제공합니다. 이 도구는 고객이 FedRAMP High 컨트롤을 구현해야 하는 Azure 배포 아키텍처에 대한 핵심 정책 집합을 배포하는 데 도움이 됩니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure 및 Azure Government
- [Dynamics 365 미국 정부](https://aka.ms/d365-compliance-list)
- Intune
- Office 365 미국, 미국, Office 365- High, Office 365 미국 정부방부
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스

## <a name="azure-dynamics-365-and-fedramp"></a>Azure, Dynamics 365 및 FedRAMP

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure FedRAMP 서비스를 참조하세요.](/azure/compliance/offerings/offering-fedramp)

## <a name="office-365-and-fedramp"></a>Office 365 및 FedRAMP

- Office 365 및 Office 365 미국 정부는 미국 DHHS(보건복지부)의 ATO가 있습니다.
- Office 365 미국 국방부에는 DISA(미국방부 정보 시스템 기관)의 P-ATO가 있습니다. 미국 Office 365 배포하고자 하는 모든 고객은 DISA P-ATO를 사용하여 기관 ATO를 생성하여 승인을 문서화할 수 있습니다.
- Office 365(기업 및 비즈니스 요금제) 및 Office 365 DHHS 일반의 중간 영향 수준에 FedRAMP 기관 ATO가 Office 있습니다. Office 365 미국 정부는 이 인증을 획득한 첫 번째 클라우드 기반 전자 메일 및 공동 작업 서비스입니다.

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **GCC** | 작업 피드 서비스, Bing 서비스, 예약, Delve, Exchange Online, Exchange Online Protection, 인프라, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office 온라인, Office 서비스, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |
| **GCC High** | 작업 피드 서비스, Bing 서비스, 예약, Exchange Online, Exchange Online Protection, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |
| **DoD** | 작업 피드 서비스, Bing 서비스, 예약, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 감사, 보고서 및 인증서

Microsoft는 P-ATOs 및 ATOs를 유지하기 위해 매년 클라우드 서비스를 재인증해야 합니다. 이를 위해 Microsoft는 보안 제어를 지속적으로 모니터링하고 평가하고, 서비스의 보안이 규정을 준수하는지 입증해야 합니다.

- [Microsoft FedRAMP 감사 보고서](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a>질문과 대답

**Microsoft 클라우드 서비스가 FISMA(Federal Information Security Management Act)를 준수하나요?**

FISMA는 미국 연방 기관 및 해당 파트너가 FISMA 요구 사항을 준수하는 조직에서만 정보 시스템 및 서비스를 조달해야 하는 연방 법률입니다. FISMA 준수를 나타내는 대부분의 기관 및 공급업체는 특수 발행물 800-53 rev 4에서 NIST로 식별된 컨트롤을 충족하는 방법을 참조합니다. FISMA 프로세스(기본적으로 표준 자체는 아는 경우)는 2011년 FedRAMP로 대체되었습니다.

**FedRAMP는 누구에게 적용하나요?**

'FedRAMP is mandatory for federal agency cloud deployments and service models at the low and moderate risk impact levels.' CSP에 참여하려는 연방 기관은 FedRAMP 사양을 충족해야 할 수 있습니다. 또한 연방 정부에서 사용하는 제품 또는 서비스에서 클라우드 기술을 사용하는 회사에서 ATO를 획득해야 할 수 있습니다.

**기관에서 자체 규정 준수 노력은 어디에서 시작하나요?**

FedRAMP를 성공적으로 탐색하고 해당 요구 사항을 충족하기 위해 연방 기관이 취해야 하는 단계에 대한 개요를 확인하려면 [Get Authorized: Agency Authorization 로 이동하세요.](https://www.fedramp.gov/agency-authorization/)

**기관의 인증 프로세스에서 Microsoft 규정 준수를 사용할 수 있나요?**

예. 연방 정부 기관의 ATO가 필요한 프로그램 또는 이니셔티브의 기초로 Microsoft 클라우드 서비스의 인증을 사용할 수 있습니다. 그러나 이러한 서비스 외부의 구성 요소에 대한 자체 권한 부여를 달성해야 합니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [Federal Risk and Authorization Management Program](https://www.fedramp.gov/)
- [FedRAMP 보안 평가 프레임워크](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Microsoft의 클라우드에서 규정 준수 관리](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government 클라우드](https://go.microsoft.com/fwlink/p/?linkid=2087246)
