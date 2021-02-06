---
title: FedRAMP(Federal Risk and Authorization Management Program)
description: Microsoft는 미국 연방 위험 및 권한 부여 관리 프로그램 P-ATOS 및 ATOS를 부여했습니다.
keywords: Microsoft 365, 규정 준수, 제안
localization_priority: None
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
ms.openlocfilehash: ccfeb35005250b29342e8fc80c1a1b2537a09908
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120327"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>FedRAMP(Federal Risk and Authorization Management Program)

## <a name="fedramp-overview"></a>FedRAMP 개요

미국 FedRAMP(Federal Risk and Authorization Management Program)는 FISMA(Federal Information Security Management Act)에 따라 클라우드 컴퓨팅 제품 및 서비스를 평가, 모니터링 및 승인하는 표준화된 접근 방식을 제공하고 연방 기관의 보안 클라우드 솔루션 채택을 가속화하기 위해 수립되었습니다.

이제 관리국 및 예산부에서는 모든 행정 기관이 FedRAMP를 사용하여 클라우드 서비스의 보안 유효성을 검사해야 합니다. (다른 기관에서도 채택하여 공공 부문의 다른 영역에서도 유용합니다.) NIST(National Institute of Standards and Technology) SP 800-53은 필수 표준을 설정하고, 정보 시스템의 보안 범주(기밀성, 무결성 및 가용성)를 설정하여 정보 및 정보 시스템이 손상된 경우 조직에 미칠 수 있는 영향을 평가합니다. FedRAMP는 클라우드 서비스 공급자(CSP)가 해당 표준을 충족하는지 인증하는 프로그램입니다.

연방 기관에 서비스를 판매하기를 원하는 CSP는 FedRAMP 규정 준수를 입증하기 위해 세 가지 경로를 사용할 수 있습니다.

- JAB(조인트 인증 위원회)에서 P-ATO(Provisional Authority to Operate)를 획득합니다. JAB는 FedRAMP의 기본 거버넌스 및 의사 결정 규약입니다. 국방부, 국토안보부 및 일반 서비스 관리 담당자가 보드에서 일합니다. 이 보드는 FedRAMP 규정 준수를 입증한 CSP에 P-ATO를 부여합니다.
- 연방 기관으로부터 ATO(Authority to Operate)를 받을 수 있습니다.
- 또는 프로그램 요구 사항을 충족하는 CSP 제공 패키지를 개발하기 위해 독립적으로 작업합니다.

이러한 각 경로는 FedRAMP PMO(Program Management Office)에서 엄격한 기술 검토를 수행하고 프로그램에 의해 인증된 독립적인 타사 조직의 평가가 필요합니다.

FedRAMP 권한 부여는 NIST 지침(낮음, 보통, 높음)에 따라 세 가지 영향 수준으로 부여됩니다. 이러한 수준은 기밀성, 무결성 또는 가용성 손실이 조직에 미칠 수 있는 영향의 순위를 낮음(제한된 효과), 보통(심각한 부정적인 효과) 및 높음(심각한 또는 대재해성 효과)으로 순위를 정합니다.

## <a name="microsoft-and-fedramp"></a>Microsoft 및 FedRAMP

Azure Government, Dynamics 365 Government 및 Office 365 미국 정부를 비롯한 Microsoft의 정부 클라우드 서비스는 미국 연방 위험 및 권한 부여 관리 프로그램(FedRAMP)의 요구 사항을 충족하여 미국 연방 기관이 Microsoft 클라우드의 비용 절감 및 엄격한 보안을 혜택을 받을 수 있도록 합니다.

Microsoft 정부 클라우드 서비스는 공공 부문 고객에게 FedRAMP를 준수하는 다양한 서비스와 고객이 FedRAMP High 컨트롤을 구현해야 하는 Azure 배포 아키텍처에 대한 핵심 정책 집합을 배포하는 데 도움이 되는 [FedRAMP High Blueprint를](https://aka.ms/fedrampblueprint)비롯한 강력한 지침 및 구현 도구를 제공합니다.

## <a name="microsoft-azure-p-atos"></a>Microsoft Azure P-ATOs

Azure 및 Azure Government는 Azure 및 Azure Government를 사용하여 중요한 데이터를 처리하기 위해 권한을 부여하는 FedRAMP 승인을 위한 최고 표시줄인 합동 인증 위원회로부터 높은 영향 수준에서 P-ATO를 획득했습니다.

Azure 및 Azure Government의 FedRAMP 감사에는 범위 내 서비스의 인프라, 개발, 운영, 관리 및 지원을 아우를 수 있는 정보 보안 관리 시스템이 포함되어 있습니다. P-ATO가 부여된 경우 CSP에는 해당 기관이 함께 작업하는 모든 정부 기관의 권한 부여(ATO)가 필요합니다. Azure의 경우 정부 기관은 자체 보안 인증 프로세스에서 Azure P-ATO를 사용하여 FedRAMP 요구 사항을 충족하는 대리점 ATO를 발행하기 위한 기반으로 사용할 수 있습니다.

Azure는 다른 클라우드 공급자보다 FedRAMP 높은 영향 수준에서 더 많은 서비스를 계속 지원하고 있습니다. 또한 Azure 공용 클라우드의 FedRAMP High는 많은 미국 정부 고객의 요구를 충족하는 반면, 더 엄격한 요구 사항을 충족하는 기관은 Azure Government를 계속 사용하여 직원의 선고를 높이는 등의 추가 세이프가드를 제공합니다. Microsoft는 현재 Azure Government에서 사용할 수 있는 모든 [Azure](/azure/azure-government/compliance/azure-services-in-fedramp-auditscope#azure-public-services-by-audit-scope) 공용 서비스를 FedRAMP High 경계에 나열하고 현재 연도에 계획된 서비스를 나열합니다.

## <a name="microsoft-dynamics-365-us-government-ato"></a>Microsoft Dynamics 365 미국 정부 ATO

Dynamics 365 미국 정부는 미국 HUD(도시 및 도시 개발부)에서 높은 영향 수준에서 FedRAMP Agency ATO를 부여했습니다. 인증 범위는 정부 커뮤니티 클라우드로 제한되어 있습니다. Dynamics 365 미국 정부 비즈니스 및 엔터프라이즈 계획은 동일한 엄격한 FedRAMP 제어 집합을 따라 운영됩니다.

## <a name="microsoft-office-365-and-office-365-us-government-atos"></a>Microsoft Office 365 및 Office 365 미국 정부 ATOS

- Office 365 및 Office 365 미국 정부에는 미국 보건부(DHHS)의 ATO가 있습니다.
- Office 365 U.S. Government Defense에는 미국 DISA(Defense Information Systems Agency)의 P-ATO가 있습니다. Office 365 U.S. Government Defense를 배포하고자 하는 고객은 DISA P-ATO를 사용하여 기관 ATO를 생성하여 승인을 문서화할 수 있습니다.
- Office 365(엔터프라이즈 및 비즈니스 요금제) 및 Office 365 미국 정부는 검사기 일반 DHHS 사무실의 중간 영향 수준에서 FedRAMP 기관 ATO를 가급적 습니다. Office 365 미국 정부는 이 인증을 획득한 첫 번째 클라우드 기반 전자 메일 및 공동 작업 서비스입니다.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 범위 내 클라우드 서비스

- [Azure 및 Azure Government](https://go.microsoft.com/fwlink/p/?linkid=2095323)
- [Dynamics 365 미국 정부](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 및 Office 365 미국 관리](https://go.microsoft.com/fwlink/p/?linkid=2077751)
- Office 365 US Government Defense
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스
- Microsoft Defender ATP

> [!NOTE]
> Azure Government 내에서 Azure Active Directory를 사용하려면 Azure 공용 클라우드에서 Azure Government 외부에 배포되는 구성 요소를 사용해야 합니다.

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

Microsoft는 P-ATOs 및 ATOs를 유지하기 위해 매년 클라우드 서비스를 재인증해야 합니다. 이를 위해 Microsoft는 보안 제어를 지속적으로 모니터링하고 평가하고 서비스 보안이 규정을 준수하는지 입증해야 합니다.

- [Microsoft 클라우드 서비스 FedRAMP 권한 부여</span>](https://marketplace.fedramp.gov/#/product/azure-government?sort=productName&productNameSearch=azure)
- [Microsoft FedRAMP 감사 보고서</span>](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

다른 FedRAMP 보고서를 받으면 Azure 연방 설명서로 [전자 메일을 보내야 합니다.](mailto:AzFedDoc@microsoft.com)

## <a name="quickly-deploy-your-fedramp-solutions-on-azure-government"></a>Azure Government에 FedRAMP 솔루션을 신속하게 배포

Microsoft에서 ATO 프로세스를 안내하고 FedRAMP High Blueprint를 사용하여 FedRAMP 솔루션을 신속하게 배포할 수 있도록 하여 고객이 FedRAMP High 컨트롤을 구현해야 하는 Azure 배포 아키텍처에 대한 핵심 정책 집합을 구현하는 데 도움이 됩니다.

[Azure FedRAMP High Blueprint 사용 시작](https://aka.ms/fedrampblueprint)

## <a name="frequently-asked-questions"></a>자주 묻는 질문

**Microsoft 클라우드 서비스가 FISMA(Federal Information Security Management Act)를 준수하나요?**

FISMA는 미국 연방 기관 및 해당 파트너가 FISMA 요구 사항을 준수하는 조직에서만 정보 시스템 및 서비스를 조달해야 하는 연방법입니다. FISMA 규격으로 표시하는 대부분의 기관 및 해당 공급업체는 특수 발행물 800-53개 참조 4에서 NIST로 식별된 컨트롤을 충족하는 방법을 참조합니다. FISMA 프로세스(단, 기준 자체는 아미르)는 2011년 FedRAMP로 대체되었습니다.

**FedRAMP는 누구에게 적용하나요?**

'FedRAMP is mandatory for federal agency cloud deployments and service models at the low and moderate risk impact levels.' CSP에 참여하려는 연방 기관은 FedRAMP 사양을 충족해야 할 수 있습니다. 또한 연방 정부에서 사용하는 제품 또는 서비스에서 클라우드 기술을 사용하는 회사는 ATO를 획득해야 할 수 있습니다.

**기관에서 자체 규정 준수 노력을 어디에서 시작하나요?**

FedRAMP를 탐색하고 해당 요구 사항을 충족하기 위해 연방 기관이 취해야 하는 단계에 대한 개요를 확인하려면 [권한 부여: 기관](https://www.fedramp.gov/agency-authorization/)인증으로 이동합니다.

**기관의 인증 프로세스에서 Microsoft 규정 준수를 사용할 수 있나요?**

예. 연방 정부 기관의 ATO가 필요한 프로그램 또는 이니셔티브의 기초로 Microsoft 클라우드 서비스의 인증을 사용할 수 있습니다. 그러나 이러한 서비스 외부의 구성 요소에 대한 자체 권한 부여를 달성해야 합니다.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [Federal Risk and Authorization Management Program](https://www.fedramp.gov/)
- [FedRAMP 보안 평가 프레임워크](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Microsoft의 클라우드에서 규정 준수 관리](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government 클라우드](https://go.microsoft.com/fwlink/p/?linkid=2087246)
- [Azure 규정 준수 제품](https://aka.ms/azurecompliance)
