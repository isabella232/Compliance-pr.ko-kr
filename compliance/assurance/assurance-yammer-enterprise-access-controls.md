---
title: Microsoft 365 Yammer 엔터프라이즈 액세스 제어
description: 이 문서에는 프로덕션 환경의 액세스 Yammer Enterprise 대한 간략한 요약이 포함되어 있습니다.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ac02d8ba8719d9ef78a24bee37732007af7cba8b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573576"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer 액세스 제어 

프로덕션 환경에 대한 물리적 및 Yammer 액세스는 소수의 사용자(인프라 및 운영)로 제한됩니다. 다른 Microsoft 365 엔지니어와 Yammer 고객 데이터에 대한 액세스 권한이 없습니다. 제한된 수의 승인자가 있는 Lockbox와 유사한 승인 기반의 정식 액세스 제어 시스템을 사용하여 액세스를 요청해야 합니다. 승인자는 요청(예: 요청이 필요, 비즈니스 사례, 시간 등에 따라 합법적인지 확인)을 확인한 다음 요청을 승인하거나 거부합니다. 요청이 승인되면 정의된 제한된 시간 동안 JIT 액세스 권한이 부여됩니다. 액세스 시간이 초과되면 액세스가 자동으로 만료됩니다.

다른 Microsoft 365 서비스와 Yammer 프로덕션 환경에 대한 모든 액세스는 다단계 인증을 사용 합니다. 모든 액세스 및 명령 기록은 사용자에게 특성이 부여되어 있으며 보안 팀에서 정기적으로 Yammer 검토합니다.

관리 및 관리 Yammer 대한 자세한 내용은 관리자 Yammer [참조하세요.](/yammer/yammer-landing-page)