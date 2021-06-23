---
title: Microsoft 직원 이전 및 종료
description: Microsoft 직원 이전 및 종료 프로세스에 대해 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b31dd13f4a6209712a9cc212ab3bcd9c5addf6b7
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089657"
---
# <a name="microsoft-employee-transfer-and-termination"></a><span data-ttu-id="9537f-103">Microsoft 직원 이전 및 종료</span><span class="sxs-lookup"><span data-stu-id="9537f-103">Microsoft employee transfer and termination</span></span>

<span data-ttu-id="9537f-104">직원 이전 및 퇴사는 모든 조직의 정상적인 비즈니스 운영의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-104">Employee transfers and terminations are a part of every organization's normal business operations.</span></span> <span data-ttu-id="9537f-105">직원이 직위를 변경하거나 퇴사할 때 부적절한 액세스를 시기적절하게 해지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-105">When an employee changes positions or leaves the company, it is essential to revoke inappropriate access in a timely manner.</span></span> <span data-ttu-id="9537f-106">효율적인 액세스 변경 및 액세스 해지 작업을 Microsoft 365 표준화된 절차와 자동화된 프로세스를 사용하여 HRIS(인사 정보 시스템)를 IDM(ID 관리) 시스템과 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-106">To facilitate efficient access changes and access revocations, Microsoft 365 uses standardized procedures and automated processes to coordinate the Human Resources Information System (HRIS) with the Identity Management (IDM) system.</span></span> <span data-ttu-id="9537f-107">이러한 두 시스템 간의 자동화된 오케스트레이션은 운영 일관성을 유지하고, Microsoft 365 및 데이터를 보호하고, 권한 크리프를 방지하고, 내부자 위협과 관련된 위험을 줄이는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-107">Automated orchestration between these two systems is essential to maintaining operational consistency, safeguarding Microsoft 365's services and data, preventing privilege creep, and reducing risks related to insider threats.</span></span>

<span data-ttu-id="9537f-108">Microsoft 365 시스템은 엔지니어를 위해 프로덕션 환경에 대한 관리 액세스 권한 없이 작동하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-108">Microsoft 365 systems are designed to operate without standing administrative access to production environments for our engineers.</span></span> <span data-ttu-id="9537f-109">Microsoft는 JIT(Just-In-Time), JEA(Just-Enough-Access) 모델을 사용하여 엔지니어에게 필요할 때 서비스를 지원하는 데 필요한 임시 액세스 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-109">Microsoft uses a Just-In-Time (JIT), Just-Enough-Access (JEA) model to provide engineers with the temporary access needed to support their service when required.</span></span> <span data-ttu-id="9537f-110">JIT 액세스를 위해 서비스 팀 계정을 요청하고 사용하려면 엔지니어가 IDM 도구를 통해 자격을 요청하고 유지 관리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-110">To request and use a service team account for JIT access, engineers must request and maintain eligibilities through the IDM tool.</span></span> <span data-ttu-id="9537f-111">직원이 양도 또는 해지되면 해당 서비스 팀 계정 및 관련 자격이 부적절한 액세스를 방지하기 위해 자동으로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-111">When employees are transferred or terminated, their service team account and related eligibilities are automatically modified to prevent inappropriate access.</span></span>

## <a name="transfer-and-reassignment"></a><span data-ttu-id="9537f-112">전송 및 재할당</span><span class="sxs-lookup"><span data-stu-id="9537f-112">Transfer and reassignment</span></span>

<span data-ttu-id="9537f-113">직원 이전은 직원의 상사에 의해 이전 트랜잭션 요청을 통해 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-113">Employee transfers are initiated through a transfer transaction request by the employee's manager.</span></span> <span data-ttu-id="9537f-114">관리자는 재지정을 만들고 제안서 프로세스에 대해 전역 인재 인수에 참여합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-114">The manager creates a requisition and engages with Global Talent Acquisition for the offer letter process.</span></span> <span data-ttu-id="9537f-115">직원이 새 역할에 대한 제안을 수락하면 HR 서비스는 HR 핵심 도구의 이전을 완료하여 IDM이 모든 직원의 자격에 대한 만료 날짜를 설정하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-115">Once the employee accepts the offer for the new role, HR services completes the transfer in the HR core tools, triggering IDM to set an expiration date for all the employee's eligibilities.</span></span> <span data-ttu-id="9537f-116">직원은 요청을 제출하고 새 관리자로부터 승인을 받아 자격을 유지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-116">The employee must submit a request and receive approval from their new manager to retain their eligibilities.</span></span> <span data-ttu-id="9537f-117">요청을 제출하거나 관리자 승인을 받지 못하면 전달된 직원의 자격이 해지됩니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-117">Failure to submit a request or receive manager approval results in the revocation of the transferred employee's eligibilities.</span></span> <span data-ttu-id="9537f-118">특정 보안이 포함된 전송의 경우 시스템 액세스 및 보안 그룹 구성원 자격이 새 역할을 반영하도록 즉시 다시 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-118">For transfers that include specific security implications, system accesses and security group memberships are reevaluated immediately to reflect their new role.</span></span>

## <a name="termination"></a><span data-ttu-id="9537f-119">종료</span><span class="sxs-lookup"><span data-stu-id="9537f-119">Termination</span></span>

<span data-ttu-id="9537f-120">Microsoft는 명확하게 정의된 정책 및 절차를 사용하여 직원이 해지될 때 Microsoft 시스템 및 리소스에 대한 물리적 및 논리적 액세스를 즉시 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-120">Microsoft uses clearly defined policies and procedures to promptly revoke physical and logical access to Microsoft systems and resources when an employee is terminated.</span></span> <span data-ttu-id="9537f-121">직원이 통지를 하면 직원의 상사는 종료 날짜를 HRIS에 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-121">When an employee gives their notice, the employee's manager enters the termination date into the HRIS.</span></span> <span data-ttu-id="9537f-122">직원의 마지막 작업일 다음에 HRIS는 직원을 종료된 것으로 표시하고 정보를 IDM에 공유하여 모든 서비스 팀 계정 및 자격을 자동으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-122">Following the employee's last working day, the HRIS marks the employee as terminated and shares the information to IDM, which removes all service team accounts and eligibilities automatically.</span></span>

<span data-ttu-id="9537f-123">자발적 종료의 경우 HR은 직원의 관리자와 함께 적절한 단계에 따라 직원을 종료하고 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-123">For involuntary terminations, HR works with the employee's manager to follow the appropriate steps to terminate and offboard the employee.</span></span> <span data-ttu-id="9537f-124">자발적 종료와 마찬가지로 종료 정보는 유효 날짜 조정, 액세스 제거와 같은 필요한 단계와 함께 HRIS에 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="9537f-124">Similar to a voluntary termination, the termination information is entered into the HRIS along with any necessary steps such as effective date coordination, access removal.</span></span> <span data-ttu-id="9537f-125">및 역할 전환과 상대적인 다른 모든 단계</span><span class="sxs-lookup"><span data-stu-id="9537f-125">and any other steps relative to transitioning out of role.</span></span>
