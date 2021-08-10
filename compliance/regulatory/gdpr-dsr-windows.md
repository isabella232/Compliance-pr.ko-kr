---
title: GDPR 및 CCPA에 대한 Windows 진단 데이터 프로세서 구성 데이터 주체 요청
description: Microsoft 제품, 서비스 및 관리 도구를 사용하여 개인 데이터를 찾아서 작업을 하여 DSR에 응답하는 방법을 알아봅니다.
keywords: Microsoft 365, Microsoft 365 Education, Microsoft 365 설명서, GDPR
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: 365aa84ce2c88468b7f6689aa73507e458a435fd2d3bc58583114f37f50537ac
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293055"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>GDPR 및 CCPA에 대한 Windows 진단 데이터 프로세서 구성 데이터 주체 요청

>[!NOTE]
>이 항목은 Windows 10 Enterprise, Pro 및 Education 버전, 버전 1809(2021년 7월 업데이트 및 최신 업데이트 포함)에 적용됩니다.

## <a name="introduction-to-data-subject-requests-dsrs"></a>DSR(데이터 주체 요청) 소개

EU GDPR(일반 데이터 보호 규정)은 사람들(규정에서 _데이터 주체_)에게 고용주 또는 다른 유형의 기관이나 조직(_데이터 컨트롤러_ 또는 간단하게 _컨트롤러_)에 의해 수집된 개인 데이터를 관리할 권한을 제공합니다. GDPR에서 개인 데이터는 식별되거나 식별 가능한 자연인에 관련된 모든 데이터로 광범위하게 정의됩니다. GDPR은 데이터 주체에게 개인 데이터에 대한 특정 권한을 제공합니다. 이러한 권한에는 개인 데이터의 복사본을 얻거나, 수정을 요청하거나, 처리를 제한하거나, 삭제하거나, 다른 관리자에게 전달할 수 있도록 전자 형식으로 개인 데이터를 수신할 권한이 포함됩니다. 데이터 주체가 개인 데이터에 대한 작업을 수행하도록 관리자에게 공식적으로 요청하는 것을 DSR(_Data Subject Request_)이라고 합니다.

마찬가지로 CCPA(캘리포니아 소비자 개인 정보 보호법)은 캘리포니아 소비자에게 GDPR의 데이터 주체 권리와 유사한 권리를 포함하여, 소비자의 개인 정보 삭제, 액세스 및 수신(이식성)과 같은 개인 정보 보호 권리 및 의무를 제공합니다. 또한 CCPA는 특정 공개, 실행 권리 행사 시 차별 대우로부터 보호, “판매”로 분류되는 특정 데이터 전송에 대한 “옵트아웃(opt-out)/옵트인(opt-in)” 요구도 제공합니다. 판매는 가치 있는 대가관계를 위하여 데이터 공유를 포함하도록 광범위하게 정의됩니다. CCPA에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법](/microsoft-365/compliance/offering-ccpa) 및 [캘리포니아 소비자 개인 정보 보호법 FAQ](/microsoft-365/compliance/ccpa-faq)를 참조하세요.

이 가이드에서는 Microsoft 제품, 서비스 및 관리 도구를 사용하여 컨트롤러 고객이 DSR에 응답하기 위해 개인 데이터를 찾고 조치를 취하는 데 도움을 주는 방식을 설명합니다. 특히 Windows 진단 데이터 프로세서 구성이 사용하도록 설정된 경우 Microsoft에서 수집한 Windows 진단 데이터에서 개인 데이터를 찾고, 액세스하고, 조치를 수행하는 방법이 포함됩니다. 다음은 이 가이드에 설명된 프로세스에 대한 간략한 개요입니다.

1. **액세스** - 데이터 주체와 연결된 Windows 진단 데이터를 검색하고, 요청될 경우 데이터 주체가 사용할 수 있는 복사본을 만듭니다.
2. **삭제** -데이터 주체와 연결된 Windows 진단 데이터를 영구적으로 제거합니다.
3. **내보내기** - Windows 진단 데이터의 전자 사본(컴퓨터가 읽을 수 있는 형식)을 데이터 주체에게 제공합니다.

CCPA 하에서 개인 정보는 식별된 또는 식별 가능한 개인과 관련 있는 모든 정보입니다. 이때 개인의 비공개, 공개 또는 업무 역할이 구분되지 않습니다. 정의된 "개인 정보"라는 용어는 GDPR에 따른 "개인 데이터"와 대략 일치합니다. 그러나 CCPA에는 가족 및 가정 데이터가 포함되어 있습니다. CCPA에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법](/microsoft-365/compliance/offering-ccpa) 및 [캘리포니아 소비자 개인 정보 보호법 FAQ](/microsoft-365/compliance/ccpa-faq)를 참조하세요.

이 가이드의 각 섹션에서는 Windows 진단 데이터 프로세서 구성이 사용하도록 설정된 경우 Microsoft에서 수집한 Windows 진단 데이터에 대한 DSR에 응답하기 위해 데이터 컨트롤러 조직에서 수행할 수 있는 기술적 절차를 간략하게 설명합니다.

## <a name="terminology"></a>용어

다음 목록은 이 가이드와 관련된 용어의 정의를 제공합니다.

* _통제자:_ 단독으로 또는 다른 대상과 함께 개인 데이터 처리의 목적 및 방법을 결정하는 자연인이나 법인, 공공 기관, 대리점 또는 기타 단체입니다. 이러한 처리의 목적 및 방법을 연합국 법률 또는 회원국 법률에 따라 결정하는 경우, 통제자 또는 구체적인 지명 기준을 연합국 법률 또는 회원국 법률에서 제공할 수 있습니다.

* _개인 데이터 및 데이터 주체_ 식별되었거나 식별 가능한 자연인(‘데이터 주체’)과 관련된 모든 정보입니다. 식별 가능한 자연인은 직간접적으로, 특히 이름, 식별 번호, 위치 데이터, 온라인 식별자 또는 해당 자연인의 신체적, 생리적, 유전적, 정신적, 경제적, 문화적 또는 사회적 ID와 같은 식별자를 참조하여 식별될 수 있는 사람입니다.

* _데이터 프로세서_ 데이터 컨트롤러를 대신하여 개인 정보를 처리하는 자연인 또는 법인, 공공 당국, 기관 또는 기타 주체입니다.

* _고객 데이터_—모든 텍스트, 사운드, 비디오 또는 이미지 파일 및 소프트웨어를 포함한 모든 데이터와 엔터프라이즈 서비스를 사용하여 고객이 또는 대신하여 Microsoft에 제공합니다. 

* _Windows 진단 데이터_- 디바이스와 Windows 및 관련 소프트웨어의 작동 방식에 대한 Windows 디바이스의 기술 데이터입니다. Windows를 최신 상태로 유지하고, 안전하고, 안정적이며, 성능을 향상시키고, 제품을 개선하는 데 사용됩니다. Windows 진단 데이터의 몇 가지 예로는 사용 중인 하드웨어 유형, 각각의 용도에 맞게 설치된 응용 프로그램 및 디바이스 드라이버의 안정성 정보가 있습니다. 일부 Windows 구성 요소 및 앱은 Microsoft 서비스에 직접 연결되지만 교환하는 데이터는 Windows 진단 데이터가 아닙니다. 예를 들어 지역 날씨 또는 뉴스를 위해 사용자 위치를 교환하는 것은 Windows 진단 데이터의 예가 아닙니다.

## <a name="how-to-use-this-guide"></a>이 가이드를 사용하는 방법

Windows 진단 데이터 프로세서 구성을 사용하도록 설정하면 디바이스에서 수집된 Windows 진단 데이터의 컨트롤러가 됩니다. 이 구성에 대한 자세한 내용은 [조직에서 Windows 진단 데이터 구성](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)을 참조하세요.

## <a name="windows-diagnostic-data"></a>Windows 진단 데이터

Microsoft는 사용자의 Windows 진단 데이터 프로세서 구성이 사용하도록 설정된 디바이스 사용과 관련된 Windows 진단 데이터에 액세스, 삭제 및 내보낼 수 있는 기능을 제공합니다.

> [!IMPORTANT]
> 일부 Windows 진단 데이터는 디바이스 식별자와만 연결되며 특정 사용자와 연결되지 않습니다. 이러한 유형의 디바이스 수준 데이터는 내보내지지 않으며 30일 이내에 시스템에서 삭제됩니다.<br><br>
> Windows 진단 데이터를 수정하는 기능은 지원되지 않습니다. Windows 진단 데이터는 Windows 내에서 수행되는 사실상의 작업으로, 이러한 데이터를 수정하면 작업 기록의 기록이 손상되어 보안 위험이 증가하고 신뢰성이 저하됩니다.

다음 섹션에서는 AAD(Azure Active Directory) 사용자 ID와 연결된 Windows 진단 데이터에 대한 데이터 주체 요청을 실행하는 방법에 대한 단계를 제공합니다. 자세한 내용은 [Windows 10 및 개인 정보 준수: IT 및 규정 준수 전문가용 가이드](/windows/privacy/windows-10-and-privacy-compliance)를 참조하세요.

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Windows 진단 데이터에 대한 DSR 실행

Microsoft는 Azure Portal을 통해 그리고 또한 기존 API(응용 프로그래밍 인터페이스)를 통해 직접 특정 Windows 진단 데이터에 액세스, 삭제 및 내보낼 수 있는 기능을 제공합니다.

### <a name="step-1-access"></a>1단계: 액세스

Microsoft는 조직 내의 테넌트 관리자가 특정 사용자의 Windows 진단 데이터 프로세서 구성이 사용하도록 설정된 디바이스 사용과 관련된 Windows 진단 데이터에 액세스하는 방법을 제공합니다. 액세스 요청에 대해 검색된 데이터는 내보내기를 통해 시스템에서 읽을 수 있는 형식으로 제공되며, 사용자가 데이터와 연결된 장치 및 서비스를 알 수 있는 파일로 제공됩니다. 이전에 설명한 것처럼 검색된 데이터에는 Windows 장치의 보안이나 안정성을 해칠 수 있는 데이터가 포함되지 않습니다.

Azure Portal에서는 기업 고객의 테넌트 관리자가 DSR 액세스 요청을 관리할 수 있는 기능을 제공합니다. [Azure DSR, 2부, 3단계: 내보내기](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export)에서는 Azure Portal에서 내보내기를 통해 Windows 진단 데이터에 대한 DSR 액세스 요청을 실행하는 방법을 설명합니다.

### <a name="step-2-delete"></a>2단계: 삭제

Microsoft는 특정 사용자의 Azure Active Directory 개체를 기반으로 사용자 기반 DSR 삭제 요청을 실행하는 방법을 제공합니다.

사용자 기반 삭제 요청의 경우 Microsoft는 두 가지 솔루션을 제공합니다.  기업 고객의 테넌트 관리자가 DSR 삭제 요청을 관리할 수 있는 기능을 제공하는 포털 환경이 있습니다. [Azure DSR, 1부, 5단계: 삭제](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete)에서는 Azure Portal에서 사용자와 연결된 데이터를 삭제하여 Windows 진단 데이터에 대한 DSR 삭제 요청을 실행하는 방법을 설명합니다.

Microsoft는 사용자를 삭제할 수 있는 기능을 제공하며, 이 기능을 사용하면 기존 API(응용 프로그램 프로그래밍 인터페이스)를 통해 Windows 진단 데이터를 직접 삭제할 수 있습니다. 자세한 내용은 [API 참조 설명서](/graph/api/directory-deleteditems-delete)에 설명되어 있습니다.

>[!IMPORTANT]
>수집된 데이터를 삭제해도 디바이스의 추가 수집이 중지되지 않습니다. 데이터 수집을 해제하려면 [관련 서비스의 참조 문서](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management)에 설명된 절차를 따릅니다.

### <a name="step-3-export"></a>3단계: 내보내기

조직 내의 테넌트 관리자만 특정 사용자의 Windows 진단 데이터 프로세서 구성이 사용하도록 설정된 디바이스 사용과 관련된 Windows 진단 데이터에 액세스할 수 있습니다. 내보내기 요청에 대해 검색된 데이터는 시스템에서 읽을 수 있는 형식으로 제공되며 사용자가 해당 데이터와 연결된 장치 및 서비스를 알 수 있는 파일로 제공됩니다. 이전에 설명한 것처럼 검색된 데이터에는 Windows 장치의 보안이나 안정성을 해칠 수 있는 데이터가 포함되지 않습니다. [Azure DSR, 2부, 3단계: 내보내기](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export)에서는 Azure Portal을 통해 Windows 진단 데이터에 대한 DSR 내보내기 요청을 실행하는 방법을 설명합니다.

또한 Microsoft는 기존 API(응용 프로그램 프로그래밍 인터페이스)를 통해 Windows 진단 데이터를 직접 내보낼 수 있는 기능을 제공합니다. 자세한 내용은 [API 참조 설명서](/graph/api/user-exportpersonaldata)에 설명되어 있습니다.

## <a name="notify-us-about-exporting-or-deleting-issues"></a>내보내기 또는 삭제 중 발생하는 문제에 대한 알림

Azure Portal에서 Windows 진단 데이터를 내보내거나 삭제하는 동안 문제가 발생하면 Azure Portal **도움말 + 지원** 블레이드로 이동하여 **구독 관리 > 구독에 대한 개인 정보 보호 및 준수 요청 > 개인 정보 보호 블레이드 및 GDPR 요청** 에서 새 티켓을 제출합니다.

>[!NOTE]
>Windows 진단 데이터 내보내기 요청을 완료하는 데 최대 5일이 걸릴 수 있습니다. 문제가 발생할 경우 최소 7일 이상 여유를 두고 지원 티켓을 여세요.
