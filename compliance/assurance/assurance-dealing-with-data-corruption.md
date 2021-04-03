---
title: 데이터 손상 처리 Microsoft 365
description: 이 문서에서는 Microsoft 365의 데이터 손상과 Microsoft가 데이터를 방지 및 복구하기 위해 취한 노력에 대해 설명합니다.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497590"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="d539e-103">Microsoft 365에서 데이터 손상 처리</span><span class="sxs-lookup"><span data-stu-id="d539e-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="d539e-104">대규모 클라우드 서비스를 실행하는 데 까다로울 수 있는 측면 중 하나는 데이터 및 독립적인 시스템이 많은 경우 데이터 손상을 처리하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="d539e-105">데이터 손상은 다음으로 인해 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="d539e-106">응용 프로그램 또는 인프라 버그, 응용 프로그램 상태 일부 또는 전체 손상</span><span class="sxs-lookup"><span data-stu-id="d539e-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="d539e-107">데이터가 손실되거나 데이터를 읽지 못하게 하는 하드웨어 문제</span><span class="sxs-lookup"><span data-stu-id="d539e-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="d539e-108">휴먼 운영 오류</span><span class="sxs-lookup"><span data-stu-id="d539e-108">Human operational errors</span></span>
- <span data-ttu-id="d539e-109">악의적인 해커 및 불만이 있는 직원</span><span class="sxs-lookup"><span data-stu-id="d539e-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="d539e-110">데이터가 일부 손실되는 외부 서비스의 인시던트</span><span class="sxs-lookup"><span data-stu-id="d539e-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="d539e-111">데이터 무결성의 복구력은 데이터 손상 인시던트 수가 줄어든다는 것을 의미하기 때문에 Microsoft는 손상 발생을 방지하기 위한 Microsoft 365 보호 메커니즘과 데이터 복구를 가능하게 하는 시스템 및 프로세스를 내장했습니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="d539e-112">검사 및 프로세스는 다음을 포함하여 데이터 손상에 대한 탄력성 향상을 위한 엔지니어링 릴리스 프로세스의 다양한 단계 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="d539e-113">시스템 디자인</span><span class="sxs-lookup"><span data-stu-id="d539e-113">System Design</span></span>
- <span data-ttu-id="d539e-114">코드 조직 및 구조</span><span class="sxs-lookup"><span data-stu-id="d539e-114">Code organization and structure</span></span>
- <span data-ttu-id="d539e-115">코드 검토</span><span class="sxs-lookup"><span data-stu-id="d539e-115">Code review</span></span>
- <span data-ttu-id="d539e-116">단위 테스트, 통합 테스트 및 시스템 테스트</span><span class="sxs-lookup"><span data-stu-id="d539e-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="d539e-117">트립 와이어 테스트/게이트</span><span class="sxs-lookup"><span data-stu-id="d539e-117">Trip wires tests/gates</span></span>

<span data-ttu-id="d539e-118">Microsoft 365 프로덕션 환경 내에서 데이터 센터 간의 피어 복제는 항상 모든 데이터의 라이브 복사본이 여러 개 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="d539e-119">표준 이미지 및 스크립트는 손실된 서버를 복구하는 데 사용하며, 복제된 데이터는 고객 데이터를 복원하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="d539e-120">Microsoft는 기본 제공 데이터 복구 검사 및 프로세스로 인해 SharePoint Online의 기본 제공 복제와 내부 코드 리포지토리 도구인 Source Depot를 사용하여 Microsoft 365 정보 시스템 설명서(보안 관련 설명서 포함)의 백업만 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="d539e-121">시스템 설명서는 SharePoint Online에 저장되고 원본 디포트에는 시스템 및 응용 프로그램 이미지가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="d539e-122">SharePoint Online 및 원본 디포 모두 버전 기능을 사용하며 거의 실시간으로 복제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d539e-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
