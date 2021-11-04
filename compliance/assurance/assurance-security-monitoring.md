---
title: 보안 모니터링 개요
description: 2013의 보안 모니터링에 대해 Microsoft 365
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
ms.openlocfilehash: 55cca0d9e6cf3ce306c0f659c867ad717586754a
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/04/2021
ms.locfileid: "60779964"
---
# <a name="security-monitoring-overview"></a>보안 모니터링 개요

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>보안 모니터링을 위한 Microsoft의 전략은 무엇입니까?

Microsoft는 시스템을 지속적으로 보안 모니터링하여 Microsoft 온라인 서비스에 대한 위협을 감지하고 대응합니다. 보안 모니터링 및 경고에 대한 주요 원칙은:

- 견고성: 다양한 공격 동작을 감지하는 신호 및 논리
- 정확도: 노이즈의 산만을 방지하기 위한 의미 있는 경고
- 속도: 공격을 중지할 만큼 빠르게 공격을 catch하는 능력

자동화, 규모 및 클라우드 기반 솔루션은 모니터링 및 대응 전략의 핵심 요소입니다. Microsoft의 일부 온라인 서비스 규모에서 공격을 효과적으로 방지하려면 모니터링 시스템이 거의 실시간으로 매우 정확한 경고를 자동으로 발생해야 합니다. 마찬가지로 문제가 감지되면 대규모로 위험을 완화할 수 있는 능력이 필요하면 팀에서 수동으로 컴퓨터 간 문제를 해결할 수 없습니다. 대규모로 위험을 완화하기 위해 클라우드 기반 도구를 사용하여 대책을 자동으로 적용하고 엔지니어에게 환경 전반에 승인된 완화 조치를 신속하게 적용할 수 있는 도구를 제공합니다.

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>Microsoft 온라인 서비스는 보안 모니터링을 어떻게 수행하나요?

Microsoft 온라인 서비스는 중앙 로깅을 사용하여 보안 인시던트가 표시될 수 있는 활동에 대한 로그 이벤트를 수집하고 분석합니다. 중앙 집중식 로깅 도구는 이벤트 로그, 애플리케이션 로그, 액세스 제어 로그 및 네트워크 기반 침입 탐지 시스템을 포함한 모든 시스템 구성 요소의 로그를 집계합니다. 핵심 인프라에는 서버 로깅 및 응용 프로그램 수준 데이터 외에도 자세한 원격 분석이 생성되어 호스트 기반 침입 감지를 제공하는 사용자 지정된 보안 에이전트가 탑재되어 있습니다. Microsoft는 이 원격 분석을 모니터링 및 포렌식에 사용합니다.

수집하는 로깅 및 원격 분석 데이터를 통해 24/7 보안 경고를 사용할 수 있습니다. 당사의 경고 시스템은 업로드되는 로그 데이터를 분석하여 거의 실시간으로 경고를 생성합니다. 여기에는 규칙 기반 경고와 기계 학습 모델을 기반으로 하는 보다 정교한 경고가 포함됩니다. Microsoft의 모니터링 로직은 일반적인 공격 시나리오를 넘어 서비스 아키텍처 및 운영에 대한 깊은 인식을 통합합니다. 보안 모니터링 데이터를 분석하여 모델을 지속적으로 개선하여 새로운 종류의 공격을 감지하고 보안 모니터링의 정확도를 향상시킵니다.

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>Microsoft 온라인 서비스는 보안 모니터링 경고에 어떻게 대응하나요?

경고를 트리거하는 보안 이벤트가 서비스 전체에서 신속한 대응 조치 또는 추가 조사가 필요한 경우 클라우드 기반 도구를 사용하여 환경 전체에서 신속한 대응을 할 수 있습니다. 이러한 도구에는 보안 대책으로 탐지된 위협에 대응하는 완전 자동화된 지능형 에이전트가 포함됩니다. 많은 경우 이러한 에이전트는 자동 대응책을 배포하여 사람의 개입 없이 대규모로 보안 탐지를 완화합니다. 이 응답을 사용할 수 없는 경우 보안 모니터링 시스템은 감지된 위협을 대규모로 완화하기 위해 실시간으로 작업할 수 있는 도구 집합을 갖춘 적절한 통화 엔지니어에게 자동으로 경고합니다. 잠재적인 인시던트는 해당 Microsoft 보안 대응 팀으로 에스컬레이터된 후 보안 인시던트 대응 프로세스를 사용하여 해결됩니다.

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>Microsoft Online Services에서 시스템 가용성을 모니터링하는 방법

Microsoft는 리소스 과다 사용률 및 비정상적인 사용의 지표에 대한 시스템을 적극적으로 모니터링합니다. 리소스 모니터링은 서비스 중복을 보완하여 예기치 않은 작동을 방지하고 고객에게 제품 및 서비스에 대한 안정적인 액세스 권한을 제공합니다. Microsoft 온라인 서비스 상태 문제는 SHD(서비스 상태 대시보드)를 통해 고객에게 즉시 전달됩니다.

Azure 및 Dynamics 365 온라인 서비스는 여러 인프라 서비스를 사용하여 보안 및 상태 가용성을 모니터링합니다. STX(가상 트랜잭션) 테스트를 구현하면 Azure 및 Dynamics 서비스가 해당 서비스의 가용성을 확인할 수 있습니다. STX 프레임워크는 실행 중인 서비스에서 구성 요소의 자동화된 테스트를 지원하도록 설계되고 라이브 사이트 오류 경고에서 테스트됩니다. 또한 Azure ASM(보안 모니터링) 서비스는 새로운 서비스와 실행 중인 서비스 모두에서 보안 경고가 예상대로 작동하고 있는지 확인하기 위해 중앙 집중식 가상 테스트 절차를 구현했습니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 보안 모니터링과 관련된 컨트롤의 유효성 검사는 다음 표를 참조합니다.

### <a name="azure-and-dynamics-365"></a>Azure 및 Dynamics 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 가용성 모니터링 및 용량 계획 | 2020년 12월 2일 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 가용성 모니터링 및 용량 계획 <br> A.16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2020년 12월 2일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: 인시던트 관리 프레임워크 <br> IM-2: 인시던트 검색 구성 <br> IM-3: 인시던트 관리 절차 <br> IM-4: 인시던트 사후 모의 <br> VM-1: 보안 이벤트 로깅 및 수집 <br> VM-12: Azure 서비스 가용성 모니터링 <br> VM-4: 악성 이벤트 조사 <br> VM-6: 보안 취약성 모니터링 | 2021년 3월 31일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: 인시던트 관리 프레임워크 <br> IM-2: 인시던트 검색 구성 <br> IM-3: 인시던트 관리 절차 <br> IM-4: 인시던트 사후 모의 <br> PI-2: Azure Portal SLA 성능 검토 <br> VM-1: 보안 이벤트 로깅 및 수집 <br> VM-12: Azure 서비스 가용성 모니터링 <br> VM-4: 악성 이벤트 조사 <br> VM-6: 보안 취약성 모니터링 | 2021년 3월 31일 |

### <a name="office-365"></a>Office 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-17: 원격 액세스 <br> AU-7: 감사 감소 및 보고서 생성 <br> SI-4: 정보 시스템 모니터링 <br> SI-7: 소프트웨어, 펌웨어 및 정보 무결성 <br> | 2020년 9월 24일 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: 가용성 모니터링 및 용량 계획 | 2021년 4월 20일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 모니터링 변경 <br> CA-26: 보안 인시던트 보고 <br> CA-29: 통화 엔지니어 <br> CA-48: 데이터 센터 로깅 | 2020년 12월 24일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: 모니터링 변경 <br> CA-26: 보안 인시던트 보고 <br> CA-29: 통화 엔지니어 <br> CA-30: 가용성 모니터링 <br> CA-48: 데이터 센터 로깅 | 2020년 12월 24일 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: 인시던트 보고 <br> CUEC-10: 서비스 계약 | 2020년 12월 24일 |

## <a name="resources"></a>리소스

- [비하인드 스토리: Microsoft 365 서비스를 지원하는 인프라 보안](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
