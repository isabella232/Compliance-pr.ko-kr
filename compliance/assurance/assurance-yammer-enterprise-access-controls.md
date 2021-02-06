---
title: Microsoft 365 Yammer 엔터프라이즈 액세스 제어
description: 이 문서에서는 프로덕션 환경에서 엔터프라이즈 액세스 Yammer 대한 간략한 요약을 제공합니다.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120367"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer 액세스 제어 

프로덕션 환경에 대한 물리적 Yammer 논리적 액세스는 소수의 사용자(인프라 및 작업)로 제한됩니다. 다른 Microsoft 365 엔지니어와 Yammer 기술자는 고객 데이터에 대한 제로 스와딩 액세스를 하게 됩니다. 제한된 수의 승인자가 있는 Lockbox와 유사한 승인 기반의 Just-In-Time 액세스 제어 시스템을 사용하여 액세스를 요청해야 합니다. 승인자는 요청(예: 요청이 필요, 비즈니스 사례, 시간 등에 따라 합법적인지 확인)을 확인한 다음 요청을 승인하거나 거부합니다. 요청이 승인되면 정의된 제한된 시간 동안 JIT 액세스 권한이 부여됩니다. 액세스 시간이 초과되면 액세스가 자동으로 만료됩니다.

다른 Microsoft 365 서비스와 Yammer 프로덕션 환경에 대한 모든 액세스는 다단계 인증을 사용하게 됩니다. 모든 액세스 및 명령 기록은 사용자에게 특성이 부여되어 있으며 보안 팀에서 정기적으로 Yammer 기록됩니다.

관리 및 관리 Yammer 대한 자세한 내용은 관리자 [도움말을 Yammer 참조하세요.](/yammer/yammer-landing-page)