---
title: ISO/IEC 27017:2015 정보 보안 통제를 위한 규약
description: Microsoft 클라우드 서비스는 정보 보안 통제를 위해 이 규약을 구현했습니다.
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
ms.openlocfilehash: b51d7879b0b20773f76ed194a0080b2ae88c1fb8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509508"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a><span data-ttu-id="e384c-104">ISO/IEC 27017:2015 정보 보안 통제를 위한 규약</span><span class="sxs-lookup"><span data-stu-id="e384c-104">ISO/IEC 27017:2015 Code of Practice for Information Security Controls</span></span>

## <a name="iso-iec-27017-overview"></a><span data-ttu-id="e384c-105">ISO-IEC 27017 개요</span><span class="sxs-lookup"><span data-stu-id="e384c-105">ISO-IEC 27017 Overview</span></span>

<span data-ttu-id="e384c-p101">ISO/IEC 27017:2015 행동 강령은 조직이 ISO/IEC 27002:2013 기반 클라우드 컴퓨팅 정보 보안 관리 시스템을 구현할 때 클라우드 서비스 정보 보안 제어를 선택하기 위한 참조 자료로 사용할 수 있도록 설계되었습니다. 또한 클라우드 서비스 공급자는 일반적으로 허용되는 보호 제어를 구현하기 위한 지침 문서로도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p101">The ISO/IEC 27017:2015 code of practice is designed for organizations to use as a reference for selecting cloud services information security controls when implementing a cloud computing information security management system based on ISO/IEC 27002:2013. It can also be used by cloud service providers as a guidance document for implementing commonly accepted protection controls.</span></span>

<span data-ttu-id="e384c-p102">이 국제 표준은 ISO/IEC 27002에 기반한 클라우드별 구현 지침을 추가로 제공하며, 제어, 구현 지침 및 기타 정보에 대한 ISO/IEC 27002: 2013의 5-18 조항과 관련하여 클라우드별 정보 보안 위협 및 리스크를 해결하기 위한 추가적인 제어 기능을 제공합니다. 구체적으로, 이 표준은 ISO/IEC 27002에서 37개의 컨트롤에 대한 지침을 제공하며, ISO/IEC 27002에서 중복되지 않는 7개의 새로운 컨트롤을 특징으로 합니다. 이러한 새로운 컨트롤은 다음과 같은 중요한 영역을 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p102">This international standard provides additional cloud-specific implementation guidance based on ISO/IEC 27002, and provides additional controls to address cloud-specific information security threats and risks referring to clauses 5-18 in ISO/IEC 27002: 2013 for controls, implementation guidance, and other information. Specifically, this standard provides guidance on 37 controls in ISO/IEC 27002, and it also features seven new controls that are not duplicated in ISO/IEC 27002. These new controls address the following important areas:</span></span>

- <span data-ttu-id="e384c-111">클라우드 컴퓨팅 환경에서의 공유 역할과 책임</span><span class="sxs-lookup"><span data-stu-id="e384c-111">Shared roles and responsibilities within a cloud computing environment</span></span>
- <span data-ttu-id="e384c-112">계약 종료 시 클라우드 서비스 고객 자산의 제거와 반환</span><span class="sxs-lookup"><span data-stu-id="e384c-112">Removal and return of cloud service customer assets upon contract termination</span></span>
- <span data-ttu-id="e384c-113">한 고객의 가상 환경과 다른 고객의 가상 환경의 분리 및 보호</span><span class="sxs-lookup"><span data-stu-id="e384c-113">Protection and separation of a customer's virtual environment from environments of other customers</span></span>
- <span data-ttu-id="e384c-114">비즈니스 요구를 충족하기 위한 가상 컴퓨터 강화 요구 사항</span><span class="sxs-lookup"><span data-stu-id="e384c-114">Virtual machine hardening requirements to meet business needs</span></span>
- <span data-ttu-id="e384c-115">클라우드 컴퓨팅 환경의 관리 작업 절차</span><span class="sxs-lookup"><span data-stu-id="e384c-115">Procedures for administrative operations of a cloud computing environment</span></span>
- <span data-ttu-id="e384c-116">고객이 클라우드 컴퓨팅 환경 내의 관련 활동을 모니터링할 수 있도록 지원</span><span class="sxs-lookup"><span data-stu-id="e384c-116">Enabling customers to monitor relevant activities within a cloud computing environment</span></span>
- <span data-ttu-id="e384c-117">가상 네트워크와 물리적 네트워크의 보안 관리 일관성 유지</span><span class="sxs-lookup"><span data-stu-id="e384c-117">Alignment of security management for virtual and physical networks</span></span>

## <a name="microsoft-and-isoiec-27017"></a><span data-ttu-id="e384c-118">Microsoft와 ISO/IEC 27017</span><span class="sxs-lookup"><span data-stu-id="e384c-118">Microsoft and ISO/IEC 27017</span></span>

<span data-ttu-id="e384c-p103">ISO/IEC 27017은 클라우드 서비스 제공자와 클라우드 서비스 고객 모두에게 지침을 제공하는 데 있어 독보적입니다. 또한 클라우드 서비스 고객에게 클라우드 서비스 제공자에게 무엇을 기대해야 하는지에 대한 실질적인 정보도 제공합니다. 고객은 클라우드의 공유 책임을 확실히 이해함으로써 ISO/IEC 27017의 직접적인 혜택을 누릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p103">ISO/IEC 27017 is unique in providing guidance for both cloud service providers and cloud service customers. It also provides cloud service customers with practical information on what they should expect from cloud service providers. Customers can benefit directly from ISO/IEC 27017 by ensuring they understand the shared responsibilities in the cloud.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="e384c-122">Microsoft 범위 내 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="e384c-122">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="e384c-123">Azure, Azure Government, Azure Germany</span><span class="sxs-lookup"><span data-stu-id="e384c-123">Azure, Azure Government, and Azure Germany</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="e384c-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e384c-124">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="e384c-125">Dynamics 365, Dynamics 365 및 Dynamics 365 Germany</span><span class="sxs-lookup"><span data-stu-id="e384c-125">Dynamics 365, Dynamics 365, and Dynamics 365 Germany</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="e384c-126">Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e384c-126">Microsoft Defender Advanced Threat Protection</span></span>
- <span data-ttu-id="e384c-127">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e384c-127">Microsoft Graph</span></span>
- <span data-ttu-id="e384c-128">Microsoft Healthcare Bot</span><span class="sxs-lookup"><span data-stu-id="e384c-128">Microsoft Healthcare Bot</span></span>
- <span data-ttu-id="e384c-129">Intune</span><span class="sxs-lookup"><span data-stu-id="e384c-129">Intune</span></span>
- <span data-ttu-id="e384c-130">Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="e384c-130">Microsoft Managed Desktop</span></span>
- <span data-ttu-id="e384c-131">독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power Automate(이전 Microsoft Flow) 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="e384c-131">Power Automate (formerly Microsoft Flow) cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="e384c-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, 및 Office 365 Germany</span><span class="sxs-lookup"><span data-stu-id="e384c-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, and Office 365 Germany</span></span>
- <span data-ttu-id="e384c-133">독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 PowerApps 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="e384c-133">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="e384c-134">독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="e384c-134">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- <span data-ttu-id="e384c-135">Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="e384c-135">Power BI Embedded</span></span>
- <span data-ttu-id="e384c-136">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="e384c-136">Microsoft Stream</span></span>
- <span data-ttu-id="e384c-137">Office 365에서 적용되는 서비스에 대한 [자세한 목록](https://go.microsoft.com/fwlink/p/?linkid=2077751)보기</span><span class="sxs-lookup"><span data-stu-id="e384c-137">See a [detailed list](https://go.microsoft.com/fwlink/p/?linkid=2077751) of covered services in Office 365</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="e384c-138">감사, 보고서 및 인증서</span><span class="sxs-lookup"><span data-stu-id="e384c-138">Audits, reports, and certificates</span></span>

<span data-ttu-id="e384c-139">Microsoft 클라우드 서비스는 ISO/IEC 27001:2013에 대한 인증 프로세스의 일부로서 ISO/IEC 27017:2015 규약에 대해 1년에 한 번씩 감사를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-139">Microsoft cloud services are audited once a year for the ISO/IEC 27017:2015 code of practice as part of the certification process for ISO/IEC 27001:2013.</span></span>

- [<span data-ttu-id="e384c-140">Azure ISO 27017 인증서</span><span class="sxs-lookup"><span data-stu-id="e384c-140">Azure ISO 27017 Certificate</span></span>](https://aka.ms/azureiso27017cert)
- [<span data-ttu-id="e384c-141">Azure ISO 27017 평가 보고서</span><span class="sxs-lookup"><span data-stu-id="e384c-141">Azure ISO 27017 Assessment report</span></span>](https://aka.ms/azureiso27017report)
- [<span data-ttu-id="e384c-142">Office 365: ISO 27001, 27018 및 27017 감사 평가 보고서</span><span class="sxs-lookup"><span data-stu-id="e384c-142">Office 365: ISO 27001, 27018, and 27017 Audit Assessment Report</span></span>](https://aka.ms/o365isoreport)

## <a name="frequently-asked-questions"></a><span data-ttu-id="e384c-143">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="e384c-143">Frequently asked questions</span></span>

<span data-ttu-id="e384c-144">이 표준은 누구에게 적용됩니까?</span><span class="sxs-lookup"><span data-stu-id="e384c-144">To whom does the standard apply?</span></span>

<span data-ttu-id="e384c-p104">이 행동 강령은 클라우드 서비스 제공자와 클라우드 서비스 고객 모두에게 제어 및 구현 지침을 제공합니다. ISO/IEC 27002:2013과 유사한 형식으로 구성되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p104">This code of practice provides controls and implementation guidance for both cloud service providers and cloud service customers. It is structured in a format similar to ISO/IEC 27002:2013.</span></span>

<span data-ttu-id="e384c-147">**ISO/IEC 27017:2015에 대한 Microsoft의 규정 준수 정보는 어디에서 확인할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="e384c-147">**Where can I view Microsoft's compliance information for ISO/IEC 27017:2015?**</span></span>

<span data-ttu-id="e384c-148">Azure, Intune, Power BI에 대한 [ISO/IEC 27017:2015 인증서](https://aka.ms/azureiso27017)를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-148">You can download the [ISO/IEC 27017:2015 certificate](https://aka.ms/azureiso27017) for Azure, Intune, and Power BI.</span></span>

<span data-ttu-id="e384c-149">**우리 회사의 인증 프로세스에 Microsoft 서비스의 ISO/IEC 27017 규정 준수를 사용할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="e384c-149">**Can I use the ISO/IEC 27017 compliance of Microsoft services in my organization's certification process?**</span></span>

<span data-ttu-id="e384c-p105">예. 귀사가 범위 내 모든 Microsoft 엔터프라이즈 클라우드 서비스에 구현된 구현에 대한 인증을 받으려는 경우 규정 준수 평가에서 Microsoft의 관련 인증을 사용할 수 있습니다. 그러나 사용자는 평가인을 참여시켜 규정 준수를 위한 구현 평가와 조직 내 통제 및 프로세스에 대한 평가를 수행할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p105">Yes. If your business is seeking certification for implementations deployed on any Microsoft in-scope enterprise cloud services, you can use Microsoft's relevant certifications in your compliance assessment. However, you are responsible for engaging an assessor to evaluate your implementation for compliance, and for the controls and processes within your own organization.</span></span>

<span data-ttu-id="e384c-153">**적용되는 감사 보고서 사본을 구하려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="e384c-153">**How can I get copies of the applicable audit reports?**</span></span>

<span data-ttu-id="e384c-p106">[서비스 신뢰 포털](https://aka.ms/stphelp)은(는) 독립적인 타사 감사 보고서 및 기타 관련 설명서를 제공합니다. 포털을 사용하여 이 문서를 다운로드하고 검토하여 자체 규정 요구 사항에 대한 지원을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p106">The [Service Trust Portal](https://aka.ms/stphelp) provides independent, third-party audit reports and other related documentation. You can use the portal to download and review this documentation for assistance with your own regulatory requirements.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="e384c-156">Microsoft 준수 관리자를 사용하여 위험 평가</span><span class="sxs-lookup"><span data-stu-id="e384c-156">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="e384c-p107">[Microsoft 준수 관리자](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)는 사용자 조직의 준수 상태를 이해하고 위험을 줄이기 위한 활동에 도움을 주는 [Microsoft 365 규정 준수 센터](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규정에 관한 평가를 작성하기 위한 프리미엄 문서 서식을 제공합니다. 준수 관리자의 **평가 문서 서식 페이지** 에서 문서 서식을 찾을 수 있습니다. [준수 관리자에서 평가를 빌드](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments)하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="e384c-p107">[Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks. Compliance Manager offers a premium template for building an assessment for this regulation. Find the template in the **assessment templates** page in Compliance Manager. Learn how to [build assessments in Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="e384c-161">리소스</span><span class="sxs-lookup"><span data-stu-id="e384c-161">Resources</span></span>

- [<span data-ttu-id="e384c-162">ISO/IEC 27017:2015 규약</span><span class="sxs-lookup"><span data-stu-id="e384c-162">ISO/IEC 27017:2015 code of practice</span></span>](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [<span data-ttu-id="e384c-163">Microsoft 온라인 서비스 사용 약관</span><span class="sxs-lookup"><span data-stu-id="e384c-163">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="e384c-164">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="e384c-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
