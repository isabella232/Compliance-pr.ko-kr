---
title: 'Microsoft 365 보안 인시던트 관리: 검색 및 분석'
description: 이 문서에서는 Microsoft 365의 보안 인시던트 관리 감지 및 분석 프로세스에 대한 개요를 제공합니다.
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
ms.openlocfilehash: 433b8da98e25c4f465473143074eda055419234d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497400"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Microsoft 365 보안 인시던트 관리: 검색 및 분석

악의적인 활동을 감지하기 위해 Microsoft 365는 보안 이벤트 및 기타 데이터를 중앙에서 기록하고 다양한 분석 기술을 수행하여 이상하거나 의심스러운 활동을 검색합니다. 로그 파일은 Microsoft 365 서버 및 인프라 장치에서 수집되고 중앙 및 통합 데이터베이스에 저장됩니다.

Microsoft는 악의적인 활동을 감지하는 위험 기반 접근 방식을 제공합니다. 인시던트 데이터 및 위협 인텔리전스를 사용하여 검색을 정의하고 우선 순위를 지정합니다.

숙련된 숙련된 숙련된 사용자로 된 팀을 고용하는 것은 검색 및 분석 단계에서 성공하기 위한 가장 중요한 기조 중 하나입니다. Microsoft 365는 여러 서비스 팀을 사용하며, 이러한 팀에는 네트워크, 라우터, 방화벽, 부하 균형 조정기, 운영 체제 및 응용 프로그램을 포함하여 스택 내의 모든 구성 요소에 대한 역량이 있는 직원이 포함됩니다.

Microsoft 365의 보안 검색 메커니즘에는 다양한 원본에서 시작된 알림 및 알림도 포함됩니다. Microsoft 365 보안 대응 팀은 보안 인시던트 에스컬레이션 프로세스의 주요 오케스트레이터입니다. 이 팀은 모든 에스컬레이터를 받고 보안 인시던트의 유효성을 분석하고 확인하는 업무를 담당합니다.

검색의 기본 기조 중 하나는 알림입니다.

- 각 서비스 팀은 Microsoft 365 보안 팀의 요구 사항에 따라 서비스 내부의 작업 또는 이벤트를 기록할 책임이 있습니다. 서로 다른 서비스 팀에서 만든 모든 로그는 미리 정의한 보안 및 검색 규칙을 사용하여 SIEM(보안 정보 및 이벤트 관리) 솔루션에서 처리됩니다. 이러한 규칙은 이전 보안 인시던트에서 학습된 정보에 따라 Microsoft 365 보안 팀의 권장에 따라 진화하여 의심스러우거나 악의적인 활동이 있는지 여부를 판단합니다.
- 고객이 보안 인시던트가 진행 중이라 판단할 경우 Microsoft와 함께 지원 사례를 열 수 있습니다. Microsoft 365 CxP(고객 환경) 커뮤니케이션 팀에 할당되어 모든 적절한 팀으로 에스컬레이터로 변경됩니다.

Microsoft 365 서비스 팀은 보안 모니터링 및 로깅을 통해 추세 분석에서 얻은 인텔리전스를 사용하여 공격 또는 보안 인시던트가 표시될 수 있는 Microsoft 365 정보 시스템의 비정상을 감지합니다. Microsoft 365 서버는 프로덕션 환경의 이러한 로그에서 중앙 로깅 서버로 출력을 집계합니다. 이 중앙 로깅 서버에서는 프로덕션 환경 전체의 추세를 파악하기 위해 로그를 검사합니다. 중앙 집중식 서버에 집계된 데이터는 고급 쿼리, 대시보드 작성 및 변이 및 악의적인 활동 감지를 위해 로깅 서비스로 안전하게 전송됩니다. 또한 이 서비스는 기계 학습을 사용하여 로그 출력에서 이 문제를 검색합니다.

에스컬레이터 단계에서 보안 인시던트의 특성에 따라 Microsoft 365 보안 대응 팀은 Microsoft의 여러 팀에서 하나 이상의 주제 전문가를 참여할 수 있습니다.

- 온라인 서비스 보안 및 규정 준수 팀
- MSTIC(Microsoft Threat Intelligence Center)
- MSRC(Microsoft Security Response Center)
- CELA(회사, 외부 및 법률 업무)
- Azure Security
- Microsoft 365 엔지니어링 및 기타.

Microsoft 365 보안 대응 팀으로의 에스컬레이터가 발생하기 전에 서비스 팀은 다음과 같은 정의된 기준에 따라 보안 인시던트의 심각도 수준을 결정하고 설정해야 합니다.

- 개인 정보
- 영향
- 범위
- 영향을 받는 테넌트 수
- Region
- 서비스
- 인시던트 세부 정보
- 특정 고객 산업 또는 시장 규정.

인시던트 우선 순위는 인시던트의 기능 영향, 인시던트의 정보 영향 및 인시던트로부터의 복구 가능성 등 고유한 요인을 사용하여 결정됩니다.

보안 인시던트에 대한 에스컬레이터를 받은 후 Microsoft 365 보안 팀은 Microsoft 365 보안 대응 팀, 서비스 팀 및 Microsoft 365 인시던트 커뮤니케이션 팀의 구성원으로 구성된 가상 팀(v-team)을 구성합니다. 이 v-team의 활동에서 더 복잡한 부분은 보안 인시던트와 가짓 긍정을 제거하는 것입니다. 준비 단계에서 결정된 표시기에서 제공하는 정보의 정확성이 중요합니다. v-team은 벡터 공격 범주별로 이 정보를 분석하여 보안 인시던트가 합법적인 문제인지 확인할 수 있습니다.

조사 시작 시 Office 보안 인시던트 대응 팀은 사례 관리 정책에 따라 인시던트에 대한 모든 정보를 기록합니다. 사례가 진행될 때 당사는 지속적인 작업을 추적하고 인시던트 수명 주기 동안 이 데이터를 수집, 보존 및 보호하기 위한 증거 처리 표준을 준수합니다.

이러한 작업의 몇 가지 예는 다음과 같습니다.

- 인시던트 및 잠재적인 영향에 대한 간략한 설명을 요약합니다.
- 인시던트의 심각도 및 우선 순위는 잠재적인 영향을 평가하여 파생됩니다.
- 인시던트 감지를 이행한 식별된 모든 표시기 목록
- 관련 인시던트 목록
- v-team에서 수행한 모든 작업 목록
- 모의 후 분석 및 향후 포렌식 조사를 위해 보존될 수집된 증거
- 권장되는 다음 단계 및 작업

보안 인시던트 확인 후 Microsoft 365 보안 대응 팀과 적절한 서비스 팀의 기본 목표는 공격을 방지하고, 공격으로부터 서비스를 보호하고, 전역적으로 더 큰 영향을 받지 않도록 하는 것입니다. 이와 동시에 적절한 엔지니어링 팀은 근본 원인을 파악하고 첫 번째 복구 계획을 준비합니다.

다음 단계에서 Microsoft 365 보안 대응 팀은 보안 인시던트의 영향을 받는 고객을 식별합니다(있는 경우). 효과 범위는 지역, 데이터 센터, 서비스, 서버 팜, 서버 등에서 결정하는 데 시간이 걸릴 수 있습니다. 영향을 받는 고객 목록은 서비스 팀과 Microsoft 365 CxP Communications 팀에서 컴파일한 다음 계약 및 규정 준수 의무 내에서 고객 알림 프로세스를 처리합니다.

## <a name="related-articles"></a>관련 문서

- [Microsoft 365 보안 인시던트 관리](assurance-security-incident-management.md)
- [Microsoft 365 보안 인시던트 관리 준비](assurance-sim-preparation.md)
- [Microsoft 365 보안 인시던트 관리 포함, 지우기 및 복구](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 보안 인시던트 관리 사후 활동](assurance-sim-post-incident-activity.md)
