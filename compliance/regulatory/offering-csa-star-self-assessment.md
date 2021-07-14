---
title: 규정 준수 제공 - CSA (Cloud Security Alliance) STAR 자체 평가
description: Microsoft STAR 자체 평가에서는 클라우드 서비스에서 Cloud Security Alliance 요구 사항을 충족하는 방법에 대해 자세히 설명합니다.
keywords: Microsoft 365, 규정 준수, 제안
localization_priority: Priority
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
ms.openlocfilehash: c2736c5ddb9c29a65d37f95c271bfb56e97fee88
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384218"
---
# <a name="cloud-security-alliance-csa-star-self-assessment"></a><span data-ttu-id="c4e07-104">CSA (Cloud Security Alliance) STAR 자체 평가</span><span class="sxs-lookup"><span data-stu-id="c4e07-104">Cloud Security Alliance (CSA) STAR self-assessment</span></span>

## <a name="csa-star-self-assessment-overview"></a><span data-ttu-id="c4e07-105">CSA STAR 자체 평가 개요</span><span class="sxs-lookup"><span data-stu-id="c4e07-105">CSA STAR self-assessment overview</span></span>

<span data-ttu-id="c4e07-106">CSA(Cloud Security Alliance)는 전문직 종사자, 회사 및 기타 주요 이해 관계자 연합이 주도하는 비영리 단체입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-106">The Cloud Security Alliance (CSA) is a nonprofit organization led by a broad coalition of industry practitioners, corporations, and other important stakeholders.</span></span> <span data-ttu-id="c4e07-107">이 단체는 보다 안전한 클라우드 컴퓨팅 환경을 유지하고 잠재적 클라우드 고객이 IT 운영을 클라우드로 전환할 때 현명한 결정을 내릴 수 있도록 도와줄 모범 사례를 정의하는 데 전념하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-107">It is dedicated to defining best practices to help ensure a more secure cloud computing environment, and to helping potential cloud customers make informed decisions when transitioning their IT operations to the cloud.</span></span>  
  
<span data-ttu-id="c4e07-108">CSA는 2010년에 클라우드 IT 운영(CSA 관리 방식, 위험 관리 및 규정 준수(GRC) 스택)을 평가할 도구를 발표했습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-108">In 2010, the CSA published a suite of tools to assess cloud IT operations: the CSA Governance, Risk Management, and Compliance (GRC) Stack.</span></span> <span data-ttu-id="c4e07-109">클라우드 고객이 CSP(클라우드 서비스 공급자)가 업계 모범 사례 및 표준을 준수하고 규정을 준수하는 방식을 평가하는 데 도움을 주도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-109">It was designed to help cloud customers assess how cloud service providers (CSPs) follow industry best practices and standards and comply with regulations.</span></span>  
  
<span data-ttu-id="c4e07-110">2013년 CSA와 British Standards Institution(영국 표준 협회)는 CPS가 CSA 관련 평가를 게시할 수 있도록 STAR(Security, Trust & Assurance Registry: 보안, 트러스트 및 보증 등록)라고 하는 무료 및 공개적으로 액세스할 수 있는 등록 프로그램을 시작했습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-110">In 2013, the CSA and the British Standards Institution launched the Security, Trust & Assurance Registry (STAR), a free, publicly accessible registry in which CSPs can publish their CSA-related assessments.</span></span>  
  
<span data-ttu-id="c4e07-111">CSA STAR는 CSA GRC 스택의 두 가지 주요 구성 요소를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-111">CSA STAR is based on two key components of the CSA GRC Stack:</span></span>

- <span data-ttu-id="c4e07-112">CCM(Cloud Controls Matrix): 클라우드 고객이 CSP의 전반적인 보안 위험을 평가하는 데 도움이 되도록 16개 도메인의 기본 보안 원칙을 다루는 제어 프레임워크</span><span class="sxs-lookup"><span data-stu-id="c4e07-112">Cloud Controls Matrix (CCM): a controls framework covering fundamental security principles across 16 domains to help cloud customers assess the overall security risk of a CSP.</span></span>
- <span data-ttu-id="c4e07-113">CAIQ(Consensus Assessments Initiative Questionnaire): 고객 또는 클라우드 감사자가 CSA 모범 사례를 준수하는지 평가하기 위해 CSP에 질문할 수 있는 CCM을 기반으로 하는 140개 이상의 질문 집합.</span><span class="sxs-lookup"><span data-stu-id="c4e07-113">The Consensus Assessments Initiative Questionnaire (CAIQ): a set of more than 140 questions based on the CCM that a customer or cloud auditor may want to ask of CSPs to assess their compliance with CSA best practices.</span></span>

<span data-ttu-id="c4e07-114">STAR는 세 가지 수준의 보장을 제공합니다. CSA-STAR 자체 평가는 수준 1의 도입 제안으로, 무료이며 모든 CSP에게 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-114">STAR provides three levels of assurance; CSA-STAR Self-Assessment is the introductory offering at Level 1, which is free and open to all CSPs.</span></span> <span data-ttu-id="c4e07-115">보장 스택을 더 올라가 STAR 프로그램의 수준 2는 제3의 독립 기관 평가 기반 인증을 포함하고, 수준 3은 지속적인 모니터링을 기반으로 하는 인증을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-115">Going further up the assurance stack, Level 2 of the STAR program involves third-party assessment-based certifications, and Level 3 involves certifications based on continuous monitoring.</span></span>

## <a name="microsoft-and-csa-star-self-assessment"></a><span data-ttu-id="c4e07-116">Microsoft와 CSA STAR 자체 평가</span><span class="sxs-lookup"><span data-stu-id="c4e07-116">Microsoft and CSA STAR self-assessment</span></span>

<span data-ttu-id="c4e07-117">STAR 자체 평가의 일환으로 CSP는 CSA 모범 사례 준수를 보여주는 두 가지 유형의 문서(완료된 CAIQ 또는 CCM 준수를 문서화한 보고서)를 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-117">As part of the STAR Self-Assessment, CSPs can submit two different types of documents to indicate their compliance with CSA best practices: a completed CAIQ, or a report documenting compliance with CCM.</span></span> <span data-ttu-id="c4e07-118">CSA STAR 자체 평가를 위해 Microsoft는 Microsoft Azure에 대한 CAIQ 및 CCM 기반 보고서와 Microsoft Dynamics 365와 Microsoft Office 365에 대한 CCM 기반 보고서를 모두 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-118">For the CSA STAR Self-Assessment, Microsoft publishes both a CAIQ and a CCM-based report for Microsoft Azure, and CCM-based reports for Microsoft Dynamics 365 and Microsoft Office 365.</span></span>  

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="c4e07-119">Microsoft 범위 내 클라우드 플랫폼 및 서비스</span><span class="sxs-lookup"><span data-stu-id="c4e07-119">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="c4e07-120">Azure 및 Azure Government</span><span class="sxs-lookup"><span data-stu-id="c4e07-120">Azure and Azure Government</span></span>
- [<span data-ttu-id="c4e07-121">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c4e07-121">Dynamics 365</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="c4e07-122">Office 365</span><span class="sxs-lookup"><span data-stu-id="c4e07-122">Office 365</span></span>

## <a name="azure-dynamics-365-and-csa-star-self-assessment"></a><span data-ttu-id="c4e07-123">Azure, Dynamics 365 및 CSA STAR 자체 평가</span><span class="sxs-lookup"><span data-stu-id="c4e07-123">Azure, Dynamics 365, and CSA STAR self-assessment</span></span>

<span data-ttu-id="c4e07-124">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure CSA STAR 자체 평가 제품](/azure/compliance/offerings/offering-csa-star-self-assessment)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4e07-124">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure CSA STAR self-assessment offering](/azure/compliance/offerings/offering-csa-star-self-assessment).</span></span>

## <a name="office-365-and-csa-star-self-assessment"></a><span data-ttu-id="c4e07-125">Office 365 및 CSA STAR 자체 평가</span><span class="sxs-lookup"><span data-stu-id="c4e07-125">Office 365 and CSA STAR self-assessment</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="c4e07-126">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="c4e07-126">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="c4e07-127">Office 365 적용 가능성 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="c4e07-127">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="c4e07-128">다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="c4e07-128">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="c4e07-129">**적용 가능성**</span><span class="sxs-lookup"><span data-stu-id="c4e07-129">**Applicability**</span></span> | <span data-ttu-id="c4e07-130">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="c4e07-130">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="c4e07-131">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="c4e07-131">**Office 365**</span></span> |<span data-ttu-id="c4e07-132">Exchange Online, Exchange Online Protection, Office 365 고객 포털, Office Online, Office 서비스 인프라, 비즈니스용 OneDrive, SharePoint Online, 비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="c4e07-132">Exchange Online, Exchange Online Protection, Office 365 Customer Portal, Office Online, Office Services Infrastructure, OneDrive for Business,SharePoint Online, Skype for Business</span></span> |

### <a name="frequently-asked-questions"></a><span data-ttu-id="c4e07-133">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="c4e07-133">Frequently asked questions</span></span>

<span data-ttu-id="c4e07-134">**CSA CCM이 어떤 산업 표준과 일치하나요?**</span><span class="sxs-lookup"><span data-stu-id="c4e07-134">**Which industry standards does the CSA CCM align with?**</span></span>

<span data-ttu-id="c4e07-135">CCM는 ISO 27001, PCI DSS, HIPAA, AICPA SOC 2, CIP, FedRAMP, NIST 등과 같은 업계에서 인정받는 보안 표준, 규정 및 제어 프레임워크에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-135">The CCM corresponds to industry-accepted security standards, regulations, and control frameworks such as ISO 27001, PCI DSS, HIPAA, AICPA SOC 2, NERC CIP, FedRAMP, NIST, and many more.</span></span> <span data-ttu-id="c4e07-136">최신 목록은 [CSA 웹 사이트](https://cloudsecurityalliance.org/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4e07-136">For the most current list, visit the [CSA website](https://cloudsecurityalliance.org/).</span></span>

<span data-ttu-id="c4e07-137">**CSA 별 자체 평가가 중요한 이유는 무엇인가요?**</span><span class="sxs-lookup"><span data-stu-id="c4e07-137">**Why is the CSA STAR Self-Assessment important?**</span></span>

<span data-ttu-id="c4e07-138">이를 통해 CSP는 CSA에서 게시한 모범 사례 준수 사항을 투명한 방식으로 문서화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-138">It enables CSPs to document compliance with CSA published best practices in a transparent manner.</span></span> <span data-ttu-id="c4e07-139">자체 평가 보고서는 일반에게 공개되고 따라서 클라우드 고객은 CSP 보안 관례를 보고 동일한 기준을 사용하여 다양한 CSP를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-139">Self-assessment reports are publicly available, thereby helping cloud customers gain visibility into the security practices of CSPs, and compare various CSPs using the same baseline.</span></span>

<span data-ttu-id="c4e07-140">**Office 365는 어떤 CSA STAR 보증 수준을 획득했나요?**</span><span class="sxs-lookup"><span data-stu-id="c4e07-140">**Which CSA STAR levels of assurance has Office 365 attained?**</span></span>

- <span data-ttu-id="c4e07-141">**수준 1**: **CSA STAR 자체 평가**: 클라우드 서비스 공급자가 고객이 서비스 보안을 평가하는 것을 돕기 위해 보안 컨트롤을 문서화하는 무료 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e07-141">**Level 1**: **CSA STAR Self-Assessment**: a complimentary offering from cloud service providers to document their security controls to help customers assess the security of the service.</span></span>

### <a name="office-365-resources"></a><span data-ttu-id="c4e07-142">Office 365 리소스</span><span class="sxs-lookup"><span data-stu-id="c4e07-142">Office 365 Resources</span></span>

- [<span data-ttu-id="c4e07-143">Cloud Security Alliance</span><span class="sxs-lookup"><span data-stu-id="c4e07-143">Cloud Security Alliance</span></span>](https://cloudsecurityalliance.org/)
- [<span data-ttu-id="c4e07-144">Cloud Controls Matrix (CCM)</span><span class="sxs-lookup"><span data-stu-id="c4e07-144">Cloud Controls Matrix (CCM)</span></span>](https://cloudsecurityalliance.org/group/cloud-controls-matrix/)
- [<span data-ttu-id="c4e07-145">Consensus Assessments Initiative Questionnaire (CAIQ)</span><span class="sxs-lookup"><span data-stu-id="c4e07-145">Consensus Assessments Initiative Questionnaire (CAIQ)</span></span>](https://cloudsecurityalliance.org/group/consensus-assessments/)
- [<span data-ttu-id="c4e07-146">CSA STAR(Security, Trust & Assurance Registry: 보안, 트러스트 및 보증 등록)</span><span class="sxs-lookup"><span data-stu-id="c4e07-146">CSA Security, Trust & Assurance Registry (STAR)</span></span>](https://cloudsecurityalliance.org/star/)
- [<span data-ttu-id="c4e07-147">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="c4e07-147">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)