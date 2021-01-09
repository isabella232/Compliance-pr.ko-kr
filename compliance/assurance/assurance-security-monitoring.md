---
title: 보안 모니터링 개요
description: Microsoft 365의 보안 모니터링에 대해 자세히
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 8a538ee055d10b002ea7efcc7d39ce20658df12b
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787357"
---
# <a name="security-monitoring-overview"></a>보안 모니터링 개요

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Microsoft의 보안 모니터링 전략은 무엇입니까?

Microsoft 365는 시스템에 대한 지속적인 보안 모니터링을 통해 Microsoft 365 서비스에 대한 위협을 감지하고 대응합니다. 보안 모니터링 및 경고에 대한 주요 원칙은:

- 견고성: 다양한 공격 동작을 감지하는 신호 및 논리
- 정확도: 노이즈를 방해하지 않도록 의미 있는 경고
- 속도: 공격을 중지할 만큼 빠르게 공격을 catch하는 능력

자동화, 규모 및 클라우드 기반 솔루션은 모니터링 및 응답 전략의 핵심 기조입니다. 일부 Microsoft 365 핵심 서비스의 규모에서 공격을 효과적으로 catch하고 중지하려면 모니터링 시스템이 거의 실시간으로 매우 정확한 경고를 자동으로 발생해야 합니다. 마찬가지로 문제가 감지되면 대규모로 위험을 완화할 수 있는 능력이 필요하면 팀에서 수동으로 컴퓨터 간 문제를 해결할 수 없습니다. 대규모로 위험을 완화하기 위해 클라우드 기반 도구를 사용하여 대책을 자동으로 적용하고 엔지니어에게 승인된 완화를 환경에 신속하게 적용할 수 있는 도구를 제공합니다.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Microsoft 365는 보안 모니터링을 어떻게 수행하나요?

Microsoft 365는 중앙 로깅을 사용하여 보안 인시던트가 표시될 수 있는 활동에 대한 로그 이벤트를 수집하고 분석합니다. 중앙 로깅 도구는 이벤트 로그, 응용 프로그램 로그, 액세스 제어 로그 및 네트워크 기반 침입 감지 시스템을 비롯한 모든 시스템 구성 요소의 로그를 집계합니다. 이 서비스의 핵심 인프라에는 서버 로깅 및 응용 프로그램 수준 데이터 외에도 자세한 원격 분석이 생성되어 호스트 기반 침입 감지를 제공하는 사용자 지정된 보안 에이전트가 탑재되어 있습니다. 모니터링 및 포렌식에 이 원격 분석이 사용됩니다.

수집하는 로깅 및 원격 분석 데이터를 통해 24/7 보안 경고를 사용할 수 있습니다. 경고 시스템은 로그 데이터가 업로드되는 경우 이를 분석하여 거의 실시간으로 경고를 생성합니다. 여기에는 규칙 기반 경고와 기계 학습 모델을 기반으로 보다 정교한 경고가 포함됩니다. 모니터링 논리는 일반적인 공격 시나리오를 넘어 서비스 아키텍처 및 운영에 대한 심층 인식을 통합합니다. 당사는 보안 모니터링 데이터를 사용하여 지속적으로 모델을 개선하여 새로운 종류의 공격을 감지하고 보안 모니터링의 정확도를 향상시킵니다.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Microsoft 365는 보안 모니터링 경고에 어떻게 대응하나요?

경고에 응답하거나 서비스 전체에서 포렌식 증거를 추가로 조사하기 위해 조치를 취해야 하는 경우 클라우드 기반 도구를 통해 환경 전체에서 빠르게 대응할 수 있습니다. 이러한 도구에는 보안 대책을 사용하여 감지된 위협에 대응하는 완전히 자동화된 지능형 에이전트가 포함됩니다. 대부분의 경우 이러한 에이전트는 수동 개입 없이 대규모로 보안 검색을 완화하기 위해 자동 대책을 배포합니다. 이 작업을 할 수 없는 경우 보안 모니터링 시스템은 감지된 위협을 대규모로 완화하기 위해 실시간으로 작업할 수 있는 도구 집합이 장착된 적절한 통화 엔지니어에게 자동으로 경고합니다. Microsoft 365 보안 대응 팀으로 에스컬레이터된 잠재적인 인시던트는 보안 인시던트 대응 프로세스를 사용하여 해결됩니다.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Microsoft 365는 시스템 가용성을 어떻게 모니터링하나요?

Microsoft 365는 시스템에서 리소스 과다 사용률 및 비정상적인 사용을 나타내는 지표를 적극적으로 모니터링합니다. 리소스 모니터링은 서비스 중복을 보완하여 예기치 않은 작동을 방지하고 고객에게 제품 및 서비스에 대한 안정적인 액세스 권한을 제공합니다. 서비스 상태 문제는 SHD(서비스 상태 대시보드)를 통해 고객에게 즉시 전달됩니다.

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 보안 모니터링과 관련된 컨트롤의 유효성 검사는 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------|:--------|:------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-17: 원격 액세스 <br> AU-7: 감사 감소 및 보고서 생성 <br> SI-4: 정보 시스템 모니터링 <br> SI-7: 소프트웨어, 펌웨어 및 정보 무결성 <br> | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 가용성 모니터링 및 용량 계획 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 가용성 모니터링 및 용량 계획 <br> A.16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 모니터링 변경 <br> CA-26: 보안 인시던트 보고 <br> CA-29: 통화 엔지니어 <br> CA-48: 데이터 센터 로깅 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 모니터링 변경 <br> CA-26: 보안 인시던트 보고 <br> CA-29: 통화 엔지니어 <br> CA-30: 가용성 모니터링 <br> CA-48: 데이터 센터 로깅 | 2020년 12월 24일 |
| [SOC 3(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: 인시던트 보고 <br> CUEC-10: 서비스 계약 | 2020년 12월 24일 |

## <a name="resources"></a>리소스

- [배경: Microsoft 365 서비스에 기반을 두는 인프라 보안](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
