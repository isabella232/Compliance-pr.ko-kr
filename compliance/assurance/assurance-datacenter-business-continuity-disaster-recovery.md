---
title: 데이터 센터 비즈니스 연속성 및 재해 복구
description: Microsoft 데이터 센터 비즈니스 연속성 및 재해 복구에 대해 자세히 알아보습니다.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 948e1f9e1b15b83817c072e63ffaae0b444445f8
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265107"
---
# <a name="datacenter-business-continuity-and-disaster-recovery"></a>데이터 센터 비즈니스 연속성 및 재해 복구

재해는 예측할 수 없지만 Microsoft 데이터 센터 및 운영 담당자는 예기치 않은 이벤트가 발생할 경우 운영의 연속성을 제공하기 위해 재해에 대비합니다. 복원성 있는 아키텍처와 테스트를 거친 최신 연속성 계획은 잠재적인 손상을 완화하고 데이터 센터 운영의 신속한 복구를 촉진합니다. 위기 관리 계획은 위기 전, 중, 후의 역할, 책임 및 완화 활동에 대한 명확성을 제공합니다. 이러한 계획에 정의된 역할과 연락처는 위기 상황에서 명령 체계를 효과적으로 확대하는 데 도움이 됩니다.

## <a name="business-resilience"></a>비즈니스 복원성

Microsoft 클라우드 운영 및 혁신(CO+I) 비즈니스 연속성 프로그램에서 데이터 센터는 지속적인 운영 및 위기 이벤트에 대한 대응을 테스트해야 합니다. 각 Microsoft 관리 데이터 센터에는 CO+I Resilience Center of Excellence 및 Datacenter Operations의 주요 주제 전문 지식을 사용하여 사이트별 컨텍스트가 긴급 준비에 고려되도록 하여 자체 비즈니스 연속성 계획이 있습니다. 이러한 계획에서는 다양한 재해 시나리오에 대한 역할, 책임, 직원 안전 절차, 알림 기준, 에스컬레이터 단계 및 검사 목록을 설명합니다.

Microsoft의 CO+I 조직의 탄력성 기능은 Enterprise 비즈니스 연속성 관리 프로그램에 의해 제어되고 Enterprise 정책 및 표준을 준수합니다. 프로그램의 성과는 비즈니스 연속성 위원회, 부서 리더십 및 궁극적으로 Microsoft의 수석 리더십 팀에서 정기적으로 검토합니다.

## <a name="crisis-management-and-pandemic-response"></a>위기 관리 및 팬데믹 대응

위기 관리 프로그램은 전 세계적으로 존재하는 주요 이벤트에 대한 Microsoft의 대응에서 없어서는 안될 부분입니다. Microsoft의 데이터 센터 위기 관리 계획은 업계 모범 사례를 기반으로 하며 주요 이벤트에 대응하는 전술적 접근을 허용하는 데 필요한 중요한 구성 요소를 포함합니다. 또한 CO+I응용성 센터는 운영에 영향을 줄 수 있는 감염성 감염에 대처하는 데 사용되는 Pandemic 및 감염성 감염 계획을 개발하고 계속 유지 관리하고 있습니다. 파노라마 대응의 일부로, 탄력성 지원 팀은 Redmond 기반 Microsoft 리더십에 중요하고 시의적시에 현지 감염 인텔리전스를 제공하여 포괄적인 완화 전략을 촉진합니다.

Microsoft는 회사 전체에서 비즈니스 연속성 Enterprise 지침 역할을 하는 조직 전체의 EBCM(비즈니스 연속성 관리) 프레임워크를 설정했습니다. 이 프로그램에는 비즈니스 연속성 정책, 구현 지침, BIA(비즈니스 영향 분석), 위험 평가, 종속성 분석 및 프로그램 모니터링 및 개선 절차가 포함됩니다. Enterprise Microsoft Office 관리 및 성능 보고를 관리하는 데 필요한 관리 CO+I 탄력성 프로그램은 Co+I Resilience Center of Excellence를 통해 조정하여 프로그램이 일관된 장기 비전과 임무를 준수하고 엔터프라이즈 프로그램 표준, 방법, 정책 및 메트릭과 일치하도록 보장합니다. CO+I Resilience Center of Excellence는 CO+I 조직에 추가 거버넌스를 제공하도록 설계된 일련의 표준을 수립했습니다.

TRP(CO+I Technology Resilience Plans)는 중요 기술을 계속 사용할 수 있도록 심각도 인시던트 또는 재해로부터 복구하기 위해 CO+I 내의 다양한 엔지니어링 그룹을 위한 것입니다.

BRP(비즈니스 복구 계획) 및 TRP에는 서비스, 복원 절차 및 인시던트 관리 팀과의 통신에 대한 범위 및 적용 가능한 종속성이 포함되어 있습니다. BRP 및 TRP는 적어도 매년 전용 계획 소유자가 검토 및 승인하며 모든 해당 사용자에게 제공됩니다. 계획은 적용 가능한 표준의 일부로 정의된 테스트 일정에 따라 테스트됩니다.

## <a name="resiliency-program"></a>Resiliency Program

Microsoft는 심각한 부정적인 이벤트가 발생할 때 작업 대응, 복구 및 다시 시작에 대한 지침으로 사용할 BRP를 정의했습니다. BRP는 중요한 비즈니스 프로세스 및 운영을 계속하는 데 필요한 주요 담당자, 리소스, 서비스 및 작업을 다합니다. BRP 개발은 Microsoft의 Enterprise 지침에 따라 Office.

이 계획의 범위는 24시간 이내에 필요한 경우 정의되는 Microsoft의 중요한 비즈니스 프로세스입니다. 이러한 프로세스는 BIA 중에 결정됩니다. 이 BIA에서는 Microsoft가 프로세스를 수행할 수 없는 경우 잠재적인 운영 및 금전적 영향을 예측하고 RTO(복구 시간 목표) 및 RPO(복구 지점 목표)를 결정했습니다. BIA에 따라 비기술 종속성 분석을 수행하여 프로세스를 수행하는 데 필요한 특정 사용자, 응용 프로그램, 중요 레코드 및 사용자 요구 사항을 확인합니다.

Microsoft는 BRP를 주기적으로 테스트하여 효율성, 사용 효율성을 평가하고 위험을 제거하거나 완화할 수 있는 영역을 식별합니다. 해당되는 경우 타사와 관련된 종속 관계가 있는 경우 타사가 테스트에 참여합니다. 테스트 결과는 적절한 직원의 승인을 문서화, 유효성 검사, 승인합니다. 이 정보는 작업 항목을 만들고 우선 순위를 지정하는 데 사용됩니다.

## <a name="datacenter-resilience-program"></a>Datacenter Resilience Program

CO+I 우수성 센터 팀은 데이터 센터 탄력성 프로그램의 일부로 조직의 비즈니스 연속성에 필요한 정보 보안 요구 사항을 충족하는 방법, 정책 및 메트릭을 개발합니다. 팀에서 중단이 발생할 경우 중요한 프로세스 및 필요한 리소스를 지속적으로 운영하기 위한 TRP를 개발합니다.
