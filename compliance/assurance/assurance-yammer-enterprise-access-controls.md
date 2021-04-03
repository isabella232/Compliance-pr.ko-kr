---
title: Microsoft 365 Yammer 엔터프라이즈 액세스 제어
description: 이 문서에는 프로덕션 환경의 엔터프라이즈 액세스 Yammer 대한 간략한 요약이 포함되어 있습니다.
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
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497349"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="0a67d-103">Yammer 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="0a67d-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="0a67d-104">프로덕션 환경에 대한 물리적 및 Yammer 액세스는 소수의 사용자(인프라 및 운영)로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="0a67d-105">다른 Microsoft 365 엔지니어와 Yammer 고객 데이터에 대한 액세스 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="0a67d-106">제한된 수의 승인자가 있는 Lockbox와 유사한 승인 기반의 정식 액세스 제어 시스템을 사용하여 액세스를 요청해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="0a67d-107">승인자는 요청(예: 요청이 필요, 비즈니스 사례, 시간 등에 따라 합법적인지 확인)을 확인한 다음 요청을 승인하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="0a67d-108">요청이 승인되면 정의된 제한된 시간 동안 JIT 액세스 권한이 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="0a67d-109">액세스 시간이 초과되면 액세스가 자동으로 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="0a67d-110">다른 Microsoft 365 서비스와 Yammer 프로덕션 환경에 대한 모든 액세스는 다단계 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="0a67d-111">모든 액세스 및 명령 기록은 사용자의 특성이 있으며 보안 팀에서 정기적으로 Yammer 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="0a67d-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="0a67d-112">관리 및 관리 Yammer 대한 자세한 내용은 관리자 Yammer [참조하세요.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="0a67d-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>