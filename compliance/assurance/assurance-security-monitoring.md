---
title: 보안 모니터링 개요
description: Microsoft 365의 보안 모니터링에 대 한 자세한 정보
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
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508849"
---
# <a name="security-monitoring-overview"></a>보안 모니터링 개요

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>보안 모니터링에 대 한 Microsoft의 전략 이란?

Microsoft 365은 시스템에 대 한 지속적인 보안 모니터링을 통해 Microsoft 365 서비스에 대 한 위협을 검색 하 고 대응 합니다. 보안 모니터링 및 경고에 대 한 주요 원칙은 다음과 같습니다.

- 견고성: 다양 한 공격 동작을 감지 하는 신호 및 논리
- 정확도: 소음 으로부터 혼란을 방지 하기 위한 의미 있는 경고
- 속도: 공격자가 신속 하 게 중단할 수 있는 기능

자동화, 확장 및 클라우드 기반 솔루션은 모니터링 및 대응 전략의 핵심 핵심 요소로입니다. Microsoft 365 핵심 서비스의 확장을 통해 공격을 효과적으로 파악 하 고 중지 하기 위해, 모니터링 시스템은 거의 정확한 경고를 가까운 시간에 자동으로 처리 해야 합니다. 마찬가지로 문제를 감지 하는 경우에는 대규모 위험을 완화 하는 기능이 필요 하며, 팀에 의존 하 여 문제를 수동으로 해결 하는 것은 불가능 합니다. 확장으로 위험을 완화 하기 위해 클라우드 기반 도구를 사용 하 여 자동으로 대책을 적용 하 고 엔지니어에 게 승인 된 완화를 환경 전체에 적용 하는 도구를 제공 합니다.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Microsoft 365에서 보안 모니터링을 수행 하는 방법

Microsoft 365에서는 중앙 로깅을 사용 하 여 보안 인시던트를 나타낼 수 있는 작업에 대 한 로그 이벤트를 수집 하 고 분석 합니다. 중앙 로깅 도구는 이벤트 로그, 응용 프로그램 로그, 액세스 제어 로그 및 네트워크 기반 침입 감지 시스템을 비롯 한 모든 시스템 구성 요소의 로그를 집계 합니다. 이 서비스의 핵심 인프라는 서버 로깅 및 응용 프로그램 수준 데이터 외에도 자세한 원격 분석을 생성 하 고 호스트 기반 침입 감지를 제공 하는 사용자 지정 된 보안 에이전트를 포함 합니다. 이 원격 분석은 모니터링 및 법적 조사에 사용 됩니다.

Microsoft에서 수집 하는 로깅 및 원격 분석 데이터를 통해 24/7 보안 경고를 사용할 수 있습니다. 경고 시스템은 업로드 된 로그 데이터를 분석 하 여 거의 실시간으로 경고를 생성 합니다. 여기에는 규칙 기반 알림과 기계 학습 모델을 기반으로 하는 보다 복잡 한 경고가 포함 됩니다. 이 모니터링 논리는 일반적인 공격 시나리오를 능가 하며 서비스 아키텍처 및 작업에 대 한 심층적인 인식을 통합 합니다. 보안 모니터링 데이터를 사용 하 여 모델을 지속적으로 개선 하 여 새로운 유형의 공격을 검색 하 고 보안 모니터링의 정확성을 개선 합니다.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Microsoft 365이 보안 모니터링 경고에 어떻게 대처 하나요?

경고에 대 한 응답으로 또는 서비스 전체에서 법적 증거를 추가로 조사 하기 위해 작업을 수행 해야 하는 경우 클라우드 기반 도구를 사용 하면 전체 환경에서 빠르게 응답할 수 있습니다. 이러한 도구에는 검색 된 위협에 대처 하는 완전 자동화 된 지능형 에이전트 (보안 대책)가 포함 되어 있습니다. 대부분의 경우 이러한 에이전트는 자동 대책을 배포 하 여 사용자 간섭 없이도 확장에서 보안 검색을 완화 합니다. 이것이 불가능 한 경우 보안 모니터링 시스템은 자동으로 적절 한 호출 엔지니어에 게 경고 하 여 검색 된 위협을 완화 하기 위해 실시간으로 작동할 수 있도록 하는 일련의 도구를 설치 합니다. Microsoft 365 보안 대응 팀으로 제기 되는 잠재적 인시던트는 보안 인시던트 대응 프로세스를 사용 하 여 해결 됩니다.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Microsoft 365에서 시스템 가용성을 모니터링 하는 방법은 무엇 인가요?

Microsoft 365는 시스템을 적극적으로 모니터링 하 여 리소스 사용률 및 비정상적인 사용을 표시 합니다. 서비스 중복을 통해 리소스 모니터링은 예기치 않은 가동 중지 시간을 방지 하 고 고객에 게 제품 및 서비스에 대 한 안정적인 액세스 권한을 제공 하기 위해 지원 합니다. 서비스 상태 문제는 SHD (서비스 상태 대시보드)를 통해 고객에 게 즉시 전달 됩니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 보안 모니터링과 관련 된 컨트롤의 유효성 검사에 대 한 자세한 내용은 다음 표를 참조 하십시오.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-17: 원격 액세스 <br> AU-7: 감사 감소 및 보고서 생성 <br> SI-4: 정보 시스템 모니터링 <br> SI-7: 소프트웨어, 펌웨어 및 정보 무결성 <br> | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3: 가용성 모니터링 및 용량 계획 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3: 가용성 모니터링 및 용량 계획 <br> 16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: 변경 모니터링 <br> CA-26: 보안 문제 보고 <br> CA-29: 통화 중 엔지니어 <br> CA-48: 데이터 센터 로깅 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: 변경 모니터링 <br> CA-26: 보안 문제 보고 <br> CA-29: 통화 중 엔지니어 <br> CA-30: 가용성 모니터링 <br> CA-48: 데이터 센터 로깅 | 2019년 9월 30일 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | , 2008-08: 보고 인시던트 <br> \ EC-10: 서비스 계약 | 2019년 9월 30일 |

## <a name="resources"></a>리소스

- [배후에서: 인프라 보호 Microsoft 365 서비스 켜기](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
