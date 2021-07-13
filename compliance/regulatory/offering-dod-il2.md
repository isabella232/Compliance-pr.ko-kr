---
title: DoD(국방부) 영향 수준 2(IL2)
description: Microsoft가 IL2(국방부) 영향 수준 2(IL2) 표준을 충족하는 방법을 알아보습니다.
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
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385754"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a><span data-ttu-id="68e64-104">DoD(국방부) 영향 수준 2(IL2)</span><span class="sxs-lookup"><span data-stu-id="68e64-104">Department of Defense (DoD) Impact Level 2 (IL2)</span></span>

## <a name="dod-il2-overview"></a><span data-ttu-id="68e64-105">DoD IL2 개요</span><span class="sxs-lookup"><span data-stu-id="68e64-105">DoD IL2 overview</span></span>

<span data-ttu-id="68e64-106">DISA(Defense Information Systems Agency)는 DoD 클라우드 컴퓨팅 보안 요구 사항 [가이드(SRG)의](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)개발 및 유지 관리 업무를 담당하는 미국 DoD(국방부)의 기관입니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="68e64-107">SRG는 DoD가 클라우드 서비스 공급자(CSP)의 보안 상태를 평가하는 데 사용하는 기준 보안 요구 사항을 정의하여 CSP가 DoD 임무를 호스팅할 수 있는 PA(DoD Provisional Authorization)를 부여하는 결정을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="68e64-108">이전에 게시된 DoD 클라우드 보안 모델(CSM)을 통합, 위임 및 다시 사용하며 DoD RMF(위험 관리 프레임워크)에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="68e64-109">DISA는 CSP 사용을 계획하고 승인하는 DoD 기관 및 부서를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="68e64-110">또한 CSP 제품에서 DoD 표준 준수에 대한 문서를 제공하는 인증 프로세스인 SRG를 준수하는지 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="68e64-111">적절한 경우 DoD PAS(Provisional Authorizations)를 적용하기 때문에 DoD 기관 및 지원 조직은 전체 승인 프로세스를 거치지 않고도 클라우드 서비스를 사용하여 시간 및 노력을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="68e64-112">상용 클라우드 컴퓨팅 서비스 획득 및 사용에 대한  업데이트된 지침에 관한 [2014년 12월 15일 DoD CIO memo는](https://www.esi.mil/contentview.aspx?id=585) 'FedRAMP가 모든 DoD 클라우드 서비스에 대한 최소 보안 기준 역할을 할 것'으로 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-112">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="68e64-113">SRG는 모든 IL(정보 영향 수준)에서 FedRAMP 보통 기준을 사용하며 일부에서는 높은 기준을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-113">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="68e64-114">[SRG 섹션 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* 보안 제어의 DoD 사용 IL2 정보는 섹션 5.6.2에 설명된 직원 보안 요구 사항을 준수하는 경우 최소한 FedRAMP 보통 PA 및 DoD 수준 2 PA를 보유하는 CSP에서 호스팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimally holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2.</span></span> <span data-ttu-id="68e64-115">그러나 이 방법을 통해 CSP가 임무 소유자가 요구하는 다른 보안 및 통합 요구 사항을 충족하지는 못합니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-115">However, this approach does not alleviate the CSP from meeting other security and integration requirements as required by the Mission Owner.</span></span> <span data-ttu-id="68e64-116">[SRG 섹션 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2* 위치 및 분리 요구 사항에 따라 DoD IL2 PA에는 IL2 PA에 대한 요구 사항이 추가로 평가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-116">According to [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements*, DoD IL2 PA is adequately covered by a FedRAMP Moderate PA such that the requirements will not be additionally assessed for an IL2 PA.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="68e64-117">Microsoft 범위 내 클라우드 플랫폼 & 서비스</span><span class="sxs-lookup"><span data-stu-id="68e64-117">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="68e64-118">Azure</span><span class="sxs-lookup"><span data-stu-id="68e64-118">Azure</span></span>
- <span data-ttu-id="68e64-119">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="68e64-119">Dynamics 365</span></span>
- <span data-ttu-id="68e64-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="68e64-120">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="68e64-121">엔드포인트용 Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="68e64-121">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="68e64-122">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="68e64-122">Microsoft Graph</span></span>
- <span data-ttu-id="68e64-123">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="68e64-123">Microsoft Intune</span></span>
- <span data-ttu-id="68e64-124">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="68e64-124">Microsoft Stream</span></span>
- <span data-ttu-id="68e64-125">Office 365 미국 정부, Office 365 미국 정부 - 높음</span><span class="sxs-lookup"><span data-stu-id="68e64-125">Office 365 U.S. Government, Office 365 U.S. Government - High</span></span>
- <span data-ttu-id="68e64-126">Power Apps</span><span class="sxs-lookup"><span data-stu-id="68e64-126">Power Apps</span></span>
- <span data-ttu-id="68e64-127">Power Automate</span><span class="sxs-lookup"><span data-stu-id="68e64-127">Power Automate</span></span>
- <span data-ttu-id="68e64-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="68e64-128">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il2"></a><span data-ttu-id="68e64-129">Azure, Dynamics 365 및 DoD IL2</span><span class="sxs-lookup"><span data-stu-id="68e64-129">Azure, Dynamics 365, and DoD IL2</span></span>

<span data-ttu-id="68e64-130">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure DoD IL2 서비스를 참조하세요.](/azure/compliance/offerings/offering-dod-il2)</span><span class="sxs-lookup"><span data-stu-id="68e64-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL2 offering](/azure/compliance/offerings/offering-dod-il2).</span></span>

## <a name="office-365-and-dod-il2"></a><span data-ttu-id="68e64-131">Office 365 및 DoD IL2</span><span class="sxs-lookup"><span data-stu-id="68e64-131">Office 365 and DoD IL2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="68e64-132">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="68e64-132">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="68e64-133">Office 365 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="68e64-133">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="68e64-134">다음 표를 사용하여 서비스 및 구독에 Office 365 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68e64-134">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="68e64-135">**적용 가능 여부**</span><span class="sxs-lookup"><span data-stu-id="68e64-135">**Applicability**</span></span> | <span data-ttu-id="68e64-136">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="68e64-136">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="68e64-137">**GCC**</span><span class="sxs-lookup"><span data-stu-id="68e64-137">**GCC**</span></span> | <span data-ttu-id="68e64-138">작업 피드 서비스, Bing 서비스, Delve, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="68e64-138">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="68e64-139">**GCC 높음**</span><span class="sxs-lookup"><span data-stu-id="68e64-139">**GCC High**</span></span> | <span data-ttu-id="68e64-140">작업 피드 서비스, Bing 서비스, Delve, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="68e64-140">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="resources"></a><span data-ttu-id="68e64-141">리소스</span><span class="sxs-lookup"><span data-stu-id="68e64-141">Resources</span></span>

- [<span data-ttu-id="68e64-142">Microsoft 정부 솔루션</span><span class="sxs-lookup"><span data-stu-id="68e64-142">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="68e64-143">DoD 클라우드 컴퓨팅 보안 요구 사항 가이드</span><span class="sxs-lookup"><span data-stu-id="68e64-143">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="68e64-144">FedRAMP 문서</span><span class="sxs-lookup"><span data-stu-id="68e64-144">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="68e64-145">정보 시스템 및 조직을 위한 [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) 위험 관리 *프레임워크:* 보안 및 Life-Cycle 대한 시스템 관리 접근 방식</span><span class="sxs-lookup"><span data-stu-id="68e64-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="68e64-146">정보 시스템 및 조직에 대한 [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) 보안 및 개인 정보 *보호 컨트롤*</span><span class="sxs-lookup"><span data-stu-id="68e64-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="68e64-147">DoD IT(DoD Information Technology)에 대한 DoD 명령 [8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework(RMF)*</span><span class="sxs-lookup"><span data-stu-id="68e64-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
