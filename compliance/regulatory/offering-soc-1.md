---
title: SOC(시스템 및 조직 컨트롤) 1 Type 2
description: Microsoft 클라우드 서비스가 운영 보안을 위해 SOC(시스템 및 조직 컨트롤) 1 Type 2 표준을 준수하는 방법을 알아봅니다.
keywords: Microsoft 365, 규정 준수, 제품
ms.localizationpriority: high
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
ms.openlocfilehash: 8c374ce340538e4030e0cd07a2bdbe0aa4f4615d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161166"
---
# <a name="system-and-organization-controls-soc-1-type-2"></a>SOC(시스템 및 조직 컨트롤) 1 Type 2

## <a name="soc-1-type-2-overview"></a>SOC 1 Type 2 개요

서비스 조직을 위한 SOC(시스템 및 조직 컨트롤)는 AICPA(American Institute of Certified Public Accountants)가 만든 내부 컨트롤 보고서입니다. SOC의 목적은 최종 사용자가 아웃소싱된 서비스와 관련된 위험을 평가하고 해결할 수 있도록 서비스 조직에서 제공하는 서비스를 검사하는 것입니다.

SOC 1 Type 2 증명은 다음에 따라 수행됩니다.

- SSAE No. 18, 증명 표준: 명확화 및 재집성(AT-C 320조 포함), *재무 보고에 관한 사용자 업체의 내부 컨트롤과 관련된 서비스 조직의 컨트롤 조사에 관한 보고*(AICPA, 전문 표준)
- 재무 보고에 관한 사용자 업체의 내부 컨트롤과 관련된 서비스 조직의 컨트롤 조사에 관한 SOC 1 보고(AICPA 가이드).

SSAE 18(Standards for Attestation Engagements 18)에 관한 AICPA Statement 외에도 Office 365 SOC 1 Type 2 감사는 ISAE 3402(International Standard on Assurance Engagements No. 3402)에 따라 수행됩니다. SOC 1 증명은 SAS 70을 대체했으며, 재무 보고에 관한 사용자 업체 내부 컨트롤과 관련된 서비스 조직의 컨트롤을 보고하는 데 적합합니다. Type 2 보고서에는 지정된 모니터링 기간 동안 관련 컨트롤 목표를 달성하기 위한 컨트롤 유효성에 대한 감사자의 의견이 포함됩니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

범위 내 Microsoft 온라인 서비스는 Azure SOC 1 Type 2 증명 보고서에 표시됩니다.

- Azure(자세한 정보는 [Microsoft Azure 규정 준수 제품](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) 또는 Azure SOC 1 Type 2 증명 보고서 참조)
- Azure DevOps(별도 Azure DevOps SOC 1 Type 2 증명 보고서 참조)
- Dynamics 365(자세한 정보는 Azure SOC 1 Type 2 증명 보고서 참조)
- Microsoft 365 Defender
- Microsoft Cloud App Security(MCAS)
- 엔드포인트용 Microsoft Defender(이전의 Microsoft Defender Advanced Threat Protection)
- Microsoft Defender for Identity(이전의 Azure Advanced Threat Protection)
- Microsoft Forms Pro(Azure Government의 경우 범위에 포함되지 않음)
- Microsoft Graph
- Microsoft Intune
- Microsoft Managed Desktop(Azure Government의 경우 범위에 포함되지 않음)
- Microsoft Stream
- Microsoft 위협 전문가(Azure Government의 경우 범위에 포함되지 않음)
- 추천 포털
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents(Azure Government의 경우 범위에 포함되지 않음)
- 업데이트 준수(Azure Government의 경우 범위에 포함되지 않음)

## <a name="azure-dynamics-365-and-soc-1"></a>Azure, Dynamics 365 및 SOC 1

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure SOC 1 제품](/azure/compliance/offerings/offering-soc-1)을 참조하세요.

## <a name="office-365-and-soc-1"></a>Office 365 및 SOC 1

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | 준수 관리자, 고객 Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox(Torus), Microsoft Teams, MyAnalytics, Office 365 고객 포털, Office 365 마이크로 서비스(Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, 학교 데이터 동기화, Siphon, Speech, StaffHub, eXtensible Application Program 등), Office Online, Office Services Infrastructure, 비즈니스용 OneDrive, Planner, PowerApps, Power BI, Project Online, 고객 키를 사용한 서비스 암호화, SharePoint Online, 비즈니스용 Skype |
| **GCC** | Azure Active Directory, 준수 관리자, Delve, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream |
| **GCC High** | Azure Active Directory, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype |
| **DoD** | Azure Active Directory, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, Power BI, SharePoint Online, 비즈니스용 Skype |

### <a name="office-365-audit-reports"></a>Office 365 감사 보고서

- [Office 365 Core - SSAE 18 SOC 1 보고서](https://aka.ms/o365SOC-1)
- 브리지 레터 및 추가 감사 보고서 참조

필요한 경우 SOC 1 및 SOC 2 증명 보고서 및 브리지 레터를 다운로드하려면 Office 365 또는 Office 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다.

### <a name="frequently-asked-questions"></a>자주 묻는 질문

**Office 365 SOC 보고서는 얼마나 자주 발행되나요?**

Office 365 및 기타 온라인 서비스에 대한 SOC 보고서는 과거 12개월 연속 실행 기간(감사 기간)을 기반으로 하고 1년에 두 번 새 보고서가 발행됩니다(기간 종료는 3월 31일과 9월 30일). 이전 3개월을 포함하는 *브리지 레터* 는 분기별로 발급됩니다. 예를 들어 1월 레터는 10월 1일~12월 31일, 4월 레터는 1월 1일~3월 31일, 7월 레터는 4월 1일~6월 30일, 10월 레터는 7월 1일~9월 30일을 포함합니다.

**고객은 Office 365 SOC 1 Type 2 증명을 어떻게 활용할 수 있나요?**

고객은 SOX(Sarbanes-Oxley), FFIEC(Federal Financial Institutions Examination Commission), GLBA(Gramm-Leach-Bliley Act) 등과 같은 자체 금융 산업별 규정 준수 요구 사항을 준수할 때 Office 365 SOC 1 Type 2 증명을 사용할 수 있습니다.

**브리지 레터를 포함하여 Office 365 SOC 감사 설명서는 어디에서 받을 수 있나요?**

감사 설명서에 대한 링크는 감사 보고서 섹션을 참조하세요. 로그인하려면 Office 365 또는 Office 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다. 그런 다음 감사 인증서, 평가 보고서 및 기타 관련 문서를 다운로드하여 자체 규정 요구 사항에 도움을 받을 수 있습니다.

**명시된 예외에 대한 관리자 응답은 어디에서 확인할 수 있나요?**

관리자 응답은 SOC 증명 보고서의 끝 부분에 있습니다. 문서에서 ‘관리자 응답’을 검색하세요.

**사용자 업체 책임은 어디에서 확인할 수 있나요?**

사용자 업체 책임은 SOC 증명 보고서의 맨 끝에 있습니다. 문서에서 ‘사용자 업체 책임’을 검색하세요.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [Service Trust Portal 감사 보고서](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SSAE No. 18, Attestation Standards: Clarification and Recodification](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)(SSAE No. 18, 증명 표준: 명확화 및 재집성)
- [SOC 1 Reporting on an Examination of Controls at a Service Organization Relevant to User Entities' Internal Control Over Financial Reporting (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-user-entities-internal-control-over-financial-reporting-soc-1-guide-OPL)(재무 보고에 관한 사용자 업체의 내부 컨트롤과 관련된 서비스 조직의 컨트롤 조사에 관한 SOC 1 보고(AICPA 가이드)(구매 가능)
