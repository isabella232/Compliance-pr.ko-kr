---
title: FFIEC(연방 금융 기관 검사 위원회)
description: Microsoft는 금융 서비스 클라이언트가 FFIEC(연방 금융 기관 검사 위원회)의 감사 요구 사항을 준수할 수 있습니다.
keywords: Microsoft 365, 규정 준수, 제품
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
ms.openlocfilehash: 7cdc024d19ce0753d3d0c0e5cf45b6276939d6f2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948285"
---
# <a name="federal-financial-institutions-examination-council-ffiec"></a>FFIEC(연방 금융 기관 검사 위원회)

## <a name="ffiec-overview"></a>FFIEC 개요

FFIEC(연방 금융 기관 검사 위원회)는 미국의 금융 기관에 대한 미국 연방 정부 검사를 담당하는 5개의 은행 규제 기관으로 이체된 공식적인 중간 위원회입니다. FFIEC 검사자 교육 Office 기관의 현장 검사용 IT 검사 핸드북을 게시합니다.

[FFIEC](https://ithandbook.ffiec.gov/it-booklets/audit.aspx) 감사 IT 검사 지침에는 이러한 검사자가 금융 기관과 TSP 모두의 IT 감사 프로그램의 품질과 효율성을 평가하기 위한 지침이 포함되어 있습니다. 특히 독립 감사 보고서의 예로 AICPA(American Institute of Certified Public Accountants)의 SOC 1, SOC 2 및 SOC 3 증명 보고서에 대한 언급이 포함되어 있습니다. 그러나 FFIEC는 금융 기관이 이러한 보고서에 포함된 정보만 사용하는 것이 아니라 [FFIEC](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)아웃소싱 기술 서비스 IT 검사 핸드북에 자세히 설명된 확인 및 모니터링 절차를 사용하는 것이 좋습니다.

## <a name="microsoft-and-ffiec"></a>Microsoft 및 FFIEC

Microsoft Azure Microsoft Power BI 및 Microsoft Office 365 금융 서비스 기관에 클라우드 서비스를 제공하는 엄격한 요구 사항을 충족하기 위해 구축되었습니다. Azure는 금융 기관에 SOC 1 유형 2, SOC 2 유형 2 및 고객이 자체 FFIEC 규정 준수 의무를 충족하는 데 도움을 줄 수 있도록 독립적인 감사 회사에서 생성한 SOC 3 확증 보고서를 제공합니다. 예를 들어 [SOC 1 유형 2는](./offering-soc-1.md) 다음에 따라 수행됩니다.

- SSAE No. 18, 증명 표준: 명확화 및 재집성(AT-C 320조 포함), *재무 보고에 관한 사용자 업체의 내부 컨트롤과 관련된 서비스 조직의 컨트롤 조사에 관한 보고*(AICPA, 전문 표준)
- 재무 보고에 관한 사용자 업체의 내부 컨트롤과 관련된 서비스 조직의 컨트롤 조사에 관한 SOC 1 보고(AICPA 가이드).

AICPA SSAE 18 표준은 SAS 70을 대체하며, 재무 보고에 대한 사용자 엔터티 내부 제어와 관련된 서비스 조직의 컨트롤에 대한 보고에 적절합니다. 이는 금융 기관이 Azure에 배포된 자산에 대한 자체 FFIEC 특정 규정 준수 의무를 추구할 때 기술 서비스 공급자의 타사 검토를 활용할 수 있는 공식 감사입니다. 여기에는 지정된 모니터링 기간 동안 관련 제어 목표를 달성하기 위한 제어 효율성에 대한 감사자 의견이 포함됩니다.

또한 Azure는 금융 기관이 Azure 서비스를 기준으로 수행하려는 위험 평가를 Excel 위한 Excel 기반의 클라우드 보안 진단 도구를 개발했습니다. 이 도구는 FFIEC IT 검사 핸드북을 포함하여 관련 표준 및 금융 서비스 관련 규정에 설정된 요구 사항을 식별하는 19개의 개별 도메인이 있는 스프레드시트를 기반으로 합니다.  위험 평가 도구는 Azure가 클라우드 서비스 공급자에 적용되는 요구 사항을 준수하는 방법에 대한 설명으로 미리 채워지며, 고객이 자체 FFIEC 규정 준수 요구 사항을 충족하도록 지원할 수 있습니다.

또한 고객이 Azure 서비스 사용에 대한 지침과 FFIEC 요구 사항을 준수하기 위한 고려 사항을 제공하는 Azure FFIEC 클라우드 보안 진단 통합 문서 도우미도 제공됩니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure
- Intune
- Office 365 Office 365 미국 정부
- Power BI 클라우드 서비스(독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태)

## <a name="azure-guidance-documents"></a>Azure 지침 문서

클라우드 채택에 대한 FFIEC 감독을 준수하는 금융 기관을 지원하기 위해 Microsoft는 서비스 신뢰 포털 데이터 보호 리소스 [-](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3) 규정 준수 가이드 섹션에서 다운로드할 수 있는 다음 지침 문서를 게시했습니다.

- Azure - 클라우드 보안 진단 도구
- Azure - FFIEC 클라우드 보안 진단 통합 문서 도우미

## <a name="office-365-and-ffiec"></a>Office 365 및 FFIEC

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | Azure Active Directory, Azure Information Protection, Bookings, 준수 관리자, Delve, Exchange Online, Exchange Online Protection, Forms, Kaizala, Microsoft Analytics, Microsoft Booking, Office 365용 Microsoft Defender, Microsoft Graph, Microsoft Teams, 웹용 Microsoft To-Do, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 Cloud App Security, Office 365 그룹, Office 365 보안 및 준수 센터, Office 365 비디오, Office 온라인, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, StaffHub, Stream, Sway, Yammer Enterprise |
| **GCC** | Azure Active Directory, 준수 관리자, Delve, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 감사, 보고서 및 인증서

SOC Office 365 보고서를 참조합니다.

### <a name="frequently-asked-questions"></a>자주 묻는 질문

**SoC 표준에 대한 Microsoft 규정 준수를 사용하여 기관에 대한 FFIEC 규정 준수 의무를 충족할 수 있나요?**

이러한 의무를 충족할 수 있도록 Microsoft는 위에서 설명한 SOC 표준 준수에 대한 구체적인 정보를 제공합니다. 그러나 궁극적으로, 서비스가 해당 기관에 적용되는 특정 법률 및 규정을 준수하는지 여부는 사용자가 결정해야 합니다. 또한 FFIEC는 '감사 보고서 또는 검토의 사용자는 보고서에 포함된 정보만 사용하여 TSP의 내부 제어 환경을 확인하면 안 됩니다. FFIEC IT 검사 핸드북의 아웃소싱 [](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx) 기술 책자에서 보다 완벽하게 설명한 다른 확인 및 모니터링 절차를 따라야 합니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [FFIEC(연방 금융 기관 검사 위원회)](https://www.ffiec.gov/)
- [미국의 클라우드 컴퓨팅 및 규제 원칙의 규정 준수 맵](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [FFIEC 감사 IT 검사 핸드북](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)
- [FFIEC 아웃소싱 기술 서비스 IT 검사 핸드북](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)

## <a name="other-microsoft-resources-for-financial-services"></a>금융 서비스에 대한 기타 Microsoft 리소스

- [Azure 규정 준수 문서](/azure/compliance/)
- [Azure는 규정 준수의 세계를 구현합니다.](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Microsoft 클라우드 금융 서비스 리소스](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Microsoft 클라우드 금융 서비스 준수 프로그램](https://aka.ms/FSCP-Print)
- [Microsoft 클라우드의 금융 기관을 위한 위험 평가 및 규정 준수 가이드](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [금융 서비스 산업 사용 사례](/azure/industry/financial/)
