---
title: 전송되는 데이터 암호화
description: 이 문서에서는 Microsoft가 전송되는 Microsoft 365 고객 데이터를 암호화하는 방법에 대한 간략한 설명을 제공합니다.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497247"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="8d6a2-103">전송되는 데이터 암호화</span><span class="sxs-lookup"><span data-stu-id="8d6a2-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="8d6a2-104">Microsoft는 미사용 고객 데이터를 보호하는 것 외에도 암호화 기술을 사용하여 전송되는 고객 데이터를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="8d6a2-105">데이터가 전송 중입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-105">Data is in transit:</span></span>

- <span data-ttu-id="8d6a2-106">클라이언트 컴퓨터와 Microsoft 서버 통신하는 경우</span><span class="sxs-lookup"><span data-stu-id="8d6a2-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="8d6a2-107">Microsoft 서버가 다른 Microsoft 서버와 통신하는 경우 및</span><span class="sxs-lookup"><span data-stu-id="8d6a2-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="8d6a2-108">Microsoft 서버가 타사 서버와 통신하는 경우(예: Exchange Online이 타사 전자 메일 서버로 전자 메일을 배달하는 경우).</span><span class="sxs-lookup"><span data-stu-id="8d6a2-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="8d6a2-109">Microsoft 서버 간의 데이터 센터 간 통신은 TLS 또는 IPsec을 통해 진행하며 모든 고객 연결 서버는 클라이언트 컴퓨터와 함께 TLS를 사용하여 보안 세션을 협상합니다(예를 들어 Exchange Online에서는 256비트 암호 강도가 256비트인 TLS 1.2를 사용).(FIPS 140-2 수준 2 유효성 검사).</span><span class="sxs-lookup"><span data-stu-id="8d6a2-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="8d6a2-110">(Office [](/microsoft-365/compliance/technical-reference-details-about-encryption) 365에서 지원하는 TLS 암호화 제품군 목록은 암호화에 대한 기술 참조 세부 정보를 참조하세요.) 이는 Outlook, 비즈니스용 Skype, Microsoft Teams 및 웹용 Outlook(예: HTTP, POP3 등)과 같은 클라이언트에서 사용하는 프로토콜에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="8d6a2-111">공용 인증서는 전송된 정보의 기밀성을 보호하기 위한 내부 Microsoft 도구인 SSLAdmin을 사용하여 Microsoft IT SSL에서 발급합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="8d6a2-112">Microsoft IT에서 발급한 모든 인증서의 길이는 2048비트 이상이기 때문에 Webtrust 준수를 위해서는 SSLAdmin이 Microsoft가 소유한 공용 IP 주소에만 인증서를 발급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="8d6a2-113">이 기준을 충족하지 못하는 IP 주소는 예외 프로세스를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="8d6a2-114">사용되는 TLS 버전, FS(Forward Secrecy) 사용 여부, 암호 제품군 순서 등의 모든 구현 세부 정보를 공개적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="8d6a2-115">이러한 세부 정보를 보는 한 가지 방법은 [Qualys SSL 랩과](https://www.ssllabs.com)같은 타사 웹 사이트를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="8d6a2-116">다음은 다음 서비스에 대한 정보를 표시하는 Qualys의 자동화된 테스트 페이지에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6a2-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="8d6a2-117">Office 365 포털</span><span class="sxs-lookup"><span data-stu-id="8d6a2-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="8d6a2-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8d6a2-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="8d6a2-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8d6a2-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="8d6a2-120">비즈니스용 Skype(SIP)</span><span class="sxs-lookup"><span data-stu-id="8d6a2-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="8d6a2-121">비즈니스용 Skype(웹)</span><span class="sxs-lookup"><span data-stu-id="8d6a2-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="8d6a2-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8d6a2-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="8d6a2-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8d6a2-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="8d6a2-124">Exchange Online Protection의 경우 URL은 테넌트 이름에 따라 다릅니다. 그러나 모든 고객은 를 사용하여 Microsoft 365를 테스트할 **microsoft-com.mail.protection.outlook.com.**</span><span class="sxs-lookup"><span data-stu-id="8d6a2-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
