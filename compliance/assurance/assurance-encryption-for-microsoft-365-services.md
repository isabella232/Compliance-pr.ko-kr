---
title: Skype, OneDrive, SharePoint 및 Exchange
description: '요약: Skype, OneDrive, SharePoint, Microsoft Teams 및 Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 480e7e03564075707c90e25ad5777631c1e68ed8
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160469"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>비즈니스용 Skype, 비즈니스용 OneDrive, SharePoint Online, Microsoft Teams 및 Exchange Online

Microsoft 365 보안은 물리적 데이터 센터 보안, 네트워크 보안, 액세스 보안, 응용 프로그램 보안 및 데이터 보안과 같은 여러 계층에서 광범위한 보호를 제공하는 매우 안전한 환경입니다.

## <a name="skype-for-business"></a>비즈니스용 Skype

비즈니스용 Skype 고객 데이터는 모임 참가자가 업로드하는 파일 또는 프레젠테이션 형태로 저장될 수 있습니다. 웹 회의 서버는 256비트 키와 함께 AES를 사용하여 고객 데이터를 암호화합니다. 암호화된 고객 데이터는 파일 공유에 저장됩니다. 각 고객 데이터는 임의로 생성된 256비트 키를 사용하여 암호화됩니다. 회의에서 고객 데이터를 공유하는 경우 웹 회의 서버는 회의 클라이언트가 HTTPS를 통해 암호화된 고객 데이터를 다운로드할 수 있도록 지시합니다. 고객 데이터를 암호 해독할 수 있도록 클라이언트에 해당 키를 전송합니다. 또한 웹 회의 서버는 클라이언트가 회의 고객 데이터에 액세스할 수 있도록 허용하기 전에 회의 클라이언트를 인증합니다. 웹 회의에 참가할 때 각 회의 클라이언트는 먼저 TLS를 통해 프런트 엔드 서버 내에서 실행되는 회의 포커스 구성 요소와 SIP 대화 상자를 설정합니다. 회의 포커스가 웹 회의 서버에서 생성된 인증 쿠키를 회의 클라이언트로 전달합니다. 그러면 회의 클라이언트가 서버에서 인증할 인증 쿠키를 제시하는 웹 회의 서버에 연결합니다.

## <a name="sharepoint-online-and-onedrive-for-business"></a>Microsoft Office SharePoint Online 및 비즈니스용 OneDrive

SharePoint Online의 모든 고객 파일은 항상 단일 테넌트에서만 사용할 수 있는 고유한 파일당 키로 보호됩니다. 키는 SharePoint Online 서비스에서 생성 및 관리하거나 고객 키를 사용, 생성 및 관리할 때 만들어집니다. 파일이 업로드될 때 Azure 저장소로 전송되기 전에 SharePoint 요청 컨텍스트 내에서 SharePoint Online에서 암호화를 수행합니다. 파일이 다운로드되면 SharePoint Online은 고유한 문서 식별자를 기반으로 Azure Storage에서 암호화된 고객 데이터를 검색하고 사용자에게 보내기 전에 고객 데이터를 암호 해독합니다. Azure Storage에는 고객 데이터를 식별하거나 이해할 수 있는 능력이 없습니다. 모든 암호화 및 암호 해독은 온라인에서 지원되는 테넌트 Azure Active Directory SharePoint 시스템에서 실행됩니다.

Microsoft 365 작업은 SharePoint Online에 모든 파일을 저장하는 Microsoft Teams, SharePoint Online에 모든 파일을 저장하는 비즈니스용 OneDrive(저장소에 SharePoint Online 사용)를 포함하여 SharePoint Online에 데이터를 저장합니다. SharePoint Online에 저장된 모든 고객 데이터는 암호화되고(하나 이상의 AES 256비트 키 사용) 다음과 같이 데이터 센터에 분산됩니다. (이 암호화 프로세스의 모든 단계에서는 FIPS 140-2 수준 2의 유효성을 검사합니다. FIPS 140-2 규정 준수에 대한 자세한 내용은 [FIPS 140-2 준수를 참조하세요.](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- 각 파일은 파일 크기에 따라 하나 이상의 청크로 분할됩니다. 각 청크는 고유한 AES 256비트 키를 사용하여 암호화됩니다.
- 파일이 업데이트될 때 업데이트는 하나 이상의 청크로 분할되고 각 청크는 별도의 고유 키로 암호화되는 방식으로 처리됩니다.
- 파일, 파일 조각, 업데이트 델타 등 이러한 청크는 여러 Azure 저장소 계정에 임의로 분산되는 Azure 저장소에 Blob으로 저장됩니다.
- 이러한 고객 데이터 청크에 대한 암호화 키 집합은 자체적으로 암호화됩니다.

    - Blob을 암호화하는 데 사용되는 키는 온라인 콘텐츠 SharePoint 저장됩니다.
    - 콘텐츠 데이터베이스는 미사용 데이터베이스 액세스 제어 및 암호화로 보호됩니다. 암호화는 에서 [TDE(투명한 데이터 암호화)를](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) 사용하여 [Azure SQL Database.](/azure/sql-database/sql-database-technical-overview) (Azure SQL Database 관계형 데이터, JSON, 공간 Microsoft Azure XML과 같은 구조를 지원하는 데이터베이스의 일반적인 용도의 관계형 데이터베이스 서비스입니다.) 이러한 비밀은 테넌트 수준이 아닌 SharePoint Online의 서비스 수준에 있습니다. 이러한 비밀(마스터 키라고도 불리며)은 키 저장소라는 별도의 보안 저장소에 저장됩니다. TDE는 활성 데이터베이스와 데이터베이스 백업 및 트랜잭션 로그 모두에 대해 미사용 보안을 제공합니다.
    - 고객이 선택적 키를 제공하는 경우 고객 키는 Azure Key Vault에 저장되고 서비스에서는 키로 테넌트 키를 암호화합니다. 이 키는 사이트 키를 암호화하는 데 사용되며, 이 키는 파일 수준 키를 암호화하는 데 사용됩니다. 기본적으로 고객이 키를 제공하면 새 키 계층 구조가 도입됩니다.
- 파일을 다시 어셈블하는 데 사용되는 맵은 암호 해독에 필요한 마스터 키와는 별도로 암호화된 키와 함께 콘텐츠 데이터베이스에 저장됩니다.
- 각 Azure 저장소 계정에는 액세스 유형별로 고유한 자격 증명이 있습니다(읽기, 쓰기, 열기 및 삭제). 각 자격 증명 집합이 보안 키 저장소에 보관되고 정기적으로 새로 고쳐집니다. 위에서 설명한 대로 각각 고유한 기능을 가지는 세 가지 유형의 저장소가 있습니다.
    - 고객 데이터는 Azure 저장소에 암호화된 Blob으로 저장됩니다. 고객 데이터의 각 청크에 대한 키는 암호화되고 콘텐츠 데이터베이스에 별도로 저장됩니다. 고객 데이터 자체는 암호 해독 방법에 대한 단서를 저장하지 않습니다.
    - 콘텐츠 데이터베이스는 SQL Server 데이터베이스입니다. Azure Storage에 보관된 고객 데이터 Blob을 찾고 다시 배정하는 데 필요한 맵과 이러한 Blob을 암호화하는 데 필요한 키가 보관됩니다. 그러나 키 집합은 위에서 설명한 대로 자체적으로 암호화되고 별도의 키 저장소에 보관됩니다.
    - 키 저장소는 콘텐츠 데이터베이스 및 Azure 저장소와 물리적으로 분리됩니다. 각 Azure 저장소 컨테이너에 대한 자격 증명과 마스터 키는 콘텐츠 데이터베이스에 보관된 암호화된 키 집합에 보관됩니다.

이러한 세 가지 저장소 구성 요소(Azure Blob 저장소, 콘텐츠 데이터베이스 및 키 저장소)는 물리적으로 분리되어 있습니다. 구성 요소 중 하나에 보관된 정보를 자체적으로 사용할 수는 없습니다. 세 가지 모두에 액세스하지 않으면 청크에 대한 키를 검색하거나, 키를 사용할 수 있도록 암호 해독하거나, 키를 해당 청크에 연결하거나, 각 청크의 암호를 해독하거나, 구성 청크에서 문서를 재구성할 수 없습니다.

데이터 센터에 있는 컴퓨터의 실제 디스크 볼륨을 보호하는 BitLocker 인증서는 팜 키로 보호되는 보안 저장소(SharePoint Online 비밀 저장소)에 저장됩니다.

Blob당 키를 보호하는 TDE 키는 다음 두 위치에 저장됩니다.

- BitLocker 인증서를 포함하며 팜 키로 보호되는 보안 리포지토리 및
- 보안 저장소에서 관리되는 Azure SQL Database.

Azure 저장소 컨테이너에 액세스하는 데 사용되는 자격 증명도 SharePoint Online 비밀 저장소에 보관되어 있으며 SharePoint 온라인 팜에 위임됩니다. 이러한 자격 증명은 Azure Storage SAS 서명으로, 데이터를 읽거나 쓰는 데 사용되는 별도의 자격 증명과 정책이 적용되어 60일마다 자동 만료됩니다. 데이터를 읽거나 쓰는 데 서로 다른 자격 증명이 사용되거나(둘 다가 아니라) 온라인 팜에 열 SharePoint 권한이 부여되지 않습니다.

> [!NOTE]
> 미국 Office 365 고객의 경우 데이터 Blob은 Azure U.S. Government 2013에 Storage. 또한 미국 SharePoint 있는 Office 365 온라인 키에 대한 액세스는 Office 365 직원으로 제한됩니다. Azure 미국 정부 운영 직원은 데이터 blob 암호화에 SharePoint 온라인 키 저장소에 액세스할 수 없습니다.

SharePoint Online 및 비즈니스용 OneDrive 암호화에 대한 자세한 내용은 비즈니스용 OneDrive 및 SharePoint [Online의 데이터 암호화를 참조하세요.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>온라인에서 항목 SharePoint 목록

목록 항목은 사용자가 만든 목록의 행, SharePoint Online 블로그의 개별 게시물 또는 SharePoint Online 위키 페이지 내의 항목과 같이 사이트 내에서 더 동적으로 사용할 수 있는 고객 데이터의 작은 청크입니다. 목록 항목은 콘텐츠 데이터베이스(Azure SQL Database)에 저장되고 TDE로 보호됩니다.

## <a name="encryption-of-data-in-transit"></a>전송 중인 데이터 암호화

비즈니스용 OneDrive 및 SharePoint Online에는 데이터 센터를 시작 및 종료하는 데이터에 대한 두 가지 시나리오가 있습니다.

- **서버와의** 클라이언트 통신 - 인터넷을 통해 SharePoint 온라인 및 비즈니스용 OneDrive 통신에서는 TLS 연결을 사용 합니다.
- **데이터 센터 간** 데이터 이동 - 데이터 센터 간에 데이터를 이동하는 주된 이유는 재해 복구를 사용하도록 설정하기 위한 지리적 복제입니다. 예를 들어 SQL Server 트랜잭션 로그 및 Blob Storage 델타가 이 파이프를 따라 이동합니다. 이 데이터는 개인 네트워크를 사용하여 이미 전송되었지만 최고급 암호화로 추가 보호됩니다.

## <a name="exchange-online"></a>Exchange Online

Exchange Online 모든 사서함 데이터에 대해 BitLocker를 사용하며 BitLocker 구성은 [BitLocker for Encryption에 설명되어 있습니다.](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption) 서비스 수준 암호화는 사서함 수준에서 모든 사서함 데이터를 암호화합니다. 

서비스 암호화 외에도 Microsoft 365 암호화를 토대한 고객 키도 지원됩니다. 고객 키는 Microsoft의 로드맵에도 Exchange Online 서비스 암호화를 위한 Microsoft에서 관리하는 키 옵션입니다. 이 암호화 방법은 데이터 암호 해독에 필요한 암호화 키와 서버 관리자를 분리하기 때문에 BitLocker에서 제공되지 않는 보호를 강화합니다. 암호화는 데이터에 직접 적용되며(논리 디스크 볼륨에서 암호화를 적용하는 BitLocker와는 달리) Exchange 서버에서 복사된 모든 고객 데이터는 암호화된 상태로 남아 있습니다.

Exchange Online 암호화의 범위는 서비스 암호화 내에 저장되어 있는 고객 Exchange Online. (비즈니스용 Skype 사서함 내에 거의 모든 사용자 생성 콘텐츠를 저장하므로 Exchange Online 사서함의 서비스 암호화 기능을 상속합니다Exchange Online.


## <a name="microsoft-teams"></a>Microsoft Teams

Teams TLS 및 MTLS를 사용하여 인스턴트 메시지를 암호화합니다. 모든 서버 간 트래픽에는 트래픽이 내부 네트워크로 제한되거나 내부 네트워크 경계를 넘든 관계없이 MTLS가 필요합니다.

이 표에는 이 문서에서 사용하는 프로토콜이 요약되어 Teams.

|**트래픽 유형**|**암호화된 메시지**|
|:-----|:-----|
|서버 대 서버|MTLS|
|클라이언트-서버(예: 인스턴트 메시징 및 현재 상태)|TLS|
|미디어 흐름(예: 미디어의 오디오 및 비디오 공유)|TLS|
|미디어의 오디오 및 비디오 공유|SRTP/TLS|
|신호|TLS|

#### <a name="media-encryption"></a>미디어 암호화

미디어 트래픽은 RTP 트래픽에 기밀성, 인증 및 재생 공격 보호를 제공하는 Real-Time 전송 프로토콜(RTP)의 프로필인 SRTP(Secure RTP)를 사용하여 암호화됩니다. SRTP는 보안 난수 생성기를 사용하여 생성된 세션 키를 사용하며 신호 TLS 채널을 사용하여 교환됩니다. 클라이언트-클라이언트 미디어 트래픽은 클라이언트-서버 연결 신호를 통해 협상되지만 클라이언트-클라이언트로 직접 진행할 때 SRTP를 사용하여 암호화됩니다.

Teams 통해 미디어 릴레이에 안전하게 액세스하기 위해 자격 증명 기반 토큰을 사용할 수 있습니다. 미디어 릴레이는 TLS 보안 채널을 통해 토큰을 교환합니다.

#### <a name="fips"></a>FIPS

Teams 암호화 키 교환에 FIPS(Federal Information Processing Standard) 호환 알고리즘을 사용합니다. FIPS 구현에 대한 자세한 내용은 [FIPS(Federal Information Processing Standard) 게시 140-2를 참조하세요.](/microsoft-365/compliance/offering-fips-140-2)
