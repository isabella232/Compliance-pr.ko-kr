---
title: Microsoft 365의 기술 컨트롤
description: 이 문서에서는 Microsoft 365의 기술 제어를 위해 Microsoft에서 사용하는 도구 및 기술에 대한 개요를 제공합니다.
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fd23a1fdf949518ce3447d9db1bff7b6848d557c
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497372"
---
# <a name="technology-controls-in-microsoft-365"></a>Microsoft 365의 기술 컨트롤 

Microsoft는 여러 도구 및 기술을 사용하여 온라인 서비스의 고객 데이터에 대한 액세스를 제어, 관리 및 감사합니다. 이러한 설정은 Exchange Online, SharePoint Online, Lockbox 및 Customer Lockbox, 다단계 인증 등에서 적용됩니다. Yammer 엔터프라이즈 액세스 제어 에 설명된 Yammer [컨트롤을 사용하는지와 비슷합니다.](assurance-yammer-enterprise-access-controls.md)

Microsoft 365 엔지니어는 Microsoft 365 고객 데이터에 대한 액세스 권한이 없습니다. 엔지니어는 서비스 운영을 위한 고객 데이터에 액세스하기 전에 Microsoft 승인 프로세스를 거치야 합니다. 고객이 Exchange Online 및 SharePoint Online에 대한 고객 Lockbox 기능에 라이선스를 부여하는 경우 고객 데이터에 액세스하려면 고객 승인이 필요합니다. 승인되면 서비스별 관리 계정이 서비스 요청에 필요한 작업에 대한 Just-In-Time 액세스로 프로비전됩니다.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox 및 Customer Lockbox

드물지만 고객은 Microsoft 엔지니어에게 고객 콘텐츠를 노출하는 지원을 Microsoft에 요청할 수 있습니다. Exchange Online에 대한 액세스를 제어하기 위해 Microsoft는 Lockbox라는 액세스 제어 시스템을 사용 합니다. Microsoft 엔지니어가 Exchange Online 또는 SharePoint Online 시스템 또는 데이터에 액세스하기 전에 Lockbox를 사용하여 액세스 요청을 제출해야 합니다. Exchange Online 및 SharePoint Online에 대한 모든 서비스 요청은 Lockbox 시스템에서 처리됩니다. Lockbox와 Customer Lockbox를 모두 사용하여 승인된 모든 액세스는 고유한 사용자에 의해 추적할 수 있으며, 엔지니어는 고객 데이터 처리를 책임지게 됩니다.

> [!NOTE]
> Exchange Online에는 사용자 사서함에 저장된 비즈니스용 Skype 데이터가 포함됩니다. 비즈니스용 Skype 범위에는 Skype 모임 브로드캐스트 녹음/녹화 또는 사용자가 모임에 업로드한 콘텐츠가 포함되어 있지 않습니다. SharePoint Online에는 비즈니스용 OneDrive가 포함되어 있습니다.

Lockbox는 엔지니어에게 서비스 내에서 운영 및 관리 기능을 수행할 수 있는 권한을 부여하는 사용 권한 요청을 처리합니다. 엔지니어가 Lockbox를 통해 요청을 제출하고, 엔지니어가 고객 데이터에 액세스하려면 먼저 Microsoft 관리자가 요청을 승인해야 합니다. 관리자 승인 후 엔지니어는 고객 데이터에 대한 시간 제한 및 범위 제한 액세스 권한을 부여하여 고객 문제를 해결합니다.

Microsoft 365용 고객 Lockbox는 명시적 데이터 액세스 권한 부여를 위한 절차가 필요한 경우 규정 준수 의무를 충족하는 데 도움이 됩니다. 이는 FedRAMP 및 HIPAA와 같은 일부 준수 표준에 대한 요구 사항입니다. 고객 Lockbox는 Lockbox 승인 프로세스에 삽입하고 서비스 운영을 위해 Exchange Online 또는 SharePoint Online 콘텐츠에 대한 Microsoft 액세스 권한 부여를 제어할 수 있는 기능을 제공합니다.

드문 경우지만 Microsoft 서비스 엔지니어가 데이터에 액세스해야 하는 경우에는 문제를 해결하는 데 필요한 데이터와 제한된 시간 동안에만 액세스 권한을 부여합니다. 액세스 요청을 거부하면 Microsoft 엔지니어가 콘텐츠에 액세스할 수 있으며 서비스 작업을 완료할 수 없습니다. 요청을 승인하면 Microsoft 엔지니어가 모니터링 및 제한된 관리 인터페이스를 통해 콘텐츠에 대한 정시 액세스를 제한합니다.

지원 엔지니어가 수행한 작업은 감사 목적으로 기록되어 있으며 [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) 관리 활동 API 및 보안 및 준수 센터를 통해 액세스할 [수 있습니다.](https://protection.office.com/)

>[!NOTE]
> 고객 Lockbox는 추가 기능 [구매로 Microsoft 365 E5에서](https://products.office.com/business/office-365-enterprise-e5-business-software) 사용할 수 있습니다. 자세한 내용은 [Microsoft 365 Customer Lockbox Requests를 참조하세요.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Just-In-Time 액세스

Microsoft는 Microsoft 365에 JIT(Just-In-Time) 액세스 원칙을 사용하여 자격 증명 변조 위험 및 측면 공격을 완화합니다. JIT는 서비스에 대한 영구적 관리 액세스를 제거하고 권리 권한을 요구 시 해당 역할로 승격하는 기능을 대체합니다. 관리자의 영구 액세스 권한을 제거하면 필요할 때만 자격 증명을 사용할 수 있으며 자격 증명 도난 위험을 줄일 수 있습니다.

JIT 액세스 모델을 사용하려면 엔지니어가 제한된 기간 동안 관리자 권한 상승을 요청하여 관리 업무를 수행해야 합니다. 또한 엔지니어는 컴퓨터 생성 복잡한 암호로 만든 임시 계정을 사용하며 필요한 작업을 수행할 수 있도록 하는 역할만 부여합니다. 예를 들어 Lockbox에 의해 부여되는 관리 액세스는 시간 제한이 있으며, 액세스 권한이 부여되는 시간은 요청된 역할에 따라 결정됩니다. 엔지니어는 Lockbox 시스템에 대한 요청에 필요한 시간 액세스 기간을 지정합니다. Lockbox 시스템은 요청된 시간이 권한 상승에 허용되는 최대 시간을 초과하면 요청을 거부합니다. 만료 후 관리 액세스가 제거되고 임시 계정이 만료됩니다.

액세스 권한이 부여 및 승인되면 엔지니어는 인증 시스템에서 생성한 일회용 관리 암호를 받게 됩니다. 상승된 액세스 요청이 승인될 때마다 새 암호가 생성됩니다. 암호는 안전한 암호로 복사되어 Microsoft 회사 환경에 대한 엔지니어의 자격 증명과는 별개로, 승인된 상승된 액세스 세션에만 좋습니다.

## <a name="constrained-management-interfaces"></a>제한 관리 인터페이스

엔지니어는 두 가지 관리 인터페이스인 보안 TSG(터미널 서비스 게이트웨이)를 통한 원격 데스크톱 및 원격 PowerShell 관리 작업을 수행합니다. 이러한 관리 인터페이스 내에서 소프트웨어 정책 및 액세스 제어는 실행되는 응용 프로그램과 사용 가능한 명령 및 cmdlet에 상당한 제한을 적용합니다.

Microsoft 365 서버는 동시 세션을 서버당 서비스 팀 관리자 한 명으로 제한합니다. TSG는 사용자에 대해 단일 동시 세션만 허용하고 여러 세션을 허용하지 않습니다. TSG는 서버당 단일 세션을 사용하여 Microsoft 365 서비스 팀 관리자가 동시에 여러 서버에 연결할 수 있도록 하여 관리자가 업무를 효과적으로 수행할 수 있도록 합니다. 서비스 팀 관리자에게는 TSG 자체에 대한 권한이 없습니다. TSG는 MFA(다단계 인증) 및 암호화 요구 사항을 적용하는 데만 사용됩니다. 서비스 팀 관리자가 TSG를 통해 특정 서버에 연결하면 특정 서버는 관리자당 하나의 세션 제한을 적용합니다.

Microsoft 365 직원에 대한 사용 제한 및 연결 및 구성 요구 사항은 Active Directory 그룹 정책에 의해 설정됩니다. 이러한 정책에는 다음과 같은 특성이 포함됩니다.

- TSG는 [FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2의 유효성이 검사된 암호화만 사용합니다.
- 30분 동안 비활성 상태를 한 후 TSG 세션 연결이 끊어집니다.
- TSG 세션은 24시간 후에 자동으로 로그오프됩니다.

또한 TSG에 연결하려면 별도의 실제 스마트 카드와 엔지니어의 Microsoft 회사 자격 증명과는 별개인 계정을 사용하는 MFA가 필요합니다. 엔지니어는 다양한 플랫폼에 대해 서로 다른 스마트 카드를 발급하고 비밀 관리 플랫폼은 자격 증명의 보안 저장소를 보장합니다. TSG는 Active Directory 그룹 정책을 사용하여 원격 서버에 로그인할 수 있는 사용자, 허용되는 세션 수 및 유휴 시간 제한 설정을 제어합니다. 추가 정책은 허용되는 응용 프로그램에 대한 액세스를 제한하고 인터넷 액세스를 제한합니다.

Exchange Online에서는 특수하게 구성된 TSG를 사용하는 원격 액세스 외에도 서비스 엔지니어 작업 역할이 있는 사용자가 원격 PowerShell을 사용하여 프로덕션 서버의 특정 관리 기능에 액세스할 수 있습니다. 이렇게하려면 사용자에게 Microsoft 365 프로덕션 환경에 대한 읽기 전용(디버그) 액세스 권한을 부여해야 합니다. Lockbox 프로세스를 사용하여 TSG에 대해 권한 에스컬레이터를 사용하도록 설정한 방식과 동일하게 권한 에스컬레이터를 사용할 수 있습니다.

원격 액세스의 경우 각 데이터 센터에는 단일 액세스 지점 역할을 하는 부하 분산된 가상 IP가 있습니다. 사용 가능한 원격 PowerShell cmdlet은 인증 중에 얻은 액세스 클레임에 식별된 권한 수준을 기반으로 합니다. 이러한 cmdlet은 이 방법을 사용하여 연결하는 사용자가 액세스할 수 있는 유일한 관리 기능을 제공합니다. 원격 PowerShell은 엔지니어가 사용할 수 있는 명령 범위를 제한하며 Lockbox 프로세스를 통해 부여된 액세스 수준을 기반으로 합니다. 예를 들어 Exchange Online에서는 Get-Mailbox 수 있지만 Set-Mailbox 없습니다.
