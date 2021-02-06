---
title: Microsoft 365 SharePoint Online 데이터 지우기
description: 삭제된 콘텐츠가 저장되는 위치 및 기간과 같이 SharePoint Online에서 데이터 삭제가 작동하는 방식에 대해 자세히 알아보겠습니다.
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120747"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="78e54-103">Microsoft 365에서 SharePoint Online 데이터 지우기</span><span class="sxs-lookup"><span data-stu-id="78e54-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="78e54-104">SharePoint Online에서는 개체를 응용 프로그램 데이터베이스에 추상화 코드로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="78e54-105">사용자가 SharePoint Online에 파일을 업로드하면 해당 파일이 분해되어 응용 프로그램 코드로 변환되어 여러 데이터베이스의 여러 테이블에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="78e54-106">SharePoint Online에서 고객이 업로드하는 모든 콘텐츠는 청크로 나누고, 암호화되고(잠재적으로 여러 AES 256비트 키를 사용하여) 데이터 센터에 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="78e54-107">청크 및 암호화 프로세스에 대한 자세한 내용은 Microsoft 클라우드의 암호화를 [참조하세요.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)</span><span class="sxs-lookup"><span data-stu-id="78e54-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="78e54-108">SharePoint Online에서는 항목을 원래 위치에서 삭제한 날부터 93일 동안 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="78e54-109">누군가가 해당 사이트에서 해당 사이트를 삭제하거나 해당 재활용 Bin을 비우지 않는 한 사이트 전체를 사이트 재활용 Bin에 유지하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="78e54-110">이 경우 항목은 사이트 모음 재활용 Bin으로 이동하여 나머지 93일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="78e54-111">삭제된 항목 복원에 대한 자세한 내용은 [SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) 사이트의 휴지란에 있는 항목 복원 및 사이트 모음 휴지 상태의 삭제된 항목 [복원을 참조하세요.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)</span><span class="sxs-lookup"><span data-stu-id="78e54-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="78e54-112">SharePoint Online에서는 재활용 보관 기간을 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="78e54-113">사이트 모음을 삭제하면 모음의 사이트 계층 구조와 사이트 내의 모든 콘텐츠도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="78e54-114">문서 및 문서 라이브러리</span><span class="sxs-lookup"><span data-stu-id="78e54-114">Documents and document libraries</span></span>
- <span data-ttu-id="78e54-115">목록 및 목록 데이터</span><span class="sxs-lookup"><span data-stu-id="78e54-115">Lists and list data</span></span>
- <span data-ttu-id="78e54-116">사이트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="78e54-116">Site configuration settings</span></span>
- <span data-ttu-id="78e54-117">사이트 또는 해당 하위 사이트와 관련된 역할 및 보안 정보</span><span class="sxs-lookup"><span data-stu-id="78e54-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="78e54-118">최상위 웹 사이트의 하위 사이트, 해당 콘텐츠 및 사용자 정보</span><span class="sxs-lookup"><span data-stu-id="78e54-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="78e54-119">사이트 모음을 실수로 삭제한 경우 SharePoint 관리 센터를 사용하여 전역 또는 SharePoint 관리자가 사이트 모음을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="78e54-120">삭제된 사이트 모음은 93일 동안 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="78e54-121">93 일이 지나면 목록, 라이브러리, 페이지, 모든 하위 사이트를 포함 한 사이트와 해당 콘텐츠 및 설정이 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="78e54-122">영구 삭제는 사용자가 사이트 모음의 삭제된 항목을 삭제하거나, 보존 및 백업 기간이 만료될 때 또는 [관리자가 Remove-SPODeletedSite cmdlet을](/powershell/module/sharepoint-online/remove-spodeletedsite)사용하여 사이트 모음을 영구적으로 삭제하는 경우 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="78e54-123">사용자가 SharePoint Online에서 콘텐츠를 영구적으로 삭제하거나 삭제하면 삭제된 청크의 모든 암호화 키도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="78e54-124">이전에 삭제된 청크를 저장한 디스크의 블록은 사용되지 않은 것으로 표시되고 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78e54-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
