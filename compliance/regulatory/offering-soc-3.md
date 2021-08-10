---
title: SOC(시스템 및 조직 컨트롤) 3
description: Microsoft 클라우드 서비스가 운영 보안을 위해 SOC(시스템 및 조직 컨트롤) 3 표준을 준수하는 방법을 알아봅니다.
keywords: Microsoft 365, 규정 준수, 제품
localization_priority: Priority
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
ms.openlocfilehash: 738970a410baa8f76334d026bd778c8a1f05b4546c85b9c1157e653f401476e0
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54294275"
---
# <a name="system-and-organization-controls-soc-3"></a>SOC(시스템 및 조직 컨트롤) 3

## <a name="soc-3-overview"></a>SOC 3 개요

서비스 조직을 위한 SOC(시스템 및 조직 컨트롤)는 AICPA(American Institute of Certified Public Coordinators)가 만든 내부 제어 보고서입니다. 최종 사용자가 아웃소스한 서비스와 관련된 위험을 평가하고 해결할 수 있도록 서비스 조직에서 제공하는 서비스를 검사하기 위한 것입니다.

*서비스 조직을 위한 SOC 3 SOC: 일반 사용 보고서* 를 위한 Trust Services Criteria는 보안, 상태, 처리 무결성, 기밀성 또는 개인 정보와 관련된 서비스 조직 컨트롤에 대한 보증이 필요하지만 전체 SOC 2 보고서가 필요하지 않은 사용자를 위한 간단한 공개 버전의 SOC 2 유형 2 증명 보고서입니다. SOC 3 보고서는 일반적인 사용 보고서이므로 자유롭게 배포할 수 있습니다.

SOC 3 보고서는 적용 가능한 Trust Services Criteria에 따라 약정을 이행하기 위한 컨트롤 효율성과 관련된 서비스 조직 관리자의 서면 어설션과 관리의 어설션이 공평하게 명시되었는지에 대한 서비스 감사자의 의견을 포함합니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

Microsoft 범위 내 서비스는 Azure [SOC 2 유형 2 증명](offering-soc-2.md) 보고서에서 확인할 수 있습니다.

- Azure(자세한 정보는 [Microsoft Azure 규정 준수 제품](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) 또는 Azure SOC 2 Type 2 증명 보고서 참조)
- Dynamics 365(자세한 정보는 Azure SOC 2 Type 2 증명 보고서 참조)
- Microsoft 365 Defender
- Microsoft Cloud App Security(MCAS)
- 엔드포인트용 Microsoft Defender
- ID용 Microsoft Defender
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

## <a name="azure-dynamics-365-and-soc-3"></a>Azure, Dynamics 365 및 SOC 3

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure SOC 3 제품](/azure/compliance/offerings/offering-soc-3)을 참조하세요.

## <a name="office-365-and-soc-3"></a>Office 365 및 SOC 3

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **Office 365** | 준수 관리자, 고객 Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox(Torus), Microsoft Teams, MyAnalytics, Office 365 고객 포털, Office 365 마이크로 서비스(Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, 학교 데이터 동기화, Siphon, Speech, StaffHub, eXtensible Application Program 등), Office Online, Office 서비스 인프라, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, Project Online, 고객 키를 사용한 서비스 암호화, SharePoint Online, 비즈니스용 Skype |
| **GCC** | Azure Active Directory, 준수 관리자, Delve, Exchange Online, 
, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream |
| **GCC High** | Azure Active Directory, Exchange Online, Flow, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype |
| **DoD** | Azure Active Directory, Exchange Online, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype |

### <a name="office-365-audit-reports"></a>Office 365 감사 보고서

- [Office 365 Core - SSAE 18 SOC 3 보고서](https://aka.ms/o365SOC-3)
- [브리지 레터 및 추가 감사 보고서 참조](https://aka.ms/auditreports)

필요한 경우 SOC 1 및 SOC 2 증명 보고서 및 브리지 레터를 다운로드하려면 Office 365 또는 Office 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다.

### <a name="frequently-asked-questions"></a>자주 묻는 질문

**Office 365 SOC 보고서는 얼마나 자주 발행되나요?**

Office 365 및 기타 온라인 서비스에 대한 SOC 보고서는 과거 12개월 연속 실행 기간(감사 기간)을 기반으로 하고 1년에 두 번 새 보고서가 발행됩니다(기간 종료는 3월 31일과 9월 30일). 이전 3개월을 포함하는 *브리지 레터* 는 분기별로 발급됩니다. 예를 들어 1월 레터는 10월 1일~12월 31일, 4월 레터는 1월 1일~3월 31일, 7월 레터는 4월 1일~6월 30일, 10월 레터는 7월 1일~9월 30일을 포함합니다.

**브리지 레터를 포함하여 Office 365 SOC 감사 설명서는 어디에서 받을 수 있나요?** 감사 문서 링크는 감사 보고서 섹션을 참조하세요. 로그인하려면 Office 365 또는 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다. 그런 다음 감사 인증서, 평가 보고서 및 기타 관련 문서를 다운로드하여 자체 규정 요구 사항에 도움을 받을 수 있습니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [Service Trust Portal 감사 보고서](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [AICPA SOC for Service Organizations](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)(서비스 조직을 위한 AICPA SOC)
- [SSAE No. 18, Attestation Standards: Clarification and Recodification (AICPA Professional Standards)](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)(SSAE No. 18, 증명 표준: 명확화 및 재집성(AICPA 전문 표준)
- [SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL)(보안, 가용성, 처리 무결성, 기밀성 또는 개인 정보 보호와 관련된 서비스 조직의 컨트롤 조사에 관한 SOC 2 보고(AICPA 가이드)(구매 가능)
- [TSP section 100 (AICPA, 2017 Trust Services Criteria)](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)(TSP 100조(AICPA, 2017 트러스트 서비스 기준)
