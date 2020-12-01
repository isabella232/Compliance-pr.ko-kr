---
title: 복구 및 연속성
description: Microsoft 365의 복구 및 연속성에 대해 자세히 알아보기
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
ms.openlocfilehash: 6763e363938c422ac419fe9e76f9170912627dd5
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507730"
---
# <a name="resiliency-and-continuity-overview"></a>복구 및 연속성 개요

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Microsoft는 재해 또는 기타 서비스 가용성 위협을 일으킬 경우 비즈니스 연속성을 보장 하나요?

Microsoft의 EBCM (비즈니스 연속성 관리) 팀은 Microsoft 서비스와 클라우드 제품 간의 비즈니스 연속성 관리 및 재해 복구 활동을 oversees 합니다. Microsoft 365와 같은 Microsoft 사업부의 대표자는 EBCM 팀과 협력 하 여 비즈니스 연속성 계획을 개발 하 고 비즈니스 연속성 요구 사항을 준수 하는지 확인 합니다.

BCM (비즈니스 연속성 관리) 방법론의 핵심은 BCM 수명 주기입니다. 이 3 단계 프로세스는 Microsoft에서 다양 한 비즈니스 모델을 통해 구현할 수 있도록 융통성 있게 설계 되었습니다. 비즈니스 연속성 프로그램에 포함 해야 하는 중요 프로세스 및 목표를 식별 하기 위한 **평가** 단계부터 시작 합니다. 또한 평가 단계에는 BIA (비즈니스 영향 분석)가 필요 합니다. **계획** 단계는 공식적인 비즈니스 연속성 계획에 문서화 하는 것은 물론 복원 력 및 복구 전략의 개발 및 구현에 중점을 둔 것입니다. 마지막으로 **기능 유효성 검사** 에서는 비즈니스 연속성 계획 및 해당 구현을 테스트 하 여 효율성을 확인 하 고 잠재적으로 개선 된 기능을 파악 합니다.

Microsoft 365 business 연속성 전략은 하드웨어, 네트워크 및 데이터 센터 중복성을 활용 합니다. 데이터가 데이터 센터 간에 분산 되어 있으면 치명적이 문제가 발생할 경우 고가용성 및 안정성이 제공 됩니다. 또한 격리 된 하드웨어 오류 또는 데이터 손상과 같은 자세한 사고의 회복을 증가 시킵니다.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft는 어떻게 비즈니스 연속성 및 재해 복구 계획을 테스트 하나요?

Microsoft의 EBCM (비즈니스 연속성 관리) 정책은 모든 Microsoft 비즈니스 연속성 및 재해 복구 계획을 연간 단위로 테스트, 업데이트 및 검토 해야 함을 stipulates. Microsoft 365 서비스는 EBCM 정책에 따라 최소 매년의 비즈니스 연속성 계획을 테스트 합니다. 테스트 중에 발견 된 문제에 대 한 응답으로 작업 보고서를 만들고 검토 한 후에는 테스트 결과를 확인 하 고 계획 업데이트를 알려야 합니다.

다양 한 잠재적 사고에 대 한 복원 및 복구 전략의 유효성을 검사 하기 위해 EBCM 프로그램은 사용자, 위치 및 기술에 영향을 주는 다양 한 테스트 시나리오 범주를 정의 합니다. 각 서비스에 필요한 유효성 검사 수준은 서비스의 중요도를 기반으로 하며 보다 엄격한 유효성 검사를 수신 하는 보다 중요 한 서비스를 제공 합니다. 각 Microsoft 365 서비스 팀은 EBCM 지침에 따라 비즈니스 연속성 계획을 테스트 하 여 계획의 효율성을 측정 하 고 서비스 팀이 계획을 실행할 수 있도록 준비를 수행 합니다.

EBCM 지침에 따라 비즈니스 연속성 계획 및 기능 유효성 검사에 대 한 연간 검토는 마지막 검토 12 개월 이내에 수행 되어야 합니다. 기능 유효성 검사에서는 BIA와 같은 지원 문서에 대 한 검토를 포함 하 여 정확성을 유지 해야 합니다. Microsoft는 고객 들이 분기별 보고서를 통해 사용할 수 있는 select Microsoft 365 서비스에 대 한 기능 유효성 검사 결과를 제공 합니다.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Microsoft 365에서 시스템 용량이 수요를 충족 하는지 확인 하는 방법

용량 계획은 서비스 팀이 Microsoft 365 서비스 가용성을 지 원하는 데 필요한 리소스를 할당 하도록 지원 합니다. 일반적인 용량 계획은 Microsoft의 EBCM 프로그램의 일부로 필요 합니다. 서비스 팀은 분기별 검토 중에도 용량 데이터를 검토 하 고 추가 용량 검토를 지 원하는 비상 상황을 살펴봅니다.

용량 계획에 대 한 원시 데이터는 각 서비스 팀에서 유지 관리 되며 시스템 처리, 메모리 및 하드웨어 용량과 같은 메트릭을 포함 합니다. 예약 된 검토 시스템의 현재 용량 모델을 사용 하 고 응급 상황에서 예상 되는 요구에 대해 테스트 합니다. 모델에 용량 차이가 표시 되는 경우 시스템 용량에 대 한 제안 된 변경 내용이 검토를 위해 서비스 팀 리더에 게 제출 됩니다. 승인 된 변경 내용은 서비스 팀 엔지니어가 구현 하기 전에 새 모델에 통합 됩니다.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>일상적인 시스템 오류 동안 Microsoft 365에서 서비스 가용성을 유지 하는 방법은 무엇 인가요?

Microsoft 365는 중복 아키텍처, 데이터 복제 및 자동화 된 무결성 검사를 통해 서비스 복구 력을 달성 합니다. 중복 아키텍처는 Microsoft 365 서비스에 대 한 내결함성을 높이기 위해 지리적이 고 물리적으로 분리 된 하드웨어에 여러 서비스 인스턴스를 배포 하는 것을 포함 합니다. 데이터 복제를 사용 하면 항상 서로 다른 오류 영역에 고객 데이터 복사본이 여러 개 있으므로 고객이 손상, 손실 또는 실수로 삭제 한 경우에도 중요 한 고객 데이터를 복구할 수 있습니다. 자동화 된 무결성 검사를 통해 여러 종류의 실제 또는 논리적 손상으로 영향을 받는 데이터를 자동으로 복원 하 여 데이터 가용성을 향상 시킵니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 회복성 및 연속성과 관련 된 컨트롤의 유효성 검사에 대해서는 다음 표를 참조 하세요.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: 긴급 복구 계획 <br> CP-3: 긴급 상황 교육 <br> CP-4: 긴급 복구 계획 테스트 <br> CP-6: 대체 저장소 사이트 <br> CP-7: 대체 처리 사이트 <br> CP-9: 정보 시스템 백업 <br> CP-10: 정보 시스템 복구 및 reconstitution | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 17.1: 정보 보안 연속성 <br> 17.2: 중복 | 2020년 2월 22일 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 모든 컨트롤 | 2019년 3월 18일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: 백업 정책 <br> CA-50: 비즈니스 연속성 <br> CA-51: 데이터 복제 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: 백업 정책 <br> CA-50: 비즈니스 연속성 <br> CA-51: 데이터 복제 | 2019년 9월 30일 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | 로열티 EC-09: EXO 전자 메일 복원 | 2019년 9월 30일 |

## <a name="resources"></a>리소스

- [Microsoft 엔터프라이즈 비즈니스 연속성 관리 프로그램 백서](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft 클라우드 EBCM 및 재해 복구 계획 유효성 검사 보고서: FY20 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=5437a1d9-5883-468b-aee0-8c8a8e4ef56a&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>법적 고 지 사항

- [엔터프라이즈 비즈니스 연속성 법적 고지 사항](assurance-ebcm-legal-disclaimer.md)