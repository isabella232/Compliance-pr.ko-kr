---
title: Office Server GDPR
description: 온-프레미스 Office 서버에서 유럽 연합 일반 개인정보보호법(GDPR) 요구 사항을 해결하는 방법을 알아봅니다.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496085"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="e2620-103">Office 온-프레미스 Server GDPR</span><span class="sxs-lookup"><span data-stu-id="e2620-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="e2620-p101">GDPR(일반 데이터 보호 규정)은 조직에 요구 사항을 소개하여 개인 데이터를 보호하고 데이터 주체 요청에 적절하게 응답합니다. 이 일련의 문서는 온-프레미스 작업에 권장되는 접근 방식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e2620-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="e2620-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="e2620-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="e2620-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="e2620-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="e2620-108">비즈니스용 Skype 서버</span><span class="sxs-lookup"><span data-stu-id="e2620-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="e2620-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="e2620-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="e2620-110">Office Web Apps Server 및 Office Online Server</span><span class="sxs-lookup"><span data-stu-id="e2620-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="e2620-111">온-프레미스 파일 공유</span><span class="sxs-lookup"><span data-stu-id="e2620-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="e2620-112">GDPR 및 Microsoft가 지원하는 방법에 대한 자세한 내용은 [Microsoft 보안 센터](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2620-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="e2620-p102">온-프레미스 데이터로 작업을 수행하기 전에 먼저 법률 및 규정 준수 팀에 문의하여 안내를 받고 개인 데이터를 사용하여 작업하는 접근 방식 및 기존 분류 스키마에 대해 알아보세요. 수 및 기존 분류에 대한 자세한 내용은  스키마 및 개인 데이터 작업을 위한 접근 방식을합니다. Microsoft는 [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>)에서 Microsoft GDPR 데이터 검색 도구 키트의 분류 스키마를 개발하고 확장하는 권장 사항을 제공합니다. 또한, 이 도구 키트는 원하는 경우 더 정교한 데이터 거버넌스 기능을 사용할 수 있는 클라우드로 온-프레미스 데이터를 이동하는 접근 방식을 설명합니다. 이 섹션에 나와 있는 문서는 온-프레미스로 유지하기 위한 데이터 권장 사항을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e2620-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="e2620-p103">다음 그림은 이러한 각 작업에 사용하여 개인 데이터를 검색, 분류, 보호, 모니터링할 수 있는 권장 기능을 나열합니다. 자세한 내용은 이 섹션의 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2620-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![작업 전반에서 개인 데이터를 검색, 분류, 보호 및 모니터링하는 기능을 설명하는 다이어그램](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="e2620-120">그림 설명</span><span class="sxs-lookup"><span data-stu-id="e2620-120">Illustration description</span></span>

<span data-ttu-id="e2620-121">다음 표에서는 이해를 돕기 위해 그림과 동일한 예제를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e2620-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="e2620-122">작업</span><span class="sxs-lookup"><span data-stu-id="e2620-122">Action</span></span>|<span data-ttu-id="e2620-123">Windows Server 파일 공유</span><span class="sxs-lookup"><span data-stu-id="e2620-123">Windows Server file shares</span></span>|<span data-ttu-id="e2620-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="e2620-124">SharePoint Server</span></span>|<span data-ttu-id="e2620-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="e2620-125">Exchange Server</span></span>|<span data-ttu-id="e2620-126">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="e2620-126">Skype for Business</span></span>|<span data-ttu-id="e2620-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="e2620-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="e2620-128">검색</span><span class="sxs-lookup"><span data-stu-id="e2620-128">Discover</span></span>|<span data-ttu-id="e2620-129">Azure Information Protection 스캐너<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e2620-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="e2620-130">검색 센터 또는 eDiscovery(데이터가 분류된 후)</span><span class="sxs-lookup"><span data-stu-id="e2620-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="e2620-131">Azure Information Protection 스캐너<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e2620-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="e2620-132">Exchange eDiscovery 포털</span><span class="sxs-lookup"><span data-stu-id="e2620-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="e2620-133">Exchange eDiscovery 포털</span><span class="sxs-lookup"><span data-stu-id="e2620-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="e2620-134">검색 및 내보내기용 SQL 스크립트</span><span class="sxs-lookup"><span data-stu-id="e2620-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="e2620-135">분류</span><span class="sxs-lookup"><span data-stu-id="e2620-135">Classify</span></span>|<span data-ttu-id="e2620-136">Azure Information Protection 스캐너<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e2620-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="e2620-137">Office 365 중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="e2620-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="e2620-138">Azure Information Protection 스캐너<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e2620-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="e2620-139">Office 365 중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="e2620-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="e2620-140">Exchange 보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="e2620-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="e2620-141">Exchange 보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="e2620-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="e2620-142">보호</span><span class="sxs-lookup"><span data-stu-id="e2620-142">Protect</span></span>||<span data-ttu-id="e2620-143">Exchange Server 데이터 손실 방지 규칙</span><span class="sxs-lookup"><span data-stu-id="e2620-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="e2620-144">IRM 보호에 대한 라이브러리 사용 권한</span><span class="sxs-lookup"><span data-stu-id="e2620-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="e2620-145">Exchange Server 데이터 손실 방지 규칙</span><span class="sxs-lookup"><span data-stu-id="e2620-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="e2620-146">Exchange Server와의 IRM 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="e2620-147">모니터링</span><span class="sxs-lookup"><span data-stu-id="e2620-147">Monitor</span></span>|<span data-ttu-id="e2620-148">SIEM 도구와 로그 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="e2620-149">SIEM 도구와 로그 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="e2620-150">SIEM 도구와 로그 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="e2620-151">SIEM 도구와 로그 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="e2620-152">SIEM 도구와 로그 통합</span><span class="sxs-lookup"><span data-stu-id="e2620-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="e2620-153"><sup>\*</sup> 보호 기능이 파일을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="e2620-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="e2620-154">따라서 SharePoint Server가 보호된 파일에서 중요한 정보 유형을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2620-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
