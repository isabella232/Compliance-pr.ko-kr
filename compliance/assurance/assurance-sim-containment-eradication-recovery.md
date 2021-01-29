---
title: 'Microsoft 365 보안 인시던트 관리: 포함, 지우기 및 복구'
description: 이 문서에서는 Microsoft 365의 보안 인시던트 관리 포함, 지우기 및 복구 프로세스에 대한 개요를 제공합니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037638"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Microsoft 365 보안 인시던트 관리: 포함, 지우기 및 복구

Microsoft 365 보안 대응 팀, 서비스 팀 및 기타에서 수행한 분석에 따라 보안 인시던트의 영향을 최소화하기 위해 적절한 포함 및 복구 계획을 개발합니다. 그런 다음 적절한 서비스 팀은 Microsoft 365 보안 대응 팀의 지원을 통해 프로덕션에서 해당 계획을 적용합니다.

## <a name="containment"></a>포함

보안 인시던트가 검색된 후 공격이 더 많은 리소스에 액세스하거나 더 많은 손상을 발생하기 전에 침입을 포함하는 것이 중요합니다. 보안 인시던트 대응 절차의 주요 목표는 고객 또는 해당 데이터 또는 Microsoft 시스템, 서비스 및 응용 프로그램에 대한 영향을 제한하는 것입니다.

## <a name="eradication"></a>지우기

지우기 프로세스는 높은 수준의 신뢰도로 보안 인시던트의 근본 원인을 제거하는 프로세스입니다. 목표는 다음 두 가지입니다.

- 환경에서 역행위를 완전히 제거하기 위해
- 를 사용하여 환경을 다시 활성화하거나 활성화할 수 있는 취약성(알려진 경우)을 완화합니다.

인시던트의 특성, 보안 인시던트의 범위, 침투의 깊이 및 가능한 상황에 따라 Microsoft 365 보안 대응 팀은 서비스 팀이 지우기 기술을 채택하는 것이 좋습니다. 이러한 삭제 단계로 인해 발생할 수 있는 잠재적인 비즈니스 영향을 고려하면 서비스 팀과 Microsoft 365 보안 대응 팀이 임원 인시던트 관리자의 자세한 분석 및 승인(필요한 경우)을 수행한 후에 이러한 결정을 내릴 수 있습니다.

## <a name="recovery"></a>복구

응답 팀이 적대적이 환경에서 제거되고 알려진 모든 취약한 경로를 제거했다는 확신이 타당해지자 개별 서비스 팀은 복원 단계를 시작하여 서비스를 알려진 양호한 구성으로 되살리게 됩니다. 이러한 복원 단계는 Microsoft 365 보안 대응 팀과 협의합니다. 이 활동에는 마지막으로 알려진 서비스의 양호한 상태를 식별하고, 백업에서 이 상태로 복원하고, 복원된 상태의 취약한 공격 경로를 검사하는 등의 작업을 포함합니다. Microsoft 365 보안 대응 팀은 서비스 팀과 협의하여 환경에 가장 적합한 복구 계획을 결정할 것입니다.

복구의 주요 측면은 복구 계획이 성공적으로 실행되고 환경에 위반의 징후가 없는지 확인할 수 있는 향상된 보안 및 제어 기능을 준비하는 것입니다.

## <a name="customer-notification-of-security-incident"></a>보안 인시던트에 대한 고객 알림

Microsoft에서 보안 인시던트가 발생했다고 판단할 경우 부적당하게 지연되고 계약 및 규정 준수 요구 사항 내에서 사용자에게 알릴 것입니다. 영향을 받는 모든 테넌트 식별 후 Microsoft 365 CxP(사용자 환경) 커뮤니케이션 팀은 영향을 받는 테넌트에 적용될 수 있는 관련 규정을 식별하기 위해 작업합니다. Microsoft 365 CxP Communications 팀은 해당 규정에 정의된 적절한 통신 채널을 사용하여 적절한 테넌트 담당자에게 알릴 수 있습니다.

알림에는 인시던트에 대한 설명, 고객 데이터에 대한 영향, Microsoft에서 취한 작업, 고객이 문제를 해결하고 재발을 방지하기 위해 취할 수 있는 제안된 조치 등 인시던트에 대한 자세한 정보가 포함됩니다. 알림은 Microsoft 365 테넌트의 지정된 관리자에게 전달됩니다. 알림을 수신하려면 관리자가 테넌트 프로필에서 정확한 연락처 정보를 제공하고 유지 관리해야 합니다. 또한 인시던트의 특성에 따라 Microsoft 365 서비스 상태 대시보드를 통해 고객에게 알림을 전달할 수도[있습니다.](http://status.yammer.com/)

## <a name="related-articles"></a>관련 문서

- [Microsoft 365 보안 인시던트 관리](assurance-security-incident-management.md)
- [Microsoft 365 보안 인시던트 관리 준비](assurance-sim-preparation.md)
- [Microsoft 365 보안 인시던트 관리 감지 및 분석](assurance-sim-detection-analysis.md)
- [Microsoft 365 보안 인시던트 관리 인시던트 사후 활동](assurance-sim-post-incident-activity.md)
