---
title: Microsoft 365 엔지니어링에 대한 내부 Microsoft 365 로깅
description: 이 문서에서는 엔지니어링 팀의 내부 로깅이 작동하는 Microsoft 365 있습니다.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088597"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="e69a1-103">Microsoft 365 엔지니어링에 대한 내부 로깅</span><span class="sxs-lookup"><span data-stu-id="e69a1-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="e69a1-104">Microsoft는 고객이 사용할 수 있는 이벤트 및 로그 데이터 외에도 microsoft 엔지니어가 사용할 수 있는 내부 로그 데이터 Microsoft 365 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="e69a1-105">여러 유형의 로그 데이터가 Microsoft 365 서버에서 NRT(거의 실시간) 분석을 위한 독점 보안 모니터링 솔루션으로 업로드되어 장기 저장소를 위한 내부 Cosmos(big data computing Service)에 업로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="e69a1-106">이 데이터 전송은 ODL(Office Data Loader)이라는 전용 자동화 도구를 사용하여 승인된 포트 및 프로토콜에서 FIPS 140-2 유효성이 검사된 TLS 연결을 통해 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="e69a1-107">감사 레코드를 Microsoft 365 데 사용되는 도구는 원래 감사 레코드 콘텐츠 또는 시간 순서를 영구적으로 또는 돌이할 수 없는 변경을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="e69a1-108">서비스 팀은 Cosmos 저장소로 사용하여 응용 프로그램 사용 현황을 분석하고 시스템 및 운영 성능을 측정하고 문제나 보안 문제를 나타낼 수 있는 비정상 및 패턴을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="e69a1-109">각 서비스 팀은 다음을 포함하는 기준을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="e69a1-110">이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="e69a1-110">Event logs</span></span>
- <span data-ttu-id="e69a1-111">AppLocker 로그</span><span class="sxs-lookup"><span data-stu-id="e69a1-111">AppLocker logs</span></span>
- <span data-ttu-id="e69a1-112">성능 데이터</span><span class="sxs-lookup"><span data-stu-id="e69a1-112">Performance data</span></span>
- <span data-ttu-id="e69a1-113">System Center 데이터</span><span class="sxs-lookup"><span data-stu-id="e69a1-113">System Center data</span></span>
- <span data-ttu-id="e69a1-114">통화 정보 기록</span><span class="sxs-lookup"><span data-stu-id="e69a1-114">Call detail records</span></span>
- <span data-ttu-id="e69a1-115">환경 품질 데이터</span><span class="sxs-lookup"><span data-stu-id="e69a1-115">Quality of experience data</span></span>
- <span data-ttu-id="e69a1-116">IIS 웹 서버 로그</span><span class="sxs-lookup"><span data-stu-id="e69a1-116">IIS Web Server logs</span></span>
- <span data-ttu-id="e69a1-117">SQL Server 로그</span><span class="sxs-lookup"><span data-stu-id="e69a1-117">SQL Server logs</span></span>
- <span data-ttu-id="e69a1-118">Syslog 데이터</span><span class="sxs-lookup"><span data-stu-id="e69a1-118">Syslog data</span></span>
- <span data-ttu-id="e69a1-119">보안 감사 로그</span><span class="sxs-lookup"><span data-stu-id="e69a1-119">Security audit logs</span></span>

<span data-ttu-id="e69a1-120">업로드하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용하여 테넌트 정보 및 최종 사용자 식별 가능 정보와 같은 고객 데이터가 포함된 모든 필드를 제거하고 해당 필드를 해시 값으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="e69a1-121">스크러빙된 로그는 Cosmos 및 성능 지표에 대한 로그를 분석하는 NRT 보안 모니터링 솔루션에 업로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="e69a1-122">감사 로그 데이터 보존 기간은 Cosmos 팀에 의해 결정됩니다. 대부분의 감사 로그 데이터는 보안 인시던트 조사를 지원하고 규정 보존 요구 사항을 충족하기 위해 90일 이상 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="e69a1-123">사용자 Microsoft 365 데이터에 대한 액세스는 Cosmos 권한이 있는 직원으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="e69a1-124">Microsoft는 감사 로그 관리를 감사 기능을 담당하는 보안 팀 구성원의 제한된 하위 집합으로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="e69a1-125">보안 팀은 보안 팀에 대한 관리자 액세스 권한이 Cosmos 모든 변경 내용이 기록 및 감사됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="e69a1-126">NRT 분석 후 각 서비스 팀은 데이터 상관 관계, 대화형 쿼리 및 데이터 분석을 위해 분석 도구 및 대시보드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="e69a1-127">이러한 보고서는 서비스의 전반적인 성능을 모니터링하고 개선하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69a1-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
