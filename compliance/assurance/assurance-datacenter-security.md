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
ms.openlocfilehash: b67fad5e0901af3384b5a3b4717763e6edab1bcd
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508255"
---
# <a name="datacenter-security-overview"></a>데이터 센터 보안 개요

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft는 어떻게 온라인 서비스를 호스트 하나요?

Microsoft는 고객에 게 연중 무휴까지 Microsoft Azure, Microsoft 365 및 Microsoft Dynamics 365과 같은 엔터프라이즈 서비스를 포함 하 여 200 개 이상의 클라우드 서비스를 제공 합니다. 이러한 서비스는 전역 분산 데이터 센터, edge 컴퓨팅 노드 및 서비스 작업 센터로 구성 된 Microsoft의 클라우드 인프라에서 호스팅됩니다. 이러한 기능은 전세계의 최대 글로벌 네트워크 중 하나로, 광범위 한 파이버를 사용 하 여 지원 되 고 연결 됩니다.

클라우드를 제공 하는 데이터 센터는 전 세계의 고객 및 파트너에 게 높은 안정성, 운영 및 비용 효율성, 환경 지속 가능성 및 신뢰할 수 있는 온라인 환경에 중점을 둔 것입니다. Microsoft는 내부 및 타사 감사를 모두 통해 데이터 센터 보안을 정기적으로 테스트 합니다. 따라서 세계에서 가장 높은 규제를 하는 조직이 Microsoft 클라우드를 신뢰 하며,이는 다른 클라우드 서비스 공급자 보다 더 많은 인증을 준수 합니다.

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft가 해당 데이터 센터에서 무단 액세스를 보호 하는 방법

실제 데이터 센터 기능에 대 한 액세스는 경계 펜스, 보안 관리자, 잠긴 서버 랙, 통합 경보 시스템, 운영 센터에의 한 시계 및 다단계 액세스 제어를 포함 하 여 각 수준에서 보안을 강화 하는 외부 및 내부 perimeters에 긴밀 하 게 제어 됩니다. 필요한 직원만 Microsoft 데이터 센터에 액세스할 수 있는 권한이 부여 됩니다. 고객 데이터를 포함 하 여 Microsoft 365 인프라에 대 한 논리적 액세스는 Microsoft 데이터가 완벽 하 게 허용 되지 않습니다.

Microsoft의 보안 운영 센터에서는 통합 전자 액세스 제어 시스템과 함께 비디오 감시를 사용 하 여 데이터 센터 사이트 및 시설을 모니터링 합니다. 카메라는 설비 경계, entrances, 선적 베이, 서버 cages, 내부 aisles 및 기타 중요 한 보안 지점의 효과적인 수신 범위에 맞게 전략적으로 배치 됩니다. 여러 계층으로 구성 된 보안 상태에서 통합 보안 시스템에 의해 검색 되는 무단 항목 시도는 보안 담당자에 게 즉각적인 대응 및 수정을 위해 알림을 생성 합니다.

## <a name="how-does-microsoft-protect-its-datacenters-from-environmental-hazards"></a>Microsoft가 해당 데이터 센터에서 환경적 위험 으로부터 보호 하는 방법

Microsoft는 데이터 센터 가용성에 대 한 환경 위협 으로부터 보호 하기 위해 다양 한 보호책을 채택 하 고 있습니다. 데이터 센터 사이트는 홍수, 지진, 허리케인 및 기타 자연 재해를 비롯 한 다양 한 요인으로 인 한 위험을 최소화할 수 있도록 전략적으로 선택 됩니다. 데이터 센터는 기후 제어를 사용 하 여 직원, 장비 및 하드웨어에 대 한 최적화 된 conditioned 공간을 모니터링 하 고 유지 관리 합니다. 화재 감지 및 억제 시스템 및 물 센서는 장비에 대 한 화재 및 물 피해를 감지 하 고 방지 하는 데 도움이 됩니다.

재해는 예측할 수 없지만 Microsoft 데이터 센터 및 운영 인력은 예기치 않은 이벤트가 발생 해야 하는 재해의 연속성을 준비 합니다. 복원성 아키텍처 및 최신 테스트를 거친 연속성 계획은 잠재적인 손상을 완화 하 고 데이터 센터 작업의 swift 복구를 촉진 합니다. 위기 관리 계획은 위기 전후에 역할, 책임 및 완화 작업을 명확 하 게 제공 합니다. 이러한 계획에 정의 된 역할과 연락처는 위기 상황에서 명령 체인을 효율적으로 확대 하는 데 도움이 됩니다.

## <a name="how-does-microsoft-verify-the-effectiveness-of-datacenter-security"></a>Microsoft에서 데이터 센터 보안의 효율성을 확인 하는 방법

고객은 클라우드의 이점을 완벽 하 게 실현 하기 위해 클라우드 서비스 공급자를 신뢰할 수 있어야 합니다. 당사의 인프라 및 클라우드 서비스 제품군은 고객의 엄격한 보안 및 개인 정보 요구 사항을 해결 하기 위해 처음부터 작성 되었습니다. 고객은 클라우드 서비스 공급자에 대 한 가장 포괄적인 준수 집합을 제공 하 여 개인 데이터의 수집 및 사용을 관리 하는 국내, 지역별 및 업계 관련 요구 사항을 준수 하는 데 도움이 됩니다.

당사의 클라우드 인프라 및 제품은 ISO, HIPAA, FedRAMP 및 SOC와 같은 광범위 한 국제 및 산업별 준수 표준을 충족 하 고, 오스트레일리아의 IRAP, UK의 G-Cloud, 싱가포르의 MTCS와 같은 국가의 특정 표준에 적합 합니다. 엄격한 제 3 자 감사는 이러한 표준 요구 사항을 충족 하는 엄격한 보안 제어가 준수 하는지 확인 합니다. [Microsoft 서비스 보안 포털](https://servicetrust.microsoft.com/)에서는 데이터 센터 인프라 및 클라우드 서비스에 대 한 감사 보고서를 확인할 수 있습니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 데이터 센터 보안과 관련 된 컨트롤의 유효성 검사에 대해서는 다음 표를 참조 하세요.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | PE-2: 실제 액세스 권한 부여 <br> PE-3: 실제 액세스 제어 <br> PE-6: 실제 액세스 모니터링 <br> PE-11: 비상 전력 <br> PE-13: Fire 보호 <br> PE-14: 온도 및 습도 컨트롤 <br> PE-15: 워터 데미지 보호 | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 11: 물리적 및 환경 보안 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> 자격 (https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports | 11: 물리적 및 환경 보안 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39: 데이터 센터 액세스 제어 <br> CA-40: 데이터 센터 네트워크 인증 <br> CA-41: 데이터 센터의 두 요소 인증 <br> CA-48: 데이터 센터 로깅 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39: 데이터 센터 액세스 제어 <br> CA-40: 데이터 센터 네트워크 인증 <br> CA-41: 데이터 센터의 두 요소 인증 <br> CA-48: 데이터 센터 로깅 | 2019년 9월 30일 |
