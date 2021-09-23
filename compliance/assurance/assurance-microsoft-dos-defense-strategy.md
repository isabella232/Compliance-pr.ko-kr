---
title: Microsoft 서비스 거부 방어 전략
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
ms.openlocfilehash: e1613765d3ffb7b43b80d07823fe8aef45719b70
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486195"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Microsoft 서비스 거부 방어 전략

## <a name="denial-of-service-defense-strategy"></a>서비스 거부 방어 전략

네트워크 기반 분산 DDoS(서비스 거부) 공격을 방어하는 Microsoft의 전략은 전 세계적 공간으로 인해 고유하므로 Microsoft는 대부분의 다른 조직에서 사용할 수 없는 전략과 기술을 활용할 수 있습니다. 또한 Microsoft는 Microsoft 파트너와 더 광범위한 인터넷 보안 커뮤니티를 포함하는 광범위한 위협 인텔리전스 네트워크로 집계된 집합적 지식에 기여하고 이를 모집합니다. 이 인텔리전스와 온라인 서비스 및 Microsoft의 글로벌 고객 기반에서 수집한 정보와 함께 모든 Microsoft 온라인 서비스의 자산을 보호하는 Microsoft의 DDoS 방어 시스템을 지속적으로 개선합니다.

Microsoft DDoS 전략의 초석은 글로벌 현재 상태입니다. Microsoft는 전 세계 인터넷 공급자, 피어링 공급자(공용 및 개인) 및 개인 기업과 함께 일합니다. 이 계약은 Microsoft에 상당한 인터넷 제공을 제공하며 Microsoft가 넓은 표면 영역에 대한 공격을 흡수할 수 있도록 합니다.

시간이 지날 때 Microsoft의 에지 용량이 커지자 개별 가장자리에 대한 공격의 중요성은 크게 줄어 났습니다. 이러한 감소로 Microsoft는 DDoS 방지 시스템의 검색 및 완화 구성 요소를 분리했습니다. Microsoft는 에지 노드에서 전역 완화를 유지하면서 채도 지점에 가깝게 공격을 감지하기 위해 지역별 데이터 센터에 다층 계층 검색 시스템을 배포합니다. 이 전략은 여러 동시 Microsoft 서비스 처리할 수 있도록 합니다.

Microsoft에서 DDoS 공격에 대해 가장 효과적이고 저렴한 방어 중 하나는 서비스 공격 표면을 줄이는 것입니다. 원치 않는 트래픽은 데이터를 인라인으로 분석, 처리 및 스크러빙하는 대신 네트워크 에지에서 삭제됩니다.

공용 네트워크와의 인터페이스에서 Microsoft는 방화벽, 네트워크 주소 변환 및 IP 필터링 기능에 특수 용도의 보안 장치를 사용합니다. 또한 Microsoft는 ECMP(Global equal-cost multi-path) 라우팅을 사용 합니다. 전역 ECMP 라우팅은 서비스에 도달할 전역 경로가 여러 개 있도록 하는 네트워크 프레임워크입니다. 각 서비스에 대한 여러 경로를 사용하여 DDoS 공격은 공격이 시작된 지역으로 제한됩니다. 최종 사용자는 다른 경로를 사용하여 해당 지역의 서비스에 도달할 수 있는 다른 지역은 공격의 영향을 받지 않습니다. 또한 Microsoft는 흐름 데이터, 성능 메트릭 및 기타 정보를 사용하여 DDoS 공격을 빠르게 감지하는 내부 DDoS 상관 관계 및 검색 시스템을 개발했습니다.

클라우드 서비스를 더욱 보호하기 위해 Microsoft는 기본 제공되는 DDoS 보호 시스템인 Azure DDoS 보호를 Microsoft Azure 지속적인 모니터링 및 침투 테스트 프로세스를 사용합니다. Azure DDoS 보호는 외부 공격을 방어할 뿐만 아니라 다른 Azure 테넌트의 공격을 방지하도록 고안된 것입니다. Azure는 SYN 쿠키, 속도 제한 및 연결 제한과 같은 표준 감지 및 완화 기술을 사용하여 DDoS 공격으로부터 보호합니다. 자동화된 보호를 지원하기 위해 워크로드 간 DDoS 인시던트 대응 팀은 팀 전체의 역할과 책임, 에스컬레이터 기준 및 영향을 받는 팀 전체의 인시던트 처리 프로토콜을 식별합니다.

대상에 대해 시작된 대부분의 DDoS 공격은 OSI(Open [Systems Interconnection)](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) 모델의 네트워크(L3) 및 전송(L4) 계층에 있습니다. L3 및 L4 계층을 위한 공격은 공격 트래픽이 있는 네트워크 인터페이스 또는 서비스를 넘쳐 리소스를 과도하게 사용하며 합법적인 트래픽에 대응할 수 있는 기능을 거부하도록 디자인되었습니다. L3 및 L4 공격으로부터 보호하기 위해 Microsoft의 DDoS 솔루션은 데이터 센터 라우터의 트래픽 샘플링 데이터를 사용하여 인프라와 고객 목표를 보호합니다. 트래픽 샘플링 데이터는 네트워크 모니터링 서비스에서 분석하여 공격을 감지합니다. 공격이 감지되면 자동화된 방어 메커니즘이 시작되어 공격을 완화하고 한 고객을 위한 공격 트래픽이 다른 고객에 대한 네트워크 품질이 하되지 않도록 합니다.

Microsoft는 또한 DDoS 방어에 대한 공격적인 접근 방식을 입니다. 봇넷은 DDoS 공격을 수행하기 위한 일반적인 명령 및 제어의 소스로, 공격을 확대하고 비동기성을 유지 관리합니다. Microsoft DCU(Digital Crimes Unit)는 맬웨어 배포 및 통신 인프라를 식별, 조사 및 중단하여 봇넷의 규모와 영향을 줄입니다.

## <a name="application-level-defenses"></a>응용 프로그램 수준 방어

Microsoft 엔지니어링 팀은 Microsoft Operational Security [Assurance에서](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 설정한 엄격한 표준을 준수하여 고객 데이터를 보호합니다. Microsoft의 클라우드 서비스는 응용 프로그램 수준 DDoS 공격으로부터 보호하는 데 도움이 되는 높은 부하를 지원하기 위해 의도적으로 구축됩니다. Microsoft의 확장된 아키텍처는 관련 워크로드에 대한 지역별 및 작업별 조정 기능을 사용하여 여러 전역 데이터 센터에 서비스를 배포합니다.

각 고객의 국가 또는 지역( 고객의 관리자가 서비스의 초기 구성 중에 식별)에 따라 해당 고객의 데이터에 대한 기본 저장소 위치가 결정됩니다. 고객 데이터는 기본/백업 전략에 따라 중복 데이터 센터 간에 복제됩니다. 기본 데이터 센터는 소프트웨어에서 실행되는 모든 기본 고객 데이터와 함께 응용 프로그램 소프트웨어를 호스트합니다. 백업 데이터 센터는 자동 장애 조치(failover)를 제공합니다. 어떤 이유로든 기본 데이터 센터가 작동하지 않을 경우 요청은 백업 데이터 센터의 소프트웨어 및 고객 데이터 복사본으로 리디렉션됩니다. 고객 데이터는 어떤 경우든 기본 데이터 센터 또는 백업 데이터 센터에서 처리될 수 있습니다. 여러 데이터 센터에 데이터를 분산하면 한 데이터 센터가 공격을 받는 경우 영향을 받는 표면 영역을 줄일 수 있습니다. 또한 영향을 받는 데이터 센터의 서비스는 빠르게 보조 데이터 센터로 리디렉션하여 공격 중에 가용성을 유지 관리하고 공격이 완화된 후 기본 데이터 센터로 다시 리디렉션될 수 있습니다.

DDoS 공격에 대한 또 다른 완화 기능으로 개별 워크로드에는 리소스 사용률을 관리하는 기본 제공 기능이 포함되어 있습니다. 예를 들어 Exchange Online 및 SharePoint Online의 스로틀 메커니즘은 DDoS 공격을 방어하는 다단계 접근 방식의 일부입니다.

Azure SQL Database IP 주소를 기반으로 실패한 로그인 시도를 추적하는 DoSGuard라는 게이트웨이 서비스 형식의 추가 보안 계층이 있습니다. 동일한 IP에서 로그인 시도에 실패한 임계값에 도달하면 DoSGuard는 미리 결정된 시간 동안 주소를 차단합니다.

## <a name="resources"></a>리소스

- [Azure DDoS 보호 표준 개요](/azure/ddos-protection/ddos-protection-overview)
- [Azure DDoS 보호 표준 기본 모범 사례](/azure/ddos-protection/fundamental-best-practices)
- [DDoS 응답 전략의 구성 요소](/azure/ddos-protection/ddos-response-strategy)
