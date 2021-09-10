---
title: GDPR 및 CCPA에 따른 Office 365 데이터 주체 요청
description: GDPR 및 CCPA에 따른 사용자 권한 및 기업에서 Office 365를 사용하여 DSR에 대한 응답으로 데이터를 찾고 작업하는 방법을 이해합니다.
keywords: Office 365, DSR, Microsoft 365, Microsoft 365 Education, Microsoft 365 설명서, GDPR, CCPA
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
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: f5b0acae758e149f2bfde5683a0b9f2c45f0db29
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948230"
---
# <a name="office-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>GDPR 및 CCPA에 대한 Office 365 데이터 주체 요청

## <a name="introduction-to-dsrs"></a>DSR 소개

EU(유럽 연합) [GDPR(일반 데이터 보호 규정)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm)은 사용자(규정에 *데이터 주체* 로 알려짐)에게 고용주 또는 다른 유형의 대리점 및 조직(*정보 통제자* 또는 단순히 *통제자* 로 지칭)이 수집한 개인 데이터를 관리할 수 있는 권한을 부여합니다. 개인 데이터는 GDPR에서는 광범위하게 식별되었거나 식별 가능한 자연인과 관련된 모든 데이터로 정의됩니다. GDPR은 데이터 주체에게 개인 데이터에 대한 특정 권한을 부여합니다. 이러한 권한에는 데이터 복사본 획득, 변경 요청, 처리 제한, 삭제 또는 다른 통제자에게 이동될 수 있도록 전자 형식으로 수신하는 권한이 포함됩니다. 데이터 주체가 통제자에게 개인 데이터에 대해 조치를 취할 것을 요구하는 공식적인 요청을 *데이터 주체 요청* 또는 DSR이라고 합니다. 통제자는 각 DSR을 즉시 고려하고, 요청된 조치를 취하거나 통제자가 해당 DSR을 처리할 수 없는 이유에 대한 설명을 제공하여 실질적인 응답을 제공할 의무가 있습니다.

마찬가지로 CCPA(캘리포니아 소비자 개인 정보 보호법)은 캘리포니아 소비자에게 GDPR의 데이터 주체 권리와 유사한 권리를 포함하여, 소비자의 개인 정보 삭제, 액세스 및 수신(이식성)과 같은 개인 정보 보호 권리 및 의무를 제공합니다. 또한 CCPA는 특정 공개, 실행 권리 행사 시 차별 대우로부터 보호, “판매"로 분류되는 특정 데이터 전송에 대한 "옵트아웃(opt-out)/옵트인(opt-in)" 요구도 허용합니다. 판매는 가치 있는 대가관계를 위하여 데이터 공유를 포함하도록 광범위하게 정의됩니다. CCPA에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법](offering-ccpa.md) 및 [캘리포니아 소비자 개인 정보 보호법 FAQ](ccpa-faq.yml)를 참조하세요.

이 가이드에서는 Office 365 제품, 서비스 및 관리 도구를 사용하여 고객이 DSR에 응답하기 위해 개인 데이터 또는 개인 정보를 찾고 조치를 취하는 데 도움을 주는 방식을 설명합니다. 특히, Microsoft 클라우드에 있는 개인 데이터 또는 개인 정보를 찾고, 액세스하고, 조치를 취하는 방법도 포함되어 있습니다. 이 가이드에 설명된 프로세스에 대한 간략한 개요는 다음과 같습니다.

- **검색:** 검색 도구를 사용하여 DSR의 대상이 될 수 있는 고객 데이터를 좀 더 쉽게 찾을 수 있습니다. 잠재적인 반응형 문서가 일단 수집되면 다음 단계에 설명된 DSR 작업 중 하나 이상을 수행하여 요청에 응답할 수 있습니다. 또는 요청이 DSR에 응답하기 위한 조직 지침을 충족하지 않는지도 확인할 수 있습니다.
- **액세스:** Microsoft 클라우드에 있는 개인 데이터를 검색하고, 요청될 경우 데이터 주체가 사용할 수 있는 복사본을 만듭니다.
- **수정:** 해당되는 경우 개인 데이터를 변경하거나 요청된 다른 작업을 구현합니다.
- **제한:** 가능한 경우 다양한 Microsoft 클라우드 서비스에 대한 라이선스를 제거하거나 원하는 서비스를 해제하여 개인 데이터의 처리를 제한합니다. 또한 Microsoft 클라우드에서 데이터를 제거하고 온-프레미스 또는 다른 위치에 유지할 수도 있습니다.
- **삭제:** Microsoft 클라우드에 있는 개인 데이터를 영구적으로 제거합니다.
- **내보내기/수신(이식성):** 개인 데이터 또는 개인 정보의 전자 사본(컴퓨터가 읽을 수 있는 형식)을 데이터 주체에게 제공합니다. CCPA 하에서 개인 정보는 식별된 또는 식별 가능한 개인과 관련 있는 모든 정보입니다. 이때 개인의 비공개, 공개 또는 업무 역할이 구분되지 않습니다. 정의된 "개인 정보"라는 용어는 GDPR에 따른 "개인 데이터"와 대략 일치합니다. 그러나 CCPA에는 가족 및 가정 데이터가 포함되어 있습니다. CCPA에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법](offering-ccpa.md) 및 [캘리포니아 소비자 개인 정보 보호법 FAQ](ccpa-faq.yml)를 참조하세요.

### <a name="terminology"></a>용어

다음은 이 가이드와 관련된 GDPR 용어의 정의입니다.

- **통제자:** 단독으로 또는 다른 대상과 함께 개인 데이터 처리의 목적 및 방법을 결정하는 자연인이나 법인, 공공 기관, 대리점 또는 기타 단체입니다. 이러한 처리의 목적 및 방법을 연합국 법률 또는 회원국 법률에 따라 결정하는 경우, 통제자 또는 구체적인 지명 기준을 연합국 법률 또는 회원국 법률에서 제공할 수 있습니다.
- **개인 데이터 및 데이터 주체** 식별되었거나 식별 가능한 자연인(‘데이터 주체’)과 관련된 모든 정보입니다. 식별 가능한 자연인은 직간접적으로, 특히 이름, 식별 번호, 위치 데이터, 온라인 식별자 또는 해당 자연인의 신체적, 생리적, 유전적, 정신적, 경제적, 문화적 또는 사회적 ID와 같은 식별자를 참조하여 식별될 수 있는 사람입니다.
- **프로세서:** 통제자를 대신하여 개인 데이터를 처리하는 자연인이나 법인, 공공 기관, 대리점 또는 기타 단체입니다.
- **고객 데이터:** 엔터프라이즈 서비스를 사용하여 고객이 또는 고객을 대신해서 Microsoft에 제공되는 모든 텍스트, 사운드, 비디오 또는 이미지 파일, 소프트웨어를 포함하는 모든 데이터입니다. 고객 데이터에는 (1) 최종 사용자의 식별 가능 정보(예: 사용자 이름 및 Azure Active Directory의 연락처 정보) 및 고객이 특정 서비스에서 업로드하거나 만든 고객 콘텐츠(예: Word 또는 Excel 문서 또는 Exchange Online 전자 메일 텍스트의 고객 콘텐츠, SharePoint Online 사이트에 추가되거나 비즈니스용 OneDrive 계정에 저장된 고객 콘텐츠)가 둘 다 포함됩니다.
- **시스템 생성 로그:** Microsoft가 사용자에게 엔터프라이즈 서비스를 제공하는 데 도움을 주는 Microsoft 생성 로그 및 관련 데이터입니다. 시스템 생성 로그에는 일반적으로 자체적으로는 개인을 식별할 수 없지만 사용자에게 엔터프라이즈 서비스를 전달하는 데 사용되는 시스템 생성 번호에 해당하는 주로 필명화된 데이터(예: 고유 식별자)가 포함됩니다. 최종 사용자에 대한 식별 가능 정보(예: 사용자 이름)도 시스템 생성 로그에 포함될 수 있습니다.

### <a name="how-to-use-this-guide"></a>이 가이드를 사용하는 방법

사용 사례와 관련된 정보를 찾을 수 있도록 이 가이드는 4부로 구성되어 있습니다.

- **[1부: 고객 데이터에 대한 DSR에 응답](#part-1-responding-to-dsrs-for-customer-data):** *고객 데이터* 는 일상적인 비즈니스 운영을 위해 Office 365에서 생산되고 저장되는 데이터입니다. 데이터를 작성하는 데 가장 일반적으로 사용되는 Office 365 응용 프로그램에는 Word, Excel, PowerPoint, Outlook, OneNote 등이 있습니다. 또한 Office 365는 SharePoint Online, Teams, Forms 등 다른 사용자와 보다 효율적으로 공동 작업을 수행할 수 있는 응용 프로그램으로 구성되어 있습니다. 이 가이드의 1부에서는 Office 365 온라인 서비스에서 데이터를 작성 및 저장하는 데 사용된 Office 365 응용 프로그램에서 데이터를 검색, 액세스, 수정, 제한, 삭제 및 내보내는 방법을 설명합니다. 또한 Microsoft가 고객 조직의 데이터 처리자 역할을 함에 따라 DSR 기능을 테넌트 관리자로 사용할 수 있는 하는 제품 및 서비스를 소개합니다.
- **[2부: Office 365에서 생성된 정보에 관한 DSR에 응답](#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365):** Office 365는 Delve, MyAnalytics 및 Workplace Analytics와 같은 서비스를 통해 특정 정보를 제공합니다. 이 가이드의 2부에서는 이러한 정보가 생성되는 방법 및 이러한 정보와 관련된 DSR에 응답하는 방법을 설명합니다.
- **[3부: 시스템 생성 로그에 대한 DSR에 응답](#part-3-responding-to-dsrs-for-system-generated-logs):** Office 365 엔터프라이즈 서비스를 사용할 때 Microsoft는 온라인 서비스에서 기능의 사용 또는 성능을 기록하는 서비스 로그와 같은 몇 가지 정보를 생성합니다. 서비스 생성 데이터에는 대부분 Microsoft에서 생성하는 가명 식별자가 포함되어 있으므로 이 문서에서는 이 범주를 일반적으로 *시스템 생성 로그* 라고 합니다. 이 데이터는 추가 정보를 사용하지 않고는 특정 데이터로 분류될 수 없지만 "개인 데이터"에 대한 GDPR의 정의에서 개인 데이터로 간주될 수 있습니다. 이 가이드의 3부에서는 시스템 생성 로그를 액세스, 삭제 및 내보내는 방법을 설명합니다.
- **[4부: DSR을 지원하는 추가 리소스](#part-4-additional-resources-to-assist-you-with-dsrs):** 이 가이드의 4부에서는 특정 Office 365 제품 및 서비스를 사용할 때 Microsoft가 데이터 통제자인 제한된 시나리오를 나열합니다.

> [!NOTE]
> 대부분의 경우 조직의 사용자가 Microsoft Office 365 제품 및 서비스를 사용할 때는 여러분이 데이터 통제자이고 Microsoft는 처리자입니다. 데이터 통제자로서 여러분은 데이터 주체에 직접 응답하는 역할을 담당합니다. 이를 지원하기 위해 이 가이드의 1~3부에서는 조직이 DSR 요청에 응답하는 데 사용할 수 있는 기술적 기능을 자세히 설명합니다. 그러나 일부 제한된 시나리오에서는 사용자가 특정 Office 365 제품 또는 서비스를 사용할 때 Microsoft가 데이터 통제자가 됩니다. 이러한 경우 4부의 정보는 데이터 주체가 Microsoft에 DSR 요청을 전송할 수 있는 방법에 대한 지침을 제공합니다.

### <a name="office-365-national-clouds"></a>Office 365 국가별 클라우드

Microsoft Office 365 서비스는 국가별 클라우드 환경, [Office 365 Germany](/microsoft-365/admin/admin-overview/learn-about-office-365-germany), [21Vianet에서 운영하는 Office 365(중국)](/microsoft-365/admin/services-in-china/services-in-china) 및 [Office 365 미국 정부](https://www.microsoft.com/microsoft-365/government/compare-office-365-government-plans)에서도 사용할 수 있습니다. 이 문서에 설명된 데이터 주체 요청 관리 지침 대부분은 이러한 국가별 클라우드 환경에도 적용됩니다. 그러나 이러한 환경이 격리되어 있으므로 몇 가지 예외가 있습니다. 이러한 예외 중에서 중요한 내용은 해당 참고 사항에 명시되어 있습니다.

### <a name="hybrid-deployments"></a>하이브리드 배포

조직은 클라우드 기반 서비스와 온-프레미스 서버 제품이 조합된 Microsoft 서비스 제품으로 구성될 수 있습니다. 일반적으로 하이브리드 배포는 클라우드와 온-프레미스에 존재하는 사용자 계정(ID 관리)과 리소스(예: 사서함, 웹 사이트, 데이터)를 공유합니다. 일반적인 하이브리드 시나리오는 다음과 같습니다.

- Exchange 하이브리드 배포: 온-프레미스 사서함을 보유하는 사용자도 있고, Exchange Online 사서함을 보유하는 사용자도 있습니다.
- SharePoint 하이브리드 배포: 사이트 및 파일 서버는 온-프레미스에 있고 비즈니스용 OneDrive 계정은 Office 365에 있습니다.
- Azure Activity Directory와 동기화되는 온-프레미스 ID 관리 시스템(Active Directory): Office 365의 기본 디렉터리 서비스입니다.

DSR 요청에 응답할 경우, DSR 요청에 해당되는 데이터가 Microsoft 클라우드에 있는지 또는 온-프레미스 조직에 있는지를 확인한 후, 해당 요청에 응답하기 위한 적절한 단계를 수행해야 할 수 있습니다. Office 365 데이터 주체 요청 가이드(이 가이드)에서는 클라우드 기반 데이터에 응답하기 위한 지침을 제공합니다. 온-프레미스 조직의 데이터에 대한 지침은 [Office 온-프레미스 서버에 대한 GDPR](/Office365/Enterprise/gdpr-for-office-servers)을 참조하세요.

## <a name="part-1-responding-to-dsrs-for-customer-data"></a>1부: 고객 데이터에 대한 DSR에 응답

고객 데이터에 대한 DSR에 응답하기 위한 지침은 다음 네 개의 섹션으로 구성되어 있습니다.

- [콘텐츠 검색 eDiscovery 도구를 사용하여 DSR에 응답](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)
- [앱 내 기능을 사용하여 DSR에 응답](#using-in-app-functionality-to-respond-to-dsrs)
- [DSR 수정 요청에 응답](#responding-to-dsr-rectification-requests)
- [DSR 제한 요청에 응답](#responding-to-dsr-restriction-requests)

### <a name="how-to-determine-the-office-365-applications-that-may-be-in-scope-for-a-dsr-for-customer-data"></a>데이터에 대한 DSR의 범위 내에 있을 수 있는 Office 365 응용 프로그램을 확인하는 방법

개인 데이터를 검색할 위치 또는 검색할 항목을 쉽게 확인하려면 조직의 사용자가 Office 365에서 데이터를 만들고 저장하는 데 사용할 수 있는 Office 365 응용 프로그램을 식별하면 됩니다. 이를 알면 DSR의 범위 내에 속하는 Office 365 응용 프로그램의 범위가 좁혀지고 DSR과 관련된 개인 데이터를 검색하고 액세스하는 방법을 확인하는 데 도움이 됩니다. 특히 이는 콘텐츠 검색 도구를 사용할 수 있는지 여부 또는 데이터가 만들어진 응용 프로그램의 앱 내 기능을 사용해야 하는지 여부를 의미합니다.

조직의 사용자가 고객 데이터를 만드는 데 사용하는 Office 365 응용 프로그램을 빠르게 식별하는 방법은 조직의 비즈니스용 Microsoft 365 구독에 포함된 응용 프로그램을 확인하는 것입니다. 이렇게 하려면 Office 365 관리자 포털에서 사용자 계정에 액세스하여 제품 라이선스 정보를 확인하면 됩니다. [사용자에게 라이선스 할당하기](/microsoft-365/admin/manage/assign-licenses-to-users)를 참조하세요.

## <a name="using-the-content-search-ediscovery-tool-to-respond-to-dsrs"></a>콘텐츠 검색 eDiscovery 도구를 사용하여 DSR에 응답

조직이 Office 365를 사용하여 만들고 저장하는 대규모 데이터 집합 내에서 개인 데이터를 찾을 때 먼저 사용자가 이러한 데이터를 작성하는 데 사용했을 수 있는 응용 프로그램을 고려할 수 있습니다. Microsoft에서는 Office 365에 저장된 조직의 데이터 중 90% 이상이 Word, Excel, PowerPoint, OneNote 및 Outlook에서 작성되는 것으로 추정합니다. 이러한 Office 응용 프로그램에서 작성된 문서는 엔터프라이즈용 Microsoft 365 앱 또는 Office 영구 라이선스를 통해 구매했더라도 SharePoint Online 사이트, 사용자의 비즈니스용 OneDrive 계정 또는 사용자의 Exchange Online 사서함에 저장될 가능성이 매우 높습니다. 이는 콘텐츠 검색 eDiscovery 도구를 사용하여 SharePoint Online 사이트, 비즈니스용 OneDrive 계정 및 Exchange Online 사서함(Microsoft 365 그룹, Microsoft Teams, EDU 과제와 연결된 사이트 및 사서함 포함)에서 검색해 조사 중인 DSR과 관련될 수 있는 문서 및 사서함 항목을 찾을 수 있음을 의미합니다. 또한 콘텐츠 검색 도구를 사용하여 다른 Office 365 응용 프로그램에서 작성된 고객 데이터를 검색할 수 있습니다.

다음 목록에서는 사용자가 고객 작성 콘텐츠를 만드는 데 사용하고 콘텐츠 검색을 사용하여 검색할 수 있는 Office 365 응용 프로그램에 제시됩니다. DSR 가이드의 이 섹션에서는 Office 365 응용 프로그램을 사용하여 만든 데이터를 검색, 액세스, 내보내기 및 삭제하는 방법에 대한 지침을 제공합니다.

콘텐츠 검색을 사용하여 고객 데이터를 찾을 수 있는 응용 프로그램:

- 일정
- Excel
- Office Lens
- 비즈니스용 OneDrive
- OneNote
- Outlook/Exchange
- 사용자
- PowerPoint
- SharePoint
- 비즈니스용 Skype
- 작업
- Teams
- To Do
- 비디오
- Visio
- Word

> [!NOTE]
> 콘텐츠 검색 eDiscovery 도구를 [21Vianet에서 운영하는 Office 365(중국)](/microsoft-365/admin/services-in-china/services-in-china)에서는 사용할 수 없습니다. 즉, 표 1에 나와 있는 Office 365 응용 프로그램에서 고객 데이터를 검색 및 내보낼 때는 이 도구를 사용할 수 없습니다. 그러나 Exchange Online의 원본 위치 eDiscovery 도구를 사용하여 사용자 사서함에서 콘텐츠를 검색할 수 있습니다. 또한 SharePoint Online에서 eDiscovery 센터를 사용하여 SharePoint 사이트 및 OneDrive 계정에서 콘텐츠를 검색할 수도 있습니다. 또는 문서 소유자에게 콘텐츠를 찾도록 도와달라고 요청하고 필요에 따라 콘텐츠를 변경 또는 삭제하거나 내보낼 수 있습니다. 자세한 내용은 다음을 참조하세요.
> 
> * [원본 위치 eDiscovery 검색 만들기](/exchange/create-in-place-ediscovery-search-exchange-2013-help)
> * [SharePoint Online에서 eDiscovery 센터 설정](https://support.office.com/article/Set-up-an-eDiscovery-Center-in-SharePoint-Online-A18F8975-AA7F-43B4-A7D6-001D14744D8E)

### <a name="using-content-search-to-find-personal-data"></a>콘텐츠 검색을 사용하여 개인 데이터 찾기

DSR에 응답하는 첫 번째 단계에서는 DSR의 주체인 개인 데이터를 찾습니다. 이는 Office 365 eDiscovery 도구를 사용하여 개인 데이터(Office 365에 있는 조직의 모든 데이터 중)를 검색하거나 데이터를 만든 기본 응용 프로그램으로 직접 이동하는 과정으로 구성됩니다. 이 첫 번째 단계(개인 데이터 찾기 및 검토)는 DSR이 데이터 주체 요청 수락 또는 거절에 대한 조직의 요구 사항을 충족하는지 여부를 결정하는 데 도움이 됩니다. 예를 들어 개인 데이터를 찾아서 검토한 후 다른 사용자의 권한과 자유에 부정적인 영향을 줄 수 있거나 개인 데이터가 조직에서 보유 시 적법한 비즈니스 이익이 있는 비즈니스 레코드에 포함되어 있어 요청이 조직의 요구 사항을 충족하지 못하는 것으로 결정할 수 있습니다.

앞서 언급했듯이 Microsoft는 조직의 데이터 중 90% 이상이 Word 및 Excel와 같은 Office 응용 프로그램을 사용하여 만들어지는 것으로 추정합니다. 이는 보안 및 준수 센터에서 콘텐츠 검색을 사용하여 대부분의 DSR 관련 데이터를 검색할 수 있음을 의미합니다.

이 가이드에서는 DSR 요청에 응답할 수 있는 개인 데이터를 검색하는 관리자 또는 사용자가 보안 및 준수 센터에서 콘텐츠 검색 도구를 사용하는 데 익숙하거나 경험이 있다고 가정합니다. 콘텐츠 검색 사용에 대한 일반적인 지침은 [Office 365에서 콘텐츠 검색하기](/microsoft-365/compliance/content-search)를 참조하세요. 검색을 실행하는 사용자에게 보안 및 준수 센터에서 필요한 권한이 할당되어 있는지 확인해야 합니다. 이 사용자는 보안 및 준수 센터에서 eDiscovery 매니저 역할 그룹의 구성원으로 추가되어야 합니다. [보안 및 준수 센터에서 eDiscovery 권한 할당하기](/microsoft-365/compliance/assign-ediscovery-permissions)를 참조하세요. DSR 조사에 참여하는 조직의 다른 사용자를 eDiscovery 매니저 역할 그룹에 추가하여 이들이 콘텐츠 검색 도구에서 검색 결과 미리 보기 및 내보내기와 같은 필요한 작업을 수행할 수 있도록 하는 것이 좋습니다. 그러나 준수 경계를 설정([여기](#set-up-compliance-boundaries-to-limit-the-scope-of-content-searches)의 설명 참조)하지 않은 경우 eDiscovery 매니저는 DSR 조사와 관련이 없을 수도 있는 위치를 포함하여 조직의 모든 콘텐츠 위치를 검색할 수 있습니다. 

데이터를 찾은 후에 데이터 주체의 요청을 충족하기 위한 특정 작업을 수행할 수 있습니다.

> [!NOTE]
> Office 365 Germany에서 보안 및 준수 센터는 https://protection.office.de에 있습니다.

#### <a name="searching-content-locations"></a>콘텐츠 위치 검색

콘텐츠 검색 도구를 사용하여 검색할 수 있는 콘텐츠 유형은 다음과 같습니다.

- Exchange Online 사서함. 여기에는 Microsoft 365 그룹 및 Microsoft Teams와 연관된 사서함이 포함됩니다.
- Exchange 온라인 공용 폴더
- SharePoint Online 사이트. 여기에는 Microsoft 365 그룹 및 Microsoft Teams와 연관된 사이트가 포함됩니다.
- 비즈니스용 OneDrive 계정

> [!NOTE]
> 이 가이드에서는 DSR 조사와 관련이 있을 수 있는 모든 데이터가 Office 365, 즉 Microsoft 클라우드에 저장된다고 가정합니다. 사용자의 로컬 컴퓨터에 저장되거나 조직의 파일 서버에 온-프레미스 저장된 데이터는 Office 365에 저장된 데이터에 대한 DSR 조사 범위를 벗어납니다. 온-프레미스 조직의 데이터에 대한 DSR 요청에 응답하는 방법에 대한 지침은 [Office 온-프레미스 서버에 대한 GDPR](/Office365/Enterprise/gdpr-for-office-servers)을 참조하세요.

#### <a name="tips-for-searching-content-locations"></a>콘텐츠 위치 검색을 위한 팁

- 조직에서 모든 콘텐츠 위치를 검색(단일 검색으로 검색 가능한)하여 검색 쿼리와 일치하는 항목이 포함된 콘텐츠 위치를 빠르게 확인할 수 있습니다. 그런 다음 검색을 다시 실행하여 관련 항목이 포함된 특정 위치로 검색 범위를 좁힐 수 있습니다.
- 검색 통계를 사용하여 검색 쿼리와 일치하는 항목이 포함된 주요 위치를 식별할 수 있습니다. [콘텐츠 검색 결과에 대한 주요 키워드 보기](/microsoft-365/compliance/view-keyword-statistics-for-content-search)를 참조하세요.
- 감사 로그에서 DSR의 주체인 사용자가 수행한 최근 파일 및 폴더 활동을 검색할 수 있습니다. 감사 로그를 검색하면 사용자가 최근에 상호 작용한 리소스의 이름과 위치가 포함된 감사 레코드 목록이 반환됩니다. 이 정보를 사용하여 콘텐츠 검색 쿼리를 작성할 수 있습니다. [보안 및 준수 센터에서 감사 로그 검색](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)을 참조하세요.

#### <a name="building-search-queries-to-find-personal-data"></a>검색 쿼리를 작성하여 개인 데이터 찾기

조사 중인 DSR에는 개인 데이터를 검색하기 위해 키워드 검색 쿼리에서 사용할 수 있는 식별자가 포함될 가능성이 높습니다. 개인 데이터를 찾기 위해 검색 쿼리에서 사용될 수 있는 몇 가지 일반적인 식별자는 다음과 같습니다.

- 전자 메일 주소 또는 별칭
- 전화 번호
- 우편 주소
- 직원 ID 번호
- 국가 ID 번호 또는 EU 회원국 버전의 사회 보장 번호

조사 중인 DSR에는 검색 쿼리에서 사용할 수 있는 요청의 주체인 개인 데이터에 대한 식별자 및 기타 세부 정보가 포함될 가능성이 높습니다.

전자 메일 주소나 직원 ID만 검색해도 많은 결과가 반환될 수 있습니다. DSR과 관련성이 높은 콘텐츠가 반환되도록 검색 범위를 좁히려면 검색 쿼리에 조건을 추가하면 됩니다. 조건을 추가한 경우 키워드와 검색 조건은 **AND** 부울 연산자로 논리적으로 연결됩니다. 이는 키워드 및 조건 *둘 다* 와 일치하는 항목만 검색 결과에 반환됨을 의미합니다.

다음 표에서는 검색 범위를 좁히는 데 사용할 수 있는 몇 가지 조건을 보여 줍니다. 또한 특정 문서 유형 및 사서함 항목을 검색하기 위해 각 조건에 사용할 수 있는 값을 보여 줍니다.

***표 2: 조건을 사용하여 검색 범위 좁히기***

| 조건 | 설명 | 조건 값의 예 |
| :--- | :--- |:--- |
| 파일 형식 | 문서 또는 파일의 확장명입니다. 이 조건을 사용하여 Office 365 응용 프로그램에서 만든 Office 문서 및 파일을 검색할 수 있습니다. SharePoint Online 사이트 및 비즈니스용 OneDrive 계정의 문서를 검색할 때 이 조건을 사용합니다.<br/>해당 문서 속성은 filetype입니다. <br/>검색할 수 있는 파일 확장명의 전체 목록은 SharePoint에서 크롤링되는 기본 파일 이름 확장명 및 구문 분석되는 파일 형식https://technet.microsoft.com/library/jj219530.aspx)을 참조하세요.|&nbsp;&bull;&nbsp;&nbsp;csv – CSV(쉼표로 구분된 값) 파일 검색. Excel 파일을 CSV 형식으로 저장할 수 있으며 CSV 파일을 Excel로 쉽게 가져올 수 있습니다.<br><br>&bull;&nbsp;&nbsp;docx - Word 파일 검색 <br><br>&bull;&nbsp;&nbsp;mpp – Project 파일 검색<br/><br>&bull;&nbsp;&nbsp;one – OneNote 파일 검색 <br><br>&bull;&nbsp;&nbsp;pdf - PDF 형식으로 저장된 파일 검색 <br><br>&bull;&nbsp;&nbsp;pptx – PowerPoint 파일 검색 <br><br>&bull;&nbsp;&nbsp;xlxs – Excel 파일 검색 <br><br>&bull;&nbsp;&nbsp;vsd – Visio 파일 검색 <br><br>&bull;&nbsp;&nbsp;wmv – Windows Media 동영상 파일 검색 <br>|
| 메시지 유형 | 검색할 전자 메일 메시지 유형입니다. 이 조건을 사용하여 사서함에서 연락처(사용자), 모임(일정) 작업 또는 비즈니스용 Skype 대화를 검색할 수 있습니다. 해당 전자 메일 속성은 *kind* 입니다.|&bull;&nbsp;&nbsp;*연락처 — 사서함의 내 연락처 목록(사용자) 검색 <br><br>&bull;&nbsp;&nbsp;* 전자 메일 — 전자 메일 메시지 검색 <br><br>&bull;&nbsp;&nbsp;*im — 비즈니스용 Skype 대화 검색<br><br>&bull;&nbsp;&nbsp;* 모임 — 약속 및 모임 요청(일정) 검색 <br><br>&bull;&nbsp;&nbsp;*작업 – 내 작업 목록(작업) 검색. 이 값을 사용하면 Microsoft To Do에서 만든 작업도 반환됩니다.<br>|
| 준수 태그 |전자 메일 메시지 또는 문서에 할당되는 레이블입니다. 레이블은 데이터 거버넌스를 위해 전자 메일 및 문서를 분류하고, 레이블로 정의된 분류에 따라 보존 규칙을 적용하는 데 사용됩니다. 이 조건을 사용하여 자동 또는 수동으로 레이블이 할당된 항목을 검색할 수 있습니다.<br/>조직에서는 레이블을 사용하여 데이터 개인 정보와 관련되거나 개인 데이터 또는 중요한 정보가 포함된 콘텐츠를 분류할 수 있으므로 이는 DSR 조사에 유용한 조건입니다. [보존 정책 및 보존 레이블에 대해 자세히 알아보기](/microsoft-365/compliance/labels)에서 "콘텐츠 검색을 사용하여 특정 레이블이 적용된 모든 콘텐츠 찾기" 섹션을 참조하세요.|compliancetag="개인 데이터"|
||||

보다 복잡한 검색 쿼리를 작성하는 데 사용할 수 있는 더 많은 전자 메일 및 문서 속성과 검색 조건이 있습니다. 자세한 내용은 [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](/microsoft-365/compliance/keyword-queries-and-search-conditions) 도움말 항목에서 다음 섹션을 참조하세요.

- [검색 가능한 전자 메일 속성](/microsoft-365/compliance/keyword-queries-and-search-conditions)
- [검색 가능한 사이트(문서) 속성](/microsoft-365/compliance/keyword-queries-and-search-conditions)
- [검색 조건](/microsoft-365/compliance/keyword-queries-and-search-conditions)

#### <a name="searching-for-personal-data-in-sharepoint-lists-discussions-and-forms"></a>SharePoint 목록, 토론 및 양식에서 개인 데이터 검색

문서에서 개인 데이터를 검색하는 것 외에도 콘텐츠 검색을 사용하여 기본 SharePoint Online 앱에서 만든 다른 유형의 데이터를 검색할 수 있습니다. 여기에는 SharePoint 목록, 토론 및 양식을 사용하여 만든 데이터가 포함됩니다. 콘텐츠 검색을 실행하고 SharePoint Online 사이트(또는 비즈니스용 OneDrive 계정)를 검색하면 목록, 토론 및 양식에서 검색 조건과 일치하는 데이터가 검색 결과에 반환됩니다.

##### <a name="examples-of-search-queries"></a>검색 쿼리의 예

다음은 키워드 및 조건을 사용하여 DSR에 대한 응답으로 개인 데이터를 검색하는 검색 쿼리의 몇 가지 예입니다. 이 예에서는 두 가지 버전의 쿼리, 즉 키워드 구문(조건이 키워드 상자에 포함된)과 조건이 포함된 GUI 기반 버전의 쿼리를 보여 줍니다.

##### <a name="example-1"></a>예 1

이 예에서는 SharePoint Online 사이트 및 비즈니스용 OneDrive 계정의 Excel 파일 중 지정된 전자 메일 주소가 포함된 Excel 파일을 반환합니다. 전자 메일 주소가 파일 메타데이터에 표시되는 경우 파일이 반환될 수 있습니다.

***키워드 구문***

```Query
pilar@contoso.com AND filetype="xlxs"
```

***GUI***

![키워드 대화 상자 예 1.](../media/O365-DSR-Doc_image18.png)

##### <a name="example-2&quot;></a>예 2

이 예에서는 SharePoint Online 사이트 및 비즈니스용 OneDrive 계정에 있는 Excel 또는 Word 파일 중 지정된 직원 ID 또는 생일이 포함된 Excel 또는 Word 파일을 반환합니다.

```
(98765 OR &quot;01-20-1990") AND (filetype="xlxs" OR filetype="docx")
```

***GUI***

![키워드 대화 상자 예 2.](../media/O365-DSR-Doc_image19.png)

##### <a name="example-3"></a>예 3

이 예에서는 지정된 ID 번호, 즉 프랑스 사회 보장 번호(INSEE)가 포함된 전자 메일 메시지를 반환합니다.

```Query
"1600330345678 97" AND kind="email"
```

***GUI***

![키워드 대화 상자 예 3.](../media/O365-DSR-Doc_image20.png)

#### <a name="working-with-partially-indexed-items-in-content-search"></a>콘텐츠 검색에서 부분적으로 인덱싱된 항목 사용

부분적으로 인덱싱된 항목(*인덱싱되지 않은 항목* 이라고도 함)은 SharePoint Online 및 비즈니스용 OneDrive 사이트에서 어떤 이유로 검색에 대해 인덱싱되지 않아 콘텐츠 검색을 사용하여 검색할 수 없는 Exchange Online 사서함 항목 및 문서입니다. 대부분의 전자 메일 메시지 및 사이트 문서는 [Office 365에 인덱싱 제한](/microsoft-365/compliance/limits-for-content-search) 내에 속하기 때문에 성공적으로 인덱싱됩니다. 전자 메일 메시지 또는 파일이 검색에 대해 인덱싱되지 않는 이유는 다음과 같습니다.

- 파일 형식이 [인식할 수 없거나 인덱싱에 지원되지 않는](/microsoft-365/compliance/partially-indexed-items-in-content-search) 파일 형식입니다. 간혹 인덱싱에 대해 지원되는 경우도 있지만 특정 파일에 대해 인덱싱 오류가 발생합니다.
- 전자 메일 메시지에 이미지 파일(부분적으로 인덱싱된 전자 메일 항목의 가장 일반적인 사유)과 같은 유효한 처리기가 없는 첨부 파일이 있습니다.
- 전자 메일 메시지에 첨부된 파일이 너무 크거나 첨부 파일이 너무 많습니다.

DSR 요청에 응답할 때 작업할 수 있도록 부분적으로 인덱싱된 항목에 대해 보다 자세히 알아보는 것이 좋습니다. 자세한 내용은 다음을 참조하세요.

- [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](/microsoft-365/compliance/partially-indexed-items-in-content-search)
- [Office 365 eDiscovery에서 부분적으로 인덱싱된 항목 조사](/microsoft-365/compliance/investigating-partially-indexed-items-in-ediscovery)
- [인덱싱되지 않은 항목 내보내기](/microsoft-365/compliance/export-search-results)

#### <a name="tips-for-working-with-partially-indexed-items"></a>부분적으로 인덱싱된 항목 사용을 위한 팁

DSR 조사에 응답하는 데이터가 부분적으로 인덱싱된 항목에 있을 수도 있습니다. 부분적으로 인덱싱된 항목 사용에 대한 몇 가지 제안 사항은 다음과 같습니다.

- 검색을 실행한 후 예상되는 부분적으로 인덱싱된 항목 수가 검색 통계에 표시됩니다. 이 예상에는 SharePoint Online 및 비즈니스용 OneDrive의 부분적으로 인덱싱된 항목은 포함되지 않습니다. 부분적으로 인덱싱된 항목에 대한 정보를 가져오려면 콘텐츠 검색에 대한 보고서를 내보냅니다. **Unindexed Items.csv** 보고서에는 항목의 위치, URL(항목이 SharePoint Online 또는 비즈니스용 OneDrive에 있는 경우) 및 제목 줄(메시지의 경우)이나 문서 이름을 포함하여 부분적으로 인덱싱된 항목에 대한 정보가 포함됩니다. 자세한 내용은 [콘텐츠 검색 보고서 내보내기](/microsoft-365/compliance/export-a-content-search-report)를 참조하세요.

- 콘텐츠 검색 결과와 함께 반환되는 통계 및 부분적으로 인덱싱된 항목 목록은 모두 검색된 콘텐츠 위치의 부분적으로 인덱싱된 항목입니다.

- 잠재적으로 DSR 조사에 응답하는 부분적으로 인덱싱된 항목을 검색하려면 다음 중 하나를 수행하면 됩니다.

##### <a name="export-all-partially-indexed-items"></a>모든 부분적으로 인덱싱된 항목 내보내기

검색된 위치에서 콘텐츠 검색 결과와 부분적으로 인덱싱된 항목을 모두 내보낼 수 있습니다. 또한 부분적으로 인덱싱된 항목만 내보낼 수도 있습니다. 그런 다음 해당 기본 응용 프로그램에서 열고 콘텐츠를 검토할 수 있습니다. SharePoint Online 및 비즈니스용 OneDrive에서 항목을 내보내려면 이 옵션을 사용해야 합니다. [보안 및 준수 센터에서 콘텐츠 검색 결과 내보내기](/microsoft-365/compliance/export-search-results)를 참조하세요.

##### <a name="export-a-specific-set-of-partially-indexed-items-from-mailboxes"></a>사서함에서 부분적으로 인덱싱된 항목의 특정 집합 내보내기

검색에서 모든 부분적으로 인덱싱된 사서함 항목을 내보내는 대신 콘텐츠 검색을 다시 실행하여 부분적으로 인덱싱된 항목의 특정 목록을 검색한 다음 내보낼 수 있습니다. 이 작업은 사서함 항목에만 수행할 수 있습니다. [Office 365에서 대상이 지정된 콘텐츠 검색을 위한 CSV 파일 준비](/microsoft-365/compliance/csv-file-for-an-id-list-content-search)를 참조하세요.

### <a name="next-steps"></a>다음 단계

DSR과 관련된 개인 데이터를 찾은 후에는 데이터를 찾는 데 사용한 특정 콘텐츠 검색을 유지해야 합니다. [복사본 가져오기](#providing-a-copy-of-personal-data), [내보내기](#exporting-personal-data), [영구적으로 삭제하기](#deleting-personal-data) 등 DSR 응답 프로세스의 다른 단계를 완료하는 데 이 검색을 다시 사용할 수 있습니다.

### <a name="additional-considerations-for-selected-applications"></a>선택한 응용 프로그램에 대한 추가 고려 사항

다음 섹션에서는 아래의 Office 365 응용 프로그램에서 데이터를 검색할 때 염두에 두어야 하는 사항을 설명합니다.

- [Office Lens](#office-lens)
- [비즈니스용 OneDrive 및 SharePoint 환경 설정](#onedrive-for-business-and-sharepoint-online-experience-settings)
- [교육용 Microsoft Teams](#microsoft-teams-for-education)
- [Microsoft To Do](#microsoft-to-do)
- [비즈니스용 Skype](#skype-for-business)

#### <a name="office-lens"></a>Office Lens

Office Lens(iOS, Android 및 Windows를 실행하는 장치에서 지원되는 카메라 앱) 사용자는 화이트보드, 하드 카피 문서, 명함 및 기타 많은 텍스트가 포함된 것의 사진을 찍을 수 있습니다. Office Lens는 이미지에서 텍스트를 추출하여 Word, PowerPoint 및 OneNote와 같은 Office 문서 또는 PDF 파일로 저장하는 광학 문자 인식 기술을 사용합니다. 사용자는 이미지의 텍스트가 포함된 파일을 Office 365에서 비즈니스용 OneDrive 계정에 업로드할 수 있습니다. 따라서 콘텐츠 검색 도구를 사용하여 Office Lens 이미지에서 생성된 파일의 데이터를 검색, 액세스, 삭제 및 내보낼 수 있습니다. Office Lens에 대한 자세한 내용은 다음을 참조하세요.

- [iOS용 Office Lens](https://support.microsoft.com/office/microsoft-office-lens-for-ios-fbdca5f4-1b1b-4391-a931-dc1c2582397b)
- [Android용 Office Lens](https://support.office.com/article/Office-Lens-for-Android-ec124207-0049-4201-afaf-b5874a8e6f2b)
- [Windows용 Office Lens](https://support.microsoft.com/office/office-lens-for-windows-577ec09d-8da2-4029-8bb7-12f8114f472a)

#### <a name="onedrive-for-business-and-sharepoint-online-experience-settings"></a>비즈니스용 OneDrive 및 SharePoint Online 환경 설정

비즈니스용 OneDrive 계정과 SharePoint Online 사이트에 저장된 사용자가 만든 파일 외에도 이러한 서비스는 다양한 환경을 지원하는 데 사용되는 사용자에 대한 정보를 저장합니다. 조직의 사용자는 여전히 제품 내 기능을 사용하여 이러한 정보의 대부분에 액세스할 수 있습니다. 다음 정보는 비즈니스용 OneDrive 및 SharePoint Online 응용 프로그램 데이터를 액세스하고, 보고, 내보내는 방법에 대한 지침을 제공합니다.

##### <a name="sharepoint-user-profiles"></a>SharePoint 사용자 프로필

사용자는 자신의 Delve 프로필을 통해 생일, 휴대폰 번호(및 기타 연락처 정보), 자기 소개, 프로젝트, 기술 및 전문 지식, 학력, 관심사, 취미 등 SharePoint Online 사용자 프로필에 저장된 속성을 유지 관리할 수 있습니다.

###### <a name="end-users"></a>최종 사용자

최종 사용자는 Delve 프로필 환경을 사용하여 SharePoint Online 사용자 프로필을 검색, 액세스 및 수정할 수 있습니다. 자세한 내용은 [Office Delve에서 프로필 보기 및 업데이트](https://support.office.com/article/view-and-update-your-profile-in-office-delve-4e84343b-eedf-45a1-aeb9-8627ccca14ba)를 참조하세요.

사용자가 자신의 SharePoint 프로필 데이터에 액세스하는 또 다른 방법은 비즈니스용 OneDrive 계정에서 **프로필 편집 페이지** 로 이동하는 것입니다. 이 페이지에 액세스하려면 비즈니스용 OneDrive 계정 URL 아래의 **EditProfile.aspx** 경로로 이동하면 됩니다. 예를 들어 <strong>user1@contoso.com</strong> 사용자의 경우 비즈니스용 OneDrive 계정은 다음 위치에 있습니다.

```http
https://contoso-my.sharepoint.com/personal/user1\_contoso\_com/\_layouts/15/OneDrive.aspx
```

프로필 편집 페이지의 URL은 다음과 같습니다.

```http
https://contoso-my.sharepoint.com/personal/user1\_contoso\_com/\_layouts/15/EditProfile.aspx
```

Azure Active Directory에서 제공되는 속성은 SharePoint Online 내에서 변경할 수 없습니다. 그러나 사용자는 Office 365 헤더에서 자신의 **사진** 을 선택한 다음 **내 계정** 을 선택하여 **계정** 페이지로 이동할 수 있습니다. 여기에서 속성을 변경하려면 사용자가 관리자와 함께 사용자 프로필 속성을 검색, 액세스 또는 수정해야 할 수 있습니다.

###### <a name="admins"></a>관리자

관리자는 SharePoint 관리 센터에서 프로필 속성을 보고, 액세스하고, 수정할 수 있습니다. **SharePoint 관리 센터** 에서 **사용자 프로필** 탭을 선택하고 **사용자 프로필 관리** 를 선택한 다음 사용자의 이름을 입력하고 **찾기** 를 선택합니다. 관리자는 사용자를 마우스 오른쪽 단추로 선택하고 **내 프로필 편집** 을 선택할 수 있습니다. Azure Active Directory에서 제공되는 속성은 SharePoint Online 내에서 변경할 수 없습니다.

관리자는 SharePoint Online PowerShell에서 **Export-SPOUserProfile** cmdlet을 사용하여 사용자의 모든 사용자 프로필 속성을 내보낼 수 있습니다. [Export-SPOUserProfile](/powershell/module/sharepoint-online/export-spouserprofile)을 참조하세요.

사용자 프로필에 대한 자세한 내용은 [SharePoint 관리 센터에서 사용자 프로필 관리](/sharepoint/manage-user-profiles)를 참조하세요.

##### <a name="user-information-list-on-sharepoint-online-sites"></a>SharePoint Online 사이트의 사용자 정보 목록

사용자의 SharePoint 사용자 프로필 하위 집합은 사용자가 방문하거나 액세스 권한이 있는 모든 사이트의 사용자 정보 목록에 동기화됩니다. 이는 문서 라이브러리의 사용자 열과 같은 SharePoint Online 환경에서 문서 작성자의 이름과 같은 사용자에 대한 기본 정보를 표시하는 데 사용됩니다. 사용자 정보 목록의 데이터는 SharePoint 사용자 프로필에 저장된 정보와 일치하며, 원본이 변경되면 자동으로 수정됩니다. 삭제된 사용자의 경우 SharePoint 열 필드의 참조 무결성을 위해 상호 작용하는 사이트에서 이 데이터가 그대로 유지됩니다. 

관리자는 SharePoint 관리 센터 내에서 복제할 수 있는 속성을 제어할 수 있습니다. 이렇게 하려면 다음을 수행합니다.

1. **SharePoint 관리 센터** 로 이동하여 **사용자 프로필** 탭을 선택합니다.
2. **사용자 속성 관리** 를 선택하여 속성 목록을 표시합니다.
3. 속성을 마우스 오른쪽 단추로 선택하고 **편집** 을 선택하여 다양한 설정을 조정합니다.
4. **정책 설정** 아래의 복제 가능 속성은 속성이 사용자 정보 목록에 표시되는지 여부를 제어합니다. 일부 속성은 이러한 조정을 지원하지 않습니다.

관리자는 SharePoint Online PowerShell에서 **Export-SPOUserInfo** cmdlet을 사용하여 지정된 사이트에서 사용자의 모든 사용자 정보 속성을 내보낼 수 있습니다. [Export-SPOUserInfo](/powershell/module/sharepoint-online/export-spouserinfo)를 참조하세요.

##### <a name="onedrive-for-business-experience-settings"></a>비즈니스용 OneDrive 환경 설정

사용자의 비즈니스용 OneDrive 환경에서는 사용자가 관심 있는 콘텐츠를 찾고 탐색하는 데 도움이 되는 정보를 저장합니다. 최종 사용자는 해당 제품 내 기능을 사용하여 이 정보의 대부분에 액세스할 수 있습니다. 관리자는 [PowerShell 스크립트](/powershell/scripting/overview) 및 [SharePoint CSOM(클라이언트 쪽 개체 모델)](/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-client-library-code) 명령을 사용하여 정보를 내보낼 수 있습니다.

설정, 설정이 저장되는 방식 및 내보내는 방법에 대한 자세한 내용은 [비즈니스용 OneDrive 환경 설정 내보내기](/sharepoint/export-odfb-lists)를 참조하세요.

##### <a name="onedrive-for-business-and-sharepoint-online-search"></a>비즈니스용 OneDrive 및 SharePoint Online 검색

비즈니스용 OneDrive 및 SharePoint Online의 앱 내 검색 환경은 사용자의 검색 쿼리를 30일 동안 저장하여 검색 결과의 관련성을 높입니다. 관리자는 SharePoint Online PowerShell에서 **Export-SPOQueryLogs** cmdlet을 사용하여 사용자의 검색 쿼리를 내보낼 수 있습니다. [Export-SPOQueryLogs](/powershell/module/sharepoint-online/export-spoquerylogs)를 참조하세요.

#### <a name="microsoft-teams-for-education"></a>교육용 Microsoft Teams

교육용 Microsoft Teams는 교사와 학생들이 개인 데이터를 만들고 저장하는 데 사용할 수 있는 두 가지 추가 공동 작업 기능인 과제와 OneNote 수업용 전자 필기장을 제공합니다. 콘텐츠 검색을 사용하여 이 두 기능 모두에서 데이터를 검색할 수 있습니다.

##### <a name="assignments"></a>Assignments

과제와 연관된 학생 파일은 해당 Teams SharePoint Online 사이트의 문서 라이브러리에 저장됩니다. IT 관리자는 콘텐츠 검색 도구를 사용하여 과제와 연관된 학생 파일을 검색할 수 있습니다. 예를 들어 관리자는 조직의 모든 SharePoint Online 사이트를 검색하고 검색 쿼리에서 학생의 이름과 수업 또는 과제 이름을 사용하여 DSR과 관련된 데이터를 찾을 수 있습니다.

수업 팀 SharePoint Online 사이트에 저장되지 않는 과제와 관련된 다른 데이터가 있습니다. 이러한 데이터는 콘텐츠 검색으로 검색할 수 없으며 다음과 같습니다.

- 교사가 과제의 일환으로 학생에게 할당하는 파일
- 학생의 성적과 교사의 피드백
- 각 학생이 과제에 대해 제출한 문서 목록
- 과제 메타데이터

이 데이터 유형의 경우 IT 관리자 또는 데이터 소유자(예: 교사)는 DSR과 관련된 데이터를 찾기 위해 수업 팀의 과제로 이동해야 할 수도 있습니다.

##### <a name="onenote-class-notebook"></a>OneNote 수업용 전자 필기장

OneNote 수업용 전자 필기장은 수업 팀 SharePoint Online 사이트에 저장됩니다. 학급의 모든 학생에게는 교사와 공유되는 개인 전자 필기장이 있습니다. 또한 교사가 학생들과 문서를 공유할 수 있는 콘텐츠 라이브러리 및 학습의 모든 학생을 위한 공동 작업 공간도 있습니다. 이러한 기능과 관련된 데이터는 콘텐츠 검색을 사용하여 검색할 수 있습니다.

수업용 전자 필기장을 검색하기 위한 특정 지침은 다음과 같습니다.

1. 다음 검색 조건을 사용하여 콘텐츠 검색을 실행합니다.

   - 모든 SharePoint Online 사이트 검색
   - 수업 팀의 이름(예: “9C Biology”)을 검색 키워드로 포함합니다.

2. 검색 결과를 미리 보고 수업용 전자 필기장에 해당하는 항목을 찾습니다.
3. 이 항목을 선택한 다음 세부 정보 창에 표시되는 폴더 경로를 복사합니다. 이 폴더는 수업용 전자 필기장의 루트 폴더입니다.
4. 1단계에서 만든 검색을 편집하여 키워드 쿼리의 학습 이름을 수업용 전자 필기장의 폴더 경로로 바꾸고 이 폴더 경로 앞에 **path** 사이트 속성을 입력합니다(예: **path:"<https://contosoedu.onmicrosoft.com/sites/9C> Biology/SiteAssets/9C Biology Notebook/"**). 따옴표와 후행 슬래시를 포함해야 합니다.
5. 검색 조건을 추가하고 파일 형식 조건을 선택한 후 파일 형식 값에 one을 사용합니다. 그러면 검색 결과에 모든 OneNote 파일이 반환됩니다. 결과 키워드 구문은 [다음](#building-search-queries-to-find-personal-data)과 같습니다.

   ```Query
   path:"<https://contosoedu.onmicrosoft.com/sites/9C> Biology/SiteAssets/9C Biology Notebook/" AND filetype="one"
   ```

6. 콘텐츠 검색을 다시 실행합니다. 검색 결과에 수업 팀의 수업용 전자 필기장에 대한 모든 OneNote 파일이 포함되어야 합니다.

#### <a name="microsoft-to-do"></a>Microsoft To Do

Microsoft To-Do의 Tasks(*할 일* 이라고 하며, *할 일 목록* 에 저장됨)은 사용자의 Exchange Online 사서함에 작업으로 저장됩니다. 따라서 콘텐츠 검색 도구를 사용하여 할 일을 검색, 액세스, 삭제 및 내보낼 수 있습니다. 자세한 내용은 [Microsoft To-Do 설정](https://support.microsoft.com/office/set-up-microsoft-to-do-490c1a8c-2333-4952-8125-841afadb9620)을 참조하세요.

#### <a name="skype-for-business"></a>비즈니스용 Skype

비즈니스용 Skype에서 개인 데이터를 액세스하고, 보고, 내보내는 방법에 대한 몇 가지 추가 정보는 다음과 같습니다.

- 모임에 첨부된 파일은 실제 모임에서 180일 동안 유지된 후 액세스할 수 없게 됩니다. 모임 참가자는 모임 요청에서 모임에 참석하여 첨부된 파일을 보거나 다운로드하는 방식으로 이러한 파일에 액세스할 수 있습니다. [비즈니스용 Skype 모임에 대한 첨부 파일 미리 로드](https://support.microsoft.com/office/preload-attachments-for-a-skype-for-business-meeting-fd3d9f9d-b448-4754-b813-02e49393f251)에서 "모임에 첨부 파일 사용" 섹션을 참조하세요.
- 비즈니스용 Skype의 대화는 사용자 사서함의 대화 내용 폴더에 보관됩니다. 콘텐츠 검색을 사용하여 사서함에서 Skype 대화 내의 데이터를 검색할 수 있습니다.
- 데이터 주체는 비즈니스용 Skype에서 자신의 대화 상대를 내보낼 수 있습니다. 이렇게 하려면 비즈니스용 Skype에서 대화 상대 그룹을 마우스 오른쪽 단추로 선택하고 **복사** 를 선택합니다. 그런 다음 전자 메일 주소 목록을 텍스트 또는 Word 문서에 붙여넣을 수 있습니다.
- 모임 참가자의 Exchange Online 사서함에 소송 보존이 적용되거나 Office 365 보존 정책이 할당된 경우 모임에 첨부된 파일은 참가자의 사서함에 보존됩니다. 파일 보존 기간이 만료되지 않은 경우 콘텐츠 검색을 사용하여 참가자의 사서함에서 이러한 파일을 검색할 수 있습니다. 파일 보존에 대한 자세한 내용은 [비즈니스용 Skype 모임에 첨부된 대용량 파일 보존](/skypeforbusiness/set-up-policies-in-your-organization/retaining-large-files-attached-to-a-meeting)을 참조하세요.

## <a name="providing-a-copy-of-personal-data"></a>개인 데이터의 복사본 제공

DSR에 응답하는 개인 데이터를 찾은 후 여러분과 조직은 데이터 주체에게 제공할 데이터를 결정해야 합니다. 예를 들어 실제 문서의 사본, 적절히 편집된 버전 또는 공유할 수 있는 부분의 스크린샷을 제공할 수 있습니다. 액세스 요청에 대한 이러한 각 응답에 대해, 응답 데이터를 포함하는 문서 또는 기타 항목 사본을 검색해야 합니다.

데이터 주체에 사본을 제공할 때는 다른 데이터 주체에 대한 개인 정보와 모든 기밀 정보를 제거하거나 편집해야 할 수 있습니다.

### <a name="using-content-search-to-get-a-copy-of-personal-data"></a>콘텐츠 검색을 사용하여 개인 데이터의 복사본 가져오기

콘텐츠 검색을 사용하여 검색을 실행한 후 찾은 문서 또는 사서함 항목의 복사본을 가져오는 두 가지 방법이 있습니다.

- 검색 결과를 미리 본 후 문서 또는 항목의 복사본을 다운로드합니다. 이는 몇 가지 항목 또는 파일을 다운로드하는 데 적절한 방법입니다.
- 검색 결과를 내보낸 다음 검색에서 반환되는 모든 항목의 복사본을 다운로드합니다. 이 방법은 보다 복잡하지만 DSR에 응답하는 많은 항목을 다운로드하는 데 적절한 방법입니다. 검색 결과 내보내기에는 유용한 보고서도 포함됩니다. 이러한 보고서를 사용하여 각 항목에 대한 추가 정보를 얻을 수 있습니다. **Results.csv** 보고서는 항목의 정확한 위치(예: 전자 메일 메시지의 사서함 또는 SharePoint Online 및 비즈니스용 OneDrive 사이트에 있는 문서나 목록의 URL)와 같은 내보낸 항목에 대한 많은 정보를 포함하므로 유용합니다. DSR 조사 프로세스에서 항목의 소유자에게 연락해야 하는 경우 이 정보를 통해 해당 소유자를 식별할 수 있습니다. 검색 결과를 내보낼 때 포함되는 보고서에 대한 자세한 내용은 [콘텐츠 검색 보고서 내보내기](/microsoft-365/compliance/export-a-content-search-report)를 참조하세요.

#### <a name="preview-and-download-items"></a>항목 미리 보기 및 다운로드

새 검색을 실행하거나 기존 검색을 연 후 검색 쿼리와 일치한 각 항목을 미리 보고 해당 항목이 현재 조사 중인 DSR과 관련이 있는지 확인할 수 있습니다. 여기에는 검색 결과에서 반환되는 SharePoint 목록 및 웹 페이지도 포함됩니다. 또한 데이터 주체에게 제공해야 하는 경우 원본 파일도 다운로드할 수 있습니다. 두 경우 모두 데이터 주체의 정보 요청을 충족하기 위해 스크린샷을 만들 수 있습니다.

일부 유형의 항목은 미리 볼 수 없습니다. 항목 또는 파일 형식의 미리 보기가 지원되지 않는 경우 로컬 컴퓨터나 매핑된 네트워크 드라이브 또는 다른 네트워크 위치에 개별 항목을 다운로드할 수 있습니다. [지원되는 파일 형식](/microsoft-365/compliance/content-search)만 미리 볼 수 있습니다.

항목을 미리 보고 다운로드하려면

1. 보안 및 준수 센터에서 콘텐츠 검색을 엽니다.
2. 결과가 표시되지 않으면 **결과 미리 보기** 를 선택합니다.
3. 항목을 선택하여 확인합니다.
4. **원본 파일 다운로드** 를 선택하여 항목을 로컬 컴퓨터에 다운로드합니다. 미리 볼 수 없는 항목도 다운로드해야 합니다.

검색 결과 미리 보기에 대한 자세한 내용은 [검색 결과 미리 보기](/microsoft-365/compliance/content-search)를 참조하세요.

#### <a name="export-and-download-items"></a>항목 내보내기 및 다운로드

콘텐츠 검색 결과를 내보내 개인 데이터가 포함된 전자 메일 메시지, 문서, 목록 및 웹 페이지의 복사본을 가져올 수도 있습니다. 물론 이 방법은 항목 미리 보기보다 더 복잡합니다. [콘텐츠 검색 결과 내보내기](#export-and-download-content-using-content-search)에 대한 자세한 내용은 다음 섹션을 참조하세요.

## <a name="exporting-personal-data"></a>개인 데이터 내보내기

"데이터 이동권"을 통해 데이터 주체는 "구조화되고 자주 사용되며 컴퓨터가 읽을 수 있는 형식"으로 된 개인 데이터의 전자 복사본을 요청하고, 조직에서 이러한 전자 파일을 다른 데이터 통제자에게 전송하도록 요청할 수 있습니다. Microsoft는 다음 두 가지 방법으로 이 권한을 지원합니다.

- 컴퓨터가 읽을 수 있고 자주 사용되는 기본 전자 형식으로 데이터를 저장하는 Office 365 응용 프로그램을 제공합니다. Office 파일 형식에 대한 자세한 내용은 [Office 파일 형식-기술 문서](https://msdn.microsoft.com/library/office/cc313105(v=office.12).aspx)를 참조하세요.
- 조직에서 기본 파일 형식 또는 다른 응용 프로그램으로 쉽게 가져올 수 있는 형식(예: CSV, TXT 및 JSON)으로 데이터를 내보내도록 지원합니다.

DSR 내보내기 요청을 충족하기 위해 Office 문서를 해당 기본 파일 형식으로 내보내고, 다른 Office 365 응용 프로그램에서 데이터를 내보낼 수 있습니다.

### <a name="export-and-download-content-using-content-search"></a>콘텐츠 검색을 사용하여 콘텐츠 내보내기 및 다운로드

콘텐츠 검색 결과를 내보내는 경우 PST 파일 또는 개별 메시지(.msg 파일)로 전자 메일 항목을 다운로드할 수 있습니다. SharePoint Online 및 비즈니스용 OneDrive 사이트에서 문서 및 목록을 내보낼 때는 기본 파일 형식의 복사본을 내보냅니다. 예를 들어 SharePoint 목록은 CSV 파일로 내보내고, 웹 페이지는 .aspx 또는 html 파일로 내보냅니다.

> [!NOTE]
> 콘텐츠 검색을 사용하여 사용자의 사서함에서 사서함 항목을 내보려면 사용자(항목을 내보내는 사서함의 소유자)에게 Exchange Online 요금제 2 라이선스가 할당되어 있어야 합니다. 

항목을 내보내고 다운로드하려면

1. 보안 및 준수 센터에서 콘텐츠 검색을 엽니다.
2. 검색 플라이아웃 페이지에서 ![다운로드 아이콘](../media/o365-dsr_image21.png) **자세히** 를 선택한 다음 **결과 내보내기** 를 선택합니다. 보고서를 내보낼 수도 있습니다.
3. **결과 내보내기** 플라이아웃 페이지의 섹션을 완료합니다. 스크롤 막대를 사용하여 모든 내보내기 옵션을 확인해야 합니다.
4. 보안 및 준수 센터의 콘텐츠 검색 페이지로 돌아가 **내보내기** 탭을 선택합니다.
5. **새로 고침** 을 선택하여 페이지를 업데이트합니다.
6. **이름** 열에서 방금 만든 내보내기 작업을 선택합니다. 내보내기 작업의 이름은 **\_내보내기** 가 추가된 콘텐츠 검색의 이름입니다.
7. 내보내기 플라이아웃 페이지의 **내보내기 키** 에서 **클립보드로 복사를 선택** 합니다. 10단계에서 이 키를 사용하여 검색 결과를 다운로드하게 됩니다.
8. 플라이아웃 페이지 위쪽에서 ![다운로드 아이콘](../media/o365-dsr_image21.png) **결과 다운로드** 를 선택합니다.
9. **Microsoft Office 365 eDiscovery 내보내기 도구** 를 설치하라는 메시지가 표시되면 **설치** 를 선택합니다.
10. **eDiscovery 내보내기 도구** 에서 7단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다.
11. **찾아보기** 를 선택하여 검색 결과 파일을 다운로드하려는 위치를 지정합니다.
12. **시작** 을 선택하여 컴퓨터에 검색 결과를 다운로드합니다.

내보내기 프로세스가 완료되면 로컬 컴퓨터의 다운로드된 위치에서 파일에 액세스할 수 있습니다. 콘텐츠 검색 결과는 Content Search라는 폴더에 다운로드되고, 사이트의 문서는 **SharePoint** 라는 하위 폴더에 복사되며, 사서함 항목은 **Exchange** 라는 하위 폴더에 복사됩니다.

자세한 단계별 지침은 [보안 및 준수 센터에서 콘텐츠 검색 결과 내보내기](/microsoft-365/compliance/export-search-results)를 참조하세요.

### <a name="downloading-documents-and-lists-from-sharepoint-online-and-onedrive-for-business"></a>SharePoint Online 및 비즈니스용 OneDrive에서 문서 및 목록 다운로드

SharePoint Online 및 비즈니스용 OneDrive에서 데이터를 내보내는 또 다른 방법은 SharePoint Online 사이트 또는 비즈니스용 OneDrive 계정에서 문서 및 목록을 직접 다운로드하는 것입니다. 사이트 액세스 권한을 할당 받은 다음 사이트로 이동하여 콘텐츠를 다운로드해야 합니다. 다음을 참조하세요.

- [OneDrive 또는 SharePoint에서 파일 및 폴더 다운로드](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05)
- [SharePoint 목록을 Excel로 내보내기](https://support.office.com/article/export-to-excel-from-sharepoint-bfb2ea48-6118-4fa9-abb6-cced9424e5d9)

일부 DSR 내보내기 요청의 경우 데이터 주체가 직접 콘텐츠를 다운로드하도록 허용할 수 있습니다. 이 경우 데이터 주체는 SharePoint Online 사이트 또는 공유 폴더로 이동한 후 **동기화** 를 선택하여 문서 라이브러리 또는 선택한 폴더의 모든 콘텐츠를 동기화할 수 있습니다. 다음을 참조하세요.

- [사용자가 새 OneDrive 동기화 클라이언트를 사용하여 SharePoint 파일을 동기화하도록 설정](/sharepoint/let-users-use-new-onedrive-sync-client)
- [새 OneDrive 동기화 클라이언트를 사용하여 SharePoint 파일 동기화](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-client-6de9ede8-5b6e-4503-80b2-6190f3354a88)

## <a name="deleting-personal-data"></a>개인 데이터 삭제

조직의 고객 데이터에서 개인 데이터를 제거할 수 있는 "삭제권"은 GDPR의 주요 보호 기능입니다. 개인 데이터 제거에는 전체 문서 또는 파일 삭제, 문서 또는 파일 내의 특정 데이터 삭제(이 가이드의 수정 섹션에 설명된 것과 같은 작업 및 프로세스) 등이 포함됩니다.

DSR에 응답하여 개인 데이터를 조사하거나 삭제할 준비를 할 때 Office 365에서 데이터 삭제(및 보존)가 작동하는 방식에 대해 이해해야 할 몇 가지 사항은 다음과 같습니다.

- **일시 삭제와 영구 삭제**: Exchange Online, SharePoint Online 및 비즈니스용 OneDrive와 같은 Office 365 서비스에는 복구할 기회 없이 Microsoft 클라우드에서 영구적으로 제거되기 전에 삭제된 항목의 복구 가능성(일반적으로 제한된 기간 동안)과 관련된 *일시 삭제* 및 *영구 삭제* 개념이 있습니다. 이 맥락에서 일시 삭제된 항목은 영구 삭제되기 전에 제한된 기간 동안 사용자 및/또는 관리자에 의해 복구될 수 있습니다. 항목이 영구 삭제된 경우에는 영구 제거로 표시되고 해당 Office 365 서비스에서 처리되는 때에 삭제됩니다. 사서함 및 사이트에서 항목에 대해 일시 삭제 및 영구 삭제가 작동하는 방식은 다음과 같습니다(항목을 데이터 소유자가 삭제하든 관리자가 삭제하든 상관없음).

  - **사서함:** 지운 편지함 폴더에서 삭제되거나 사용자가 **Shift+Del** 을 눌러 삭제하는 경우 항목은 일시 삭제됩니다. 일시 삭제된 항목은 사서함의 복구 가능한 항목 폴더로 이동합니다. 이때 사용자는 삭제된 항목 보존 기간(Office 365에서는 삭제된 항목 보존 기간이 14일이지만 관리자가 최대 30일로 늘릴 수 있음)이 만료될 때까지 해당 항목을 복구할 수 있습니다. 보존 기간이 만료된 후에는 항목이 영구 삭제되고 숨겨진 폴더(*제거* 폴더라고 함)로 이동합니다. 이 항목은 다음에 사서함이 처리될 때(사서함은 7일마다 한 번 처리됨) Office 365에서 영구적으로 제거됩니다.

  - **SharePoint Online 및 비즈니스용 OneDrive 사이트**: 파일 또는 문서가 삭제되면 사이트의 휴지통(*1단계 휴지통* 이라고도 하며, Windows의 휴지통과 유사함)으로 이동합니다. 이 항목은 93일(Office 365의 사이트에 대한 삭제된 항목 보존 기간) 동안 휴지통에서 유지됩니다. 이 기간이 지나면 항목은 사이트 모음의 휴지통(*2단계 휴지통* 이라고도 함)으로 자동으로 이동합니다(적절한 권한을 가진 사용자 또는 관리자가 1단계 휴지통에서 항목을 삭제할 수도 있음). 이때 항목은 일시 삭제되며 여전히 SharePoint Online의 사이트 모음 관리자 또는 비즈니스용 OneDrive의 사용자 또는 관리자에 의해 복구될 수 있습니다. 항목이 2단계 휴지통에서 삭제(수동 또는 자동으로)되면 영구 삭제되고 사용자 또는 관리자가 액세스할 수 없게 됩니다. 1단계 휴지통과 2단계 휴지통 모두 보존 기간은 93일입니다. 즉, 2단계 휴지통 보존은 항목이 처음 삭제된 경우에 시작되므로 총 최대 보존 기간은 두 휴지통 모두 93일입니다.

> [!NOTE]
> 항목이 일시 삭제되거나 영구 삭제되는 작업을 이해하면 삭제 요청에 응답할 때 GDPR 요구 사항을 충족하는 방식으로 데이터를 삭제하는 방법을 결정하는 데 도움이 됩니다.

- **법적 보존 및 보존 정책:** Office 365에서 "보존"은 사서함 및 사이트에 적용될 수 있습니다. 즉, 사서함 또는 사이트가 보존 상태인 경우 항목의 보존 기간이 만료되거나 보존이 제거될 때까지 어떤 항목도 영구적으로 제거(영구 삭제)되지 않습니다. 이는 DSR에 응답하여 고객 콘텐츠를 삭제하는 맥락에서 중요합니다. 항목이 보존 중인 콘텐츠 위치에서 영구 삭제되는 경우 이 항목은 Office 365에서 영구적으로 제거되지 않습니다. 즉, IT 관리자가 복구할 수 있습니다. 조직에 DSR에 대한 응답으로 데이터가 영구적으로 삭제되고 Office 365에서 복구할 수 없는 요구 사항이나 정책이 있는 경우에는 사서함 또는 사이트에서 보존이 제거되어 Office 365에서 데이터가 영구적으로 삭제됩니다. DSR 응답에 대한 조직의 지침에는 특정 DSR 삭제 요청이 우선인지 법적 보존이 우선인지 결정하기 위한 프로세스가 있습니다. 보존이 제거되어 항목이 삭제되는 경우 항목이 삭제된 후 보존을 다시 구현할 수 있습니다.

### <a name="deleting-documents-in-sharepoint-online-and-onedrive-for-business"></a>SharePoint Online 및 비즈니스용 OneDrive에서 문서 삭제

SharePoint Online 사이트 또는 비즈니스용 OneDrive 계정에서 삭제해야 하는 문서를 찾은 후(이 가이드의 검색 섹션에 설명된 지침 참조) 데이터 개인 정보 관리자 또는 IT 관리자는 필요한 권한을 할당 받아야 사이트에 액세스하고 문서를 삭제할 수 있습니다. 해당되는 경우 문서 소유자에게 문서를 삭제하도록 지시할 수도 있습니다.

사이트에서 문서를 삭제하기 위한 대략적인 프로세스는 다음과 같습니다.

1. 사이트로 이동하여 문서를 찾습니다.
2. 문서를 삭제합니다. 사이트에서 문서를 삭제하면 1단계 휴지통으로 문서가 전송됩니다.
3. 1단계 휴지통(사이트 휴지통)으로 이동하여 이전 단계에서 삭제한 동일한 문서를 삭제합니다. 이 문서는 2단계 휴지통으로 전송됩니다. **이때 이 문서는 일시 삭제됩니다**.
4. 2단계 휴지통(사이트 모음 휴지통)으로 이동하여 1단계 휴지통에서 삭제한 동일한 문서를 삭제합니다. **이때 이 문서는 영구 삭제됩니다.**

> [!IMPORTANT]
> 보존(Office 365의 보존 또는 법적 보류 기능 중 하나) 중인 사이트에 있는 문서는 삭제할 수 없습니다. DSR 삭제 요청이 법적 보류에 우선하는 경우 문서를 영구적으로 삭제하려면 먼저 사이트에서 보존을 제거해야 합니다.

자세한 절차는 다음 항목을 참조하세요.

- [SharePoint 문서 라이브러리에서 파일, 폴더 또는 링크 삭제](https://support.microsoft.com/office/delete-a-file-folder-or-link-from-a-sharepoint-document-library-71f3c90a-0d24-4d80-8b66-f88234b79a52)
- [SharePoint 사이트의 휴지통 항목 삭제 또는 비우기](https://support.microsoft.com/office/delete-items-or-empty-the-recycle-bin-of-a-sharepoint-site-2e713599-d13e-40d6-96dc-66f0a366f74e)
- [사이트 모음 휴지통에서 항목 삭제](https://support.microsoft.com/office/delete-items-from-the-site-collection-recycle-bin-dd5c00c2-aef6-4458-9d04-80b185077653)
- [이전 사용자의 데이터에 대한 액세스 권한 얻기 및 백업](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data)의 "이전 직원의 비즈니스용 OneDrive 문서에 대한 액세스 권한 얻기" 섹션
- [비즈니스용 OneDrive에서 파일 또는 폴더 삭제](https://support.office.com/article/Delete-files-or-folders-in-OneDrive-21fe345a-e488-4fa7-932b-f053c1bebe8a)
- [SharePoint에서 목록 삭제](https://support.microsoft.com/office/delete-a-list-in-sharepoint-2a7bca5b-b8fd-4e5b-8f4b-2ac034f3070d)
- [SharePoint Online에서 목록 항목 삭제](https://support.office.com/article/delete-list-items-in-sharepoint-online-db722233-4a38-4889-a6cf-4b33fe5c60c0)

### <a name="deleting-a-sharepoint-site"></a>SharePoint 사이트 삭제

DSR 삭제 요청에 응답하는 가장 좋은 방법은 전체 SharePoint 사이트를 삭제하는 것입니다. 그러면 사이트에 있는 모든 데이터가 삭제됩니다. SharePoint Online PowerShell에서 cmdlet을 실행하여 이 작업을 수행할 수 있습니다.

- 사이트를 삭제하여 SharePoint Online 휴지통으로 이동하려면 [Remove-SPOSite](/powershell/module/sharepoint-online/remove-sposite) cmdlet을 사용합니다(일시 삭제).
- 사이트를 영구적으로 삭제하려면 [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite) cmdlet을 사용합니다(영구 삭제).

eDiscovery 보존이 적용되거나 보존 정책이 할당된 사이트는 삭제할 수 없습니다. 사이트를 삭제하려면 먼저 eDiscovery 보존 또는 보존 정책에서 사이트를 제거해야 합니다.

### <a name="deleting-a-onedrive-for-business-site"></a>비즈니스용 OneDrive 사이트 삭제

마찬가지로, DSR 삭제 요청에 대한 응답으로 사용자의 비즈니스용 OneDrive 사이트를 삭제할 수 있습니다. 사용자의 Office 365 계정을 삭제하는 경우 해당 비즈니스용 OneDrive는 30일 동안 보존됩니다(복원 가능). 30일 후에는 SharePoint Online 휴지통으로 이동(일시 삭제)되었다가 93일 후 영구적으로 삭제됩니다(영구 삭제). 이 프로세스를 빠르게 진행하려면 [Remove-SPOSite](/powershell/module/sharepoint-online/remove-sposite) cmdlet을 사용하여 비즈니스용 OneDrive 사이트를 휴지통으로 이동한 다음 [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite) cmdlet을 사용하여 영구적으로 삭제하면 됩니다. SharePoint Online의 사이트와 마찬가지로 eDiscovery 보존 또는 보존 정책에 할당된 경우에는 사용자의 계정을 삭제하기 전에 사용자의 비즈니스용 OneDrive 사이트를 삭제할 수 없습니다.

### <a name="deleting-onedrive-for-business-and-sharepoint-online-experience-settings"></a>비즈니스용 OneDrive 및 SharePoint Online 환경 설정 삭제

이 서비스는 비즈니스용 OneDrive 및 SharePoint Online에 저장된 사용자가 만든 파일 뿐만 아니라 다양한 환경을 활용하기 위해 사용하는 사용자에 관한 정보를 저장합니다. 이 내용은 이전에 이 문서에 기재되었습니다. 비즈니스용 OneDrive 및 SharePoint Online 응용 프로그램 데이터에 액세스하고, 보고, 내보내는 방법에 대한 정보는 [콘텐츠 검색 eDiscovery 도구를 사용하여 DSR에 응답](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)의 [선택한 응용 프로그램에 관한 추가 고려 사항](#additional-considerations-for-selected-applications) 섹션을 참조하세요.

#### <a name="deleting-a-sharepoint-user-profile"></a>SharePoint 사용자 프로필 삭제

SharePoint 사용자 프로필은 Azure Active Directory에서 사용자 계정이 삭제된 후 30일이 지나면 영구적으로 삭제됩니다. 그러나 사용자 계정을 영구 삭제할 수 있으며 이 경우 SharePoint 사용자 프로필이 제거됩니다. 자세한 내용은 [이 가이드의 사용자 삭제 섹션](#deleting-a-user)을 참조하세요.

관리자는 SharePoint Online PowerShell에서 **Remove-SPOUserProfile** cmdlet을 사용하여 사용자의 사용자 프로필을 신속하게 삭제할 수 있습니다. [Remove-SPOUserProfile](/powershell/module/sharepoint-online/remove-spouserprofile)을 참조하세요. 이를 위해서는 사용자가 적어도 Azure Active Directory에서 일시적으로 삭제되어야 합니다.

#### <a name="deleting-user-information-lists-on-sharepoint-online-sites"></a>SharePoint Online 사이트에서 사용자 정보 목록 삭제

조직에 남아 있는 사용자의 경우, 이 데이터는 SharePoint 열 필드의 참조 무결성을 위해 상호 작용하는 사이트에 그대로 남아 있습니다. 관리자는 SharePoint Online PowerShell에서 **Remove-SPOUserInfo** 명령을 사용하여 지정된 사이트에서 사용자의 모든 사용자 정보 속성을 삭제할 수 있습니다. 이 PowerShell cmdlet 실행에 대한 내용은 [Remove-SPOUserInfo](/powershell/module/sharepoint-online/remove-spouserinfo)를 참조하세요.

기본적으로 이 명령은 사용자의 표시 이름을 유지하고 전화 번호, 전자 메일 주소, 기술 및 전문 지식 또는 SharePoint Online 사용자 프로필에서 복사된 기타 속성과 같은 속성을 삭제합니다. 관리자는 **RedactUser** 매개 변수를 사용하여 사용자 정보 목록에서 사용자의 대체 표시 이름을 지정할 수 있습니다. 이는 사용자 경험의 여러 부분에 영향을 미치며 사이트의 파일 기록에서 정보가 손실됩니다.

마지막으로, 편집 기능은 문서에서 사용자를 참조할 수 있는 모든 메타데이터 또는 콘텐츠를 제거할 수 없습니다. 파일 콘텐츠 및 메타데이터를 수정하는 방법은 이 가이드의 [비즈니스용 OneDrive 및 SharePoint Online에서 콘텐츠 변경](#making-changes-to-content-in-onedrive-for-business-and-sharepoint-online) 섹션에 설명되어 있습니다. 이 방법은 파일의 편집된 복사본을 다운로드하고 삭제한 다음 업로드하는 과정으로 구성됩니다.

#### <a name="deleting-onedrive-for-business-experience-settings"></a>비즈니스용 OneDrive 환경 설정 삭제

모든 비즈니스용 OneDrive 환경 설정 및 정보를 삭제하려면 보존된 파일을 다른 사용자에게 다시 할당한 후 사용자의 비즈니스용 OneDrive 사이트를 제거하는 것이 좋습니다. 관리자는 [PowerShell Script](/powershell/scripting/overview) 및 [SharePoint CSOM(클라이언트 쪽 개체 모델)](/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-client-library-code) 명령을 사용하여 이러한 목록을 삭제할 수 있습니다. 설정, 설정을 저장하는 방법 및 삭제하는 방법에 대한 자세한 내용은 [비즈니스용 OneDrive 환경 설정 삭제](/sharepoint/delete-odfb-lists)를 참조하세요.

#### <a name="onedrive-for-business-and-sharepoint-online-search-queries"></a>비즈니스용 OneDrive 및 SharePoint Online 검색 쿼리

비즈니스용 OneDrive 및 SharePoint Online 검색 환경에서 만든 사용자의 검색 쿼리는 사용자가 쿼리를 만든 후 30일이 지나면 자동으로 삭제됩니다.

### <a name="deleting-items-in-exchange-online-mailboxes"></a>Exchange Online 사서함에서 항목 삭제

DSR 삭제 요청을 충족하기 위해 Exchange Online 사서함의 항목을 삭제해야 할 수 있습니다. IT 관리자가 사서함의 항목을 삭제할 수 있는 방법에는 대상 항목을 일시 삭제할지 또는 영구 삭제할지에 따라 두 가지 방법이 있습니다. SharePoint Online 또는 비즈니스용 OneDrive 사이트의 문서와 마찬가지로 보존 중인 사서함의 항목은 Office 365에서 영구적으로 삭제할 수 없습니다. 항목을 삭제하려면 먼저 보존을 제거해야 합니다. 사서함 보존이 우선인지 또는 DSR 삭제 요청이 우선인지 결정해야 합니다.

#### <a name="soft-delete-mailbox-items"></a>사서함 항목 일시 삭제

콘텐츠 검색 작업 기능을 사용하여 콘텐츠 검색에서 반환되는 항목을 일시 삭제할 수 있습니다. 앞서 설명한 것처럼 일시 삭제된 항목은 사서함의 복구 가능한 항목 폴더로 이동되지만 영구 삭제된 항목은 영구적으로 삭제되며 복구할 수 없습니다.

다음은 이 프로세스에 대한 간략한 개요입니다.

1. 콘텐츠 검색을 만들고 실행하여 사용자 사서함에서 삭제할 항목을 찾습니다. 검색을 다시 실행하여 삭제할 항목만 검색 결과에 반환되도록 검색 결과의 범위를 좁힐 수 있습니다.
2. Office 365 PowerShell에서 **New-ComplianceSearchAction** **-Purge** **PurgeType** **SoftDelete** 또는 **New-ComplianceSearchAction** **-Purge** **PurgeType** **HardDelete** 명령을 사용하여 이전 단계에서 만든 콘텐츠 검색에서 반환되는 항목을 일시 삭제합니다.

자세한 지침은 [조직에서 전자 메일 메시지 검색 및 삭제하기](/microsoft-365/compliance/search-for-and-delete-messages-in-your-organization)를 참조하세요.

#### <a name="hard-delete-items-in-a-mailbox-on-hold"></a>보존 중인 사서함의 항목 영구 삭제

앞서 설명했듯이 보존 중인 사서함에서 항목을 영구 삭제하는 경우 이 항목은 사서함에서 제거되지 않습니다. 복구 가능한 항목 폴더의 숨겨진 폴더(**제거** 폴더)로 이동하여 해당 항목의 보존 기간이 만료되거나 사서함에서 보존이 제거될 때까지 유지됩니다. 둘 중 하나가 발생한 경우 항목은 다음에 사서함이 처리될 때 Office 365에서 제거됩니다.

조직에서는 보존 기간이 만료될 때 영구적으로 삭제되는 항목이 DSR 삭제요청에 대한 요구 사항을 충족하는지 확인할 수 있습니다. 그러나 사서함 항목이 Office 365에서 즉시 제거되어야 하는 경우 사서함에서 보존을 제거한 다음 사서함에서 항목을 영구 삭제해야 합니다. 자세한 지침은 [보존 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제](/microsoft-365/compliance/delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold)를 참조하세요.

> [!NOTE]
> 이전 항목의 절차에 따라 DSR 삭제 요청을 충족하기 위해 사서함 항목을 영구 삭제하려면 사서함이 여전히 보존 중인 동안 해당 항목을 일시 삭제하여 복구 가능한 항목 폴더로 이동하도록 해야 할 수 있습니다.

## <a name="deleting-a-user"></a>사용자 삭제

DSR 삭제 요청에 대한 응답으로 개인 데이터를 삭제하는 것 외에도 사용자 계정을 삭제하여 데이터 주체의 “잊혀질 권리”를 이행할 수도 있습니다. 사용자를 삭제하려고 할 수 있는 몇 가지 이유는 다음과 같습니다.

- 데이터 주체가 조직을 떠났거나 떠나는 중입니다.
- 데이터 주체가 자신에 대해 수집된 시스템 생성 로그를 삭제하도록 요청했습니다. 시스템 생성 로그의 데이터에는 Office 365 앱 및 서비스 사용 현황 데이터, 데이터 주체가 수행한 검색 요청에 대한 정보, 시스템 기능 및 사용자 또는 다른 시스템의 상호 작용으로 인해 제품 및 서비스에서 생성된 데이터 등이 포함됩니다. 자세한 내용은 이 가이드에서 [3부: 시스템 생성 로그에 대한 DSR에 응답](#part-3-responding-to-dsrs-for-system-generated-logs)을 참조하세요.
- 데이터 주체가 Office 365에서 데이터에 액세스하거나 처리하는 것을 영구적으로 방지합니다([DSR 제한 요청에 응답](#responding-to-dsr-restriction-requests) 섹션에 설명된 방법을 통한 일시적인 액세스 제한과 반대).

사용자 계정을 삭제한 후:

- 사용자가 더 이상 Office 365에 로그인할 수 없거나 조직의 Microsoft 리소스(예: 비즈니스용 OneDrive 계정, SharePoint Online 사이트 또는 Exchange Online 사서함)에 액세스할 수 없습니다.
- 사용자 계정과 연결된 개인 데이터(예: 전자 메일 주소, 별칭, 전화 번호, 우편 주소)가 삭제됩니다.
- 일부 Office 365 앱에서 사용자에 대한 정보가 제거됩니다. 예를 들어 Microsoft Flow의 경우 삭제된 사용자는 공유 흐름에 대한 소유자 목록에서 제거됩니다.
- 서비스의 보안 혹은 안정성을 손상시킬 수 있는 데이터를 제외하고 데이터 주체에 대한 시스템 생성 로그는 사용자 계정을 삭제한 후 30일 후에 삭제됩니다. 자세한 내용은 [시스템 생성 로그 삭제 섹션](#deleting-system-generated-logs)을 참조하세요.

> [!IMPORTANT]
> 사용자 계정을 삭제한 후 이 사용자는 Office 365에 로그인할 수 있는 권한 및 이전에 회사 또는 학교 계정으로 사용한 제품 또는 서비스에 로그인할 수 있는 권한을 상실합니다. 또한 Microsoft가 데이터 통제자인 인스턴스에서 Microsoft를 통해 직접 DSR 요청을 시작할 수 없습니다. 자세한 내용은 이 가이드의 4부에서 [Microsoft가 데이터 통제자인 조직 ID로 인증된 제품 및 서비스](#product-and-services-authenticated-with-an-org-id-for-which-microsoft-is-a-data-controller) 섹션을 참조하세요.

> [!NOTE]
> 현재 FastTrack 마이그레이션에 연결된 고객의 경우, 사용자 계정을 삭제하면 Microsoft FastTrack 팀이 보유하는 데이터 복사본이 삭제되지 않습니다. FastTrack 팀은 오직 마이그레이션 완료 목적으로 복사본을 보유합니다. 마이그레이션하는 동안 Microsoft FastTrack 팀이 데이터 복사본도 삭제하게 하려면 [요청을 제출](https://go.microsoft.com/fwlink/?linkid=874544)할 수 있습니다. 일반 업무 과정에서 Microsoft FastTrack은 마이그레이션이 완료되면 모든 데이터 복사본을 삭제합니다.

개인 데이터 삭제에 대한 이전 섹션에서 설명된 데이터의 일시 삭제 및 영구 삭제와 마찬가지로 사용자 계정을 삭제할 때도 일시 삭제 및 영구 삭제 상태가 있습니다.

- 관리 센터 또는 Azure Portal에서 사용자를 삭제하여 초기에 사용자 계정을 삭제한 경우 해당 사용자 계정은 일시 삭제되며 Azure의 휴지통으로 이동하여 최대 30일 동안 보존됩니다. 이때는 사용자 계정을 복원할 수 있습니다.
- 사용자 계정을 영구적으로 삭제한 경우 해당 사용자 계정은 영구 삭제되며 Azure의 휴지통에서 제거됩니다. 이때는 사용자 계정을 복원할 수 없으며, 사용자 계정과 연결된 모든 데이터가 Microsoft 클라우드에서 영구적으로 제거됩니다. 계정을 영구 삭제하면 데이터 주체에 대한 시스템 생성 로그는 서비스의 보안 혹은 안정성을 손상시킬 수 있는 데이터를 제외하고 삭제됩니다.

조직에서 사용자를 삭제하는 대략적인 프로세스는 다음과 같습니다.

1. 관리 센터 또는 Azure Portal로 이동하여 사용자를 찾습니다.

2. 사용자를 삭제합니다. 초기에 사용자를 삭제하는 경우 해당 사용자의 계정은 휴지통으로 전송됩니다. 이때 사용자는 일시 삭제됩니다. 이 계정은 30일 동안 일시 삭제된 상태로 보존되므로 계정을 복원할 수 있습니다. 30일 후에는 계정이 자동으로 영구 삭제됩니다. 구체적인 지침은 [Azure AD에서 사용자 삭제](/azure/active-directory/add-users-azure-active-directory)를 참조하세요.<br><br> 관리 센터에서 사용자 계정을 일시 삭제할 수도 있습니다. [조직에서 사용자 삭제](/microsoft-365/admin/add-users/delete-a-user)를 참조합니다.

3. 사용자 계정이 영구 삭제될 때까지 30일 동안 기다리지 않으려는 경우 수동으로 영구 삭제할 수 있습니다. Azure Portal에서 이렇게 하려면 최근에 삭제된 사용자 목록으로 이동하여 사용자를 영구적으로 삭제합니다. 이때 사용자는 영구 삭제됩니다. 지침은 [최근에 삭제된 사용자를 영구적으로 삭제하는 방법](/azure/active-directory/active-directory-users-restore)을 참조하세요.

Office 365 관리 포털에서 사용자를 영구 삭제할 수 없습니다.

> [!NOTE]
> 21Vianet에서 운영하는 Office 365(중국)에서는 앞서 설명한 대로 사용자를 영구적으로 삭제할 수 없습니다. 사용자를 영구적으로 삭제하려면 이 [URL](https://portal.partner.microsoftonline.cn/AdminPortal/Home#/homepage)의 Office 365 관리자 포털을 통해 요청을 제출할 수 있습니다. **상거래** 로 이동한 후 **구독** -> **개인 정보** ->  **GDPR** 을 선택하고 필수 정보를 입력합니다.

### <a name="removing-exchange-online-data"></a>Exchange Online 데이터 제거

사용자를 삭제할 때 이해해야 하는 한 가지는 사용자의 Exchange Online 사서함에서 발생하는 사항입니다. 사용자 계정이 영구 삭제(이전 프로세스의 3단계)된 후 삭제된 사용자의 사서함은 Office 365에서 자동으로 제거되지 않습니다. Office 365에서 영구적으로 제거되려면 사용자 계정이 영구 삭제된 후 최대 60일이 걸립니다. 다음은 사용자 계정이 삭제된 후 사서함 수명 주기 및 그동안 사서함 데이터의 상태에 대한 설명입니다.

- **1~30일** - 일시 삭제된 사용자 계정을 복원하여 사서함을 완전히 복원할 수 있습니다.
- **31~60일** - 사용자 계정이 영구 삭제된 후 30일 동안 조직의 관리자는 사서함의 데이터를 복구하여 다른 사서함으로 가져올 수 있습니다. 이에 따라 필요한 경우 조직에 사서함 데이터를 복원할 수 있는 기능이 제공됩니다.
- **61~90일** - 관리자는 사서함의 데이터를 더 이상 복구할 수 없습니다. 사서함 데이터는 영구적으로 제거된 것으로 표시되며, 최대 30일 후 Office 365에서 제거됩니다.

이 사서함 수명 주기가 DSR 삭제 요청에 응답하기 위한 조직의 요구 사항을 충족하지 않는 경우 사용자 계정을 영구 삭제한 *후* [Microsoft 지원에 문의](https://support.microsoft.com/)하여 Microsoft에 프로세스를 수동으로 초기화하여 사서함 데이터를 영구적으로 제거하도록 요청할 수 있습니다. 사서함 데이터를 영구적으로 제거하는 이 프로세스는 수명 주기에서 61일 후에 자동으로 시작되므로 수명 주기에서 이 시점 후에는 Microsoft에 문의할 이유가 없습니다.

## <a name="using-in-app-functionality-to-respond-to-dsrs"></a>앱 내 기능을 사용하여 DSR에 응답

대부분의 고객 데이터는 이전 섹션에 설명된 응용 프로그램을 사용하여 작성 및 생성되지만 Office 365에서는 고객이 고객 데이터를 생성하고 저장하는 데 사용할 수 있는 다른 많은 응용 프로그램도 제공합니다. 그러나 콘텐츠 검색에는 현재 이러한 다른 Office 365 응용 프로그램에서 작성된 데이터를 찾을 수 있는 기능이 없습니다. 이러한 응용 프로그램에서 생성된 데이터를 찾으려면 관리자 또는 데이터 소유자가 제품 내 기능을 사용하여 DSR과 관련이 있을 수 있는 데이터를 찾아야 합니다. 다음 목록에는 이러한 Office 365 응용 프로그램이 나와 있습니다.

앱 내 기능을 사용하여 고객 데이터를 찾을 수 있는 응용 프로그램:

- Access
- Office 365용 비즈니스 앱
- Education
- Flow
- Forms
- Kaizala
- Planner
- Power Apps
- Power BI
- Project
- 게시자
- Stream
- Yammer

### <a name="access"></a>Access

다음 섹션에서는 Microsoft Access의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

##### <a name="discover"></a>검색

DSR 요청에 적합할 수 있는 Access 데이터베이스의 레코드를 검색할 수 있는 몇 가지 방법이 있습니다. DSR 조사의 경우, 데이터 주체와 관련된 레코드를 검색하거나 특정 데이터를 포함하는 레코드를 검색할 수 있습니다. 예를 들어, 데이터 주체에 해당하는 레코드를 검색하거나 해당 레코드로 이동할 수 있습니다. 또는 데이터 주체에 대한 개인 데이터 같은 특정 데이터를 포함하는 레코드를 검색할 수 있습니다. 자세한 내용은 다음을 참조하세요.

- [Access 데이터베이스에서 레코드 찾기](https://support.microsoft.com/office/find-records-in-an-access-database-705220b7-0255-4ef9-9349-6bd7442d1b7e) 
- [단순 선택 쿼리 만들기](https://support.office.com/article/create-a-simple-select-query-de8b1c8d-14e9-4b25-8e22-70888d54de59)

##### <a name="access"></a>Access

DSR 요청과 관련된 레코드 또는 필드를 찾은 후 데이터의 스크린샷을 생성하거나 Excel 파일, Word 파일 또는 텍스트 파일로 내보낼 수 있습니다. 레코드 원본이나 데이터를 찾기 위해 만든 선택 쿼리에 따라 보고서를 만들고 인쇄할 수도 있습니다. 다음을 참조하세요.

- [Access 보고서 소개](https://support.office.com/article/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Excel로 데이터 내보내기](https://support.office.com/article/export-data-to-excel-64e974e6-ae43-4301-a53e-20463655b1a9)
- [Word 문서에 데이터 내보내기](https://support.microsoft.com/office/export-access-data-to-a-word-document-6e954c8e-2243-4cb9-8544-607e5b7bfc12)
- [텍스트 파일로 데이터 내보내기](https://support.microsoft.com/office/export-data-to-a-text-file-f72dfc38-a8a0-4c5b-8c2c-bf2950814140)

##### <a name="export"></a>내보내기

앞에서 설명한 것처럼 Access 데이터베이스에서 다른 파일 형식으로 데이터를 내보낼 수 있습니다. 선택한 내보내기 파일 형식은 데이터 주체의 특정 DSR 내보내기 요청에 의해 결정될 수 있습니다. 다른 파일 형식으로 Access 데이터를 내보내는 방법을 설명하는 항목 목록은 [가져오기 및 내보내기](https://support.microsoft.com/office/import-and-export-c060505b-d8ac-4499-8879-733e56c6106f)를 참조하세요.

##### <a name="delete"></a>삭제

Access 데이터베이스에서 전체 레코드 또는 필드 하나만 삭제할 수 있습니다. Access 데이터베이스에서 레코드를 삭제하는 가장 빠른 방법은 데이터 시트 보기에서 테이블을 열고, 삭제하려는 레코드(행) 또는 필드의 데이터만 선택한 후 Delete 키를 누릅니다. 데이터를 찾기 위해 사용자가 만든 선택 쿼리를 사용한 후 삭제 쿼리로 변환할 수도 있습니다. 다음을 참조하세요.

- [데이터베이스에서 하나 이상의 레코드 삭제](https://support.office.com/article/ways-to-add-edit-and-delete-records-5e90a80c-106d-4c55-996e-07d7200980ce)
- [삭제 쿼리 만들기 및 실행](https://support.office.com/article/create-and-run-a-delete-query-6da65fe1-0fc7-4a64-8ef0-c052cd4c3ec5)

### <a name="business-apps-for-office-365"></a>Office 365용 비즈니스 앱

이 섹션에서는 다음의 각 Office 365용 비즈니스 앱에 포함되어 있는 앱 내 기능을 사용하여 DSR 요청에 응답하는 방법을 설명합니다.

- [Bookings](#bookings)
- [Listings](#listings)
- [Connections](#connections)

#### <a name="bookings"></a>Bookings

다음 섹션에서는 Microsoft Bookings의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다. 이 내용은 독립 실행형 Bookings 앱과 비즈니스 센터를 통해 액세스하는 Bookings 둘 다에 적용됩니다.

Microsoft Bookings를 사용하여 조직에서 Bookings 라이선스를 보유하고 있는 관리자 및 사용자나 직원은 고객이 약속을 예약하고 변경하고, 확인 전자 메일, 업데이트, 취소 및 미리 알림 전자 메일을 수신할 수 있도록 예약 페이지를 설정할 수 있습니다. 비즈니스 소유자 및 해당 직원은 Bookings를 사용하여 고객 대신 이벤트를 예약할 수도 있습니다. 

고객, 관리자 또는 직원은 다음과 같은 유형의 데이터를 만듭니다.

- **고객, 파트너 및 친구의 연락처 정보** - 이 데이터에는 이름, 전화번호, 전자 메일 주소, 주소, 메모가 포함됩니다.

    - 모든 사용자에 대한 연락처는 Bookings Web, iOS 및 Android 클라이언트를 사용하여 수동으로 만들 수 있습니다.
    
    - Bookings iOS와 Android 클라이언트를 사용하여 모든 사용자에 대한 연락처를 C1의 모바일 장치에서 Bookings로 가져올 수 있습니다.
    
    - 예약한 모든 사용자에 대한 예약 워크플로우를 통해 예약할 때, 예약은 사용자가 고객을 대신하여 작성하는지, 또는 고객이 소유자의 예약 페이지를 사용하여 작성했는지도 자동으로 작성됩니다.

- **예약 이벤트** - 비즈니스 소유자 또는 지정된 해당 담당자 및 고객 간 진행되는 모임입니다. 이 모임은 비즈니스 소유자의 공개 예약 페이지를 통해 비즈니스 소유자 또는 고객이 만든 모임입니다. 이 데이터에는 이름, 주소, 전자 메일 주소, 전화번호 및 비즈니스 소유자가 예약 시 고객으로부터 수집하는 기타 모든 정보를 포함합니다.

- **확인/취소/업데이트 전자 메일** - 특정 예약 이벤트와 관련하여 시스템이 생성하고 전송하는 전자 메일 메시지입니다.  여기에는 관련 서비스를 전달하도록 예약된 직원에 대한 개인 데이터가 포함되며, 비즈니스 소유자 또는 고객이 예약 시에 입력한 고객의 개인 데이터도 포함됩니다.

모든 고객 콘텐츠는 조직의 예약을 호스트하는 Exchange Online 사서함에 저장됩니다. 이 콘텐츠는 이러한 비즈니스 소유자 및 고객이 데이터 삭제를 명시적으로 요청되거나 서비스를 탈퇴하지 않는 한, 비즈니스 소유자 및 고객이 서비스에서 활성 상태를 유지하는 동안 유지됩니다. 이 콘텐츠는 제품 UI, cmdlet을 사용하거나 예약 사서함을 삭제하여 삭제될 수 있습니다. 삭제 작업이 시작되면 데이터는 비즈니스 소유자가 설정된 기간 내에 삭제됩니다. 

고객이 서비스를 종료하기로 결정하면 고객의 콘텐츠는 90일 후에 삭제됩니다. 사용자 계정을 삭제한 후에 사서함 콘텐츠를 삭제하는 경우에 대한 자세한 내용은 [Exchange Online 데이터 제거](#removing-exchange-online-data)를 참조하세요.

#### <a name="end-user-identifiable-information"></a>최종 사용자 식별 가능 정보

EUII(최종 사용자 식별 가능 정보)에는 Bookings에서 예약한 직원에 대한 개인 및 연락처 정보가 포함되어 있습니다. 비즈니스 소유자가 Bookings를 설치하고 설치 후에 업데이트를 하면 직원 세부 정보 페이지에 이 정보가 추가됩니다. 여기에는 직원 구성원의 이름, 이니셜, 전자 메일 주소 및 전화 번호가 포함됩니다. 이 데이터는 Bookings를 호스트하는 Exchange Online 사서함에 저장됩니다.

이 데이터는 앱 UI를 사용하거나 관련 예약 사서함을 삭제하여 비즈니스 소유자 또는 관리자를 명시적으로 삭제하지 않는 한, 직원 구성원이 서비스에서 활성 상태인 동안 유지됩니다. 관리자가 직원의 세부 정보 삭제를 시작하거나 직원 구성원이 서비스를 탈퇴하면 비즈니스 소유자 또는 관리자가 설정한 Exchange Online 사서함의 콘텐츠 보존 정책에 따라 해당 세부 정보가 삭제됩니다.

##### <a name="discoveraccess"></a>검색/액세스

Bookings에서는 다음과 같은 유형의 데이터를 수집하고 저장합니다.

- **비즈니스 프로필 정보:** Bookings를 사용하는 비즈니스에 대한 고객 콘텐츠는 Bookings의 비즈니스 정보 양식을 통해 수집되고, 고객이 비즈니스 센터와 함께 Bookings를 사용하는 경우에는 비즈니스 센터 비즈니스 프로필과 동기화됩니다. 이 데이터와 연결된 유일한 EUII는 C1의 전자 메일 주소입니다. 새 예약 알림과 업데이트 전자 메일이 이 주소로 전송됩니다.
- **고객 연락처:** 연락처는 Bookings Web, iOS 및 Android 클라이언트에서 수동으로 생성되거나, 모바일 장치에서 가져올 수 있습니다. 또한 셀프 서비스 예약 페이지를 사용하는 동안에도 연락처가 자동으로 생성됩니다. 이러한 연락처는 EUII를 포함하며 Bookings 사서함에 저장됩니다.
- **직원 세부 정보:** 고객 콘텐츠에는 Bookings Web, iOS 또는 Android 클라이언트에서 만든 서비스를 제공할 수 있는 자격이 있는 직원에 대한 데이터가 포함됩니다. 직원 세부 정보에는 이름, 전자 메일 주소 및 전화 번호가 포함될 수 있습니다.
- **예약 이벤트:** 웹 클라이언트 또는 Android/iOS 앱을 사용하여 기업에서 만들었거나 고객이 공개 예약 페이지(또는 Facebook 페이지)를 사용하여 만든 고객 모임 및 관련 고객 콘텐츠입니다. 이러한 이벤트에는 이름, 주소, 전자 메일 주소, 전화 번호 및 약속 세부 정보가 포함될 수 있습니다.
- **모임 요청, 전자 메일 확인/취소/업데이트, 전자 메일 미리 알림:** 예약과 관련해서 시스템이 전송하는 전자 메일 메시지입니다. 여기에는 예약 시에 입력된 직원 데이터 및 고객 데이터가 포함됩니다.

##### <a name="export"></a>내보내기

비즈니스 소유자, 직원 및 고객에 해당하는 데이터를 내보내려면 [비즈니스 센터 개인 정보 포털](https://businessaccount.microsoft.com/)을 사용할 수 있습니다.

##### <a name="delete"></a>삭제

DSR 삭제 요청에 대한 응답으로 다음과 같은 유형의 Bookings 데이터를 삭제할 수 있습니다.

- **비즈니스 프로필 정보 및 연락처:** 관리 센터에서 Bookings 사서함을 삭제할 수 있습니다. 사서함을 삭제한 후 30일 이내에 복원할 수 있습니다. 30일이 지나면 이 계정과 해당 사서함이 영구적으로 삭제됩니다. 사용자 계정 삭제에 관한 자세한 내용은 [사용자 삭제](#deleting-a-user) 섹션을 참조하세요.
- **직원 세부 정보:** Bookings 대시보드에서 직원을 삭제할 수 있습니다. 직원 세부 정보를 영구적으로 삭제하려면 해당 Office 365 계정을 삭제할 수 있습니다.
- **Bookings 이벤트:** Bookings 일정에서 예약 이벤트를 삭제할 수 있으며 이벤트를 삭제하면 고객의 정보가 제거됩니다.
- **모임 요청, 전자 메일 확인/취소/업데이트 및 전자 메일 미리 알림:** Bookings 일정에서 이러한 항목을 삭제하여 고객 정보를 제거할 수 있습니다.

비즈니스 소유자, 직원 및 고객에 해당하는 데이터를 내보내려면 [비즈니스 센터 개인 정보 포털](https://businessaccount.microsoft.com/)을 사용할 수 있습니다.

또한 비즈니스 소유자 및 직원 데이터를 삭제하고, 해당 사용자 계정을 삭제할 수 있습니다. 자세한 내용은 [사용자 삭제](#deleting-a-user) 섹션을 참조하세요.

#### <a name="listings"></a>Listings

다음 섹션에서는 Microsoft Listings의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

##### <a name="discover"></a>검색

Listings 소유자는 비즈니스를 Google, Bing, Yelp 및 Facebook에 연결하여 집계된 평점 및 리뷰를 볼 수 있습니다. Listings는 다음과 같은 유형의 데이터를 수집하고 저장합니다.

- Google 리뷰 및 평점
- Bing 리뷰 및 평점
- Yelp 리뷰 및 평점
- Facebook 리뷰 및 평점

##### <a name="access"></a>액세스
Listings 소유자는 Listings 대시보드에 로그인하여 해당 리뷰와 평점을 볼 수 있습니다.

##### <a name="export"></a>내보내기

비즈니스 소유자, 직원 및 고객에 해당하는 데이터를 내보내려면 [비즈니스 센터 개인 정보 포털](https://businessaccount.microsoft.com/)을 사용할 수 있습니다.

##### <a name="delete"></a>삭제

Listings 소유자는 Listings 정보를 삭제하려는 경우 Listings 페이지에서 공급자로부터 연결을 끊을 수 있습니다. 연결을 끊은 후에는 Listings 정보가 삭제됩니다.

#### <a name="connections"></a>Connections

다음 섹션에서는 Microsoft Connections의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

##### <a name="discover"></a>검색

Connections에서는 다음과 같은 유형의 데이터를 수집하고 저장합니다. 

- 고객/연락처는 기업에서 웹 클라이언트 또는 모바일 앱(iOS, Android)을 사용하여 만들거나 비즈니스 연락처로 전자 메일 마케팅 캠페인이 전송될 때 해당 앱을 사용하여 만들어집니다. 고객 데이터에는 이름, 주소, 전자 메일 주소 및 과세 ID 번호가 포함될 수 있습니다. 연락처는 모든 비즈니스 센터 앱에서 공유됩니다.
- 고객은 Connections 등록 페이지에서 등록하고 개인 정보를 저장할 수 있습니다.
- 전자 메일 캠페인의 링크

##### <a name="access"></a>Access

Connections 소유자는 Connections 대시보드에 로그인하고 전송한 전자 메일 캠페인을 볼 수 있습니다.

##### <a name="export"></a>내보내기

비즈니스 소유자, 직원 및 고객에 해당하는 데이터를 내보내려면 [비즈니스 센터 개인 정보 포털](https://businessaccount.microsoft.com/)을 사용할 수 있습니다.

##### <a name="delete"></a>삭제

Connections 소유자는 전자 메일 캠페인을 전송한 후에 캠페인을 삭제할 수 없습니다. 삭제하려는 초안 캠페인이 있는 경우 Connections 대시보드에 로그인한 후 해당 초안 캠페인을 삭제할 수 있습니다.

### <a name="education"></a>Education

이 섹션에서는 다음 Microsoft Education 앱의 앱 내 기능을 사용하여 DSR 요청에 응답하는 방법을 설명합니다.

- Assignments
- Class Notebook

#### <a name="assignments"></a>Assignments

다음 섹션에서는 Assignments의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

##### <a name="discoveraccess"></a>검색/액세스

Assignments는 교사와 학생이 생성한 정보를 모두 저장합니다. 이 정보 중 일부는 SharePoint에 저장소되고, 일부는 SharePoint 이외의 위치에 저장됩니다.

##### <a name="finding-assignments-data-stored-in-sharepoint"></a>SharePoint에 저장된 Assignments 데이터 찾기

과제 제출과 관련된 학생 파일은 문서 라이브러리(**학생 과제물**)에 저장되고 교사가 만들고 학생이 액세스하는 Assignments에 연결된 파일은 다른 문서 라이브러리(**클래스 파일**)에 저장됩니다. 두 문서 라이브러리는 해당하는 수업 팀 SharePoint 사이트에 있습니다.

관리자는 보안 및 준수 센터의 콘텐츠 검색 도구를 사용하여 과제 관련 파일 및 과제 제출과 관련된 학생 파일(학생 과제물 및 클래스 파일 라이브러리에 포함)을 검색할 수 있습니다. 예를 들어, 관리자는 조직의 모든 SharePoint 사이트를 검색하고 검색 쿼리에서 학생의 이름과 수업 또는 과제 이름을 사용하여 DSR 요청과 관련된 데이터를 찾을 수 있습니다.

마찬가지로, 관리자는 교사가 학생에게 배포한 파일의 과제 관련 교사 파일을 검색할 수 있습니다. 예를 들어, 관리자는 조직의 모든 SharePoint 사이트를 검색할 수 있으며, 검색 쿼리에 교사 이름 및 클래스 또는 과제 이름을 사용하여 DSR 요청 관련 데이터를 찾을 수 있습니다.

자세한 내용은 다음을 참조하세요.

- [과제 관리자 설명서](/microsoft-365/education/deploy/assignments-admin-documentation)
- [콘텐츠 검색 eDiscovery 도구를 사용하여 DSR에 응답](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)(이 가이드에 포함)

##### <a name="finding-assignments-data-not-stored-in-sharepoint"></a>SharePoint에 저장되지 않은 Assignments 데이터 찾기

다음과 같은 유형의 Assignments 데이터는 수업 팀 SharePoint 사이트에 저장되지 않으므로 콘텐츠 검색을 사용하여 검색할 수 없습니다. 이러한 데이터에는 포함됩니다.

- 학생의 성적과 교사의 피드백
- 각 학생이 과제에 대해 제출한 문서 목록
- 과제 세부 정보(예: 과제 기한)

데이터를 찾기 위해 관리자 또는 교사는 수업 팀 사이트의 과제로 이동한 후 DSR 요청과 관련이 있을 수 있는 데이터를 찾아야 합니다. 관리자는 수업의 소유자로서 자기 자신을 추가하고, 해당 수업 팀의 모든 과제를 볼 수 있습니다.

학생이 해당 클래스에 더 이상 속하지 않더라도 해당 데이터는 클래스에 계속 존재하여 “등록되지 않음”으로 표시됩니다. 이 경우 DSR 요청을 제출하는 학생이 공식적으로 등록한 클래스 목록을 관리자에게 제공해야 합니다.

##### <a name="export"></a>내보내기

PowerShell 스크립트를 사용하여 학생의 수업 목록을 가져온 다음 PowerShell 스크립트를 사용하여 데이터를 내보내면, 특정 학생이 등록된 모든 수업에서 해당 학생에 대한 Assignments 데이터를 내보낼 수 있습니다. 다음을 참조하세요.

- [Teams에 대한 Assignments 구성](/microsoft-365/education/deploy/configure-assignments-for-teams)
- [특정 학생에 대한 수업 목록 가져오기](/microsoft-365/education/deploy/assignments-script-get)
- [Assignments에서 학생 및 교사 데이터 내보내기](/microsoft-365/education/deploy/assignments-script-export)

수업 팀 사이트에서 학생을 제거한 경우 관리자는 export 스크립트를 실행하기 전에 해당 학생을 사이트에 다시 추가할 수 있습니다. 또는 관리자가 스크립트의 입력 파일을 사용하여 학생이 이미 등록된 모든 클래스를 식별할 수 있습니다. 또한 Assignment export 스크립트를 사용하여 교사가 액세스할 수 있는 모든 과제에 대한 제출 데이터를 내보낼 수도 있습니다.

##### <a name="delete"></a>삭제

PowerShell 스크립트를 사용하여 학생의 수업 목록을 가져온 다음 PowerShell 스크립트를 사용하여 데이터를 삭제하면, 특정 학생이 등록된 모든 수업에서 해당 학생에 대한 Assignments 데이터를 삭제할 수 있습니다. 수업에서 학생을 제거하기 전에 먼저 이 작업을 수행해야 합니다. 자세한 내용은 다음을 참조하세요.

- [Teams에 대한 Assignments 구성](/microsoft-365/education/deploy/configure-assignments-for-teams)
- [특정 학생에 대한 수업 목록 가져오기](/microsoft-365/education/deploy/assignments-script-get)
- [Assignments에서 학생 데이터 삭제](/microsoft-365/education/deploy/assignments-script-delete)

수업 팀 사이트에서 학생을 제거한 경우 관리자는 export 스크립트를 실행하기 전에 해당 학생을 사이트에 다시 추가할 수 있습니다. 또는 관리자가 스크립트의 입력 파일을 사용하여 학생이 이미 등록된 모든 클래스를 식별할 수 있습니다. 모든 Assignments가 수업 팀 사이트에서 공유되므로 교사 데이터를 삭제할 때는 Assignment deletion 스크립트를 사용할 수 없습니다. 따라서 관리자는 교사 데이터를 삭제하려면 자기 자신을 수업 팀 사이트에 추가한 후 특정 과제를 삭제해야 합니다.

#### <a name="class-notebook"></a>수업용 전자 필기장

수업용 전자 필기장에서 콘텐츠를 검색하는 방법은 이 가이드의 앞에서 설명되어 있습니다. [OneNote 수업용 전자 필기장](#onenote-class-notebook) 섹션을 참조하세요. 콘텐츠 검색 도구를 사용하여 수업용 전자 필기장에서 데이터를 내보낼 수도 있습니다. 또는 관리자 또는 데이터 주체가 수업용 전자 필기장에서 데이터를 내보낼 수 있습니다. 수업용 [전자 필기장의 복사본 저장](https://support.office.com/article/44733e18-0ef1-4d4b-be51-fc2ac5bfe9ec)을 참조 하세요.

### <a name="flow"></a>Flow

다음 섹션에서는 Microsoft Flow의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

사용자는 Flow를 사용하여 응용 프로그램 간의 파일 동기화, Office 365 서비스 간의 파일 복사, 특정 Office 365 앱에서 데이터를 수집하여 다른 Office 365 앱에 저장 등 데이터 관련 작업을 수행할 수 있습니다. 예를 들어 사용자는 Outlook 전자 메일 첨부 파일을 자신의 비즈니스용 OneDrive 계정에 저장하도록 Flow를 설정할 수 있습니다. 이 예에서는 콘텐츠 검색 도구를 사용하여 사용자의 사서함에서 첨부 파일이 포함된 전자 메일 메시지를 검색하거나 비즈니스용 OneDrive 계정에서 파일을 검색할 수 있습니다. 이는 Flow에서 처리된 데이터를 Flow 워크플로로 연결된 Office 365 서비스에서 검색할 수 있는 예입니다.

또한 사용자는 Flow를 사용하여 Office 365에서 외부 서비스(예: Dropbox)로 파일을 복사하거나 업로드할 수 있습니다. 이러한 경우 외부 서비스의 데이터와 관련된 DSR 요청을 이 유형의 시나리오에서 데이터를 처리하는 해당 외부 서비스에 제출해야 합니다.

관리자가 DSR 요청을 받으면 자신을 사용자 흐름의 소유자로 추가할 수 있습니다. 이를 통해 관리자는 흐름 정의 내보내기, 실행 기록 및 흐름 권한 재할당 수행과 같은 기능을 수행할 수 있습니다. [관리 센터에서 흐름 관리](https://flow.microsoft.com/blog/managing-flow-resources-in-the-admin-center/)를 참조하십시오.

관리자가 자신을 흐름의 소유자로 추가하려면 다음 권한이 있는 계정이 필요합니다.

- Flow/PowerApps 요금제 2 라이선스(유료 또는 평가판)

- [전역 관리자\](/microsoft-365/admin/add-users/assign-admin-roles)

    또는

- [Azure Active Directory 전역 관리자](/azure/active-directory/active-directory-assign-admin-roles-azure-portal)

이러한 권한이 있으면 Flow 관리 센터를 사용하여 조직의 모든 흐름에 액세스할 수 있습니다.

자신을 흐름의 소유자로 추가하려면

1. <https://admin.flow.microsoft.com>으로 이동합니다.
2. Office 365 자격 증명으로 로그인합니다.
3. **환경** 페이지에서 액세스하려는 흐름의 환경을 선택합니다. 조직에는 기본 환경이 있습니다.
4. 선택한 환경에 대한 페이지에서 **리소스** 를 선택한 다음, **흐름** 을 선택합니다. 환경의 모든 흐름 목록이 표시됩니다.
5. 자신을 구성원으로 추가하려는 흐름에 대해 **세부 정보 보기** 를 선택합니다.
6. **소유자** 에서 **공유 관리** 를 선택합니다.
7. **공유** 플라이아웃에서 자신을 구성원으로 추가하고 변경 내용을 저장합니다.

자신을 소유자로 지정한 후에는 **흐름** \> **내 흐름** \> **팀 흐름** 으로 이동하여 흐름에 액세스합니다. 여기에서 실행 기록을 다운로드하거나 흐름을 내보낼 수 있습니다. 다음을 참조하세요.

- [흐름 실행 기록 다운로드](https://flow.microsoft.com/blog/download-history-recurrence/)
- [패키징을 사용하여 환경 간에 흐름 내보내기 및 가져오기](https://flow.microsoft.com/blog/import-export-bap-packages/)

#### <a name="access"></a>액세스

사용자는 자신의 흐름에 대한 정의 및 실행 기록에 액세스할 수 있습니다.

- **흐름 정의:** 흐름 정의를 내보낼 수 있습니다(zip 파일 JSON 형식의 Flow 패키지로 내보냄). [패키징을 사용하여 환경 간에 흐름 내보내기 및 가져오기](https://flow.microsoft.com/blog/import-export-bap-packages/)를 참조하세요.
- **흐름 실행 기록:** 각 흐름의 실행 기록을 다운로드할 수 있습니다. 흐름 실행 기록은 CSV 파일로 다운로드되고, Excel에서 열어 필터링하거나 검색할 수 있습니다. 여러 흐름에 대한 실행 기록을 다운로드할 수도 있습니다. [흐름 실행 기록 다운로드](https://flow.microsoft.com/blog/download-history-recurrence/)를 참조하세요.

#### <a name="delete"></a>삭제

관리자는 Flow 관리 센터에서 자신을 사용자 흐름의 소유자로 추가할 수 있습니다. 사용자가 조직을 떠나고 해당 Office 365 계정이 삭제된 경우 해당 사용자가 단독 소유자인 흐름은 그대로 유지됩니다. 이는 조직에서 흐름을 새 소유자로 전환하고 공유 비즈니스 프로세스에 사용될 수 있는 흐름에 대한 비즈니스의 중단을 방지하기 위한 것입니다. 그런 다음 관리자는 해당 사용자가 소유했던 흐름을 삭제할지 또는 새 소유자에게 다시 할당할지를 결정하고 조치를 취해야 합니다.

공유 흐름의 경우 사용자가 조직에서 삭제되면 해당 사용자의 이름이 소유자 목록에서 제거됩니다.

#### <a name="export"></a>내보내기

관리자는 사용자의 흐름에 대한 정의 및 실행 기록을 내보낼 수 있습니다. 이렇게 하려면 관리자가 Flow 관리 센터에서 자신을 해당 사용자 흐름의 소유자로 추가해야 합니다.

- **흐름 정의:** 관리자가 자신을 흐름의 소유자로 추가한 후, **흐름** \> **내 흐름** \> **팀 흐름** 으로 이동하여 흐름 정의를 내보낼 수 있습니다(zip 파일 JSON 형식의 Flow 패키지로 내보냄).  [패키징을 사용하여 환경 간에 흐름 내보내기 및 가져오기](https://flow.microsoft.com/blog/import-export-bap-packages/)를 참조하세요.

- **흐름 실행 기록:** 마찬가지로 관리자가 흐름 실행 기록을 내보내려면 흐름 소유자로 자신을 추가 해야 합니다. 흐름 실행 기록은 CSV 파일로 다운로드되므로, Excel을 사용하여 필터링하거나 검색할 수 있습니다. 소유권이 있는 한, 여러 흐름의 실행 기록을 다운로드할 수도 있습니다. [흐름 실행 기록 다운로드](https://flow.microsoft.com/blog/download-history-recurrence/)를 참조하세요.

#### <a name="connections-and-custom-connectors-in-flow"></a>Flow의 연결 및 사용자 지정 커넥터

연결하려면 사용자가 APIO, SaaS 응용 프로그램 및 사용자 지정 개발 시스템에 연결할 수 있는 자격 증명을 제공해야 합니다. 이러한 연결은 해당 연결을 설정한 사용자가 소유하며 제품에서 [관리](/flow/add-manage-connections)될 수 있습니다. 흐름이 다시 할당된 후 관리자는 PowerShell cmdlet을 사용하여 이러한 연결을 나열하고 사용자 삭제의 일부로 삭제할 수 있습니다.

사용자 지정 커넥터를 사용하면 조직에서 기본 커넥터를 사용할 수 없는 시스템에 연결하여 Flow의 기능을 확장할 수 있습니다. 사용자 지정 커넥터 작성자는 자신의 커넥터를 조직의 다른 사람과 [공유](/flow/register-custom-api)할 수 있습니다. DSR 삭제 요청을 받은 후 관리자는 비즈니스 중단을 방지하기 위해 이러한 커넥터의 소유권을 다시 할당해야 합니다. 이 프로세스를 신속히 처리하기 위해 관리자는 PowerShell cmdlet을 사용하여 사용자 지정 커넥터를 나열하거나, 다시 할당하거나, 삭제할 수 있습니다.

### <a name="forms"></a>Forms

다음 섹션에서는 Microsoft Forms의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

Forms 사용자는 <https://forms.office.com>으로 이동한 후 **내 양식** 을 선택하여 자신이 만든 양식을 볼 수 있습니다. 또한 **공유한 항목** 을 선택하여 다른 사람이 링크를 통해 공유한 양식을 볼 수 있습니다. 정렬할 양식이 많은 경우 사용자는 제품 내 검색 창을 사용하여 제목 또는 작성자별로 양식을 검색할 수 있습니다. Microsoft Forms가 DSR에 응답적인 개인 데이터가 있을 가능성이 있는 곳에 있는지 여부를 확인하려면 데이터 주체에게 **공유한 항목** 목록을 검색하여 데이터 주체에게 양식을 보낸 사용자(“양식 소유자”)를 확인해 달라고 요청합니다. 그런 다음 양식 소유자에게 양식을 보고 DSR에 중요한지 확인할 수 있도록 위쪽 탐색 모음에서 **공유** 를 선택하고 특정 양식에 대한 링크를 보내 달라고 요청할 수 있습니다.

#### <a name="access"></a>Access

관련 Forms가 발견되면 **응답** 탭을 클릭하여 Forms에 대한 응답에 액세스할 수 있습니다. [퀴즈 결과를 확인](https://support.microsoft.com/office/check-and-share-your-quiz-results-c4a9b45c-d62f-4eb7-b5db-ad81892c7c07)하거나 [form 결과](https://support.office.com/article/02859424-341d-406f-b32a-9a0fbaf357af)를 확인하는 방법에 대해 자세히 알아보세요. Excel에서 응답 결과를 검토하려면 **응답** 탭을 선택한 다음 **Excel에서 열기** 를 선택합니다. 데이터 주체에게 Form 사본을 보내려는 경우, 응용 프로그램에 표시된 관련 질문 및 답변의 스크린샷을 서식있는 텍스트 형식으로 찍을 수 있거나, 데이터 주체에게 결과를 Excel 사본으로 보낼 수 있습니다. Excel을 사용하면서 설문 결과의 데이터 주체 부분만 공유하려는 경우 결과를 공유하기 전에 특정 행이나 열을 삭제하거나 나머지 섹션을 삭제합니다. 또는 **공유\>복제본에 대한 링크를 가져오기**(서식 파일로 공유 아래)로 이동하여 전체 Form의 복제본을 데이터 주체에게 제공할 수 있습니다.

#### <a name="delete"></a>삭제

모든 설문 조사, 퀴즈, 질문 사항 또는 투표는 해당 소유자가 영구적으로 삭제할 수 있습니다. "개인 정보 삭제" DSR을 수락하여 양식을 완전히 삭제하려면 양식 목록에서 해당 양식을 찾아서 미리 보기 창의 오른쪽 위에 있는 일련의 점(줄임표)을 선택한 후 **삭제** 를 선택합니다. 양식이 삭제되고 나면 검색할 수 없습니다. 자세한 내용은 [양식 삭제](https://support.microsoft.com/office/delete-a-form-2207e468-ce1b-4c4a-a256-caf631d87af0)를 참조하세요.

#### <a name="export"></a>내보내기

양식 질문과 대답을 Excel 파일로 내보내려면 양식을 열고 **응답** 탭을 선택한 다음 **Excel에서 열기** 를 선택합니다.

### <a name="kaizala"></a>Kaizala

다음 섹션에서는 Microsoft Kaizala의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

관리자는 Kaizala 관리 포털에서 조직 그룹 내에서 공유되는 사용자의 조직 데이터에 액세스할 수 있습니다. 조직 데이터는 조직의 보존 정책에 따라 지정된 기간 동안 보존됩니다. Kaizala 서버는 사용자 데이터 외에, 다음 유형의 조직 데이터도 저장합니다.

- 조직 그룹에 속한 구성원 목록
- 조직 그룹에서 공유되는 메시지 및 응답을 나타내는 조직 그룹 메시지 데이터
- 조직의 사용자 목록
- 조직의 모든 사용자에 대해 캡처된 제품 및 서비스 사용 현황 데이터
- 조직에서 만든 Kaizala 작업
- Kaizala 커넥터 데이터

데이터 주체는 소비자 데이터용 Kaizala 모바일 앱을 사용하여 사용자의 소비자 데이터에 액세스할 수 있습니다. 소비자 데이터에는 다음과 같은 유형의 데이터가 포함됩니다.

- Kaizala의 비공개 그룹에 속하는 데이터(90일 동안 Kaizala 서버에 저장)
- 사용자의 프로필 정보 및 사용자의 연락처
- 사용자와 같은 그룹에 속하는 구성원 목록
- 그룹 간에 공유되는 그룹 메시지 및 응답
- 사용자의 연락처 목록(Kaizala 서비스에 저장)
- Kaizala에서 사용자가 수행한 거래(인도의 Kaizala 사용자에게만 해당)
- 사용자의 제품 및 서비스 사용 현황 데이터

#### <a name="access"></a>Access

Kaizala 사용자는 해당 모바일 장치로 이동하여 장치에서 만들어진 Kaizala 콘텐츠를 확인할 수 있습니다. Kaizala 모바일 앱이 DSR에 해당하는 개인 데이터가 있을 가능성이 높은 위치인지 확인하기 위해 데이터 주체에게 Kaizala 앱에서 요청된 정보를 검색하도록 요청할 수 있습니다.

#### <a name="export"></a>내보내기

조직의 사용자가 Kaizala를 사용하면 소비자 데이터가 생성되며, 사용자가 조직 그룹에 참여할 경우 조직 데이터가 생성될 수 있습니다. 관리자는 Kaizala 관리 포털에서 사용자의 조직 데이터를 내보낼 수 있습니다. Kaizala 소비자 사용자는 Kaizala 모바일 앱에서 해당 개인 데이터를 내보낼 수 있습니다. 두 경우 모두, 관리자 또는 사용자가 Kaizala 데이터를 내보낼 때 제품 및 서비스 사용 현황 데이터도 내보내집니다. 자세한 내용은 다음을 참조하세요.

- [Kaizala에서 사용자의 조직 데이터 내보내기 또는 삭제](/office365/kaizala/export-or-delete-a-user-s-data)
- [Kaizala 모바일 앱에서 데이터 내보내기 또는 삭제](/office365/kaizala/export-or-delete-your-data)

#### <a name="delete"></a>삭제

Kaizala 관리자는 Kaizala 관리 포털에서 Kaizala 사용자의 계정을 제거할 수 있습니다. 사용자 계정이 삭제되면 해당 사용자는 조직에 속한 모든 그룹에서 제거되고 조직 데이터가 해당 장치에서 삭제됩니다. 

사용자의 모바일 장치에서 모든 개인 데이터를 제거하기 위해 Kaizala 사용자는 해당 Kaizala 계정을 삭제할 수 있습니다. 계정이 삭제되면 채팅, 사진을 비롯한 모든 관련 Kaizala 콘텐츠와 기타 데이터가 장치에서 삭제됩니다.

자세한 내용은 다음을 참조하세요.

- [Kaizala에서 사용자의 조직 데이터 내보내기 또는 삭제](/office365/kaizala/export-or-delete-a-user-s-data)
- [Kaizala 모바일 앱에서 데이터 내보내기 또는 삭제](/office365/kaizala/export-or-delete-your-data)

### <a name="planner"></a>Planner

다음 섹션에서는 Microsoft Planner의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

Planner 계획은 Microsoft 365 그룹과 연결되고, Microsoft 365 그룹의 파일은 해당 그룹의 연결된 SharePoint Online 사이트에 저장됩니다. 즉, Microsoft 365 그룹 사이트를 검색하여 콘텐츠 검색을 사용하면 Planner 파일을 찾을 수 있습니다. 이렇게 하려면 Microsoft 365 그룹에 대한 URL이 있어야 합니다. "Office 365의 콘텐츠 검색" 도움말 항목에서 [Microsoft Teams 및 Microsoft 365 그룹 검색](/microsoft-365/compliance/content-search)을 참조하여 해당 SharePoint Online 사이트에서 Planner 파일을 검색하는 데 도움이 되는 Microsoft 365 그룹에 대한 정보를 얻는 방법에 대한 팁을 참조하세요.

#### <a name="access"></a>Access

이전에 설명한 것처럼 계획과 연관된 기본 SharePoint Online 사이트 및 사서함을 검색할 수 있습니다. 그런 다음 관련 검색 결과를 미리 보거나 다운로드하여 데이터에 액세스할 수 있습니다.

#### <a name="delete"></a>삭제

사용자가 속해 있는 계획에 액세스할 수 있는 권한을 직접 부여하거나 사용자로 로그인해 변경 작업을 수행하여 해당 사용자의 개인 정보를 수동으로 삭제할 수 있습니다. [Microsoft Planner에서 사용자 데이터 삭제](https://support.office.com/article/delete-user-data-in-microsoft-planner-4349ded2-1891-4896-8e27-05fd40f3929f)를 참조하세요.

#### <a name="export"></a>내보내기

PowerShell 스크립트를 사용하여 Planner에서 사용자의 데이터를 내보낼 수 있습니다. 데이터를 내보내는 경우 사용자가 속해 있는 각 계획에 대해 별도의 JSON 파일을 내보냅니다. [Microsoft Planner에서 사용자 데이터 내보내기](https://support.office.com/article/export-user-data-from-microsoft-planner-91258c96-b353-4da1-b6d9-d78e4809cf08)를 참조하세요.

### <a name="power-bi"></a>Power BI

다음 섹션에서는 Microsoft Power BI의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색
대시보드, 보고서, 통합 문서 및 데이터 집합을 비롯한 Power BI의 다른 작업 영역에서 콘텐츠를 검색할 수 있습니다. 각 유형의 작업 영역에는 작업 영역을 검색하는 데 사용할 수 있는 검색 필드가 포함되어 있습니다. 자세한 내용은 [Power BI 서비스에서 콘텐츠 검색, 찾기 및 정렬](/power-bi/service-navigation-search-filter-sort)을 참조하세요.

#### <a name="access"></a>Access

Power BI의 보고서에서 대시보드, 보고서 및 시각적 개체를 인쇄하여 실제 복사본을 만들 수 있습니다. 전체 보고서를 인쇄할 수는 없습니다. 한번에 한 페이지만 인쇄할 수 있습니다. 이렇게하려면 보고서로 이동하고 검색 필드를 사용하여 특정 데이터를 찾은 다음 해당 페이지를 인쇄합니다. [Power BI 서비스에서 인쇄](/power-bi/service-print)를 참조하세요.

#### <a name="delete"></a>삭제

대시보드, 보고서 및 통합 문서를 삭제하려면 [Power BI 서비스에서 거의 모든 항목 삭제](/power-bi/service-delete)를 참조하세요.

대시보드, 보고서 또는 통합 문서를 삭제해도 기본 데이터 집합은 삭제되지 않습니다. Power BI는 완전성과 정확성을 위해 기본 원본 데이터에 대한 실시간 연결에 의존하므로 기본 원본 데이터에서 개인 데이터를 삭제해야 합니다. 예를 들어 Dynamics 365 for Sales가 실시간 데이터 원본으로 연결된 Power BI 보고서를 만든 경우 Dynamics 365 for Sales에서 해당 데이터를 수정해야 합니다.

데이터가 삭제된 후 Power BI의 [예약된 데이터 새로 고침](/power-bi/refresh-scheduled-refresh) 기능을 사용하여 Power BI에 저장된 데이터 집합을 업데이트할 수 있습니다. 이후에는 해당 데이터를 활용한 모든 Power BI 보고서 또는 대시보드에서 삭제된 데이터가 더 이상 반영되지 않습니다.  GDPR 요구 사항을 준수하려면 적절한 주기로 데이터를 새로 고치는 정책이 있어야 합니다.

#### <a name="export"></a>내보내기

데이터 이동성 요청을 용이하게 하기 위해 Power BI에서 대시보드와 보고서를 내보낼 수 있습니다.

- 대시보드 및 보고서에 대한 기본 데이터를 정적 Excel 파일로 내보낼 수 있습니다. [Power BI 서비스에서 인쇄](/power-bi/service-print)의 동영상을 참조하세요. Excel을 사용하여 이동성 요청에 포함되도록 개인 데이터를 편집한 후 자주 사용되고 컴퓨터에서 읽을 수 있는 형식(예: .csv 또는 .xml)으로 저장할 수 있습니다.
- Office 365의 Power BI에서 .pbix 파일로 보고서를 내보낼(다운로드) 수 있습니다(원래 Power BI Desktop을 사용하여 게시된 경우). 그런 다음 이 파일을 Power BI Desktop으로 가져와 다른 조직의 Power BI 서비스에 게시(내보내기)할 수 있습니다. [Power BI 서비스에서 Desktop으로 보고서 내보내기](/power-bi/service-export-to-pbix)를 참조하세요.

### <a name="powerapps"></a>PowerApps

다음 섹션에서는 Microsoft Power Apps의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다. 다음 단계에서는 관리자가 앱과 해당 종속 리소스를 새 소유자에게 전환하여 비즈니스 중단을 제한할 수 있는 방법을 간략하게 설명합니다.

#### <a name="discover"></a>검색

PowerApps는 조직 내에서 공유 및 사용할 수 있는 앱 빌드용 서비스입니다. 앱을 빌드하거나 실행하는 프로세스의 일부로 사용자는 앱, 환경, 연결, 사용자 지정 커넥터, 사용 권한 등 여러 유형의 리소스와 데이터를 PowerApps 서비스에 저장하게 됩니다.

PowerApps와 관련된 DSR 요청을 용이하게 하기 위해 [PowerApps 관리 센터](https://admin.powerapps.com/) 및 [PowerApps 관리 PowerShell cmdlet](https://go.microsoft.com/fwlink/?linkid=871804)에 노출된 관리 작업을 활용할 수 있습니다. 이러한 도구에 액세스하려면 다음 권한이 있는 계정이 필요합니다.

- 유료 PowerApps Plan 2 라이선스 또는 PowerApps Plan 2 평가판 라이선스. [여기](https://web.powerapps.com/trial)에서 30일 평가판 라이선스에 등록할 수 있습니다.
- [전역 관리자](/microsoft-365/admin/add-users/assign-admin-roles) 또는
- [Azure Active Directory 전역 관리자](/azure/active-directory/active-directory-assign-admin-roles-azure-portal)

개인 데이터를 찾는 방법에 대한 자세한 내용은 [PowerApps 개인 데이터 검색](https://go.microsoft.com/fwlink/?linkid=871880)을 참조하세요.

PowerApps 서비스에는 사용자가 Common Data Service 데이터베이스 내에 표준 및 사용자 지정 엔터티에 데이터를 저장할 수 있도록 하는 응용 프로그램에 대한 Common Data Service도 포함 되어 있습니다. [PowerApps Maker 포털](https://web.powerapps.com)에서 이러한 엔터티에 저장된 데이터를 확인하고, [고급 검색](/dynamics365/customer-engagement/basics/save-advanced-find-search)의 제품내 검색 기능을 사용하여 엔터티에서 특정 데이터를 검색할 수 있습니다. Common Data Service에서 개인 데이터를 검색하는 방법에 대한 자세한 내용은 [Common Data Service 개인 데이터 검색](https://go.microsoft.com/fwlink/?linkid=871881)을 참조 하세요.

#### <a name="access"></a>Access

관리자는 [PowerApps 관리 센터](https://admin.powerapps.com/) 또는 [PowerApps 관리 PowerShell cmdlet](https://go.microsoft.com/fwlink/?linkid=871804)을 사용하여 앱 및 연결된 리소스(흐름, 연결, 사용자 지정 커넥터 포함)를 액세스하고 실행할 수 있는 권한을 자신에게 할당할 수 있습니다.

사용자의 앱에 대한 액세스 권한을 얻은 후에는 웹 브라우저를 사용하여 앱을 열 수 있으며, 앱을 연 후에는 데이터의 스크린샷을 만들 수 있습니다. [웹 브라우저에서 PowerApps 사용](/powerapps/run-app-browser)을 참조하세요.

#### <a name="delete"></a>삭제

PowerApps를 통해 사용자는 조직의 일상적인 운영에 중요한 요소일 수 있는 LOB(기간 업무) 응용 프로그램을 만들 수 있으므로 사용자가 조직을 떠나고 해당 Office 365 계정이 삭제된 경우 관리자는 이 사용자가 소유한 앱을 삭제할지 또는 새 소유자에게 다시 할당할지 결정해야 합니다. 이는 조직에서 앱을 새 소유자에게 전환하여 공유 비즈니스 프로세스에 사용될 수 있는 앱에 대한 비즈니스 중단을 방지하도록 도와주기 위한 것입니다.

앱과 같은 공유 데이터의 경우 관리자는 해당 사용자의 공유 데이터를 영구적으로 삭제할지 또는 조직 내에서 자신이나 다른 누군가에게 데이터를 재할당하여 유지할지 결정해야 합니다. [PowerApps 개인 데이터 삭제](https://go.microsoft.com/fwlink/?linkid=871883)를 참조하세요.

또한 관리자는 제품 내 기능을 사용하여 사용자가 Common Data Service For Apps 데이터베이스의 엔터티에 저장한 모든 데이터를 검토하고 필요한 경우 삭제해야 합니다. [Common Data Service 사용자 개인 데이터 삭제](https://go.microsoft.com/fwlink/?linkid=871886)를 참조하세요.

#### <a name="export"></a>내보내기

관리자는 [PowerApps 관리 센터](https://admin.powerapps.com/) 및 [PowerApps 관리 PowerShell cmdlet](https://go.microsoft.com/fwlink/?linkid=871804)을 사용하여 PowerApps 서비스 내에 저장된 사용자의 개인 데이터를 내보낼 수 있습니다. [PowerApps 개인 데이터 내보내기](https://go.microsoft.com/fwlink/?linkid=871883)를 참조하세요.

[상세하게 찾기](/dynamics365/customer-engagement/basics/save-advanced-find-search)의 제품 내 검색 기능을 사용하여 엔터티에서 사용자의 개인 데이터를 검색할 수도 있습니다. Common Data Service에서 개인 데이터 내보내기에 대한 자세한 내용은 [Common Data Service 개인 데이터 내보내기](https://go.microsoft.com/fwlink/?linkid=871889)를 참조하세요.

#### <a name="connections-and-custom-connectors-in-powerapps"></a>PowerApps의 연결 및 사용자 지정 커넥터

연결하려면 사용자가 APIO, SaaS 응용 프로그램 및 사용자 지정 개발 시스템에 연결할 수 있는 자격 증명을 제공해야 합니다. 이러한 연결은 해당 연결을 설정한 사용자가 소유하며 제품에서 [관리](/powerapps/maker/canvas-apps/add-data-connection)될 수 있습니다. PowerApps가 다시 할당된 후 관리자는 PowerShell cmdlet을 사용하여 이러한 연결을 나열하고 사용자 삭제의 일부로 삭제할 수 있습니다.

사용자 지정 커넥터를 사용하면 조직에서 기본 커넥터를 사용할 수 없는 시스템에 연결하여 PowerApps의 기능을 확장할 수 있습니다. 사용자 지정 커넥터 작성자는 자신의 커넥터를 조직의 다른 사람과 [공유](/connectors/custom-connectors/use-custom-connector-powerapps)할 수 있습니다. DSR 삭제 요청을 받은 후 관리자는 비즈니스 중단을 방지하기 위해 이러한 커넥터의 소유권을 다시 할당해야 합니다. 이 프로세스를 신속히 처리하기 위해 관리자는 PowerShell cmdlet을 사용하여 사용자 지정 커넥터를 나열하거나, 다시 할당하거나, 삭제할 수 있습니다.

### <a name="project-online"></a>Project Online

다음 섹션에서는 Microsoft Project Online의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover-and-access"></a>검색 및 액세스

콘텐츠 검색을 사용하여 프로젝트와 연결된 SharePoint Online 사이트를 검색할 수 있습니다(프로젝트를 처음 만들면 연결된 SharePoint Online 사이트를 만들 수 있는 옵션이 제공됨). 콘텐츠 검색은 Project Online에서 실제 프로젝트의 데이터를 검색하는 것이 아니라 연결된 사이트를 검색합니다. 콘텐츠 검색은 제목에 언급된 사용자와 같은 프로젝트에 대한 메타데이터를 검색하지만 이는 DSR과 관련된 데이터가 포함된 프로젝트를 찾고 액세스하는 데 도움이 될 수 있습니다.

> [!TIP]
> 사이트가 프로젝트와 연결된 조직의 사이트 모음에 대한 URL은 `https://<your org>.sharepoint.com/sites/pwa`(예: **<https://contoso.sharepoint.com/pwa>**). 이 특정 사이트 모음을 콘텐츠 검색의 위치로 사용한 다음 검색 쿼리에서 프로젝트의 이름을 사용할 수 있습니다. 또한 IT 관리자는 SharePoint 관리 센터의 사이트 모음 페이지를 사용하여 조직의 PWA 사이트 모음 목록을 가져올 수 있습니다.

#### <a name="delete"></a>삭제

Project Online 환경에서 사용자에 대한 정보를 삭제할 수 있습니다. [Project Online에서 사용자 데이터 삭제](https://support.office.com/article/delete-user-data-from-project-online-252fa593-9c25-47ed-b861-643fe8bf1cb7)를 참조하세요.

#### <a name="export"></a>내보내기

Project Online 환경에서 특정 사용자의 콘텐츠를 내보낼 수 있습니다. 이 데이터는 JSON 형식의 여러 파일로 내보내집니다. 단계별 지침은 [Project Online에서 사용자 데이터 내보내기](https://support.office.com/article/export-user-data-from-project-online-27f3838d-3dbe-4b98-80dc-df55f851154d)를 참조하고, 내보내는 파일에 대한 자세한 내용은 [Project Online 내보내기 json 개체 정의](https://support.office.com/article/project-online-export-json-object-definitions-ce5faeae-9af4-4696-b847-a1f4f20327c7)를 참조하세요.

### <a name="publisher"></a>Publisher

다음 섹션에서는 Microsoft Publisher의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

대부분의 Office 응용 프로그램에서 사용하는 방법과 마찬가지로 앱 내 검색 기능을 사용하여 Publisher 파일에서 텍스트를 찾을 수 있습니다. [텍스트 찾기 및 바꾸기](https://support.office.com/article/find-and-replace-text-bfe54275-b7c7-4d0f-904d-a2f38d322268)를 참조하세요.

#### <a name="access"></a>액세스

데이터를 찾은 후 해당 데이터의 스크린샷을 찍거나 Word 또는 텍스트 파일에 복사하여 붙여넣고 데이터 주체에 제공할 수 있습니다. 발행물을 Word, PDF 또는 XPS 파일로 저장할 수도 있습니다. 자세한 내용은 다음을 참조하세요.

  - [발행물을 Word 문서로 저장](https://support.microsoft.com/office/save-a-publication-as-a-word-document-b5eaaae5-6f1b-48c1-bebc-44460376b693)
  - [다른 이름으로 저장 또는 Publisher를 사용하여 발행물을 .pdf 또는.xps로 변환](https://support.microsoft.com/office/save-as-or-convert-a-publication-to-pdf-or-xps-using-publisher-657332d0-d2c2-464a-9870-e9b3d22e6469)

#### <a name="export"></a>내보내기

데이터 주체에 실제 Publisher 파일을 제공하거나 이전에 설명한 바와 같이 발행물을 Word, PDF 또는 XPS 파일로 저장할 수 있습니다. 다음을 참조하세요.

  - [발행물을 Word 문서로 저장](https://support.microsoft.com/office/save-a-publication-as-a-word-document-b5eaaae5-6f1b-48c1-bebc-44460376b693)
  - [다른 이름으로 저장 또는 Publisher를 사용하여 발행물을 .pdf 또는.xps로 변환](https://support.microsoft.com/office/save-as-or-convert-a-publication-to-pdf-or-xps-using-publisher-657332d0-d2c2-464a-9870-e9b3d22e6469)

#### <a name="delete"></a>삭제

발행물에서 콘텐츠를 삭제하고, 전체 페이지를 삭제하거나, 전체 Publisher 파일을 삭제할 수 있습니다. [페이지 추가 또는 삭제](https://support.office.com/article/add-or-delete-pages-daf71e39-86e0-4bbc-a186-d5ec70450b08)를 참조하세요.

### <a name="stream"></a>Stream

다음 섹션에서는 Microsoft Stream의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

생성되었거나 Stream으로 업로드된 콘텐츠 중에서 데이터 주체 요청과 관련이 있을 수 있는 콘텐츠를 검색하기 위해 Stream 관리자는 사용자 보고서를 실행하여 Stream 사용자가 업로드했거나, 만들었거나, 게시된 비디오, 비디오 설명, 그룹, 채널 또는 댓글을 확인할 수 있습니다. 보고서 생성 방법에 대한 지침은 [Microsoft Stream에서 사용자 데이터 관리](/stream/managing-user-data)를 참조하세요. 보고서 출력은 HTML 형식이고 관심이 있을 수 있는 비디오로 이동하는 데 사용할 수 있는 하이퍼링크를 포함합니다. 사용자 지정 권한이 설정된 비디오를 보려고 하며 비디오의 의도된 원래 사용자가 아닌 경우 관리자 모드에서 비디오를 볼 수 있습니다. 자세한 내용은 [Microsoft Stream의 관리자 기능](/stream/manage-content-permissions)을 참조하세요.  

#### <a name="access"></a>Access

데이터 주체 요청의 특성에 따라, 위에서 설명한 보고서 사본을 사용하여 데이터 주체 요청을 충족할 수 있습니다. 사용자 보고서에는 Stream 사용자의 이름 및 고유 ID, 사용자가 업로드한 비디오 목록, 사용자에게 액세스 권한이 있는 비디오 목록, 사용자가 만든 채널 목록, 사용자가 구성원으로 속해 있는 모든 그룹의 목록 및 사용자가 비디오에 대해 남긴 모든 댓글 목록이 포함됩니다. 보고서에는 사용자가 사용자 보고서에 나열된 각 비디오를 시청했는지 여부도 추가적으로 표시됩니다. DSR 요청을 충족하기 위해 데이터 주체에게 비디오에 대한 액세스 권한을 제공하려는 경우 비디오를 공유할 수 있습니다.

#### <a name="export"></a>내보내기

Stream에 대한 액세스 섹션을 참조하세요. 

#### <a name="delete"></a>삭제

비디오 또는 기타 Stream 콘텐츠를 삭제하거나 편집하기 위해 Stream 관리자는 필요한 기능을 수행하기 위해 관리자 모드에서 보기를 선택할 수 있습니다. 자세한 내용은 [Microsoft Stream의 관리자 기능](/stream/manage-content-permissions)을 참조하세요. 사용자가 조직을 떠났으며 업로드한 비디오 옆에 표시되는 이름을 제거하고 싶어하는 경우 해당 이름을 제거하거나 다른 이름으로 바꿀 수 있습니다. 자세한 내용은 [Microsoft Stream에서 삭제된 사용자 관리](/stream/managing-deleted-users)를 참조하세요.

### <a name="sway"></a>Sway

다음 섹션에서는 Microsoft Sway의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

Sway ([www.sway.com](https://sway.office.com/)에서 찾음)를 사용하여 만든 콘텐츠는 소유자와 작성자가 Sway를 볼 수 있도록 허용한 사람만 볼 수 있습니다. [Sway의 개인 정보 설정](https://support.microsoft.com/office/privacy-settings-in-sway-394b551c-be6f-4bd7-a70a-f318d72bf217)을 참조하세요. Sway가 사용자의 DSR에 대응하는 개인 데이터가 있는 장소인지 여부를 확인하려면 데이터 주체 및 데이터 주체에 대한 컨텐츠를 생성할 가능성이 있는 조직 사용자에게 Sways를 검색하고 데이터 주체의 요청에 응답하는 개인 데이터를 포함할 가능성이 있는 Sways를 공유하도록 요청할 수 있습니다. Sway를 공유하는 방법에 대한 자세한 내용은 이 [Sway 공유](https://support.microsoft.com/office/share-your-sway-1cf853b8-ef7e-46b0-b704-003e58d28998) 문서에서 "조직 계정에서 Sway를 공유하세요"를 참조하세요.

#### <a name="access"></a>Access

Sway에서 데이터 주체와 공유할 개인 데이터를 찾은 경우 여러 가지 방법 중 하나를 통해 데이터 주체에게 데이터에 대한 액세스 권한을 제공할 수 있습니다. 데이터 주체에게 Sway 온라인 버전(위 설명 참조)의 복사본을 제공할 수 있습니다. 공유할 Sway의 관련 부분에 대한 스크린샷을 만들거나, Sway를 인쇄 또는 Word에 다운로드하거나, Sway를 PDF로 변환할 수 있습니다. Sway를 다운로드하는 방법은 아래의 "내보내기" 섹션에 자세히 설명되어 있습니다.

#### <a name="delete"></a>삭제

Sway를 삭제하는 방법을 알아보려면 [Sway의 개인 정보 설정](https://support.microsoft.com/office/privacy-settings-in-sway-394b551c-be6f-4bd7-a70a-f318d72bf217)에서 "내 Sway를 삭제하려면 어떻게 해야 하나요?" 섹션으로 이동하세요.

#### <a name="export"></a>내보내기

Sway를 내보내려면 다운로드할 Sway를 열고 오른쪽 위에서 일련의 점(줄임표)을 선택한 후 **내보내기** 를 선택하고 **Word** 또는 **PDF** 를 선택합니다.

### <a name="whiteboard"></a>Whiteboard

다음 섹션에서는 Microsoft Whiteboard의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

- [Surface Hub의 Whiteboard 2016](#whiteboard-2016-on-surface-hub)
- [다른 모든 플랫폼의 Whiteboard](#whiteboard-for-pc-surface-hub-and-other-platforms)

#### <a name="whiteboard-2016-on-surface-hub"></a>Surface Hub의 Whiteboard 2016

이 섹션에서는 Surface Hub에서 기본 제공 Whiteboard 2016 앱을 사용하여 만든 데이터에 대한 DSR 요청에 응답하는 방법을 설명합니다.

##### <a name="discover"></a>검색

화이트보드 파일(.wbx 파일)은 사용자의 비즈니스용 OneDrive 계정에 저장됩니다. 데이터 주체 또는 다른 사용자에게 만든 화이트보드에 DSR 요청에 해당하는 개인 데이터가 포함되어 있을 수 있는지 물어볼 수 있습니다. 이러한 사용자는 화이트보드를 공유하거나 데이터 주체에게 사본을 제공할 수 있습니다.

화이트보드를 액세스 및 전송하려면 

1. 자기 자신에게 사용자의 비즈니스용 OneDrive 계정에 대한 액세스 권한을 부여합니다. [이전 사용자의 데이터에 대한 액세스 권한 얻기 및 백업](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data)의 "이전 직원의 비즈니스용 OneDrive 문서에 대한 액세스 권한 얻기" 섹션을 참조하세요.
2. 사용자의 비즈니스용 OneDrive 계정에서 화이트보드 앱 데이터 폴더로 이동한 후 전송하려는 화이트보드의 .wbx 파일을 복사합니다.
3. 자기 자신에게 데이터 주체의 비즈니스용 OneDrive 계정에 대한 액세스 권한을 부여한 후 화이트보드 앱 데이터 폴더로 이동합니다.
4. 이전 단계에서 복사한 .wbx 파일을 붙여넣습니다.

##### <a name="access"></a>Access

화이트보드에서 DSR 액세스 요청에 해당하는 개인 데이터를 찾으면 다음과 같은 여러 가지 방법으로 데이터 주체에게 화이트보드에 대한 액세스 권한을 제공할 수 있습니다.

- 화이트보드의 관련 부분에 대한 스크린샷을 만듭니다.
- .wbx 파일의 복사본을 데이터 주체의 비즈니스용 OneDrive 계정에 업로드합니다. .wbx 파일을 액세스 및 전송하는 단계는 이전 섹션을 참조하세요.
- 화이트보드 복사본을 .png 파일로 내보냅니다.

##### <a name="export"></a>내보내기

화이트보드의 복사본을 가져온 경우 내보낼 수 있습니다. 

1. Surface Hub에서 Whiteboard를 시작합니다.
2. 공유 단추를 탭하고 복사본 내보내기를 선택합니다. 화이트보드를 OneNote(.one) 파일이나 이미지(.png) 파일로 내보낼 수 있습니다.

##### <a name="delete"></a>삭제

자기 자신에게 사용자의 비즈니스용 OneDrive 계정에 대한 액세스 권한을 부여한 후 화이트보드를 삭제할 수 있습니다.

1. 자기 자신에게 데이터 주체의 비즈니스용 OneDrive 계정에 대한 액세스 권한을 부여합니다. [이전 사용자의 데이터에 대한 액세스 권한 얻기 및 백업](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data)의 "이전 직원의 비즈니스용 OneDrive 문서에 대한 액세스 권한 얻기" 섹션을 참조하세요.
2. 화이트보드 앱 데이터 폴더로 이동한 후 이 폴더의 내용을 삭제합니다.

#### <a name="whiteboard-for-pc-surface-hub-and-other-platforms"></a>PC, Surface Hub 및 기타 플랫폼용 Whiteboard

관리자는 새로운 화이트보드 탭에서 데이터에 대한 DSR 요청을 수신할 경우 Whiteboard PowerShell을 사용하여 자기 자신(또는 다른 사용자)을 사용자 화이트보드의 소유자로 추가할 수 있습니다. 그러면 관리자는 화이트보드 액세스, 내보내기 및 삭제를 비롯한 작업을 수행할 수 있습니다. **Set-WhiteboardOwner** cmdlet을 사용하여 자기 자신이나 다른 사용자를 화이트보드의 소유자로 추가하거나 **Invoke-TransferAllWhiteboards** cmdlet을 사용하여 특정 사용자에 대한 모든 화이트보드의 소유권을 새 소유자에게 이전할 수 있습니다. 이러한 cmdlet을 사용하고 Whiteboard PowerShell 모듈을 설치하는 방법에 대한 내용은 [Microsoft Whiteboard cmdlet 참조](/powershell/module/whiteboard/)를 참조하세요.

화이트보드에 대한 소유권을 얻은 후에는 [화이트보드 지원 문서](https://go.microsoft.com/fwlink/?linkid=872780)에서 화이트보드 액세스, 내보내기 및 삭제 방법에 대한 자세한 지침을 참조하세요.

### <a name="yammer"></a>Yammer

다음 섹션에서는 Microsoft Yammer의 앱 내 기능을 사용하여 개인 데이터를 찾고, 액세스하고, 내보내고, 삭제하는 방법을 설명합니다.

#### <a name="discover"></a>검색

Yammer 관리 센터에서 Yammer 확인된 관리자 (전역 관리자 또는 Yammer에 설정된 관리자)는 지정된 사용자에 관련된 데이터를 내보낼 수 있습니다. 내보내기에는 사용자가 게시하고 수정한 메시지와 파일 및 사용자가 만든 주제 및 그룹에 대한 정보가 포함됩니다. 사용자별 데이터 내보내기가 실행되면 관리자는 선택한 경우 사용자에게 제공할 수 있는 사용자의 계정 활동 데이터가 포함된 받은 편지함 메시지를 받습니다. 자세한 지침은 [Yammer Enterprise: 개인 정보](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)를 참조하세요.

사용자별 내보내기는 단일 네트워크에 적용되므로 사용자가 외부 Yammer 네트워크에 있는 경우 관리자는 홈 네트워크뿐와 해당 외부 네트워크에 데이터를 내보내야 합니다.

데이터 내보내기에 포함되지 않은 데이터에 액세스하려면 사용자의 프로필, 설정, 그룹 구성원 자격, 책갈피에 지정된 메시지, 팔로우한 사용자 및 팔로우한 항목에 대한 스크린샷을 만들 수 있습니다. 사용자 또는 관리자는 이 정보를 수집할 수 있습니다.  자세한 내용은 [Yammer Enterprise: 개인 정보](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)를 참조하세요.

#### <a name="access"></a>Access

메시지의 전체 텍스트 및 파일의 내용을 포함하여 내보낸 파일의 데이터를 볼 수 있습니다. 또한 내보낸 파일의 링크를 선택하여 Yammer에 게시된 메시지와 파일 및 사용자가 만든 그룹과 항목, 사용자가 링크한 메시지, 사용자가 멘션한 메시지, 사용자가 투표한 설문 조사 및 사용자가 추가한 링크로 직접 이동할 수 있습니다.

사용자 단위 데이터 내보내기에 다음은 포함되지 않습니다.

- 사용자의 프로필:
    - Yammer ID가 있는 사용자는 자신의 프로필에 대한 모든 권한을 가집니다. 프로필을 보고 수정하는 방법은 [Yammer 프로필 및 설정 변경](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851)을 참조하세요.
    
    - 사용자에게 Office 365 ID가 있는 경우 Office 365에서 Yammer 사용자 프로필을 자동으로 가져옵니다. 즉, AAD(Azure Active Directory)에서 프로필 정보를 가져오게 됩니다. Yammer 사용자는 Yammer에서 일시적으로 자신의 프로필을 변경할 수 있지만 이러한 변경 내용은 AAD에서 변경 내용이 있는 경우 덮어쓰므로 AAD에서 디렉터리 데이터를 보고 변경해야 합니다. [Office 365에서 수명 주기 동안 Yammer 사용자 관리](/yammer/manage-yammer-users/manage-users-across-their-lifecycle) 및 [Azure Active Directory에서 사용자에 대한 프로필 정보 추가 또는 변경](/azure/active-directory/active-directory-users-profile-azure-portal)을 참조하세요.

-   사용자의 설정:

- 사용자는 자신의 설정을 보고 변경할 수 있습니다. 사용자 설정을 보고 수정하는 방법에 대한 자세한 내용은 [Yammer 프로필 및 설정 변경](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851)을 참조하세요. 관리자는 이 정보를 보고 스크린샷을 찍을 수 있으나 변경할 수는 없습니다. Yammer 설정 \> **사용자** 로 이동한 다음 사용자 이름을 선택합니다. <br/>
    - 사용자의 그룹 구성원 자격, 책갈피로 지정된 메시지, 팔로우한 사용자 및 팔로우한 항목.
    
    - 사용자는 이 정보를 볼 수 있습니다. 사용 방법에 대한 정보는 [Yammer에서 구성된 상태를 유지하는 방법](https://support.office.com/article/tips-for-staying-organized-in-yammer-40ae9666-75c0-4254-a84c-d87a9542f380)을 참조하세요. 관리자는 이 정보를 보고 스크린샷을 찍을 수 있으나 변경할 수는 없습니다. Yammer 설정 \> **사용자** 로 이동한 다음 사용자 이름을 선택합니다. 

#### <a name="export"></a>내보내기

데이터를 내보내는 방법에 대한 지침은 [Yammer Enterprise에서 GDPR 데이터 주체 요청 관리](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)를 참조하세요. 사용자가 구성원으로 있는 각 Yammer 네트워크에 대해 사용자 단위 내보내기를 실행해야 합니다.

Yammer에는 사용자가 메시지 또는 파일을 삭제한 경우 데이터를 일시 삭제하거나 영구 삭제하는 데이터 보존 설정이 있습니다. 일시 삭제하도록 설정된 경우 사용자가 삭제한 데이터는 내보내기에 포함됩니다. Yammer 데이터 보존 설정이 영구 삭제하도록 지정된 경우 삭제된 정보는 더 이상 Yammer에 저장되지 않으므로 내보내기에 포함되지 않습니다.

#### <a name="delete"></a>삭제

확인된 관리자는 DSR을 받은 경우 Yammer에서 Yammer 관리 센터를 통해 GDPR 준수 삭제를 실행할 수 있습니다. 이 옵션을 사용자 지우기라고 하며, 14일 동안 사용자를 일시 중지한 후 파일 및 메시지를 제외하고 이들의 모든 개인 데이터를 제거합니다. 사용자가 게스트인 경우 해당 사용자가 구성원으로 있는 각 외부 네트워크에 대해 이 작업을 수행해야 합니다.

> [!NOTE]
> 14일 동안 사용자의 파일 및 메시지를 제거하려는 경우 관리자는 사용자 수준 내보내기를 수행하여 파일 및 메시지를 식별한 다음, 제품 내 삭제 또는 PowerShell 스크립트를 사용하여 삭제할 항목을 결정해야 합니다. 14일 후에는 관리자가 사용자를 파일 또는 메시지에 더 이상 연결할 수 없습니다.

사용자 지우기 옵션을 통해 사용자가 삭제되면 모든 네트워크 관리자 및 확인된 관리자의 Yammer 받은 편지함으로 알림이 전송됩니다. 사용자 지우기 옵션을 선택하면 사용자의 Yammer 프로필이 삭제되지만 해당 Office 365 또는 Azure Active Directory 프로필은 삭제되지 않습니다.

사용자를 제거하기 위한 세부 단계는 [Yammer Enterprise에서 GDPR 데이터 주체 요청 관리](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)를 참조하세요.

## <a name="responding-to-dsr-rectification-requests"></a>DSR 수정 요청에 응답

데이터 주체가 Office 365에 저장된 조직의 데이터에 있는 개인 데이터를 수정하도록 요청한 경우 여러분과 조직에서는 요청을 수락하는 것이 적절한지 결정해야 합니다. 요청을 수락하기로 선택한 경우 데이터 수정에는 개인 데이터를 편집하거나 문서 또는 다른 유형/항목에서 개인 데이터를 제거하는 등의 작업이 포함될 수 있습니다. 가장 빠른 방법은 데이터/문서 소유자에게 적절한 Office 365 응용 프로그램을 사용하여 요청된 변경 작업을 수행해 달라고 요구하는 것입니다. 또는 조직의 IT 관리자에게 변경 작업을 수행하도록 요청할 수 있습니다. 이 경우 IT 관리자(또는 SharePoint Online 사이트 모음 관리자와 같은 적절한 권한을 가진 조직의 다른 사용자)는 자신 또는 DSR 작업을 수행하는 다른 사용자에게 문서 또는 콘텐츠 위치(문서를 직접 변경할 수 있는 곳)에 액세스하는 데 필요한 권한을 할당해야 할 수 있습니다.

### <a name="requesting-that-the-data-owner-to-make-the-approved-change"></a>데이터 소유자에게 승인된 변경 작업을 수행하도록 요청

개인 데이터를 수정하는 가장 직접적인 방법은 데이터 소유자에게 변경 작업을 수행하도록 요청하는 것입니다. DSR의 주체인 데이터를 찾은 후 데이터 소유자가 변경 작업을 수행할 수 있도록 다음 정보를 제공할 수 있습니다.

- 변경해야 하는 항목의 위치와 파일 이름(문서 및 기타 파일). 해당 데이터를 찾는 것은 이전에 설명된 [검색 프로세스](#using-content-search-to-find-personal-data)의 일부입니다.
- 데이터 소유자가 적용해야 하는 승인된 변경 내용

여러분 또는 DSR 조사에 참여한 다른 사람이 요청된 변경 내용이 적용되었는지 확인하는 확인 프로세스를 구현할 수 있습니다.

### <a name="gaining-access-to-a-sharepoint-online-site-or-onedrive-for-business-account-to-make-changes"></a>변경 작업을 수행하기 위해 SharePoint Online 사이트 또는 비즈니스용 OneDrive 계정에 대한 액세스 권한 얻기

데이터 소유자가 데이터 주체의 수정 요청을 구현할 수 없는 경우 IT 관리자 또는 조직의 SharePoint 관리자는 콘텐츠 위치에 대한 액세스 권한을 얻은 후 필요한 변경 작업을 수행할 수 있습니다. 또는 관리자는 여러분이나 다른 데이터 개인 정보 관리자에게 필요한 권한을 할당할 수 있습니다.

#### <a name="sharepoint-online"></a>SharePoint Online

여러분이나 다른 사용자가 해당 문서에 액세스하여 편집할 수 있도록 관리자 또는 소유자를 SharePoint Online 사이트에 할당하려면 다음을 참조하세요.

- [사이트 모음에 대한 관리자 관리](/sharepoint/manage-site-collection-administrators)

- [SharePoint 목록 또는 라이브러리에 대한 사용 권한 편집 및 관리](https://support.office.com/article/Edit-and-manage-permissions-for-a-SharePoint-list-or-library-02d770f3-59eb-4910-a608-5f84cc297782)

#### <a name="onedrive-for-business"></a>비즈니스용 OneDrive

전역 관리자는 다음과 같은 방법으로 사용자의 비즈니스용 OneDrive 계정에 액세스할 수 있습니다.

1. Office 365에 전역 관리자 자격 증명으로 로그인합니다.
2. 관리 센터로 이동합니다.
3. **활성 사용자** 로 이동하여 사용자를 선택합니다.
4. 세부 정보 창에서 **비즈니스용 OneDrive 설정** 을 확장하고 **파일 액세스** 를 선택합니다.
5. URL을 선택하여 사용자의 비즈니스용 OneDrive 계정으로 이동합니다.

### <a name="gaining-access-to-an-exchange-online-mailbox-to-make-changes-to-data"></a>데이터를 변경하기 위해 Exchange Online 사서함에 대한 액세스 권한 얻기

전역 관리자는 자신이 사서함 소유자인 것처럼 다른 사용자의 사서함에 있는 항목을 열고 편집(또는 삭제)하는 데 필요한 권한을 자신에게 할당할 수 있습니다. 특히, 전역 관리자는 Exchange Online의 모든 권한인 **읽기 및 관리** 권한을 추가해야 합니다. 자세한 내용은 다음을 참조하세요.

- [Office 365에서 다른 사용자에게 사서함 권한 제공](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user)
- [다른 사용자의 사서함 액세스](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081)

사용자 사서함이 법적 보존 상태이거나 보존 정책에 할당된 경우 보존 기간이 만료되거나 사서함에서 보존이 제거될 때까지 사서함의 모든 버전이 유지됩니다. 따라서 사서함 항목이 DSR 수정 요청에 응답하여 변경된 경우 원래 항목(변경 내용이 적용되기 전)의 복사본은 사용자 사서함의 복구 가능한 항목 폴더 내 숨겨진 폴더에 유지 및 저장됩니다.

### <a name="making-changes-to-content-in-onedrive-for-business-and-sharepoint-online"></a>비즈니스용 OneDrive 및 SharePoint Online의 콘텐츠 변경

관리자 또는 데이터 소유자는 SharePoint Online 문서, 목록 및 페이지를 변경할 수 있습니다. SharePoint 콘텐츠를 변경할 때 다음 사항에 유의해야 합니다.

- 문서를 업데이트하면 개정판이 포함된 새 버전의 문서가 저장됩니다. 이전 버전의 문서는 업데이트 되지 않습니다. 즉, DSR 수정 요청의 주체인 데이터가 이전 버전의 항목에서 유지될 수 있음을 의미합니다. 이전 버전의 항목을 삭제한 다음 Office 365에서 영구적으로 제거할 수 있습니다. 이 가이드의 [SharePoint Online 및 비즈니스용 OneDrive에서 문서 삭제 섹션](#deleting-documents-in-sharepoint-online-and-onedrive-for-business)을 참조하세요.
- 파일의 모든 버전 및 데이터 주체가 수행한 기록된 모든 활동을 포함하여 데이터 주체의 모든 추적을 파일에서 제거하는 방식으로 SharePoint 파일을 편집하려면 다음 단계를 수행해야 합니다.

    1. 파일의 복사본을 로컬 컴퓨터에 다운로드합니다.
    2. 파일을 삭제한 다음 1단계 및 2단계 휴지통에서 삭제하여 SharePoint Online에서 파일을 영구적으로 삭제합니다. 이 가이드의 [SharePoint Online 및 비즈니스용 OneDrive에서 문서 삭제](#deleting-documents-in-sharepoint-online-and-onedrive-for-business) 섹션을 참조하세요.
    3. 로컬 컴퓨터에서 문서의 복사본을 수정합니다.
    4. 수정된 파일을 원래 SharePoint Online 위치에 업로드합니다.

- SharePoint 목록의 데이터를 편집할 수 있습니다. [목록 항목 추가, 편집 또는 삭제](https://support.microsoft.com/office/add-edit-or-delete-list-items-a4b31f53-f044-470e-9823-4526594bacde)를 참조하세요.

또한 IT 관리자는 문서와 연관된 특정 개인 속성이 수정할 수 있습니다.

SharePoint 사용자 프로필 또는 Office 365의 사용자 정보는 해당 사용자를 나타내기 위해 비즈니스용 OneDrive 및 SharePoint Online 문서에 연결되는 경우가 종종 있습니다(예: 문서나 목록 항목의 만든 사람 또는 수정한 사람 열에 있는 사용자의 이름). 이 사용자 정보는 원본에 따라 여러 가지 방법으로 수정할 수 있습니다.

- 자신의 온-프레미스 Active Directory에서 사용자 속성을 수정합니다. 사용자 표시 이름, 이름 등 온-프레미스 AD의 사용자 속성과 동기화하는 고객의 경우 온-프레미스 AD에서 이러한 속성을 수정해야 합니다. 적절히 매핑된 속성은 Office 365로 이동한 다음 비즈니스용 OneDrive와 SharePoint Online으로 이동합니다.
- 관리 센터에서 사용자 속성을 수정합니다. 계정 정보에 대한 변경 내용이 비즈니스용 OneDrive 및 SharePoint Online 환경에 자동으로 반영 됩니다. 자세한 내용은 [Azure Active Directory에서 사용자에 대한 프로필 정보 추가 또는 변경](https://go.microsoft.com/fwlink/?linkid=864809)을 참조하세요. Office 365에서 제공되는 속성의 경우 SharePoint 측에서 변경할 수 없습니다.
- SharePoint 관리 센터의 SharePoint 사용자 프로필 환경에서 사용자 속성을 수정합니다. SharePoint 관리 센터의 사용자 프로필 탭에서 관리자는 **사용자 프로필 관리** 를 선택하고 사용자의 모든 속성을 조회할 수 있습니다.  그런 다음 사용자의 속성을 편집하도록 선택할 수 있습니다.
- 사용자 지정 원본에서 사용자 속성을 수정합니다. SharePoint 프로필 속성은 MIM(Microsoft Identity Manager) 또는 다른 방법을 통해 사용자 지정 원본에서 동기화될 수 있습니다.

문서에 텍스트로 유지되는 사용자의 이름과 같은 이전 정보를 유지할 수 있는 일부 환경은 영향을 받지 않습니다.

### <a name="making-changes-to-content-in-power-bi"></a>Power BI의 콘텐츠 변경

Power BI는 완전성과 정확성을 위해 대시보드 및 보고서에서 사용되는 기본 원본 데이터에 의존하므로 부정확하거나 불완전한 원본 데이터는 기본 원본 데이터에서 수정해야 합니다. 예를 들어 Dynamics 365 for Sales가 실시간 데이터 원본으로 연결된 Power BI 보고서를 만든 경우 Dynamics 365 for Sales에서 해당 데이터를 수정해야 합니다.

이러한 변경 내용이 적용된 후 [예약된 데이터 새로 고침](/power-bi/refresh-scheduled-refresh) 기능을 활용하여 수정된 데이터가 종속된 Power BI 자산에 반영되도록 Power BI에 저장된 데이터 집합을 업데이트할 수 있습니다. GDPR 요구 사항을 준수하려면 적절한 주기로 데이터를 새로 고치는 정책이 있어야 합니다.

### <a name="making-changes-to-content-in-yammer"></a>Yammer에서 콘텐츠 변경

메시지의 경우 사용자는 지정된 메시지를 편집하여 부정확성을 수정할 수 있습니다. Yammer 확인 관리자에게 자신의 모든 메시지 목록을 요청한 후 파일의 링크를 선택하여 각 메시지를 검토할 수 있습니다.

파일의 경우 사용자는 지정된 파일을 편집하여 부정확성을 수정할 수 있습니다. Yammer 확인 관리자에게 자신이 게시한 모든 파일 목록을 요청한 후 Yammer에서 파일에 액세스할 수 있습니다. 파일 폴더로 내보낸 파일은 번호로 파일을 검색하여 확인할 수 있습니다. 예를 들어 내보내기에 12345678.ppx라는 파일이 있는 경우 Yammer의 검색 상자를 사용하여 1235678.ppx를 검색합니다. 또는 <strong>https://www.yammer.com/\<network\_name\>/\#/files/\<file\_number\></strong>(예: <strong>https://www.yammer.com/contosomkt.onmicrosoft.com/\#/files/12345678</strong>)로 이동합니다.

사용자가 자신의 프로필 및 설정을 통해 액세스할 수 있는 데이터의 경우 사용자는 필요한 모든 항목을 변경할 수 있습니다.

- 사용자의 프로필:

    - Yammer ID가 있는 사용자는 자신의 프로필에 대한 모든 권한을 가집니다. 프로필을 보고 수정하는 방법은 [Yammer 프로필 및 설정 변경](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851)을 참조하세요.
    - 사용자에게 Office 365 ID가 있는 경우 Office 365에서 Yammer 사용자 프로필을 자동으로 가져오게 되므로 AAD (Azure Active Directory)에서 프로필 정보를 가져옵니다. Yammer 사용자는 Yammer에서 프로필을 일시적으로 변경할 수 있지만 AAD에 변경 사항이 있을 경우 이러한 변경 내용을 덮어쓰게 되므로 디렉터리 데이터를 보고 변경하는 가장 좋은 위치는 AAD입니다. 사용자가 AAD를 업데이트 하도록 요청해야 합니다. [Office 365의 수명 주기 동안 Yammer 사용자 관리](/yammer/manage-yammer-users/manage-users-across-their-lifecycle)와 [Azure Active Directory에서 사용자의 프로필 정보를 추가하거나 변경](/azure/active-directory/active-directory-users-profile-azure-portal)을 참조합니다.

- 사용자의 설정:

    - 사용자는 자신의 설정을 변경할 수 있습니다. 사용자 설정을 보고 수정하는 방법에 대한 자세한 내용은 [Yammer 프로필 및 설정 변경](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851)을 참조하세요.
    - 사용자의 그룹 구성원 자격, 책갈피로 지정된 메시지, 팔로우한 사용자 및 팔로우한 항목. 사용자는 이 정보를 변경할 수 있습니다. [Yammer에서 구성된 상태로 유지하기 위한 팁](https://support.office.com/article/tips-for-staying-organized-in-yammer-40ae9666-75c0-4254-a84c-d87a9542f380)을 참조하세요.

## <a name="responding-to-dsr-restriction-requests"></a>DSR 제한 요청에 응답

다음은 Office 365에서 데이터 처리를 제한하는 방법입니다.

- Office 365 응용 프로그램 라이선스를 제거하여 사용자가 응용 프로그램을 통해 데이터에 액세스하지 못하도록 합니다.
- 사용자가 비즈니스용 OneDrive 계정에 액세스하지 못하도록 합니다.
- 데이터 처리에서 Office 365 서비스를 해제합니다.
- SharePoint Online 및 비즈니스용 OneDrive에서 일시적으로 데이터를 제거하고 온-프레미스에서 유지합니다.
- SharePoint Online 사이트에 대한 모든 액세스를 일시적으로 제한합니다.
- 사용자가 Office 365에 로그인하지 못하도록 합니다.

나중에 조직에서 제한을 더 이상 적용하지 않기로 결정한 경우 라이선스를 다시 할당하거나, 서비스를 다시 설정하거나, 사용자가 Office 365에 로그인하도록 허용하는 등 제한하기 위해 수행한 단계를 역순으로 수행하여 제한을 종료할 수 있습니다.

### <a name="removing-the-license-for-an-office-365-application"></a>Office 365 응용 프로그램에 대한 라이선스 제거

앞서 설명한 것처럼 조직의 비즈니스용 Microsoft 365 구독에 포함된 모든 Office 365 응용 프로그램에 대한 라이선스는 기본적으로 모든 사용자에게 할당됩니다. IT 관리자는 DSR이 적용되는 데이터에 대한 액세스를 제한해야 할 필요가 있는 경우 Office 365 관리 포털을 사용하여 응용 프로그램에 대한 사용자 라이선스를 일시적으로 해제할 수 있습니다. 사용자가 해당 응용 프로그램을 사용하려고 하면 사용 허가되지 않은 제품 알림이나 해당 사용자에게 더 이상 액세스 권한이 없다는 메시지가 나타납니다. 자세한 내용은 [비즈니스용 Office 365 사용자로부터 라이선스 제거](/microsoft-365/admin/add-users/delete-a-user)를 참조하세요.

**참고:**

- 사용자가 Yammer에 액세스하는 것을 제한하려면 먼저 [Yammer 사용자에 대해 Office 365 ID를 적용](/yammer/configure-your-yammer-network/enforce-office-365-identity)한 다음 사용자의 Yammer 라이선스를 제거해야 합니다.

- Power BI Embedded를 활용하는 시나리오의 경우 콘텐츠가 포함된 ISV(Independent Software Vendor) 응용 프로그램에 대한 액세스를 제한할 수 있습니다.

### <a name="preventing-users-from-accessing-their-onedrive-for-business-account"></a>사용자가 비즈니스용 OneDrive 계정에 액세스하지 못하도록 방지

사용자의 SharePoint Online 라이선스를 제거해도 해당 사용자의 비즈니스용 OneDrive 계정이 존재하면 이에 액세스할 수 있습니다. 비즈니스용 OneDrive 계정에 대한 사용자 권한을 제거해야 합니다. 비즈니스용 OneDrive 계정의 사이트 모음 소유자로 사용자를 제거하여 이 작업을 수행할 수 있습니다. 특히 사용자 프로필의 기본 사이트 모음 관리자 및 사이트 모음 관리자 그룹에서 사용자를 제거해야 합니다. [SharePoint 관리 센터의 사용자 프로필 관리](/sharepoint/manage-user-profiles)에서 "비즈니스용 OneDrive 계정에서 관리자 추가 및 제거" 섹션을 참조하세요.

### <a name="turning-off-an-office-365-service"></a>Office 365 서비스 해제

데이터 처리 제한에 대한 DSR 요청을 해결하는 또 다른 방법은 Office 365 서비스를 해제하는 것입니다. 이는 전체 조직의 모든 사용자에게 영향을 주며 모든 사람이 서비스를 사용하거나 서비스의 데이터에 액세스하는 것을 방지합니다.

서비스를 해제하는 가장 빠른 방법은 Office 365 PowerShell을 사용하여 조직의 모든 사용자로부터 해당 사용자 라이선스를 제거하는 것입니다. 이는 모든 사람이 해당 서비스의 데이터에 액세스하는 것을 제한합니다. 자세한 지침은 [Office 365 PowerShell을 사용하여 서비스에 대한 액세스를 사용하지 않도록 설정](/microsoft-365/enterprise/disable-access-to-services-with-microsoft-365-powershell)을 참조하고 절차에 따라 단일 라이선스 계획에서 사용자에 대해 Office 365 서비스를 사용하지 않도록 설정하세요.

> [!NOTE]
> Yammer의 경우 사용자 계정에서 Yammer 라이선스를 제거하는 것 외에 Yammer 자격 증명을 사용하여 Yammer에 로그인하는 기능도 사용하지 않도록 설정해야 합니다(로그인할 때 Office 365 자격 증명을 사용하도록 적용). 자세한 지침은 [Microsoft 365 사용자에 대한 Yammer 액세스 해제하기](https://support.office.com/article/Turn-off-Yammer-access-for-Office-365-users-1f79bfad-f713-4143-aa5d-5584985ce53a)를 참조하세요.

### <a name="temporarily-removing-data-from-sharepoint-online-or-onedrive-for-business-sites"></a>SharePoint Online 또는 비즈니스용 OneDrive 사이트에서 일시적으로 데이터 제거

개인 데이터 처리를 제한하는 또 다른 방법은 DSR에 응답하여 Office 365에서 개인 데이터를 일시적으로 제거하는 것입니다. 조직에서 제한을 더 이상 적용하지 않기로 결정한 경우 Office 365로 데이터를 다시 가져올 수 있습니다.

대부분의 Office 문서는 SharePoint Online 또는 비즈니스용 OneDrive 사이트에 있는 때문에 사이트에서 문서를 제거한 다음, 다시 가져오는 개략적인 프로세스는 다음과 같습니다.

1. 제한 요청의 주체인 문서의 복사본을 가져옵니다. 사이트에 대한 액세스를 요청하거나 전역 관리자 또는 사이트 모음 관리자에게 문서의 복사본을 제공하도록 요청해야 할 수도 있습니다.
2. 온-프레미스 위치(예: 파일 서버 또는 파일 공유) 또는 Microsoft 클라우드의 Office 365 테넌트가 아닌 다른 위치에 문서를 저장합니다.
3. Office 365에서 원본 문서를 영구적으로 삭제(제거)합니다. 이는 다음 세 단계 프로세스입니다.

   1.  문서의 원래 복사본을 삭제합니다. 사이트에서 문서를 삭제하면 사이트의 휴지통(*1단계 휴지통* 이라고도 함)으로 문서가 전송됩니다.

   1.  사이트 휴지통으로 이동하여 문서의 해당 복사본을 삭제합니다. 사이트 휴지통에서 문서를 삭제하면 사이트 모음 휴지통(*2단계 휴지통* 이라고도 함)으로 문서가 전송됩니다. [SharePoint 문서 라이브러리에서 파일, 폴더 또는 링크 삭제](https://support.microsoft.com/office/delete-a-file-folder-or-link-from-a-sharepoint-document-library-71f3c90a-0d24-4d80-8b66-f88234b79a52)를 참조하세요.

   1.  사이트 모음 휴지통으로 이동하여 문서의 해당 복사본을 삭제하면 Office 365에서 영구적으로 제거됩니다. [사이트 모음 휴지통에서 항목 삭제](https://support.microsoft.com/office/delete-items-from-the-site-collection-recycle-bin-dd5c00c2-aef6-4458-9d04-80b185077653)를 참조하세요.

4. 제한이 더 이상 적용되지 않는 경우 온-프레미스에 저장된 문서의 복사본을 Office 365의 사이트에 다시 업로드할 수 있습니다.

> [!IMPORTANT]
> 이전 절차는 문서가 보류(Microsoft Office 365의 보존 또는 법적 보류 기능 중 하나) 중인 사이트에 있는 경우에는 적용되지 않습니다. DSR 제한 요청이 법적 보존에 우선하는 경우 문서를 영구적으로 삭제하려면 먼저 사이트에서 보존을 제거해야 합니다. 이 경우 삭제된 문서의 문서 기록도 영구적으로 제거됩니다.

### <a name="temporarily-restricting-access-to-sharepoint-online-sites"></a>일시적으로 SharePoint Online 사이트에 대한 액세스 제한

SharePoint Online 관리자는 일시적으로 SharePoint Online PowerShell의 **Set-SPOSite -LockState** 명령을 사용하여 사이트 모음을 잠가서 모든 사용자가 SharePoint Online 사이트 모음에 액세스하지 못하게 할 수 있습니다. 이렇게 하면 사용자가 사이트 모음 및 사이트에 있는 콘텐츠나 데이터에 액세스할 수 없습니다. 그런 다음 사용자가 사이트에 액세스할 수 있어야 한다고 결정하면 관리자는 사이트의 잠금을 해제할 수 있습니다. 이 PowerShell cmdlet 실행에 대한 자세한 내용은 [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite)를 참조하세요.

### <a name="preventing-a-user-from-signing-in-to-office-365"></a>사용자가 Office 365에 로그인하지 못하도록 방지

IT 관리자는 사용자가 Office 365 로그인하지 못하도록 할 수도 있습니다. 이렇게 하면 사용자가 Office 365 온라인 서비스에 액세스하지 못하거나 Office 365에 저장된 데이터를 처리하지 못하게 됩니다. [퇴사한 직원의 Office 365 데이터 액세스 차단](/microsoft-365/admin/add-users/remove-former-employee)을 참조하세요.

## <a name="part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365"></a>2부: Office 365에서 생성된 정보에 관한 DSR에 응답

Microsoft의 Office 365 서비스 제품군에는 사용자와 조직에 정보를 제공하는 온라인 서비스가 포함되어 있습니다.

- Delve 및 MyAnalytics는 개별 사용자에게 정보 제공
- Workplace Analytics는 조직에 정보 제공

다음 섹션에서는 이러한 서비스에 대해 설명합니다.

### <a name="delve"></a>Delve

Delve에서는 사용자가 Office 365 프로필을 관리하고 관련된 사람과 문서를 검색할 수 있습니다. 사용자는 액세스 권한이 있는 문서만 볼 수 있습니다. Delve에 대한 유용한 문서의 시리즈에 대한 자세한 내용은 [Office Delve](https://support.office.com/article/What-is-Office-Delve-1315665a-c6af-4409-a28d-49f8916878ca)를 참조하세요.

#### <a name="access-and-export"></a>액세스 및 내보내기

관리자는 사용자의 Delve 데이터에 액세스하거나 내보낼 수 없습니다. 즉, 사용자가 직접 Delve 데이터에 액세스하고 내보내야 합니다. 대부분의 데이터 형식은 Delve에서 직접 액세스하고 내보낼 수 있지만 일부 데이터 형식은 다른 서비스를 통해서만 사용할 수 있습니다.

##### <a name="data-available-in-the-delve-user-interface"></a>Delve 사용자 인터페이스에서 사용할 수 있는 데이터

- **프로필 데이터:** 사용자가 자신에 대해 추가하도록 선택한 정보(선택 사항)와 Azure Active Directory에 있는 조직의 전체 주소 목록의 프로필 정보입니다. Delve에서 프로필 데이터에 액세스하거나 데이터를 내보내려면 **나** \> **프로필 업데이트** 를 선택합니다. 페이지에서 직접 콘텐츠를 복사하거나 
- **블로그 데이터:** 사용자가 게시한 블로그 게시물입니다. 사용자는 **나** \> **모든 게시물** 을 선택하여 블로그 데이터에 액세스하거나 데이터를 내보낼 수 있습니다. 페이지에서 직접 콘텐츠를 복사하거나 스크린샷을 찍을 수 있습니다.
- **최근 사용자 데이터:** 일정 시기에 가장 관련이 높은 조직 내 사용자를 Delve가 유추한 정보입니다. 사용자가 “사용자를 선택하여 각자 진행 중인 작업 보기” 창에서 **나** \> **모두 보기** 를 선택하면 일정 시기에 가장 관련이 높은 사용자가 Delve에 표시됩니다.

##### <a name="data-available-through-an-export-link-in-delve"></a>Delve에서 내보내기 링크를 통해 사용할 수 있는 데이터

- **사용자 목록 데이터:** 사용자가 Delve에서 본 사람입니다. **사용자** 목록은 홈 페이지의 왼쪽 창에 표시됩니다. 사용자는 Delve에서 가장 최근에 본 사람의 목록을 내보낼 수 있습니다.
- **즐겨찾기 데이터:** 사용자가 즐겨찾기로 표시한 보드 및 문서입니다. **즐겨찾기** 페이지에는 사용자가 자신의 즐겨찾기에 추가한 보드 및 문서가 표시됩니다. 사용자는 현재 즐겨 찾는 보드 및 문서 목록을 내보낼 수 있습니다.
- **기능 설정 데이터:** 사용자가 Delve를 사용한 결과로 발생하는 Delve 구성 또는 작업입니다. 사용자는 이러한 설정의 전체 목록을 내보낼 수 있습니다.

위 데이터를 액세스 하거나 내보내려면 사용자가 Delve 오른쪽 위 모서리에 있는 기어 아이콘을 선택하고 **기능 설정** > **데이터 내보내기** 를 선택해야 합니다. 정보는 JSON 형식으로 내보내집니다.

##### <a name="data-thats-available-through-other-services"></a>다른 서비스를 통해 사용할 수 있는 데이터

- **인기 문서 데이터:** 사용자와 연관이 있을 수 있는 문서와 전자 메일 첨부 파일입니다. Delve는 사용자의 활동과 Office 365에서 함께 작업하는 사람들을 기준으로 이 문서와 전자 메일 메시지를 자동으로 정리합니다. 사용자가 Delve를 열거나 **홈** 을 선택하면 일정 시간에 사용자에게 가장 관련이 있는 문서 또는 첨부 파일이 Delve에 표시됩니다. 사용자는 실제 문서 및 첨부 파일에 액세스하거나 내보내기 위해 문서 또는 첨부 파일을 사용할 수 있는 플랫폼(예: Office.com, SharePoint Online, 비즈니스용 OneDrive 또는 Exchange Online)을 통해 Office 365 서비스로 이동할 수 있습니다.
- **최근 문서 및 전자 메일 첨부 파일 데이터:** 사용자가 수정한 최근 문서 및 전자 메일 첨부 파일입니다. “최근 문서 및 전자 메일 첨부 파일로 돌아가기” 창에서 사용자가 **나** \> **모두 보기** 를 선택하면 일정 시기에 사용자가 수정한 최근 문서와 전자 메일 첨부 파일이 Delve에 표시됩니다. 사용자는 실제 문서 및 첨부 파일에 액세스하거나 내보내기 위해 문서 또는 첨부 파일을 사용할 수 있는 플랫폼(예: Office.com, SharePoint Online, 비즈니스용 OneDrive 또는 Exchange Online)을 통해 Office 365 서비스로 이동할 수 있습니다.
- **주변 사용자의 문서 데이터:** Delve가 일정 시기에 사용자와 가장 관련이 높은 것으로 추정한 문서입니다. 사용자가 “주변 사용자의 문서 검색” 창에서 **나** \> **모두 보기** 를 선택하면 일정 시기에 사용자와 가장 관련이 높은 문서가 Delve에 표시됩니다. 사용자는 실제 문서에 액세스하거나 내보내기 위해 문서 또는 첨부 파일을 사용할 수 있는 플랫폼(예: Office.com, SharePoint Online, 비즈니스용 OneDrive 또는 Exchange Online)을 통해 Office 365 서비스로 이동할 수 있습니다.

#### <a name="rectify"></a>수정

사용자는 Delve에서 다음 정보를 수정할 수 있습니다.

- **프로필 정보:** 사용자는 **나** \> **프로필 업데이트** 를 선택하여 자신의 정보를 업데이트할 수 있습니다. 전체 주소 목록에서 조직의 설정에 따라 사용자는 이름 또는 직함과 같은 일부 프로필 정보를 수정하지 못할 수도 있습니다.
- **기능 설정:** 사용자는 Delve의 오른쪽 위에 있는 기어 아이콘을 선택한 다음 **기능 설정** \>을 선택하여 원하는 설정을 변경할 수 있습니다.

#### <a name="restrict"></a>제한

Delve에서 조직에 대한 처리를 제한하기 위해 Office Graph를 해제할 수 있습니다. 자세한 내용은 [여기](/sharepoint/delve-for-office-365-admins)를 참조하세요.

#### <a name="delete"></a>삭제

사용자는 Delve에서 다음 정보를 삭제할 수 있습니다.

- **프로필 정보:** 프로필 정보를 삭제하려면 사용자는 **나** \> **프로필 업데이트** 를 선택하고 자유 형식 텍스트를 삭제하면 됩니다. 전체 주소 목록에서 조직의 설정에 따라 사용자는 이름 또는 직함과 같은 일부 프로필 정보를 삭제하지 못할 수도 있습니다.
- **문서 및 전자 메일 첨부 파일:** 문서 또는 첨부 파일을 삭제하려면 사용자는 해당 문서 또는 첨부 파일이 저장된 서비스(예: SharePoint Online, 비즈니스용 OneDrive 또는 Exchange Online)로 이동하여 문서를 삭제해야 합니다.

### <a name="myanalytics"></a>MyAnalytics

MyAnalytics는 사용자에게 회사에서 시간을 어떻게 보냈는지 이해하는 데 도움이 되는 통계를 제공합니다. 사용자가 자신의 개인 대시보드에 표시되는 데이터 및 이러한 데이터의 계산 방식을 보다 잘 이해하도록 도와주려면 [MyAnalytics 개인 대시보드](/workplace-analytics/myanalytics/use/dashboard-2) 로 안내하세요.

#### <a name="access-and-export"></a>액세스 및 내보내기

조직에서 MyAnalytics를 사용하는 경우 Microsoft는 모든 사용자에 대한 인사이트를 제공합니다. 모든 MyAnalytics 인사이트는 사용자 사서함의 전자 메일 및 모임 머리글에서 가져옵니다. 사용자는 자신의 Office 365 계정에 로그인 한 상태에서 [MyAnalytics 대시 보드](https://delve.office.com)로 이동하여 직장에서 시간을 보내는 방법에 대한 인사이트를 볼 수 있습니다. 사용자가 자신의 정보에 대한 영구적인 복사본을 갖고 싶어하는 경우 MyAnalytics 인사이트를 스크린샷할 수 있습니다.

#### <a name="rectify"></a>수정

MyAnalytics에서 생성되는 모든 정보는 사용자의 메일 및 일정 항목에서 파생됩니다. 따라서 원본 전자 메일 또는 일정 항목 외에는 어떤 항목도 수정할 수 없습니다.

#### <a name="restrict"></a>제한

특정 사용자에 대한 처리를 제한하려면 이들을 MyAnalytics에서 옵트아웃하면 됩니다. 방법은 [MyAnalytics 사용자 설정 구성](/workplace-analytics/myanalytics/setup/configure-myanalytics)을 참조하세요.

#### <a name="delete"></a>삭제

MyAnalytics 데이터를 포함하는 모든 사서함 콘텐츠는 Active Directory에서 사용자 계정이 "영구 삭제"되면 제거됩니다. 자세한 내용은 이 가이드의 [사용자 삭제](#deleting-a-user) 섹션을 참조하세요.

### <a name="workplace-analytics"></a>Workplace Analytics

조직에서는 Workplace Analytics를 통해 자체 비즈니스 데이터로 Office 365 데이터를 보강하여 조직의 생산성, 공동 작업 패턴 및 직원 참여도에 대한 정보를 얻을 수 있습니다. [이 문서](/workplace-analytics/index-orig)에서는 Workplace Analytics에서 처리하는 데이터 및 이러한 데이터에 액세스할 수 있는 사람에 대한 조직의 제어 기능을 설명합니다.

Workplace Analytics에서 DSR을 지원하려면 

1. 조직에서 Workplace Analytics를 사용하고 있는지 확인합니다. 자세한 내용은 [비즈니스용 Office 365에서 사용자에게 라이선스 할당](/microsoft-365/admin/manage/assign-licenses-to-users)을 참조하세요. 조직에서 Workplace Analytics를 사용하고 있지 않으면 추가 작업이 필요하지 않습니다.

2. 조직에서 Workplace Analytics를 사용하는 경우 조직에서 Workplace Analytics 관리자 역할이 할당된 사람을 확인합니다. 또한 데이터 주체의 사서함이 Workplace Analytics에 대한 라이선스가 있는지 확인합니다. 필요한 경우 다음 DSR 요청을 처리할 때 Workplace Analytics 관리자에게 Microsoft 지원 서비스에 문의하라고 합니다. 

#### <a name="access-and-export"></a>액세스 및 내보내기

사용자가 만든 Workplace Analytics 인사이트 보고서에는 조직이 Office 365 데이터를 보완하는 데 사용한 정보에 따라 Workplace Analytics에 대한 라이선스가 있는 사용자의 개인 데이터가 포함되어 있을 수도 있고 그렇지 않을 수도 있습니다. Workplace Analytics 관리자는 이러한 보고서를 검토하여 사용자의 개인 데이터가 포함되어 있는지 확인해야 합니다. 보고서에 사용자의 개인 데이터가 포함된 경우 이 보고서의 복사본을 해당 사용자에게 제공할지 결정해야 합니다. Workplace Analytics에서 보고서를 내보낼 수 있습니다. 

#### <a name="rectify"></a>수정

위에서 설명한 것처럼 Workplace Analytics에서는 관심 있는 보고서를 생성하기 위해 제공한 조직의 데이터와 Office 365 데이터를 사용합니다. Office 365 데이터는 사용자의 전자 메일 및 일정 활동을 기반으로 하므로 수정할 수 없습니다. 그러나 보고서를 생성하기 위해 Workplace Analytics에 업로드한 조직의 데이터는 수정할 수 있습니다. 이렇게 하려면 원본 데이터를 수정하여 업로드한 후 보고서를 다시 실행하여 새 Workplace Analytics 보고서를 생성해야 합니다.

#### <a name="restrict"></a>제한

특정 사용자에 대한 처리를 제한하기 위해 해당 Workplace Analytics 라이선스를 제거할 수 있습니다.

#### <a name="delete"></a>삭제

Workplace Analytics 보고서 또는 보고서 집합에서 데이터 주체를 제거하려는 경우 해당 보고서를 삭제할 수 잇습니다. 보고서를 생성하는 데 사용한 조직 데이터에서 사용자를 삭제하고 해당 데이터를 다시 업로드하는 것은 사용자의 책임입니다. Azure Active Directory에서 사용자 계정이 "영구 삭제"되면 사용자에 대한 모든 데이터도 제거됩니다. 

데이터 주체의 개인 데이터를 제거하려면 전역 관리자는 다음 단계를 수행할 수 있습니다. 

1. 데이터 주체에서 Workplace Analytics 라이선스를 제거합니다.
2. 데이터 주체에 대한 Azure Active Directory(AAD) 항목을 삭제합니다. (자세한 내용은 [사용자 삭제](/azure/active-directory/fundamentals/add-users-azure-active-directory#delete-a-user)를 참조하세요.)
3. 고객 지원에 문의하여 데이터 주체 권한(DSR) 사용자 삭제 요청 티켓을 엽니다. 이 티켓의 사용자 보안 주체 이름(UPN)을 사용하여 데이터 주체를 식별합니다.
4. 회사의 HR 시스템의 HR 데이터 사본을 내보내고([데이터 내보내기 ](/workplace-analytics/setup/prepare-organizational-data) 참조) 해당 HR 데이터 파일에서 데이터 주체 정보를 제거한 다음, 편집된 HR 데이터 파일을 .csv 형식으로 Workplace Analytics에 업로드합니다.([조직 데이터 업로드](/workplace-analytics/setup/upload-organizational-data) 참조)

## <a name="part-3-responding-to-dsrs-for-system-generated-logs"></a>3부: 시스템 생성 로그에 대한 DSR에 응답

또한 Microsoft는 GDPR의 광범위한 “개인 데이터” 정의에 따라 개인적인 것으로 인식될 수 있는 시스템 생성 로그를 액세스, 내보내기 및 삭제하는 기능을 사용자에게 제공합니다. GDPR에 따라 개인적인 것으로 인식될 수 있는 시스템 생성 로그의 예는 다음과 같습니다.

- 사용자 활동 로그와 같은 제품 및 서비스 사용 데이터
- 사용자 검색 요청 및 쿼리 데이터
- 시스템 기능 및 사용자나 기타 시스템의 상호 작용의 산물로서 제품 및 서비스에서 생성된 데이터

시스템 생성 로그의 데이터를 제한하거나 수정하는 기능은 지원되지 않습니다. 시스템 생성 로그 데이터는 Microsoft 클라우드 및 진단 데이터 내에서 수행되는 실제 작업으로 구성되며 이러한 데이터를 수정하면 작업의 기록 데이터가 손상되어 사기 및 보안 위험이 높아질 수 있습니다.

### <a name="accessing-and-exporting-system-generated-logs"></a>시스템 생성 로그 액세스 및 내보내기

테넌트 관리자는 Office 365 서비스 및 응용 프로그램의 특정 사용자의 사용과 관련된 시스템 생성 로그에 액세스할 수 있는 조직 내의 유일한 사람입니다. 내보내기 요청에 대한 검색된 데이터는 컴퓨터가 읽을 수 있는 형식으로 제공되며, 데이터가 어떤 서비스에 연결되어 있는지 알 수 있도록 하는 파일로 제공됩니다. 위에서 설명한 것처럼 검색된 데이터에 서비스의 보안 또는 안정성을 침해할 수 있는 데이터는 포함되지 않습니다.

시스템 생성 로그에 액세스하여 내보내려면 다음을 수행합니다.

1. Azure 포털에 로그인하고 **모든 서비스** 를 선택합니다.
2. 필터에 정책을 입력한 다음 **정책** 을 선택합니다.
3. **정책** 블레이드에서 **사용자 개인 정보** 를 선택하고 **사용자 요청 관리** 를 선택한 후 **내보내기 요청 추가** 를 선택합니다.
4. 다음과 같이 **데이터 내보내기 요청** 을 완료합니다.

    - **사용자**. 내보내기를 요청한 Azure Active Directory 사용자의 전자 메일 주소를 입력합니다.
    - **구독**. 리소스 사용량을 보고하고 서비스 요청을 청구하는 데 사용하는 계정을 선택합니다. Azure Storage 계정의 위치이기도 합니다.
    - **저장소 계정**. Azure Storage(BLOB)의 위치를 선택합니다. 자세한 내용은 Microsoft Azure Storage 소개 - BLOB 저장소 게시물을 참조하세요.
    - **컨테이너**. 사용자가 내보낸 개인 정보 데이터의 저장소 위치로 새 컨테이너를 만들거나 기존 컨테이너를 선택합니다.

5. **만들기** 를 선택합니다.

내보내기 요청이 **보류 중** 상태가 됩니다. **사용자 개인 정보** > **개요 블레이드** 에서 보고서 상태를 볼 수 있습니다.

> [!IMPORTANT]
> 개인 데이터는 여러 시스템에서 가져올 수 있으므로 내보내기 프로세스를 완료하는 데 최대 1개월이 소요될 수 있습니다.

### <a name="notify-about-exporting-or-deleting-issues"></a>내보내기 또는 삭제 중 발생하는 문제에 대한 알림

Azure Portal에서 데이터를 내보내거나 삭제하는 동안 문제가 발생하면 Azure Portal **도움말 + 지원** 블레이드로 이동하여 **구독 관리** > **구독에 대한 개인 정보 보호 및 준수 요청** > **개인 정보 보호 블레이드 및 GDPR 요청** 에서 새 티켓을 제출합니다.

> [!NOTE]
> Azure Portal의 데이터를 내보내면 몇 가지 애플리케이션에 대한 시스템 생성 데이터가 내보내지지 않습니다. 이러한 애플리케이션에 대한 데이터를 내보내려면 [시스템 생성 로그 데이터를 내보내기 위한 추가 단계](/microsoft-365/compliance/gdpr-system-generated-log-data)를 참조하세요.

아래에 시스템 생성 로그를 액세스하고 내보내는 방법을 요약해서 설명합니다.

- **Azure Portal을 사용하는 내보내기 요청이 요청을 완료하는 데 얼마나 걸리나요?**: 여러 요인에 따라 달라질 수 있습니다. 통상적으로 1~2일 후에 완료해야 하지만 최대 30일이 걸릴 수 있습니다.
- **출력 형식:** 컴퓨터에서 읽을 수 있는 구조화된 파일(예: XML, CSV 또는 JSON)로 출력됩니다.
- **Azure 포털에 액세스하여 시스템 생성 데이터에 대한 액세스 요청을 제출할 수 있는 사용자:** Office 365 전역 관리자는 Azure 포털에 액세스할 수 있습니다.
- **내보내기 결과에 반환된 데이터**: 결과에 Microsoft에서 저장하는 시스템 생성 로그가 포함되어 있습니다. 내보낸 데이터는 Office 365, Azure 및 Dynamics를 포함하여 다양한 Microsoft 서비스에 걸쳐져 있습니다. 결과에는 서비스의 보안 또는 안정성을 손상시킬 수 있는 데이터가 포함되지 않습니다.
- **사용자에게 데이터를 반환하는 방식:** 데이터는 조직의 Azure 저장소 위치로 내보내집니다. 이 데이터를 사용자에게 표시/반환하는 방식은 조직의 관리자가 결정합니다.
- **시스템 생성 로그 데이터 형태:** 다음은 데이터를 JSON 형식으로 표시한 예제입니다.

    ```JSON
    [{
    "DateTime": "2017-04-28T12:09:29-07:00",
    "AppName": "SharePoint",
    "Action": "OpenFile",
    "IP": "154.192.13.131",
    "DevicePlatform": "Windows 1.0.1607"
    }]
    ```

보안 및 준수 센터의 Office 365 감사 로그를 검색하여 Exchange Online, SharePoint Online, 비즈니스용 Skype, Yammer, Office 365 그룹 등 Microsoft의 가장 자주 사용되는 일부 서비스에 대한 제품 서비스 사용 현황 데이터를 검색할 수도 있습니다. 자세한 내용은 부록 A에서 DSR 조사에서 [Office 365 감사 로그 검색 도구 사용](#use-the-audit-log-search-tool-in-dsr-investigations)을 참조하세요. 조직의 다른 사용자(예: 준수 관리자)에게 감사 로그를 검색하여 이 데이터에 액세스할 수 있는 권한을 할당할 수 있으므로 감사 로그 사용은 여러분과 관련이 있을 수 있습니다.

### <a name="deleting-system-generated-logs"></a>시스템 생성 로그 삭제

액세스 요청을 통해 검색된 시스템 생성 로그를 삭제하려면 서비스에서 사용자를 제거하고 해당 Azure Active Directory 계정을 영구적으로 삭제해야 합니다. 사용자를 영구적으로 삭제하는 방법에 대한 지침은 이 가이드에서 [사용자 삭제](#deleting-a-user)를 참조하세요. 사용자 계정을 영구적으로 삭제하는 작업을 일단 시작하면 되돌릴 수 없습니다.

영구적으로 사용자 계정을 삭제하면, 서비스의 보안이나 안정성을 손상시킬 수 있는 데이터를 제외하고, 30일 이내에 거의 모든 Office 365 서비스의 시스템 생성 로그에서 사용자의 데이터가 제거됩니다. 

이 30일 기간의 예외 중 하나는 Exchange Online에서 사용자 계정을 영구적으로 삭제하는 데 30일 이상 걸린다는 것입니다. 이는 Exchange Online 콘텐츠의 중요성과 우발적인 데이터 손실을 방지하기 위한 것입니다. Exchange Online은 사용자 계정이 영구적으로 삭제된 후 최대 60일 동안 의도적으로 데이터를 보류 상태로 두도록 설계되었습니다. 사용자의 Exchange Online 데이터를 30일 내에 영구적으로 삭제하려면 Azure Active Directory에서 사용자 계정을 영구적으로 삭제한 다음 [Microsoft 지원](https://support.microsoft.com/) 서비스에 문의하여 예약된 삭제 프로세스 외에 해당 사용자의 Exchange Online 데이터를 수동으로 제거해 달라고 요청합니다. 자세한 내용은 이 가이드의 앞부분에 설명된 [Exchange Online 데이터 제거](#removing-exchange-online-data)를 참조하세요.

사용자 계정을 삭제해도 Yammer 및 Kaizala에 대한 시스템 생성 로그는 제거되지 않습니다. 이러한 응용 프로그램에서 데이터를 제거하려면 다음 중 하나를 참조합니다.

- Yammer - [Yammer Enterprise에서 GDPR 데이터 주체 요청 관리](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- Kaizala - [Kaizala에서 사용자의 조직 데이터 내보내기 또는 삭제](/office365/kaizala/export-or-delete-a-user-s-data)

#### <a name="national-clouds"></a>국가별 클라우드

전역 IT 관리자는 다음과 같은 국가별 클라우드에서 시스템 생성 로그를 내보내려면 다음을 수행해야 합니다.

- **Office 365 Germany**: 위 단계를 따릅니다.
- **Office 365 미국 정부**: [Office 365 관리 포털로 이동한 후](https://portal.office365.us) Microsoft 지원 서비스에 요청을 제출합니다.
- **21Vianet에서 운영하는 Office 365(중국)**: [21Vianet에서 운영하는 Office 365 관리 포털로 이동](https://portal.partner.microsoftonline.cn/AdminPortal/Home#/homepage)한 후 **상거래** > **구독** > **개인 정보** > **GDPR** 로 가서 필수 정보를 입력합니다.

## <a name="part-4-additional-resources-to-assist-you-with-dsrs"></a>4부: DSR을 지원하는 추가 리소스

### <a name="dsr-guides-for-other-microsoft-enterprise-services"></a>다른 Microsoft 엔터프라이즈 서비스에 대한 DSR 가이드

이 가이드는 Office 365 제품, 서비스 및 관리 도구를 사용할 때 DSR에 응답하기 위해 개인 데이터를 찾고 작업하는 방법 항목에만 적용됩니다. 다른 Microsoft 엔터프라이즈 서비스에 대한 유사한 가이드에 액세스하려면 [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/)로 이동하세요.

### <a name="microsoft-support"></a>Microsoft 지원 서비스

"지원 데이터"는 여러분의 조직 또는 사용자가 Office 365 또는 다른 Microsoft 제품 및 서비스와 관련된 제품 지원(예: 예기치 않은 제품 문제 해결)을 받기 위해 Microsoft에 참여하는 경우 여러분과 여러분의 사용자가 Microsoft에 제공하는 데이터입니다. 이 데이터의 일부에는 개인 데이터가 포함될 수 있습니다. 자세한 내용은 [GDPR에 대한 Microsoft 지원 서비스 및 전문 서비스 데이터 주체 요청](/microsoft-365/compliance/gdpr-dsr-prof-services)을 참조하세요.

### <a name="product-and-services-authenticated-with-an-org-id-for-which-microsoft-is-a-data-controller"></a>Microsoft가 데이터 통제자인 조직 ID로 인증된 제품 및 서비스

이 가이드의 1–3부에서는 Microsoft가 조직의 데이터 처리자이므로 DSR 기능이 테넌트 관리자에게 제공되는 제품 및 서비스를 다룹니다. 조직의 사용자가 회사 또는 학교 계정("Azure Active Directory ID" 또는 "AAD"라고도 함)을 사용하여 Microsoft가 데이터 통제자인 Microsoft 제품 및 서비스에 로그인할 수 있는 다양한 경우가 있습니다. 이 모든 제품 및 서비스에 대해 사용자는 자신의 데이터 주체 요청을 Microsoft에 직접 시작해야 하며, Microsoft는 사용자에게 직접 요청을 이행합니다. 사용자가 만든 콘텐츠의 저장소를 포함하여 제품 및 서비스는 사용자가 자신이 만든 콘텐츠를 제품의 고유 기능 중 일부로 액세스하고, 내보내고, 수정하고, 삭제할 수 있도록 지원합니다. 이러한 기능이 적용될 수 있는 시나리오는 다음과 같습니다.

- **선택적 연결된 온라인 서비스:** 엔터프라이즈용 Microsoft 365 앱은 사용자가 특정 온라인 서비스(선택 사항)를 사용할 수 있도록 합니다. 이러한 서비스 및 관련된 사용자 컨트롤 목록이 [여기](https://support.office.com/article/microsoft-s-other-connected-services-92c234f1-dc91-4dc1-925d-6c90fc3816d8)에 나와 있습니다. 최종 사용자가 이러한 서비스를 사용하도록 허용할지 여부를 결정할 수 있습니다. 자세한 내용은 [관리자가 엔터프라이즈용 Microsfot 365 앱에서 컨트롤러 서비스를 관리할 수 있는 방법](/DeployOffice/manage-controller-services-office-365-proplus)을 참조하세요. 이러한 선택적 서비스가 개인 데이터를 처리하는 경우 Microsoft는 이러한 서비스에 대한 데이터 통제자가 됩니다.
- **사용자 의견:** 사용자에게 Microsoft 제품 및 서비스에 대해 의견을 제공하기로 선택하며 이러한 의견에 개인 데이터가 포함될 경우 Microsoft는 이러한 의견에 대한 데이터 통제자가 됩니다. Microsoft는 사용자에게 의견 수집 프로세스 동안 개인 데이터를 포함하지 않도록 안내한 경우를 제외하고 Microsoft에서 수집하는 의견(Microsoft 하위 프로세서가 관리하는 의견 포함)에 대한 모든 데이터 주체 요청을 이행합니다. 예외: Microsoft가 사용자 의견을 수집하는 동안 사용자에게 개인 데이터를 포함하지 않도록 안내한 경우 Microsoft는 이러한 안내에 따라 제공된 개인 데이터가 없는 것으로 가정합니다. 타사 사용자 의견 서비스 제공자를 통해 별도의 계정을 만든 사용자는 해당 제공자와 함께 자신의 DSR을 직접 이행해야 합니다.
- **회사 또는 학교 계정을 통해 인증된 Windows:** 조직에서 Windows 라이선스를 구매하고 사용자가 회사 또는 학교 계정으로 조직에서 제공하는 Windows에 인증하는 경우, Microsoft는 데이터 통제자의 역할을 합니다. 
- **사용자가 구입한 제품 또는 서비스:** 사용자가 인증에 AAD를 사용하는 Microsoft 제품 또는 서비스(예: Office 추가 기능 또는 Microsoft Store에서 구입할 수 있는 응용 프로그램)를 개인적으로 구입하도록 허용한 경우 Microsoft는 데이터 통제자일 수 있습니다. 이러한 Microsoft 제품 또는 서비스의 경우 사용자는 Microsoft에 직접 문의하여 DSR을 시작해야 합니다.

> [!IMPORTANT]
> Azure Active Directory를 통해 활성화된 사용자를 삭제한 경우 이 사용자는 이전에 회사 또는 학교 계정으로 사용할 수 있었던 제품 또는 서비스에 로그인할 수 없게 됩니다. 또한 Microsoft는 Microsoft가 데이터 통제자인 제품 또는 서비스에 대한 DSR 요청과 관련하여 해당 사용자를 더 이상 인증할 수 없습니다. 사용자가 이러한 서비스에 대해 DSR을 시작하도록 하려면 사용자의 AAD 계정을 삭제하기 전에 해당 사용자에게 DSR을 시작하도록 지시해야 합니다.

### <a name="personal-accounts"></a>개인 계정

사용자가 Microsoft 계정(즉, 개인 계정)을 사용하여 Microsoft가 데이터 통제자인 제품 및 서비스를 Microsoft에서 개인적인 용도로 구입한 경우 사용자는 [Microsoft 개인 정보 대시보드](https://account.microsoft.com/account/privacy)를 사용하여 DSR 요청을 시작할 수 있습니다.

### <a name="third-party-products"></a>타사 제품

조직 또는 사용자가 개인적으로 타사에서 제품 또는 서비스를 구입하고 Microsoft 회사 또는 학교 계정을 인증에 사용하는 경우에는 모든 데이터 주체 요청을 해당 타사로 전달해야 합니다.

## <a name="appendix-a-preparing-for-dsr-investigations"></a>부록 A: DSR 조사 준비

조직에서 Office 365 서비스를 사용하여 DSR 조사를 준비하도록 도와주려면 다음 권장 사항을 고려하세요.

- 보안 및 준수 센터에서 DSR eDiscovery 사례 도구를 사용하여 DSR 조사를 관리합니다.
- 콘텐츠 검색 범위를 제한하도록 준수 경계를 설정합니다.
- DSR 조사에서 감사 로그 검색 도구를 사용합니다.

### <a name="use-the-dsr-case-tool-to-manage-dsr-investigations"></a>DSR 사례 도구를 사용하여 DSR 조사를 관리합니다.

보안 및 준수 센터에서 DSR 사례 도구를 사용하여 DSR 조사를 관리하는 것이 좋습니다. DSR 사례 도구를 사용하면 다음을 수행할 수 있습니다.

- 각 DSR 조사에 대한 별도의 사례를 만들 수 있습니다.

- 기본 제공 기능을 사용하여 특정 데이터 주체와 관련된 모든 콘텐츠를 검색할 수 있습니다. 케이스를 만들고 검색을 시작하면 이러한 콘텐츠 위치가 검색됩니다.

   - 조직의 모든 사서함(모든 Microsoft Teams 및 Microsoft 365 그룹과 연결된 사서함 포함)
   - 조직의 모든 SharePoint Online 사이트 및 비즈니스용 OneDrive 계정
   - 조직의 모든 Microsoft Teams 사이트 및 Microsoft 365 그룹 사이트
   - Exchange Online의 모든 공용 폴더

- 기본 검색 쿼리를 수정하고 검색을 다시 실행하여 검색 결과의 범위를 좁힐 수 있습니다.

- 사용자를 구성원으로 추가하여 사례에 액세스할 수 있는 사람을 제어할 수 있습니다. 구성원만 사례에 액세스할 수 있으며, 보안 및 준수 센터의 DSR 사례 페이지에 있는 사례 목록에서 자신의 사례만 볼 수 있습니다. 또한 동일한 사례의 여러 구성원에게 서로 다른 권한을 할당할 수 있습니다. 예를 들어 일부 구성원은 사례 및 콘텐츠 검색 결과만 보도록 허용하고, 다른 구성원은 검색을 만들고 검색 결과를 내보내도록 허용할 수 있습니다.

- 내보내기 작업을 만들어 DSR 내보내기 요청에 대한 응답으로 검색 결과를 내보낼 수 있습니다. 콘텐츠 검색에서 반환되는 모든 콘텐츠를 내보낼 수 있습니다. 데이터 주체와 관련된 다른 Office 365 데이터도 내보낼 수 있습니다.

- 내보내기 작업을 만들어 DSR 내보내기 요청에 대한 응답으로 검색 결과를 내보낼 수 있습니다. 콘텐츠 검색에서 반환되는 모든 콘텐츠를 내보낼 수 있습니다. Office 로밍 서비스에 대한 시스템 생성 로그를 내보낼 수 있습니다.

- DSR 조사 프로세스가 완료된 경우 사례를 삭제할 수 있습니다. 이렇게 하면 모든 콘텐츠 검색이 제거되고 사례와 연결된 작업이 내보내집니다.

DSR 사례 사용을 시작하려면 보안 및 준수 센터에서 [DSR 사례 도구를 사용하여 GDPR 데이터 주체 요청 관리하기](/microsoft-365/compliance/manage-gdpr-data-subject-requests-with-the-dsr-case-tool)를 참조하세요.

> [!IMPORTANT]
> eDiscovery 관리자는 조직의 모든 DSR 사례를 보고 관리할 수 있습니다. eDiscovery와 관련된 여러 역할에 대한 자세한 내용은 [잠재적 사례 구성원에게 eDiscovery 권한 할당](/Office365/SecurityCompliance/assign-ediscovery-permissions)을 참조하세요.

### <a name="set-up-compliance-boundaries-to-limit-the-scope-of-content-searches"></a>콘텐츠 검색 범위를 제한하도록 준수 경계를 설정합니다.

보안 준수 센터의 검색 권한 필터링 기능을 사용하여 준수 경계를 구현할 수 있습니다. 준수 경계는 조직 내에서 IT 관리자 또는 준수 관리자가 검색할 수 있는 콘텐츠 위치(예: Exchange Online 사서함 및 SharePoint Online 사이트)를 제어/제한하는 논리적 검색 경계를 만듭니다. 준수 경계는 지리적 경계를 고려해야 하는 다국적 조직, 여러 기관을 분리해야 하는 정부 조직, 비즈니스 단위 또는 부서로 세분화된 비즈니스 조직 등에 유용합니다. 이 모든 시나리오에서 DSR 조사에 준수 경계를 사용하여 조사에 참여한 사람이 검색할 수 있는 사서함 및 사이트를 제한할 수 있습니다.

준수 경계를 eDiscovery 사례와 함께 사용하여 조사에서 검색할 수 있는 콘텐츠 위치를 기관 또는 비즈니스 단위 내부의 위치로만 제한할 수 있습니다.

DSR 조사에 대한 준수 경계(eDiscovery 사례와 함께)를 구현하는 방법에 대한 대략적인 개요는 다음과 같습니다.

1. 조직에서 준수 경계로 지정할 기관을 결정합니다.

2. Azure Active Directory에서 준수 경계를 정의하는 데 사용할 사용자 개체 특성을 결정합니다. 예를 들어 다음 단계에서 만든 관리자 역할 그룹의 구성원만 특정 특성 값을 가진 사용자의 콘텐츠 위치를 검색할 수 있도록 Country, CountryCode 또는 Department 특성을 선택할 수 있습니다. 이러한 방법으로 특정 기관에서 콘텐츠를 검색할 수 있는 사람을 제한할 수 있습니다.

   > [!NOTE]
   > 비즈니스용 OneDrive의 경우 추가 단계를 수행하고 Microsoft 지원에 비즈니스용 OneDrive 계정에 특성을 동기화하도록 요청해야 합니다.

3. 보안 및 준수 센터에서 각 준수 경계에 대한 관리자 역할 그룹을 만듭니다. 기본 제공 eDiscovery 관리자 역할 그룹을 복사한 다음, 필요에 따라 역할을 제거하여 이러한 역할 그룹을 만드는 것이 좋습니다.

4. 각 특정 역할 그룹에 구성원을 eDiscovery 관리자로 추가합니다. 구성원은 DSR을 조사 및 응답하는 역할을 수행하며, 일반적으로 IT 관리자, 데이터 개인 정보 관리자, 준수 관리자 및 인사 담당자로 구성됩니다.

5. 해당 관리자 역할 그룹의 구성원만 해당 기관/준수 경계 내 사용자의 사서함 및 사이트를 검색할 수 있도록 각 준수 경계에 대해 검색 권한 필터를 만듭니다. 검색 권한 필터는 해당 역할 그룹의 구성원이 기관/준수 경계에 해당하는 사용자 개체 특성 값이 있는 콘텐츠 위치만 검색하도록 허용합니다.

단계별 지침은 [Office 365에서 eDiscovery 조사에 대한 준수 경계 설정](/microsoft-365/compliance/set-up-compliance-boundaries)을 참조하세요.

### <a name="use-the-audit-log-search-tool-in-dsr-investigations"></a>DSR 조사에서 감사 로그 검색 도구를 사용합니다.

IT 관리자는 보안 및 준수 센터에서 감사 로그 검색 도구를 사용하여 문서, 파일 및 기타 사용자가 만들거나, 액세스하거나, 변경하거나, 삭제한 Office 365 리소스를 식별할 수 있습니다. 이러한 종류의 활동을 검색하는 것은 DSR 조사에서 유용할 수 있습니다. 예를 들어 SharePoint Online 및 비즈니스용 OneDrive에서는 사용자가 다음 활동을 수행할 때 감사 이벤트가 기록됩니다.

- 파일에 액세스
- 파일 수정
- 파일 이동
- 파일 업로드 또는 다운로드

특정 활동, 활동 유형, 특정 사용자가 수행한 활동 및 기타 검색 조건에 대해 감사 로그를 검색할 수 있습니다. SharePoint Online 및 비즈니스용 OneDrive 활동 외에도 Flow, Power BI 및 Microsoft Teams에서 활동을 검색할 수 있습니다. 감사 레코드는 90일 동안 보관됩니다. 따라서 90일 이전에 발생한 사용자 활동은 검색할 수 없습니다. 감사되는 활동의 전체 목록 및 감사 로그를 검색하는 방법은 [보안 및 준수 센터에서 감사 로그 검색](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)을 참조하세요.

> [!TIP]
> 위에 설명된 90일 제한 문제를 해결하고 조직의 감사 레코드에 대한 실행 기록을 유지 관리하려면 되풀이되는 일정(예: 30일마다)으로 모든 활동을 내보내 조직의 감사 레코드에 대한 연속 레코드를 만들면 됩니다.

## <a name="appendix-b-change-log"></a>부록 b: 변경 로그

다음 표에서는 2018년 5월 25일에 처음 게시된 이후, 변경된 Office 365 DSR 가이드 내용이 나와 있습니다.

|날짜  |섹션/앱 |변경 사항  |
|:---------|:---------|:---------|
|2018년 9월 18일 | [Whiteboard](#whiteboard) |Whiteboard 미리 보기는 더 이상 미리 보기가 아니며, 일반 공급용으로 출시되었습니다. 따라서 Whiteboard 미리 보기에 대한 섹션 이름은 "PC, Surface Hub 및 기타 플랫폼용 Whiteboard"로 변경되었으며, 데이터를 액세스, 내보내기 및 삭제하기 위한 절차가 이 섹션에서 제거된 후 Whiteboard 지원 문서에 대한 링크로 바뀌었습니다.|
|2018년 11월 8일 | [Workplace Analytics](#workplace-analytics) |Workplace Analytics에서 데이터 주체를 제거하고 Workplace Analytics 보고서에서 데이터 주체에 대한 정보를 제거하는 방법에 대한 단계별 지침이 삭제 섹션에 추가되었습니다.|
|2018년 11월 12일| 모두| 끊어진 책갈피 및 외부 항목에 대한 끊어진 링크를 수정했습니다.|
|2019년 1월 9일| StaffHub |삭제 섹션에서는 사용자 계정을 영구적으로 삭제할 때 발생하는 작업에 대한 설명이 업데이트되었습니다.|
|2019년 5월 8일| [Publisher](#publisher)|Publisher의 DSR에 대한 응답 관련 콘텐츠가 추가되었습니다.|
|2019년 7월 11일| [MyAnalytics](#myanalytics)|모든 사용자가 MyAnalytics 앱에서 해당 데이터를 볼 수 있기 때문에 관리자가 보안 및 준수 센터에서 DSR 사례 도구를 사용하여 MyAnalytics 데이터를 내보내는 기능이 제거되었습니다. |
|2019/11/6|[교육](#education)|PowerShell 스크립트를 사용하여 특정 학생의 수업 목록을 가져온 다음 해당 학생의 데이터를 내보내거나 삭제하는 방법에 대한 새 주제에 연결되었습니다.|
|2020/1/28| 모두 | 문서에서 StaffHub가 제거되었습니다. StaffHub는 사용이 중지되었습니다. |
||||
