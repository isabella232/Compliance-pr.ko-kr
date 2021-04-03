---
title: Microsoft 365의 데이터 복구
description: 이 문서에서는 Microsoft 365에서 데이터 복구 및 복구의 디자인 및 원칙에 대해 자세히 알아보습니다.
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
ms.openlocfilehash: 6e990facde47b07d50f594afb55353a5ef81dd78
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497621"
---
# <a name="data-resiliency-in-microsoft-365"></a><span data-ttu-id="ab788-103">Microsoft 365의 데이터 탄력성</span><span class="sxs-lookup"><span data-stu-id="ab788-103">Data resiliency in Microsoft 365</span></span>

<span data-ttu-id="ab788-104">클라우드 컴퓨팅의 복잡한 특성을 통해 Microsoft는 문제가 될 경우가 아니라 언제 문제가 될지 염두에 두는 것을 염두에 두고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-104">Given the complex nature of cloud computing, Microsoft is mindful that it's not a case of if things will go wrong, but rather when.</span></span> <span data-ttu-id="ab788-105">클라우드 서비스를 디자인하여 안정성을 극대화하고 문제가 발생하면 고객에게 부정적인 영향을 최소화합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-105">We design our cloud services to maximize reliability and minimize the negative effects on customers when things do go wrong.</span></span> <span data-ttu-id="ab788-106">복잡한 물리적 인프라를 활용하는 기존 전략을 넘어서 클라우드 서비스에 직접 중복을 구축했습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-106">We have moved beyond the traditional strategy of relying on complex physical infrastructure, and we have built redundancy directly into our cloud services.</span></span> <span data-ttu-id="ab788-107">당사는 서비스에 데이터 탄력성을 구축하고 고객에게 고가용성을 제공하는 덜 복잡한 물리적 인프라와 보다 지능적인 소프트웨어의 조합을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-107">We use a combination of less complex physical infrastructure and more intelligent software that builds data resiliency into our services and delivers high availability to our customers.</span></span>

## <a name="resiliency-and-recoverability-are-built-in"></a><span data-ttu-id="ab788-108">복구 및 복구 가능성은 기본 제공</span><span class="sxs-lookup"><span data-stu-id="ab788-108">Resiliency and recoverability are built-in</span></span>

<span data-ttu-id="ab788-109">복구 및 복구를 구축하는 과정은 하드웨어(인프라)가 실패하고, 사람이 실수를 하게 하며, 소프트웨어에 버그가 있을 경우를 가정하여 어느 시점에서나 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-109">Building in resiliency and recovery starts with the assumption that the underlying infrastructure and processes will fail at some point: hardware (infrastructure) will fail, humans will make mistakes, and software will have bugs.</span></span> <span data-ttu-id="ab788-110">소프트웨어 개발자가 클라우드 전에 이러한 문제를 생각하고 있지 않다고 말하기는 하지만 일반적인 IT 구현에서 이러한 문제를 처리하는 방식은 클라우드보다는 달랐습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-110">While it would be incorrect to say that software developers were not thinking about these things before the cloud, how these issues were handled in a typical IT implementation was different before the cloud:</span></span>

- <span data-ttu-id="ab788-111">첫째, 하드웨어 및 인프라 보호가 중요했습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-111">First, hardware and infrastructure protections were significant.</span></span> <span data-ttu-id="ab788-112">이 구조는 안정성이 99.99%인 데이터 센터를 확보하는 데 상당한 전원 및 네트워크 중복이 필요하며, 서버는 하드웨어 기반 클러스터링, 이중 전원 공급 장치, 이중 네트워크 인터페이스 등으로 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-112">This structure meant having datacenters with 99.99% reliability required significant power and network redundancy, and servers were implemented with hardware-based clustering, dual power supplies, dual network interfaces, and the like.</span></span>
- <span data-ttu-id="ab788-113">둘째, 프로세스가 가장 중시적입니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-113">Second, process was paramount.</span></span> <span data-ttu-id="ab788-114">운영 팀은 엄격한 절차를 유지 관리하고, 변경 창을 사용하며, 종종 상당한 프로젝트 관리 오버헤드가 일어났습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-114">Operations teams maintained rigorous procedures, change windows were employed, and there was often significant project management overhead.</span></span>
- <span data-ttu-id="ab788-115">셋째, 배포는 빠른 속도로 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-115">Third, deployment took place at a glacial pace.</span></span> <span data-ttu-id="ab788-116">소스를 소유하지 않고 코드를 배포하면 패치 릴리스를 기다리는 것이고 주 버전 릴리스에는 하드웨어 교체 및 상당한 자본 부과가 수반되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-116">Deploying code without owning the source meant waiting for patch releases, and major version releases involved hardware replacement and significant capital outlay.</span></span> <span data-ttu-id="ab788-117">또한 문제를 수정하는 유일한 방법은 롤백하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-117">Moreover, the only way to correct a problem was to roll back.</span></span> <span data-ttu-id="ab788-118">따라서 대부분의 IT 조직에서는 최신 작업을 방지하기 위해 주요 릴리스만 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-118">Thus, most IT organizations would deploy only major releases to avoid the work to keep up to date.</span></span>
- <span data-ttu-id="ab788-119">마지막으로 배포된 시스템의 규모와 상호 연결 수준은 지금까지는 현재보다 훨씬 더 작습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-119">Finally, the scale of deployed systems and the level of their interconnectedness was historically much smaller than it is now.</span></span>

<span data-ttu-id="ab788-120">오늘날 고객은 품질을 저해하지 않고도 Microsoft의 지속적인 혁신을 기대하며 이는 Microsoft의 서비스 및 소프트웨어가 복구 및 복구 기능을 염두에 두는 이유 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-120">Today, customers expect continuous innovation from Microsoft without compromising quality, and this is one of the reasons why Microsoft's services and software are built with resiliency and recoverability in mind.</span></span>

## <a name="microsoft-365-data-resiliency-principles"></a><span data-ttu-id="ab788-121">Microsoft 365 데이터 탄력성 원칙</span><span class="sxs-lookup"><span data-stu-id="ab788-121">Microsoft 365 data resiliency principles</span></span>

<span data-ttu-id="ab788-122">복구는 클라우드 기반 서비스가 특정 유형의 장애를 견디고 고객의 관점에서 완전히 작동할 수 있는 능력을 지어보는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-122">Resiliency refers to the ability of a cloud-based service to withstand certain types of failures and yet remain fully functional from the customers' perspective.</span></span> <span data-ttu-id="ab788-123">데이터 복구는 Microsoft 365 내에서 발생하는 오류에 상관없이 중요한 고객 데이터는 그대로 유지되는 것을 의미하며 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-123">Data resiliency means that no matter what failures occur within Microsoft 365, critical customer data remains intact and unaffected.</span></span> <span data-ttu-id="ab788-124">이를 위해 Microsoft 365 서비스는 다음 다섯 가지 특정 탄력성 원칙에 따라 설계됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-124">To that end, Microsoft 365 services have been designed around five specific resiliency principles:</span></span>

- <span data-ttu-id="ab788-125">중요하고 중요하지 않은 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-125">There is critical and non-critical data.</span></span> <span data-ttu-id="ab788-126">중요하지 않은 데이터(예: 메시지를 읽은지 여부)는 드물게 실패 시나리오에서 삭제될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-126">Non-critical data (for example, whether a message was read) can be dropped in rare failure scenarios.</span></span> <span data-ttu-id="ab788-127">중요한 데이터(예: 전자 메일 메시지와 같은 고객 데이터)는 극도의 비용으로 보호해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-127">Critical data (for example, customer data such as email messages) should be protected at extreme cost.</span></span> <span data-ttu-id="ab788-128">디자인 목표는 배달된 메일 메시지가 항상 중요하며 메시지를 읽은 경우와 같은 것은 중요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-128">As a design goal, delivered mail messages are always critical, and things like whether a message has been read is non-critical.</span></span>
- <span data-ttu-id="ab788-129">고객 데이터의 복사본을 서로 다른 장애 영역 또는 오류 도메인(예: 단일 자격 증명(프로세스, 서버 또는 운영자)에서 액세스할 수 있는 데이터 센터)로 분리하여 오류 분리를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-129">Copies of customer data must be separated into different fault zones or as many fault domains as possible (for example, datacenters, accessible by single credentials (process, server, or operator)) to provide failure isolation.</span></span> 
- <span data-ttu-id="ab788-130">중요한 고객 데이터는 Atomicity, Consistency, Isolation, Durability (DURABILITY)의 일부에 실패하는지 모니터링해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-130">Critical customer data must be monitored for failing any part of Atomicity, Consistency, Isolation, Durability (ACID).</span></span>
- <span data-ttu-id="ab788-131">고객 데이터는 손상으로부터 보호되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-131">Customer data must be protected from corruption.</span></span> <span data-ttu-id="ab788-132">적극적으로 검사하거나 모니터링하고 복구할 수 있으며 복구할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-132">It must be actively scanned or monitored, repairable, and recoverable.</span></span>
- <span data-ttu-id="ab788-133">대부분의 데이터 손실은 고객 작업으로 인한 결과로, 고객이 실수로 삭제된 항목을 복원할 수 있도록 하는 GUI를 사용하여 자체적으로 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-133">Most data loss results from customer actions, so allow customers to recover on their own using a GUI that enables them to restore accidentally deleted items.</span></span>

<span data-ttu-id="ab788-134">Microsoft 365는 강력한 테스트 및 유효성 검사와 함께 이러한 원칙에 대한 클라우드 서비스를 구축하여 지속적인 혁신 및 개선을 위한 플랫폼을 보장하면서 고객의 요구 사항을 충족하고 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab788-134">Through the building of our cloud services to these principles, coupled with robust testing and validation, Microsoft 365 is able to meet and exceed the requirements of customers while ensuring a platform for continuous innovation and improvement.</span></span>

## <a name="related-articles"></a><span data-ttu-id="ab788-135">관련 문서</span><span class="sxs-lookup"><span data-stu-id="ab788-135">Related articles</span></span>

- [<span data-ttu-id="ab788-136">데이터 손상 처리</span><span class="sxs-lookup"><span data-stu-id="ab788-136">Dealing with Data Corruption</span></span>](assurance-dealing-with-data-corruption.md)
- [<span data-ttu-id="ab788-137">맬웨어 및 랜섬웨어 보호</span><span class="sxs-lookup"><span data-stu-id="ab788-137">Malware and Ransomware Protection</span></span>](assurance-malware-and-ransomware-protection.md)
- [<span data-ttu-id="ab788-138">모니터링 및 자동 복구</span><span class="sxs-lookup"><span data-stu-id="ab788-138">Monitoring and Self-Healing</span></span>](assurance-monitoring-and-self-healing.md)
- [<span data-ttu-id="ab788-139">Exchange 데이터 탄력성</span><span class="sxs-lookup"><span data-stu-id="ab788-139">Exchange Data Resiliency</span></span>](assurance-exchange-data-resiliency.md)
