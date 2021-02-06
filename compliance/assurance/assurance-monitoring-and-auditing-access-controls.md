---
title: Microsoft 365 액세스 제어 모니터링 및 감사
description: '요약: Microsoft 365 내에서 사용할 수 있는 다양한 모니터링 및 감사 액세스 제어에 대한 요약입니다.'
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120447"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="065cb-103">Microsoft 365의 액세스 제어 모니터링 및 감사</span><span class="sxs-lookup"><span data-stu-id="065cb-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="065cb-104">Microsoft는 Microsoft 365 내에서 발생하는 모든 위임, 권한 및 작업에 대한 광범위한 모니터링 및 감사를 수행하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="065cb-105">Microsoft 365 액세스 제어는 최소 권한 원칙을 사용하여 구축된 자동화된 프로세스로, 데이터 액세스 제어 및 감사를 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="065cb-106">허용된 모든 액세스는 고유한 사용자에 따라 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="065cb-107">관리자는 고객 콘텐츠를 처리할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="065cb-108">액세스 제어 요청, 승인 및 관리 작업 로그는 보안 및 악의적인 이벤트를 분석하기 위해 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="065cb-109">액세스 수준은 보안 그룹 구성원 자격에 따라 거의 실시간으로 검토하여 업무 정당성을 부여하고 자격 요구 사항을 충족하는 사용자만 시스템에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="065cb-110">Microsoft 365, 해당 액세스 제어 및 지원 서비스(Azure Active Directory 및 실제 데이터 센터 포함)는 [ISO/IEC 27001, ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP(Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)및 기타 표준을 준수하기 위해 독립적인 타사에서 정기적으로 감사를 [합니다.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons) [](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018)</span><span class="sxs-lookup"><span data-stu-id="065cb-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="065cb-111">Microsoft 365 엔지니어는 연도당 보안 교육을 수행하고, 높은 액세스 모범 절차를 검토하고, 서비스에 대한 권리 유지를 위해 Microsoft의 보안 및 개인 정보 보호 정책을 인정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="065cb-112">자동화된 경고는 짧은 기간 내에 여러 번 실패한 로그인과 같은 의심스러운 활동이 감지되면 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="065cb-113">Microsoft 365 보안 대응 팀은 기계 학습 및 빅 데이터 분석을 사용하여 활동을 검토 및 분석하고, 불규칙한 액세스 패턴을 찾아서, 촉각적이지 못하고 부정한 활동에 선제적으로 대응합니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="065cb-114">또한 Microsoft는 침투 테스터의 전담 팀을 고용하고 주기적인 Red Team 및 Blue Team 연습에 참여하여 서비스에서 보안 및 액세스 제어 문제를 찾아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="065cb-115">고객은 감사 보고서 및 Microsoft 365에서 제공하는 관리 활동 API를 사용하여 액세스 제어 시스템의 효율성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="065cb-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="065cb-116">자세한 내용은 [Microsoft 365의 Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) 관리 활동 API 참조 및 감사 및 [보고를 참조하세요.](assurance-auditing-and-reporting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="065cb-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
