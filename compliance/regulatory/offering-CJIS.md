---
title: CJIS(범죄 범죄 정보 서비스) 보안 정책
description: Microsoft 정부 클라우드 서비스는 미국 범죄 범죄 정보 서비스 보안 정책을 준수합니다.
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
ms.openlocfilehash: 0a8cc37a24d3a51d79fb1ac34c92d96fc7e76fdd
ms.sourcegitcommit: 66a26facea6ec9a95e5e61f1b5b69402f03db481
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/17/2021
ms.locfileid: "50279845"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a><span data-ttu-id="fed4e-104">CJIS(범죄 범죄 정보 서비스) 보안 정책</span><span class="sxs-lookup"><span data-stu-id="fed4e-104">Criminal Justice Information Services (CJIS) Security Policy</span></span>

## <a name="cjis-overview"></a><span data-ttu-id="fed4e-105">CJIS 개요</span><span class="sxs-lookup"><span data-stu-id="fed4e-105">CJIS overview</span></span>

<span data-ttu-id="fed4e-106">미국 FBI(연방 조사국)의 CJIS(범죄 정보 서비스) 부서는 주, 지역 및 연방 사법 기관 및 범죄 사법 기관이 지문 기록 및 범죄 기록과 같은 CJI(범죄 범죄 정보)에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-106">The Criminal Justice Information Services (CJIS) Division of the US Federal Bureau of Investigation (FBI) gives state, local, and federal law enforcement and criminal justice agencies access to criminal justice information (CJI) — for example, fingerprint records and criminal histories.</span></span> <span data-ttu-id="fed4e-107">미국의 사법 기관 및 기타 정부 기관은 CJI 전송, 저장 또는 처리에 클라우드 서비스를 사용하는 것이 CJI 보호를 위한 최소 보안 요구 사항 및 제어를 수립하는 [CJIS](https://aka.ms/cjis-security-policy)보안 정책을 준수하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-107">Law enforcement and other government agencies in the United States must ensure that their use of cloud services for the transmission, storage, or processing of CJI complies with the [CJIS Security Policy](https://aka.ms/cjis-security-policy), which establishes minimum security requirements and controls to safeguard CJI.</span></span>

<span data-ttu-id="fed4e-108">CJIS 보안 정책은 NIST(National Institute of Standards and Technology)의 지침과 함께, 대선 및 FBI 지시문, 연방법, 형사 사법 커뮤니티의 자문 정책 위원회 결정을 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-108">The CJIS Security Policy integrates presidential and FBI directives, federal laws, and the criminal justice community's Advisory Policy Board decisions, along with guidance from the National Institute of Standards and Technology (NIST).</span></span> <span data-ttu-id="fed4e-109">발전하는 보안 요구 사항을 반영하기 위해 정책이 주기적으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-109">The Policy is periodically updated to reflect evolving security requirements.</span></span>

<span data-ttu-id="fed4e-110">CJIS 보안 정책은 클라우드 서비스 공급자와 같은 개인 계약자가 클라우드 서비스의 사용이 CJIS 요구 사항과 일치할 수 있는지 여부를 결정하기 위해 평가해야 하는 13개 영역을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-110">The CJIS Security Policy defines 13 areas that private contractors such as cloud service providers must evaluate to determine if their use of cloud services can be consistent with CJIS requirements.</span></span> <span data-ttu-id="fed4e-111">이러한 영역은 NIST 800-53에 해당하며, 이는 Microsoft가 정부 클라우드 제품 인증을 받은 프로그램인 [FedRAMP(Federal Risk and Authorization Management](offering-FedRAMP.md)Program)의 기반이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-111">These areas correspond closely to NIST 800-53, which is also the basis for the [Federal Risk and Authorization Management Program (FedRAMP)](offering-FedRAMP.md), a program under which Microsoft has been certified for its Government Cloud offerings.</span></span>

<span data-ttu-id="fed4e-112">또한 CJI를 처리한 모든 비공개 계약자는 보안 정책에 필요한 CJI의 보안 및 기밀성을 보장하는 미국 법무 장관이 승인한 일직선 계약인 CJIS 보안 부록에 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-112">In addition, all private contractors who process CJI must sign the CJIS Security Addendum, a uniform agreement approved by the US Attorney General that helps ensure the security and confidentiality of CJI required by the Security Policy.</span></span> <span data-ttu-id="fed4e-113">또한 계약업체는 연방 및 주 법률, 규정 및 표준에 따라 보안 프로그램을 유지 관리하고, CJI의 사용을 정부 기관이 제공한 목적으로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-113">It also commits the contractor to maintaining a security program consistent with federal and state laws, regulations, and standards, and limits the use of CJI to the purposes for which a government agency provided it.</span></span>

## <a name="microsoft-and-cjis-security-policy"></a><span data-ttu-id="fed4e-114">Microsoft 및 CJIS 보안 정책</span><span class="sxs-lookup"><span data-stu-id="fed4e-114">Microsoft and CJIS Security Policy</span></span>

<span data-ttu-id="fed4e-115">Microsoft는 CJIS 정보 계약을 통해 CJIS 보안 부록에 주에 서명합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-115">Microsoft signs the CJIS Security Addendum in states with CJIS Information Agreements.</span></span> <span data-ttu-id="fed4e-116">이는 CJIS 보안 정책을 준수하는 주 법 집행 기관에 Microsoft의 클라우드 보안 제어가 데이터의 전체 수명 주기를 보호하고 CJI에 액세스할 수 있는 운영 담당자의 적절한 배경 심사를 보장하는 방법을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-116">These tell state law enforcement authorities responsible for compliance with CJIS Security Policy how Microsoft's cloud security controls help protect the full lifecycle of data and ensure appropriate background screening of operating personnel with access to CJI.</span></span> <span data-ttu-id="fed4e-117">Microsoft는 계속해서 주 정부와 함께 CJIS 정보 계약을 체결합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-117">Microsoft continues to work with state governments to enter into CJIS Information Agreements.</span></span>

<span data-ttu-id="fed4e-118">Microsoft는 Microsoft Azure Government, Microsoft Office 365 미국 정부 및 Microsoft Dynamics 365 미국 정부의 운영 정책 및 절차를 평가하고 범위 내 서비스 사용에 대한 FBI 요구 사항을 충족하기 위해 해당 서비스 계약의 기능을 테스트할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-118">Microsoft has assessed the operational policies and procedures of Microsoft Azure Government, Microsoft Office 365 U.S. Government, and Microsoft Dynamics 365 U.S. Government, and will attest to their ability in the applicable services agreements to meet FBI requirements for the use of in-scope services.</span></span>

<span data-ttu-id="fed4e-119">Microsoft 클라우드에서 CJIS 보안 정책의 이점에 대해 자세히 알아보고 Genetec이 범죄 조사를 어떻게 [지웠는가를 읽어요.](https://customers.microsoft.com/story/genetec)</span><span class="sxs-lookup"><span data-stu-id="fed4e-119">Learn about the benefits of CJIS Security policy on the Microsoft Cloud: [Read how Genetec cleared criminal investigations](https://customers.microsoft.com/story/genetec)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="fed4e-120">Microsoft 범위 내 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="fed4e-120">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="fed4e-121">Azure Government</span><span class="sxs-lookup"><span data-stu-id="fed4e-121">Azure Government</span></span>](/azure/azure-government/documentation-government-welcome)
- [<span data-ttu-id="fed4e-122">Dynamics 365 미국 정부</span><span class="sxs-lookup"><span data-stu-id="fed4e-122">Dynamics 365 U.S. Government</span></span>](/power-platform/admin/microsoft-dynamics-365-government#certifications-and-accreditations)
- [<span data-ttu-id="fed4e-123">Office 365 미국 정부</span><span class="sxs-lookup"><span data-stu-id="fed4e-123">Office 365 U.S. Government</span></span>](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc#us-government-community-compliance)
- <span data-ttu-id="fed4e-124">독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="fed4e-124">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="fed4e-125">감사, 보고서 및 인증서</span><span class="sxs-lookup"><span data-stu-id="fed4e-125">Audits, reports, and certificates</span></span>

<span data-ttu-id="fed4e-126">FBI는 CJIS 요구 사항을 준수하는 Microsoft에 대한 인증을 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-126">The FBI does not offer certification of Microsoft compliance with CJIS requirements.</span></span> <span data-ttu-id="fed4e-127">대신 Microsoft와 주 CJIS 기관 간의 계약과 Microsoft와 고객 간의 계약에 Microsoft 의 의거가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-127">Instead, a Microsoft attestation is included in agreements between Microsoft and a state's CJIS authority, and between Microsoft and its customers.</span></span>

[<span data-ttu-id="fed4e-128">Microsoft CJIS 클라우드 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fed4e-128">Microsoft CJIS Cloud Requirements</span></span>](https://aka.ms/MicrosoftCJISCloudRequirements)

## <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a><span data-ttu-id="fed4e-129">미국의 CJIS 상태(2020년 11월 5일 현재)</span><span class="sxs-lookup"><span data-stu-id="fed4e-129">CJIS status in the United States (current as of 11/5/2020)</span></span>

<span data-ttu-id="fed4e-130">녹색 지도에 강조 표시된 관리 계약을 체결한 44개 주 및 콜롬비아 교육구에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-130">44 states and the District of Columbia with management agreements, highlighted on the map in green include:</span></span>

<span data-ttu-id="fed4e-131">앨라배마, 알래스카, 애리조나, 아리조나, 앨라배마주, 플로리다, 조지아, 캘리포니아, Idaho, 일리노이, 인디애나, 아이오와, 칸사스, 킷킷, 마이네, 매사키츠, 미시간, 미네소타, 미시시피, 미주리, 몬타나, 네브래스카, 네바다, New Hampshire, New Jersey, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Washington, West Virginia, Wisconsin, and the District of Columbia.</span><span class="sxs-lookup"><span data-stu-id="fed4e-131">Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Maine, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, and the District of Columbia.</span></span>

<span data-ttu-id="fed4e-132">적용 가능한 CJIS 규제를 충족하기 위한 Microsoft의 약속을 통해 범죄자 조직은 클라우드 기반 솔루션을 구현하고 CJIS 보안 정책 V5.8을 준수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-132">Microsoft's commitment to meeting the applicable CJIS regulatory controls allows Criminal Justice organizations to implement cloud-based solutions and be compliant with CJIS Security Policy V5.8.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="fed4e-133">자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="fed4e-133">Frequently asked questions</span></span>

<span data-ttu-id="fed4e-134">**준수 정보는 어디에서 요청할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="fed4e-134">**Where can I request compliance information?**</span></span>

<span data-ttu-id="fed4e-135">관심 있는 관할권에 대한 정보는 Microsoft 계정 담당자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="fed4e-135">Contact your Microsoft account representative for information on the jurisdiction you are interested in.</span></span> <span data-ttu-id="fed4e-136">현재 <cjis@microsoft.com> 사용 가능한 서비스(상태)에 대한 자세한 내용은 연락처를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fed4e-136">Contact <cjis@microsoft.com> for information on which services are currently available in which states.</span></span>

<span data-ttu-id="fed4e-137">**Microsoft는 클라우드 서비스가 내 주 요구 사항을 준수할 수 있도록 하는 방법을 어떻게 보여 주나요?**</span><span class="sxs-lookup"><span data-stu-id="fed4e-137">**How does Microsoft demonstrate that its cloud services enable compliance with my state's requirements?**</span></span>

<span data-ttu-id="fed4e-138">Microsoft는 CSA(CJIS Systems Agency)와 정보 계약에 서명합니다. 주 CSA에서 복사본을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-138">Microsoft signs an Information Agreement with a state CJIS Systems Agency (CSA); you may request a copy from your state's CSA.</span></span> <span data-ttu-id="fed4e-139">또한 Microsoft는 고객에게 자세한 보안, 개인 정보 및 규정 준수 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-139">In addition, Microsoft provides customers with in-depth security, privacy, and compliance information.</span></span> <span data-ttu-id="fed4e-140">고객은 또한 독립적인 감사자에 의해 준비된 보안 및 준수 보고서를 검토하여 Microsoft가 관련 감사 범위에 적합한 보안 제어(예: ISO 27001)를 구현한지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-140">Customers may also review security and compliance reports prepared by independent auditors so they can validate that Microsoft has implemented security controls (such as ISO 27001) appropriate to the relevant audit scope.</span></span>

<span data-ttu-id="fed4e-141">**기관의 규정 준수 노력은 어디에서 시작하나요?**</span><span class="sxs-lookup"><span data-stu-id="fed4e-141">**Where do I start with my agency's compliance effort?**</span></span>

<span data-ttu-id="fed4e-142">[CJIS 보안 정책은](https://aka.ms/cjis-security-policy) 기관에서 CJI를 보호하기 위해 취해야 하는 예방 조치를 다합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-142">[CJIS Security Policy](https://aka.ms/cjis-security-policy) covers the precautions that your agency must take to protect CJI.</span></span> <span data-ttu-id="fed4e-143">또한 Microsoft 계정 담당자가 관할권의 요구 사항에 익숙한 사용자와 연락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-143">In addition, your Microsoft account representative can put you in touch with those familiar with the requirements of your jurisdiction</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="fed4e-144">Microsoft 준수 관리자를 사용하여 위험 평가</span><span class="sxs-lookup"><span data-stu-id="fed4e-144">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="fed4e-145">[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-145">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="fed4e-146">준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-146">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="fed4e-147">준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-147">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="fed4e-148">[준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="fed4e-148">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="fed4e-149">리소스</span><span class="sxs-lookup"><span data-stu-id="fed4e-149">Resources</span></span>

- [<span data-ttu-id="fed4e-150">범죄 행위 정보 서비스</span><span class="sxs-lookup"><span data-stu-id="fed4e-150">Criminal Justice Information Services</span></span>](https://aka.ms/cjis)
- [<span data-ttu-id="fed4e-151">CJIS 보안 정책</span><span class="sxs-lookup"><span data-stu-id="fed4e-151">CJIS Security Policy</span></span>](https://aka.ms/cjis-security-policy)
- [<span data-ttu-id="fed4e-152">Azure Government에 대한 CJIS 구현 지침</span><span class="sxs-lookup"><span data-stu-id="fed4e-152">CJIS implementation guidelines for Azure Government</span></span>](https://aka.ms/cjisimplementationguidelines)
- [<span data-ttu-id="fed4e-153">Microsoft 공통 컨트롤 허브 규정 준수 프레임 워크</span><span class="sxs-lookup"><span data-stu-id="fed4e-153">Microsoft Common Controls Hub Compliance Framework</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="fed4e-154">Microsoft Government 클라우드</span><span class="sxs-lookup"><span data-stu-id="fed4e-154">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/?linkid=2087246)
- [<span data-ttu-id="fed4e-155">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="fed4e-155">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
