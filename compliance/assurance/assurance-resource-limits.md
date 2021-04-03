---
title: Microsoft 365 리소스 제한
description: 이 문서에서는 Microsoft 365 내의 다양한 응용 프로그램에 대한 리소스 제한에 대한 정보를 찾을 수 있습니다.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497506"
---
# <a name="service-resource-limits"></a><span data-ttu-id="47390-103">서비스 리소스 제한 사항</span><span class="sxs-lookup"><span data-stu-id="47390-103">Service resource limits</span></span>

<span data-ttu-id="47390-104">리소스 제한은 할당량(제한) 및 제한을 사용하여 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="47390-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="47390-105">Azure AD(Azure Active Directory) 및 개별 Microsoft 365 서비스는 둘 다를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="47390-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="47390-106">제한은 서비스별 제한으로, 시간이 지날 때 새로운 기능이 추가될 때 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="47390-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="47390-107">다양한 서비스의 현재 제한에 대한 자세한 내용은 다음 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="47390-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="47390-108">Azure AD 서비스 제한 사항</span><span class="sxs-lookup"><span data-stu-id="47390-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="47390-109">Exchange Online 제한</span><span class="sxs-lookup"><span data-stu-id="47390-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="47390-110">SharePoint Online 소프트웨어 경계 및 제한</span><span class="sxs-lookup"><span data-stu-id="47390-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="47390-111">비즈니스용 Skype 제한</span><span class="sxs-lookup"><span data-stu-id="47390-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="47390-112">Yammer REST API 및 속도 제한</span><span class="sxs-lookup"><span data-stu-id="47390-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="47390-113">Sway의 파일 크기 제한</span><span class="sxs-lookup"><span data-stu-id="47390-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="47390-114">이러한 제한 외에도 Azure AD 및 Microsoft 365 전체에서 여러 제한 메커니즘이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="47390-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="47390-115">Microsoft 데이터 센터의 네트워크 리소스가 서비스를 사용하는 광범위한 고객 집합에 최적화되어 있는 경우 서비스 내의 스로틀은 특히 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="47390-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="47390-116">다음과 같은 스로틀 메커니즘이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47390-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="47390-117">Azure AD 및 Microsoft 365는 단일 사용자가 수행할 수 있는 트랜잭션 또는 동시 통화(스크립트 또는 코드로)의 수를 제한하는 사용자 수준 제한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="47390-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="47390-118">기본 PowerShell 스로틀 정책은 테넌트 만들기 시 각 테넌트에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="47390-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="47390-119">이러한 설정은 단일 관리자가 열 수 있는 최대 동시 PowerShell 세션 수와 같은 다른 항목에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47390-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="47390-120">각 Exchange Online 고객에게는 EWS 클라이언트 작업에 맞게 조정된 기본 EWS(Exchange 웹 서비스) 정책과 모든 Outlook 클라이언트에 적용되는 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47390-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
