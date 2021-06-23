---
title: 뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 보호 고려 사항
description: Microsoft NZ는 뉴질랜드 클라우드 컴퓨팅 프레임워크에 게시된 질문을 해결합니다.
keywords: Microsoft 365, 규정 준수, 제품
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
ms.openlocfilehash: da53b5e2cdac7095e2fc3ff9b243d2863b85fdbf
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088787"
---
# <a name="new-zealand-government-cloud-computing-security-and-privacy-considerations"></a><span data-ttu-id="1fa8a-104">뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 보호 고려 사항</span><span class="sxs-lookup"><span data-stu-id="1fa8a-104">New Zealand Government Cloud Computing Security and Privacy Considerations</span></span>

## <a name="new-zealand-government-cloud-computing-security-and-privacy-overview"></a><span data-ttu-id="1fa8a-105">뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 개요</span><span class="sxs-lookup"><span data-stu-id="1fa8a-105">New Zealand Government Cloud Computing Security and Privacy overview</span></span>

<span data-ttu-id="1fa8a-106">2015년 10월 뉴질랜드 정부는 공공 부문에서 정보 기술을 사용하는 '클라우드 우선' 정책을 재확인하는 수정된 모든 정부 ICT 전략을 인정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-106">In October 2015, the New Zealand Government endorsed a revised all-government ICT strategy that reaffirmed its 'cloud first' policy on using information technology across the public sector.</span></span> <span data-ttu-id="1fa8a-107">수정된 전략은 NZ 정부 최고 정보 책임자(GCIO)의 권한으로 개발 및 구현된 '클라우드 컴퓨팅 위험 및 보증 프레임워크'를 보유합니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-107">The revised strategy retains the 'Cloud Computing Risk and Assurance Framework' that was developed and implemented under the authority of the NZ Government Chief Information Officer (GCIO).</span></span>

<span data-ttu-id="1fa8a-108">정부는 클라우드 서비스를 평가하고 채택할 때 모든 뉴질랜드 주 정부 기관이 이 프레임워크 내에서 작업할 것으로 기대합니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-108">The government expects all New Zealand State Service agencies to work within this framework when assessing and adopting cloud services.</span></span> <span data-ttu-id="1fa8a-109">'클라우드 컴퓨팅 요구 사항'에서는 정부의 클라우드 정책 내역과 함께 클라우드 서비스를 채택할 때 기관이 해야 하는 작업을 간략하게 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-109">'Requirements for Cloud Computing' outlines what agencies must do when adopting cloud services along with an overview of the history of the government's cloud policy.</span></span>

<span data-ttu-id="1fa8a-110">GCIO는 NZ 정부 기관이 잠재적인 클라우드 솔루션에 대해 일관되고 강력한 실사 수행을 지원하기 위해 클라우드 [컴퓨팅: ISPC(정보](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html)보안 및 개인 정보 보호 고려 사항)를 게시했습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-110">To assist NZ government agencies in conducting consistent and robust due diligence on potential cloud solutions, the GCIO has published [Cloud Computing: Information Security and Privacy Considerations (ISPC)](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html).</span></span> <span data-ttu-id="1fa8a-111">이 문서에는 데이터 주권, 개인 정보, 보안, 거버넌스, 기밀성, 데이터 무결성, 가용성 및 인시던트 대응 및 관리에 초점을 맞추는 100개 이상의 질문이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-111">This document contains more than 100 questions focused on data sovereignty, privacy, security, governance, confidentiality, data integrity, availability, and incident response and management.</span></span> <span data-ttu-id="1fa8a-112">ISPC는 클라우드 서비스 공급자가 공식적인 규정 준수를 입증해야 하는 NZ 정부 표준을 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-112">The ISPC does not define a NZ government standard against which cloud service providers must demonstrate formal compliance.</span></span> <span data-ttu-id="1fa8a-113">그러나 문서에 설정된 많은 질문은 클라우드 서비스 공급자가 다양한 관련 표준을 준수하는 방식에 대한 이해의 중요성을 강조합니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-113">Many of the questions set out in the document do, however, point toward the importance of understanding how cloud service providers comply with a wide array of relevant standards.</span></span>

## <a name="microsoft-and-new-zealand-government-cloud-computing-security-and-privacy-considerations"></a><span data-ttu-id="1fa8a-114">Microsoft 및 뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 보호 고려 사항</span><span class="sxs-lookup"><span data-stu-id="1fa8a-114">Microsoft and New Zealand Government Cloud Computing Security and Privacy Considerations</span></span>

<span data-ttu-id="1fa8a-115">기관이 Microsoft 엔터프라이즈 클라우드 서비스를 분석하고 평가할 수 있도록 Microsoft 뉴질랜드는 엔터프라이즈 클라우드 서비스가 Microsoft 클라우드 서비스가 '클라우드 컴퓨팅 ISPC'에 설정된 질문을 Microsoft 클라우드 서비스가 인증된 표준에 연결하여 해결 방법을 보여 주는 문서를 제작했습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-115">To help agencies undertake their analysis and evaluation of Microsoft enterprise cloud services, Microsoft New Zealand has produced documents showing how its enterprise cloud services address the questions set out in the 'Cloud Computing ISPC' by linking them to the standards against which Microsoft cloud services are certified.</span></span> <span data-ttu-id="1fa8a-116">이러한 인증은 Microsoft가 개인 정보 및 보안 위험을 효과적으로 완화하고 데이터 주권 문제를 해결하기 위해 클라우드 서비스를 설계, 구축 및 운영하고 공공 부문 고객 모두에게 제공하는 방법의 핵심입니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-116">These certifications are central to how Microsoft assures both public and private sector customers that its cloud services are designed, built, and operated to effectively mitigate privacy and security risks and address data sovereignty concerns.</span></span> <span data-ttu-id="1fa8a-117">클라우드 [컴퓨팅 ISPC에 대한 Azure](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/) 응답은 고객이 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-117">The [Azure response to Cloud Computing ISPC](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/) is available to customers for download.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="1fa8a-118">Microsoft 범위 내 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="1fa8a-118">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="1fa8a-119">Azure 및 Azure Government</span><span class="sxs-lookup"><span data-stu-id="1fa8a-119">Azure and Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="1fa8a-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1fa8a-120">Dynamics 365</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="1fa8a-121">Intune</span><span class="sxs-lookup"><span data-stu-id="1fa8a-121">Intune</span></span>
- <span data-ttu-id="1fa8a-122">독립형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스</span><span class="sxs-lookup"><span data-stu-id="1fa8a-122">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- [<span data-ttu-id="1fa8a-123">Office 365</span><span class="sxs-lookup"><span data-stu-id="1fa8a-123">Office 365</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=2077751)
- <span data-ttu-id="1fa8a-124">Exchange Online, SharePoint 온라인 및 Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-124">Exchange Online, SharePoint Online, and Microsoft Teams.</span></span> <span data-ttu-id="1fa8a-125">Microsoft NZ는 GCIO 팀과 함께 통합을 위한 참조 아키텍처를 개발하기 위해 Exchange Online 참조 아키텍처를 개발하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-125">Microsoft NZ has worked with the GCIO team to develop a reference architecture for integrating Exchange Online and SEEMail.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1fa8a-126">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="1fa8a-126">Frequently asked questions</span></span>

<span data-ttu-id="1fa8a-127">**프레임워크는 누구에게 적용하나요?**</span><span class="sxs-lookup"><span data-stu-id="1fa8a-127">**To whom does the framework apply?**</span></span>

<span data-ttu-id="1fa8a-128">GCIO 위임, 공공 및 비공용 서비스 부서, 20개 교육구 보건 위원회 및 7개 교육구 기관에 속하는 조직은 클라우드 서비스 사용을 결정할 때 프레임워크를 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-128">Organizations that fall under the GCIO mandate, the public and non-public service departments, the 20 district health boards, and 7 Crown entities, must adhere to the framework when they are deciding on the use of a cloud service.</span></span>

<span data-ttu-id="1fa8a-129">**기관에서 ICT 시스템의 인증 프로세스에서 이 프레임워크에 대한 Microsoft의 응답을 사용할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="1fa8a-129">**Can my agency use Microsoft's responses to this framework in the certification process of our ICT systems?**</span></span>

<span data-ttu-id="1fa8a-130">기관이 뉴질랜드 정보 보안 설명서에 따라 ICT 시스템의 인증 및 [](https://go.microsoft.com/fwlink/p/?linkid=2099496)인증을 획득해야 하는 경우 이러한 응답을 분석의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fa8a-130">If your agency is required to undertake certification and accreditation of its ICT system under the [New Zealand Information Security Manual](https://go.microsoft.com/fwlink/p/?linkid=2099496), then you can use these responses as part of your analysis.</span></span>

## <a name="resources"></a><span data-ttu-id="1fa8a-131">리소스</span><span class="sxs-lookup"><span data-stu-id="1fa8a-131">Resources</span></span>

- [<span data-ttu-id="1fa8a-132">해상에서 호스팅되는 Office 생산성 서비스에 대한 보안 요구 사항: Office 365</span><span class="sxs-lookup"><span data-stu-id="1fa8a-132">Security requirements for offshore hosted Office productivity services: conformance guide for Office 365</span></span>](https://aka.ms/o365-gcio-conformance-guidance)
- [<span data-ttu-id="1fa8a-133">NZ Government ICT Strategy 2015</span><span class="sxs-lookup"><span data-stu-id="1fa8a-133">NZ Government ICT Strategy 2015</span></span>](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [<span data-ttu-id="1fa8a-134">클라우드 컴퓨팅: ISPC(정보 보안 및 개인 정보 보호 고려 사항)</span><span class="sxs-lookup"><span data-stu-id="1fa8a-134">Cloud Computing: Information Security and Privacy Considerations (ISPC)</span></span>](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [<span data-ttu-id="1fa8a-135">Microsoft 온라인 서비스 사용 약관</span><span class="sxs-lookup"><span data-stu-id="1fa8a-135">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="1fa8a-136">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="1fa8a-136">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a><span data-ttu-id="1fa8a-137">'클라우드 컴퓨팅 IPSC'에 대한 Microsoft 응답</span><span class="sxs-lookup"><span data-stu-id="1fa8a-137">Microsoft responses to 'Cloud Computing IPSC'</span></span>

- [<span data-ttu-id="1fa8a-138">Azure</span><span class="sxs-lookup"><span data-stu-id="1fa8a-138">Azure</span></span>](https://aka.ms/Azure-NZ-response)
- [<span data-ttu-id="1fa8a-139">Intune</span><span class="sxs-lookup"><span data-stu-id="1fa8a-139">Intune</span></span>](https://aka.ms/Intune-NZ-response)
- [<span data-ttu-id="1fa8a-140">Office 365</span><span class="sxs-lookup"><span data-stu-id="1fa8a-140">Office 365</span></span>](https://aka.ms/O365-NZ-Response)
- [<span data-ttu-id="1fa8a-141">Power BI</span><span class="sxs-lookup"><span data-stu-id="1fa8a-141">Power BI</span></span>](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)
