---
title: GDPR 검색, 보호 및 Microsoft 365 개발/테스트 환경에서 보고
description: Microsoft 365 개발/테스트 환경에서 GDPR에 맞춰 PII(개인 식별이 가능한 정보)를 구성하고 입증하는 방법을 알아봅니다.
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
- MS-Compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: a12e8e735df05004e63080f22c3c9b4de5749506
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496655"
---
# <a name="gdpr-discovery-protection-and-reporting-in-the-devtest-environment"></a><span data-ttu-id="a2132-103">개발/테스트 환경에서 GDPR 검색, 보호 및 보고</span><span class="sxs-lookup"><span data-stu-id="a2132-103">GDPR discovery, protection, and reporting in the dev/test environment</span></span>

 <span data-ttu-id="a2132-104">**요약:** Microsoft 365의 GDPR 기능을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-104">**Summary:** Demonstrate GDPR capabilities in Microsoft 365.</span></span>

<span data-ttu-id="a2132-105">이 문서에서는 Microsoft 365 개발/테스트 환경에서 GDPR(일반 데이터 보호 규정)에 대한 PII(개인 식별 정보) 검색, 보호 및 보고를 구성하고 설명하는 방법에 관해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-105">This article describes how you configure and demonstrate personally identifiable information (PII) discovery, protection, and reporting for the General Data Protection Regulation (GDPR) in a Microsoft 365 dev/test environment.</span></span>

## <a name="phase-1-create-and-configure-your-trial-microsoft-365-subscription"></a><span data-ttu-id="a2132-106">1단계: 평가판 Microsoft 365 구독 만들기 및 구성하기</span><span class="sxs-lookup"><span data-stu-id="a2132-106">Phase 1: Create and configure your trial Microsoft 365 subscription</span></span>

<span data-ttu-id="a2132-107">먼저 [Microsoft 365 개발/테스트 환경](/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) 문서의 2단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-107">First, follow the steps in [Phase 2 of the Microsoft 365 dev/test environment](/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) article.</span></span>

<span data-ttu-id="a2132-108">다음으로, eDiscovery 관리자를 구성하려면 다음 단계를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-108">Next, use these steps to configure the eDiscovery manager:</span></span>

1. <span data-ttu-id="a2132-109">전역 관리자 계정을 사용하여 Microsoft 365 평가판 테넌트에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-109">Sign in to your Microsoft 365 trial tenant with your global administrator account.</span></span>
2. <span data-ttu-id="a2132-110">Microsoft 365 홈 페이지에서 **보안 및 준수** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-110">From the Microsoft 365 home page, click **Security & Compliance**.</span></span>
3. <span data-ttu-id="a2132-111">새 Security & Compliance 탭에서 **권한** > **eDiscovery 매니저** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-111">From the new Security & Compliance tab, click **Permissions** > **eDiscovery Manager**.</span></span>
4. <span data-ttu-id="a2132-112">eDiscovery 매니저의 **편집** 을 클릭한 다음 **eDiscovery 매니저 선택** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-112">Click **Edit** for eDiscovery Manager, and then click **Choose eDiscovery Manager**.</span></span>
5. <span data-ttu-id="a2132-113">**+ 추가** 를 클릭하고 전역 관리자 계정 이름을 검색하고 전역 관리자 계정을 eDiscovery 매니저로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-113">Click **+ Add**, search for your global administrator account name and add your global administrator account as an eDiscovery Manager.</span></span>
6. <span data-ttu-id="a2132-114">**완료** > **저장** > **닫기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-114">Click **Done** > **Save** > **Close**.</span></span>

## <a name="phase-2-add-personally-identifiable-information-to-your-tenant"></a><span data-ttu-id="a2132-115">2단계: 개인 식별이 가능한 정보를 테넌트에 추가</span><span class="sxs-lookup"><span data-stu-id="a2132-115">Phase 2: Add personally identifiable information to your tenant</span></span>

<span data-ttu-id="a2132-116">이 단계에서는 예제 IBAN(국제 은행 계좌 번호) 집합에 대해 PII가 있는 문서를 만들고, Microsoft 365 개발/테스트 환경에서 SharePoint Online 사이트에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-116">In this phase, you create a document with PII for a set of example International Banking Account Numbers (IBANs) and store it on a SharePoint Online site in your Microsoft 365 dev/test environment.</span></span>

1. <span data-ttu-id="a2132-117">로컬 컴퓨터에서 Microsoft Word를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-117">On your local computer, open Microsoft Word.</span></span>
2. <span data-ttu-id="a2132-118">다음 테이블을 Word 파일에 붙여넣고 로컬 컴퓨터에 ‘IBANs.docx’로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-118">Paste the following table in the Word file and save it as 'IBANs.docx' on your local computer.</span></span>

   |<span data-ttu-id="a2132-119">숫자</span><span class="sxs-lookup"><span data-stu-id="a2132-119">Number</span></span>|<span data-ttu-id="a2132-120">국가</span><span class="sxs-lookup"><span data-stu-id="a2132-120">Country</span></span>|<span data-ttu-id="a2132-121">코드</span><span class="sxs-lookup"><span data-stu-id="a2132-121">Code</span></span>|<span data-ttu-id="a2132-122">IBAN</span><span class="sxs-lookup"><span data-stu-id="a2132-122">IBAN</span></span>|
   |---|---|---|---|
   |<span data-ttu-id="a2132-123">1</span><span class="sxs-lookup"><span data-stu-id="a2132-123">1</span></span>|<span data-ttu-id="a2132-124">오스트리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-124">Austria SEPA</span></span>|<span data-ttu-id="a2132-125">AT</span><span class="sxs-lookup"><span data-stu-id="a2132-125">AT</span></span>|<span data-ttu-id="a2132-126">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="a2132-126">AT611904300234573201</span></span>|
   |<span data-ttu-id="a2132-127">2</span><span class="sxs-lookup"><span data-stu-id="a2132-127">2</span></span>|<span data-ttu-id="a2132-128">불가리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-128">Bulgaria SEPA</span></span>|<span data-ttu-id="a2132-129">BG</span><span class="sxs-lookup"><span data-stu-id="a2132-129">BG</span></span>|<span data-ttu-id="a2132-130">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="a2132-130">BG80BNBG96611020345678</span></span>|
   |<span data-ttu-id="a2132-131">3</span><span class="sxs-lookup"><span data-stu-id="a2132-131">3</span></span>|<span data-ttu-id="a2132-132">덴마크 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-132">Denmark SEPA</span></span>|<span data-ttu-id="a2132-133">DK</span><span class="sxs-lookup"><span data-stu-id="a2132-133">DK</span></span>|<span data-ttu-id="a2132-134">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="a2132-134">DK5000400440116243</span></span>|
   |<span data-ttu-id="a2132-135">4</span><span class="sxs-lookup"><span data-stu-id="a2132-135">4</span></span>|<span data-ttu-id="a2132-136">핀란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-136">Finland SEPA</span></span>|<span data-ttu-id="a2132-137">FI</span><span class="sxs-lookup"><span data-stu-id="a2132-137">FI</span></span>|<span data-ttu-id="a2132-138">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="a2132-138">FI2112345600000785</span></span>|
   |<span data-ttu-id="a2132-139">5</span><span class="sxs-lookup"><span data-stu-id="a2132-139">5</span></span>|<span data-ttu-id="a2132-140">프랑스 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-140">France SEPA</span></span>|<span data-ttu-id="a2132-141">FR</span><span class="sxs-lookup"><span data-stu-id="a2132-141">FR</span></span>|<span data-ttu-id="a2132-142">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="a2132-142">FR1420041010050500013M02606</span></span>|
   |<span data-ttu-id="a2132-143">6</span><span class="sxs-lookup"><span data-stu-id="a2132-143">6</span></span>|<span data-ttu-id="a2132-144">독일 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-144">Germany SEPA</span></span>|<span data-ttu-id="a2132-145">DE</span><span class="sxs-lookup"><span data-stu-id="a2132-145">DE</span></span>|<span data-ttu-id="a2132-146">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="a2132-146">DE89370400440532013000</span></span>|
   |<span data-ttu-id="a2132-147">7</span><span class="sxs-lookup"><span data-stu-id="a2132-147">7</span></span>|<span data-ttu-id="a2132-148">그리스 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-148">Greece SEPA</span></span>|<span data-ttu-id="a2132-149">GR</span><span class="sxs-lookup"><span data-stu-id="a2132-149">GR</span></span>|<span data-ttu-id="a2132-150">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="a2132-150">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="a2132-151">8</span><span class="sxs-lookup"><span data-stu-id="a2132-151">8</span></span>|<span data-ttu-id="a2132-152">이탈리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-152">Italy SEPA</span></span>|<span data-ttu-id="a2132-153">IT</span><span class="sxs-lookup"><span data-stu-id="a2132-153">IT</span></span>|<span data-ttu-id="a2132-154">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="a2132-154">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="a2132-155">9</span><span class="sxs-lookup"><span data-stu-id="a2132-155">9</span></span>|<span data-ttu-id="a2132-156">네덜란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-156">Netherlands SEPA</span></span>|<span data-ttu-id="a2132-157">NL</span><span class="sxs-lookup"><span data-stu-id="a2132-157">NL</span></span>|<span data-ttu-id="a2132-158">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="a2132-158">NL91ABNA0417164300</span></span>|
   |<span data-ttu-id="a2132-159">10</span><span class="sxs-lookup"><span data-stu-id="a2132-159">10</span></span>|<span data-ttu-id="a2132-160">폴란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-160">Poland SEPA</span></span>|<span data-ttu-id="a2132-161">PL</span><span class="sxs-lookup"><span data-stu-id="a2132-161">PL</span></span>|<span data-ttu-id="a2132-162">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="a2132-162">PL27114020040000300201355387</span></span>|

   <span data-ttu-id="a2132-163">참고:- 이 샘플 데이터 집합은 공개적으로 사용 가능한 정보에서 얻은 것이며, 테스트 용도로 사용하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-163">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

3. <span data-ttu-id="a2132-164">브라우저의 새 탭에 **https://**\<YourTenantName\>**.sharepoint.com** 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-164">In a new tab of your browser, type:  **https://**\<YourTenantName\>**.sharepoint.com**</span></span>
4. <span data-ttu-id="a2132-p101">**문서** 를 클릭하여 사이트에 대한 문서 라이브러리를 엽니다. 새 목록 환경 둘러보기가 표시되면 완료될 때까지 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p101">Click **Documents** to open the document library for this site. If you're prompted for a new list experience tour, click **Next** until it's finished.</span></span>
5. <span data-ttu-id="a2132-167">**파일** > **업로드** 를 클릭하고 2단계에서 만든 IBANs.docx를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-167">Click **Upload** > **Files** and select the IBANs.docx you created in step 2.</span></span>

## <a name="phase-3-demonstrate-data-discovery"></a><span data-ttu-id="a2132-168">3단계: 데이터 검색 설명</span><span class="sxs-lookup"><span data-stu-id="a2132-168">Phase 3: Demonstrate data discovery</span></span>

<span data-ttu-id="a2132-169">이 단계에서는 IBAN이 포함된 콘텐츠를 기반으로 2단계에서 만들어지고 저장된 문서를 찾을 수 있는 검색 기능을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-169">In this phase, you demonstrate search to find the document created and stored in Phase 2, based on its content containing IBANs.</span></span>

1. <span data-ttu-id="a2132-170">Security & Compliance 탭에서 **홈** 을 클릭한 다음 **검색 및 확인** > **콘텐츠 검색** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-170">From the Security & Compliance tab, click **Home**, and then click **Search & investigation** > **Content search**.</span></span>
2. <span data-ttu-id="a2132-171">**+** 를 클릭하여 새 검색 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-171">Create a new search item by clicking on **+**.</span></span>
3. <span data-ttu-id="a2132-172">새 창에서 다음 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-172">In a new window, provide the following information: a.</span></span> <span data-ttu-id="a2132-173">이름: IBAN 검색 b</span><span class="sxs-lookup"><span data-stu-id="a2132-173">Name: IBAN Search b.</span></span> <span data-ttu-id="a2132-174">검색 대상: **검색할 특정 사이트를 선택**(**+** 클릭)하고 사이트의 URL을 입력합니다. **https://**\<YourTenantName\>**.sharepoint.com/** c.</span><span class="sxs-lookup"><span data-stu-id="a2132-174">Where do you want us to look?: **Choose specific sites to search** (click **+**), and then enter the site's URL: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span></span> <span data-ttu-id="a2132-175">**추가** 를 클릭한 다음 **OK** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-175">Click **Add**, and then click **OK**.</span></span> <span data-ttu-id="a2132-176">경고가 표시되면 **OK** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-176">If you see a Warning, click **OK**.</span></span>
    <span data-ttu-id="a2132-177">d.</span><span class="sxs-lookup"><span data-stu-id="a2132-177">d.</span></span> <span data-ttu-id="a2132-178">**새로 검색** 창에서 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-178">Click **Next** on a **New search** window.</span></span>
    <span data-ttu-id="a2132-179">e.</span><span class="sxs-lookup"><span data-stu-id="a2132-179">e.</span></span> <span data-ttu-id="a2132-180">**검색 대상**: **SensitiveType:"IBAN(국제 은행 계좌 번호)"** 와 **검색** 을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-180">For **What do you want us to look for?**: **SensitiveType:"International Banking Account Number (IBAN)"**, and then click **Search**.</span></span>

4. <span data-ttu-id="a2132-181">**IBAN 검색** 결과에 나열된 항목이 하나 이상 표시되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-181">Make sure you see at least one item listed in the **IBAN Search** results.</span></span>

## <a name="phase-4-create-a-custom-sensitive-information-type-via-powershell"></a><span data-ttu-id="a2132-182">4단계: PowerShell을 통해 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="a2132-182">Phase 4: Create a custom sensitive information type via PowerShell</span></span>

<span data-ttu-id="a2132-p103">이 단계에서는 Microsoft PowerShell Contoso를 사용하여 가상 Contoso Corporation에 대해 사용자 지정 중요한 정보 형식을 만듭니다. Contoso는 Contoso 사용자 지정 숫자(CCN)를 사용하여 고객 데이터베이스에서 각 고객을 식별합니다. CCN은 다음 구조로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p103">In this phase, you create a custom sensitive information type for the fictional Contoso Corporation using Microsoft PowerShell.  Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following structure:</span></span>

- <span data-ttu-id="a2132-186">레코드가 만들어진 연도를 나타내는 두 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-186">Two digits to represent the year that the record was created.</span></span>
  - <span data-ttu-id="a2132-187">Contoso는 2002년에 설립되었습니다. 따라서 가능한 가장 빠른 값은 02입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-187">Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span>
- <span data-ttu-id="a2132-188">레코드를 만든 파트너 에이전시를 나타내는 세 자리 숫자.</span><span class="sxs-lookup"><span data-stu-id="a2132-188">Three digits to represent the partner agency that created the record.</span></span>
  - <span data-ttu-id="a2132-189">가능한 에이전시 값 범위는 000에서 999입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-189">Possible agency values range from 000 to 999.</span></span>
- <span data-ttu-id="a2132-190">비즈니스 분야를 나타내는 알파벳 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-190">An alphabetic character to represent the line of business.</span></span>
  - <span data-ttu-id="a2132-191">가능한 값은 a-z이고 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-191">Possible values are a-z and should be case insensitive.</span></span>
- <span data-ttu-id="a2132-192">4자리 일련 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-192">A four-digit serial number.</span></span>
  - <span data-ttu-id="a2132-193">가능한 일련 번호 값의 범위는 0000에서 9999까지입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-193">Possible serial number values range from 0000 to 9999.</span></span>

<span data-ttu-id="a2132-p104">Contoso는 내부 서신, 외부 서신, 문서 및 기타 양식에서 항상 CCN을 사용하여 고객을 참조합니다. Microsoft 365 콘텐츠에서는 사용자 지정 중요한 항목 유형을 만들어 CCN의 사용을 감지할 수 있으므로 이러한 형식의 개인 식별 가능한 정보를 사용할 때 보호 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p104">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, and other forms. Contoso needs a custom sensitive item type to detect the use of CCNs in Microsoft 365 content so that they may apply protection to the use of this form of personal identifiable information.</span></span>

1. <span data-ttu-id="a2132-196">[보안 및 준수 센터 PowerShell](/powershell/exchange/connect-to-scc-powershell)에 연결의 MFA(다단계 인증) 연결 지침을 사용하고 글로벌 관리자 계정의 UPN을 사용하여 보안 및 준수 센터에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-196">Use the multi-factor authentication (MFA) connection instructions in [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and connect to the Security & Compliance Center with UPN of your global administrator account.</span></span>

2. <span data-ttu-id="a2132-197">다음 PowerShell 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-197">Run the following PowerShell commands.</span></span>

   ```powershell
   #Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName#Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName
   ```

3. <span data-ttu-id="a2132-198">다음 PowerShell 명령을 실행하고 만들어진 GUID를 컴퓨터의 열린 메모장 인스턴스에 나열된 순서대로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-198">Run the following PowerShell commands and copy the generated GUIDs to an open instance of Notepad on your computer in the order in which they are listed.</span></span>

   ```powershell
   #Generate three unique GUIDs
   Write-Host "GUID1 = "([guid]::NewGuid().Guid)
   Write-Host "GUID2 = "([guid]::NewGuid().Guid)
   Write-Host "GUID3 = "([guid]::NewGuid().Guid)
   ```

4. <span data-ttu-id="a2132-199">로컬 컴퓨터에서 메모장의 다른 인스턴스를 열고 다음 콘텐츠를 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-199">On your local computer, open another instance of Notepad and paste in the following content:</span></span>

   ```text
   <?xml version="1.0" encoding="utf-8"?>
   <RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
   <RulePack id="GUID1">
   <Version major="1" minor="0" build="0" revision="0" />
   <Publisher id="GUID2" />
   <Details defaultLangCode="en">
   <LocalizedDetails langcode="en">
   <PublisherName>Contoso Ltd.</PublisherName>
   <Name>Contoso Rule Package</Name>
   <Description>Defines Contoso's custom set of classification rules</Description>
   </LocalizedDetails>
   </Details>
   </RulePack>
   <Rules>
   <!-- Contoso Customer Number (CCN) -->
   <Entity id="GUID3" patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
   <IdMatch idRef="Regex_contoso_ccn" />
   <Match idRef="Keyword_contoso_ccn" />
   <Match idRef="Regex_eu_date" />
   </Pattern>
   </Entity>
   <Regex id="Regex_contoso_ccn">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</Regex>
   <Keyword id="Keyword_contoso_ccn">
   <Group matchStyle="word">
   <Term caseSensitive="false">customer number</Term>
   <Term caseSensitive="false">customer no</Term>
   <Term caseSensitive="false">customer #</Term>
   <Term caseSensitive="false">customer#</Term>
   <Term caseSensitive="false">Contoso customer</Term>
   </Group>
   </Keyword>
   <Regex id="Regex_eu_date"> (0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)? |feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|apr(ile|il)?|abr(il)?|avril |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)? |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}</Regex>
   <LocalizedStrings>
   <Resource idRef="GUID3">
   <Name default="true" langcode="en-us">Contoso Customer Number (CCN)</Name>
   <Description default="true" langcode="en-us">Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</Description>
   </Resource>
   </LocalizedStrings>
   </Rules>
   </RulePackage>
   ```

5. <span data-ttu-id="a2132-200">4단계의 XML 텍스트에 있는 GUID1, GUID2, GUID3 값을 3단계의 값으로 바꾼 다음 ContosoCCN.xml이라는 이름으로 로컬 컴퓨터의 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-200">Replace the values of GUID1, GUID2, and GUID3 in the XML text of step 4 with their values from step 3, and then save the contents on your local computer with the name ContosoCCN.xml.</span></span>

6. <span data-ttu-id="a2132-201">ContosoCCN.xml 파일에 경로를 채우고 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-201">Fill in the path to your ContosoCCN.xml file and run the following commands.</span></span>

   ```powershell
   #Create new Sensitive Information Type
   $path="<path to the ContosoCCN.xml file, such as C:\Scripts\ContosoCCN.xml>"
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path $path -Encoding Byte -ReadCount 0)
   ```

7. <span data-ttu-id="a2132-p105">Security & Compliance 탭에서 **분류** > **중요한 정보 유형** 을 클릭합니다. 목록에서 Contoso 사용자 지정 숫자(CCN)를 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p105">From the Security & Compliance tab, click **Classifications** > **Sensitive information types**. You should see the Contoso Customer Number (CCN) in the list.</span></span>

## <a name="phase-5-demonstrate-data-protection"></a><span data-ttu-id="a2132-204">5단계: 데이터 보호 설명</span><span class="sxs-lookup"><span data-stu-id="a2132-204">Phase 5: Demonstrate data protection</span></span>

<span data-ttu-id="a2132-205">Microsoft 365의 개인 정보 보호에는 DLP(데이터 손실 방지) 기능이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-205">Protection of personal information in Microsoft 365 includes using data loss prevention (DLP) capabilities.</span></span>  <span data-ttu-id="a2132-206">DLP 정책을 사용하여 Microsoft 365에서 중요한 정보를 자동으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-206">With DLP policies, you can automatically protect sensitive information across Microsoft 365.</span></span>

<span data-ttu-id="a2132-p107">보호를 적용할 수 있는 여러 가지 방법이 있습니다. EU 상주 데이터가 사용자 환경에 저장되고 직원이 처리하도록 허용된 방법에 대한 인식을 개선하고 교육하는 것은 Office 365 DLP를 사용하는 한 수준의 정보 보호를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p107">There are multiple ways you can apply the protection. Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Office 365 DLP.</span></span>

<span data-ttu-id="a2132-209">이 단계에서는 새 DLP 정책을 만들고 2단계에서 SharePoint Online에 저장된 IBANs.docx 파일에 적용되는 방법과 IBAN을 포함하는 전자 메일을 보내려고 시도하는 경우에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-209">In this phase, you create a new DLP policy and demonstrate how it gets applied to the IBANs.docx file you stored in SharePoint Online in Phase 2 and when you attempt to send an email containing IBANs.</span></span>

1. <span data-ttu-id="a2132-210">브라우저의 Security & Compliance 탭에서 **홈** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-210">From the Security & Compliance tab of your browser, click **Home**.</span></span>
2. <span data-ttu-id="a2132-211">**데이터 손실 방지** > **정책** 을 클릭합니다</span><span class="sxs-lookup"><span data-stu-id="a2132-211">Click **Data loss prevention** > **Policy**.</span></span>
3. <span data-ttu-id="a2132-212">**+ 정책 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-212">Click **+ Create a policy**.</span></span>
4. <span data-ttu-id="a2132-213">**템플릿으로 시작하거나 사용자 지정 정책 만들기** 에서 **사용자 지정** > **사용자 지정** > **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-213">In **Start with a template or create a custom policy**, click **Custom** > **Custom policy** > **Next**.</span></span>
5. <span data-ttu-id="a2132-p108">**정책 이름 지정** 에서 다음 세부 정보를 제공하고 **다음** 을 클릭합니다. a. 이름: **EU 시민 PII 정책** b. 설명: **유럽 시민의 개인 식별이 가능한 정보 보호**</span><span class="sxs-lookup"><span data-stu-id="a2132-p108">In **Name your policy**, provide the following details and then click **Next**:  a. Name: **EU Citizen PII Policy** b. Description: **Protect the personally identifiable information of European citizens**</span></span>
6. <span data-ttu-id="a2132-p109">**위치 선택** 에서 **Microsoft 365의 모든 위치** 를 선택합니다. 여기에는 Exchange 전자 메일, OneDrive, SharePoint 문서의 콘텐츠가 포함됩니다. 그리고 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p109">In **Choose locations**, select **All locations in Microsoft 365**. This will include content in Exchange email and OneDrive and SharePoint documents. And then click **Next**.</span></span>
7. <span data-ttu-id="a2132-220">**보호하려는 콘텐츠의 유형 사용자 지정** 에서 **다음이 포함된 콘텐츠 찾기:** 를 클릭한 다음 **편집** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-220">In **Customize the type of content you want to protect**, click **Find content that contains:** and then click **Edit**.</span></span>
8. <span data-ttu-id="a2132-221">**보호할 콘텐츠 유형 선택** 에서 **추가** > **중요한 정보 유형** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-221">In **Choose the types of content to protect**, click **Add** > **Sensitive info types**.</span></span>
9. <span data-ttu-id="a2132-222">**중요한 정보 유형** 에서 **+ 추가** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-222">In **Sensitive info types**, click **+ Add**.</span></span>
10. <span data-ttu-id="a2132-223">**중요한 정보 유형** 에서 **IBAN** 을 검색하고 **IBAN(국제 은행 계좌 번호)** 의 확인란을 선택한 다음 **추가** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-223">In **Sensitive info types**, search for **IBAN**, select the check box for **International Banking Account Number (IBAN)**, and then click **Add**.</span></span>
11. <span data-ttu-id="a2132-224">**IBAN(국제 은행 계좌 번호)** 중요한 정보 유형이 추가되었는지 확인한 다음 **완료** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-224">Confirm that the **International Banking Account Number (IBAN)** sensitive information type was added, and then click **Done**.</span></span>
12. <span data-ttu-id="a2132-225">**콘텐츠 포함** 에서 중요한 정보 유형이 추가되었는지 확인한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-225">In **Content contains**, confirm that the sensitive information types were added and then click **Save**.</span></span>
13. <span data-ttu-id="a2132-226">**보호할 콘텐츠 유형 사용자 지정** 에서 **포함된 콘텐츠 찾기** 에 **IBAN(국제 은행 계좌 번호)** 을 포함하고 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-226">In **Customize the type of content you want to protect**, confirm  **Find content that contains:** contains the **International Banking Account Number (IBAN)**, and then click **Next**.</span></span>
14. <span data-ttu-id="a2132-227">**다음이 공유되는 콘텐츠에 포함된 경우 검색** 에서 값을 **10** 에서 **1** 로 변경하고 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-227">In **Detect when content that's being shared contains:**, change the value from **10** to **1**, and then click **Next**.</span></span>
15. <span data-ttu-id="a2132-228">**정책을 켜거나 먼저 테스트를 수행하시겠습니까?** 에서 다음 설정을 선택하고 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-228">In **Do you want to turn on the policy or test things out first?**, choose the following settings, and then click **Next**.</span></span>
    <span data-ttu-id="a2132-229">a.</span><span class="sxs-lookup"><span data-stu-id="a2132-229">a.</span></span> <span data-ttu-id="a2132-230">**먼저 테스트 수행** 에 대한 옵션을 선택합니다 b.</span><span class="sxs-lookup"><span data-stu-id="a2132-230">Select the option for **I'd like to test it out first** b.</span></span> <span data-ttu-id="a2132-231">**테스트 모드인 경우 정책 팁 표시** 에 대한 확인란 선택</span><span class="sxs-lookup"><span data-stu-id="a2132-231">Select the check box for **Show policy tips while in test mode**</span></span>
16. <span data-ttu-id="a2132-p111">**설정 검토** 에서 설정을 검토한 후 **만들기** 를 클릭합니다. 참고: 새 DLP 정책을 만든 후 적용되려면 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p111">In **Review your settings**, click **Create** after reviewing the settings. NOTE: After you create a new DLP policy, it will take a while for it to take effect.</span></span>
17. <span data-ttu-id="a2132-234">로컬 컴퓨터에서 브라우저의 개인 인스턴스를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-234">On your local computer, open a private instance of your browser.</span></span>
18. <span data-ttu-id="a2132-235">주소 표시줄에 **https://**\<YourTenantName\>**.sharepoint.com** 을 입력하고 전역 관리자 계정을 사용하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-235">In the address bar, type **https://**\<YourTenantName\>**.sharepoint.com** and sign in using your global administrator account.</span></span>
19. <span data-ttu-id="a2132-236">**문서** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-236">Click **Documents**.</span></span>
20. <span data-ttu-id="a2132-p112">‘IBANs.docx’라는 파일을 클릭합니다. ‘IBANs.docx의 정책 팁’이 표시되어야 합니다. IBANs.docx 파일은 외부 수신자와 공유되어 DLP 정책을 위반했습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p112">Click the file named 'IBANs.docx'. You should see 'Policy tip for IBANs.docx'.  The IBANs.docx file was shared with external recipients, which violates the DLP policy.</span></span>
21. <span data-ttu-id="a2132-240">주소 표시줄에 `https://outlook.office365.com`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-240">In the address bar, type: `https://outlook.office365.com`</span></span>
22. <span data-ttu-id="a2132-241">**새로 만들기** - **전자 메일 메시지** 를 클릭하고 다음을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-241">Click **New** - **Email message** and provide the following:</span></span>

    - <span data-ttu-id="a2132-242">**받는 사람:** \<a personal email address\></span><span class="sxs-lookup"><span data-stu-id="a2132-242">**To:** \<a personal email address\></span></span>
    - <span data-ttu-id="a2132-243">**제목:** GDPR 테스트</span><span class="sxs-lookup"><span data-stu-id="a2132-243">**Subject:** GDPR Test</span></span>
    - <span data-ttu-id="a2132-244">**본문:** 아래 표시된 값의 테이블에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-244">**Body:** Copy in the table of values shown below.</span></span>

      |<span data-ttu-id="a2132-245">숫자</span><span class="sxs-lookup"><span data-stu-id="a2132-245">Number</span></span>|<span data-ttu-id="a2132-246">국가</span><span class="sxs-lookup"><span data-stu-id="a2132-246">Country</span></span>|<span data-ttu-id="a2132-247">코드</span><span class="sxs-lookup"><span data-stu-id="a2132-247">Code</span></span>|<span data-ttu-id="a2132-248">IBAN</span><span class="sxs-lookup"><span data-stu-id="a2132-248">IBAN</span></span>|
      |---|---|---|---|
      |<span data-ttu-id="a2132-249">1</span><span class="sxs-lookup"><span data-stu-id="a2132-249">1</span></span>|<span data-ttu-id="a2132-250">오스트리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-250">Austria SEPA</span></span>|<span data-ttu-id="a2132-251">AT</span><span class="sxs-lookup"><span data-stu-id="a2132-251">AT</span></span>|<span data-ttu-id="a2132-252">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="a2132-252">AT611904300234573201</span></span>|
      |<span data-ttu-id="a2132-253">2</span><span class="sxs-lookup"><span data-stu-id="a2132-253">2</span></span>|<span data-ttu-id="a2132-254">불가리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-254">Bulgaria SEPA</span></span>|<span data-ttu-id="a2132-255">BG</span><span class="sxs-lookup"><span data-stu-id="a2132-255">BG</span></span>|<span data-ttu-id="a2132-256">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="a2132-256">BG80BNBG96611020345678</span></span>|
      |<span data-ttu-id="a2132-257">3</span><span class="sxs-lookup"><span data-stu-id="a2132-257">3</span></span>|<span data-ttu-id="a2132-258">덴마크 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-258">Denmark SEPA</span></span>|<span data-ttu-id="a2132-259">DK</span><span class="sxs-lookup"><span data-stu-id="a2132-259">DK</span></span>|<span data-ttu-id="a2132-260">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="a2132-260">DK5000400440116243</span></span>|
      |<span data-ttu-id="a2132-261">4</span><span class="sxs-lookup"><span data-stu-id="a2132-261">4</span></span>|<span data-ttu-id="a2132-262">핀란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-262">Finland SEPA</span></span>|<span data-ttu-id="a2132-263">FI</span><span class="sxs-lookup"><span data-stu-id="a2132-263">FI</span></span>|<span data-ttu-id="a2132-264">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="a2132-264">FI2112345600000785</span></span>|
      |<span data-ttu-id="a2132-265">5</span><span class="sxs-lookup"><span data-stu-id="a2132-265">5</span></span>|<span data-ttu-id="a2132-266">프랑스 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-266">France SEPA</span></span>|<span data-ttu-id="a2132-267">FR</span><span class="sxs-lookup"><span data-stu-id="a2132-267">FR</span></span>|<span data-ttu-id="a2132-268">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="a2132-268">FR1420041010050500013M02606</span></span>|
      |<span data-ttu-id="a2132-269">6</span><span class="sxs-lookup"><span data-stu-id="a2132-269">6</span></span>|<span data-ttu-id="a2132-270">독일 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-270">Germany SEPA</span></span>|<span data-ttu-id="a2132-271">DE</span><span class="sxs-lookup"><span data-stu-id="a2132-271">DE</span></span>|<span data-ttu-id="a2132-272">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="a2132-272">DE89370400440532013000</span></span>|
      |<span data-ttu-id="a2132-273">7</span><span class="sxs-lookup"><span data-stu-id="a2132-273">7</span></span>|<span data-ttu-id="a2132-274">그리스 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-274">Greece SEPA</span></span>|<span data-ttu-id="a2132-275">GR</span><span class="sxs-lookup"><span data-stu-id="a2132-275">GR</span></span>|<span data-ttu-id="a2132-276">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="a2132-276">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="a2132-277">8</span><span class="sxs-lookup"><span data-stu-id="a2132-277">8</span></span>|<span data-ttu-id="a2132-278">이탈리아 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-278">Italy SEPA</span></span>|<span data-ttu-id="a2132-279">IT</span><span class="sxs-lookup"><span data-stu-id="a2132-279">IT</span></span>|<span data-ttu-id="a2132-280">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="a2132-280">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="a2132-281">9</span><span class="sxs-lookup"><span data-stu-id="a2132-281">9</span></span>|<span data-ttu-id="a2132-282">네덜란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-282">Netherlands SEPA</span></span>|<span data-ttu-id="a2132-283">NL</span><span class="sxs-lookup"><span data-stu-id="a2132-283">NL</span></span>|<span data-ttu-id="a2132-284">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="a2132-284">NL91ABNA0417164300</span></span>|
      |<span data-ttu-id="a2132-285">10</span><span class="sxs-lookup"><span data-stu-id="a2132-285">10</span></span>|<span data-ttu-id="a2132-286">폴란드 SEPA</span><span class="sxs-lookup"><span data-stu-id="a2132-286">Poland SEPA</span></span>|<span data-ttu-id="a2132-287">PL</span><span class="sxs-lookup"><span data-stu-id="a2132-287">PL</span></span>|<span data-ttu-id="a2132-288">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="a2132-288">PL27114020040000300201355387</span></span>|
      |

    <span data-ttu-id="a2132-289">참고:- 이 샘플 데이터 집합은 공개적으로 사용 가능한 정보에서 얻은 것이며, 테스트 용도로 사용하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-289">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

23. <span data-ttu-id="a2132-290">DLP 정책은 전자 메일의 본문에 IBAN이 포함되어 있음을 인식하고 메시지 창 상단에 정책 팁을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-290">You will see that the DLP policy recognized that body of the email contains IBANs and provides you with the policy tip at the top of the message window.</span></span>
24. <span data-ttu-id="a2132-291">브라우저의 개인 인스턴스를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-291">Close the private instance of your browser.</span></span>

## <a name="phase-6-demonstrate-reporting"></a><span data-ttu-id="a2132-292">6단계: 보고 설명</span><span class="sxs-lookup"><span data-stu-id="a2132-292">Phase 6: Demonstrate reporting</span></span>

<span data-ttu-id="a2132-293">이 단계에서는 5단계에서 구성된 DLP 정책에 따라 Microsoft 365 보고에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-293">In this phase, you demonstrate Microsoft 365 reporting based on the DLP policy configured in Phase 5.</span></span>

   1. <span data-ttu-id="a2132-294">브라우저의 Security & Compliance 탭에서 **홈** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-294">From the Security & Compliance tab of your browser, click **Home**.</span></span>
   2. <span data-ttu-id="a2132-295">**보고서** > **대시보드** > **DLP 정책 일치** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-295">Click **Reports** > **Dashboard** > **DLP policy matches**.</span></span>
   3. <span data-ttu-id="a2132-p113">DLP 정책은 조직의 중요한 정보를 식별하고 보호하는 데 도움이 됩니다. 예를 들어, 보고서에서 SharePoint Online에 저장된 IBAN을 포함하는 문서를 정책에서 식별했음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2132-p113">Your DLP policy helps identify and protect organization's sensitive information. For example, in the report you will see that the policy identified the document that contains IBANs stored in SharePoint Online.</span></span>
