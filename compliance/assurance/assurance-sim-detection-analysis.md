---
title: 'Microsoft 보안 인시던트 관리: 검색 및 분석'
description: 이 문서에서는 Microsoft 온라인 서비스의 보안 인시던트 관리 감지 및 분석 프로세스에 대한 개요를 제공합니다.
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
ms.openlocfilehash: 445d812b33214a3d2287268b587607004ef96ab7
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377355"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a><span data-ttu-id="e3fef-103">Microsoft 보안 인시던트 관리: 검색 및 분석</span><span class="sxs-lookup"><span data-stu-id="e3fef-103">Microsoft security incident management: Detection and analysis</span></span>

<span data-ttu-id="e3fef-104">악의적인 활동을 감지하기 위해 각 Microsoft의 온라인 서비스는 보안 이벤트 및 기타 데이터를 중앙에서 기록하고 다양한 분석 기술을 수행하여 이상하거나 의심스러운 활동을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-104">To detect malicious activity, each of Microsoft's online services centrally logs security events and other data and perform various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="e3fef-105">로그 파일은 Microsoft 온라인 서비스 서버 및 인프라 장치에서 수집되고 중앙 및 통합 데이터베이스에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-105">Log files are collected from Microsoft online services servers and infrastructure devices and stored in central and consolidated databases.</span></span>

<span data-ttu-id="e3fef-106">Microsoft는 악의적인 활동을 감지하는 위험 기반 접근 방식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="e3fef-107">인시던트 데이터 및 위협 인텔리전스를 사용하여 검색을 정의하고 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="e3fef-108">숙련된 숙련된 숙련된 사용자로 된 팀을 고용하는 것은 검색 및 분석 단계에서 성공하기 위한 가장 중요한 기조 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="e3fef-109">Microsoft는 네트워크, 라우터, 방화벽, 부하 균형 조정기, 운영 체제 및 응용 프로그램을 포함하여 스택 내의 모든 구성 요소에 대한 역량을 쌓은 직원이 포함된 여러 서비스 팀을 사용하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-109">Microsoft employs multiple service teams that include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="e3fef-110">Microsoft 온라인 서비스의 보안 검색 메커니즘에는 다양한 원본에서 시작된 알림 및 알림도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-110">The security detection mechanisms in Microsoft online services also include notifications and alerts that are initiated by different sources.</span></span> <span data-ttu-id="e3fef-111">Microsoft 온라인 서비스 보안 대응 팀은 보안 인시던트 에스컬레이션 프로세스의 주요 오케스트레이터입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-111">Microsoft online services security response teams are the key orchestrators of the security incident escalation process.</span></span> <span data-ttu-id="e3fef-112">이러한 팀은 모든 에스컬레이터를 받고 보안 인시던트의 유효성을 분석하고 확인하는 업무를 담당합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-112">These teams receive all escalations and are responsible for analyzing and confirming the validity of the security incident.</span></span>

![보안 인시던트 관리 워크플로](../media/assurance-sim-workflow.png)

<span data-ttu-id="e3fef-114">검색의 기본 기조 중 하나는 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-114">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="e3fef-115">각 서비스 팀은 온라인 서비스 보안 팀의 요구 사항에 따라 서비스 내부에서 작업 또는 이벤트를 기록할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-115">Each service team is responsible to log any action or event inside the service based on the requirements from the online service security team.</span></span> <span data-ttu-id="e3fef-116">서로 다른 서비스 팀에서 만든 모든 로그는 미리 정의한 보안 및 검색 규칙을 사용하여 SIEM(보안 정보 및 이벤트 관리) 솔루션에서 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-116">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="e3fef-117">이러한 규칙은 이전 보안 인시던트에서 학습된 정보에 따라 보안 팀 권장 사항을 기반으로 진화하여 의심스러우거나 악의적인 활동이 있는지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-117">These rules evolve based on security team recommendations, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="e3fef-118">고객이 보안 인시던트가 진행 중이라 판단하면 Microsoft 커뮤니케이션 팀에 할당되어 모든 적절한 팀으로 에스컬레이터로 설정되는 Microsoft에서 지원 사례를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-118">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="e3fef-119">Azure, Dynamics 365 및 Microsoft 365 서비스 팀은 보안 모니터링 및 로깅을 통해 추세 분석에서 얻은 인텔리전스를 사용하여 공격 또는 보안 인시던트가 표시될 수 있는 Microsoft 온라인 서비스 정보 시스템의 비정상을 감지합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-119">Azure, Dynamics 365, and Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft online services information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="e3fef-120">Microsoft 온라인 서비스 시스템은 프로덕션 환경의 이러한 로그에서 중앙 로깅 서버로 출력을 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-120">Microsoft online services systems aggregate output from these logs in the production environment into centralized logging servers.</span></span> <span data-ttu-id="e3fef-121">이러한 중앙 로깅 서버에서는 프로덕션 환경 전체의 추세를 파악하기 위해 로그를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-121">From these centralized logging servers, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="e3fef-122">중앙 집중식 서버에 집계된 데이터는 고급 쿼리, 대시보드 작성 및 변이 및 악의적인 활동 감지를 위해 로깅 서비스로 안전하게 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-122">Data aggregated in the centralized servers are securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="e3fef-123">또한 이 서비스는 기계 학습을 사용하여 로그 출력에서 이 문제를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-123">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="e3fef-124">에스컬레이터 단계에서 보안 인시던트의 특성에 따라 보안 대응 팀은 Microsoft의 다양한 팀에서 하나 이상의 주제 전문가를 참여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-124">During the escalation phase and depending on the nature of the security incident, security response teams may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="e3fef-125">온라인 서비스 보안 및 규정 준수 팀</span><span class="sxs-lookup"><span data-stu-id="e3fef-125">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="e3fef-126">MSTIC(Microsoft Threat Intelligence Center)</span><span class="sxs-lookup"><span data-stu-id="e3fef-126">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="e3fef-127">MSRC(Microsoft Security Response Center)</span><span class="sxs-lookup"><span data-stu-id="e3fef-127">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="e3fef-128">CELA(회사, 외부 및 법률 업무)</span><span class="sxs-lookup"><span data-stu-id="e3fef-128">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="e3fef-129">Azure Security</span><span class="sxs-lookup"><span data-stu-id="e3fef-129">Azure Security</span></span>
- <span data-ttu-id="e3fef-130">Microsoft 365 및 기타</span><span class="sxs-lookup"><span data-stu-id="e3fef-130">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="e3fef-131">보안 대응 팀으로의 에스컬레이터가 발생하기 전에 서비스 팀은 다음과 같은 정의된 기준에 따라 보안 인시던트의 심각도 수준을 결정하고 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-131">Before an escalation to any security response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="e3fef-132">개인 정보</span><span class="sxs-lookup"><span data-stu-id="e3fef-132">Privacy</span></span>
- <span data-ttu-id="e3fef-133">영향</span><span class="sxs-lookup"><span data-stu-id="e3fef-133">Impact</span></span>
- <span data-ttu-id="e3fef-134">범위</span><span class="sxs-lookup"><span data-stu-id="e3fef-134">Scope</span></span>
- <span data-ttu-id="e3fef-135">영향을 받는 테넌트 수</span><span class="sxs-lookup"><span data-stu-id="e3fef-135">Number of affected tenants</span></span>
- <span data-ttu-id="e3fef-136">지역</span><span class="sxs-lookup"><span data-stu-id="e3fef-136">Region</span></span>
- <span data-ttu-id="e3fef-137">서비스</span><span class="sxs-lookup"><span data-stu-id="e3fef-137">Service</span></span>
- <span data-ttu-id="e3fef-138">인시던트 세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3fef-138">Details of the incident</span></span>
- <span data-ttu-id="e3fef-139">특정 고객 산업 또는 시장 규정.</span><span class="sxs-lookup"><span data-stu-id="e3fef-139">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="e3fef-140">인시던트 우선 순위는 인시던트의 기능 영향, 인시던트의 정보 영향 및 인시던트로부터의 복구 가능성 등 고유한 요인을 사용하여 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-140">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="e3fef-141">보안 인시던트에 대한 에스컬레이터를 받은 후 보안 팀은 Microsoft 온라인 서비스 보안 대응 팀, 서비스 팀 및 인시던트 커뮤니케이션 팀의 구성원으로 구성된 가상 팀(v-team)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-141">After receiving an escalation about a security incident, the security team organizes a virtual team (v-team) comprised of members from the Microsoft online service security response team, service teams, and the incident communication team.</span></span> <span data-ttu-id="e3fef-142">그런 다음 v-팀은 보안 인시던트의 정당성에 대해 확인하고 가양성은 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-142">The v-team must then confirm the legitimacy of the security incident and eliminate any false positives.</span></span> <span data-ttu-id="e3fef-143">준비 단계에서 결정된 표시기에서 제공하는 정보의 정확성이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-143">The accuracy of information provided by the indicators determined during the preparation phase is critical.</span></span> <span data-ttu-id="e3fef-144">v-team은 벡터 공격 범주별로 이 정보를 분석하여 보안 인시던트가 합법적인 문제인지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-144">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="e3fef-145">조사를 시작하면 보안 인시던트 대응 팀은 사례 관리 정책에 따라 인시던트에 대한 모든 정보를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-145">At the beginning of the investigation, the security incident response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="e3fef-146">사례가 진행될 때 당사는 지속적인 작업을 추적하고 인시던트 수명 주기 동안 이 데이터를 수집, 보존 및 보호하기 위한 증거 처리 표준을 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-146">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="e3fef-147">이러한 작업의 몇 가지 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-147">Some examples of these actions would include:</span></span>

- <span data-ttu-id="e3fef-148">인시던트 및 잠재적인 영향에 대한 간략한 설명을 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-148">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="e3fef-149">인시던트의 심각도 및 우선 순위는 잠재적인 영향을 평가하여 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-149">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="e3fef-150">인시던트 감지를 이행한 식별된 모든 표시기 목록</span><span class="sxs-lookup"><span data-stu-id="e3fef-150">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="e3fef-151">관련 인시던트 목록</span><span class="sxs-lookup"><span data-stu-id="e3fef-151">A list of any related incidents</span></span>
- <span data-ttu-id="e3fef-152">v-team에서 수행한 모든 작업 목록</span><span class="sxs-lookup"><span data-stu-id="e3fef-152">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="e3fef-153">모의 후 분석 및 향후 포렌식 조사를 위해 보존될 수집된 증거</span><span class="sxs-lookup"><span data-stu-id="e3fef-153">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="e3fef-154">권장되는 다음 단계 및 작업</span><span class="sxs-lookup"><span data-stu-id="e3fef-154">Recommended next steps and actions</span></span>

<span data-ttu-id="e3fef-155">보안 인시던트 확인 후 보안 대응 팀과 적절한 서비스 팀의 기본 목표는 공격을 방지하고, 공격으로부터 서비스를 보호하고, 전역적으로 더 큰 영향을 받지 않도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-155">After security incident confirmation, the primary goals of the security response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="e3fef-156">이와 동시에 적절한 엔지니어링 팀은 근본 원인을 파악하고 첫 번째 복구 계획을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-156">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="e3fef-157">다음 단계에서 보안 대응 팀은 보안 인시던트의 영향을 받는 고객(있는 경우)을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-157">In the next phase, the security response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="e3fef-158">효과 범위는 지역, 데이터 센터, 서비스, 서버 팜, 서버 등에서 결정하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-158">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="e3fef-159">영향을 받는 고객 목록은 서비스 팀과 해당 Microsoft 커뮤니케이션 팀이 컴파일한 후 계약 및 규정 준수 의무 내에서 고객 알림 프로세스를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fef-159">The list of affected customers is compiled by the service team and the corresponding Microsoft communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="e3fef-160">관련 문서</span><span class="sxs-lookup"><span data-stu-id="e3fef-160">Related articles</span></span>

- [<span data-ttu-id="e3fef-161">Microsoft 보안 인시던트 관리</span><span class="sxs-lookup"><span data-stu-id="e3fef-161">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="e3fef-162">Microsoft 보안 인시던트 관리: 준비</span><span class="sxs-lookup"><span data-stu-id="e3fef-162">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="e3fef-163">Microsoft 보안 인시던트 관리: 포함, 삭제 및 복구</span><span class="sxs-lookup"><span data-stu-id="e3fef-163">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="e3fef-164">Microsoft 보안 인시던트 관리: 인시던트 사후 활동</span><span class="sxs-lookup"><span data-stu-id="e3fef-164">Microsoft security incident management: Post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
- [<span data-ttu-id="e3fef-165">보안 이벤트 지원 티켓을 기록하는 방법</span><span class="sxs-lookup"><span data-stu-id="e3fef-165">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="e3fef-166">Azure 및 Dynamics 365 GDPR의 위반 알림</span><span class="sxs-lookup"><span data-stu-id="e3fef-166">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
