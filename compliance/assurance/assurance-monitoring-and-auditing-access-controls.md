---
title: Microsoft 365 액세스 제어 모니터링 및 감사
description: '요약: 각 서비스에서 사용할 수 있는 다양한 모니터링 및 감사 액세스 제어에 Microsoft 365.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e374b22212bce461329e14764a3b35eaa76d5f27fd340e64b9b64fb26ecf35f6
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290582"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>2013의 액세스 제어 모니터링 및 Microsoft 365

Microsoft는 모든 위임, 권한 및 운영에 대한 광범위한 모니터링 및 감사를 Microsoft 365. Microsoft 365 액세스 제어는 최소 권한 원칙에 따라 구축된 자동화된 프로세스로, 데이터 액세스 제어 및 감사를 통합합니다.

- 모든 허용된 액세스는 고유한 사용자에 대한 추적이 가능합니다. 관리자는 고객 콘텐츠 처리에 대한 책임이 있습니다.
- 액세스 제어 요청, 승인 및 관리 작업 로그는 보안 및 악의적인 이벤트를 분석하기 위해 캡처됩니다.
- 액세스 수준은 보안 그룹 구성원 자격에 따라 거의 실시간으로 검토하여 업무 정당성을 부여하고 자격 요구 사항을 충족하는 사용자만 시스템에 액세스할 수 있도록 합니다.
- Microsoft 365, 액세스 제어 및 지원 서비스(Azure Active Directory 및 물리적 데이터 센터 포함)는 [ISO/IEC 27001, ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP(Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)및 기타 표준을 준수하기 [](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)위해 독립적인 타사에서 정기적으로 감사를 합니다. [](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018)
- Microsoft 365 엔지니어는 연도당 보안 교육을 수행하고, 상승된 액세스 최상의 절차를 검토하고, 서비스에 대한 자격을 유지하기 위해 Microsoft의 보안 및 개인 정보 보호 정책을 인정해야 합니다.

자동화된 경고는 짧은 기간 내에 여러 로그인 실패와 같은 의심스러운 활동이 감지되면 트리거됩니다. Microsoft 365 보안 대응 팀은 기계 학습 및 빅 데이터 분석을 사용하여 활동을 검토 및 분석하고, 불규칙한 액세스 패턴을 찾아서, 비이식적 및 부정적 활동에 선제적으로 대응합니다. 또한 Microsoft는 침투 테스터의 전담 팀을 고용하고 주기적인 Red Team 및 Blue Team 연습에 참여하여 서비스에서 보안 및 액세스 제어 문제를 찾아야 합니다. 고객은 감사 보고서 및 관리 활동 API를 사용하여 액세스 제어 시스템의 효율성을 확인할 수 Microsoft 365.

자세한 내용은 에서 [Office 365 관리](/office/office-365-management-api/office-365-management-activity-api-reference) 활동 API 참조 및 감사 및 [보고를 Microsoft 365.](assurance-auditing-and-reporting-overview.md)
