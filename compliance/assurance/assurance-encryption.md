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
hideEdit: true
ms.openlocfilehash: 48fe5dd495dceb53b60cb83710566b63d09b80bf
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497221"
---
# <a name="encryption-and-key-management-overview"></a>암호화 및 키 관리 개요

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>암호화가 고객 콘텐츠를 보호하는 데 어떤 역할을 하나요?

대부분의 Microsoft 비즈니스 클라우드 서비스는 멀티텐트입니다. 즉, 고객 콘텐츠는 다른 고객의 경우와 동일한 실제 하드웨어에 저장될 수 있습니다. 고객 콘텐츠의 기밀성을 보호하기 위해 Microsoft 365는 사용 가능한 가장 강력하고 가장 안전한 암호화 프로토콜을 사용하여 미사용 및 전송되는 모든 데이터를 암호화합니다.

암호화는 강력한 액세스 제어 대신 사용할 수 없습니다. Microsoft 365의 ZSA(Zero Standing Access)에 대한 액세스 제어 정책은 Microsoft 직원의 무단 액세스로부터 고객 콘텐츠를 보호합니다. 암호화는 저장되는 모든 곳에서 고객 콘텐츠의 기밀성을 보호하고 Microsoft 365 시스템 간에 또는 Microsoft 365와 고객 간에 전송되는 동안 콘텐츠를 읽지 못하게 하여 액세스 제어를 보완합니다.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Microsoft 365는 미사용 데이터를 암호화하는 방법

Microsoft 365의 모든 고객 콘텐츠는 하나 이상의 암호화 형태로 보호됩니다. Microsoft 서버는 BitLocker를 사용하여 볼륨 수준에서 고객 콘텐츠가 포함된 디스크 드라이브를 암호화합니다. BitLocker에서 제공하는 암호화는 고객 콘텐츠가 포함된 디스크에 무단으로 물리적으로 액세스할 수 있는 다른 프로세스 또는 제어(예: 하드웨어의 액세스 제어 또는 재생)에서 경과되는 경우 고객 콘텐츠를 보호합니다.

Exchange Online, Microsoft Teams, SharePoint Online 및 비즈니스용 OneDrive에서도 응용 프로그램 계층의 서비스 암호화를 사용하여 고객 콘텐츠를 암호화합니다. 서비스 암호화는 강력한 암호화 보호를 통해 권한 보호 및 관리 기능을 제공합니다. 또한 Windows 운영 체제와 해당 운영 체제에서 저장하거나 처리한 고객 데이터를 분리할 수 있습니다.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Microsoft 365는 전송되는 데이터를 암호화하는 방법

Microsoft 365 제품 및 서비스는 TLS와 같은 강력한 전송 프로토콜을 사용하여 권한이 없는 사용자가 네트워크를 통해 이동하는 동안 고객 데이터를 도청하지 못하게 합니다. 전송되는 데이터의 예로는 배달 중인 메일 메시지, 온라인 모임에서 진행되는 대화 또는 데이터 센터 간에 복제되는 파일이 있습니다.

Microsoft 365에서 데이터는 사용자의 장치가 Microsoft 서버와 통신하거나 Microsoft 서버가 다른 서버와 통신할 때마다 '전송 중'으로 간주됩니다. Exchange Online, SharePoint Online, Microsoft Teams 및 Office Online은 모두 TLS를 사용하여 전송되는 동안 데이터를 기밀로 유지하도록 합니다.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Microsoft 365는 암호화에 사용되는 키를 어떻게 관리하나요?

강력한 암호화는 데이터를 암호화하는 데 사용되는 키만큼 안전합니다. Microsoft는 자체 보안 인증서를 사용하여 전송되는 데이터에 대한 TLS 연결을 암호화합니다. 미사용 데이터의 경우 BitLocker로 보호되는 볼륨은 볼륨 마스터 키로 암호화되는 전체 볼륨 암호화 키로 암호화되며, 이 키는 서버의 TPM(신뢰할 수 있는 플랫폼 모듈)에 바인딩됩니다. BitLocker는 FIPS 호환 알고리즘을 사용하여 암호화 키가 유선으로 저장되거나 유선으로 전송되지 않도록 합니다.

서비스 암호화는 Exchange Online, Microsoft Teams, SharePoint Online 및 비즈니스용 OneDrive에서 고객 저장 데이터를 위한 추가 암호화 계층을 제공합니다. 서비스 암호화는 고객에게 암호화 키 관리에 대한 두 가지 옵션( Microsoft 관리 키 또는 고객 키)을 제공합니다. Microsoft 관리 키를 사용하는 경우 Microsoft 365 서비스는 서비스 암호화에 사용되는 루트 키를 자동으로 생성하고 안전하게 저장합니다.

자체 루트 암호화 키를 제어해야 하는 요구 사항이 있는 고객은 고객 키로 서비스 암호화를 활용할 수 있습니다. 고객은 고객 키를 사용하여 자체 암호화 키를 생성할 수 있으며, 이러한 키는 HSM(On-프레미스 하드웨어 서비스 모듈) 또는 AKV(Azure Key Vault)를 사용하여 생성할 수 있습니다. 고객 루트 키는 AKV에 저장되며 고객 사서함 데이터 또는 파일을 암호화하는 키사인 중 하나의 루트로 사용할 수 있습니다. 고객 루트 키는 데이터 암호화를 위한 Microsoft 365 서비스 코드에서 간접적으로만 액세스할 수 있으며 Microsoft 직원은 직접 액세스할 수 없습니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 암호화 및 키 관리와 관련된 컨트롤의 유효성 검사는 다음 표를 참조하세요.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: 전송 기밀성 및 무결성 <br> SC-13: 암호화 사용 <br> SC-28: 미사용 정보 보호 <br>  | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 암호화 컨트롤 <br> A.18.1.5: 암호화 컨트롤 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 암호화 컨트롤 <br> A.18.1.5: 암호화 컨트롤 | 2020년 2월 22일 |
| [ISO 27018(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: 공용 데이터 전송 네트워크를 통해 전송된 PII 암호화 | 2020년 2월 22일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: 데이터 전송 암호화 <br> CA-54: 미사용 데이터 암호화 <br> CA-62: 고객 키 사서함 암호화 <br> CA-63: 고객 키 데이터 지우기 <br> CA-64: 고객 키 | 2020년 12월 24일 |
| [SOC 3(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: 고객 암호화 키 <br> CUEC-17: 고객 키 자격 증명 모음 <br>  CUEC-18: 고객 키 회전| 2020년 12월 24일 |
