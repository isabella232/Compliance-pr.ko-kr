---
title: DPIA(데이터 보호 영향 평가) - Windows 진단 데이터 프로세서 구성을 사용하는 컨트롤러에 대한 지침
description: Windows Enterprise용 Microsoft 데이터 프로세서 서비스를 사용할 때 DPIA(데이터 보호 영향 평가)가 필요한지 여부를 확인하는 정보를 찾습니다.
keywords: DPIA, Microsoft 365, Microsoft 365 Education, Microsoft 365 설명서, GDPR
ms.localizationpriority: high
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
ms.openlocfilehash: 325dc91f1d3480414236abfde38eb48d372f3e69
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161182"
---
# <a name="data-protection-impact-assessments-guidance-for-controllers-using-windows-diagnostic-data-processor-configuration"></a>데이터 보호 영향 평가 - Windows 진단 데이터 프로세서 구성을 사용하는 컨트롤러에 대한 지침

>[!NOTE]
>이 항목은 Windows 10 Enterprise, Pro 및 Education 버전, 버전 1809(2021년 7월 업데이트 및 최신 업데이트 포함)에 적용됩니다.

GDPR(일반 데이터 보호 규정)에 따르면 컨트롤러는 “자연인의 권리와 자유에 높은 위험을 초래하기 쉬운” 작업을 처리하기 위한 DPIA(데이터 보호 영향 평가)를 준비해야 합니다. Windows 진단 데이터 프로세서 구성 자체에는 이를 사용하여 컨트롤러에서 DPIA를 생성해야 하는 고유한 기능이 없습니다. 대신 DPIA가 필요한지 여부는 컨트롤러가 [Windows 진단 데이터 프로세서 구성](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)을 배포, 구성 및 사용하는 방법에 대한 세부 정보와 컨텍스트에 따라 달라집니다.

이 문서의 목적은 컨트롤러에 Windows 진단 데이터 프로세서 구성에 대한 정보를 제공함으로써 DPIA가 필요한지 여부 및 필요한 경우 포함할 세부 정보를 결정하는 데 도움이 되는 정보를 제공하기 위한 것입니다.

>[!Note]
>Microsoft는이 문서에 법적 자문을 제공하지 않습니다. 이 문서는 정보 제공의 목적으로만 제공됩니다. 고객은 개인 정보 보호 담당자 및 법률 고문과 협력하여 Windows 진단 데이터 프로세서 구성 또는 기타 Microsoft 온라인 서비스 사용과 관련된 모든 DPIA의 필요성과 내용을 파악해야 합니다.

## <a name="part-1-determining-whether-a-dpia-is-needed"></a>1부: DPIA가 필요한지 여부를 판단

GDPR 제35조에는 컨트롤러가 특별히 새로운 기술을 이용한 처리 유형인 '[w]여기서 데이터 보호 영향 평가(DPIA) '[w]를 작성하도록 하고 있으며, 처리의 특성, 범위, 맥락 및 목적을 고려한다면 자연인의 권리와 자유에 대한 위험성이 높아지기 쉽습니다.' 또한 이러한 고위험을 나타내는 특정 요인을 추가로 제시하며, 이 요인은 다음 표에 설명되어 있습니다. DPIA가 필요한지 여부를 결정하기 위해 컨트롤러는 컨트롤러의 특정 구현 및 Windows 진단 데이터 프로세서 구성 사용에 비추어 다른 관련 요소와 함께 이러한 요인을 고려해야 합니다.

## <a name="table-1-windows-diagnostic-data-processor-configuration-dpia-risk-factors"></a>표 1: Windows 진단 데이터 프로세서 구성 DPIA 위험 요인

| 높은 위험 요인 | Windows 진단 데이터 프로세서 구성에 대한 관련 정보 |
|:----|:----|
| 프로파일링 등을 포함한 자동화된 처리에 기반한 자연인에 관한 개인적 측면의 체계적이고 광범위한 평가로 해당 평가에 근거한 결정이 해당 자연인에게 법적 효력을 미치거나 이와 유사히 자연인에게 중대한 영향을 미치는 경우입니다. |Windows 진단 데이터 프로세서 구성은 특정 데이터 자동 처리를 수행할 수 있는 기능을 제공하지 않습니다. <br><br> 그러나 다른 서비스는 Windows 진단 데이터 프로세서 구성에 따라 수집된 진단 데이터를 데이터 원본으로 사용하기 때문에 데이터 컨트롤러는 이러한 처리에 사용하도록 해당 서비스를 구성할 수 있습니다. 컨트롤러는 Windows 진단 데이터 프로세서 구성에 따라 수집된 진단 데이터를 사용하는 서비스의 사용량에 따라 이 결정을 내려야 합니다.|
| 특정 범주의 대규모* 데이터(인종 또는 민족 태생, 정치적 견해, 종교적 또는 철학적 신념, 노동 조합 회원 및 유전자 데이터, 자연인의 고유한 식별을 목적으로 하는 생체 데이터, 건강 또는 자연인의 성생활이나 성적 취향에 관한 데이터의 처리) 처리 또는 범죄 유죄 판결 및 범죄와 관련된 개인 데이터 처리. | Windows 진단 데이터 프로세서 구성은 특수 범주의 개인 데이터를 처리하도록 특별히 설계되지 않았으므로 Windows 진단 데이터 프로세서 구성을 사용해도 컨트롤러 처리의 내재된 위험이 증가하지 않습니다. <br><br> 그러나 데이터 컨트롤러는 Windows 진단 데이터 프로세서 구성에 따라 수집된 진단 데이터를 사용하는 서비스를 사용하여 열거된 특수 범주의 데이터를 처리할 수 있습니다. Windows 진단 데이터 프로세서 구성에 따라 수집된 진단 데이터를 데이터 원본으로 사용하는 서비스를 통해 고객은 특수 범주의 개인 데이터를 포함하여 모든 유형의 데이터를 추적하거나 처리할 수 있습니다. 그러나 데이터 프로세서는 Microsoft가 이러한 사용을 제어할 수 없으며 이러한 사용에 대한 통찰력도 거의 또는 전혀 없습니다. 데이터 컨트롤러의 데이터를 적절하게 사용하는 것은 데이터 컨트롤러의 책임입니다.|

## <a name="part-2-contents-of-a-dpia"></a>2부 - DPIA의 내용

제 35(7)조는 데이터 보호 영향 평가가 처리의 목적과 계획된 처리의 체계적 설명을 명시하도록 규정하고 있습니다. 포괄적인 DPIA의 체계적 설명에는 처리된 데이터 유형, 데이터 보존 기간, 데이터 위치 및 전송 위치, 데이터에 액세스할 수 있는 제3자 등의 요인이 포함될 수 있습니다. 또한 DPIA에는 다음이 포함되어야 합니다.

- 목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가;
- 자연인의 권리와 자유에 대한 위험 평가;
- 위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 이 규정을 준수함을 입증하기 위한 메커니즘.

다음 표에는 각 요소와 관련된 Windows 진단 데이터 프로세서 구성에 대한 정보가 포함되어 있습니다. 파트 1에서와 같이 데이터 컨트롤러는 컨트롤러의 특정 구현 및 Windows 진단 데이터 프로세서 구성 사용의 맥락에서 다른 관련 요소와 함께 아래에 제공된 세부 정보를 고려해야 합니다.

## <a name="table-2-windows-diagnostic-data-processor-configuration-dpia-elements"></a>표 2: Windows 진단 데이터 프로세서 구성 DPIA 요소

| DPIA의 요소 | Windows 진단 데이터 프로세서 구성에 대한 관련 정보 |
|:---|:---|
| 처리 목적 | Windows 진단 데이터 프로세서 구성에 따라 수집된 진단 데이터를 처리하는 목적은 이를 구현, 구성 및 사용하는 컨트롤러에 의해 결정됩니다. <br><br> Microsoft는 데이터 프로세서로서 Microsoft 제품 약관의 조건에 따라 Windows 진단 데이터 처리합니다. <br><br> Microsoft는 다음과 같은 합법적인 비즈니스 운영 지원을 위하여 개인 데이터를 사용합니다. (1) 청구 및 계정 관리. (2) 보상 (예: 사원 수수료과 파트너의 성과급 계산). (3) 내부 보고 및 모델링 (예: 예측, 수익, 용량 계획, 제품 전략); (4) Microsoft 또는 Microsoft 제품에 영향을 줄 수 있는 사기, 사이버 범죄 또는 사이버-공격 방어. (5) 접근성, 개인 정보 보호 또는 에너지 효율성의 핵심 기능 개선. (6) 법률적인 의무를 통한 재무 보고 및 준수 (Windows 진단 데이터 노출에 대한 제한 사항 준수). <br><br> Microsoft는 이러한 특정 합법적인 비즈니스 작업에 대한 Windows 진단 데이터 처리의 컨트롤러입니다. 일반적으로 Microsoft는 합법적인 비즈니스 운영에 사용하기 전에 Windows 진단 데이터를 집계하여 특정 개인을 식별할 수 있는 Microsoft의 능력을 제거하고, 합법적인 비즈니스 운영에 필요한 처리를 지원하는 가장 식별하기 어려운 형식으로 Windows 진단 데이터를 사용합니다. <br><br> Microsoft는 Windows 진단 데이터 프로세서 구성을 사용할 때 수집된 Windows 진단 데이터 또는 광고나 유사한 상업적 목적으로 수집된 정보를 사용하지 않습니다.|
| 처리된 개인 데이터의 범주 | **Windows 진단 데이터**- 디바이스와 Windows 및 관련 소프트웨어의 작동 방식에 대한 Windows 디바이스의 기술 데이터입니다. Windows를 최신 상태로 유지하고, 안전하고, 안정적이며, 성능을 향상시키고, 제품을 개선하는 데 사용됩니다. Windows 진단 데이터의 몇 가지 예로는 사용 중인 하드웨어 유형, 각각의 용도에 맞게 설치된 응용 프로그램 및 디바이스 드라이버의 안정성 정보가 있습니다. 일부 Windows 구성 요소 및 앱은 Microsoft 서비스에 직접 연결되지만 교환하는 데이터는 Windows 진단 데이터가 아닙니다. 예를 들어 지역 날씨 또는 뉴스를 위해 사용자 위치를 교환하는 것은 Windows 진단 데이터의 예가 아닙니다. <br><br> Windows 진단 데이터 프로세서 구성을 사용하는 경우 데이터 처리에 대한 자세한 내용은 [조직에 Windows 진단 데이터 구성](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 및 [Microsoft 보안 센터](https://www.microsoft.com/trust-center)를 참조하세요.|
| 데이터 보존 | Microsoft는 Microsoft 제품 약관에 따라 Windows 진단 데이터 프로세서 구성을 사용하도록 설정한 경우 수집된 Windows 진단 데이터를 보유하고 처리합니다. 고객은 [GGDPR 및 CCPA에 대한 Windows 진단 데이터 프로세서 구성 데이터 주체 요청](gdpr-dsr-windows.md)에 설명된 기능을 사용하여 데이터 주체 요청에 따라 Windows 진단 데이터를 삭제하고 내보낼 수 있습니다.|
| 개인 데이터의 위치 및 전송 | Windows 진단 데이터 프로세서 구성을 사용하는 경우 수집되는 Windows 진단 데이터는 미국에 있는 Microsoft 데이터 센터에 있습니다. |
| 타사와 데이터 공유 | Microsoft는 고객 및 기술 지원, 서비스 유지 보수 및 기타 운영과 같은 기능을 지원하기 위해 하위 프로세스(즉, 개인 데이터를 처리하는 하도급업체) 역할을 하는 타사와 데이터를 공유할 수 있습니다. Microsoft가 Windows 진단 데이터 프로세서 구성 또는 지원 데이터에 따라 수집된 Windows 진단 데이터를 전송하는 모든 하도급업자는 Microsoft 제품 약관의 조건 수준에 준하는 서면 계약을 Microsoft와 체결하게 됩니다. 고객 데이터 또는 지원 데이터를 공유하는 모든 타사 하청업체는 [하청업체 목록](https://www.microsoft.com/en-us/trust-center/privacy/data-access#subcontractors)(‘보조 처리 장치를 사용한 액세스 제한’ 참조)에 포함됩니다. <br><br>Windows 진단 데이터 프로세서 구성 및 지원 데이터에 따라 수집된 Windows 진단 데이터 대한 법 집행 및 타사 요청에 대한 Microsoft의 대응에 대한 정보는 Microsoft 제품 약관에 있습니다. Microsoft가 법적 금지되지 않는 한, Microsoft는 사법 기관 또는 타사를 고객에게 직접 요청하도록 리디렉션을 시도합니다. |
| 데이터 주체 권리 | 프로세서로 활동할 때 Microsoft는 GDPR에 따라 권한을 행사할 때 데이터 주체의 개인 데이터와 데이터 주체의 요청을 수행할 수 있는 기능을 고객(컨트롤러)에게 제공합니다. Microsoft는 제품의 기능 및 데이터 프로세서로서의 역할과 일치하는 방식으로 이를 수행합니다.  Microsoft가 고객의 데이터 주체로부터 GDPR에 따라 하나 이상의 권한을 행사하라는 요청을 받으면 해당 요청이 데이터 컨트롤러로 리디렉션됩니다.<br><br> [GDPR 및 CCPA에 대한 Windows 진단 데이터 프로세서 구성 데이터 주체 요청](gdpr-dsr-windows.md)에서는 Windows 진단 데이터 프로세서 구성에 따라 수집된 Windows 진단 데이터 대한 데이터 주체 권한을 지원하는 방법에 대한 설명을 제공합니다. |
| 목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가 | 이러한 평가는 데이터 컨트롤러의 요구와 처리 목적에 따라 달라집니다. <br><br> Microsoft에서 수행하는 처리와 관련하여 이러한 처리는 Microsoft 제품 약관에 반영된 처리 목적에 필수적이며 비례합니다. |
| 데이터 주체의 권리와 자유에 대한 위험 평가 | Windows 진단 데이터 프로세서 구성에 따라 수집된 Windows 진단 데이터 사용으로 인한 데이터 주체의 권한 및 자유에 대한 주요 위험은 컨트롤러가 Windows 진단 데이터를 구현하고, 구성하며, 사용하는 방법과 컨텍스트에 따라 결정됩니다. <br><br> Windows 진단 데이터 프로세서 구성에 따라 수집된 Windows 진단 데이터는 무단 액세스 또는 부주의로 인한 공개의 위험이 있습니다. 이러한 위험을 해결하기 위해 Microsoft에서 취하는 조치는 Microsoft 제품 약관에서 논의됩니다. |
| 위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 GDPR을 준수함을 입증하기 위한 메커니즘 | Microsoft는 Windows 진단 데이터 보안을 보호하기 위해 노력합니다. Microsoft에서 취하는 보안 조치는 Microsoft 제품 약관에 설명되어 있습니다. <br><br> Microsoft는 처리하는 개인 데이터를 보호하기 위해 합리적이고 적절한 기술 및 조직적 조치를 취합니다. 이러한 조치에는 내부 개인 정보 보호 정책 및 관행, 계약 약정, 국제 및 지역 표준 인증이 포함되며 이에 국한되지는 않습니다. 자세한 내용은 [보안 센터의 개인 정보 표준 페이지](https://www.microsoft.com/trustcenter/privacy/we-set-and-adhere-to-stringent-standards)에서 확인할 수 있습니다.<br><br> Microsoft는 Microsoft의 개인 데이터 사용 및 처리를 설명하는 데 도움이 되는 중요하고 투명한 고객 관련 보안 및 개인 정보 보호 자료를 제공합니다. 고객은 질문 사항을 준비하여 Microsoft에 문의할 것을 권장합니다. <br><br> 또한 Microsoft는 데이터 보호 영향 평가 및 기록 유지를 포함하지만 국한되지 않는 데이터 프로세스에 적용되는 모든 기타 GDPR 의무를 준수합니다. <br><br> Microsoft는 합법적인 비즈니스 운영을 위해 Windows 진단 데이터를 처리할 때 데이터 관리자에 적용되는 GDPR의 의무를 준수합니다. |

## <a name="learn-more"></a>자세한 정보

- [Microsoft 보안 센터](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
