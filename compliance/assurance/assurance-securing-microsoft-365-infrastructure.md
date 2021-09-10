---
title: Microsoft 365 인프라 보호
description: Microsoft에서 클라우드 인프라를 보호하는 Microsoft 365 대해 자세히 알아보습니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6c20c62feb1ff3ab23eeb97d5ad11abb5ad85a07
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947381"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Microsoft 365 인프라 보호

Microsoft 365 전 세계 최대 기업 및 소비자 클라우드 서비스 중 하나인 이 서비스는 고객 기반, 제품 및 기능 모두에서 급속도로 성장하고 있습니다. 고객은 Microsoft 365 생산성 솔루션뿐 아니라 지속적으로 진화하는 사이버 위협 환경으로부터 가장 중요한 정보를 보호하는 데 도움을 줍니다. 고객 데이터를 안전하게 보호하고 고객 신뢰를 유지하는 것이 Microsoft의 최우선 과제입니다.

보안이 사후에 진행되는 경우 이러한 규모와 복잡성의 시스템을 보호할 수 없는 경우 초기 디자인 프로세스 중에 보안이 통합된 후에만 효과적입니다. 자동화된 시스템과 고도로 숙련된 엔지니어의 프롬프트 응답이 있는 강력한 위협 감지 시스템이 필요합니다. 이러한 시스템의 지속적인 평가 및 유효성 검사는 보안 구성이 그대로 유지되고 이전에 알려지지 않은 취약점이 식별되도록 하는 데 필수적입니다.

## <a name="core-security-principles"></a>핵심 보안 원칙

7개의 보안 원칙은 위협으로부터  Microsoft 365 서비스를 보호하고, 위협을  감지 및 대응하고, 해당 평가  결과에 따라 보안 상태를 지속적으로 평가하고 서비스를 개선하는 프레임워크의 토대를 마련합니다.

- **데이터 개인 정보** 보호: 고객이 데이터를 소유하고 있으며 Microsoft는 관리인입니다. Microsoft 365 서비스는 고객이 명시적으로 요청하고 승인하지 않는 한 엔지니어가 고객 데이터에 액세스하지 않고 작동하도록 디자인되었습니다.
- **위반 가정:** 직원 및 서비스는 손상이 실제 가능성이 있는 것으로 취급됩니다.
- **최소 권한:** 리소스에 대한 액세스 및 사용 권한은 필요한 작업을 수행하는 데 필요한 권한으로만 제한됩니다.
- **위반 경계:** 한 경계의 ID 및 인프라가 다른 경계의 리소스와 격리됩니다. 한 경계가 손상되면 다른 경계가 손상되지 않습니다.
- **서비스 패브릭 통합 보안:** 보안 우선 순위 및 요구 사항이 새로운 기능 디자인에 기본 제공되어 각 서비스를 통해 강력한 보안 자세가 확장됩니다.
- **자동화** 및 자동: Microsoft는 지능적으로 자동으로 서비스 보안을 적용할 수 있는 지속형 제품 및 아키텍처를 개발하는 동시에 Microsoft 엔지니어가 대규모로 보안 위협에 대한 대응을 안전하게 관리할 수 있는 기능을 제공합니다.
- **적응형 보안:** Microsoft 보안 기능은 기계 학습 모델, 일상적인 침투 테스트 및 자동화된 평가를 통해 조정되고 향상됩니다.

## <a name="protection"></a>보호

### <a name="access-control"></a>액세스 제어

기본적으로 Microsoft 365 서비스를 개발하고 유지 관리하는 담당자는 서비스 인프라에 ZSA(Zero Standing Access)가 있습니다. Microsoft는 최상의 엔지니어만 고용하고 엄격한 백그라운드 검사가 필요하기는 하지만 Microsoft는 운영 서비스에서 기본적으로 신뢰할 수 있는 것으로 가정하지 않습니다. 또한 엔지니어가 권한 있는 액세스가 승인되면 특정 서비스 인프라 범위에 필요한 작업만 수행할 수 있도록 제한된 기간 동안만 액세스 권한이 부여됩니다. Microsoft는 이러한 정책을 Lockbox라는 시스템을 통해 구현되는 JIT(Just-In-Time) 및 JEA(Just-Enough-Access)라고 합니다.

관리자 권한 획득을 위해 Microsoft 엔지니어는 특정 작업에 대한 요청을 제출하고 이를 수행할 기간을 지정합니다. 승인되면 Lockbox는 요청된 작업만 수행할 수 있는 특수 JIT 계정을 생성합니다. 작업은 일반적으로 필요한 문제 해결 또는 복구를 안전하게 수행하는 자동화된 워크플로 형식을 취합니다. 인프라에 대한 직접 액세스가 필요한 경우는 드물지만 엄격하게 모니터링되는 PAW(Privileged Access Workstation)가 필요합니다.

Rogue 사용자 및 손상된 계정은 모든 조직에서 실제 가능성이 있으며, 액세스 제어 시스템은 이러한 위협으로부터 보호하도록 디자인되어 있습니다.

액세스 제어에 대한 자세한 내용은 ID 및 액세스 관리 개요 [를 참조하세요.](assurance-identity-and-access-management.md)

### <a name="encryption"></a>암호화

액세스 제어는 Microsoft 365 보호하는 데 중요한 역할을 하지만 데이터 수명 주기 동안 암호화를 사용하여 Microsoft 고객의 기밀성 및 개인 정보를 추가로 보호합니다.

클라이언트 컴퓨터, Microsoft 365 서버 및 Microsoft 365 서버 간에 전송되는 데이터는 TLS 1.2를 사용하여 암호화됩니다. 사용 가능한 경우 향상된 프로토콜을 추가하고 필요한 경우 약한 프로토콜을 제거하여 사용 가능한 암호 및 프로토콜을 정기적으로 검토합니다.

Microsoft 서버의 미사용 고객 콘텐츠는 BitLocker를 사용하여 볼륨 수준에서 암호화됩니다. 응용 프로그램 수준 암호화는 Microsoft 또는 고객이 관리하는 키를 사용하여 추가로 적용할 수 있습니다. Microsoft 관리 키에 대한 액세스는 JIT 및 JEA 프로세스를 통해 승인되고 승인된 경우만 가능합니다.

암호화의 암호화에 대한 Microsoft 365 암호화 및 키 관리 [개요를 참조하세요.](assurance-encryption.md)

### <a name="network-isolation"></a>네트워크 격리

최소 권한의 원칙에 따라 Microsoft 365 인프라의 여러 부분 간의 통신을 작동에 필요한 것으로만 제한합니다. 모든 네트워크 트래픽은 기본적으로 거부되고 명시적으로 정의된 통신만 허용됩니다. 이 제한은 인프라 전체에서 위반 경계를 설정합니다. Teams 기능을 수용하기 위해 새 네트워크 경로를 추가하려면 요청을 열기 전에 먼저 평가 및 승인해야 합니다.

네트워크의 네트워크 Microsoft 365 대한 자세한 내용은 Microsoft 365 [참조하세요.](/microsoft-365/enterprise/microsoft-365-isolation-controls)

## <a name="detection--response"></a>검색 & 응답

### <a name="security-monitoring"></a>보안 모니터링

Microsoft의 대규모 보안 모니터링은 자동화된 클라우드 기반 솔루션을 사용하여 매우 정확한 경고를 생성해야만 가능합니다. 핵심 인프라 전체에서 수집된 각 서비스 및 원격 분석 데이터의 감사 로그는 거의 실시간에 가까운 중앙 집중식 처리 및 경고 솔루션으로 전송됩니다.

검색된 위협은 가능한 경우 자동으로 트리거된 작업을 사용하여 수정됩니다. 자동화된 솔루션이 문제를 해결하지 못하거나 해결하지 못하면 Microsoft 엔지니어가 즉시 조치를 취하여 위협을 완화합니다.

보안 모니터링의 보안 모니터링에 대한 자세한 Microsoft 365 보안 모니터링 [개요를 참조하세요.](assurance-security-monitoring.md)

## <a name="assessment"></a>평가

### <a name="automated-assessments"></a>자동화된 평가

시스템 설계 방식에 관계없이 시간이 경과하면 의도적인 의도치 않은 구성 드리프트로 인해 보안이 저하될 수 있습니다. 자동화된 도구는 Microsoft 365 잘못 구성한 서비스를 찾아서 시스템과 시스템을 지속적으로 평가합니다. 이 평가를 패치, 바이러스 백신, 취약성 및 PAVC(구성 검사)라고도 합니다.

또한 아키텍처의 유효성을 검사하여 사용되지 않는 열린 포트와 같은 인스턴스 및 관리자 액세스 권한이 있는 계정을 식별합니다. 미리 정의된 원하는 상태로부터 드리프트된 서비스는 자동으로 다시 정렬됩니다.

보안 모니터링의 보안 모니터링에 대한 자세한 Microsoft 365 취약성 관리 [개요를 참조하세요.](assurance-vulnerability-management.md)

### <a name="attack-simulation-and-penetration-testing"></a>공격 시뮬레이션 및 침투 테스트

Microsoft 365 가장 우선 순위는 공격이 방어에 침투하지 못하게 하는 것입니다. Microsoft 365 이전에 알려지지 않은 취약점을 식별하고 보안 모니터링 기능을 개선하기 위해 다양한 데이터의 일정 스트림을 제공하기 위해 시뮬레이트된 공격을 지속적으로 수행하고 있는 보안 전문가의 전담 팀이 있습니다. 이러한 시뮬레이션된 공격은 자주 자동화된 소규모 공격과 전문가 중심 심층 분석의 형태를 취합니다. 이러한 활동에서 Microsoft는 공격자 감지, 대응 및 지우기 기능을 평가합니다.

에서 보안 모니터링에 대한 자세한 Microsoft 365 에서 [공격 시뮬레이션을 Microsoft 365.](assurance-monitoring-and-testing.md)

## <a name="resources"></a>리소스

[비하인드 스토리: Microsoft 365 서비스를 지원하는 인프라 보안](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
