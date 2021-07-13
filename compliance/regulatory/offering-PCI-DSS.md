---
title: PCI(Payment Card Industry) DSS(Data Security Standard)
description: Azure, SharePoint Online 및 비즈니스용 OneDrive는 Payment Card Industry Data Security 표준 수준 1 버전 3.2를 준수합니다.
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
ms.openlocfilehash: ab92c2d12477e0e7fa1890ae25e06d264305e95c
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384388"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a><span data-ttu-id="1cab1-104">PCI(Payment Card Industry) DSS(Data Security Standard)</span><span class="sxs-lookup"><span data-stu-id="1cab1-104">Payment Card Industry (PCI) Data Security Standard (DSS)</span></span>

## <a name="pci-dss-overview"></a><span data-ttu-id="1cab1-105">PCI DSS 개요</span><span class="sxs-lookup"><span data-stu-id="1cab1-105">PCI DSS overview</span></span>

<span data-ttu-id="1cab1-106">PCI(Payment Card Industry) DSS(Data Security Standard)는 신용 카드 데이터에 대한 통제를 강화하여 사기를 방지하도록 고안된 글로벌 정보 보안 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-106">The Payment Card Industry (PCI) Data Security Standards (DSS) is a global information security standard designed to prevent fraud through increased control of credit card data.</span></span> <span data-ttu-id="1cab1-107">모든 규모의 조직은 Visa, MasterCard, American Express, Discover, JCB(Japan Credit Bureau) 등 5개 주요 신용 카드 브랜드의 결제 카드를 수락하는 경우 PCI DSS 표준을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-107">Organizations of all sizes must follow PCI DSS standards if they accept payment cards from the five major credit card brands, Visa, MasterCard, American Express, Discover, and the Japan Credit Bureau (JCB).</span></span> <span data-ttu-id="1cab1-108">지불 및 카드 소유자 데이터를 저장, 처리 또는 전송하는 모든 조직은 PCI DSS를 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-108">Compliance with PCI DSS is required for any organization that stores, processes, or transmits payment and cardholder data.</span></span>

## <a name="microsoft-and-pci-dss"></a><span data-ttu-id="1cab1-109">Microsoft와 PCI DSS</span><span class="sxs-lookup"><span data-stu-id="1cab1-109">Microsoft and PCI DSS</span></span>

<span data-ttu-id="1cab1-110">Microsoft는 승인된 QSA(Qualified Security Assessor)를 사용하여 연간 PCI DSS 평가를 완료했습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-110">Microsoft completed an annual PCI DSS assessment using an approved Qualified Security Assessor (QSA).</span></span> <span data-ttu-id="1cab1-111">감사자는 인프라, 개발, 운영, 관리, 지원 및 범위 내 서비스 검증을 포함하여 Microsoft Azure, 비즈니스용 Microsoft OneDrive 및 Microsoft SharePoint Online 환경을 검토했습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-111">The auditors reviewed Microsoft Azure, Microsoft OneDrive for Business, and Microsoft SharePoint Online  environments, which include validating the infrastructure, development, operations, management, support, and in-scope services.</span></span> <span data-ttu-id="1cab1-112">PCI DSS는 거래량을 기준으로 네 가지 규정 준수 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-112">The PCI DSS designates four levels of compliance based on transaction volume.</span></span> <span data-ttu-id="1cab1-113">Azure, 비즈니스용 OneDrive, SharePoint Online은 PCI DSS 버전 3.2의 서비스 공급자 수준 1(최고 거래량이 연간 6백만 건 이상)의 규정 준수 인증을 획득했습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-113">Azure, OneDrive for Business, and SharePoint Online are certified as compliant under PCI DSS version 3.2 at Service Provider Level 1 (the highest volume of transactions, more than 6 million a year).</span></span>

<span data-ttu-id="1cab1-114">평가는 AoC(Attestation on Compliance)로 제공되며 이는 고객이 열람 가능하고 QSA에서 발행한 Report on Compliance (RoC)에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-114">The assessment results in an Attestation of Compliance (AoC), which is available to customers and Report on Compliance (RoC) issued by the QSA.</span></span> <span data-ttu-id="1cab1-115">규정 준수에 대한 유효 기간은 감사를 통과하여 평가자로부터 AoC를 받은 시점부터 AoC에 서명한 날짜가 포함된 연도의 말일까지입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-115">The effective period for compliance begins upon passing the audit and receiving the AoC from the assessor and ends one year from the date the AoC is signed.</span></span> 

<span data-ttu-id="1cab1-116">카드 데이터 전용 네트워크(CDE) 또는 카드 처리 서비스를 개발하려는 고객은 많은 기본적인 부분에서 이러한 검증을 사용할 수 있습니다. 이를 통해 자체적으로 PCI DSS 인증을 얻기 위한 관련된 작업과 비용을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-116">Customers who want to develop a cardholder environment or card processing service can use these validations in many of the underlying portions, thereby reducing the associated effort and costs of getting their own PCI DSS certification.</span></span>

<span data-ttu-id="1cab1-117">Azure, 비즈니스용 OneDrive, SharePoint Online의 PCI DSS 규정 준수 상태가 고객이 이러한 플랫폼에서 빌드하거나 호스팅하는 서비스에 대한 PCI DSS 인증으로 자동으로 전환되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-117">It is important to understand that PCI DSS compliance status for Azure, OneDrive for Business, and SharePoint Online not automatically translate to PCI DSS certification for the services that customers build or host on these platforms.</span></span> <span data-ttu-id="1cab1-118">고객은 일부 PCI DSS 요구 사항을 준수하는지 확인해야 할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-118">Customers are responsible for ensuring that they achieve compliance with PCI DSS requirements.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="1cab1-119">Microsoft 범위 내 클라우드 플랫폼 및 서비스</span><span class="sxs-lookup"><span data-stu-id="1cab1-119">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="1cab1-120">Azure 및 Azure Government</span><span class="sxs-lookup"><span data-stu-id="1cab1-120">Azure and Azure Government</span></span>
- <span data-ttu-id="1cab1-121">Intune</span><span class="sxs-lookup"><span data-stu-id="1cab1-121">Intune</span></span>
- <span data-ttu-id="1cab1-122">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="1cab1-122">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="1cab1-123">엔드포인트용 Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="1cab1-123">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- <span data-ttu-id="1cab1-124">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="1cab1-124">Microsoft Graph</span></span>
- <span data-ttu-id="1cab1-125">Office 365</span><span class="sxs-lookup"><span data-stu-id="1cab1-125">Office 365</span></span>
- <span data-ttu-id="1cab1-126">비즈니스용 OneDrive 및 SharePoint Online(미국에만 해당)</span><span class="sxs-lookup"><span data-stu-id="1cab1-126">OneDrive for Business and SharePoint Online (United States only)</span></span>
- <span data-ttu-id="1cab1-127">독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 PowerApps 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="1cab1-127">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="1cab1-128">독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power Automate(이전 Microsoft Flow) 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="1cab1-128">Power Automate (either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite)</span></span>
- <span data-ttu-id="1cab1-129">독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="1cab1-129">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="azure-dynamics-365-and-pci-dss"></a><span data-ttu-id="1cab1-130">Azure, Dynamics 365 및 PCI DSS</span><span class="sxs-lookup"><span data-stu-id="1cab1-130">Azure, Dynamics 365, and PCI DSS</span></span>

<span data-ttu-id="1cab1-131">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure PCI DSS 제품](/azure/compliance/offerings/offering-pci-dss)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1cab1-131">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure PCI DSS offering](/azure/compliance/offerings/offering-pci-dss).</span></span>

## <a name="office-365-and-pci-dss"></a><span data-ttu-id="1cab1-132">Office 365 및 PCI DSS</span><span class="sxs-lookup"><span data-stu-id="1cab1-132">Office 365 and PCI DSS</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="1cab1-133">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="1cab1-133">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="1cab1-134">Office 365 적용 가능성 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="1cab1-134">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="1cab1-135">다음 표를 사용하여 Office 365 서비스 및 구독에 대한 적용 가능성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-135">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="1cab1-136">**적용 가능성**</span><span class="sxs-lookup"><span data-stu-id="1cab1-136">**Applicability**</span></span> | <span data-ttu-id="1cab1-137">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="1cab1-137">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="1cab1-138">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="1cab1-138">**Office 365**</span></span> | <span data-ttu-id="1cab1-139">비즈니스용 OneDrive(미국), SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1cab1-139">OneDrive for Business (United States), SharePoint Online</span></span> |

### <a name="office-365-audit-reports-and-certificates"></a><span data-ttu-id="1cab1-140">Office 365 감사, 보고서 및 인증</span><span class="sxs-lookup"><span data-stu-id="1cab1-140">Office 365 audit, reports, and certificates</span></span>

- [<span data-ttu-id="1cab1-141">비즈니스용 OneDrive 및 SharePoint Online PCI DSS 준수 증명(AoC)</span><span class="sxs-lookup"><span data-stu-id="1cab1-141">OneDrive for Business and SharePoint Online PCI DSS Attestation of Compliance (AoC)</span></span>](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a><span data-ttu-id="1cab1-142">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="1cab1-142">Frequently asked questions</span></span>

<span data-ttu-id="1cab1-143">**AoC(Attestation on Compliance) 표지 페이지에 ‘2018년 6월’이 표시된 이유는 무엇인가요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-143">**Why does the Attestation of Compliance (AoC) cover page say 'June 2018'?**</span></span>

<span data-ttu-id="1cab1-144">표지 페이지의 날짜 2018년 6월은 AoC 서식 파일이 게시된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-144">The June 2018 date on the cover page is when the AoC template was published.</span></span> <span data-ttu-id="1cab1-145">평가 날짜는 2조를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1cab1-145">Refer to Section 2 for the date of the assessment.</span></span> 

<span data-ttu-id="1cab1-146">**PA DSS와 PCI DSS는 서로 어떤 관계인가요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-146">**What is the relationship between the PA DSS and PCI DSS?**</span></span>

<span data-ttu-id="1cab1-147">PA DSS(Payment Application Data Security Standard)는 PCI DSS를 준수하고, Visa의 지불 응용 프로그램 모범 사례를 대체하고, 다른 주요 카드 발급자의 규정 준수(compliance) 요건을 통합하는 요건 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-147">The Payment Application Data Security Standard (PA DSS) is a set of requirements that comply with the PCI DSS, and replaces Visa's Payment Application Best Practices, and consolidates the compliance requirements of the other primary card issuers.</span></span> <span data-ttu-id="1cab1-148">소프트웨어 공급업체에서는 PA DSS에 따라 카드 인증 또는 결제 프로세스의 일환으로 카드 소유자 지불 데이터를 저장, 처리 또는 전송하는 타사 응용 프로그램을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-148">The PA DSS helps software vendors develop third-party applications that store, process, or transmit cardholder payment data as part of a card authorization or settlement process.</span></span> <span data-ttu-id="1cab1-149">소매업체에서는 PCI DSS 규정을 효율적으로 준수하려면 PA DSS 인증 응용 프로그램을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-149">Retailers must use PA DSS certified applications to efficiently achieve their PCI DSS compliance.</span></span> <span data-ttu-id="1cab1-150">PA DSS는 Azure에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-150">The PA DSS does not apply to Azure.</span></span>

<span data-ttu-id="1cab1-151">**전표 매입업체란 무엇인가요? Azure는 매입업체를 이용하나요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-151">**What is an acquirer and does Azure use one?**</span></span>

<span data-ttu-id="1cab1-152">전표 매입업체란 결제 카드 거래를 처리하는 은행 또는 기타 기관입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-152">An acquirer is a bank or other entity that processes payment card transactions.</span></span> <span data-ttu-id="1cab1-153">Azure는 카드 결제 처리 서비스를 제공하지 않으므로 전표 매입업체를 이용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-153">Azure does not offer payment card processing as a service and thus does not use an acquirer.</span></span>

<span data-ttu-id="1cab1-154">**PCI DSS는 어떤 회사 및 판매자에게 적용되나요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-154">**To what organizations and merchants does the PCI DSS apply?**</span></span>

<span data-ttu-id="1cab1-155">거래의 규모나 수에 상관없이 카드 소유자 데이터를 수락, 전송 또는 저장하는 모든 회사에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-155">PCI DSS applies to any company, no matter the size, or number of transactions, that accepts, transmits, or stores cardholder data.</span></span> <span data-ttu-id="1cab1-156">즉, 고객이 신용 카드 또는 직불 카드를 사용하여 회사에 지불하는 경우 PCI DSS 요구 사항이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-156">That is, if any customer ever pays a company using a credit or debit card, then the PCI DSS requirements apply.</span></span> <span data-ttu-id="1cab1-157">기업은 12개월 동안의 총 거래량을 기준으로 네 가지 수준 중 하나로 검증됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-157">Companies are validated at one of four levels based on the total transaction volume over a 12-month period.</span></span> <span data-ttu-id="1cab1-158">연간 처리하는 거래 건수가 600만 건 초과인 기업은 수준 1, 100만 ~ 600만 건인 기업은 수준 2, 2만 ~ 1백만 건인 기업은 수준 3, 2만 건 미만인 기업은 수준 4에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-158">Level 1 is for companies that process over 6 million transactions a year; Level 2 for 1 million to 6 million transactions; Level 3 is for 20,000 to 1 million transactions; and Level 4 is for fewer than 20,000 transactions.</span></span>

<span data-ttu-id="1cab1-159">**비즈니스용 OneDrive 및 SharePoint Online가 미국 이외의 지역에서 PCI DSS를 준수할 계획이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-159">**Are there plans for OneDrive for Business and SharePoint Online to be PCI DSS-compliant outside of the United States?**</span></span>

<span data-ttu-id="1cab1-160">현재 비즈니스용 OneDrive 및 SharePoint Online은 미국(US)에서만 PCI-DSS를 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-160">Currently OneDrive for Business and SharePoint Online is PCI-DSS compliant only in the United States (US).</span></span> <span data-ttu-id="1cab1-161">Microsoft는 미국 이외의 지역에 대한 요구 사항과 타임라인을 평가하고 다른 지역이 로드맵에 추가되면 업데이트를 제공할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-161">Microsoft will evaluate the requirements and timelines for regions outside of US and provide updates when and if other regions are added to the roadmap.</span></span>

<span data-ttu-id="1cab1-162">**비즈니스용 OneDrive 및 SharePoint Online 범위 내에 어떤 것이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="1cab1-162">**What is in-scope for OneDrive for Business and SharePoint Online?**</span></span>

<span data-ttu-id="1cab1-163">현재 비즈니스용 OneDrive 및 SharePoint Online에 업로드된 파일과 문서만 PCI DSS를 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-163">Currently, only files and documents uploaded to OneDrive for Business and SharePoint Online will be compliant with PCI DSS.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="1cab1-164">Microsoft 준수 관리자를 사용하여 위험을 평가해 보세요.</span><span class="sxs-lookup"><span data-stu-id="1cab1-164">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="1cab1-165">[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-165">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="1cab1-166">준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-166">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="1cab1-167">준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-167">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="1cab1-168">[준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="1cab1-168">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="1cab1-169">리소스</span><span class="sxs-lookup"><span data-stu-id="1cab1-169">Resources</span></span>

- [<span data-ttu-id="1cab1-170">PCI 보안 표준 심의회(영문)</span><span class="sxs-lookup"><span data-stu-id="1cab1-170">PCI Security Standards Council</span></span>](https://www.pcisecuritystandards.org/)
- [<span data-ttu-id="1cab1-171">PCI 데이터 보안 표준(영문)</span><span class="sxs-lookup"><span data-stu-id="1cab1-171">PCI Data Security Standard</span></span>](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [<span data-ttu-id="1cab1-172">PCI DSS 빠른 참조 설명서(영문)</span><span class="sxs-lookup"><span data-stu-id="1cab1-172">PCI DSS Quick Reference Guide</span></span>](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [<span data-ttu-id="1cab1-173">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="1cab1-173">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
