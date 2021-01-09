---
title: 보안 개발 및 운영 개요
description: Microsoft 365의 보안 개발 및 운영에 대해 자세히
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
ms.openlocfilehash: 916303ff2a65777785c89c6ccae70bea9a0bfda9
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787307"
---
# <a name="security-development-and-operations-overview"></a>보안 개발 및 운영 개요

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft는 보안 개발 방법을 어떻게 구현하나요?

Microsoft의 SDL(보안 개발 수명 주기)은 보안 소프트웨어 개발 및 운영에 중점을 두는 보안 보증 프로세스입니다. SDL은 Microsoft의 개발자와 엔지니어가 제품 및 서비스의 취약점 수와 심각도 감소를 위해 세부적으로 고려할 수 있는 보안 요구 사항을 제공합니다. 모든 Microsoft 소프트웨어 개발 팀은 SDL 요구 사항을 따라야하며 변화하는 위협 환경, 업계 모범 사례 및 규정 준수 표준을 반영하도록 SDL을 지속적으로 업데이트합니다.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Microsoft의 SDL은 응용 프로그램 보안을 어떻게 개선하나요?

Microsoft의 SDL 프로세스는 요구 사항, 디자인, 구현, 검증 및 릴리스의 5개 개발 단계로 생각할 수 있습니다. 먼저 보안을 염두에 두어 소프트웨어 요구 사항을 정의합니다. 이를 위해 응용 프로그램이 어떻게 해야 하는지 보안 관련 질문과 대답을 제공합니다. 응용 프로그램에서 중요한 데이터를 수집해야 하나요? 응용 프로그램이 중요하거나 중요한 작업을 수행하나요? 응용 프로그램이 불안정한 원본의 입력을 수락해야 하나요?

관련 보안 요구 사항이 확인되면 이러한 요구 사항을 충족하는 보안 기능을 통합하도록 소프트웨어를 디자인합니다. 개발자는 수동 코드 검토, 자동화된 보안 도구 및 침투 테스트를 통해 확인하는 코드에서 SDL 및 디자인 요구 사항을 구현합니다. 마지막으로 코드를 릴리스하기 전에 새로운 기능 및 재료 변경 사항이 모든 요구 사항을 충족하는지 확인하기 위해 최종 보안 및 개인 정보 보호 검토를 진행합니다.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Microsoft에서 일반적인 취약점에 대해 소스 코드를 테스트하는 방법

코드 개발 중 및 릴리스 후에 개발자가 보안 요구 사항을 구현할 수 있도록 Microsoft는 소스 코드에서 보안 결함 및 취약점을 자동으로 검사하는 보안 개발 도구 모음을 제공합니다. Microsoft는 Microsoft 빌드 파이프라인 내에서 자동으로 실행되는 기본 제공 보안 검사와 함께 컴파일러 및 개발 환경과 같은 개발자가 사용할 승인된 도구 목록을 정의하고 게시합니다. 개발자는 승인된 최신 버전의 도구를 사용하여 새로운 보안 기능을 활용합니다.

릴리스 분기로 코드를 체크 인하려면 SDL을 사용하려면 별도의 검토자에 의해 수동 코드 검토가 필요합니다. 코드 검토자는 코딩 오류를 확인하고 코드 변경 내용이 SDL 및 디자인 요구 사항을 충족하는지 확인하고, 기능 및 보안 테스트를 통과하고 안정적으로 수행됩니다. 또한 관련 문서, 구성 및 종속성도 검토하여 코드 변경 내용이 적절하게 문서화되어 의도하지 않은 부작용을 발생하지 않도록 합니다. 검토자에서 코드 검토 중에 문제를 발견하면 제출자에게 제안된 변경 내용 및 추가 테스트가 있는 코드를 다시 제출해 달라고 요청할 수 있습니다. 코드 검토자는 요구 사항을 충족하지 않는 코드에 대한 체크 인을 완전히 차단할 수도 있습니다. 검토자에 의해 코드가 만족스러운 것으로 인정된 경우 검토자 승인을 제공해야 코드가 다음 배포 단계로 진행됩니다.

Microsoft는 보안 개발 도구 및 수동 코드 검토 외에도 자동화된 보안 도구를 사용하여 SDL 요구 사항을 적용합니다. 이러한 도구 중 다수는 커밋 파이프라인에 기본 제공되며, 체크 인되고 새 빌드가 컴파일될 때 코드에서 보안 결함을 자동으로 분석합니다. 예를 들어 일반적인 보안 결점에 대한 정적 코드 분석과 포함된 비밀에 대한 코드를 분석하는 자격 증명 스캐너가 있습니다. 자동화된 보안 도구로 해결해야 새 빌드가 보안 검토를 통과하고 릴리스를 승인할 수 있습니다.

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft는 오픈 소스 소프트웨어를 어떻게 관리하나요?

Microsoft는 다음과 같은 도구 및 워크플로를 활용하는 오픈 소스 보안을 관리하기 위한 개략적인 전략을 채택했습니다.

- 제품 및 서비스에서 사용되는 오픈 소스 구성 요소를 이해합니다.
- 이러한 구성 요소가 사용되는 위치 및 방법을 추적합니다.
- 이러한 구성 요소에 취약점이 있는지 여부를 파악합니다.
- 이러한 구성 요소에 영향을 주는 취약점이 발견되는 경우 적절히 대응합니다.

Microsoft 엔지니어링 팀은 제품 또는 서비스에 포함된 모든 오픈 소스 소프트웨어의 보안에 대한 책임을 유지 관리합니다. 이를 대규모로 달성하기 위해 Microsoft는 오픈 소스 검색, 법적 요구 사항 워크플로 및 취약한 구성 요소에 대한 경고를 자동화하는 CG를 통해 엔지니어링 시스템에 필수적인 기능을 구축했습니다. 자동화된 CG 도구 검사는 오픈 소스 구성 요소 및 관련 보안 취약성 또는 법적 의무를 위해 Microsoft에서 빌드합니다. 검색된 구성 요소는 등록되어 비즈니스 및 보안 검토를 위해 적절한 팀에 제출됩니다. 이러한 검토는 오픈 소스 구성 요소와 관련된 법적 의무 또는 보안 취약점을 평가하고 배포에 대한 구성 요소를 인가하기 전에 이를 해결하도록 디자인되었습니다.

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 보안 개발 및 작업과 관련된 컨트롤의 유효성을 검사하기 위해 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: 시스템 개발 수명 주기 | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: 관리 컨트롤 변경 <br> A.14.2: 개발 및 지원 프로세스의 보안 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: 관리 컨트롤 변경 <br> A.14.2: 개발 및 지원 프로세스의 보안 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: 위험 관리 <br> CA-18: 변경 관리 <br> CA-19: 모니터링 변경 <br> CA-21: 변경 테스트 <br> CA-38: 기준 구성 <br> CA-46: 보안 검토 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: 위험 관리 <br> CA-18: 변경 관리 <br> CA-19: 모니터링 변경 <br> CA-21: 변경 테스트 <br> CA-38: 기준 구성 <br> CA-46: 보안 검토 | 2020년 12월 24일 |

## <a name="resources"></a>리소스

- [Microsoft의 보안 개발 수명 주기](https://www.microsoft.com/securityengineering/sdl)
