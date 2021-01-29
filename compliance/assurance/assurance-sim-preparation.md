---
title: 'Microsoft 365 보안 인시던트 관리: 준비'
description: 이 문서에서는 Microsoft 365의 보안 인시던트 관리 준비 프로세스에 대한 개요를 제공합니다.
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
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040341"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Microsoft 365 보안 인시던트 관리: 준비

## <a name="training-and-background-checks"></a>교육 및 배경 검사

Microsoft 365에서 작업하는 각 직원에게는 역할에 적합한 보안 인시던트 및 대응 절차에 대한 교육이 제공됩니다. 모든 Microsoft 365 직원은 가입 시 교육을 받고 그 이후 매년 매년 재구성 교육을 받게 됩니다. 이 교육은 직원에게 Microsoft의 보안 방식에 대한 기본적인 이해를 제공하도록 디자인된 것으로, 교육이 완료된 후 모든 직원이 다음을 이해할 수 있도록 합니다.

- 보안 인시던트 정의
- 보안 인시던트 보고에 대한 모든 직원의 책임
- Microsoft 365 보안 대응 팀으로 잠재적인 보안 인시던트 에스컬레이터하는 방법
- Microsoft 365 보안 인시던트 대응 팀이 보안 인시던트에 대응하는 방법
- 개인 정보, 특히 고객 개인 정보 보호와 관련한 특별 문제
- 보안 및 개인 정보 보호 및 에스컬레이터 연락처에 대한 추가 정보를 찾을 수 있는 위치
- 기타 관련 보안 영역(필요한 경우)

해당 직원은 매년 보안에 대한 재구성 교육을 받을 수 있습니다. 연례 재구성 교육에서는 다음을 중점적으로 진행합니다.

- 이전 연도의 표준 운영 절차에 대한 변경 내용
- 보안 인시던트 보고에 대한 모든 사람 책임 및 보고 방법
- 보안 및 개인 정보 보호 및 에스컬레이터 연락처에 대한 추가 정보를 찾을 수 있는 위치
- 매년 관련성이 있을 수 있는 기타 보안 중심 영역

또한 Microsoft 365에서 작업하는 각 직원은 후보의 교육, 고용, 범죄 기록 및 HIPAA(Health Insurance Portability and Accountability Act), ITAR(International Traffic in Arms Regulations), FedRAMP(Federal Risk and Authorization Management Program) 등 미국 규정에 따라 특정 정보를 포함하는 적절하고 철저한 배경 조사를 거치게 됩니다.

백그라운드 검사는 Microsoft 365 엔지니어링 내에서 작업하는 모든 직원에게 필수입니다. 일부 Microsoft 365 환경 및 운영자 역할에는 전체 지문, 시민권 요구 사항, 정부의 인증 요구 사항 및 기타 더 엄격한 제어가 필요할 수도 있습니다. 또한 일부 서비스 팀과 역할은 필요한 경우 특수 보안 교육을 거치게 될 수 있습니다. 마지막으로 보안 팀 구성원 자체는 보안과 직접적으로 관련된 특수 교육 및 회의 참가를 얻습니다. 이 교육은 팀과 직원의 요구에 따라 다르지만 업계 회의, 내부 Microsoft 보안 회의 및 업계에서 잘 알려진 보안 교육 공급업체를 통한 외부 교육 과정과 같은 과정이 포함됩니다. 또한 Microsoft 전체의 보안 커뮤니티를 위해 연중 내내 게시되고 Microsoft 365 전문 문서가 정기적으로 게시됩니다.

## <a name="penetration-testing--assessment"></a>침투 테스트 & 평가

Microsoft는 다양한 산업 기관 및 보안 전문가와 함께 새로운 위협과 진화하는 추세를 이해합니다. Microsoft는 자체 시스템을 지속적으로 취약점을 평가하고 동일한 작업을 하는 다양한 독립적인 외부 전문가와 계약합니다.

Microsoft 365 내에서 서비스 보안 테스트를 수행하면 다음과 같은 네 가지 일반 범주로 그룹화할 수 있습니다.

1. **자동화된 보안 테스트:** 내부 및 외부 담당자는 Microsoft SDL 사례, OWASP(Open Web Application Security Project) 10개 위험 및 다양한 산업 기관에서 보고하는 새로운 위협에 따라 Microsoft 365 환경을 정기적으로 검사합니다.
2. **취약점 평가:** 독립적인 타사 테스터와의 공식 계약은 주요 논리적 컨트롤이 다양한 규제 기관의 서비스 의무를 이행하기 위해 효과적으로 운영되고 있는지 정기적으로 검증합니다. 평가는 CREST(Registered Ethical Security Testers) 인증 담당자가 수행하며 OWASP 상위 10개 위험 및 기타 서비스 적용 위협을 기반으로 합니다. 발견된 모든 위협은 폐쇄로 추적됩니다.
3. **지속적인 시스템 취약점 테스트:** Microsoft는 팀이 새로운 위협, 혼합된 위협 및/또는 고급 영구 위협을 사용하여 시스템 위반을 시도하는 정기적인 테스트를 수행하고, 다른 팀은 이러한 위반 시도를 차단합니다.
4. **Microsoft Online Services 버그 부호 프로그램:** 이 프로그램은 Microsoft 365에서 고객이 시작한 제한적인 취약점 평가를 허용하는 정책을 운영합니다. 자세한 내용은 버그 [Microsoft Online Services 용어를 참조하세요.](https://www.microsoft.com/msrc/bounty-terms)

Microsoft 365 엔지니어링 팀은 다양한 규정 준수 문서를 주기적으로 게시합니다. 이러한 문서 중 일부를 [Microsoft 클라우드](https://aka.ms/STP) 서비스 보안 포털 또는 [Microsoft 365](https://compliance.office.com) 규정 준수 센터의 Service Assurance 영역의 공개 계약에 따라 사용할 수 있습니다.

>[!NOTE]
>Service Trust Portal에 액세스하는 방법에 대한 자세한 내용은 비즈니스용 Office 365, Azure 및 Dynamics CRM Online 구독용 Service Trust Portal 시작을 참조하세요. Microsoft 365 규정 준수 센터에 액세스하려면 Microsoft 365 구독이 필요합니다.

## <a name="attack-simulation"></a>공격 시뮬레이션

Microsoft는 탐지 및 대응 기능을 개선하기 위해 보안 및 대응 계획의 지속적인 공격 시뮬레이션 연습 및 실시간 사이트 침투 테스트에 참여합니다. Microsoft는 실제 위반을 정기적으로 시뮬레이트하고, 지속적인 보안 모니터링을 수행하며, Microsoft 365와 Azure의 보안을 검증하고 개선하기 위한 보안 인시던트 대응 방법을 제공합니다.

Microsoft는 다음 두 가지 핵심 팀을 사용하여 침해 가정 보안 전략을 실행합니다.

### <a name="red-teams"></a>빨간색 팀

Microsoft 365 보안 Red Team은 Microsoft의 인프라, 플랫폼 및 Microsoft 자체 테넌트 및 응용 프로그램 위반에 초점을 맞추는 Microsoft 내의 전일 직원 그룹입니다. 온라인 서비스(고객 응용 프로그램 또는 데이터는 아우라)에 대해 대상 및 영구적 공격을 수행하는 전담 공격자(인용해커 그룹)입니다. 또한 서비스 인시던트 대응 기능에 대한 지속적인 '전체 스펙트럼' 유효성 검사(예: 기술 제어, 용지 정책, 인적 대응 등)를 제공합니다.

### <a name="blue-teams"></a>파란색 팀

Microsoft 365 보안 Blue 팀은 보안 인시던트 대응, 엔지니어링 및 운영 팀 전체의 전담 보안 응답자 및 구성원으로 구성됩니다. 이들은 독립적이며 Red 팀과는 별도로 운영됩니다. Blue 팀은 확립된 보안 프로세스를 따르고 최신 도구 및 기술을 사용하여 공격 및 침투 시도를 감지하고 대응합니다. 실제 공격과 마찬가지로, 파란색 팀은 Red 팀의 공격이 언제 또는 어떻게 발생하거나 어떤 방법을 사용할 수 있을지 알 수 없습니다. Red Team 공격이든, 실제 공격이든 이들의 작업은 모든 보안 인시던트의 감지 및 대응입니다. 이러한 이유로, Blue 팀은 지속적으로 통화 중이기 때문에 Red 팀이 다른 적을 위반하는 경우와 동일한 방식으로 위반에 대응해야 합니다.

Microsoft 직원은 전일 빨간색 팀과 파란색 팀을 서비스 전체와 내부에서 운영하는 다양한 부서에서 분리합니다. *Red Teaming이라고* 하는 접근 방식은 인프라 및 플랫폼 엔지니어링 또는 운영 팀에 대한 설명 없이 실제 프로덕션 인프라와 동일한 전략, 기술 및 절차를 사용하여 Microsoft 서비스 시스템 및 운영 전반에 걸쳐 테스트하는 것입니다. 이 테스트는 보안 검색 및 응답 기능을 테스트하고 프로덕션 취약성, 구성 오류, 잘못된 가정 또는 기타 보안 문제를 제어된 방식으로 식별하는 데 도움이 됩니다. 모든 Red 팀 침해 후 서비스 팀을 포함하여 Red 팀과 Blue 팀 간의 전체 공개를 통해 공백을 식별하고, 결과를 해결하고, 위반 대응을 현저하게 개선합니다.

>[!NOTE]
>Red Teaming 또는 라이브 사이트 침투 연습 중에 고객 데이터는 대상으로 지정되지 않습니다. 테스트는 Microsoft 365 및 Azure 인프라 및 플랫폼뿐만 아니라 Microsoft 자체 테넌트, 응용 프로그램 및 데이터에 대해 수행됩니다. Microsoft 365 또는 Azure에서 호스트되는 고객 테넌트, 응용 프로그램 및 데이터는 계약 규칙에 따라 대상으로 지정되지 않습니다.

### <a name="joint-exercises"></a>공동 연습

Microsoft 365 보안 파랑 및 Red 팀은 작업 중 관계가 각 팀의 선택된 직원 집합보다 파트너가 더 많은 공동 작업을 수행하게 됩니다. 이러한 연습은 팀 간에 잘 조정되어 도형 해커와 응답자 간의 실시간 공동 작업을 통해 보다 대상이 지정된 결과 집합을 구동합니다. 이러한 '자주색 팀' 연습은 기회를 최대화하기 위해 각 작업에 맞게 고도로 조정되지만 각 작업의 기본은 목표를 달성하기 위한 높은 대역폭 정보 공유 및 파트너 관계입니다.

## <a name="related-articles"></a>관련 문서

- [Microsoft 365 보안 인시던트 관리](assurance-security-incident-management.md)
- [Microsoft 365 보안 인시던트 관리 감지 및 분석](assurance-sim-detection-analysis.md)
- [Microsoft 365 보안 인시던트 관리 포함, 지우기 및 복구](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 보안 인시던트 관리 인시던트 사후 활동](assurance-sim-post-incident-activity.md)
