---
title: Microsoft 365 보안 인시던트 관리
description: 이 문서에서는 보안 인시던트 관리 프로세스에 대한 개요를 Microsoft 365.
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
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5f3123d4b4ef853357c0b98f1b6973cc8ba4d1e8
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088890"
---
# <a name="microsoft-365-security-incident-management"></a>Microsoft 365 보안 인시던트 관리

Microsoft는 모든 고객에 대해 안전하고 엔터프라이즈급 서비스를 제공하기 위해 Microsoft 365 있습니다. 이 문서에서는 Microsoft에서 보안 인시던트 처리 방법에 대해 Microsoft 365. 보안 인시던트는 Microsoft 장비 또는 Microsoft 시설에 저장된 고객 데이터에 대한 불법 액세스 또는 고객 데이터의 손실, 공개 또는 변경을 발생될 가능성이 있는 장비 또는 시설에 대한 무단 액세스입니다. 보안 인시던트에 대응할 때 Microsoft의 목표는 고객 데이터 및 서비스 Microsoft 365 것입니다.

Microsoft 365 보안 팀과 다양한 서비스 팀은 함께 작업하며 보안 인시던트에 대해 동일한 접근 방식을 취합니다.

- 준비
- 검색 및 분석
- 포함
- 지우기
- 복구
- 인시던트 후 활동

## <a name="microsoft-approach-to-security-incident-management"></a>보안 인시던트 관리에 대한 Microsoft 접근 방식

보안 인시던트 관리에 대한 Microsoft의 접근 방식은 [NIST(National Institute of Standards and Technology) SP(특별 발행물)](https://www.nist.gov/) 800-61을 준수합니다. Microsoft에는 보안 인시던트 방지, 모니터링, 감지 및 대응을 위해 함께 작업하는 여러 전용 팀이 있습니다.

|**팀/영역**|**설명**|
|:------------|:--------------|
| Microsoft 보안 응답 센터 | 보안 인시던트 및 Microsoft 소프트웨어 보안 취약점을 식별, 모니터링, 해결 및 대응합니다. |
| 사이버 방어 운영 센터 | 사이버 방어 운영 센터는 실시간으로 위협을 보호, 감지 및 대응하는 데 도움을 줄 수 있도록 보안 대응 팀과 전문가를 모아하는 물리적 위치입니다. |
| 회사, 외부 및 법률 업무 | 의심되는 보안 인시던트에 대한 법적 및 규정 자문을 제공합니다. |
| Microsoft 365 보안 대응 팀 | 서비스 Microsoft 365 파트너는 적절한 보안 인시던트 관리 프로세스를 구축하고 보안 인시던트 대응을 주도합니다. |
| Office 365 트러스트 | 규정 요구 사항, 규정 준수 및 개인 정보 보호에 대한 지침을 제공합니다. |
| Microsoft 365 데이터 센터 보안 팀 | 일반적인 보안 엔지니어링 투자에 중점을 두어 서비스 아키텍처 위험과 위협을 보호, 감지 및 대응하기 위해 다양한 서비스에 Microsoft 365 팀. |
| 서비스 팀 | 각 서비스에 대한 Microsoft 365 정책 및 결정을 담당하는 Exchange, SharePoint 및 Microsoft Teams 서비스용 팀을 엔지니어링합니다. |
| MSTIC(Microsoft Threat Intelligence Center) | Microsoft 인프라 및 자산에 대한 디지털 보안 위협의 현재 상태를 제공하면 Microsoft 내부 파트너 팀이 완화 및 방지 작업 계획의 우선 순위를 지정하고 거의 실시간 인시던트 모니터링/감지를 채택하여 보호를 강화할 수 있습니다. |
| 파트너 보안 팀 | Azure 보안 응답 팀, ID 보안 응답 및 Microsoft 회사 보안 대응 팀과 같은 Microsoft 365 주요 서비스를 제공하거나 주요 종속성을 담당하는 Microsoft 내 다른 파트너 보안 팀 |
| Microsoft 365 사용자 환경 커뮤니케이션 | 보안 및 서비스 인시던트에 대한 모든 고객 커뮤니케이션을 담당하는 엔지니어링 팀 |

## <a name="response-management-process"></a>응답 관리 프로세스

Microsoft 365 보안 팀과 서비스 팀은 함께 작업하고 NIST 800-61 대응 관리 단계를 기반으로 하는 보안 인시던트에 대해 동일한 접근 방식을 취합니다.

- **준비:** 도구, 프로세스, 역량 및 준비를 포함하여 대응할 수 있는 데 필요한 조직 준비를 참조합니다.
- **검색 & 분석:** 프로덕션 환경에서 보안 인시던트가 검색되고 모든 이벤트를 분석하여 보안 인시던트의 인증을 확인하는 활동을 참조합니다.
- **포함, 지우기,** 복구: 이전 단계에서 수행한 분석에 따라 보안 인시던트가 포함하기 위해 필요한 적절한 작업을 참조합니다. 이 단계에서 보안 인시던트로부터 완전히 복구하기 위해 추가 분석이 필요한 경우도 있습니다.
- **사후 인시던트 활동:** 보안 인시던트를 복구한 후 수행된 모의 후 분석을 참조합니다. 프로세스 중에 수행되는 운영 작업을 검토하여 준비 또는 검색 및 분석 단계에서 변경해야 하는지 여부를 검토합니다.

![보안 인시던트 관리 단계](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>페더전된 보안 응답 모델

Microsoft 365 서비스에는 핵심 Microsoft 온라인 서비스(Exchange, SharePoint 및 Microsoft Teams 등) 및 기타 Microsoft 클라우드 서비스(예: Azure Active Directory, Microsoft 상거래 플랫폼 및 MSTIC)가 포함됩니다. 이러한 서비스는 자체 보안 운영 프로세스를 통해 별도의 팀에서 운영합니다. Microsoft의 다른 팀은 또한 Microsoft의 다양한 보안 측면에 참여하고 Microsoft 365. Microsoft는 여러 팀이 보안 운영 관리를 위해 여러 팀을 운영하고 있기 때문에 Microsoft 365 보안 응답 모델을 구현했습니다.

이 표에서는 다양한 보안 운영 팀과 Microsoft 365 서비스 팀 간의 운영 Microsoft 365 제공합니다.

|**활동**|**Microsoft 365 보안 팀 운영**|**Microsoft 365 서비스 팀 작업**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 검색 및 분석 | - 검색 요구 사항 <br> - 보안 모니터링 및 분석 <br> - IOC(손상 표시기) 스위프 <br> - 위반 헌트 <br> - 24x7 보안 통화 및 인시던트 대응 리드 | - 검색 요구 사항 <br> - 인프라 배포 모니터링 <br> - 서비스 분석 및 인사이트 <br> - 이벤트 및 경고 triage <br> - 24x7 서비스 엔지니어링 통화  |
| 포함, 지우기, 복구 | - 인시던트 대응 리드 <br> - 포렌식 조사 <br> - 보안 전문 지식 및 컨설팅 <br> - 복구 지침 | - 보안 인시던트 소유자 <br> - 서비스 인사이트 및 전문 지식 <br> - 포함, 지우기 및 복구 실행 |
| 인시던트 사후 활동 | - 인시던트 사후 분석 리드 <br> - 데이터 수집 및 보관 <br> - 학습한 교훈 및 버그 요청 <br> - 인시던트 보고 | - 서비스 쪽 인시던트 분석 <br> - 후속 작업 우선 순위 지정 <br> - 구현 보안 투자 <br> - 서비스 보안 준비 |

## <a name="related-articles"></a>관련 문서

- [Microsoft 365 인시던트 관리 준비](assurance-sim-preparation.md)
- [Microsoft 365 인시던트 관리 검색 및 분석](assurance-sim-detection-analysis.md)
- [Microsoft 365 인시던트 관리 포함, 삭제 및 복구](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 인시던트 관리 사후 활동 관리](assurance-sim-post-incident-activity.md)
