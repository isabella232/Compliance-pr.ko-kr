---
title: GDPR에 따른 Azure, Dynamics 365 및 Windows 위반 알림
description: Azure 및 Dynamics 365가 개인 데이터 위반으로부터 보호하는 방법 및 Microsoft가 위반 발생 시 대응하고 사용자에게 알리는 방법입니다.
keywords: Azure, Microsoft 365, Dynamics 365, Microsoft 365 설명서, GDPR
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
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 23d6b1ebb30f34fcb549e3e1f44c98a0c0e11b12
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479810"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>GDPR에 따른 Azure, Dynamics 365 및 Windows 위반 알림

Microsoft는 GDPR(일반 데이터 보호 규정)에 따라 의무를 다합니다. Microsoft는 데이터 침해로부터 보호하기 위해 온라인 서비스 내에서 광범위한 보안 조치를 취합니다. 여기에는 물리적 및 논리적 보안 제어 뿐만 아니라 자동화된 보안 프로세스, 포괄적인 정보 보안 및 개인 정보 보호 정책, 모든 직원에 대한 개인 정보 보호 교육이 포함됩니다.

설계 단계부터 개인 정보 보호(Privacy-by-Design) 및 기본적으로 개인 정보 보호(Privacy-by-Default) 방법을 통합하는 필수 개발 프로세스인 [보안 개발 수명 주기](https://www.microsoft.com/sdl/)를 통해 처음부터 Microsoft Azure에 보안이 기본적으로 제공됩니다. Microsoft 보안 전략의 주요 원칙은 심층 방어 전략이 확장된 "위반 가정"입니다. Microsoft는 Azure의 보안 기능을 지속적으로 개선함으로써 새로운 위협에 앞서나갈 수 있습니다. Azure 보안에 대한 자세한 내용은 다음 [리소스](https://www.microsoft.com/trustcenter/security/azure-security)를 참조하세요.

Microsoft는 Microsoft Azure에 대한 공격 영향력을 완화하기 위해 운영되는 전담 글로벌 연중무휴 인시던트 대응 서비스를 제공하고 있습니다. 여러 보안 및 준수 감사(예: [ISO/IEC 27018](offering-iso-27018.md))를 통해 입증된 결과에 따라, Microsoft는 데이터 센터에서 연중무휴 CCTV 모니터링, 훈련된 보안 직원, 스마트 카드 및 생체 인식 제어를 비롯한 엄격한 운영 및 프로세스를 사용하여 무단 액세스를 방지합니다.

## <a name="detection-of-potential-breaches"></a>잠재적인 위반 감지

최신 클라우드 컴퓨팅의 특성으로 인해, 고객 클라우드 환경에서 발생하는 일부 데이터 침해는 Microsoft Azure 서비스와 관련된 것이 아닙니다. Microsoft는 Azure 서비스에 대해 공유 책임 모델을 사용하여 보안 및 운영 책임을 정의합니다. 클라우드 서비스 공급자와 고객 모두 클라우드 보안 부분에 책임이 있으므로, 클라우드 서비스의 보안을 논의할 때 공동 책임이 중요합니다.

Microsoft는 고객의 책임 영역 내에서 보안 인시던트를 모니터링하거나 대응하지 않습니다. 고객만의 보안 손상은 Azure 보안 인시던트로 처리되지 않으며 고객 테넌트에서 대응 노력을 관리해야 합니다. 적절한 서비스 계약이 있는 경우, 고객 인시던트 대응은 Microsoft Azure [고객 지원](https://azure.microsoft.com/support/options/)과 협력해서 진행될 수 있습니다. 또한 Microsoft Azure는 고객이 보안 인시던트 대응을 개발 및 관리하기 위해 활용할 수 있는 다양한 서비스(예: [Azure Security Center](https://azure.microsoft.com/services/security-center/))도 제공합니다.

Azure는 Microsoft Azure 인시던트 관리 플랜의 하위 집합인 보안 인시던트 대응 프로세스에 따라 잠재적인 데이터 위반에 대응합니다. Microsoft의 Azure 보안 인시던트 대응은 감지, 평가, 진단, 안정화 및 종료의 5단계 프로세스로 구현됩니다. 보안 인시던트 대응 팀은 조사가 진행되면서 진단 및 안정화 단계 간을 전환할 수 있습니다. 보안 인시던트 대응 프로세스의 개요는 다음과 같습니다.

| 단계 | 설명 |
|:------- |------------- |
| ***1: 감지*** | 잠재적인 인시던트의 최초 지표 |
| ***2: 평가*** | 대기 인시던트 대응 팀 구성원이 이벤트의 영향 및 심각도를 평가합니다. 이러한 평가는 증거에 따라 보안 대응 팀으로의 추가 에스컬레이션으로 이어질 수도 있고 그렇지 않을 수도 있습니다. |
| ***3: 진단*** | 보안 대응 전문가는 기술 또는 법정 조사를 수행하고 제약, 완화 및 해결 전략을 파악합니다. 보안 팀에서 고객 데이터가 불법적이거나 권한이 없는 개인에게 노출될 수 있다고 판단하는 경우 고객 인시던트 알림 프로세스가 동시에 실행됩니다. |
| ***4: 안정화 및 복구*** | 인시던트 대응 팀이 문제를 완화하기 위한 복구 계획을 세웁니다. 영향을 받은 시스템을 격리하는 등의 위기 제약 단계가 즉시 진행되거나 진단과 동시에 진행될 수 있습니다. 즉각적인 위험이 지나간 후에 더 장기적인 완화 조치를 계획할 수 있습니다. |
| ***5: 종료 및 사후 분석*** | 인시던트 대응 팀은 정책, 절차 및 프로세스를 수정하여 이벤트 재발을 방지하기 위해 인시던트의 세부 정보를 대략적으로 설명하는 사후 평가를 만듭니다. |

Microsoft Azure에서 사용하는 감지 프로세스는 Azure 서비스의 기밀성, 무결성 및 가용성을 침해하는 이벤트를 검색하도록 고안되었습니다. 다음과 같은 일부 이벤트가 조사를 트리거할 수 있습니다.

- 내부 모니터링 및 경고 프레임워크를 통한 자동화된 시스템 경고. 이러한 경고는 맬웨어 방지, 침입 감지와 같은 서명 기반 경보나 비정상 상황 발생 시 예상되는 활동 및 경고를 프로파일링하도록 고안된 알고리즘을 통해 제공될 수 있습니다.
- 첫 번째 파티는 Microsoft Azure 및 Azure Government에서 실행되는 Microsoft 서비스의 첫 번째 파티 보고서입니다.
- 보안상 취약한 부분은 [문제 보고](https://msrc.microsoft.com/create-report)를 통해 [MSRC(Microsoft 보안 대응 센터)](https://www.microsoft.com/msrc)에 보고됩니다. MSRC는 전 세계의 파트너 및 보안 연구자들과 협력하여 보안 인시던트를 방지하고 Microsoft 제품 보안을 향상시킬 수 있도록 지원합니다.
- 고객은 [고객 지원 포털](https://www.windowsazure.com/support/contact/) 또는 Microsoft Azure 및 Azure Government 관리 포털을 통해 보고하고 Azure 인프라에 기인하는 의심스러운 작업(고객의 책임 범위 내에서 발생하는 작업과는 반대됨)을 설명합니다.
- 보안 [Red 팀 및 Blue 팀](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/) 활동. 이 전략은 공격적 보안 전문가로 구성된 고도로 훈련된 Red 팀을 사용하여 Azure에서 잠재적인 취약점을 밝히고 공격할 수 있습니다. 보안 응답 Blue 팀은 Red 팀의 활동을 감지하고 방어해야 합니다. Azure 보안 대응 노력으로 보안 문제를 효과적으로 관리하는지 확인하는 데 Red 및 Blue 팀 작업이 모두 사용 됩니다. 보안 Red 팀 및 Blue 팀 활동은 고객 데이터 보호를 보장하기 위해 계약 규칙에 따라 운영됩니다.
- Azure 서비스 운영자에 의한 에스컬레이션. Microsoft 직원은 잠재적인 보안 문제를 식별하고 에스컬레이션하기 위한 교육을 받습니다.

## <a name="azures-data-breach-response"></a>Azure의 데이터 위반 대응

Microsoft는 업무에 미치는 영향, 복구 가능성 및 인시던트의 영향 정보를 확인하여 조사 작업에 적절한 우선 순위 및 심각도를 할당합니다. 우선 순위와 심각도는 조사를 진행하는 동안 새롭게 알아낸 사실과 결론에 따라 변경될 수 있습니다. 고객 데이터에 대한 임박하거나 확인된 위험을 수반하는 보안 이벤트는 높은 심각도로 취급되며, 해결 방안을 찾기 위해 24시간 내내 작업이 진행됩니다.

보안 대응 팀은 Microsoft Azure 보안 엔지니어 및 SME와 공조하여 증거를 통한 실제 데이터를 기준으로 이벤트를 분류합니다. 보안 이벤트를 다음과 같이 분류할 수 있습니다.

- **가양성**: 검색 조건을 충족하지만 정상적인 비즈니스 방식의 일부로 확인되며 필터링할 필요가 있는 이벤트입니다. 서비스 팀은 가양성에 대한 근본 원인을 파악하고 필요한 경우에 따라 체계적인 방식으로 처리하여 미세 조정합니다.
- **보안 이벤트**: 시스템, 서비스 및/또는 네트워크에서 공격 시도, 보안 컨트롤 우회 또는 고객 데이터 또는 개인 데이터가 손실, 제거, 변경, 공개 또는 권한 부여 없이 액세스되었을 수 있음을 나타내는 식별되는 문제를 관찰합니다.
- **보안 인시던트/고객 보고 가능 보안/개인 정보 인시던트(CRSPI)**: Microsoft에서 처리하는 동안 고객 데이터 또는 개인 데이터의 우발적 또는 법에 저촉되는 소멸, 손실, 변조, 무단 공개 또는 액세스로 이어지는 확인된(예를 들어 선언된) 보안 침해입니다.
- **개인 정보 이벤트**: Microsoft 개인정보처리방침, 표준 및 컨트롤을 준수하지 않는 등 개인 정보에 의도하지 않은 결과가 발생한, 개인 데이터 또는 데이터 처리에 영향을 주는 보안 이벤트입니다.
- **개인 정보 인시던트/고객 보고 가능 보안/개인 정보 인시던트(CRSPI)**: Microsoft 개인정보처리방침, 표준 및 컨트롤을 준수하지 않는 등 개인 정보에 의도하지 않은 결과가 발생한, 개인 데이터, 데이터 또는 데이터 처리에 영향을 주는 보안 인시던트입니다.

CRSPI가 선언되려면, Microsoft가 고객 데이터에 대한 무단 액세스가 발생했거나 발생했을 가능성이 높고, 알림이 진행되어야 하는 법적 또는 계약 조항이 있음을 확인해야 합니다. 구체적인 고객 영향, 리소스 액세스 및 복구 단계가 공개되면 좋지만 반드시 그럴 필요는 없습니다. 인시던트는 일반적으로 보안 인시던트의 진단 단계가 끝난 후에 CRSPI로 선언됩니다. 그렇지만 모든 관려 정보를 사용할 수 있게 되는 어느 시점에서든 이러한 선언이 진행될 수 있습니다.

Microsoft는 고객 및 비즈니스 위험이 성공적으로 방지되고, 수정 조치가 구현되는지 확인합니다. 필요한 경우 이벤트와 연결된 즉각적인 보안 위험을 해결하기 위한 긴급 완화 단계가 수행됩니다.

또한 Microsoft는 데이터 침해에 대한 내부 사후 평가도 완료합니다. 이 과정의 일부로, 대응 및 운영 절차가 충분한지 평가되고, 보안 인시던트 대응 SOP 또는 관련 프로세스에 필요할 수 있는 모든 업데이트가 파악되고 구현됩니다. 데이터 침해에 대한 내부 사후 평가는 고객이 사용할 수 없는 중대한 기밀 기록입니다. 그렇지만 사후 평가를 요약하여 다른 고객 이벤트 알림에 포함할 수 있습니다. 이러한 보고서는 Azure의 정기 감사 주기의 일부로 검토될 수 있게 외부 감사자에게 제공됩니다.

## <a name="customer-notification"></a>고객 알림

Microsoft는 필요에 따라 데이터 침해 사실을 영향을 받은 고객과 규제 기관에 알립니다. Microsoft은 Azure를 운영하면서 내부 구조를 과도하게 구획화하고 있습니다. 데이터 흐름 로그도 강력해졌습니다. 이러한 설계 방식은 대부분의 인시던트를 구체적인 고객의 범주에 포함할 수 있다는 장점이 있습니다. 이렇게 하는 목적은 데이터 침해 시, 영향을 받은 고객에게 정확하고 실행 가능한 방식으로 시기 적절하게 알리는 것입니다.

CRSPI를 선언한 후에는 빠르게 이동하는 보안 위험을 고려하면서 최대한 신속하게 알림 프로세스가 수행됩니다. 일반적으로 인시던트 조사가 진행되는 동안에 알림 작성 프로세스가 수행됩니다. 고객 알림은 다음 상황을 *제외하고* 위반을 선언한 시점으로부터 72시간 이내에 전달됩니다.

- Microsoft는 알림을 수행하면 다른 고객의 위험이 증가한다고 생각합니다. 예를 들어 통지하는 행위는 침입자에게 정보를 제공하여 교정할 수 없는 상황을 야기할 수 있습니다.
- Microsoft의 법률 부서 및 인시던트 책임 관리자가 조사한 기타 비정상적이거나 극단적인 상황.
- 72시간의 타임라인 동안 일부 인시던트 정보를 남겨둘 수 있습니다. 조사가 진행됨에 따라 이 세부 내용은 고객 및 규제 기관에 제공됩니다.

Microsoft는 알림 프로세스를 과도하게 지연시키지 않으면서 내부 조사를 수행할 수 있도록 하고 최종 사용자 약정을 충족하도록 지원할 수 있는 자세한 정보를 영향 받은 고객에게 제공합니다.

개인 데이터 침해에 대한 알림은 전자 메일을 통해 Microsoft를 포함한 모든 방법으로 영향 받은 고객에게 전달됩니다. 데이터 위반 알림은 Azure Security Center에서 제공하는 보안 담당자 목록으로 전달되며 [구현 지침](/azure/security-center/security-center-provide-security-contact-details)에 따라 구성할 수 있습니다. Azure Security Center에서 연락처 정보가 제공되지 않으면 Azure 구독으로 한 명 이상의 관리자에게 알림이 전송됩니다. 통지가 성공적으로 전달될 수 있도록 각 신청 및 온라인 서비스 포털의 관리 연락처 정보가 올바른지 확인하는 것은 고객의 책임입니다.

Microsoft Azure 또는 Azure Government 팀은 CSS(고객 지원 서비스) 팀원 및 고객 AM(계정 관리자) 또는 TAM(기술 계정 관리자)과 같은 다른 Microsoft 직원에게도 알리도록 선택할 수 있습니다. 이러한 개인은 고객과 밀접하게 관련되어 있는 경우가 많으며 보다 빠른 수정이 이루어지는 데 도움이 될 수 있습니다.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Microsoft Dynamics 365 기본 제공 보안 기능

Microsoft Dynamics 365는 클라우드 서비스 인프라 및 기본 제공 보안 기능을 통해 데이터를 보호하는 보안 조치 및 메커니즘을 사용하여 데이터를 안전하게 유지합니다. 또한 Dynamics 365는 [보안 ID, 데이터 보호, 역할 기반 보안 및 위협 관리](https://www.microsoft.com/trustcenter/security/dynamics365-security) 영역에서 데이터 무결성 및 개인 정보 보호를 보장하는 효율적인 데이터 액세스 및 공동 작업을 제공합니다.

Microsoft Dynamics 365 제품은 데이터 위반 프로세스로부터 보호하기 위해 하나 이상의 Microsoft Azure 서비스 팀이 취하는 기술 및 조직 차원의 동일한 측정 방법을 따릅니다. 따라서 여기에 있는 ‘Microsoft Azure 데이터 위반’ 알림 문서에 설명된 모든 정보는 Microsoft Dynamics 365와 유사합니다.

## <a name="windows-diagnostic-data-processor-configuration"></a>Windows 진단 데이터 프로세서 구성

[Windows 진단 데이터 프로세서 구성](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)은 클라우드 서비스 인프라 및 기본 제공 보안 기능을 통해 데이터를 보호하는 보안 조치 및 메커니즘을 사용하여 데이터를 안전하게 유지합니다.

Windows 진단 데이터 프로세서 구성은 하나 이상의 Microsoft Azure 서비스 팀이 데이터 위반으로부터 보호하기 위해 사용하는 기술 및 조직 차원의 동일한 방법을 따릅니다. 따라서 여기의 ‘Microsoft Azure 데이터 위반’ 알림 문서에 설명된 모든 정보는 Windows 진단 데이터 프로세스 구성과 유사합니다.

## <a name="learn-more"></a>자세한 정보

[Microsoft 보안 센터](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
