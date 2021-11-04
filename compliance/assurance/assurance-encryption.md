---
title: 암호화 및 키 관리 개요
description: 암호화 및 키 관리에 대해 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f5ba22f53b0f40983bd0f76d2a9ffc2061c2c30e
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/04/2021
ms.locfileid: "60780104"
---
# <a name="encryption-and-key-management-overview"></a>암호화 및 키 관리 개요

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>암호화가 고객 콘텐츠를 보호하는 데 어떤 역할을 하나요?

대부분의 Microsoft 비즈니스 클라우드 서비스는 다중 테넌트입니다. 즉, 고객 콘텐츠는 다른 고객과 동일한 실제 하드웨어에 저장될 수 있습니다. 고객 콘텐츠의 기밀성을 보호하기 위해 Microsoft 온라인 서비스는 사용 가능한 가장 강력하고 가장 안전한 암호화 프로토콜을 사용하여 미사용 및 전송되는 모든 데이터를 암호화합니다.

암호화는 강력한 액세스 제어 대신 사용할 수 없습니다. Microsoft의 ZSA(Zero Standing Access)에 대한 액세스 제어 정책은 Microsoft 직원의 무단 액세스로부터 고객 콘텐츠를 보호합니다. 암호화는 저장되는 모든 곳에서 고객 콘텐츠의 기밀성을 보호하고 Microsoft 온라인 서비스 시스템 간에 또는 Microsoft 온라인 서비스와 고객 간에 전송되는 동안 콘텐츠를 읽지 못하게 하여 액세스 제어를 보완합니다.

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>Microsoft 온라인 서비스는 미사용 데이터를 암호화하는 방법

Microsoft 온라인 서비스의 모든 고객 콘텐츠는 하나 이상의 암호화 형태로 보호됩니다. Microsoft 서버는 BitLocker를 사용하여 볼륨 수준에서 고객 콘텐츠가 포함된 디스크 드라이브를 암호화합니다. BitLocker에서 제공하는 암호화는 고객 콘텐츠가 포함된 디스크에 무단으로 물리적으로 액세스할 수 있는 다른 프로세스나 제어(예: 하드웨어의 액세스 제어 또는 재생)에 경과가 있을 경우 고객 콘텐츠를 보호합니다.

Microsoft 온라인 서비스는 볼륨 수준 암호화 외에도 응용 프로그램 계층의 서비스 암호화를 사용하여 고객 콘텐츠를 암호화합니다. 서비스 암호화는 강력한 암호화 보호를 통해 권한 보호 및 관리 기능을 제공합니다. 또한 이러한 운영 체제에 Windows 고객 데이터와 이러한 운영 체제가 저장하거나 처리한 고객 데이터를 구분할 수 있습니다.

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>Microsoft 온라인 서비스는 전송되는 데이터를 암호화하는 방법

Microsoft 온라인 서비스는 TLS와 같은 강력한 전송 프로토콜을 사용하여 권한이 없는 사용자가 네트워크를 통해 이동하는 동안 고객 데이터를 도청하지 못하게 합니다. 전송되는 데이터의 예로는 배달 중인 메일 메시지, 온라인 모임에서 진행되는 대화 또는 데이터 센터 간에 복제되는 파일이 있습니다.

Microsoft 온라인 서비스의 경우 사용자의 장치가 Microsoft 서버와 통신하거나 Microsoft 서버가 다른 서버와 통신할 때마다 데이터가 '전송 중'으로 간주됩니다.

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>Microsoft 온라인 서비스는 암호화에 사용되는 키를 어떻게 관리하나요?

강력한 암호화는 데이터를 암호화하는 데 사용되는 키만큼 안전합니다. Microsoft는 자체 보안 인증서를 사용하여 전송되는 데이터에 대한 TLS 연결을 암호화합니다. 미사용 데이터의 경우 BitLocker로 보호되는 볼륨은 볼륨 마스터 키로 암호화되는 전체 볼륨 암호화 키로 암호화되며, 이 키는 서버의 TPM(신뢰할 수 있는 플랫폼 모듈)에 바인딩됩니다. BitLocker는 FIPS 호환 알고리즘을 사용하여 암호화 키가 유선으로 저장되거나 유선으로 전송되지 않도록 합니다.

서비스 암호화는 고객에게 암호화 키 관리에 대한 두 가지 옵션( Microsoft 관리 키 또는 고객 키)을 제공하는 고객 데이터 저장을 위한 또 다른 암호화 계층을 제공합니다. Microsoft에서 관리하는 키를 사용하는 경우 Microsoft 온라인 서비스는 서비스 암호화에 사용되는 루트 키를 자동으로 생성하고 안전하게 저장합니다.

자체 루트 암호화 키를 제어해야 하는 요구 사항이 있는 고객은 고객 키와 함께 서비스 암호화를 사용할 수 있습니다. 고객은 고객 키를 사용하여 자체 암호화 키를 생성할 수 있으며, 이러한 키는 HSM(On-프레미스 하드웨어 서비스 모듈) 또는 AKV(Azure Key Vault)를 사용하여 생성할 수 있습니다. 고객 루트 키는 AKV에 저장되며 고객 사서함 데이터 또는 파일을 암호화하는 키사인 중 하나의 루트로 사용할 수 있습니다. 고객 루트 키는 데이터 암호화를 위해 Microsoft 온라인 서비스 코드에서 간접적으로만 액세스할 수 있으며 Microsoft 직원은 직접 액세스할 수 없습니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. 암호화 및 키 관리와 관련된 컨트롤의 유효성 검사는 다음 표를 참조하세요.

### <a name="azure-and-dynamics-365"></a>Azure 및 Dynamics 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 암호화 컨트롤 <br> A.18.1.5: 암호화 컨트롤 | 2020년 12월 2일 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 암호화 컨트롤 <br> A.18.1.5: 암호화 컨트롤 | 2020년 12월 2일 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: 공용 데이터 전송 네트워크를 통해 전송된 PII 암호화 | 2020년 12월 2일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: 암호화 인증서 및 키의 보안 저장소 <br> DS-2: 고객 데이터가 전송 중으로 암호화됩니다. <br> DS-3: 전송 중 암호화된 Azure 구성 요소의 내부 통신 <br> DS-4: 암호화 제어 및 절차 | 2021년 3월 31일 |

### <a name="office-365"></a>Office 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: 전송 기밀성 및 무결성 <br> SC-13: 암호화 사용 <br> SC-28: 미사용 정보 보호 <br>  | 2020년 9월 24일 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: 암호화 컨트롤 <br> A.18.1.5: 암호화 컨트롤 | 2021년 4월 20일 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: 공용 데이터 전송 네트워크를 통해 전송된 PII 암호화 | 2021년 4월 20일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: 데이터 전송 암호화 <br> CA-54: 미사용 데이터 암호화 <br> CA-62: 고객 키 사서함 암호화 <br> CA-63: 고객 키 데이터 지우기 <br> CA-64: 고객 키 | 2020년 12월 24일 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: 고객 암호화 키 <br> CUEC-17: 고객 키 자격 증명 모음 <br>  CUEC-18: 고객 키 회전| 2020년 12월 24일 |
