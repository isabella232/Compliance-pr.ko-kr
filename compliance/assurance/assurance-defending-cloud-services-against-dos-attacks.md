---
title: 서비스 거부 공격에 대해 Microsoft 365 클라우드 서비스 보호
description: 이 문서에서는 Microsoft가 DoS(서비스 거부) 공격에 대해 클라우드 서비스를 보호하는 방법을 알아보고 있습니다.
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
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120577"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>서비스 거부 공격에 대해 Microsoft 365 클라우드 서비스 보호

Microsoft 데이터 센터는 경계 펜싱, 비디오 카메라, 보안 담당자 및 생체 인식, 스마트 카드 및 다단계 인증을 사용하는 보안 입장을 포함하는 심층 방어 보안으로 보호됩니다. 심층 방어 보안은 시설의 모든 영역과 각 실제 서버 단위로 계속됩니다. [Microsoft 클라우드 인프라 및 운영 그룹은](https://www.microsoft.com/cloud-platform/global-datacenters) 클라우드 서비스에 대한 핵심 인프라 및 기본 기술을 제공합니다. 데이터 센터는 물리적 보안 및 안정성에 대한 업계 표준을 준수하고 Microsoft 운영 담당자가 관리, 모니터링 및 관리합니다.

클라우드 서비스를 더욱 보호하기 위해 Microsoft는 Microsoft Azure 연속 모니터링 및 침투 테스트 프로세스의 일부인 DDoS 방어 시스템을 제공합니다. Azure DDoS 방어 시스템은 외부뿐만 아니라 다른 Azure 테넌트로부터의 공격을 견디기 위해 고안된 것입니다. Azure는 SYN 쿠키, 속도 제한 및 연결 제한과 같은 표준 감지 및 완화 기술을 사용하여 DDoS 공격으로부터 보호합니다.

Microsoft의 클라우드 서비스는 여러 소스의 공격 위협의 대상이 됩니다. 다양한 DoS 위협을 완화하고 보호하기 위해 DoS 공격으로부터 기본 인프라를 보호하고 클라우드 서비스 고객의 서비스 중단을 방지하는 기본 목표를 사용하여 확장성이 뛰어난 동적 Azure 기반 위협 감지 및 완화 시스템을 개발 및 구현했습니다. Azure DoS 완화 시스템은 인바운드, 아웃바운드 및 지역 간 트래픽을 보호합니다.

대부분의 DoS 공격은 OSI(Open [Systems Interconnection)](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) 모델의 네트워크(L3) 및 전송(L4) 계층에서 대상에 대해 시작되었습니다. L3 및 L4 계층을 위한 공격은 네트워크 인터페이스 또는 서비스를 공격 트래픽으로 넘쳐나 리소스를 과도하게 사용하며 합법적인 트래픽에 대응하는 기능을 거부하도록 디자인되었습니다. 특히 L3 및 L4 공격은 네트워크 링크, 장치 또는 서비스의 용량을 포화하거나 응용 프로그램을 지원하는 서버 또는 가상 컴퓨터의 용량을 과도하게 사용하려고 합니다.

Microsoft는 L3 및 L4 공격으로부터 보호하기 위해 이러한 계층을 보호하여 공격 대상 인프라 및 고객 대상을 보호하기 위한 솔루션을 설계, 개발 및 배포했습니다. 인프라를 보호하면 한 고객을 위한 공격 트래픽으로 인해 다른 고객에 대한 네트워크 품질이 손상되거나 손상되지 않습니다. 솔루션은 데이터 센터 라우터의 트래픽 샘플링 데이터를 사용합니다. 이 데이터는 네트워크 모니터링 서비스에서 분석하여 공격을 감지합니다. 공격이 감지되면 자동화된 방어 메커니즘이 시작됩니다.

## <a name="application-level-defenses"></a>Application-Level 방어
Microsoft 엔지니어링 팀은 Microsoft Operational Security [Assurance에서](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 설정한 엄격한 표준을 준수하여 고객 데이터를 보호합니다. Microsoft의 클라우드 서비스는 높은 부하를 지원하고 응용 프로그램 수준 DoS 공격을 보호하고 완화하기 위해 의도적으로 구축됩니다. 일부 워크로드에서 지역별 고리 및 조정 기능을 사용하여 서비스를 여러 전역 데이터 센터에 분산하는 확장된 아키텍처를 구현했습니다.

서비스의 초기 설정 중에 고객의 관리자가 식별하는 각 고객의 국가 또는 지역은 해당 고객의 데이터에 대한 기본 저장소 위치를 지정합니다. 고객 데이터는 기본/백업 전략에 따라 중복 데이터 센터 간에 복제됩니다. 기본 데이터 센터는 소프트웨어에서 실행되는 모든 기본 고객 데이터와 함께 응용 프로그램 소프트웨어를 호스팅합니다. 백업 데이터 센터는 자동 장애 조치(failover)를 제공합니다. 어떤 이유로든 기본 데이터 센터가 작동하지 않을 경우 요청은 백업 데이터 센터의 소프트웨어 및 고객 데이터 복사본으로 리디렉션됩니다. 고객 데이터는 기본 데이터 센터 또는 백업 데이터 센터에서 처리될 수 있습니다. 여러 데이터 센터에 데이터를 배포하면 한 데이터 센터가 공격을 받는 경우 영향을 받는 표면 영역이 줄어듭습니다. 또한 영향을 받는 데이터 센터의 서비스는 복구 메커니즘 중 하나로 보조 데이터 센터로 빠르게 리디렉션될 수 있으며, 서비스가 복원되면 기본 데이터 센터로 다시 리디렉션될 수도 있습니다.

개별 워크로드에는 리소스 사용률을 관리하는 기본 제공 기능이 포함되어 있습니다. 예를 들어 Exchange Online 및 SharePoint Online의 스로틀 메커니즘은 DoS 공격을 방어하는 다단계 접근 방식의 일부입니다. Exchange Online 사용자에 대한 스로틀은 최종 사용자가 소비하는 리소스 수준, 리소스가 Active Directory, Exchange Online 정보 저장소 또는 다른 곳에 있는지에 따라 결정됩니다. 사용자가 소비하는 리소스를 제한하기 위해 각 클라이언트에 예산이 할당됩니다. 사용자 작업 및 시스템 구성 요소에 대한 Exchange Online 스로틀은 작업 관리를 [기반으로 합니다.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Exchange Online 작업은 Exchange Online 시스템 리소스 관리를 위해 명시적으로 정의된 Exchange Online 기능, 프로토콜 또는 서비스입니다. 각 Exchange Online 작업에는 사용자 요청 또는 백그라운드 작업을 수행하기 위해 CPU, 사서함 데이터베이스 작업 또는 Active Directory 요청과 같은 시스템 리소스가 필요합니다. Exchange Online 작업의 예로는 웹용 Outlook, Exchange ActiveSync, 사서함 마이그레이션 및 사서함 도우미가 있습니다. 테넌트 관리자는 Exchange 관리 셸을 사용하여 사용자의 Exchange 작업 관리 스로틀 설정을 관리할 수 있습니다. PowerShell, Exchange 웹 서비스 및 POP 및 IMAP, Exchange ActiveSync, 모바일 장치 연결, 받는 사람 등 Exchange Online 내에서 구현된 다양한 형태의 스로틀이 있습니다. 관리자가 스로틀 정책을 구성할 수 있는 반면, 관리자는 Exchange Online에 대한 스로틀 정책을 구성할 수 없습니다.

SharePoint Online에서 가장 일반적인 스로틀링 트리거는 너무 높은 빈도로 너무 많은 작업을 수행하는 CSOM(클라이언트 쪽 개체 모델) 코드입니다. CSOM을 사용할 경우 단일 요청으로 많은 작업을 수행할 수 있으며, 이로 인해 사용 제한이 초과될 수 있으며 사용자당 제한이 발생할 수 있습니다.

제한이 될 수 있는 활동에 관계없이 사용자가 사용 제한을 초과하면 SharePoint Online은 일반적으로 짧은 기간 동안 해당 사용자 계정의 추가 요청을 제한합니다. 사용자 스로틀이 적용된 동안에는 다음 기준에 따라 해당 사용자의 모든 작업이 스로틀이 만료될 때까지 스로틀됩니다.
- 사용자가 브라우저에서 직접 수행한 요청의 경우 SharePoint Online은 스로틀 정보 페이지로 리디렉션하며 요청이 실패합니다.
- CSOM 통화를 비롯한 다른 모든 요청에 대해 SharePoint Online은 HTTP 상태 코드 429("너무 많은 요청")를 반환하며 요청이 실패합니다.

문제가 있는 프로세스가 계속 사용 제한을 초과하면 SharePoint Online에서 프로세스를 완전히 차단하고 HTTP 상태 코드 503("서비스를 사용할 수 없음")을 반환할 수 있습니다.

## <a name="vulnerability-and-penetration-testing"></a>취약성 및 침투 테스트
Microsoft는 [](https://www.microsoft.com/trustcenter/security/threatmanagement) 클라우드 서비스, VM(가상 컴퓨터) 및 기타 시스템에 대한 맬웨어 방지 구성 요소 및 서비스를 사용하는 것을 포함하여 정교한 최신 위협으로부터 클라우드 인프라 및 프레미스 네트워크를 보호하기 위해 많은 보안 기술 및 관행을 사용합니다. [](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) Advanced Threat Analytics - 네트워크, 시스템 및 사용자에 대한 일반적인 사용 패턴을 모니터링하고 기계 학습을 사용하여 일반 및 정기적인 침투 테스트에서 멀어진 모든 동작에 플래그를 지정합니다.

자체 침투 테스트를 수행하고 [고객에게 Microsoft 클라우드](https://technet.microsoft.com/mt784683)통합 침투 테스트 프로그램을 제공하는 것 외에도 클라우드 서비스에 대한 정기적인 취약점 평가 및 침투 테스트를 수행하는 타사 보안 전문가와도 함께 작업합니다. 이러한 타사 취약점 평가의 보고서를 [Service Trust](https://aka.ms/STP) 및 Service Assurance 포털에서 다운로드할 수 [있도록](https://aka.ms/ServiceAssurance) 합니다.
