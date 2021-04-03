---
title: Microsoft 365의 관리 액세스 제어
description: 이 문서에서는 Microsoft 365의 관리 액세스 제어 및 데이터 분류에 대한 개요를 제공합니다.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497698"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="90aa3-103">Microsoft 365의 관리 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="90aa3-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="90aa3-104">Microsoft는 Microsoft의 고객 콘텐츠에 대한 액세스를 의도적으로 제한하면서 대부분의 Microsoft 365 작업을 자동화하는 시스템 및 제어에 많은 투자를 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="90aa3-105">인간은 서비스를 관리하고 소프트웨어는 서비스를 운영합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="90aa3-106">이 구조를 통해 Microsoft는 Microsoft 365를 대규모로 관리하고 고객 콘텐츠에 대한 내부 위협 위험을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="90aa3-107">기본적으로 Microsoft 엔지니어는 Microsoft 365의 고객 콘텐츠에 대한 제로 스텐딩 관리 권한과 제로 스텐딩 액세스 권한을 습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="90aa3-108">Microsoft 엔지니어는 제한된 기간 동안 고객 콘텐츠에 대한 액세스 권한을 제한, 감사 및 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="90aa3-109">액세스는 서비스 작업에 필요한 경우와 Microsoft 고위 관리 구성원이 승인한 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="90aa3-110">고객 Lockbox 라이선스 고객의 경우 고객은 Microsoft 365에서 호스트되는 콘텐츠에 대한 액세스 승인을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="90aa3-111">Microsoft는 여러 형태의 클라우드 배달을 사용하여 온라인 서비스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="90aa3-112">**공용 클라우드:** Microsoft 365, Azure의 다중 테넌트 버전 및 북미, 남미, 유럽, 아시아, 오스트레일리아 등에서 호스팅되는 기타 서비스를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="90aa3-113">**국가 클라우드:** 중국의 Microsoft 365(21Vianet에서 운영) 및 독일의 Microsoft 365(Microsoft에서 운영하지만 독일 데이터 수탁자인 독일어 데이터 수탁자, 독일어 Telekom)는 고객 데이터를 포함하는 고객 데이터 및 시스템에 대한 Microsoft의 액세스를 제어하고 모니터링하는 모델에 따라 미국 외부의 모든 주권자 및 타사 운영 클라우드(이전에 언급한 클라우드 제외)를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="90aa3-114">**정부 클라우드:** 미국 정부 고객에게 제공된 Microsoft 365 및 Azure 서비스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="90aa3-115">이 문서의 목적을 위해 Microsoft 365 서비스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="90aa3-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="90aa3-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="90aa3-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="90aa3-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="90aa3-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="90aa3-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="90aa3-119">비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="90aa3-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="90aa3-120">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="90aa3-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="90aa3-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="90aa3-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="90aa3-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="90aa3-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="90aa3-123">Microsoft 365 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="90aa3-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="90aa3-124">액세스 제어를 위해 Microsoft는 Microsoft 365 데이터를 고객 데이터 또는 기타 유형의 데이터로 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="90aa3-125">고객 데이터</span><span class="sxs-lookup"><span data-stu-id="90aa3-125">Customer data</span></span>

<span data-ttu-id="90aa3-126">고객 데이터는 Microsoft 365 서비스를 사용할 때 고객이 제공하거나 고객을 대신하여 제공한 모든 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="90aa3-127">이 데이터는 다음을 포함하여 Microsoft 365 사용자가 직접 만들거나 업로드한 고객 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="90aa3-128">전자 메일</span><span class="sxs-lookup"><span data-stu-id="90aa3-128">Emails</span></span>
- <span data-ttu-id="90aa3-129">SharePoint Online 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="90aa3-129">SharePoint Online content</span></span>
- <span data-ttu-id="90aa3-130">인스턴트 메시지</span><span class="sxs-lookup"><span data-stu-id="90aa3-130">Instant messages</span></span>
- <span data-ttu-id="90aa3-131">일정 항목</span><span class="sxs-lookup"><span data-stu-id="90aa3-131">Calendar items</span></span>
- <span data-ttu-id="90aa3-132">문서</span><span class="sxs-lookup"><span data-stu-id="90aa3-132">Documents</span></span>
- <span data-ttu-id="90aa3-133">Contacts</span><span class="sxs-lookup"><span data-stu-id="90aa3-133">Contacts</span></span>
- <span data-ttu-id="90aa3-134">EUII(최종 사용자 식별 정보)(사용자에게 고유하거나 개별 사용자에게 연결 가능하지만 고객 콘텐츠는 포함하지 않는 데이터)</span><span class="sxs-lookup"><span data-stu-id="90aa3-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="90aa3-135">기타 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="90aa3-135">Other types of data</span></span>

<span data-ttu-id="90aa3-136">기타 데이터 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-136">Other types of data include:</span></span>

- <span data-ttu-id="90aa3-137">**계정 데이터:** 관리 데이터(관리자가 서비스를 등록하거나 구매할 때 제공한 정보) 및 결제 데이터(신용 카드 세부 정보 등 결제 수단에 대한 정보)가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="90aa3-138">**조직 식별이 가능한 정보:** 테넌트, 사용 현황 데이터를 식별하는 데 사용되는 데이터를 포함하며 개별 사용자 또는 고객 콘텐츠에 포함될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="90aa3-139">**시스템 메타데이터:** 구성 설정, 시스템 상태, Microsoft IP 주소 및 구독 및 테넌트에 대한 기술 정보를 포함하는 서비스 로그를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="90aa3-140">Microsoft는 고객 데이터 또는 액세스 제어 데이터에 대한 승인되지 않은 액세스 권한을 아무도 가지지 않도록 액세스 제어 메커니즘을 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="90aa3-141">액세스 제어 데이터는 고객 콘텐츠 또는 EUII, Microsoft 암호, 보안 인증서 및 기타 인증 관련 데이터에 대한 액세스를 포함하여 환경 내의 다른 유형의 데이터 또는 기능에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="90aa3-142">또한 액세스 제어 메커니즘은 Microsoft 365 프로덕션 환경에 대한 승인되지 않은 물리적, 논리적 또는 원격 액세스를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="90aa3-143">Microsoft 365를 운영하기 위해 Microsoft에서 사용하는 세 가지 액세스 제어 범주가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="90aa3-144">Isolation controls</span><span class="sxs-lookup"><span data-stu-id="90aa3-144">Isolation controls</span></span>
- <span data-ttu-id="90aa3-145">직원 컨트롤</span><span class="sxs-lookup"><span data-stu-id="90aa3-145">Personnel controls</span></span>
- <span data-ttu-id="90aa3-146">기술 컨트롤</span><span class="sxs-lookup"><span data-stu-id="90aa3-146">Technology controls</span></span>

<span data-ttu-id="90aa3-147">이러한 컨트롤을 결합하면 Microsoft 365에서 악의적인 작업을 방지하고 감지하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="90aa3-148">Microsoft에서 사용하는 통제, 직원 및 기술 컨트롤 외에도 네 번째 범주의 제어가 있습니다. 즉, 고객이 구현하는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="90aa3-149">Microsoft 365를 사용하면 데이터 관리 방식과 동일한 방식으로 데이터를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="90aa3-150">Microsoft 365에 대한 조직에 등록하는 사용자가 자동으로 전역 관리자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="90aa3-151">전역 관리자는 관리 포털의 모든 기능에 액세스할 수 있으며 다음을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="90aa3-152">사용자 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="90aa3-152">Create or edit users</span></span>
- <span data-ttu-id="90aa3-153">다른 사용자에게 관리자 역할 할당</span><span class="sxs-lookup"><span data-stu-id="90aa3-153">Assign admin roles to others</span></span>
- <span data-ttu-id="90aa3-154">사용자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="90aa3-154">Reset user passwords</span></span>
- <span data-ttu-id="90aa3-155">사용자 라이선스 관리</span><span class="sxs-lookup"><span data-stu-id="90aa3-155">Manage user licenses</span></span>
- <span data-ttu-id="90aa3-156">도메인 관리</span><span class="sxs-lookup"><span data-stu-id="90aa3-156">Manage domains</span></span>
- <span data-ttu-id="90aa3-157">고객 Lockbox 요청 승인</span><span class="sxs-lookup"><span data-stu-id="90aa3-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="90aa3-158">각 조직에서는 관리자 계정을 두 개 이상 구성하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="90aa3-159">대기업 조직의 경우 다양한 기능을 하는 특수한 관리자 계정을 추천합니다.</span><span class="sxs-lookup"><span data-stu-id="90aa3-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="90aa3-160">관리자 역할 및 사용 권한을 할당하는 데 대한 자세한 내용은 [관리자](/microsoft-365/admin/add-users/assign-admin-roles) 역할 할당 및 관리자 역할 [정보를 참조하세요.](/microsoft-365/admin/add-users/about-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="90aa3-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="90aa3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90aa3-161">Related Links</span></span>

- [<span data-ttu-id="90aa3-162">Microsoft 365에서 고지</span><span class="sxs-lookup"><span data-stu-id="90aa3-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="90aa3-163">Microsoft 사전 고용 차단</span><span class="sxs-lookup"><span data-stu-id="90aa3-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="90aa3-164">Microsoft 클라우드 백그라운드 검사</span><span class="sxs-lookup"><span data-stu-id="90aa3-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="90aa3-165">액세스 제어 모니터링 및 감사</span><span class="sxs-lookup"><span data-stu-id="90aa3-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="90aa3-166">Yammer Enterprise 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="90aa3-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
