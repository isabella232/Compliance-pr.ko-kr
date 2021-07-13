---
title: SOC(시스템 및 조직 컨트롤) 3
description: Microsoft 클라우드 서비스가 운영 보안을 위해 SOC(시스템 및 조직 컨트롤) 3 표준을 준수하는 방법을 알아봅니다.
keywords: Microsoft 365, 규정 준수, 제품
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
ms.openlocfilehash: 1d6f6b0a4c9bd3ebbccb90331a8cf17df7ff8928
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385768"
---
# <a name="system-and-organization-controls-soc-3"></a><span data-ttu-id="5b9a9-104">SOC(시스템 및 조직 컨트롤) 3</span><span class="sxs-lookup"><span data-stu-id="5b9a9-104">System and Organization Controls (SOC) 3</span></span>

## <a name="soc-3-overview"></a><span data-ttu-id="5b9a9-105">SOC 3 개요</span><span class="sxs-lookup"><span data-stu-id="5b9a9-105">SOC 3 overview</span></span>

<span data-ttu-id="5b9a9-106">서비스 조직을 위한 SOC(시스템 및 조직 컨트롤)는 AICPA(American Institute of Certified Public Coordinators)가 만든 내부 제어 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-106">System and Organization Controls (SOC) for Service Organizations are internal control reports created by the American Institute of Certified Public Accountants (AICPA).</span></span> <span data-ttu-id="5b9a9-107">최종 사용자가 아웃소스한 서비스와 관련된 위험을 평가하고 해결할 수 있도록 서비스 조직에서 제공하는 서비스를 검사하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-107">They are intended to examine services provided by a service organization so that end users can assess and address the risk associated with an outsourced service.</span></span>

<span data-ttu-id="5b9a9-108">*서비스 조직을 위한 SOC 3 SOC: 일반 사용 보고서* 를 위한 Trust Services Criteria는 보안, 상태, 처리 무결성, 기밀성 또는 개인 정보와 관련된 서비스 조직 컨트롤에 대한 보증이 필요하지만 전체 SOC 2 보고서가 필요하지 않은 사용자를 위한 간단한 공개 버전의 SOC 2 유형 2 증명 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-108">*SOC 3 SOC for Service Organizations: Trust Services Criteria for General Use Report* is a short, publicly facing version of the SOC 2 Type 2 attestation report for users who need assurances about service organization's controls relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy but do not need a full SOC 2 report.</span></span> <span data-ttu-id="5b9a9-109">SOC 3 보고서는 일반적인 사용 보고서이므로 자유롭게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-109">Because SOC 3 reports are general use reports, they can be freely distributed.</span></span>

<span data-ttu-id="5b9a9-110">SOC 3 보고서는 적용 가능한 Trust Services Criteria에 따라 약정을 이행하기 위한 컨트롤 효율성과 관련된 서비스 조직 관리자의 서면 어설션과 관리의 어설션이 공평하게 명시되었는지에 대한 서비스 감사자의 의견을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-110">A SOC 3 report contains a written assertion by service organization management regarding control effectiveness to achieve commitments based on the applicable trust services criteria, as well as service auditor's opinion on whether management's assertion is stated fairly.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="5b9a9-111">Microsoft 범위 내 클라우드 플랫폼 및 서비스</span><span class="sxs-lookup"><span data-stu-id="5b9a9-111">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="5b9a9-112">Microsoft 범위 내 서비스는 Azure [SOC 2 유형 2 증명](offering-soc-2.md) 보고서에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-112">Microsoft in-scope services are shown in the Azure [SOC 2 Type 2 attestation](offering-soc-2.md) report.</span></span>

- <span data-ttu-id="5b9a9-113">Azure(자세한 정보는 [Microsoft Azure 규정 준수 제품](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) 또는 Azure SOC 2 Type 2 증명 보고서 참조)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-113">Azure (for detailed insight, see [Microsoft Azure Compliance Offerings](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) or Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="5b9a9-114">Dynamics 365(자세한 정보는 Azure SOC 2 Type 2 증명 보고서 참조)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-114">Dynamics 365 (for detailed insight, see Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="5b9a9-115">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5b9a9-115">Microsoft 365 Defender</span></span>
- <span data-ttu-id="5b9a9-116">MCAS(Microsoft Cloud App Security)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-116">Microsoft Cloud App Security (MCAS)</span></span>
- <span data-ttu-id="5b9a9-117">엔드포인트용 Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5b9a9-117">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="5b9a9-118">ID용 Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5b9a9-118">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="5b9a9-119">Microsoft Forms Pro(Azure Government의 경우 범위에 포함되지 않음)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-119">Microsoft Forms Pro (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5b9a9-120">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5b9a9-120">Microsoft Graph</span></span>
- <span data-ttu-id="5b9a9-121">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="5b9a9-121">Microsoft Intune</span></span>
- <span data-ttu-id="5b9a9-122">Microsoft Managed Desktop(Azure Government의 경우 범위에 포함되지 않음)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-122">Microsoft Managed Desktop (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5b9a9-123">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="5b9a9-123">Microsoft Stream</span></span>
- <span data-ttu-id="5b9a9-124">Microsoft 위협 전문가(Azure Government의 경우 범위에 포함되지 않음)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-124">Microsoft Threat Experts (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5b9a9-125">추천 포털</span><span class="sxs-lookup"><span data-stu-id="5b9a9-125">Nomination Portal</span></span>
- <span data-ttu-id="5b9a9-126">Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="5b9a9-126">Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="5b9a9-127">Power Apps</span><span class="sxs-lookup"><span data-stu-id="5b9a9-127">Power Apps</span></span>
- <span data-ttu-id="5b9a9-128">Power Automate</span><span class="sxs-lookup"><span data-stu-id="5b9a9-128">Power Automate</span></span>
- <span data-ttu-id="5b9a9-129">Power BI</span><span class="sxs-lookup"><span data-stu-id="5b9a9-129">Power BI</span></span>
- <span data-ttu-id="5b9a9-130">Power Virtual Agents(Azure Government의 경우 범위에 포함되지 않음)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-130">Power Virtual Agents (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5b9a9-131">업데이트 준수(Azure Government의 경우 범위에 포함되지 않음)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-131">Update Compliance (not in scope for Azure Government)</span></span>

## <a name="azure-dynamics-365-and-soc-3"></a><span data-ttu-id="5b9a9-132">Azure, Dynamics 365 및 SOC 3</span><span class="sxs-lookup"><span data-stu-id="5b9a9-132">Azure, Dynamics 365, and SOC 3</span></span>

<span data-ttu-id="5b9a9-133">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure SOC 3 제품](/azure/compliance/offerings/offering-soc-3)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-133">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure SOC 3 offering](/azure/compliance/offerings/offering-soc-3).</span></span>

## <a name="office-365-and-soc-3"></a><span data-ttu-id="5b9a9-134">Office 365 및 SOC 3</span><span class="sxs-lookup"><span data-stu-id="5b9a9-134">Office 365 and SOC 3</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="5b9a9-135">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="5b9a9-135">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="5b9a9-136">Office 365 적용 가능성 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="5b9a9-136">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="5b9a9-137">다음 표를 사용하여 Office 365 서비스 및 구독에 대한 적용 가능성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-137">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="5b9a9-138">**적용 가능성**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-138">**Applicability**</span></span> | <span data-ttu-id="5b9a9-139">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-139">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="5b9a9-140">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-140">**Office 365**</span></span> | <span data-ttu-id="5b9a9-141">준수 관리자, 고객 Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox(Torus), Microsoft Teams, MyAnalytics, Office 365 고객 포털, Office 365 마이크로 서비스(Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, 학교 데이터 동기화, Siphon, Speech, StaffHub, eXtensible Application Program 등), Office Online, Office Services Infrastructure, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, Project Online, 고객 키를 사용한 서비스 암호화, SharePoint Online, 비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="5b9a9-141">Compliance Manager, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office Online, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="5b9a9-142">**GCC**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-142">**GCC**</span></span> | <span data-ttu-id="5b9a9-143">Azure Active Directory, 준수 관리자, Delve, Exchange Online,</span><span class="sxs-lookup"><span data-stu-id="5b9a9-143">Azure Active Directory, Compliance Manager, Delve, Exchange Online,</span></span> 
<span data-ttu-id="5b9a9-144">, Office 365용 Microsoft Defender, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype, Stream</span><span class="sxs-lookup"><span data-stu-id="5b9a9-144">, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="5b9a9-145">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-145">**GCC High**</span></span> | <span data-ttu-id="5b9a9-146">Azure Active Directory, Exchange Online, Flow, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="5b9a9-146">Azure Active Directory, Exchange Online, Flow, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="5b9a9-147">**DoD**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-147">**DoD**</span></span> | <span data-ttu-id="5b9a9-148">Azure Active Directory, Exchange Online, Office 365용 Microsoft Defender, Microsoft Teams, Office 365 Advanced Compliance 추가 기능, Office 365 보안 및 준수 센터, Office Online, Office Pro Plus, 비즈니스용 OneDrive, Planner, Power Automate, Power BI, SharePoint Online, 비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="5b9a9-148">Azure Active Directory, Exchange Online, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audit-reports"></a><span data-ttu-id="5b9a9-149">Office 365 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="5b9a9-149">Office 365 audit reports</span></span>

- [<span data-ttu-id="5b9a9-150">Office 365 Core - SSAE 18 SOC 3 보고서</span><span class="sxs-lookup"><span data-stu-id="5b9a9-150">Office 365 Core - SSAE 18 SOC 3 Report</span></span>](https://aka.ms/o365SOC-3)
- [<span data-ttu-id="5b9a9-151">브리지 레터 및 추가 감사 보고서 참조</span><span class="sxs-lookup"><span data-stu-id="5b9a9-151">See bridge letters and additional audit reports</span></span>](https://aka.ms/auditreports)

<span data-ttu-id="5b9a9-152">필요한 경우 SOC 1 및 SOC 2 증명 보고서 및 브리지 레터를 다운로드하려면 Office 365 또는 Office 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-152">You must have an existing subscription or free trial account in Office 365 or Office 365 U.S. Government to download SOC 1 and SOC 2 attestation reports and any bridge letters as needed.</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="5b9a9-153">자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="5b9a9-153">Frequently asked questions</span></span>

<span data-ttu-id="5b9a9-154">**Office 365 SOC 보고서는 얼마나 자주 발행되나요?**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-154">**How often are Office 365 SOC reports issued?**</span></span>

<span data-ttu-id="5b9a9-155">Office 365 및 기타 온라인 서비스에 대한 SOC 보고서는 과거 12개월 연속 실행 기간(감사 기간)을 기반으로 하고 1년에 두 번 새 보고서가 발행됩니다.(3월 31일과 9월 30일 기간 종료)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-155">SOC reports for Office 365 and other online services are based on a rolling 12-month run window (audit period) with new reports issued semi-annually (period ends are March 31 and September 30).</span></span> <span data-ttu-id="5b9a9-156">*브리지 레터* 는 이전 3개월의 내용을 포함하여 분기별로 발행됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-156">*Bridge letters* are issued each quarter to cover the prior three-month period.</span></span> <span data-ttu-id="5b9a9-157">예를 들어 1월 레터는 10월 1일~12월 31일, 4월 레터는 1월 1일~3월 31일, 7월 레터는 4월 1일~6월 30일, 10월 레터는 7월 1일~9월 30일 내용을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-157">For example, the January letter covers 1-Oct through 31-Dec, the April letter covers 1-Jan through 31-Mar, the July letter covers 1-Apr through 30-Jun, and the October letter covers 1-Jul through 30-Sep.</span></span>

<span data-ttu-id="5b9a9-158">**브리지 레터를 포함한 Office 365 SOC 감사 문서는 어디에서 받을 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="5b9a9-158">**Where can I get the Office 365 SOC audit documentation including bridge letters?**</span></span> <span data-ttu-id="5b9a9-159">감사 문서 링크는 감사 보고서 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-159">For links to audit documentation, see the audit report section.</span></span> <span data-ttu-id="5b9a9-160">로그인하려면 Office 365 또는 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government의 기존 구독 또는 평가판 계정이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-160">You must have an existing subscription or free trial account in Office 365or [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government to login.</span></span> <span data-ttu-id="5b9a9-161">그런 다음 감사 인증서, 평가 보고서 및 기타 관련 문서를 다운로드하여 자체 규정 요구 사항에 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-161">You can then download audit certificates, assessment reports, and other applicable documents to help you with your own regulatory requirements.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="5b9a9-162">Microsoft 준수 관리자를 사용하여 위험 평가</span><span class="sxs-lookup"><span data-stu-id="5b9a9-162">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="5b9a9-163">[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-163">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="5b9a9-164">준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-164">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="5b9a9-165">준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-165">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="5b9a9-166">[준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a9-166">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="5b9a9-167">리소스</span><span class="sxs-lookup"><span data-stu-id="5b9a9-167">Resources</span></span>

- [<span data-ttu-id="5b9a9-168">Service Trust Portal 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="5b9a9-168">Service Trust Portal audit reports</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [<span data-ttu-id="5b9a9-169">서비스 조직을 위한 AICPA SOC</span><span class="sxs-lookup"><span data-stu-id="5b9a9-169">AICPA SOC for Service Organizations</span></span>](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [<span data-ttu-id="5b9a9-170">SSAE 번호 18, 증명 표준: 설명 및 수정(AICPA 전문가 표준)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-170">SSAE No. 18, Attestation Standards: Clarification and Recodification (AICPA Professional Standards)</span></span>](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- <span data-ttu-id="5b9a9-171">[보안, 가용성, 처리 무결성, 기밀성 또는 개인 정보 보호와 관련된 서비스 조직의 컨트롤 검사에 대한 SOC 2 보고(AICPA 가이드)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (구입 가능)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-171">[SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (available for purchase)</span></span>
- [<span data-ttu-id="5b9a9-172">TSP 섹션 100 (AICPA, 2017 Trust Services Criteria)</span><span class="sxs-lookup"><span data-stu-id="5b9a9-172">TSP section 100 (AICPA, 2017 Trust Services Criteria)</span></span>](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
