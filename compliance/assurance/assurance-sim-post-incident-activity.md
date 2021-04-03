---
title: 'Microsoft 365 보안 인시던트 관리: 인시던트 사후 활동'
description: 이 문서에서는 Microsoft 365의 보안 인시던트 관리 사후 인시던트 활동 프로세스에 대한 개요를 제공합니다.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496707"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="91a0c-103">Microsoft 365 보안 인시던트 관리: 인시던트 사후 활동</span><span class="sxs-lookup"><span data-stu-id="91a0c-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="91a0c-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="91a0c-104">Postmortem</span></span>

<span data-ttu-id="91a0c-105">일부 보안 인시던트, 특히 고객에 영향을 미치거나 데이터 위반으로 인해 발생한 인시던트는 전체 인시던트 사후 대응의 대상이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="91a0c-106">Microsoft 365 보안 대응 팀은 다음에 대한 보안 인시던트 대응과 관련된 모든 당사자와 자세한 사후 대응을 실시합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="91a0c-107">인시던트가 발생된 이벤트 시퀀스를 문서화합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="91a0c-108">위반에 관련된 배우가 포함된 증거(알려진 경우)에서 지원되는 인시던트의 기술 요약을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="91a0c-109">이 요약에는 응답이 실행된 방법 및 기타 키가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="91a0c-110">기술 경과, 절차적 오류, 수동 오류, 프로세스 결함 및 통신 결함 및/또는 보안 인시던트 대응 중에 식별된 이전에 알려지지 않은 공격 벡터를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="91a0c-111">사후 계획은 Microsoft 365 엔지니어링 개발 주기에서 새로운 우선 순위를 설정하여 Microsoft 365 서비스 개선, 운영 프로세스 및 설명서에 직접적인 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="91a0c-112">설명서</span><span class="sxs-lookup"><span data-stu-id="91a0c-112">Documentation</span></span>

<span data-ttu-id="91a0c-113">사후 프로세스에서 발견된 모든 주요 기술 결과는 버그 또는 개발 변경 요청의 형태로 보고서 및 서비스 투자 또는 수정에 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="91a0c-114">이러한 결과는 적절한 엔지니어링 팀과 함께 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="91a0c-115">프로세스 오류 및 조직 간 문제의 경우 Microsoft 365 보안 대응 팀의 데이터베이스에 문제점이 문서화되어 있으며 해당 그룹과 함께 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="91a0c-116">프로세스 개선</span><span class="sxs-lookup"><span data-stu-id="91a0c-116">Process improvement</span></span>

<span data-ttu-id="91a0c-117">Microsoft 365의 보안 인시던트에 대응하는 과정에는 Microsoft 내의 여러 조직에 분산된 여러 그룹과의 조율 및 사법 기관과 같은 잠재적으로 적절한 외부 조직과의 조율이 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="91a0c-118">모든 보안 인시던트 이후의 대응을 평가하여 충분하고 완전한 대응을 평가하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="91a0c-119">확인된 개선 또는 변경에 대해 Microsoft 365 보안 대응 팀은 해당 팀 및 이해 관계자와 협의하여 제안 사항을 평가하고, 적절한 경우 해당 제안을 표준 운영 절차에 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="91a0c-120">보안 인시던트 대응 또는 사후 작업 중에 식별된 모든 필수 변경 사항, 버그 또는 서비스 개선 사항은 내부 Microsoft 365 엔지니어링 데이터베이스에 기록 및 추적됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="91a0c-121">모든 잠재적인 버그 또는 기능이 적절한 소유자에게 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="91a0c-122">Microsoft 365 보안 대응 팀은 문제가 해결될 때까지 모든 항목을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="91a0c-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="91a0c-123">관련 문서</span><span class="sxs-lookup"><span data-stu-id="91a0c-123">Related articles</span></span>

- [<span data-ttu-id="91a0c-124">Microsoft 365 보안 인시던트 관리</span><span class="sxs-lookup"><span data-stu-id="91a0c-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="91a0c-125">Microsoft 365 보안 인시던트 관리 준비</span><span class="sxs-lookup"><span data-stu-id="91a0c-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="91a0c-126">Microsoft 365 보안 인시던트 관리 감지 및 분석</span><span class="sxs-lookup"><span data-stu-id="91a0c-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="91a0c-127">Microsoft 365 보안 인시던트 관리 포함, 지우기 및 복구</span><span class="sxs-lookup"><span data-stu-id="91a0c-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
