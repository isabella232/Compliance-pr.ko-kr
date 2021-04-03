---
title: 'Microsoft 365 보안 인시던트 관리: 포함, 지우기 및 복구'
description: 이 문서에서는 Microsoft 365의 보안 인시던트 관리 포함, 삭제 및 복구 프로세스에 대한 개요를 제공합니다.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 7fff9c1909f0acd076945e3d569b143fe2324c0f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496725"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a><span data-ttu-id="bf188-103">Microsoft 365 보안 인시던트 관리: 포함, 지우기 및 복구</span><span class="sxs-lookup"><span data-stu-id="bf188-103">Microsoft 365 security incident management: Containment, eradication, and recovery</span></span>

<span data-ttu-id="bf188-104">Microsoft 365 보안 대응 팀, 서비스 팀 및 기타에서 수행한 분석에 따라 보안 인시던트의 영향을 최소화하기 위해 적절한 포함 및 복구 계획을 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-104">Based on the analysis performed by the Microsoft 365 Security Response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident.</span></span> <span data-ttu-id="bf188-105">그런 다음 적절한 서비스 팀은 Microsoft 365 보안 대응 팀의 지원을 통해 프로덕션에서 해당 계획을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-105">The appropriate service teams then apply that plan in production with support from the Microsoft 365 Security Response team.</span></span>

## <a name="containment"></a><span data-ttu-id="bf188-106">포함</span><span class="sxs-lookup"><span data-stu-id="bf188-106">Containment</span></span>

<span data-ttu-id="bf188-107">보안 인시던트가 감지된 후 침입을 포함해야 적대가 더 많은 리소스에 액세스하거나 더 많은 손상을 일으킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-107">After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage.</span></span> <span data-ttu-id="bf188-108">보안 인시던트 대응 절차의 주요 목표는 고객 또는 해당 데이터 또는 Microsoft 시스템, 서비스 및 응용 프로그램에 대한 영향을 제한하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-108">The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.</span></span>

## <a name="eradication"></a><span data-ttu-id="bf188-109">지우기</span><span class="sxs-lookup"><span data-stu-id="bf188-109">Eradication</span></span>

<span data-ttu-id="bf188-110">지우기 는 높은 수준의 신뢰도로 보안 인시던트의 근본 원인을 제거하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-110">Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence.</span></span> <span data-ttu-id="bf188-111">목표는 다음 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-111">The goal is two-fold:</span></span>

- <span data-ttu-id="bf188-112">환경에서 사적을 완전히 제거</span><span class="sxs-lookup"><span data-stu-id="bf188-112">to evict the adversary completely from the environment</span></span>
- <span data-ttu-id="bf188-113">를 사용하여 악의적인 사용자가 환경을 다시 사용하도록 설정할 수 있는 취약성(알려진 경우)을 완화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-113">to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.</span></span>

<span data-ttu-id="bf188-114">인시던트의 특성, 보안 인시던트의 범위, 침투 깊이 및 가능한 상황에 따라 Microsoft 365 보안 대응 팀은 서비스 팀이 지우기 기술을 채택하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-114">Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the Microsoft 365 Security Response team will recommend that service teams adopt eradication techniques.</span></span> <span data-ttu-id="bf188-115">이러한 지우기 단계로 인해 발생할 수 있는 잠재적인 비즈니스 영향을 고려하여 이러한 결정은 서비스 팀과 Microsoft 365 보안 대응 팀이 임원 인시던트 관리자의 자세한 분석 및 승인(필요한 경우)한 후에 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-115">Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the Microsoft 365 Security Response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).</span></span>

## <a name="recovery"></a><span data-ttu-id="bf188-116">복구</span><span class="sxs-lookup"><span data-stu-id="bf188-116">Recovery</span></span>

<span data-ttu-id="bf188-117">응답 팀이 적대적이 환경에서 제거되고 알려진 모든 취약한 경로를 제거했다는 합리적인 수준의 신뢰를 얻게 하여 개별 서비스 팀은 서비스를 알려진 적절한 구성으로 가져오기 위한 복원 단계를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-117">As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration.</span></span> <span data-ttu-id="bf188-118">이러한 복원 단계는 Microsoft 365 보안 대응 팀과 협의합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-118">These restoration steps will be in consultation with the Microsoft 365 Security Response team.</span></span> <span data-ttu-id="bf188-119">이 활동에는 마지막으로 알려진 서비스의 양호한 상태 식별, 백업에서 이 상태로 복원, 복원된 상태의 취약한 공격 경로 검사 등이 포함됩니다. Microsoft 365 보안 대응 팀은 서비스 팀과 협의하여 환경에 가장 적합한 복구 계획을 결정할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-119">This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The Microsoft 365 Security Response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.</span></span>

<span data-ttu-id="bf188-120">복구의 주요 측면은 복구 계획이 성공적으로 실행되고 환경에 위반 징후가 없는지 확인할 수 있는 향상된 보안 및 제어 기능을 배치하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-120">A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.</span></span>

## <a name="customer-notification-of-security-incident"></a><span data-ttu-id="bf188-121">보안 인시던트에 대한 고객 알림</span><span class="sxs-lookup"><span data-stu-id="bf188-121">Customer notification of security incident</span></span>

<span data-ttu-id="bf188-122">Microsoft가 보안 인시던트가 발생했다고 판단하면 Microsoft는 부당하게 지연되고 계약 및 규정 준수 요구 사항 내에서 사용자에게 알릴 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-122">If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to.</span></span> <span data-ttu-id="bf188-123">영향을 받는 모든 테넌트 식별 후 Microsoft 365 CxP(사용자 환경) 커뮤니케이션 팀은 영향을 받는 테넌트에 적용될 수 있는 관련 규정을 식별하기 위해 작업합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-123">After identifying all affected tenants, the Microsoft 365 Customer Experience (CxP) Communications team works to identify any relevant regulations that might apply to affected tenants.</span></span> <span data-ttu-id="bf188-124">Microsoft 365 CxP 커뮤니케이션 팀은 해당 규정에 정의된 적절한 통신 채널을 사용하여 해당 테넌트 담당자에게 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-124">The Microsoft 365 CxP Communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.</span></span>

<span data-ttu-id="bf188-125">알림에는 인시던트에 대한 자세한 정보(예: 인시던트 설명, 고객 데이터에 대한 영향, 있는 경우, Microsoft에서 취한 작업 및/또는 고객이 문제를 해결하고 재발을 방지하기 위해 취해야 하는 제안된 작업)가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-125">Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence.</span></span> <span data-ttu-id="bf188-126">알림은 Microsoft 365 테넌트의 지정된 관리자에게 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-126">Notification will be delivered to the designated administrator(s) of the Microsoft 365 tenant.</span></span> <span data-ttu-id="bf188-127">알림을 수신하려면 관리자가 테넌트 프로필에서 정확한 연락처 정보를 제공하고 유지 관리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf188-127">To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles.</span></span> <span data-ttu-id="bf188-128">또한 인시던트의 특성에 따라 Microsoft 365 서비스 상태 대시보드를 통해 고객에게 알림을 전달할 수도[있습니다.](http://status.yammer.com/)</span><span class="sxs-lookup"><span data-stu-id="bf188-128">In addition, depending on the nature of the incident, customers can also be notified via the Microsoft 365 Service Health Dashboard[.](http://status.yammer.com/)</span></span>

## <a name="related-articles"></a><span data-ttu-id="bf188-129">관련 문서</span><span class="sxs-lookup"><span data-stu-id="bf188-129">Related articles</span></span>

- [<span data-ttu-id="bf188-130">Microsoft 365 보안 인시던트 관리</span><span class="sxs-lookup"><span data-stu-id="bf188-130">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="bf188-131">Microsoft 365 보안 인시던트 관리 준비</span><span class="sxs-lookup"><span data-stu-id="bf188-131">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="bf188-132">Microsoft 365 보안 인시던트 관리 감지 및 분석</span><span class="sxs-lookup"><span data-stu-id="bf188-132">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="bf188-133">Microsoft 365 보안 인시던트 관리 사후 활동</span><span class="sxs-lookup"><span data-stu-id="bf188-133">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
