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
# <a name="encryption-for-data-in-transit"></a>전송되는 데이터 암호화

Microsoft는 미사용 고객 데이터를 보호하는 것 외에도 암호화 기술을 사용하여 전송되는 고객 데이터를 보호합니다. 데이터가 전송 중입니다.

- 클라이언트 컴퓨터와 Microsoft 서버 통신하는 경우
- Microsoft 서버가 다른 Microsoft 서버와 통신하는 경우 및
- Microsoft 서버가 타사 서버와 통신하는 경우(예: Exchange Online이 타사 전자 메일 서버로 전자 메일을 배달하는 경우).

Microsoft 서버 간의 데이터 센터 간 통신은 TLS 또는 IPsec을 통해 진행하며 모든 고객 연결 서버는 클라이언트 컴퓨터와 함께 TLS를 사용하여 보안 세션을 협상합니다(예를 들어 Exchange Online에서는 256비트 암호 강도가 256비트인 TLS 1.2를 사용).(FIPS 140-2 수준 2 유효성 검사). (Office [](/microsoft-365/compliance/technical-reference-details-about-encryption) 365에서 지원하는 TLS 암호화 제품군 목록은 암호화에 대한 기술 참조 세부 정보를 참조하세요.) 이는 Outlook, 비즈니스용 Skype, Microsoft Teams 및 웹용 Outlook(예: HTTP, POP3 등)과 같은 클라이언트에서 사용하는 프로토콜에 적용됩니다.

공용 인증서는 전송된 정보의 기밀성을 보호하기 위한 내부 Microsoft 도구인 SSLAdmin을 사용하여 Microsoft IT SSL에서 발급합니다. Microsoft IT에서 발급한 모든 인증서의 길이는 2048비트 이상이기 때문에 Webtrust 준수를 위해서는 SSLAdmin이 Microsoft가 소유한 공용 IP 주소에만 인증서를 발급해야 합니다. 이 기준을 충족하지 못하는 IP 주소는 예외 프로세스를 통해 라우팅됩니다.

사용되는 TLS 버전, FS(Forward Secrecy) 사용 여부, 암호 제품군 순서 등의 모든 구현 세부 정보를 공개적으로 사용할 수 있습니다. 이러한 세부 정보를 보는 한 가지 방법은 [Qualys SSL 랩과](https://www.ssllabs.com)같은 타사 웹 사이트를 사용하는 것입니다. 다음은 다음 서비스에 대한 정보를 표시하는 Qualys의 자동화된 테스트 페이지에 대한 링크입니다.

- [Office 365 포털](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [비즈니스용 Skype(SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [비즈니스용 Skype(웹)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Exchange Online Protection의 경우 URL은 테넌트 이름에 따라 다릅니다. 그러나 모든 고객은 를 사용하여 Microsoft 365를 테스트할 **microsoft-com.mail.protection.outlook.com.**
