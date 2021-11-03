---
title: Microsoft 365 엔지니어 액세스 제어
description: 서비스 엔지니어 액세스 Microsoft 365 아키텍처에 대한 개요입니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678475"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Microsoft 365 엔지니어 액세스 제어

ZSA(Zero Standing Access)는 Microsoft 서비스 팀 직원이 Microsoft 365 환경이나 고객 데이터에 대한 권한이 없습니다. Microsoft 서비스 팀 구성원이 어떤 이유로든 서비스를 업데이트하거나 고객 데이터에 액세스하려는 경우 요구를 정당화하는 요청을 제출하고 승인된 관리자의 승인을 수신해야 합니다. 대규모로, Microsoft 365 서비스를 유지 관리하는 데 필요한 액세스를 수동으로 제공하고 제거하는 것은 타당하지 않습니다. 따라서 Microsoft는 필요한 경우 권한 있는 액세스를 관리하는 자동화된 솔루션을 개발했습니다.

## <a name="lockbox"></a>Lockbox

Microsoft 365 시스템 및 고객 데이터에 대한 모든 액세스는 JIT(Just-In-Time) 및 JEA(Just-Enough-Access) 모델을 사용하여 서비스 엔지니어에게 지정된 Microsoft 365 서비스 및 데이터에 대한 임시 액세스 권한을 제공하는 액세스 제어 시스템인 Lockbox를 통해 브로커됩니다. 또한 모든 요청 및 작업은 감사를 위해 기록되어 있으며 Office 365 관리 활동 API 및 보안 및 준수 [센터를](/office/office-365-management-api/get-started-with-office-365-management-apis) 사용하여 액세스할 [수 있습니다.](https://protection.office.com/)

Microsoft 서비스 엔지니어가 모든 Microsoft 365 시스템에 연결하거나 고객 데이터에 액세스하려면 먼저 Lockbox를 통해 액세스 요청을 제출해야 합니다. 이 요청은 특정 기준이 충족된 경우만 승인할 수 있습니다.

- 서비스 엔지니어가 서비스 팀 계정에 대한 자격 [요구 사항을 충족합니다.](assurance-microsoft-365-account-management.md)
- 요청의 작업과 연결된 Lockbox 역할에 속합니다.
- 요청된 액세스 시간이 허용되는 최대 시간을 초과하지 않습니다.
- 정당한 업무 정당성,
- 액세스하고자 하는 요청된 자원이 작업 범위 내에 있으며,
- 관리자 승인을 받게 됩니다.

Lockbox에서 모든 조건을 충족하고 확인하면 요청된 특정 작업을 수행할 수 있는 임시 액세스 권한이 부여됩니다. 요청 시간이 경과하면 액세스가 해지됩니다.

![Lockbox 액세스 프로세스.](../media/assurance-lockbox-process.png)

또한 고객 라이선스를 취득하고 [고객 Lockbox](/microsoft-365/compliance/customer-lockbox-requests) 기능을 사용할 수 있도록 설정한 경우 Microsoft 서비스 엔지니어가 고객 데이터에 액세스하려고 시도하는 시도는 고객 테넌트의 관리자가 추가로 승인해야 합니다. 고객 데이터에 액세스해야 하는 필요성은 고객과 Microsoft 둘 다에서 발생할 수 있습니다. 예를 들어 고객이 발생한 인시던트는 문제를 해결하기 위해 또는 Microsoft가 특정 업데이트를 적용하기 위해 데이터 액세스가 필요한 경우 데이터에 액세스해야 할 수 있습니다.

![고객 Lockbox 액세스 프로세스.](../media/assurance-customer-lockbox-process.png)

고객은 고객 Lockbox 요청을 시작하는 도구가 없습니다. 고객 Lockbox 요청이 발생해야 하는 티켓을 Microsoft에 제출해야 합니다. Microsoft 서비스 엔지니어가 제기한 고객 Lockbox 요청은 Microsoft 관리자 및 고객 테넌트의 권한이 부여된 관리자가 승인해야 합니다.

### <a name="lockbox-roles"></a>Lockbox 역할

업무 분리 및 최소 권한 원칙을 적용하려면 서비스 엔지니어가 팀의 역할에 해당하는 Lockbox 역할에 속해야 합니다. Lockbox 역할은 ID 관리 도구 내에서 관리되고 서비스 팀 구성원이 Lockbox 요청 프로세스를 통해 승인할 수 있는 권한 및 작업을 정의합니다. 서비스 팀 직원은 Lockbox 역할의 구성원이 되어야 함을 요청하고 관리자 승인을 받을 수 있습니다. 승인되면 직원의 서비스 팀 계정이 AD(Active Directory) 및 AZURE ACTIVE DIRECTORY(보안 그룹)에 AAD.

## <a name="constrained-management-interfaces"></a>제한 관리 인터페이스

서비스 엔지니어는 두 가지 관리 인터페이스를 사용하여 관리 작업을 수행합니다. 보안 TSG(터미널 서비스 게이트웨이) 및 원격 PowerShell을 통해 SAW(Secure Access Workstation)에서 원격 데스크톱을 수행합니다. 이러한 관리 인터페이스 내에서 승인된 Lockbox 요청 및 소프트웨어 정책에 따라 액세스 제어는 실행되는 응용 프로그램과 사용 가능한 명령 및 cmdlet에 상당한 제한을 적용합니다.

## <a name="remote-desktop"></a>원격 데스크톱

원격 데스크톱을 사용하여 서비스를 관리하는 서비스 팀 구성원은 이 사용 사례를 위해 Microsoft에서 관리하는 특별히 디자인되고 제조된 랩톱인 SAW에서 연결해야 합니다. 공급 업체와 협력하여 짧고 안전한 공급망을 만들어 SAW를 구축합니다. SAW는 정의된 관리 작업에 필요한 기능을 제외한 모든 기능을 제한하도록 구성된 강화된 운영 체제를 사용합니다. 이러한 제한에는 모든 USB 포트의 비활성화, 엄격한 응용 프로그램 액세스 목록, 전자 메일 액세스 제거, 인터넷 검색 제한, 비활성 화면 보호 잠금 적용이 포함됩니다. Microsoft 액세스 제어 시스템은 SAW 컴퓨터를 주기적으로 검사하여 최신 보안 컨트롤을 준수하는지 확인하며, 규격이 아닌 것으로 확인되면 컴퓨터를 자동으로 사용하지 않도록 설정합니다.

서비스 엔지니어는 한 번의 TSG에만 연결할 수 있으며 여러 세션은 허용되지 않습니다. 그러나 TSG를 사용하면 Microsoft 365 서비스 팀 관리자가 각각 하나의 동시 세션만 있는 여러 서버에 연결할 수 있으므로 관리자가 업무를 효과적으로 수행할 수 있습니다. 서비스 팀 관리자에게는 TSG 자체에 대한 권한이 없습니다. TSG는 MFA(다단계 인증) 및 암호화 요구 사항을 적용하는 데만 사용됩니다. 서비스 팀 관리자가 TSG를 통해 특정 서버에 연결하면 특정 서버는 관리자당 하나의 세션 제한을 적용합니다.

Active Directory 그룹 정책에 따라 Microsoft 365 직원에 대한 사용 제한, 연결 및 구성 요구 사항이 설정됩니다. 이러한 정책에는 다음과 같은 TSG 특성이 포함됩니다.

- [FIPS 140-2](/compliance/regulatory/offering-FIPS-140-2) 유효성이 검사된 암호화만 사용
- 15분 동안 비활성화한 후 세션 연결이 끊어집니다.
- 세션이 24시간 후에 자동으로 로그오프됩니다.

TSG에 연결하려면 별도의 실제 스마트 카드를 사용하는 MFA도 필요합니다. 서비스 엔지니어는 다양한 플랫폼에 대해 서로 다른 스마트 카드를 발급하고 비밀 관리 플랫폼은 자격 증명의 보안 저장소를 보장합니다. TSG는 Active Directory 그룹 정책을 사용하여 원격 서버에 로그인할 수 있는 사용자, 허용되는 세션 수 및 유휴 시간 제한 설정을 제어합니다.

## <a name="remote-powershell"></a>Remote PowerShell

특수하게 구성된 TSG를 사용하는 원격 액세스 외에도 서비스 엔지니어 Operations Lockbox 역할이 있는 서비스 팀 직원은 원격 PowerShell을 사용하여 프로덕션 서버의 특정 관리 기능에 액세스할 수 있습니다. 이 액세스를 사용하려면 사용자에게 프로덕션 환경에 대한 읽기 전용(디버그) 액세스 권한을 Microsoft 365 합니다. Lockbox 프로세스를 사용하여 TSG에 대해 권한 에스컬레이터를 사용하도록 설정한 방식과 동일하게 권한 에스컬레이터를 사용할 수 있습니다.

원격 액세스의 경우 각 데이터 센터에는 단일 액세스 지점 역할을 하는 부하 분산된 가상 IP가 있습니다. 사용 가능한 원격 PowerShell cmdlet은 인증 중에 얻은 액세스 클레임에 식별된 권한 수준을 기반으로 합니다. 이러한 cmdlet은 이 방법을 사용하여 연결하는 사용자가 액세스할 수 있는 유일한 관리 기능을 제공합니다. 원격 PowerShell은 엔지니어가 사용할 수 있는 명령 범위를 제한하며 Lockbox 프로세스를 통해 부여된 액세스 수준을 기반으로 합니다. 예를 들어 Exchange Online 경우 Get-Mailbox cmdlet을 사용할 수 있지만 Set-Mailbox cmdlet은 사용할 수 없습니다.

## <a name="resources"></a>리소스

- [Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft 사전 고용 심사](assurance-pre-employment-screening.md)[Microsoft 클라우드 배경 검사](assurance-cloud-background-check.md)
