---
title: 'Microsoft 보안 인시던트 관리: 인시던트 사후 활동'
description: 이 문서에서는 Microsoft 온라인 서비스의 보안 인시던트 관리 사후 작업 프로세스에 대해 간략하게 소개합니다.
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
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377535"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Microsoft 보안 인시던트 관리: 인시던트 사후 활동

## <a name="postmortem"></a>Postmortem

일부 보안 인시던트, 특히 고객에 영향을 미치거나 데이터 위반으로 인해 발생한 인시던트는 전체 인시던트 사후 대응의 대상이 됩니다. 보안 대응 팀은 다음에 대한 보안 인시던트 대응과 관련된 모든 당사자와 자세한 사후 대응을 실시합니다.

- 인시던트가 발생된 이벤트 시퀀스를 문서화합니다.
- 위반에 관련된 배우가 포함된 증거(알려진 경우)에서 지원되는 인시던트의 기술 요약을 작성합니다. 이 요약에는 응답이 실행된 방법 및 기타 키가 포함됩니다.
- 기술 경과, 절차적 오류, 수동 오류, 프로세스 결함 및 통신 결함 및/또는 보안 인시던트 대응 중에 식별된 이전에 알려지지 않은 공격 벡터를 식별합니다.

사후 처리는 Microsoft 온라인 서비스 엔지니어링 개발 주기에서 새로운 우선 순위를 설정하여 Microsoft 온라인 서비스 개선, 운영 프로세스 및 설명서에 직접적인 영향을 줍니다.

## <a name="documentation"></a>설명서

사후 프로세스에서 발견된 모든 주요 기술 결과는 버그 또는 개발 변경 요청의 형태로 보고서 및 서비스 투자 또는 수정에 캡처됩니다. 이러한 결과는 적절한 엔지니어링 팀과 함께 수행됩니다. 프로세스 오류 및 조직 간 문제의 경우 보안 대응 팀의 데이터베이스에 문제점이 문서화되어 있으며 해당 그룹과 함께 문제를 해결합니다.

## <a name="process-improvement"></a>프로세스 개선

Microsoft 온라인 서비스의 보안 인시던트에 대응하기 위해 Microsoft 내의 여러 조직에 분산된 여러 그룹과의 조율 및 잠재적으로 법률 집행과 같은 적절한 외부 조직과의 조율이 수반됩니다. 모든 보안 인시던트 이후의 대응을 평가하여 충분하고 완전한 대응을 평가하는 것이 중요합니다. 확인된 개선 또는 변경에 대해 보안 대응 팀은 해당 팀 및 이해 관계자와 협의하여 제안 사항을 평가하고 적절한 경우 해당 제안을 표준 운영 절차에 통합합니다. 보안 인시던트 대응 또는 사후 작업 중에 식별된 모든 필수 변경 사항, 버그 또는 서비스 개선 사항은 내부 Microsoft 엔지니어링 데이터베이스에 기록 및 추적됩니다. 모든 잠재적인 버그 또는 기능이 적절한 소유자에게 할당됩니다. Microsoft 보안 대응 팀은 문제가 해결될 때까지 모든 항목을 검토합니다.

## <a name="related-articles"></a>관련 문서

- [Microsoft 보안 인시던트 관리](assurance-security-incident-management.md)
- [Microsoft 보안 인시던트 관리: 준비](assurance-sim-preparation.md)
- [Microsoft 보안 인시던트 관리: 검색 및 분석](assurance-sim-detection-analysis.md)
- [Microsoft 보안 인시던트 관리: 포함, 삭제 및 복구](assurance-sim-containment-eradication-recovery.md)
- [보안 이벤트 지원 티켓을 기록하는 방법](/azure/security/fundamentals/event-support-ticket)
- [Azure 및 Dynamics 365 GDPR의 위반 알림](/compliance/regulatory/gdpr-breach-azure-dynamics)
