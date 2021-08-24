---
title: GDPR용 DPIA Azure
description: Microsoft Azure를 사용하는 경우 DPIA(데이터 보호 영향 평가)가 필요한지를 결정하기 위한 정보를 찾아보세요.
keywords: DPIA, Microsoft 365, Microsoft 365 Education, Microsoft 365 설명서, GDPR
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
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: a4b04fe9e72986b9fa706a81c61a781e46695599
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479830"
---
# <a name="data-protection-impact-assessments-guidance-for-data-controllers-using-microsoft-azure"></a>데이터 보호 영향 평가: Microsoft Azure를 사용하는 데이터 컨트롤러의 참고 자료

GDPR(일반 데이터 보호 규정)에 따르면 데이터 컨트롤러는 “자연인의 권리와 자유에 높은 위험을 초래하기 쉬운” 작업을 처리하기 위한 DPIA(데이터 보호 영향 평가)를 준비해야 합니다. Microsoft Azure 자체에는 데이터 컨트롤러를 사용하여 DPIA를 생성해야 하는 고유한 기능이 없습니다. 대신 DPIA가 필요한지 여부는 데이터 컨트롤러가 Microsoft Azure를 배포, 구성 및 사용하는 *방법* 에 대한 세부 정보와 컨텍스트에 따라 달라집니다. 어떤 경우든 DPIA는 프로젝트 수명 초기에 시작하여 계획 및 개발 프로세스와 병행하여 실행되어야 합니다.

이 문서의 목적은 Microsoft Azure에 대한 정보와 데이터 컨트롤러를 제공하여 DPIA 필요 여부, 필요한 경우 포함할 세부 사항을 결정할 수 있도록 지원하는 것입니다.

>[!Note]
>Microsoft는 이 문서에 법적 자문을 제공하지 않습니다. 이 문서는 정보 제공의 목적으로만 제공됩니다. 고객은 개인 정보 책임자와 관리 담당자(및/또는 지정된 데이터 보호 책임자(DPO)) 및/또는 법적 자문 및/또는 법률 고문과 함께 Microsoft Azure 또는 기타 Microsoft 온라인 서비스 사용과 관련된 DPIA의 필요 여부 및 콘텐츠를 결정하는 것이 좋습니다.

## <a name="part-1-determining-whether-a-dpia-is-needed"></a>1부: DPIA가 필요한지 여부를 판단

GDPR 제 35조에 따라 데이터 컨트롤러는 “특히 신기술을 사용하고 처리의 특성, 범위, 컨텍스트 및 목적을 처리하는 유형이 자연인의 권리와 자유에 대한 높은 위험을 초래할 수 있는” 데이터 보호 영향 평가(DPIA)를 만들어야 합니다. 또한 다음 테이블에서 언급될 이러한 높은 위험을 나타내는 특정 요인을 다룹니다. DPIA의 필요 여부를 결정하려면 데이터 컨트롤러는 Microsoft Azure의 컨트롤러 특정 구현 및 사용에 따라 이러한 관련 요소를 고려해야 합니다.

|**고위험 요소**|**Microsoft Azure에 대한 관련 정보**|
|:----|:----|
| 프로파일링을 포함한 자동화된 처리의 기반이 되고 자연인에 관한 법적 영향을 행사하거나 유사하게 자연인에게 중대한 영향을 주는 의사 결정의 기반이 되는 자연인과 관련된 개인 측면의 체계적이고 광범위한 평가입니다.| Microsoft Azure는 특정 데이터의 자동화된 처리를 수행할 수 있는 기능을 제공하지 않습니다. <br><br> *그러나 Azure는 고도로 사용자 정의가 가능한 서비스이므로 데이터 컨트롤러가 Azure를 잠재적으로 이러한 처리에 사용되도록 구성할 수 있습니다*. 컨트롤러는 Azure의 사용 현황에 따라 결정해야 합니다. |
| 특정 범주의 대규모 데이터(인종 또는 민족 태생, 정치적 견해, 종교적 또는 철학적 신념, 노동 조합 회원 및 유전자 데이터, 자연인을 고유하게 식별하기 위한 생체 데이터, 건강 또는 자연인의 성생활이나 성적 취향에 관한 데이터의 처리) 처리 또는 범죄 유죄 판결 및 범죄와 관련된 개인 데이터 처리. | Microsoft Azure는 특수한 범주의 개인 데이터를 처리하도록 설계되지 않았으며 Azure의 사용으로 인해 컨트롤러 처리의 내재 위험이 증가하지 않습니다. <br><br> *그러나 데이터 컨트롤러는 Microsoft Azure를 사용하여 열거된 특정 범주의 데이터를 처리할 수 있습니다*. Microsoft Azure는 고도로 사용자 지정 가능한 서비스이므로 고객이 특정 범주의 개인 데이터와 같은 모든 유형의 데이터를 추적하거나 처리할 수 있습니다. 그러나 데이터 프로세서로 Microsoft는 그러한 사용을 제어할 수 없으며 그러한 사용에 대한 정보를 거의 또는 전혀 가지고 있지 않습니다. 데이터 컨트롤러 데이터의 적절한 사용을 결정하는 것은 데이터 컨트롤러의 책임입니다. |
| 공개적으로 액세스할 수 있는 영역을 대규모로 체계적으로 모니터링.  | Microsoft Azure는 이러한 모니터링을 수행하거나 용이하게 하도록 설계되지 않았습니다. <br><br> *그러나 데이터 컨트롤러는 Azure를 사용하여 이러한 모니터링을 통해 수집된 데이터를 처리할 수 있습니다.* Microsoft Azure는 고도로 사용자 지정 가능한 서비스이므로 고객이 모니터링 데이터와 같은 모든 유형의 데이터를 추적하거나 처리할 수 있습니다. 그러나 데이터 프로세서로 Microsoft는 그러한 사용을 제어할 수 없으며 그러한 사용에 대한 정보를 거의 또는 전혀 가지고 있지 않습니다. 데이터 컨트롤러 데이터의 적절한 사용을 결정하는 것은 데이터 컨트롤러의 책임입니다. |

## <a name="part-2-contents-of-a-dpia"></a>2부 - DPIA의 내용

제 35(7)조는 데이터 보호 영향 평가가 처리의 목적과 계획된 처리의 체계적 설명을 명시하도록 규정하고 있습니다. 포괄적인 DPIA의 체계적 설명에는 처리된 데이터 유형, 데이터 보존 기간, 데이터 위치 및 전송 위치, 데이터에 액세스할 수 있는 제3자 등의 요인이 포함될 수 있습니다. 또한 DPIA에는 다음이 포함되어야 합니다.

- 목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가;
- 자연인의 권리와 자유에 대한 위험 평가;
- 위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 이 규정을 준수함을 입증하기 위한 메커니즘.

다음의 표에는 각 요소와 관련된 Microsoft Azure에 대한 정보가 포함됩니다. 1부에서와 같이 데이터 컨트롤러는 Microsoft Azure의 특정 구현 및 사용의 맥락에서 기타 관련 요인과 함께 아래의 표에 제공된 세부 정보를 고려해야 합니다.

|**DPIA의 요소**|**Microsoft Azure에 대한 관련 정보**|
|:---|:---|
| 처리 목적 | Microsoft Azure를 사용하여 데이터를 처리하는 목적은 컨트롤러를 구현, 구성 및 사용하는 방식에 따라 결정됩니다. <br><br> [온라인 서비스 약관](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) 및 [데이터 보호 부록](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67)에 명시된 바와 같이, Microsoft는 데이터 프로세서로서 고객의 문서화된 지침에 따라 온라인 서비스를 제공하고자 고객 데이터를 처리합니다. <br><br> 표준 [온라인 서비스 약관](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) 및 [데이터 보호 부록](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67)에 자세히 설명된 바와 같이, Microsoft는 다음과 같은 합법적인 비즈니스 운영 지원을 위하여 개인 데이터를 사용합니다. (1) 청구 및 계정 관리. (2) 보상 (예: 사원 수수료과 파트너의 성과급 계산). (3) 내부 보고 및 모델링 (예: 예측, 수익, 용량 계획, 제품 전략); (4) Microsoft 또는 Microsoft 제품에 영향을 줄 수 있는 사기, 사이버 범죄 또는 사이버-공격 방어. (5) 접근성, 개인 정보 보호 또는 에너지 효율성의 핵심 기능 개선. (6) 법률적인 의무를 통한 재무 보고 및 준수 (온라인 서비스 약관에 요약 된 고객 데이터 노출에 대 한 제한 사항 준수). <br><br> Microsoft는 다음과 같은 합법적인 비즈니스 운영 지원을 위해 개인 정보 처리 관리를 합니다. 일반적으로 Microsoft는 개인 정보를 합법 적인 비즈니스 운영에 사용하기 전 개인 정보를 수집하여 Microsoft가 특정 개인을 식별하지 못할 뿐만 아니라 합법적 비즈니스 운영 지원을 위해 개인 정보 사용시 개인 식별 가능성을 최소화 합니다. <br><br> Microsoft는 프로파일링, 광고 또는 유사한 상업적 목적으로 고객 데이터 또는 파생된 정보를 사용하지 않습니다. |
| 처리된 개인 데이터의 범주  | *고객 데이터 - 엔터프라이즈 서비스를 사용하여 고객이 또는 고객을 대신해서 Microsoft에 제공되는 모든 텍스트, 사운드, 비디오 또는 이미지 파일, 소프트웨어를 포함하는 모든 데이터입니다. 고객 데이터에는 (1) 최종 사용자의 식별 가능 정보(예: 사용자 이름 및 Azure Active Directory의 연락처 정보) 및 고객이 특정 서비스에서 업로드하거나 만든 고객 콘텐츠(예: Azure Storage의 고객 콘텐츠, Azure SQL 데이터베이스의 고객 콘텐츠 또는 Azure Virtual Machines의 고객 가상 머신 이미지)가 둘 다 포함됩니다.<br><br> *서비스 생성 데이터 - Microsoft가 사용자에게 엔터프라이즈 서비스를 제공하는 데 도움을 주는 Microsoft 생성 로그 및 관련 데이터입니다. 서비스 생성 로그에는 일반적으로 자체적으로는 개인을 식별할 수 없지만 사용자에게 엔터프라이즈 서비스를 전달하는 데 사용되는 시스템에서 생성된 고유 식별자와 관련된 주로 필명화된 데이터가 포함됩니다. 최종 사용자에 대한 식별 가능 정보(예: 사용자 이름)도 서비스 생성 로그에 포함될 수 있습니다. <br><br> *지원 데이터 - 온라인 서비스에 대한 기술 지원을 얻기 위해 Microsoft와의 계약을 통해 Microsoft에 고객이 또는 고객을 대신하여(또는 고객이 Microsoft가 온라인 서비스에서 얻도록 승인) 제공하는 데이터입니다. <br><br> Azure에서 처리하는 데이터와 관련된 자세한 내용은 데이터 처리 계약을 포함한 [온라인 서비스 약관](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) 및 [Microsoft 보안 센터](https://www.microsoft.com/trustcenter)를 참조하세요.</p> |
| 데이터 보존 | Microsoft는 고객이 온라인 서비스를 사용할 수 있는 동안 그리고 모든 고객 데이터가 고객에 의해 검색되거나 OST의 조건에 따라 삭제될 때까지 고객 데이터를 보유 및 처리합니다. 고객의 구독 기간 동안 고객은 각 온라인 서비스에 저장된 고객 데이터를 액세스하고 추출할 수 있습니다. 무료 평가판 및 LinkedIn 서비스를 제외하고 Microsoft는 고객이 데이터를 추출할 수 있도록 고객의 구독이 만료 또는 종료된 이후 90일 동안 기능이 제한된 계정에서 온라인 서비스에 저장된 고객 데이터를 보유하게 됩니다. 90일의 보유 기간이 종료되면 Microsoft는 고객의 계정을 비활성화하고 고객 데이터를 삭제합니다. 고객은 [Azure Data Subject Request GDPR 문서](https://servicetrust.microsoft.com/ViewPage/GDPRDSR)에 설명 된 기능을 사용하여 데이터 주체 요청에 따라 개인 데이터를 삭제할 수 있습니다. |
| 개인 데이터의 위치 및 전송 | 고객은 OST에 명시된 특정 예외에 따라 [지역](https://azuredatacentermap.azurewebsites.net/) 내에서 유휴 고객 데이터를 프로비전할 수 있습니다. 서비스 배포 및 데이터 상주에 대한 추가 세부 정보는 OST(온라인 서비스 약관)에 대한 [Microsoft DPA(데이터 보호 추록)](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67) 및 [Azure 글로벌 인프라](https://azure.microsoft.com/global-infrastructure/) 웹 페이지에서도 확인할 수 있습니다.<br><br>유럽 경제 지역과 스위스 및 영국의 개인 데이터의 경우 Microsoft는 개인 정보의 제3자 혹은 국제 기관 이전 시 적절한 보호 조치를 받도록 GDPR 46조에 의거하여 이를 준수합니다. Microsoft는 프로세서 및 기타 모델 계약에 대한 표준 계약 조항에 따른 Microsoft의 약속과 더불어 [Privacy Shield 프레임워크](https://www.privacyshield.gov/) 조건을 계속 준수하지만 이를 더 이상 EU/EEA에서 미국으로 개인 데이터를 전송하는 기준으로 사용하지 않습니다. |
| 타사 하위 프로세서와 데이터 공유 | Microsoft는 고객 및 기술 지원, 서비스 유지 관리, 기타 작업과 같은 기능을 지원하기 위해 하위 프로세서 역할을 하는 타사와 데이터를 공유합니다. Microsoft가 고객 데이터, 지원 데이터 또는 개인 데이터를 전송하는 하도급업자는 [온라인 서비스 약관](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)의 데이터 보호 약관보다 덜 안전하지만 Microsoft와 서면 계약을 체결하게 됩니다. Microsoft Core Online Servic의 고객 데이터가 공유되는 모든 타사 하위 프로세서는 온라인 서비스 하도급업자 목록에 포함됩니다. 지원 데이터(고객이 지원 상호 작용 동안 공유하도록 선택한 고객 데이터 포함)에 액세스할 수 있는 모든 타사 하위 프로세서는 [Microsoft 상업적 지원 하도급자](https://www.microsoft.com/trustcenter/privacy/who-can-access-your-data-and-on-what-terms#subcontractors) 목록에 포함됩니다. |
| 데이터 주체 권리 | 프로세서로 작동할 때 Microsoft는 고객(즉, 데이터 컨트롤러)이 데이터 주체의 개인 데이터를 사용할 수 있도록 하고 고객이 GDPR에 따라 권리를 행사할 때 데이터 주체 요청을 수행할 수 있는 기능을 제공합니다. Microsoft는 제품의 기능과 프로세서로의 역할에 있어 일관된 방식으로 진행합니다. Microsoft가 고객의 데이터 주체로부터 GDPR에 따라 권리 중 하나를 행사하도록 요청을 받으면 데이터 컨트롤러에게 요청이 리디렉션됩니다. <br><br> Azure 데이터 주체 요청 가이드는 Azure의 기능을 사용하여 데이터 주체 권한을 지원하는 방법에 대한 데이터 컨트롤러의 설명을 제공합니다. <br><br> 개인 데이터의 GDPR 권한에 따라 합법적인 비즈니스 처리를 위한 데이터 주체의 데이터 처리 요청은 Microsoft 개인정보처리방침에 따라 Microsoft에 전달 되어야 합니다. <br><br> Microsoft는 일반적으로 합법적인 비즈니스 운영 이전에 개인정보를 수집하며 수집된 정보는 특정 개인을 식별하지 못하도록 되어있습니다. 이 작업은 개인에 대한 개인 정보 위험을 크게 줄일 수 있습니다.  Microsoft는 개인을 식별할 수 없기 때문에 데이터 주체의 엑세스, 지우기, 이식가능성 및 프로세스 제한성 및 거절권한을 지원할 수 없습니다. <br><br> [Azure 데이터 주체 요청 GDPR 설명서](https://servicetrust.microsoft.com/ViewPage/GDPRDSR)는 Azure의 기능을 사용하여 데이터 주체 권한을 지원하는 방법에 대한 설명을 제공합니다. |
| 목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가 | 이러한 평가는 데이터 컨트롤러의 요구와 처리 목적에 따라 달라집니다.<br><br> Microsoft는 서비스 조항 지원, 서비스 사용 주체의 데이터 처리 위험 등 합법적인 비즈니스 운영 지원을 위해 사용되는 개인 정보 보호의 익명화 및 수집을 위한 적절한 조치를 취하고 있습니다. <br><br> Microsoft에서 수행하는 처리와 관련하여 이러한 처리는 데이터 컨트롤러에 서비스를 제공하기 위해 필수적이며 비례합니다. Microsoft는 OST 준수를 약속합니다. |
| 데이터 주체의 권리와 자유에 대한 위험 평가 | Microsoft Azure 사용으로 인한 데이터 주체의 권리와 자유에 대한 주요 위험은 데이터 컨트롤러가 Microsoft Azure를 구현, 구성, 사용하는 방법과 상황의 기능입니다.<br><br> 그러나 다른 서비스와 마찬가지로 서비스에서 보관하는 개인 정보는 승인되지 않은 액세스나 부주의한 공개의 위험이 있습니다. 이러한 위험을 해결하기 위해 Microsoft에서 취하는 조치는 OST에 설명되어 있으며 아래에서 그 세부 정보를 확인할 수 있습니다. |
| 위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 GDPR을 준수함을 입증하기 위한 메커니즘 | Microsoft는 고객 데이터 보안을 보호하기 위해 노력합니다. Microsoft에서 취하는 보안 조치는 OST의 세부 정보에 설명되어 있습니다. <br><br> Microsoft는 엄격한 보안 표준 및 업계 선도적인 데이터 보호 방법론을 준수합니다. Microsoft는 새로운 위협에 대응하기 위해 지속해서 시스템을 개선하고 있습니다. 클라우드 거버넌스 및 개인 정보 보호 규정 관련 세부 정보는 [보안 센터의 클라우드 거버넌스 및 개인 정보 보호](https://www.microsoft.com/trustcenter/guidance/ensure-compliance) 페이지에서 제공됩니다. <br><br> Microsoft는 처리하는 개인 데이터를 보호하기 위해 합리적이고 적합한 기술적 및 조직적 조치를 취합니다. 이러한 조치에는 내부 개인 정보 보호 정책 및 규정, 계약상의 약속, 국제 및 지역 표준 인증이 포함되나 국한되지 않습니다. 자세한 정보는 [보안 센터의 개인 정보 보호 표준 페이지](https://www.microsoft.com/trustcenter/privacy/we-set-and-adhere-to-stringent-standards)에서 제공됩니다. <br><br> Microsoft는 Microsoft의 개인 데이터 사용 및 처리를 설명하는 데 도움이 되는 중요하고 투명한 고객 관련 보안 및 개인 정보 보호 자료를 제공합니다. 고객은 질문 사항을 준비하여 Microsoft에 문의할 것을 권장합니다. <br><br> 또한 Microsoft는 데이터 보호 영향 평가 및 기록 유지를 포함하지만 국한되지 않는 데이터 프로세스에 적용되는 모든 기타 GDPR 의무를 준수합니다. <br><br> Microsoft는 합법적인 비즈니스 운영을 위해 개인 데이터를 처리할 때 데이터 관리자에 적용되는 GDPR의 의무를 준수합니다. |

## <a name="learn-more"></a>자세히 알아보기

- [Microsoft 보안 센터](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
