---
title: 데이터 센터 보안 개요
description: Microsoft 365의 데이터 센터 보안에 대해 자세히 알아보기
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 185f926db524f64851e715fecee31e699942fa22
ms.sourcegitcommit: 247ee66ab59d06d2e1b0a3f4dba301c334ebfe71
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "49601272"
---
# <a name="datacenter-security-overview"></a>데이터 센터 보안 개요

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft는 온라인 서비스를 어떻게 호스팅하나요?

Microsoft는 Microsoft Azure, Microsoft 365 및 Microsoft Dynamics 365와 같은 엔터프라이즈 서비스를 포함하여 200개가 넘는 클라우드 서비스를 24x7x365 고객에게 제공합니다. 이러한 서비스는 전역으로 분산된 데이터 센터, 에지 컴퓨팅 노드 및 서비스 운영 센터로 구성된 Microsoft의 클라우드 인프라에서 호스팅됩니다. 이러한 네트워크는 광범위한 광섬유 공간으로 세계 최대 글로벌 네트워크 중 하나에서 지원 및 연결됩니다.

클라우드 서비스를 제공하는 데이터 센터는 전 세계 고객과 파트너를 위해 안정성, 운영 우수성, 비용 효율성, 환경 지속 가능성 및 신뢰할 수 있는 온라인 환경에 초점을 맞추고 있습니다. Microsoft는 내부 및 타사 감사를 통해 데이터 센터 보안을 정기적으로 테스트합니다. 따라서 전 세계에서 가장 높은 규제 대상 조직은 다른 클라우드 서비스 공급자보다 더 많은 인증을 준수하는 Microsoft 클라우드를 신뢰합니다.

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft는 데이터 센터를 무단 액세스로부터 어떻게 보호하나요?

물리적 데이터 센터 시설에 대한 액세스는 경계 펜싱, 보안 담당자, 잠긴 서버 랙, 통합 경보 시스템, 운영 센터의 주변 비디오 감시 및 다단계 액세스 제어를 포함하여 각 수준에서 보안이 강화되어 외부 및 내부 경계에 의해 긴밀하게 제어됩니다. 필수 직원만 Microsoft 데이터 센터에 액세스할 수 있습니다. 고객 데이터를 포함하여 Microsoft 365 인프라에 대한 논리적 액세스는 Microsoft 데이터 센터 내에서 금지됩니다.

보안 운영 센터는 통합된 전자 액세스 제어 시스템과 함께 비디오 감시를 사용하여 데이터 센터 사이트 및 시설을 모니터링합니다. 카메라는 시설 경계, 출구, 출하 시, 서버 카지, 내부 바이들 및 기타 중요한 보안 지점을 효과적으로 적용하기 위해 전략적으로 배치됩니다. 다중 계층 보안의 일부로, 통합 보안 시스템에서 감지된 모든 무단 입력 시도는 즉각적인 대응 및 수정을 위해 보안 담당자에게 경고를 생성합니다.

## <a name="how-does-microsoft-protect-its-datacenters-from-environmental-hazards"></a>Microsoft는 환경적 위험으로부터 데이터 센터를 어떻게 보호하나요?

Microsoft는 데이터 센터 가용성에 대한 환경 위협으로부터 보호하기 위해 다양한 세이프가드를 활용합니다. 데이터 센터 사이트는 홍수, 지진, 재해 및 기타 자연 재해를 비롯한 다양한 요인의 위험을 최소화하기 위해 전략적으로 선택됩니다. 당사의 데이터 센터는 환경 제어를 사용하여 직원, 장비 및 하드웨어에 최적화된 조건부 공간을 모니터링하고 유지 관리합니다. 화재 감지 및 진압 시스템과 물 센서는 장비에 대한 화재 및 물 손상을 감지하고 방지하는 데 도움이 됩니다.

재해는 예측할 수 없지만 Microsoft 데이터 센터 및 운영 담당자는 예기치 않은 이벤트가 발생할 경우 작업 연속성을 제공하기 위해 재해를 준비합니다. 복구 가능한 아키텍처 및 테스트된 최신 연속성 계획은 잠재적인 손상을 완화하고 데이터 센터 작업의 신속한 복구를 촉진합니다. 위기 관리 계획은 위기 전, 중 및 이후에 역할, 책임 및 완화 활동을 명확히 합니다. 이러한 계획에 정의된 역할 및 연락처를 사용하면 위기 상황에서 명령 체인을 효과적으로 에스컬레이터할 수 있습니다.

## <a name="how-does-microsoft-verify-the-effectiveness-of-datacenter-security"></a>Microsoft는 데이터 센터 보안의 효율성을 어떻게 확인하나요?

고객이 클라우드의 이점을 완전히 실현하려면 클라우드 서비스 공급자를 신뢰할 수 있어야 합니다. 당사의 인프라 및 클라우드 서비스 제품군은 고객의 엄격한 보안 및 개인 정보 요구 사항을 해결하기 위해 구축되었습니다. 당사는 고객이 모든 클라우드 서비스 공급자의 가장 포괄적인 규정 준수 제품 집합을 제공하여 개인 데이터 수집 및 사용에 대한 국가별, 지역 및 산업별 요구 사항을 준수하는 데 도움을 드립니다.

클라우드 인프라 및 제품은 ISO, HIPAA, FedRAMP 및 SOC와 같은 광범위한 국제 및 산업별 규정 준수 표준과 오스트레일리아의 IRAP, 영국의 G-클라우드 및 싱가포르 MTCS와 같은 국가별 표준을 충족합니다. 엄격하고 제3자 감사는 이러한 표준 규정을 준수하는 엄격한 보안 제어를 검증합니다. 데이터 센터 인프라 및 클라우드 서비스에 대한 감사 보고서는 [Microsoft Service Trust Portal에서 사용할 수 있습니다.](https://servicetrust.microsoft.com/)

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 데이터 센터 보안과 관련된 컨트롤의 유효성 검사를 위해 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|  
| [ISO 27001/27002(Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=3383676c-b365-4288-a3c0-086ed8d737e3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=4e5d7afb-2cee-4704-95cc-bb8c95a8e52a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11: 물리적 및 환경적 보안 | 2020년 5월 13일 |
| [SOC 1(Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=66043614-5628-4e26-83be-057eb3bb026c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: 데이터 센터 물리적 액세스 프로비전 <br> PE-2: 데이터 센터 보안 확인 <br> PE-3: 데이터 센터 사용자 액세스 검토 <br> PE-4: 데이터 센터 물리적 액세스 메커니즘 <br> PE-5: 데이터 센터 물리적 감시 모니터링 <br> PE-6: 데이터 센터 중요 환경 유지 관리 <br> PE-7: 데이터 센터 환경 제어 <br> PE-8: 데이터 센터 인시던트 대응 | 2020년 10월 30일 |
| [SOC 2(Azure)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ce5bfbea-3514-40ae-a8a6-3617106a0b56&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | PE-1: 데이터 센터 물리적 액세스 프로비전 <br> PE-2: 데이터 센터 보안 확인 <br> PE-3: 데이터 센터 사용자 액세스 검토 <br> PE-4: 데이터 센터 물리적 액세스 메커니즘 <br> PE-5: 데이터 센터 물리적 감시 모니터링 <br> PE-6: 데이터 센터 중요 환경 유지 관리 <br> PE-7: 데이터 센터 환경 제어 <br> PE-8: 데이터 센터 인시던트 대응 | 2020년 10월 30일 |
