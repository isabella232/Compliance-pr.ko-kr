---
title: ISO/IEC 27017:2015 정보 보안 통제를 위한 규약
description: Microsoft 클라우드 서비스는 정보 보안 통제를 위해 이 규약을 구현했습니다.
keywords: Microsoft 365, 규정 준수, 제안
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
ms.openlocfilehash: b17c7629918bdf4386ad24d28c6cb6687728603c
ms.sourcegitcommit: deff41bc5085d0da42c33dd6d1672be0724a067c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2021
ms.locfileid: "58561356"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 정보 보안 통제를 위한 규약

## <a name="iso-iec-27017-overview"></a>ISO-IEC 27017 개요

ISO/IEC 27017:2015 규약은 조직에서 ISO/IEC 27002:2013에 기초한 클라우드 컴퓨팅 정보 보안 관리 시스템을 구축할 때 클라우드 서비스 정보 보안 통제를 선택하기 위해 참조로 사용하도록 고안된 것입니다. 또한 클라우드 서비스 공급자의 경우, 일반적으로 승인되는 보호 통제 장치를 구축하기 위한 지침 문서로 사용할 수도 있습니다.

이 국제 표준은 ISO/IEC 27002에 기초한 클라우드 구현 지침을 추가로 제공하고, 규제, 구현 지침 및 기타 정보에 대한 ISO/IEC 27002: 2013 의 5항부터 18항과 관련하여 클라우드 정보 보안 위협과 위험을 해결하기 위한 추가 규제를 제공합니다. 특히 이 표준은 ISO/IEC 27002의 37개 규제에 대한 지침을 제공하며, ISO/IEC 27002에 중복되지 않은 7가지의 새로운 규제를 특별히 포함합니다. 이러한 새 규제는 다음과 같은 중요 영역에 대한 것입니다.

- 클라우드 컴퓨팅 환경에서의 공유 역할과 책임
- 계약 종료 시 클라우드 서비스 고객 자산의 제거와 반환
- 한 고객의 가상 환경과 다른 고객의 가상 환경의 분리 및 보호
- 비즈니스 요구를 충족하기 위한 가상 컴퓨터 강화 요구 사항
- 클라우드 컴퓨팅 환경의 관리 작업 절차
- 고객이 클라우드 컴퓨팅 환경 내의 관련 활동을 모니터링할 수 있도록 지원
- 가상 네트워크와 물리적 네트워크의 보안 관리 일관성 유지

## <a name="microsoft-and-isoiec-27017"></a>Microsoft와 ISO/IEC 27017

ISO/IEC 27017은 클라우드 서비스 공급자 및 클라우드 서비스 고객을 위한 지침을 제공하는 고유한 표준입니다. 또한 클라우드 서비스 고객이 클라우드 서비스 공급자에게 어떤 것을 바랄 수 있는지에 대한 실용적인 정보를 제공합니다. 고객은 클라우드를 이용한 공유의 책임을 이해함으로써 ISO/IEC 27017로부터 직접적인 혜택을 얻을 수 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure, Azure Government, Azure Germany](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365, Dynamics 365 및 Dynamics 365 Germany](https://aka.ms/d365-compliance-list)
- Intune
- 엔드포인트용 Microsoft Defender
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft Managed Desktop](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, 및 Office 365 Germany
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power Automate(이전 Microsoft Flow) 클라우드 서비스
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 PowerApps 클라우드 서비스
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스
- Power BI Embedded
- Windows 365

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365, ISO 27017:2015

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure ISO 27017 제품](/azure/compliance/offerings/offering-iso-27017)을 참조하세요.

## <a name="office-365-and-iso-270172015"></a>Office 365 및 ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | Access Online, Azure Active Directory, Azure Communications Service, 준수 관리자, Customer Lockbox, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Lockbox (Torus), Office 365용 Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 Customer Portal, Office 365 Microservices(Kaizala, ObjectStore, Sway, PowerPoint Online 문서 서비스, 쿼리 주석 서비스, 학교 데이터 동기화, Siphon, Speech, StaffHub, eXtensible 애플리케이션 프로그램을 포함하지만, 제한하지는 않음), Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, Office 서비스 인프라, 비즈니스용 Skype, Planner, PowerApps, Power Automate, Power BI, Project Online, 고객 키로 서비스 암호화, SharePoint Online, 비즈니스용 Skype, Stream |
| **GCC** | Azure Active Directory, Azure Communications Service, 준수 관리자, Delve, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream |
| **GCC High** | Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype |
| **DoD** | Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, Power BI, SharePoint Online, 비즈니스용 Skype |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 감사, 보고서 및 인증서

Microsoft 클라우드 서비스는 ISO/IEC 27001:2013에 대한 인증 프로세스의 일부로서 ISO/IEC 27017:2015 규약에 대해 1년에 한 번씩 감사를 받습니다.

- [Office 365: ISO 27001, 27018 및 27017 감사 평가 보고서](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>질문과 대답

**이 표준은 누구에게 적용되나요?**

이 규약은 클라우드 서비스 공급자 및 클라우드 서비스 고객 모두에게 규제 및 구현 지침을 제공합니다. ISO/IEC 27002:2013과 유사한 형식으로 작성되어 있습니다.

**ISO/IEC 27017:2015에 대한 Microsoft의 규정 준수 정보는 어디에서 확인할 수 있습니까?**

Azure, Intune, Power BI에 대한 [ISO/IEC 27017:2015 인증서](https://aka.ms/azureiso27017)를 다운로드할 수 있습니다.

**우리 회사의 인증 프로세스에 Microsoft의 ISO/IEC 27017 규정 준수를 사용할 수 있나요?**

예. Microsoft 범위 내 엔터프라이즈 클라우드 서비스에 배포되는 구현에 대해 인증을 받아야 하는 고객은 규정 준수 평가 시 Microsoft의 관련 인증을 사용할 수 있습니다. 하지만 구현에 대한 규정 준수를 평가하기 위한 평가자와의 계약과 고유 조직 내 통제 수단 및 프로세스에 대해서는 파트너가 책임을 져야 합니다.

**적용되는 감사 보고서 사본을 구하려면 어떻게 해야 합니까?**

[Service Trust Portal](https://aka.ms/stphelp)에서는 제3의 독립 기관 감사 보고서와 기타 관련 문서를 제공합니다. 이 포털을 이용하여 자체 규제 요건에 도움이 되는 문서를 다운로드하고 검토할 수 있습니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [ISO/IEC 27017:2015 규약](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Microsoft 온라인 서비스 사용 약관](https://aka.ms/Online-Services-Terms)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
