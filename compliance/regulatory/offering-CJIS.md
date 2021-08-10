---
title: CJIS(범죄 행위 정보 서비스) 보안 정책
description: Microsoft 정부 클라우드 서비스는 미국 범죄 정의 정보 서비스 보안 정책을 준수합니다.
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
ms.openlocfilehash: cdcf6bb91e7bd6b01a7a4372f33e2f52089d1f0c4fed3c327b85a3a13eafeac2
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292535"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a>CJIS(범죄 행위 정보 서비스) 보안 정책

## <a name="cjis-overview"></a>CJIS 개요

미국 FBI(Federal Bureau of Investigation)의 CJIS(범죄 조사 정보 서비스) 부서에서는 주, 지역 및 연방 사법 기관과 범죄 사법 기관이 지문 기록 및 범죄 기록과 같은 CJI(범죄 범죄 정보)에 액세스할 수 있도록 합니다. 미국의 사법 기관 및 기타 정부 기관은 CJI 전송, 저장 또는 처리에 클라우드 서비스를 사용하는 것이 CJI를 보호하기 위한 최소 보안 요구 사항 및 제어를 설정하는 [CJIS](https://aka.ms/cjis-security-policy)보안 정책을 준수하는지 확인합니다.

CJIS 보안 정책은 NIST(National Institute of Standards and Technology)의 지침과 함께, 대법원 및 FBI 지시문, 연방법 및 범죄 사법 기관의 자문 정책 위원회 결정을 통합합니다. 진화하는 보안 요구 사항을 반영하기 위해 정책이 주기적으로 업데이트됩니다.

CJIS 보안 정책은 클라우드 서비스 공급자와 같은 개인 계약자가 클라우드 서비스 사용이 CJIS 요구 사항과 일치할 수 있는지 여부를 결정하기 위해 평가해야 하는 13개 영역을 정의합니다. 이러한 영역은 NIST 800-53에 해당하며, 이는 Microsoft가 정부 클라우드 제품 인증을 받은 프로그램인 [FedRAMP(Federal Risk and Authorization Management](offering-FedRAMP.md)Program)의 기반이 됩니다.

또한 CJI를 처리한 모든 비공개 계약자는 보안 정책에 필요한 CJI의 보안 및 기밀성을 보장하는 데 도움이 되는 미국 법무 장관이 승인한 일류 계약인 CJIS 보안 부록에 서명해야 합니다. 또한 계약업체는 연방 및 주 법률, 규정 및 표준과 일관된 보안 프로그램을 유지 관리하고, CJI의 사용을 정부 기관이 제공한 목적으로 제한합니다.

## <a name="microsoft-and-cjis-security-policy"></a>Microsoft 및 CJIS 보안 정책

Microsoft는 CJIS 정보 계약을 통해 CJIS 보안 부록에 주에 서명합니다. CJIS 보안 정책을 준수하는 주 법 집행 기관에게 Microsoft의 클라우드 보안 제어가 데이터의 전체 수명 주기를 보호하고 CJI에 액세스할 수 있는 운영 담당자의 적절한 배경 심사를 보장하는 방법을 알 수 있습니다. Microsoft는 계속해서 주 정부와 함께 CJIS 정보 계약을 체결합니다.

Microsoft는 Microsoft Azure Government, Microsoft Office 365 미국 정부 및 Microsoft Dynamics 365 미국 정부의 운영 정책 및 절차를 평가하고 범위 내 서비스 사용에 대한 FBI 요구 사항을 충족하기 위해 해당 서비스 계약의 기능을 테스트할 것입니다.

Microsoft 클라우드에서 CJIS 보안 정책의 이점에 대해 자세히 알아보시고 [Genetec이](https://customers.microsoft.com/story/genetec) 범죄 조사를 지운 방법 읽기

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure Government
- Dynamics 365 미국 정부
- Office 365 미국 정부
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스

## <a name="azure-dynamics-365-and-cjis"></a>Azure, Dynamics 365 및 CJIS

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure CJIS 서비스를 참조하세요.](/azure/compliance/offerings/offering-cjis)

## <a name="office-365-and-cjis"></a>Office 365 및 CJIS

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **GCC** | Azure Active Directory, 준수 관리자, Delve, Exchange Online, Forms, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 감사, 보고서 및 인증서

FBI는 CJIS 요구 사항을 준수하는 Microsoft 인증을 제공하지 않습니다. 대신 Microsoft와 주 CJIS 기관 간의 계약과 Microsoft와 고객 간의 계약에 Microsoft 의약이 포함됩니다.

[Microsoft CJIS 클라우드 요구 사항](https://aka.ms/MicrosoftCJISCloudRequirements)

### <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a>미국의 CJIS 상태(2020년 11월 5일 현재)

녹색 지도에 강조 표시된 관리 계약이 있는 45개 주 및 콜롬비아 교육구에는 다음이 포함됩니다.

앨라배마, 알라스카, 애리조나, 아칸소, 캘리포니아, 콜로라도, Connecticut, 플로리다, 조지아, 하와이,Idaho, 일리노이, 인디애나, 아이오와, 칸사스, 킷킷, 메인, 매사추세츠, 미시간, 미네소타, 미시시피, 미주리 몬타나, 네브라스카, 네바다, New Hampshire, New Jersey, New Mexico, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, 텍사스, Utah, Vermont, 버지니아, 워싱턴, 서부 버지니아, 위스콘신 및 콜롬비아 교육구

적용 가능한 CJIS 규제 컨트롤을 충족하기 위한 Microsoft의 약속을 통해 범죄자 조직은 클라우드 기반 솔루션을 구현하고 CJIS 보안 정책 V5.9를 준수할 수 있습니다.

### <a name="frequently-asked-questions"></a>자주 묻는 질문

**규정 준수 정보는 어디에서 요청할 수 있나요?**

관심 있는 관할권에 대한 정보는 Microsoft 계정 담당자에게 문의하세요. 현재 사용 가능한 서비스에 대한 자세한 내용은 <cjis@microsoft.com> 연락처를 참조하십시오.

**Microsoft는 클라우드 서비스를 통해 주 요구 사항을 준수할 수 있도록 하는 방법을 보여 주나요?**

Microsoft는 주 CSA(CJIS Systems Agency)와 정보 계약에 서명합니다. 주 CSA에서 복사본을 요청할 수 있습니다. 또한 Microsoft는 고객에게 자세한 보안, 개인 정보 보호 및 규정 준수 정보를 제공합니다. 고객은 또한 독립 감사자에 의해 준비된 보안 및 규정 준수 보고서를 검토하여 Microsoft가 관련 감사 범위에 적합한 보안 제어(예: ISO 27001)를 구현한지 확인할 수 있습니다.

**기관의 규정 준수 노력은 어디에서 시작해야 하나요?**

[CJIS 보안 정책은](https://aka.ms/cjis-security-policy) 기관에서 CJI를 보호하기 위해 취해야 하는 예방 조치를 다하고 있습니다. 또한 Microsoft 계정 담당자가 관할권의 요구 사항에 익숙한 사용자와 연락할 수 있습니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [범죄 행위 정보 서비스](https://aka.ms/cjis)
- [CJIS 보안 정책](https://aka.ms/cjis-security-policy)
- [Microsoft 공통 컨트롤 허브 규정 준수 프레임 워크](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government 클라우드](https://go.microsoft.com/fwlink/?linkid=2087246)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
