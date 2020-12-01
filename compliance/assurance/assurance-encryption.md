---
title: 암호화 및 키 관리 개요
description: Microsoft 365의 암호화 및 키 관리에 대해 자세히 알아보기
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508200"
---
# <a name="encryption-and-key-management-overview"></a>암호화 및 키 관리 개요

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>고객이 콘텐츠를 보호 하기 위해 암호화가 수행 하는 역할은 무엇입니까?

대부분의 Microsoft business cloud services는 다중 테 넌 트 이며, 고객 콘텐츠는 다른 고객과 동일한 실제 하드웨어에 저장 될 수 있습니다. 고객 콘텐츠의 기밀성을 보호 하기 위해 Microsoft 365는 사용 가능한 가장 강력 하 고 안전한 암호화 프로토콜 중 일부와 함께 rest의 모든 데이터를 암호화 하 고 전송 합니다.

암호화는 강력한 액세스 제어를 대신할 수 없습니다. Microsoft 365의 액세스 제어 정책 (ZSA)은 Microsoft 직원이 무단으로 액세스 하지 못하도록 고객 콘텐츠를 보호 합니다. 암호화는 고객 콘텐츠가 저장 되는 위치를 보호 하 고 365 Microsoft 365 및 고객 간에 전송 되는 동안 콘텐츠를 읽지 못하도록 차단 하 여 액세스 제어를 보완 합니다.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Microsoft 365에서 rest 데이터를 암호화 하는 방법

Microsoft 365의 모든 고객 콘텐츠는 하나 이상의 암호화 형식으로 보호 됩니다. Microsoft 서버는 BitLocker를 사용 하 여 볼륨 수준에서 고객 콘텐츠가 포함 된 디스크 드라이브를 암호화 합니다. BitLocker에서 제공 하는 암호화는 고객 콘텐츠가 포함 된 디스크에 대 한 무단 물리적 액세스를 유발할 수 있는 다른 프로세스나 컨트롤 (예: 액세스 제어 또는 하드웨어 재활용)에 lapses 경우 고객 콘텐츠를 보호 합니다.

Exchange Online, Microsoft 팀, SharePoint Online 및 비즈니스용 OneDrive는 응용 프로그램 계층에서 서비스 암호화를 사용 하 여 고객 콘텐츠를 암호화 하기도 합니다. 서비스 암호화는 강력한 암호화 보호에 대 한 권한 보호 및 관리 기능을 제공 합니다. 또한 Windows 운영 체제와 이러한 운영 체제에 의해 저장 되거나 처리 되는 고객 데이터를 분리할 수 있습니다.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Microsoft 365에서 전송 되는 데이터를 암호화 하는 방법

Microsoft 365 제품 및 서비스는 TLS와 같은 강력한 전송 프로토콜을 사용 하 여 인증 되지 않은 사람이 네트워크를 통해 이동 하는 동안 고객 데이터를 도청 하지 못하도록 합니다. 전송 중인 데이터의 예로는 배달 중이거나, 온라인 모임에서 대화를 수행 하는 중이거나, 데이터 센터 간에 복제 되는 파일 등이 포함 된 메일 메시지를 들 수 있습니다.

Microsoft 365에서는 사용자의 장치가 Microsoft 서버와 통신 하거나 Microsoft 서버가 다른 서버와 통신 하는 경우에 데이터가 ' 전송 중 '으로 간주 됩니다. Exchange Online, SharePoint Online, Microsoft 팀 및 Office Online 모두 TLS를 사용 하 여 전송 중에 데이터가 기밀로 유지 되도록 합니다.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Microsoft 365에서 암호화에 사용 되는 키를 관리 하는 방법

강력한 암호화는 데이터를 암호화 하는 데 사용 되는 키 만큼 안전 합니다. Microsoft는 자체 보안 인증서를 사용 하 여 전송 데이터에 대 한 TLS 연결을 암호화 합니다. 휴지 상태의 데이터에 대 한 BitLocker로 보호 된 볼륨은 볼륨 마스터 키로 암호화 되는 전체 볼륨 암호화 키를 사용 하 여 암호화 되며,이 키는 차례로 서버의 TPM (신뢰할 수 있는 플랫폼 모듈)에 바인딩됩니다. BitLocker는 FIPS 호환 알고리즘을 사용 하 여 암호화 키가 전혀 저장 되지 않거나 네트워크를 통해 전송 되지 않도록 합니다.

서비스 암호화 Exchange Online, Microsoft 팀, SharePoint Online 및 비즈니스용 OneDrive에서 rest (고객 데이터)에 대 한 추가 암호화 계층을 제공 합니다. 서비스 암호화에서는 고객에 게 암호화 키 관리에 대 한 두 가지 옵션 (Microsoft 관리 키 또는 고객 키)을 제공 합니다. Microsoft 관리 키를 사용 하는 경우 Microsoft 365 서비스는 서비스 암호화에 사용 되는 루트 키를 자동으로 생성 하 고 안전 하 게 저장 합니다.

자체 루트 암호화 키를 제어 하기 위한 요구 사항이 있는 고객은 고객 키를 통해 서비스 암호화를 활용할 수 있습니다. 고객 키를 사용 하 여 고객은 온-프레미스 HSM (하드웨어 서비스 모듈) 또는 AKV (Azure Key Vault)를 사용 하 여 자체 암호화 키를 생성할 수 있습니다. 고객 루트 키는 AKV에 저장 되며, 사용자 사서함 데이터 나 파일을 암호화 하는 keychains 중 하나의 루트로 사용 될 수 있습니다. 고객 루트 키는 데이터 암호화를 위해 Microsoft 365 서비스 코드에서 간접적 으로만 액세스할 수 있으며 Microsoft 직원이 직접 액세스할 수 없습니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 암호화 및 키 관리와 관련 된 컨트롤의 유효성 검사에 대해서는 다음 표를 참조 하십시오.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: 전송 기밀성 및 무결성 <br> SC-13: 암호화 사용 <br> SC-28: 휴지 시점의 정보 보호 <br>  | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 10.1: 암호화 컨트롤 <br> A. 18.1.5: 암호화 컨트롤 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 10.1: 암호화 컨트롤 <br> A. 18.1.5: 암호화 컨트롤 | 2020년 2월 22일 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 11.6: 공용 데이터 전송 네트워크를 통해 전송 되는 PII 암호화 | 2020년 2월 22일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: 데이터 전송 암호화 <br> CA-54: 휴지 데이터 암호화 <br> CA-62: 고객 키 사서함 암호화 <br> CA-63: 고객 키 데이터 삭제 <br> CA-64: 고객 키 | 2019년 9월 30일 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | 개인 EC-16: 고객 암호화 키 <br> \ EC-17: 고객 키 자격 증명 모음 <br>  \ EC-18: 고객 키 순환| 2019년 9월 30일 |
