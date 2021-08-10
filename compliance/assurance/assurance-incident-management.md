---
title: 인시던트 관리 개요
description: 2013의 인시던트 관리에 대해 Microsoft 365
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
hideEdit: true
ms.openlocfilehash: 1c45bd4424a3ffe47aaafd14524ae6f3c507d3b683838a7b9e2c9755b77d518b
ms.sourcegitcommit: 07b748b28a7815fb5824be0dea3edba29353361d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/10/2021
ms.locfileid: "57833855"
---
# <a name="incident-management-overview"></a>인시던트 관리 개요

## <a name="what-is-a-security-incident"></a>보안 인시던트란 무엇입니까?

Microsoft는 온라인 서비스의 보안 인시던트를 Microsoft에서 처리하는 동안 고객 데이터 또는 개인 데이터의 우발적 또는 불법적 파괴, 손실, 변경, 무단 공개 또는 액세스로 이어지는 확인된 보안 위반으로 정의합니다. 예를 들어 Microsoft 온라인 서비스 인프라에 대한 무단 액세스 및 고객 데이터 유출은 보안 인시던트로 구성되는 반면 서비스 또는 고객 데이터의 기밀성, 무결성 또는 가용성에 영향을 주지 않는 규정 준수 이벤트는 보안 인시던트로 간주되지 않습니다.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft는 보안 인시던트에 어떻게 대응하나요?

보안 인시던트가 있을 때마다 Microsoft는 신속하고 효과적으로 대응하여 보안 및 고객 데이터를 Microsoft 서비스 노력합니다. Microsoft는 보안 위협을 빠르고 효율적으로 조사, 포함 및 제거하도록 설계된 인시던트 대응 전략을 사용합니다.

Microsoft 클라우드 서비스는 손상 징후를 지속적으로 모니터링합니다. 자동화된 보안 모니터링 및 경고 외에도 모든 직원은 잠재적인 보안 인시던트의 징후를 인식하고 보고하기 위한 연례 교육을 받게 됩니다. 직원, 고객 또는 보안 모니터링 도구가 감지한 의심스러운 활동은 조사를 위해 서비스별 보안 대응 팀으로 에스컬레이터됩니다. 서비스별 보안 응답 팀을 비롯한 모든 서비스 운영 팀은 24x7x365에서 리소스를 사용할 수 있도록 심층 통화 순환을 유지 관리합니다. Microsoft는 통화 순환을 통해 광범위한 이벤트 또는 동시 이벤트를 포함하여 모든 시간 또는 규모에 따라 효과적인 인시던트 대응을 탑재할 수 있습니다.

의심스러운 활동이 감지되고 에스컬레이터되면 서비스별 보안 대응 팀은 **분석, 포함,** 지우기 및 복구 프로세스를 시작됩니다. 이러한 팀은 잠재적인 인시던트에 대한 분석을 조정하여 고객 또는 고객 데이터에 대한 영향을 포함하여 해당 범위를 파악합니다. 이 분석에 따라 서비스별 보안 대응 팀은 영향을 미치는 서비스 팀과 함께 위협을 포함하는 계획을 개발하고 인시던트의 영향을 최소화하고, 환경에서 위협을 제거하고, 알려진 보안 상태로 완전히 복구합니다. 관련 서비스 팀은 서비스별 보안 응답 팀의 지원을 통해 계획을 구현하여 위협이 성공적으로 제거되고 영향을 미치는 서비스가 완전한 복구를 받되도록 합니다.

인시던트가 해결된 후 서비스 팀은 향후 유사한 인시던트의 방지, 감지 및 대응을 향상하기 위해 인시던트에서 얻은 교훈을 구현합니다. 보안 인시던트를 선택합니다. 특히 고객에 영향을 미치거나 데이터 위반이 발생한 인시던트는 전체 인시던트 사후 우발을 하게 됩니다. 사후 분석은 인시던트에 기여했거나 인시던트 대응 프로세스 중에 식별된 기술적 실수, 절차적 오류, 수동 오류 및 기타 프로세스 결함을 식별하도록 설계되었습니다. 사후 평가 중에 확인된 개선은 향후 인시던트를 방지하고 감지 및 대응 기능을 개선하는 데 도움이 하도록 서비스별 보안 대응 팀의 조정을 통해 구현됩니다.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>고객이 보안 또는 개인 정보 보호 인시던트에 대해 어떻게 언제 알림을 하나요?

Microsoft는 고객 데이터의 무단 손실, 공개 또는 수정과 관련된 보안 침해를 인식할 때마다 OST(온라인 서비스 약관)의 DPA(데이터 보호 부록)에 설명된 72시간 이내에 영향을 받는 고객에게 알립니다. 알림 타임라인 약정은 공식 보안 인시던트 선언이 발생할 때 시작됩니다. 보안 인시던트를 선언할 때 알림 프로세스는 과도한 지연 없이 최대한 신속하게 수행됩니다.

알림에는 위반의 특성, 대략적인 사용자 영향 및 완화 단계(해당하는 경우)에 대한 설명이 포함됩니다. 초기 알림 시 Microsoft의 조사가 완료되지 않은 경우 알림에는 후속 통신을 위한 다음 단계 및 타임라인도 표시됩니다.

고객이 데이터 위반을 포함하여 Microsoft에 영향을 미칠 수 있는 인시던트에 대해 알고 있는 경우 고객은 DPA에 정의된 인시던트에 대해 Microsoft에 즉시 알릴 책임이 있습니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 인시던트 관리와 관련된 컨트롤의 유효성 검사는 다음 표를 참조합니다.

### <a name="azure-and-dynamics-365"></a>Azure 및 Dynamics 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2021년 12월 2일 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2021년 12월 2일 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: PII와 관련된 데이터 위반 알림  | 2021년 12월 2일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: 인시던트 관리 프레임워크 <br> IM-2: 감지 메커니즘 및 경고 <br> IM-3: 인시던트 대응 실행 <br> IM-4: 인시던트 사후 mortems <br> IM-6: 인시던트 응답 테스트 <br> OA-7: 통화 엔지니어 액세스 | 2021년 3월 31일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9: 포렌식 절차 <br> CUEC: 인시던트 보고 <br> IM-1: 인시던트 관리 프레임워크 <br> IM-2: 감지 메커니즘 및 경고 <br> IM-3: 인시던트 대응 실행 <br> IM-4: 인시던트 사후 mortems <br> IM-6: 인시던트 응답 테스트 <br> OA-7: 통화 엔지니어 액세스 <br> SOC2-6: 고객 지원 웹 사이트 <br> SOC2-9: 서비스 대시보드 | 2021년 3월 31일 |

### <a name="office-365"></a>Office 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4: 인시던트 처리 <br> IR-6: 인시던트 보고 <br> IR-8: 인시던트 대응 계획 | 2020년 9월 24일 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: 정보 보안 인시던트 및 개선 사항 관리 | 2021년 4월 20일 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: PII와 관련된 데이터 위반 알림  | 2021년 4월 20일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: 보안 인시던트 보고 <br> CA-47: 인시던트 대응 | 2020년 12월 24일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: SLA(서비스 수준 계약) <br> CA-13: 인시던트 대응 가이드 <br> CA-15: 서비스 상태 알림  <br>  <br> CA-26: 보안 인시던트 보고 <br> CA-29: 통화 엔지니어 <br> CA-47: 인시던트 대응 | 2020년 12월 24일 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: 인시던트 보고  | 2020년 12월 24일  |

## <a name="resources"></a>리소스

- [온라인 서비스 약관(OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [DPA(데이터 보호 부록)](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure 및 Azure에 대한 Microsoft 클라우드 인시던트 관리 구현 Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Office 365 타사 취약점 평가 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
