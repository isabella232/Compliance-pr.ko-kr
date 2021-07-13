---
title: FIPS(Federal Information Processing Standard) 게시 140-2
description: Microsoft는 암호화 모듈이 미국 연방 정보 처리 표준을 준수하는지 인증합니다.
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
ms.openlocfilehash: 2c51979122aaedda90bac74740e95c9d1265de74
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385008"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a><span data-ttu-id="cbf8b-104">FIPS(Federal Information Processing Standard) 게시 140-2</span><span class="sxs-lookup"><span data-stu-id="cbf8b-104">Federal Information Processing Standard (FIPS) Publication 140-2</span></span>

## <a name="fips-140-2-standard-overview"></a><span data-ttu-id="cbf8b-105">FIPS 140-2 표준 개요</span><span class="sxs-lookup"><span data-stu-id="cbf8b-105">FIPS 140-2 standard overview</span></span>

<span data-ttu-id="cbf8b-106">FIPS(Federal Information Processing Standard) 발행물 140-2는 1996년 정보 기술 관리 재구성법의 5131조에 정의된 정보 기술 제품에서 암호화 모듈에 대한 최소 보안 요구 사항을 정의하는 미국 정부 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-106">The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.</span></span>

<span data-ttu-id="cbf8b-107">미국 [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) NIST(National Institute of Standards and Technology) 및 CCCS(Canadian Institute for Cyber Security)의 공동 노력인 CMVP(암호화 모듈 유효성  검사 프로그램)는 암호화 모듈의 보안 요구 사항(예: FIPS 140-2) 및 관련 FIPS 암호화 표준에 대한 암호화 모듈의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-107">The [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), a joint effort of the U.S. National Institute of Standards and Technology (NIST) and the Canadian Centre for Cyber Security (CCCS), validates cryptographic modules to the *Security Requirements for Cryptographic Modules* standard (i.e., FIPS 140-2) and related FIPS cryptography standards.</span></span> <span data-ttu-id="cbf8b-108">FIPS 140-2 보안 요구 사항에는 암호화 모듈의 디자인 및 구현과 관련된 11개 영역이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-108">The FIPS 140-2 security requirements cover 11 areas related to the design and implementation of a cryptographic module.</span></span> <span data-ttu-id="cbf8b-109">NIST 정보 기술 실험실은 모듈에서 FIPS 승인 암호화 알고리즘의 유효성을 검사하는 관련 프로그램을 운영합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-109">The NIST Information Technology Laboratory operates a related program that validates the FIPS approved cryptographic algorithms in the module.</span></span>

## <a name="microsofts-approach-to-fips-140-2-validation"></a><span data-ttu-id="cbf8b-110">FIPS 140-2 유효성 검사에 대한 Microsoft의 접근 방식</span><span class="sxs-lookup"><span data-stu-id="cbf8b-110">Microsoft's approach to FIPS 140-2 validation</span></span>

<span data-ttu-id="cbf8b-111">Microsoft는 2001년 표준이 시작된 이후 암호화 모듈의 유효성을 검사하여 140-2 요구 사항을 충족하기 위한 적극적인 약속을 유지하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-111">Microsoft maintains an active commitment to meeting the 140-2 requirements, having validated cryptographic modules since the standard's inception in 2001.</span></span> <span data-ttu-id="cbf8b-112">Microsoft는 NIST(National Institute of Standards and Technology) CMVP(암호화 모듈 유효성 검사 [프로그램)에서](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) 암호화 모듈의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-112">Microsoft validates its cryptographic modules under the National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP).</span></span> <span data-ttu-id="cbf8b-113">많은 클라우드 서비스를 포함한 여러 Microsoft 제품은 이러한 암호화 모듈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-113">Multiple Microsoft products, including many cloud services, use these cryptographic modules.</span></span>

<span data-ttu-id="cbf8b-114">Microsoft Windows 모듈, 각 모듈에 대한 보안 정책 및 CMVP 인증서 세부 정보 카탈로그에 대한 기술 정보는 Windows 및 Windows [Server FIPS 140-2](https://aka.ms/AA6ehud)콘텐츠를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-114">For technical information on Microsoft Windows cryptographic modules, the security policy for each module, and the catalog of CMVP certificate details, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="cbf8b-115">Microsoft 범위 내 클라우드 플랫폼 & 서비스</span><span class="sxs-lookup"><span data-stu-id="cbf8b-115">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="cbf8b-116">현재 CMVP FIPS 140-2 구현 지침에서는 클라우드 서비스 자체에 대한 FIPS 140-2 유효성 검사를 제외합니다. 클라우드 서비스 공급자는 클라우드 서비스를 구성하는 컴퓨팅 요소에 대해 FIPS 140 유효성이 검사된 암호화 모듈을 획득하고 작동하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-116">While the current CMVP FIPS 140-2 implementation guidance precludes a FIPS 140-2 validation for a cloud service itself; cloud service providers can choose to obtain and operate FIPS 140 validated cryptographic modules for the computing elements that comprise their cloud service.</span></span> <span data-ttu-id="cbf8b-117">FIPS 140-2 유효성이 검사된 구성 요소가 포함된 Microsoft 온라인 서비스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-117">Microsoft online services that include components, which have been FIPS 140-2 validated include, among others:</span></span>

- <span data-ttu-id="cbf8b-118">Azure 및 Azure Government</span><span class="sxs-lookup"><span data-stu-id="cbf8b-118">Azure and Azure Government</span></span>
- <span data-ttu-id="cbf8b-119">Dynamics 365 및 Dynamics 365 Government</span><span class="sxs-lookup"><span data-stu-id="cbf8b-119">Dynamics 365 and Dynamics 365 Government</span></span>
- <span data-ttu-id="cbf8b-120">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="cbf8b-120">Office 365, Office 365 U.S. Government, and Office 365 U.S. Government Defense</span></span>

## <a name="azure-dynamics-365-and-fips-140-2"></a><span data-ttu-id="cbf8b-121">Azure, Dynamics 365 및 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="cbf8b-121">Azure, Dynamics 365, and FIPS 140-2</span></span>

<span data-ttu-id="cbf8b-122">Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure FIPS 140-2 제공을 참조하세요.](/azure/compliance/offerings/offering-fips-140-2)</span><span class="sxs-lookup"><span data-stu-id="cbf8b-122">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure FIPS 140-2 offering](/azure/compliance/offerings/offering-fips-140-2).</span></span>

## <a name="office-365-and-fips-140-2"></a><span data-ttu-id="cbf8b-123">Office 365 및 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="cbf8b-123">Office 365 and FIPS 140-2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="cbf8b-124">Office 365 클라우드 환경</span><span class="sxs-lookup"><span data-stu-id="cbf8b-124">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="cbf8b-125">Office 365 및 범위 내 서비스</span><span class="sxs-lookup"><span data-stu-id="cbf8b-125">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="cbf8b-126">다음 표를 사용하여 서비스 및 구독에 Office 365 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-126">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="cbf8b-127">**적용 가능 여부**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-127">**Applicability**</span></span> | <span data-ttu-id="cbf8b-128">**범위 내 서비스**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-128">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="cbf8b-129">Office 365, GCC, GCC High, DoD</span><span class="sxs-lookup"><span data-stu-id="cbf8b-129">Office 365, GCC, GCC High, DoD</span></span> | <span data-ttu-id="cbf8b-130">[FIPS 140-2 유효성 검사 참조](/windows/security/threat-protection/fips-140-validation)</span><span class="sxs-lookup"><span data-stu-id="cbf8b-130">See [FIPS 140-2 Validation](/windows/security/threat-protection/fips-140-validation)</span></span> |

### <a name="frequently-asked-questions"></a><span data-ttu-id="cbf8b-131">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="cbf8b-131">Frequently asked questions</span></span>

<span data-ttu-id="cbf8b-132">**'FIPS 140 유효성 검사' 및 'FIPS 140 호환'의 차이점은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-132">**What is the difference between 'FIPS 140 Validated' and 'FIPS 140 compliant'?**</span></span>

<span data-ttu-id="cbf8b-133">'FIPS 140 Validated'는 암호화 모듈 또는 모듈을 추가하는 제품이 FIPS 140-2 요구 사항을 충족하는 것으로 CMVP에 의해 유효성을 검사('인증')했다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-133">'FIPS 140 Validated' means that the cryptographic module, or a product that embeds the module has been validated ('certified') by the CMVP as meeting the FIPS 140-2 requirements.</span></span> <span data-ttu-id="cbf8b-134">'FIPS 140 호환'은 암호화 기능에 FIPS 140 유효성 검사 제품을 사용 하는 IT 제품에 대한 업계 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-134">'FIPS 140 compliant' is an industry term for IT products that rely on FIPS 140 Validated products for cryptographic functionality.</span></span>

<span data-ttu-id="cbf8b-135">**Microsoft는 언제 FIPS 140 유효성 검사를 진행하나요?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-135">**When does Microsoft undertake a FIPS 140 validation?**</span></span>

<span data-ttu-id="cbf8b-136">모듈 유효성 검사를 시작하는 케이던스가 Windows 10 서버의 기능 Windows 정렬됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-136">The cadence for starting a module validation aligns with the feature updates of Windows 10 and Windows Server.</span></span> <span data-ttu-id="cbf8b-137">소프트웨어 산업이 발전함에 따라 운영 체제가 월별 소프트웨어 업데이트와 함께 더 자주 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-137">As the software industry evolved, operating systems are released more frequently, with monthly software updates.</span></span> <span data-ttu-id="cbf8b-138">Microsoft는 기능 릴리스에 대한 유효성 검사를 진행하지만 릴리스 사이에는 암호화 모듈의 변경 내용을 최소화하기 위해 노력합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-138">Microsoft undertakes validation for feature releases, but in between releases, seeks to minimize the changes to the cryptographic modules.</span></span>

<span data-ttu-id="cbf8b-139">**FIPS 140 유효성 검사에 포함되는 컴퓨터는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-139">**Which computers are included in a FIPS 140 validation?**</span></span>

<span data-ttu-id="cbf8b-140">Microsoft는 Windows 10 및 Windows 실행되는 하드웨어 구성의 대표 샘플에서 암호화 모듈의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-140">Microsoft validates cryptographic modules on a representative sample of hardware configurations running Windows 10 and Windows Server.</span></span> <span data-ttu-id="cbf8b-141">일반적으로 환경에서 하드웨어를 사용하는 경우 유효성 검사 프로세스에 사용되는 샘플과 유사한 이 FIPS 140-2 유효성 검사를 수락하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-141">It is common industry practice to accept this FIPS 140-2 validation when an environment uses hardware, which is similar to the samples used for the validation process.</span></span>

<span data-ttu-id="cbf8b-142">**NIST 웹 사이트에는 여러 모듈이 나열되어 있습니다. 기관에 어떤 것이 적용되는지 어떻게 알 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-142">**There are many modules listed on the NIST website. How do I know which one applies to my agency?**</span></span>

<span data-ttu-id="cbf8b-143">FIPS 140-2를 통해 유효성이 검사된 암호화 모듈을 사용하려면 사용하는 버전이 유효성 검사 목록에 나타나는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-143">If you are required to use cryptographic modules validated through FIPS 140-2, you need to verify that the version you use appears on the validation list.</span></span> <span data-ttu-id="cbf8b-144">CMVP 및 Microsoft는 제품 릴리스별로 구성되는 유효성이 검사된 암호화 모듈 목록을 유지 관리하며, Windows 시스템에 설치되는 모듈을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-144">The CMVP and Microsoft maintain a list of validated cryptographic modules, organized by product release, along with instructions for identifying which modules are installed on a Windows system.</span></span> <span data-ttu-id="cbf8b-145">규격으로 시스템을 구성하는 데 대한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)</span><span class="sxs-lookup"><span data-stu-id="cbf8b-145">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="cbf8b-146">**인증서에 대한 'FIPS 모드에서 작동하는 경우'는 무엇을 의미하나요?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-146">**What does 'When operated in FIPS mode' mean on a certificate?**</span></span>

<span data-ttu-id="cbf8b-147">이 주의는 FIPS 140-2 보안 정책과 일관된 방식으로 암호화 모듈을 사용하기 위해 필요한 구성 및 보안 규칙을 따라야 하다는 경고를 독자에게 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-147">This caveat informs the reader that required configuration and security rules must be followed to use the cryptographic module in a way that is consistent with its FIPS 140-2 security policy.</span></span> <span data-ttu-id="cbf8b-148">각 모듈에는 자체 보안 정책(작동할 보안 규칙의 정확한 사양)이 있으며 승인된 암호화 알고리즘, 암호화 키 관리 및 인증 기술을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-148">Each module has its own security policy — a precise specification of the security rules under which it will operate — and employs approved cryptographic algorithms, cryptographic key management, and authentication techniques.</span></span> <span data-ttu-id="cbf8b-149">보안 규칙은 각 모듈에 대한 보안 정책에서 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-149">The security rules are defined in the security policy for each module.</span></span> <span data-ttu-id="cbf8b-150">CMVP를 통해 유효성이 검사된 각 모듈에 대한 보안 정책에 대한 링크를 비롯한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)</span><span class="sxs-lookup"><span data-stu-id="cbf8b-150">For more information, including links to the security policy for each module validated through the CMVP, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="cbf8b-151">**FedRAMP에 FIPS 140-2 유효성 검사가 필요합니까?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-151">**Does FedRAMP require FIPS 140-2 validation?**</span></span>

<span data-ttu-id="cbf8b-152">예. FedRAMP(Federal Risk and Authorization Management Program)는 FIPS 유효성이 검사된 암호화 또는 NSA 승인 암호화 사용을 규정하는 [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 암호화 보호를 포함하여 [NIST SP 800-53 개정 4에](https://nvd.nist.gov/800-53/Rev4/)정의된 제어 기준을 활용합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-152">Yes, the Federal Risk and Authorization Management Program (FedRAMP) relies on control baselines defined by the [NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/), including [SC-13 Cryptographic Protection](https://nvd.nist.gov/800-53/Rev4/control/SC-13) mandating the use of FIPS-validated cryptography or NSA-approved cryptography.</span></span>

<span data-ttu-id="cbf8b-153">**기관의 인증 프로세스에서 Microsoft의 FIPS 140-2 준수를 사용할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-153">**Can I use Microsoft's adherence to FIPS 140-2 in my agency's certification process?**</span></span>

<span data-ttu-id="cbf8b-154">FIPS 140-2를 준수하려면 암호화 모듈이 FIPS 승인 알고리즘만 사용하는지 확인을 포함하는 FIPS 승인된 작업 모드에서 실행하도록 시스템을 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-154">To comply with FIPS 140-2, your system must be configured to run in a FIPS approved mode of operation, which includes ensuring that a cryptographic module uses only FIPS-approved algorithms.</span></span> <span data-ttu-id="cbf8b-155">규격으로 시스템을 구성하는 데 대한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)</span><span class="sxs-lookup"><span data-stu-id="cbf8b-155">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="cbf8b-156">**FIPS 140-2와 일반 조건 간의 관계는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="cbf8b-156">**What is the relationship between FIPS 140-2 and Common Criteria?**</span></span>

<span data-ttu-id="cbf8b-157">서로 다르지만 상호 보완적인 두 가지 보안 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-157">These are two separate security standards with different, but complementary, purposes.</span></span> <span data-ttu-id="cbf8b-158">FIPS 140-2는 소프트웨어 및 하드웨어 암호화 모듈의 유효성을 검사하도록 특별히 디자인된 반면, 공통 조건은 IT 소프트웨어 및 하드웨어 제품의 보안 기능을 평가하도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-158">FIPS 140-2 is designed specifically for validating software and hardware cryptographic modules, while the Common Criteria is designed to evaluate security functions in IT software and hardware products.</span></span> <span data-ttu-id="cbf8b-159">일반적인 기준 평가는 종종 FIPS 140-2 유효성 검사를 사용하여 기본 암호화 기능이 제대로 구현되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf8b-159">Common Criteria evaluations often rely on FIPS 140-2 validations to provide assurance that basic cryptographic functionality is implemented properly.</span></span>

### <a name="resources"></a><span data-ttu-id="cbf8b-160">리소스</span><span class="sxs-lookup"><span data-stu-id="cbf8b-160">Resources</span></span>

- [<span data-ttu-id="cbf8b-161">암호화 모듈에 대한 FIPS Pub 140-2 보안 요구 사항</span><span class="sxs-lookup"><span data-stu-id="cbf8b-161">FIPS Pub 140-2 Security Requirements for Cryptographic Modules</span></span>](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [<span data-ttu-id="cbf8b-162">NIST 암호화 모듈 유효성 검사 프로그램</span><span class="sxs-lookup"><span data-stu-id="cbf8b-162">NIST Cryptographic Module Validation Program</span></span>](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [<span data-ttu-id="cbf8b-163">Windows, Windows Server 및 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="cbf8b-163">Windows, Windows Server, and FIPS 140-2</span></span>](/windows/security/threat-protection/fips-140-validation)
- [<span data-ttu-id="cbf8b-164">Microsoft 보안 센터에 대한 규정 준수</span><span class="sxs-lookup"><span data-stu-id="cbf8b-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
