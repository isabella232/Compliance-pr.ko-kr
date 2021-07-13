---
title: NIST SP 800-171
description: Microsoft 클라우드 서비스는 비영리 정보 시스템에서 제어된 CUI(미분명 정보)를 보호하기 위한 NIST SP 800-171 지침을 준수합니다.
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
ms.openlocfilehash: 19b312d1b9f31683d775049010d390710554df01
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385668"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>NIST SP 800-171

미국 NIST(National Institute of Standards and Technology)는 연방 기관의 정보 및 정보 시스템을 보호하는 데 도움이 되는 측정 표준 및 지침을 홍보하고 유지 관리합니다. CUI(제어된 미분분 정보) 관리에 대한 행정 명령 13556에 따라 비영리 정보 시스템 및 조직에서 제어된 미분분 정보 보호인 [NIST SP 800-171을](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final) *게시했습니다.* CUI는 정부(또는 대신 엔터티)에서 만든 디지털 및 물리적 정보로 정의되어 있으며, 분류되지 않은 동안 여전히 중요하며 보호가 필요한 정보입니다.

NIST SP 800-171은 원래 2015년 6월에 게시되고 이후로 진화하는 사이버 위협에 대응하여 여러 번 업데이트되었습니다. 비연대 정보 시스템 및 조직에 CUI를 안전하게 액세스, 전송 및 저장하는 방법에 대한 지침을 제공합니다. 요구 사항은 다음과 같은 네 가지 주요 범주로 분류됩니다.

- 관리 및 보호를 위한 제어 및 프로세스
- IT 시스템 모니터링 및 관리
- 최종 사용자를 위한 명확한 사례 및 절차
- 기술적 및 물리적 보안 조치 구현

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft 및 NIST SP 800-171

공인 타사 평가 조직인 Kratos Secureinfo 및 Coalfire는 Microsoft와 협력하여 범위 내 클라우드 서비스가 *CUI를* 처리하면 NIST SP 800-171, 비연속 정보 시스템 및 조직에서 CUI(제어된 미분분 정보) 보호의 기준을 충족하는지 인증했습니다. [FedRAMP](offering-fedramp.md) 요구 사항을 Microsoft에서 구현하면 범위 내 클라우드 서비스가 이미 구현된 시스템 및 관행을 사용하여 NIST SP 800-171의 요구 사항을 충족하거나 초과하도록 보장할 수 있습니다.

NIST SP 800-171 요구 사항은 FedRAMP에서 사용하는 표준인 NIST SP 800-53의 하위 집합입니다. NIST SP 800-171의 부록 D는 범위 내 클라우드 서비스가 FedRAMP 프로그램에서 이미 평가되고 승인된 NIST SP 800-53의 관련 보안 제어에 대한 CUI 보안 요구 사항을 직접 매핑합니다.

연구 기관, 컨설팅 회사, 제조 계약자 등 미국 정부 CUI를 처리하거나 저장하는 모든 엔터티는 NIST SP 800-171의 엄격한 요구 사항을 준수해야 합니다. 이 의거는 Microsoft의 범위 내 클라우드 서비스가 Microsoft가 완전하게 준수할 것임에 따라 CUI 워크로드를 배포하기를 원하는 고객을 수용할 수 있는 것입니다. 예를 들어 정보 시스템에서 범위 내 Microsoft 클라우드 서비스를 사용하여 '적용된 방어 정보'를 처리, 저장 또는 전송하는 모든 DoD 계약자는 NIST SP 800-171의 보안 요구 사항을 준수해야 하는 미국 국방부 DFARS 조항을 충족합니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 & 서비스

- Azure Commercial, Azure Government
- Dynamics 365 미국 정부
- Intune
- Office 365 미국 정부 커뮤니티 클라우드(GCC), Office 365 GCC High 및 DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure, Dynamics 365 및 NIST SP 800-171

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure NIST SP 800-171 서비스를 참조하세요.](/azure/compliance/offerings/offering-nist-800-171)

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 및 NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 및 범위 내 서비스

다음 표를 사용하여 서비스 및 구독에 Office 365 여부를 확인할 수 있습니다.

| **적용 가능 여부** | **범위 내 서비스** |
|:------------------|:----------------------|
| **GCC** | 작업 피드 서비스, Bing 서비스, Delve, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |
| **GCC 높음** | 작업 피드 서비스, Bing 서비스, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, 
SharePoint 온라인, 비즈니스용 Skype, Windows Ink |
| **DoD** | 작업 피드 서비스, Bing 서비스, Exchange Online, 지능형 서비스, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, Microsoft Teams, SharePoint Online, 비즈니스용 Skype, Windows Ink |

### <a name="frequently-asked-questions"></a>질문과 대답

**조직에서 NIST SP 800-171과 함께 Microsoft 규정 준수를 사용할 수 있나요?**

예. Microsoft 고객은 자체 FedRAMP 및 NIST 위험 분석 및 자격 취득 노력의 일부로 FedRAMP 표준에 대한 독립적인 타사 평가 조직(3PAO)의 보고서에 설명된 감사 컨트롤을 사용할 수 있습니다. 이러한 보고서는 Microsoft가 범위 내 클라우드 서비스에서 구현한 컨트롤의 효율성을 시연합니다. 고객은 CUI 워크로드가 NIST SP 800-171 지침을 준수하는지 확인합니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [NIST 800-171 요구 사항을 충족하는 Microsoft DoD 인증](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 규정 준수가 사이버 보안 설명서로 시작](https://www.nist800171.com/)
- [Microsoft 클라우드 서비스 FedRAMP 권한 부여](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 감사 및 책임 Office 365 GCC 높음](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft 및 NIST Cybersecurity Framework](offering-nist-csf.md)
- [Microsoft Government 클라우드](https://www.microsoft.com/enterprise/government)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
