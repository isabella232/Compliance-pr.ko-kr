---
title: Microsoft 365 서비스 거부 방어 전략
description: 이 문서에서는 DoS(서비스 거부) 공격에 대한 Microsoft 방어 전략에 대한 개요를 확인할 수 있습니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
hideEdit: true
ms.openlocfilehash: 56888f704d3cc5da5e820e3cb80a3d10cbb1ef95
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481880"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Microsoft 365 서비스 거부 방어 전략

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>서비스 거부(Dos) 공격에 대한 보안 핵심 원칙

네트워크 기반 DoS(서비스 거부) 공격을 방어할 때에는 보호, 탐지 및 완화의 세 가지 주요 원칙이 있습니다. 감지가 발생하기 전에 감지가 발생하고 완화가 시작되기 전에 감지가 발생해야 합니다. 작은 DoS 공격도 잘 수 없는 경우 서비스가 공격이 감지될 만큼 오래 지속되지 않습니다. 시스템이 압도되기 전에 공격을 감지하여 방어자는 대응 계획을 구현할 수 있습니다.

다음 수식은 DoS 공격에 영향을 미치는 시간을 대략화하는 데 도움이 됩니다.

  **Maximum Capacity (in bytes/sec) / Growth Rate (bytes/sec) = Time to Impact (in sec)**

검색 시간이 영향을 미치는 시간보다 길면 DoS 공격에 성공할 수 있습니다. 감지 시간이 영향을 미치는 시간보다 짧을 경우 공격된 서비스는 완화 전략이 성공적이면 온라인 상태로 유지 및 액세스 가능해야 합니다.

따라서 DoS 공격을 방어하는 두 가지 기본 전략이 있습니다.

- 최대 용량의 최대값을 높이기 위해 용량을 늘려(공격을 감지하는 데 더 많은 시간이 제공) 또는
- 공격 감지 시간을 줄입니다.

Microsoft 클라우드 서비스를 사용할 때의 한 가지 보안 이점은 대규모 서비스에서 클라우드 Microsoft 서비스 효과적인 방식으로 강력한 네트워크 보호를 제공하는 방식입니다. 대규모에서도 완화, 탐지 및 완화 간에 균형을 유지해야 합니다. 이러한 균형을 찾기 위해 Microsoft는 증가율을 공격하여 얼마나 많은 Microsoft 서비스 해야 하는지 예측합니다.

## <a name="denial-of-service-defense-strategy"></a>서비스 거부 방어 전략

네트워크 기반 DoS 공격을 방어하는 Microsoft의 전략은 규모와 글로벌 공간 때문에 고유합니다. 이 확장을 통해 Microsoft는 대부분의 다른 조직에서 사용할 수 없는 전략과 기술을 활용할 수 있습니다. DoS 전략의 초석은 글로벌 현재 상태입니다. Microsoft는 전 세계 인터넷 공급자, 피어링 공급자(공용 및 개인) 및 개인 기업과 함께 일합니다. 이 계약은 Microsoft에 상당한 인터넷 기능을 제공하며 Microsoft가 넓은 표면 영역에 대한 공격을 흡수할 수 있도록 합니다.

시간이 지날 때 Microsoft의 에지 용량이 커지자 개별 가장자리에 대한 공격의 중요성은 크게 줄어 났습니다. 이러한 감소로 Microsoft는 DoS 방지 시스템의 검색 및 완화 구성 요소를 분리했습니다. Microsoft는 에지 노드에서 전역 완화를 유지하면서 채도 지점에 가깝게 공격을 감지하기 위해 지역별 데이터 센터에 다층 계층 검색 시스템을 배포합니다. 이 전략은 여러 동시 Microsoft 서비스 처리할 수 있도록 합니다.

DoS 공격에 대해 Microsoft에서 가장 효과적이고 저렴한 방어 중 하나는 서비스 공격 표면을 줄이는 것입니다. 원치 않는 트래픽은 데이터를 인라인으로 분석, 처리 및 스크러빙하는 대신 네트워크 에지에서 삭제됩니다.

공용 네트워크와의 인터페이스에서 Microsoft는 방화벽, 네트워크 주소 변환 및 IP 필터링 기능에 특수 용도의 보안 장치를 사용합니다. 또한 Microsoft는 ECMP(Global equal-cost multi-path) 라우팅을 사용 합니다. 전역 ECMP 라우팅은 서비스에 도달할 전역 경로가 여러 개 있도록 하는 네트워크 프레임워크입니다. 각 서비스에 대한 여러 경로를 사용하여 DoS 공격은 공격이 시작된 지역으로 제한됩니다. 최종 사용자는 다른 경로를 사용하여 해당 지역의 서비스에 도달할 수 있는 다른 지역은 공격의 영향을 받지 않습니다. Microsoft는 또한 흐름 데이터, 성능 메트릭 및 기타 정보를 사용하여 DoS 공격을 빠르게 감지하는 내부 DoS 상관 관계 및 검색 시스템을 개발했습니다.

클라우드 서비스를 더욱 보호하기 위해 Microsoft 365 지속적인 모니터링 및 침투 테스트 프로세스에 기본 제공되는 분산된 DDoS(서비스 거부) 방어 시스템을 Microsoft Azure 사용합니다. Azure DDoS 방어 시스템은 외부 공격을 견디기 위해 설계될 뿐만 아니라 다른 Azure 테넌트의 공격도 방어하도록 디자인됩니다. Azure는 SYN 쿠키, 속도 제한 및 연결 제한과 같은 표준 감지 및 완화 기술을 사용하여 DDoS 공격으로부터 보호합니다. 자동화된 보호를 지원하기 위해 워크로드 DoS 인시던트 대응 팀은 팀 전체의 역할과 책임, 에스컬레이터 기준 및 영향을 받는 팀 전체의 인시던트 처리 프로토콜을 식별합니다.

대상에 대해 시작된 대부분의 DoS 공격은 OSI(Open [Systems Interconnection)](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) 모델의 네트워크(L3) 및 전송(L4) 계층에 있습니다. L3 및 L4 계층을 위한 공격은 공격 트래픽이 있는 네트워크 인터페이스 또는 서비스를 넘쳐 리소스를 과도하게 사용하며 합법적인 트래픽에 대응할 수 있는 기능을 거부하도록 디자인되었습니다. L3 및 L4 공격으로부터 보호하기 위해 Microsoft의 DoS 솔루션은 데이터 센터 라우터의 트래픽 샘플링 데이터를 사용하여 인프라와 고객 목표를 보호합니다. 트래픽 샘플링 데이터는 네트워크 모니터링 서비스에서 분석하여 공격을 감지합니다. 공격이 감지되면 자동화된 방어 메커니즘이 시작되어 공격을 완화하고 한 고객을 위한 공격 트래픽이 다른 고객에 대한 네트워크 품질이 하되지 않도록 합니다.

## <a name="application-level-defenses"></a>응용 프로그램 수준 방어

Microsoft 엔지니어링 팀은 Microsoft Operational Security [Assurance에서](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 설정한 엄격한 표준을 준수하여 고객 데이터를 보호합니다. Microsoft의 클라우드 서비스는 응용 프로그램 수준 DoS 공격으로부터 보호하는 데 도움이 되는 높은 부하를 지원하기 위해 의도적으로 구축됩니다. Microsoft 365 확장 아키텍처는 관련 워크로드에 대한 지역별 고지 및 작업별 조정 기능을 사용하여 여러 전역 데이터 센터에 서비스를 배포합니다.

각 고객의 국가 또는 지역, 즉 고객의 관리자가 서비스를 처음 설정하는 동안 식별하는 국가 또는 지역은 해당 고객의 데이터에 대한 기본 저장소 위치를 지정합니다. 고객 데이터는 기본/백업 전략에 따라 중복 데이터 센터 간에 복제됩니다. 기본 데이터 센터는 소프트웨어에서 실행되는 모든 기본 고객 데이터와 함께 응용 프로그램 소프트웨어를 호스트합니다. 백업 데이터 센터는 자동 장애 조치(failover)를 제공합니다. 어떤 이유로든 기본 데이터 센터가 작동하지 않을 경우 요청은 백업 데이터 센터의 소프트웨어 및 고객 데이터 복사본으로 리디렉션됩니다. 고객 데이터는 어떤 경우든 기본 데이터 센터 또는 백업 데이터 센터에서 처리될 수 있습니다. 여러 데이터 센터에 데이터를 분산하면 한 데이터 센터가 공격을 받는 경우 영향을 받는 표면 영역을 줄일 수 있습니다. 또한 영향을 받는 데이터 센터의 서비스는 빠르게 보조 데이터 센터로 리디렉션하여 공격 중에 가용성을 유지 관리하고 공격이 완화된 후 기본 데이터 센터로 다시 리디렉션될 수 있습니다.

DoS 공격에 대한 또 다른 완화 기능으로 개별 워크로드에는 리소스 사용률을 관리하는 기본 제공 기능이 포함되어 있습니다. 예를 들어 Exchange Online SharePoint Online의 스로틀 메커니즘은 DoS 공격을 방어하는 다단계 접근 방식의 일부입니다.
