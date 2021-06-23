---
title: 보안 인프라 Microsoft 365 보안
description: Microsoft에서 클라우드 인프라를 보호하는 Microsoft 365 대해 자세히 알아보습니다.
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
ms.openlocfilehash: 224900bd60f2fd5637e7264f1aed98d5ff878b20
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089669"
---
# <a name="securing-the-microsoft-365-infrastructure"></a><span data-ttu-id="d8e8a-103">보안 인프라 Microsoft 365 보안</span><span class="sxs-lookup"><span data-stu-id="d8e8a-103">Securing the Microsoft 365 infrastructure</span></span>

<span data-ttu-id="d8e8a-104">Microsoft 365 전 세계 최대 기업 및 소비자 클라우드 서비스 중 하나인 이 서비스는 고객 기반, 제품 및 기능 모두에서 급속도로 성장하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-104">Microsoft 365 is one of the largest enterprise and consumer cloud services in the world and continues to grow rapidly, both in customer base, products, and features.</span></span> <span data-ttu-id="d8e8a-105">고객은 Microsoft 365 생산성 솔루션뿐 아니라 지속적으로 진화하는 사이버 위협 환경으로부터 가장 중요한 정보를 보호하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-105">Customers turn to Microsoft 365 not only for its world-class productivity solutions, but to help protect their most sensitive information from the constantly evolving cyber threat landscape.</span></span> <span data-ttu-id="d8e8a-106">고객 데이터를 안전하게 보호하고 고객 신뢰를 유지하는 것이 Microsoft의 최우선 과제입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-106">It is Microsoft's top priority to keep customer data secure and maintain customer trust.</span></span>

<span data-ttu-id="d8e8a-107">보안이 사후에 진행되는 경우 이러한 규모와 복잡성의 시스템을 보호할 수 없는 경우 초기 디자인 프로세스 중에 보안이 통합된 후에만 효과적입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-107">Securing a system of this scale and complexity is not possible if security is an afterthought, it is only effective if security is integrated during the initial design process.</span></span> <span data-ttu-id="d8e8a-108">자동화된 시스템과 고도로 숙련된 엔지니어의 프롬프트 응답이 있는 강력한 위협 감지 시스템이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-108">It requires a robust threat detection system with prompt responses from both automated systems and highly skilled engineers.</span></span> <span data-ttu-id="d8e8a-109">이러한 시스템의 지속적인 평가 및 유효성 검사는 보안 구성이 그대로 유지되고 이전에 알려지지 않은 취약점이 식별되도록 하는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-109">Continuous assessment and validation of these systems is essential to ensure secure configurations remain intact and previously unknown vulnerabilities are identified.</span></span>

## <a name="core-security-principles"></a><span data-ttu-id="d8e8a-110">핵심 보안 원칙</span><span class="sxs-lookup"><span data-stu-id="d8e8a-110">Core security principles</span></span>

<span data-ttu-id="d8e8a-111">7개의 보안 원칙은 위협으로부터  Microsoft 365 서비스를 보호하고, 위협을  감지 및 대응하고, 해당 평가  결과에 따라 보안 상태를 지속적으로 평가하고 서비스를 개선하는 프레임워크의 토대를 마련합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-111">Seven security principles lay the foundation for our framework of *protecting* the Microsoft 365 services from threats, *detecting and responding* to any threats, and continuously *assessing* the security posture and improving services based on the results of those assessments.</span></span>

- <span data-ttu-id="d8e8a-112">**데이터 개인 정보** 보호: 고객이 데이터를 소유하고 있으며 Microsoft는 관리인입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-112">**Data privacy**: Customers own their data and Microsoft is the custodian.</span></span> <span data-ttu-id="d8e8a-113">Microsoft 365 서비스는 고객이 명시적으로 요청하고 승인하지 않는 한 엔지니어가 고객 데이터에 액세스하지 않고 작동하도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-113">Microsoft 365 services are designed to operate without engineers accessing customer data, unless explicitly requested and approved by the customer.</span></span>
- <span data-ttu-id="d8e8a-114">**위반 가정:** 직원 및 서비스는 손상이 실제 가능성이 있는 것으로 취급됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-114">**Assume breach**: Personnel and services are treated as though compromise is a real possibility.</span></span>
- <span data-ttu-id="d8e8a-115">**최소 권한:** 리소스에 대한 액세스 및 사용 권한은 필요한 작업을 수행하는 데 필요한 권한으로만 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-115">**Least privilege**: Access and permissions to resources are limited to only what is necessary to perform needed tasks.</span></span>
- <span data-ttu-id="d8e8a-116">**위반 경계:** 한 경계의 ID 및 인프라가 다른 경계의 리소스와 격리됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-116">**Breach boundaries**: Identities and infrastructure in one boundary are isolated from resources in other boundaries.</span></span> <span data-ttu-id="d8e8a-117">한 경계가 손상되면 다른 경계가 손상되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-117">Compromise of one boundary should not lead to compromise of another.</span></span>
- <span data-ttu-id="d8e8a-118">**서비스 패브릭 통합 보안:** 보안 우선 순위 및 요구 사항이 새로운 기능 디자인에 기본 제공되어 각 서비스를 통해 강력한 보안 자세가 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-118">**Service fabric integrated security**: Security priorities and requirements are built into the design of new features and capabilities, ensuring that a strong security posture scales with each service.</span></span>
- <span data-ttu-id="d8e8a-119">**자동화** 및 자동: Microsoft는 지능적으로 자동으로 서비스 보안을 적용할 수 있는 지속형 제품 및 아키텍처를 개발하는 동시에 Microsoft 엔지니어가 대규모로 보안 위협에 대한 대응을 안전하게 관리할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-119">**Automated and automatic**: Microsoft focuses on developing durable products and architectures that can intelligently and automatically enforce service security, while giving Microsoft engineers the ability to safely manage responses to security threats at scale.</span></span>
- <span data-ttu-id="d8e8a-120">**적응형 보안:** Microsoft 보안 기능은 기계 학습 모델, 일상적인 침투 테스트 및 자동화된 평가를 통해 조정되고 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-120">**Adaptive security**: Microsoft security capabilities adapt to and are enhanced by machine learning models, routine penetration testing, and automated assessments.</span></span>

## <a name="protection"></a><span data-ttu-id="d8e8a-121">보호</span><span class="sxs-lookup"><span data-stu-id="d8e8a-121">Protection</span></span>

### <a name="access-control"></a><span data-ttu-id="d8e8a-122">액세스 제어</span><span class="sxs-lookup"><span data-stu-id="d8e8a-122">Access control</span></span>

<span data-ttu-id="d8e8a-123">기본적으로 Microsoft 365 서비스를 개발하고 유지 관리하는 담당자는 서비스 인프라에 ZSA(Zero Standing Access)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-123">By default, personnel responsible for developing and maintaining Microsoft 365 services have Zero Standing Access (ZSA) to the service infrastructure.</span></span> <span data-ttu-id="d8e8a-124">Microsoft는 최상의 엔지니어만 고용하고 엄격한 백그라운드 검사가 필요하기는 하지만 Microsoft는 운영 서비스에서 기본적으로 신뢰할 수 있는 것으로 가정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-124">While Microsoft strives to hire only the best engineers and rigorous background checks are required, Microsoft does not assume that they are trusted by default in operating services.</span></span> <span data-ttu-id="d8e8a-125">또한 엔지니어가 권한 있는 액세스가 승인되면 특정 서비스 인프라 범위에 필요한 작업만 수행할 수 있도록 제한된 기간 동안만 액세스 권한이 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-125">Additionally, when engineers are approved for privileged access, they are only granted access for a limited duration to perform only the actions needed for a specific scope of the service infrastructure.</span></span> <span data-ttu-id="d8e8a-126">Microsoft는 이러한 정책을 Lockbox라는 시스템을 통해 구현되는 JIT(Just-In-Time) 및 JEA(Just-Enough-Access)라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-126">Microsoft refers to these policies as Just-in-Time (JIT) and Just-Enough-Access (JEA) which are implemented through a system called Lockbox.</span></span>

<span data-ttu-id="d8e8a-127">관리자 권한 획득을 위해 Microsoft 엔지니어는 특정 작업에 대한 요청을 제출하고 이를 수행할 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-127">To acquire elevated privileges, Microsoft engineers submit a request for the specific task and specify the time frame to perform it.</span></span> <span data-ttu-id="d8e8a-128">승인되면 Lockbox는 요청된 작업만 수행할 수 있는 특수 JIT 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-128">Once approved, Lockbox generates a specialized JIT account with the ability to perform only the requested task.</span></span> <span data-ttu-id="d8e8a-129">작업은 일반적으로 필요한 문제 해결 또는 복구를 안전하게 수행하는 자동화된 워크플로 형식을 취합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-129">Actions usually take the form of automated workflows that securely perform any troubleshooting or recovery required.</span></span> <span data-ttu-id="d8e8a-130">인프라에 대한 직접 액세스가 필요한 경우는 드물지만 엄격하게 모니터링되는 PAW(Privileged Access Workstation)가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-130">In rare instances when direct access to the infrastructure is necessary, strictly monitored Privileged Access Workstations (PAWs) are required.</span></span>

<span data-ttu-id="d8e8a-131">Rogue 사용자 및 손상된 계정은 모든 조직에서 실제 가능성이 있으며, 액세스 제어 시스템은 이러한 위협으로부터 보호하도록 디자인되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-131">Rogue users and compromised accounts are a real possibility in any organization, and our access control system are designed to protect against these threats.</span></span>

<span data-ttu-id="d8e8a-132">액세스 제어에 대한 자세한 내용은 ID 및 액세스 관리 개요 [를 참조하세요.](assurance-identity-and-access-management.md)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-132">For more information about access control, see [Identity and access management overview](assurance-identity-and-access-management.md).</span></span>

### <a name="encryption"></a><span data-ttu-id="d8e8a-133">암호화</span><span class="sxs-lookup"><span data-stu-id="d8e8a-133">Encryption</span></span>

<span data-ttu-id="d8e8a-134">액세스 제어는 Microsoft 365 보호하는 데 중요한 역할을 하지만 데이터 수명 주기 동안 암호화를 사용하여 Microsoft 고객의 기밀성 및 개인 정보를 추가로 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-134">While access controls provide a vital role in defending Microsoft 365 services, encryption is used throughout the data lifecycle to further protect confidentiality and privacy for Microsoft customers.</span></span>

<span data-ttu-id="d8e8a-135">클라이언트 컴퓨터, Microsoft 365 서버 및 Microsoft 365 서버 간에 전송되는 데이터는 TLS 1.2를 사용하여 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-135">Data in transit between client machines, Microsoft 365 servers, and non-Microsoft 365 servers is encrypted using TLS 1.2.</span></span> <span data-ttu-id="d8e8a-136">사용 가능한 경우 향상된 프로토콜을 추가하고 필요한 경우 약한 프로토콜을 제거하여 사용 가능한 암호 및 프로토콜을 정기적으로 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-136">We regularly review the ciphers and protocols in use, adding improved protocols when available and removing weaker ones as needed.</span></span>

<span data-ttu-id="d8e8a-137">Microsoft 서버의 미사용 고객 콘텐츠는 BitLocker를 사용하여 볼륨 수준에서 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-137">Customer content at rest on Microsoft servers is encrypted at the volume-level using BitLocker.</span></span> <span data-ttu-id="d8e8a-138">응용 프로그램 수준 암호화는 Microsoft 또는 고객이 관리하는 키를 사용하여 추가로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-138">Application-level encryption can additionally be applied using keys managed by either Microsoft or the customer.</span></span> <span data-ttu-id="d8e8a-139">Microsoft 관리 키에 대한 액세스는 JIT 및 JEA 프로세스를 통해 승인되고 승인된 경우만 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-139">Access to Microsoft-managed keys is only possible when authorized and approved through the JIT and JEA process.</span></span>

<span data-ttu-id="d8e8a-140">암호화의 암호화에 대한 Microsoft 365 암호화 및 키 관리 [개요를 참조하세요.](assurance-encryption.md)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-140">For more information about encryption in Microsoft 365, see [Encryption and key management overview](assurance-encryption.md).</span></span>

### <a name="network-isolation"></a><span data-ttu-id="d8e8a-141">네트워크 고리</span><span class="sxs-lookup"><span data-stu-id="d8e8a-141">Network isolation</span></span>

<span data-ttu-id="d8e8a-142">최소 권한의 원칙에 따라 Microsoft 365 인프라의 여러 부분 간의 통신을 작동에 필요한 것으로만 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-142">In line with the principle of least privilege, Microsoft 365 restricts communication between different parts of the service infrastructure to only what is necessary to operate.</span></span> <span data-ttu-id="d8e8a-143">모든 네트워크 트래픽은 기본적으로 거부되고 명시적으로 정의된 통신만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-143">All network traffic is denied by default, with only explicitly defined communication being allowed.</span></span> <span data-ttu-id="d8e8a-144">이 제한은 인프라 전체에서 위반 경계를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-144">This restriction establishes breach boundaries throughout the infrastructure.</span></span> <span data-ttu-id="d8e8a-145">Teams 기능을 수용하기 위해 새 네트워크 경로를 추가하려면 요청을 열기 전에 먼저 평가 및 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-145">Teams that would like to add new network paths to accommodate a new feature to their service must have the request evaluated and approved before it can be opened.</span></span>

<span data-ttu-id="d8e8a-146">네트워크의 네트워크 Microsoft 365 대한 자세한 내용은 Microsoft 365 [참조하세요.](/microsoft-365/enterprise/microsoft-365-isolation-controls)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-146">For more information about network isolation in Microsoft 365, see [Microsoft 365 isolation controls](/microsoft-365/enterprise/microsoft-365-isolation-controls).</span></span>

## <a name="detection--response"></a><span data-ttu-id="d8e8a-147">검색 & 응답</span><span class="sxs-lookup"><span data-stu-id="d8e8a-147">Detection & Response</span></span>

### <a name="security-monitoring"></a><span data-ttu-id="d8e8a-148">보안 모니터링</span><span class="sxs-lookup"><span data-stu-id="d8e8a-148">Security monitoring</span></span>

<span data-ttu-id="d8e8a-149">Microsoft의 대규모 보안 모니터링은 자동화된 클라우드 기반 솔루션을 사용하여 매우 정확한 경고를 생성해야만 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-149">Security monitoring at Microsoft's massive scale is only possible by generating highly accurate alerts using automated cloud-based solutions.</span></span> <span data-ttu-id="d8e8a-150">핵심 인프라 전체에서 수집된 각 서비스 및 원격 분석 데이터의 감사 로그는 거의 실시간에 가까운 중앙 집중식 처리 및 경고 솔루션으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-150">Audit logs from each service and telemetry data gathered from throughout the core infrastructure is sent to a proprietary centralized near-real-time processing and alerting solution.</span></span>

<span data-ttu-id="d8e8a-151">검색된 위협은 가능한 경우 자동으로 트리거된 작업을 사용하여 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-151">Detected threats are remediated using automatically triggered actions when possible.</span></span> <span data-ttu-id="d8e8a-152">자동화된 솔루션이 문제를 해결하지 못하거나 해결하지 못하면 Microsoft 엔지니어가 즉시 조치를 취하여 위협을 완화합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-152">When automated solutions are unsuccessful or incapable of resolving the issue, on-call Microsoft engineers immediately take action to mitigate the threat.</span></span>

<span data-ttu-id="d8e8a-153">보안 모니터링의 보안 모니터링에 대한 자세한 Microsoft 365 보안 모니터링 [개요를 참조하세요.](assurance-security-monitoring.md)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-153">For more information about security monitoring in Microsoft 365, see [Security monitoring overview](assurance-security-monitoring.md).</span></span>

## <a name="assessment"></a><span data-ttu-id="d8e8a-154">평가</span><span class="sxs-lookup"><span data-stu-id="d8e8a-154">Assessment</span></span>

### <a name="automated-assessments"></a><span data-ttu-id="d8e8a-155">자동화된 평가</span><span class="sxs-lookup"><span data-stu-id="d8e8a-155">Automated assessments</span></span>

<span data-ttu-id="d8e8a-156">시스템 설계 방식에 관계없이 시간이 경과하면 의도적인 의도치 않은 구성 드리프트로 인해 보안이 저하될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-156">Regardless of how a system is designed, the security posture can degrade due to intentional and unintentional configuration drift over time.</span></span> <span data-ttu-id="d8e8a-157">자동화된 도구는 Microsoft 365 잘못 구성한 서비스를 찾아서 시스템과 시스템을 지속적으로 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-157">Automated tools constantly assess Microsoft 365 systems that look for unpatched and misconfigured services.</span></span> <span data-ttu-id="d8e8a-158">이 평가를 패치, 바이러스 백신, 취약성 및 PAVC(구성 검사)라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-158">This assessment is often referred to as patching, anti-virus, vulnerability, and configuration scanning (PAVC).</span></span>

<span data-ttu-id="d8e8a-159">또한 아키텍처의 유효성을 검사하여 사용되지 않는 열린 포트와 같은 인스턴스 및 관리자 액세스 권한이 있는 계정을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-159">Our architecture is also frequently validated, identifying instances such as unused open ports and accounts with standing administrative access.</span></span> <span data-ttu-id="d8e8a-160">미리 정의된 원하는 상태로부터 드리프트된 서비스는 자동으로 다시 정렬됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-160">Any services that drift from a pre-defined desired state are automatically brought back into alignment.</span></span>

<span data-ttu-id="d8e8a-161">보안 모니터링의 보안 모니터링에 대한 자세한 Microsoft 365 취약성 관리 [개요를 참조하세요.](assurance-vulnerability-management.md)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-161">For more information about security monitoring in Microsoft 365, see [Vulnerability management overview](assurance-vulnerability-management.md).</span></span>

### <a name="attack-simulation-and-penetration-testing"></a><span data-ttu-id="d8e8a-162">공격 시뮬레이션 및 침투 테스트</span><span class="sxs-lookup"><span data-stu-id="d8e8a-162">Attack simulation and penetration testing</span></span>

<span data-ttu-id="d8e8a-163">Microsoft 365 가장 우선 순위는 공격이 방어에 침투하지 못하게 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-163">Microsoft 365's top priority is to prevent attacks from infiltrating defenses.</span></span> <span data-ttu-id="d8e8a-164">Microsoft 365 이전에 알려지지 않은 취약점을 식별하고 보안 모니터링 기능을 개선하기 위해 다양한 데이터의 일정 스트림을 제공하기 위해 시뮬레이트된 공격을 지속적으로 수행하고 있는 보안 전문가의 전담 팀이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-164">Microsoft 365 has a dedicated team of security experts who are constantly conducting simulated attacks to identify previously unknown vulnerabilities and to provide a constant stream of rich data to improve security monitoring capabilities.</span></span> <span data-ttu-id="d8e8a-165">이러한 시뮬레이션된 공격은 자주 자동화된 소규모 공격과 전문가 중심 심층 분석의 형태를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-165">These simulated attacks take the form of frequent automated small-scale attacks and expert-driven deep dives.</span></span> <span data-ttu-id="d8e8a-166">이러한 활동에서 Microsoft는 공격자 감지, 대응 및 지우기 기능을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-166">From these activities, Microsoft evaluates the ability to detect, respond, and evict attackers.</span></span>

<span data-ttu-id="d8e8a-167">에서 보안 모니터링에 대한 자세한 Microsoft 365 에서 [공격 시뮬레이션을 Microsoft 365.](assurance-monitoring-and-testing.md)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-167">For more information about security monitoring in Microsoft 365, see [Attack simulation in Microsoft 365](assurance-monitoring-and-testing.md).</span></span>

## <a name="resources"></a><span data-ttu-id="d8e8a-168">리소스</span><span class="sxs-lookup"><span data-stu-id="d8e8a-168">Resources</span></span>

[<span data-ttu-id="d8e8a-169">배경: 서비스 기반 인프라 Microsoft 365 보안</span><span class="sxs-lookup"><span data-stu-id="d8e8a-169">Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service</span></span>](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
