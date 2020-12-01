---
title: 인시던트 관리 개요
description: Microsoft 365의 문제 관리에 대해 자세히 알아보기
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507850"
---
# <a name="incident-management-overview"></a>인시던트 관리 개요

## <a name="what-is-a-security-incident"></a>보안 인시던트 란?

Microsoft는 Microsoft에서 처리 하는 동안 실수로 또는 불법적 파괴, 손실, 변경, 무단 공개 또는 고객 데이터에 대 한 액세스를 허용 하는 보안 침해를 확인 하는 보안 인시던트를 온라인 서비스에 정의 합니다. 예를 들어 Microsoft 365 인프라에 대 한 무단 액세스 및 고객 데이터의 exfiltration은 보안 인시던트를 구성 하지만, 서비스 또는 고객 데이터의 기밀성, 무결성 또는 가용성에 영향을 주지 않는 규정 준수 이벤트는 보안 인시던트로 간주 되지 않습니다.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft는 어떻게 보안 인시던트에 대응 하나요?

보안 인시던트가 발생할 때마다 Microsoft는 Microsoft 서비스 및 고객 데이터를 보호 하기 위해 신속 하 고 효과적으로 대응 하도록 노력 하 고 있습니다. Microsoft는 보안 위협을 신속 하 고 효율적으로 조사, 포함 및 제거 하기 위해 설계 된 사고 대응 전략을 채택 하 고 있습니다.

Microsoft 클라우드 서비스는 손상의 징후를 지속적으로 모니터링 합니다. 모든 직원은 자동화 된 보안 모니터링 및 경고 뿐 아니라 잠재적 보안 사고의 징후를 인식 하 고 보고 하는 연간 교육을 받습니다. 직원, 고객 또는 보안 모니터링 도구에서 감지 하는 의심 스러운 활동은 조사를 위해 서비스 관련 보안 대응 팀으로 에스컬레이션 됩니다. 서비스 관련 보안 응답 팀을 비롯 한 모든 서비스 운영 팀에서는 연중 무휴 문제 대응을 위해 리소스를 사용할 수 있도록 하는 통화 간 전체 순환 순환을 유지 관리 합니다. Microsoft는 통화 간 회전을 통해 광범위 하 게 또는 동시에 발생 하는 이벤트를 비롯 하 여 언제 든 지 유효한 인시던트 응답을 탑재할 수 있습니다.

의심 스러운 활동이 감지 및 에스컬레이션 되 면 서비스 관련 보안 응답 팀이 **분석, 포함, eradication 및 복구** 프로세스를 시작 합니다. 이러한 팀은 고객 또는 고객 데이터에 대 한 영향을 포함 하 여 해당 범위를 결정 하는 잠재적 사고의 분석을 조정 합니다. 이 분석을 기반으로 서비스 관련 보안 대응 팀은 영향을 받는 서비스 팀과 협력 하 여 위협을 포함 하는 계획을 개발 하 고, 환경의 위협을 eradicate 하 고, 알려진 안전한 상태로 완벽 하 게 복구 합니다. 관련 서비스 팀은 위협이 성공적으로 제거 되 고 영향을 받는 서비스가 전체 복구를 수행할 수 있도록 서비스 관련 보안 응답 팀의 지원에 대 한 계획을 구현 합니다.

인시던트가 해결 된 후에는 서비스 팀이 사고 로부터 배운 모든 교훈을 구현 하 여 향후의 유사한 사고를 보다 효율적으로 예방, 감지 및 대응 합니다. 보안 인시던트 (특히 고객이 영향을 주는 또는 데이터 위반)를 선택 하 고 전체 문제를 사후에 진행 합니다. 사후 시행은 문제를 해결 하거나 인시던트 대응 프로세스 중에 확인 된, 기술 lapses, 절차 오류, 수동 오류 및 기타 프로세스 결점을 식별 하기 위한 것입니다. 사후 시행 중에 파악 된 개선 사항은 서비스 관련 보안 대응 팀의 조정으로 구현 되어 향후 사고가 발생 하지 않고 검색 및 대응 기능이 향상 됩니다.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>고객에 게 보안 또는 개인 정보 취급 방침에 대 한 알림이 제공 되는 경우 및 시기

Microsoft에서 고객 데이터의 무단 손실, 노출 또는 수정과 관련 한 보안 위반을 알게 되 면 Microsoft는 OST (Data Protection 추 인)에 설명 된 것 처럼 영향을 받는 고객에 게 72 시간 이내에 알립니다. 알림 일정 약속은 공식적인 보안 인시던트 선언이 발생할 때 시작 됩니다. 보안 인시던트를 선언할 때 알림 프로세스는 따라 지체 지연을 제외 하 고 가능한 한 expeditiously 발생 합니다.

알림에는 위반의 특성, 대략적인 사용자 영향 및 완화 단계에 대 한 설명이 포함 됩니다 (해당 하는 경우). 초기 알림 시점에 Microsoft의 조사가 완료 되지 않으면 다음 단계와 후속 통신에 대 한 일정도 표시 됩니다.

고객이 Microsoft에 영향을 줄 수 있으 나 데이터 위반에 제한 되지 않는 문제를 알게 되 면 고객은 DPA에 정의 된 대로 인시던트를 Microsoft에 즉시 알리는 역할을 담당 합니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 인시던트 관리와 관련 된 컨트롤의 유효성 검사에 대 한 자세한 내용은 다음 표를 참조 하십시오.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: 인시던트 처리 <br> IR-6: 인시던트 보고 <br> IR-8: 보안 문제 대응 계획 | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2020년 2월 22일 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 10.1: PII와 관련 된 데이터 위반 알림  | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-26: 보안 문제 보고 <br> CA-47: 인시던트 응답 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-12: Sla (서비스 수준 계약) <br> CA-13: 보안 문제 대응 가이드 <br> CA-15: 서비스 상태 알림  <br>  <br> CA-26: 보안 문제 보고 <br> CA-29: 통화 중 엔지니어 <br> CA-47: 인시던트 응답 | 2019년 9월 30일 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | , 2008-08: 보고 인시던트  | 2019년 9월 30일  |

## <a name="resources"></a>리소스

- [온라인 서비스 약관 (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [데이터 보호 추 록 (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure 및 Office 365에 대 한 Microsoft 클라우드 인시던트 관리 구현 지침](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-Office 365의 타사 취약성 평가-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
