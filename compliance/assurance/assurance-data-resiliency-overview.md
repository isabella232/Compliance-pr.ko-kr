---
title: Microsoft 365의 데이터 복구
description: 이 문서에서는 Microsoft 365의 데이터 복구 및 복구 디자인 및 원칙에 대해 자세히 알아보고 있습니다.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 361400bf6330fb82d34f384d17e4d4ee438ccf08
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012904"
---
# <a name="data-resiliency-in-microsoft-365"></a>Microsoft 365의 데이터 탄력성

클라우드 컴퓨팅의 복잡한 특성을 통해 Microsoft는 문제가 될 경우가 아니라 문제가 될 경우를 염두에 두게 됩니다. 클라우드 서비스를 디자인하여 안정성을 극대화하고 문제가 발생하면 고객에게 부정적인 영향을 최소화합니다. 복잡한 물리적 인프라를 활용하는 기존 전략을 넘어서 클라우드 서비스에 직접 중복을 구축했습니다. 데이터 탄력성을 서비스에 구축하고 고객에게 고가용성을 제공하는 덜 복잡한 물리적 인프라와 보다 지능적인 소프트웨어의 조합을 사용했습니다.

## <a name="resiliency-and-recoverability-are-built-in"></a>복구 및 복구 가능성은 기본 제공

복구 및 복구를 구축하는 과정은 하드웨어(인프라)가 실패하고, 사람이 실수하고, 소프트웨어에 버그가 있는 경우를 가정하고 시작해야 합니다. 소프트웨어 개발자가 클라우드 전에 이러한 문제에 대해 생각하지 않았다고 말하면 틀리지만 일반적인 IT 구현에서 이러한 문제를 처리하는 방식은 클라우드 이전과 달랐습니다.

- 첫째, 하드웨어 및 인프라 보호가 중요했습니다. 이 구조는 99.99%의 안정성을 갖는 데이터 센터가 필요하며, 서버는 하드웨어 기반 클러스터링, 이중 전원 공급 장치, 이중 네트워크 인터페이스 등에서 구현되었습니다.
- 둘째, 프로세스가 가장 주관적입니다. 운영 팀은 엄격한 절차를 유지 관리하고, 변경 창을 사용하며, 종종 상당한 프로젝트 관리 오버헤드가 일어났습니다.
- 셋째, 빠른 속도로 배포가 진행된 것입니다. 소스를 소유하지 않고 코드를 배포하면 패치 릴리스를 기다리는 의미가 있으며 주 버전 릴리스에는 하드웨어 교체 및 상당한 자본 부과가 포함되었습니다. 또한 문제를 수정하는 유일한 방법은 롤백하는 것입니다. 따라서 대부분의 IT 조직에서는 최신 작업을 유지하기 위해 주요 릴리스만 배포합니다.
- 마지막으로 배포된 시스템의 규모와 상호 연결 수준은 지금까지는 현재보다 훨씬 더 작습니다.

오늘날 고객은 품질을 하하지 않고 Microsoft의 지속적인 혁신을 기대하며 이는 Microsoft의 서비스 및 소프트웨어가 복구력과 복구 기능을 염두에 두는 이유 중 하나입니다.

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365 데이터 탄력성 원칙

복구는 클라우드 기반 서비스가 특정 유형의 장애를 견디고 고객의 관점에서 완전하게 작동할 수 있는 능력을 지어보는 것입니다. 데이터 복구는 Microsoft 365 내에서 발생하는 오류에 상관없이 중요한 고객 데이터는 그대로 유지되는 것을 의미하며 영향을 받지 않습니다. 이를 위해 Microsoft 365 서비스는 5개의 특정 탄력성 원칙에 따라 설계됩니다.

- 중요 및 중요하지 않은 데이터가 있습니다. 중요하지 않은 데이터(예: 메시지를 읽은지 여부)는 드물게 실패 시나리오에서 삭제될 수 있습니다. 중요한 데이터(예: 전자 메일 메시지와 같은 고객 데이터)는 극단적인 비용으로 보호해야 합니다. 디자인 목표로 배달된 메일 메시지는 항상 중요하며 메시지를 읽은 경우와 같은 메시지가 중요하지 않은지 여부도 중요합니다.
- 고객 데이터의 복사본을 서로 다른 장애 영역 또는 가능한 한 많은 장애 도메인(예: 단일 자격 증명(프로세스, 서버 또는 운영자)에서 액세스할 수 있는 데이터 센터)로 분리하여 오류 분리를 제공해야 합니다. 
- 중요한 고객 데이터는 Atomicity, Consistency, Isolation, 내구성(ACID)의 일부에 실패하는지 모니터링해야 합니다.
- 고객 데이터는 손상으로부터 보호되어야 합니다. It must be actively scanned or monitored, repairable, and recoverable.
- 대부분의 데이터 손실은 고객 작업으로 인한 결과로, 고객이 실수로 삭제된 항목을 복원할 수 있도록 하는 GUI를 사용하여 자체 복구할 수 있도록 합니다.

강력한 테스트 및 유효성 검사와 함께 이러한 원칙에 대한 클라우드 서비스를 구축함으로써 Microsoft 365는 지속적인 혁신과 개선을 위한 플랫폼을 보장하면서 고객의 요구 사항을 충족하고 초과할 수 있습니다.

## <a name="related-articles"></a>관련 문서

- [데이터 손상 처리](assurance-dealing-with-data-corruption.md)
- [맬웨어 및 랜섬웨어 보호](assurance-malware-and-ransomware-protection.md)
- [모니터링 및 자동 복구](assurance-monitoring-and-self-healing.md)
- [Exchange 데이터 탄력성](assurance-exchange-data-resiliency.md)
