---
title: FedRAMP(Federal Risk and Authorization Management Program)
description: Microsoft는 미국 연방 위험 및 권한 부여 관리 프로그램 P-ATOS 및 ATOS를 부여했습니다.
keywords: Microsoft 365, 규정 준수, 제안
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: d9b7988b2ab236a26aad0981879f9b49c9ed028a
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384948"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a><span data-ttu-id="a69bf-104">FedRAMP(Federal Risk and Authorization Management Program)</span><span class="sxs-lookup"><span data-stu-id="a69bf-104">Federal Risk and Authorization Management Program (FedRAMP)</span></span>

## <a name="fedramp-overview"></a><span data-ttu-id="a69bf-105">FedRAMP 개요</span><span class="sxs-lookup"><span data-stu-id="a69bf-105">FedRAMP overview</span></span>

<span data-ttu-id="a69bf-106">미국 FedRAMP(Federal Risk and Authorization Management Program)는 FISMA(Federal Information Security Management Act)에 따라 클라우드 컴퓨팅 제품 및 서비스를 평가, 모니터링 및 인증하기 위한 표준화된 접근 방식을 제공하고 연방 기관의 보안 클라우드 솔루션 채택을 가속화하기 위해 설립되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-106">The US Federal Risk and Authorization Management Program (FedRAMP) was established to provide a standardized approach for assessing, monitoring, and authorizing cloud computing products and services under the Federal Information Security Management Act (FISMA), and to accelerate the adoption of secure cloud solutions by federal agencies.</span></span>

<span data-ttu-id="a69bf-107">이제 Office 및 예산을 관리하고 예산을 세우려면 모든 정부 기관이 FedRAMP를 사용하여 클라우드 서비스의 보안 유효성을 검사해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-107">The Office of Management and Budget now requires all executive federal agencies to use FedRAMP to validate the security of cloud services.</span></span> <span data-ttu-id="a69bf-108">(다른 기관에서도 채택하고 있으므로 공공 부문의 다른 영역에서도 유용합니다.) NIST(National Institute of Standards and Technology) SP 800-53은 필수 표준을 설정하고, 정보 시스템의 보안 범주(기밀성, 무결성 및 가용성)를 설정하여 정보 및 정보 시스템이 손상된 경우 조직에 미칠 수 있는 영향을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-108">(Other agencies have also adopted it, so it is useful in other areas of the public sector as well.) The National Institute of Standards and Technology (NIST) SP 800-53 sets the mandatory standards, establish security categories of information systems—confidentiality, integrity, and availability—to assess the potential impact on an organization should its information and information systems be compromised.</span></span> <span data-ttu-id="a69bf-109">FedRAMP는 클라우드 서비스 공급자(CSP)가 해당 표준을 충족하는지 인증하는 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-109">FedRAMP is the program that certifies that a cloud service provider (CSP) meets those standards.</span></span>

<span data-ttu-id="a69bf-110">연방 기관에 서비스를 판매하기를 원하는 CSP는 FedRAMP 규정 준수를 입증하기 위해 세 가지 경로를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-110">CSPs desiring to sell services to a federal agency can take three paths to demonstrate FedRAMP compliance:</span></span>

- <span data-ttu-id="a69bf-111">JAB(합동 인증 위원회)에서 P-ATO(Provisional Authority to Operate)를 획득합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-111">Earn a Provisional Authority to Operate (P-ATO) from the Joint Authorization Board (JAB).</span></span> <span data-ttu-id="a69bf-112">JAB는 FedRAMP의 기본 거버넌스 및 의사 결정 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-112">The JAB is the primary governance and decision-making body for FedRAMP.</span></span> <span data-ttu-id="a69bf-113">국방부, 국토안보부 및 일반 서비스 관리 담당자가 보드에서 일합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-113">Representatives from the Department of Defense, the Department of Homeland Security, and the General Services Administration serve on the board.</span></span> <span data-ttu-id="a69bf-114">이 보드는 FedRAMP 규정 준수를 입증한 CSP에 P-ATO를 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-114">The board grants a P-ATO to CSPs that have demonstrated FedRAMP compliance.</span></span>
- <span data-ttu-id="a69bf-115">연방 기관에서 ATO(운영 권한)를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-115">Receive an Authority to Operate (ATO) from a federal agency.</span></span>
- <span data-ttu-id="a69bf-116">또는 독립적으로 프로그램 요구 사항을 충족하는 CSP 제공 패키지를 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-116">Or, work independently to develop a CSP Supplied Package that meets program requirements.</span></span>

<span data-ttu-id="a69bf-117">이러한 각 경로를 사용하려면 FedRAMP PMO(프로그램 관리 Office)에서 엄격한 기술 검토를 수행하고 프로그램에 의해 인증된 독립적인 타사 조직의 평가가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-117">Each of these paths requires a stringent technical review by the FedRAMP Program Management Office (PMO) and an assessment by an independent third-party organization that is accredited by the program.</span></span>

<span data-ttu-id="a69bf-118">FedRAMP 권한 부여는 NIST 지침(낮음, 보통, 높음)에 따라 세 가지 영향 수준에서 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-118">FedRAMP authorizations are granted at three impact levels based on NIST guidelines—low, medium, and high.</span></span> <span data-ttu-id="a69bf-119">이러한 수준은 기밀성, 무결성 또는 가용성 손실이 조직에 미칠 수 있는 영향의 순위를 낮음(제한된 효과), 보통(심각한 부정적인 영향) 및 높음(심각한 또는 재난적 효과)으로 순위를 높입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-119">These levels rank the impact that the loss of confidentiality, integrity, or availability could have on an organization—low (limited effect), medium (serious adverse effect), and high (severe or catastrophic effect).</span></span>

## <a name="microsoft-and-fedramp"></a><span data-ttu-id="a69bf-120">Microsoft 및 FedRAMP</span><span class="sxs-lookup"><span data-stu-id="a69bf-120">Microsoft and FedRAMP</span></span>

<span data-ttu-id="a69bf-121">Azure Government, Dynamics 365 Government 및 Office 365 미국 정부를 비롯한 Microsoft의 정부 클라우드 서비스는 미국 연방 위험 및 권한 부여 관리 프로그램(FedRAMP)의 요구 사항을 충족하여 미국 연방 기관이 Microsoft 클라우드의 비용 절감 및 엄격한 보안을 활용하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-121">Microsoft's government cloud services, including Azure Government, Dynamics 365 Government, and Office 365 U.S. Government meet the demanding requirements of the US Federal Risk and Authorization Management Program (FedRAMP), enabling U.S. federal agencies to benefit from the cost savings and rigorous security of the Microsoft Cloud.</span></span>

<span data-ttu-id="a69bf-122">Microsoft 정부 클라우드 서비스는 공공 부문 고객에게 FedRAMP를 준수하는 다양한 서비스와 [FedRAMP High Blueprint를](https://aka.ms/fedrampblueprint)비롯한 강력한 지침 및 구현 도구를 제공합니다. 이 도구는 고객이 FedRAMP High 컨트롤을 구현해야 하는 Azure 배포 아키텍처에 대한 핵심 정책 집합을 배포하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-122">Microsoft government cloud services offer public sector customers a rich array of services compliant with FedRAMP, and robust guidance and implementation tools, including the [FedRAMP High blueprint](https://aka.ms/fedrampblueprint), which helps customers deploy a core set of policies for any Azure-deployed architecture that must implement FedRAMP High controls.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="a69bf-123">Microsoft 범위 내 클라우드 플랫폼 & 서비스</span><span class="sxs-lookup"><span data-stu-id="a69bf-123">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="a69bf-124">Azure 및 Azure Government</span><span class="sxs-lookup"><span data-stu-id="a69bf-124">Azure and Azure Government</span></span>
- [<span data-ttu-id="a69bf-125">Dynamics 365 미국 정부</span><span class="sxs-lookup"><span data-stu-id="a69bf-125">Dynamics 365 U.S. Government</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="a69bf-126">Intune</span><span class="sxs-lookup"><span data-stu-id="a69bf-126">Intune</span></span>
- <span data-ttu-id="a69bf-127">Office 365 미국, 미국, Office 365- High, Office 365 미국 정부방부</span><span class="sxs-lookup"><span data-stu-id="a69bf-127">Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="a69bf-128">독립형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="a69bf-128">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="azure-dynamics-365-and-fedramp"></a><span data-ttu-id="a69bf-129">Azure, Dynamics 365 및 FedRAMP</span><span class="sxs-lookup"><span data-stu-id="a69bf-129">Azure, Dynamics 365, and FedRAMP</span></span>

<span data-ttu-id="a69bf-130">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure FedRAMP 서비스를 참조하세요.](/azure/compliance/offerings/offering-fedramp)</span><span class="sxs-lookup"><span data-stu-id="a69bf-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure FedRAMP offering](/azure/compliance/offerings/offering-fedramp).</span></span>

## <a name="office-365-and-fedramp"></a><span data-ttu-id="a69bf-131">Office 365 및 FedRAMP</span><span class="sxs-lookup"><span data-stu-id="a69bf-131">Office 365 and FedRAMP</span></span>

- <span data-ttu-id="a69bf-132">Office 365 및 Office 365 미국 정부는 미국 DHHS(보건복지부)의 ATO가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-132">Office 365 and Office 365 U.S. Government have an ATO from the US Department of Health and Human Services (DHHS).</span></span>
- <span data-ttu-id="a69bf-133">Office 365 미국 국방부에는 DISA(미국방부 정보 시스템 기관)의 P-ATO가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-133">Office 365 U.S. Government Defense has a P-ATO from the US Defense Information Systems Agency (DISA).</span></span> <span data-ttu-id="a69bf-134">미국 Office 365 배포하고자 하는 모든 고객은 DISA P-ATO를 사용하여 기관 ATO를 생성하여 승인을 문서화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-134">Any customer wishing to deploy Office 365 U.S. Government Defense may use the DISA P‑ATO to generate an agency ATO to document their acceptance of it.</span></span>
- <span data-ttu-id="a69bf-135">Office 365(기업 및 비즈니스 요금제) 및 Office 365 DHHS 일반의 중간 영향 수준에 FedRAMP 기관 ATO가 Office 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-135">Office 365 (enterprise and business plans) and Office 365 U.S. Government have a FedRAMP Agency ATO at the Moderate Impact Level from the DHHS Office of the Inspector General.</span></span> <span data-ttu-id="a69bf-136">Office 365 미국 정부는 이 인증을 획득한 첫 번째 클라우드 기반 전자 메일 및 공동 작업 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-136">Office 365 U.S. Government was the first cloud-based email and collaboration service to obtain this authorization.</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="a69bf-137">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="a69bf-137">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="a69bf-138">Office 365 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="a69bf-138">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="a69bf-139">다음 표를 사용하여 서비스 및 구독에 Office 365 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-139">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="a69bf-140">**적용 가능 여부**</span><span class="sxs-lookup"><span data-stu-id="a69bf-140">**Applicability**</span></span> | <span data-ttu-id="a69bf-141">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="a69bf-141">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="a69bf-142">**GCC**</span><span class="sxs-lookup"><span data-stu-id="a69bf-142">**GCC**</span></span> | <span data-ttu-id="a69bf-143">작업 피드 서비스, Bing 서비스, Bing Delve, Exchange Online, Exchange Online Protection, 인프라, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="a69bf-143">Activity Feed Service, Bing Services, Delve, Exchange Online, Exchange Online Protection, Infrastructure, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="a69bf-144">**GCC 높음**</span><span class="sxs-lookup"><span data-stu-id="a69bf-144">**GCC High**</span></span> | <span data-ttu-id="a69bf-145">작업 피드 서비스, Bing 서비스, Exchange Online, Exchange Online Protection, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="a69bf-145">Activity Feed Service, Bing Services, Exchange Online, Exchange Online Protection, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="a69bf-146">**DoD**</span><span class="sxs-lookup"><span data-stu-id="a69bf-146">**DoD**</span></span> | <span data-ttu-id="a69bf-147">작업 피드 서비스, Bing 서비스, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="a69bf-147">Activity Feed Service, Bing Services, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="office-365-audits-reports-and-certificates"></a><span data-ttu-id="a69bf-148">Office 365, 보고서 및 인증서</span><span class="sxs-lookup"><span data-stu-id="a69bf-148">Office 365 audits, reports, and certificates</span></span>

<span data-ttu-id="a69bf-149">Microsoft는 P-ATOs 및 ATOs를 유지하기 위해 매년 클라우드 서비스를 재인증해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-149">Microsoft is required to recertify its cloud services each year to maintain its P-ATOs and ATOs.</span></span> <span data-ttu-id="a69bf-150">이를 위해 Microsoft는 보안 제어를 지속적으로 모니터링하고 평가하고, 서비스의 보안이 규정을 준수하는지 입증해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-150">To do so, Microsoft must monitor and assess its security controls continuously, and demonstrate that the security of its services remains in compliance.</span></span>

- [<span data-ttu-id="a69bf-151">Microsoft FedRAMP 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="a69bf-151">Microsoft FedRAMP Audit Reports</span></span>](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a><span data-ttu-id="a69bf-152">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="a69bf-152">Frequently asked questions</span></span>

<span data-ttu-id="a69bf-153">**Microsoft 클라우드 서비스가 FISMA(Federal Information Security Management Act)를 준수하나요?**</span><span class="sxs-lookup"><span data-stu-id="a69bf-153">**Do Microsoft cloud services comply with the Federal Information Security Management Act (FISMA)?**</span></span>

<span data-ttu-id="a69bf-154">FISMA는 미국 연방 기관 및 해당 파트너가 FISMA 요구 사항을 준수하는 조직에서만 정보 시스템 및 서비스를 조달해야 하는 연방 법률입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-154">FISMA is the federal law that requires US federal agencies and their partners to procure information systems and services only from organizations that adhere to FISMA requirements.</span></span> <span data-ttu-id="a69bf-155">FISMA 준수를 나타내는 대부분의 기관 및 공급업체는 특수 발행물 800-53 rev 4에서 NIST로 식별된 컨트롤을 충족하는 방법을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-155">Most agencies and their vendors that indicate that they are FISMA-compliant are referring to how they meet the controls identified by the NIST in Special Publication 800-53 rev 4.</span></span> <span data-ttu-id="a69bf-156">FISMA 프로세스(기본적으로 표준 자체는 아는 경우)는 2011년 FedRAMP로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-156">The FISMA process (but not the underlying standards themselves) was replaced by FedRAMP in 2011.</span></span>

<span data-ttu-id="a69bf-157">**FedRAMP는 누구에게 적용하나요?**</span><span class="sxs-lookup"><span data-stu-id="a69bf-157">**To whom does FedRAMP apply?**</span></span>

<span data-ttu-id="a69bf-158">'FedRAMP is mandatory for federal agency cloud deployments and service models at the low and moderate risk impact levels.'</span><span class="sxs-lookup"><span data-stu-id="a69bf-158">'FedRAMP is mandatory for federal agency cloud deployments and service models at the low and moderate risk impact levels.'</span></span> <span data-ttu-id="a69bf-159">CSP에 참여하려는 연방 기관은 FedRAMP 사양을 충족해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-159">Any federal agency that wants to engage a CSP may be required to meet FedRAMP specifications.</span></span> <span data-ttu-id="a69bf-160">또한 연방 정부에서 사용하는 제품 또는 서비스에서 클라우드 기술을 사용하는 회사에서 ATO를 획득해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-160">In addition, companies that employ cloud technologies in products or services used by the federal government may be required to obtain an ATO.</span></span>

<span data-ttu-id="a69bf-161">**기관에서 자체 규정 준수 노력은 어디에서 시작하나요?**</span><span class="sxs-lookup"><span data-stu-id="a69bf-161">**Where does my agency start its own compliance effort?**</span></span>

<span data-ttu-id="a69bf-162">FedRAMP를 성공적으로 탐색하고 해당 요구 사항을 충족하기 위해 연방 기관이 취해야 하는 단계에 대한 개요를 확인하려면 [Get Authorized: Agency Authorization 로 이동하세요.](https://www.fedramp.gov/agency-authorization/)</span><span class="sxs-lookup"><span data-stu-id="a69bf-162">For an overview of the steps federal agencies must take to successfully navigate FedRAMP and meet its requirements, go to [Get Authorized: Agency Authorization](https://www.fedramp.gov/agency-authorization/).</span></span>

<span data-ttu-id="a69bf-163">**기관의 인증 프로세스에서 Microsoft 규정 준수를 사용할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="a69bf-163">**Can I use Microsoft compliance in my agency's authorization process?**</span></span>

<span data-ttu-id="a69bf-164">예.</span><span class="sxs-lookup"><span data-stu-id="a69bf-164">Yes.</span></span> <span data-ttu-id="a69bf-165">연방 정부 기관의 ATO가 필요한 프로그램 또는 이니셔티브의 기초로 Microsoft 클라우드 서비스의 인증을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-165">You may use the certifications of Microsoft cloud services as the foundation for any program or initiative that requires an ATO from a federal government agency.</span></span> <span data-ttu-id="a69bf-166">그러나 이러한 서비스 외부의 구성 요소에 대한 자체 권한 부여를 달성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-166">However, you need to achieve your own authorizations for components outside these services.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="a69bf-167">Microsoft 준수 관리자를 사용하여 위험 평가</span><span class="sxs-lookup"><span data-stu-id="a69bf-167">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="a69bf-168">[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-168">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="a69bf-169">준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-169">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="a69bf-170">준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-170">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="a69bf-171">[준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="a69bf-171">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="a69bf-172">리소스</span><span class="sxs-lookup"><span data-stu-id="a69bf-172">Resources</span></span>

- [<span data-ttu-id="a69bf-173">Federal Risk and Authorization Management Program</span><span class="sxs-lookup"><span data-stu-id="a69bf-173">Federal Risk and Authorization Management Program</span></span>](https://www.fedramp.gov/)
- [<span data-ttu-id="a69bf-174">FedRAMP 보안 평가 프레임워크</span><span class="sxs-lookup"><span data-stu-id="a69bf-174">FedRAMP Security Assessment Framework</span></span>](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [<span data-ttu-id="a69bf-175">Microsoft의 클라우드에서 규정 준수 관리</span><span class="sxs-lookup"><span data-stu-id="a69bf-175">Managing compliance in the cloud at Microsoft</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="a69bf-176">Microsoft Government 클라우드</span><span class="sxs-lookup"><span data-stu-id="a69bf-176">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2087246)
