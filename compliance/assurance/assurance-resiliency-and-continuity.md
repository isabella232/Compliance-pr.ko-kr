---
title: 복원력 및 연속성
description: 2013의 탄력성 및 연속성에 대해 Microsoft 365
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
ms.openlocfilehash: ff1719ce931a50904fb6b7e6069cd29a1883aa90
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160445"
---
# <a name="resiliency-and-continuity-overview"></a>복원력 및 연속성 개요

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>재해 또는 기타 서비스 가용성 위협이 발생하는 경우 Microsoft는 비즈니스 연속성을 어떻게 보장하나요?

Microsoft의 Enterprise EBCM(비즈니스 연속성 관리) 팀은 비즈니스 연속성 관리 및 재해 복구 활동을 Microsoft 서비스 서비스를 감독합니다. Microsoft 사업부 대표는 EBCM 팀과 협의하여 비즈니스 연속성 계획을 개발하고 비즈니스 연속성 요구 사항을 준수하는지 확인합니다.

BCM(비즈니스 연속성 관리) 수명 주기는 BCM 방법론의 핵심입니다. 이 3단계 프로세스는 Microsoft의 다양한 비즈니스 모델에 의해 구현될 수 있도록 조정 가능하도록 디자인되었습니다. 비즈니스 연속성  프로그램에 포함해야 하는 중요한 프로세스 및 목표를 식별하기 위해 평가 단계로 시작됩니다. 평가 단계에서는 BIA(비즈니스 영향 분석)도 필요합니다. 계획 **단계에서는** 복구 및 복구 전략을 개발 및 구현하고 공식 비즈니스 연속성 계획에 문서화하는 데 중점을 두습니다. 마지막으로 **기능** 유효성 검사는 비즈니스 연속성 계획 및 해당 구현을 테스트하여 효율성을 확인하고 잠재적인 개선을 식별합니다.

Microsoft 온라인 서비스 비즈니스 연속성 전략은 하드웨어, 네트워크 및 데이터 센터 중복성을 사용 합니다. 데이터 센터 간의 데이터 복제는 대재해진 인시던트 동안 고가용성 및 안정성을 제공합니다. 또한 격리된 하드웨어 오류 또는 데이터 손상과 같은 사소한 인시던트에 대한 복구를 향상합니다.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft는 비즈니스 연속성 및 재해 복구 계획을 어떻게 테스트하나요?

Microsoft의 Enterprise EBCM(비즈니스 연속성 관리) 정책은 모든 Microsoft 비즈니스 연속성 및 재해 복구 계획을 매년 테스트, 업데이트 및 검토할 수 있습니다. Microsoft 온라인 서비스는 EBCM 정책에 따라 적어도 매년 비즈니스 연속성 계획을 테스트합니다. 작업 보고서를 작성하고 검토하여 유효성을 검사하고 테스트한 후 테스트 중에 발견된 문제에 대한 응답으로 계획 업데이트를 알릴 수 있습니다.

다양한 종류의 잠재적 인시던트에 대한 복원력 및 복구 전략을 검증하기 위해 EBCM 프로그램은 사람, 위치 및 기술에 영향을 미치는 테스트 시나리오의 여러 범주를 정의합니다. 각 서비스에 필요한 유효성 검사 수준은 서비스의 중요도를 기반으로 하며 더 중요한 서비스는 더 엄격한 유효성 검사를 받습니다. 각 Microsoft 온라인 서비스 팀은 EBCM 지침에 따라 비즈니스 연속성 계획을 테스트하여 계획의 효율성 및 서비스 팀이 계획을 실행하기 위한 준비를 측정합니다.

EBCM 지침에 따라 비즈니스 연속성 계획 및 기능 유효성 검사는 마지막 검토 후 12개월 이내에 매년 검토해야 합니다. 기능 유효성 검사에는 BIA와 같은 지원 설명서에 대한 검토가 포함되어야만 문서가 정확한지 검사할 수 있습니다. Microsoft는 분기별 보고서를 통해 고객이 선택한 Microsoft 온라인 서비스에 대한 기능 유효성 검사 결과를 제공합니다.

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>Microsoft 온라인 서비스는 시스템 용량이 수요를 충족하는지 어떻게 보장하나요?

용량 계획을 통해 서비스 팀은 Microsoft 온라인 서비스 가용성을 지원하는 데 필요한 리소스를 할당할 수 있습니다. Microsoft의 EBCM 프로그램의 일부로 정기적인 용량 계획이 필요합니다. 서비스 팀은 분기별 검토 중에 용량 데이터를 검토하고 용량 검토를 더 많이 하는 긴급 상황에서 용량 데이터를 검토합니다.

용량 계획을 위한 원시 데이터는 각 서비스 팀에서 유지 관리하며 시스템 처리, 메모리 및 하드웨어 용량과 같은 메트릭을 포함합니다. 예정된 검토는 시스템의 현재 용량 모델을 사용하고 긴급 상황에서 예상되는 요구 사항에 대해 해당 모델을 테스트합니다. 모델이 용량의 격차를 나타내는 경우 시스템 용량에 대한 제안된 변경 사항은 검토를 위해 서비스 팀 리더에게 제출됩니다. 승인된 변경 사항은 서비스 팀 엔지니어가 구현하기 전에 새 모델에 통합됩니다.

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>Microsoft 온라인 서비스는 일상적인 시스템 오류 시 서비스 가용성을 유지 관리하는 방법

Microsoft 온라인 서비스는 중복 아키텍처, 데이터 복제 및 자동화된 무결성 검사를 통해 서비스 탄력성을 제공합니다. 중복 아키텍처에는 지리적 및 물리적으로 분리된 하드웨어에 여러 서비스 인스턴스를 배포하여 Microsoft 온라인 서비스에 대해 내결결성을 향상합니다. 데이터 복제를 통해 서로 다른 장애 영역의 고객 데이터의 복사본이 항상 여러 개 있도록 하므로 고객이 손상되거나 손실되거나 실수로 삭제된 경우 중요한 고객 데이터를 복구할 수 있습니다. 자동화된 무결성 검사는 다양한 종류의 물리적 또는 논리적 손상에 영향을 미치는 데이터를 자동으로 복원하여 데이터 가용성을 향상합니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 탄력성 및 연속성과 관련된 컨트롤의 유효성 검사는 다음 표를 참조합니다.

### <a name="azure-and-dynamics-365"></a>Azure 및 Dynamics 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: 정보 보안 연속성 <br> A.17.2: 중복 | 2020년 12월 2일 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 모든 컨트롤 | 2020년 5월 13일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: 비즈니스 연속성 계획 <br> BC-3: 비즈니스 연속성 및 재해 복구 절차 <br> BC-4: BCDR 테스트 <br> BC-7: 데이터 센터 비즈니스 연속성 계획 <br> BC-8: 데이터 센터 비즈니스 연속성 테스트 <br> BC-9: 데이터 센터 탄력성 평가 <br> DS-5: 백업 키 서비스 구성 요소 <br> DS-6: 중요한 구성 요소의 중복성 <br> DS-7: 고객 데이터 자동 복제 <br> DS-8: 백업 일정 <br> DS-9: 백업 복원 절차 <br> DS-11: 오프사이트 백업 <br> DS-14: 고객 서비스의 자동 복원 | 2021년 3월 31일 |

### <a name="office-365"></a>Office 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2: 대피 계획 <br> CP-3: 대피 교육 <br> CP-4: 대피 계획 테스트 <br> CP-6: 대체 저장소 사이트 <br> CP-7: 대체 처리 사이트 <br> CP-9: 정보 시스템 백업 <br> CP-10: 정보 시스템 복구 및 재구성 | 2020년 9월 24일 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: 정보 보안 연속성 <br> A.17.2: 중복 | 2021년 4월 20일 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 모든 컨트롤 | 2019년 3월 18일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: 백업 정책 <br> CA-50: 비즈니스 연속성 <br> CA-51: 데이터 복제 | 2020년 12월 24일 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: EXO 전자 메일 복원 | 2020년 12월 24일 |

## <a name="resources"></a>리소스

- [Microsoft Enterprise 비즈니스 연속성 관리 프로그램 백서](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Microsoft 클라우드 EBCM 및 재해 복구 계획 유효성 검사 보고서: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>법적 고지 조항

- [엔터프라이즈 비즈니스 연속성 법적 고지 사항](assurance-ebcm-legal-disclaimer.md)