---
title: ID 및 액세스 관리 개요
description: 2013의 ID 및 액세스 관리에 Microsoft 365
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
ms.openlocfilehash: 373c910f4c97f7f9ff89ea346c8dceef84dd6a07
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260839"
---
# <a name="identity-and-access-management-overview"></a>ID 및 액세스 관리 개요

## <a name="how-do-microsoft-online-services-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 온라인 서비스가 무단 또는 악의적인 액세스로부터 프로덕션 시스템을 보호하는 방법

Microsoft 온라인 서비스는 Microsoft 엔지니어가 고객 콘텐츠에 액세스하지 않고도 서비스를 운영할 수 있도록 디자인됩니다. 기본적으로 Microsoft 엔지니어는 고객 콘텐츠에 ZSA(Zero Standing Access)를 사용할 수 있으며 프로덕션 환경에 대한 권한 있는 액세스는 없습니다. Microsoft 온라인 서비스는 JIT(Just-In-Time), JEA(Just-Enough-Access) 모델을 사용하여 Microsoft 온라인 서비스를 지원하기 위해 이러한 액세스가 필요한 경우 서비스 팀 엔지니어에게 프로덕션 환경에 대한 임시 액세스 권한을 제공합니다. JIT 액세스 모델은 기존의 지속적인 관리 액세스를 엔지니어가 필요할 때 권한 있는 역할로 임시 승격을 요청하는 프로세스로 대체합니다.

프로덕션 서비스를 지원하기 위해 서비스 팀에 할당된 엔지니어가 ID 및 액세스 관리 솔루션을 통해 서비스 팀 계정에 대한 자격을 요청합니다. 자격 요청은 일련의 직원 검사를 트리거하여 엔지니어가 모든 클라우드 심사 요구 사항을 통과하고, 필요한 교육을 완료하고, 계정 생성 전에 적절한 관리 승인을 받았는지 확인합니다. 모든 자격 요구 사항을 충족한 후에만 요청된 환경에 대한 서비스팀 계정을 만들 수 있습니다. 서비스 팀 계정에 대한 자격을 유지하려면 담당자는 매년 역할 기반 교육을 진행하고 2년마다 다시 검사해야 합니다. 이러한 검사를 완료하거나 통과하지 못하면 자격이 자동으로 해지됩니다.

서비스 팀 계정은 상주 관리자 권한을 부여하거나 고객 콘텐츠에 대한 액세스 권한을 부여하지 않습니다. 엔지니어가 Microsoft 온라인 서비스를 지원하기 위해 추가 액세스 권한이 필요한 경우 Lockbox라는 액세스 관리 도구를 사용하여 필요한 리소스에 대한 임시 액세스 권한을 요청합니다. Lockbox는 할당된 작업을 완료하는 데 필요한 최소 권한, 리소스 및 시간에 대한 상승된 액세스를 제한합니다. 승인된 검토자가 JIT 액세스 요청을 승인하면 엔지니어에게 할당된 작업을 완료하는 데 필요한 권한만 있는 임시 계정에 부여됩니다. 이 임시 계정에는 다단계 인증이 필요하며 승인된 기간이 만료되면 자동으로 삭제됩니다.

JEA는 JIT 액세스 요청 시 자격 및 Lockbox 역할에 의해 적용됩니다. 엔지니어 자격 범위 내의 자산에 대한 액세스 요청만 수락 및 승인자에 전달됩니다. Lockbox는 허용되는 임계값을 초과하는 요청을 포함하여 엔지니어의 자격 및 Lockbox 역할의 범위를 벗어나는 JIT 요청을 자동으로 거부합니다.  

## <a name="how-do-microsoft-online-services-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Microsoft 온라인 서비스는 Lockbox와 함께 RBAC(역할 기반 액세스 제어)를 사용하여 최소 권한을 적용하는 방법

서비스 팀 계정은 상주 관리자 권한을 부여하거나 고객 콘텐츠에 대한 액세스 권한을 부여하지 않습니다. 제한된 관리자 권한에 대한 JIT 요청은 Lockbox를 통해 관리됩니다. Lockbox는 RBAC를 사용하여 엔지니어가 만들 수 있는 JIT 권한 상승 요청 유형을 제한하여 최소 권한을 적용하는 추가 보호 계층을 제공합니다. 또한 RBAC는 서비스 팀 계정을 적절한 역할로 제한하여 업무 분리를 강화하는 데 도움이 됩니다.
서비스를 지원하는 엔지니어에게는 역할에 따라 보안 그룹에 대한 구성원 자격이 부여됩니다. 보안 그룹의 구성원은 권한 있는 액세스 권한을 부여하지 않습니다. 대신, 보안 그룹에서는 엔지니어가 Lockbox를 사용하여 시스템 지원에 필요한 경우 JIT 권한 상승을 요청할 수 있습니다. 엔지니어가 할 수 있는 특정 JIT 요청은 보안 그룹 구성원 자격에 의해 제한됩니다.

## <a name="how-do-microsoft-online-services-handle-remote-access-to-production-systems"></a>Microsoft 온라인 서비스는 프로덕션 시스템에 대한 원격 액세스를 어떻게 처리하나요?

Microsoft 온라인 서비스 시스템 구성 요소는 운영 팀과 지리적으로 분리된 데이터 센터에 저장됩니다. 데이터 센터 직원은 Microsoft 온라인 서비스 시스템에 논리적으로 액세스할 수 없습니다. 따라서 Microsoft 서비스 팀 담당자는 원격 액세스를 통해 환경을 관리합니다. Microsoft 온라인 서비스를 지원하기 위해 원격 액세스가 필요한 서비스 팀 직원은 권한 있는 관리자의 승인 후에만 원격 액세스 권한을 부여받습니다. 모든 원격 액세스는 보안 원격 연결을 위해 FIPS 140-2 호환 TLS를 사용합니다.

Microsoft 온라인 서비스는 서비스 팀 원격 액세스를 위해 SAW(Secure Admin Workstation)를 사용하여 Microsoft 온라인 서비스 환경의 손상을 방지합니다. 이러한 Workstation은 USB 포트를 잠그고 Secure Admin Workstation에서 사용할 수 있는 소프트웨어를 환경 지원에 필요한 것으로 제한하는 등 프로덕션 데이터가 의도적으로 또는 의도하지 않은 손실되지 않도록 설계되었습니다. 보안 관리 Workstation은 Microsoft 엔지니어가 고객 데이터의 악의적 또는 부적당 손상을 감지하고 방지하기 위해 면밀하게 추적 및 모니터링합니다.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Customer Lockbox는 고객 콘텐츠에 대한 추가 보호 기능을 추가하는 방법

고객은 Customer Lockbox를 사용하도록 설정하여 콘텐츠에 액세스 제어 수준을 더 추가할 수 있습니다. 고객 콘텐츠에 대한 액세스 권한이 Lockbox 권한 상승 요청에 포함되는 경우 Customer Lockbox는 승인 워크플로의 마지막 단계로 고객의 승인을 요구합니다. 이 프로세스는 조직에서 이러한 요청을 승인하거나 거부할 수 있는 옵션을 제공하며 고객에게 직접 액세스 제어를 제공합니다. 고객이 고객 Lockbox 요청을 거부하면 요청된 콘텐츠에 대한 액세스가 거부됩니다. 고객이 특정 기간 내에 요청을 거부하거나 승인하지 않으면 Microsoft에서 고객 콘텐츠에 대한 액세스 권한을 얻지 않으면 요청이 자동으로 만료됩니다. 고객이 요청을 승인하면 문제 해결 작업을 완료하기 위해 할당된 시간이 만료되면 Microsoft의 고객 콘텐츠에 대한 임시 액세스가 자동으로 기록, 감사 및 해지됩니다.

## <a name="related-external-regulations--certifications"></a>인증을 위한 & 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하도록 정기적으로 감사됩니다. ID 및 액세스 제어와 관련된 컨트롤의 유효성을 검사하는 내용은 다음 표를 참조합니다.

### <a name="azure-and-dynamics-365"></a>Azure 및 Dynamics 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: 액세스 제어의 비즈니스 요구 사항 <br> A.9.2: 사용자 액세스 관리 <br> A.9.3: 사용자 책임 <br> A.9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A.15.1: 공급자 관계의 정보 보안 | 2020년 12월 2일 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: 액세스 제어의 비즈니스 요구 사항 <br> A.9.2: 사용자 액세스 관리 <br> A.9.3: 사용자 책임 <br> A.9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A.15.1: 공급자 관계의 정보 보안 | 2020년 12월 2일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | OA-2: 액세스 프로비전 <br> OA-7: JIT 액세스 <br> OA-21: 보안 관리 Workstations 및 MFA | 2021년 3월 31일 |

### <a name="office-365"></a>Office 365

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-3: 액세스 적용 <br> AC-5: 업무 분리 <br> AC-6: 최소 권한 <br> AC-17: 원격 액세스 | 2020년 9월 24일 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: 액세스 제어의 비즈니스 요구 사항 <br> A.9.2: 사용자 액세스 관리 <br> A.9.3: 사용자 책임 <br> A.9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A.15.1: 공급자 관계의 정보 보안 | 2021년 4월 20일 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한 있는 액세스 <br> CA-36: 원격 액세스 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2020년 12월 24일 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: 공유 계정 정책 <br> CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한 있는 액세스 <br> CA-36: 원격 액세스 <br> CA-53: 타사 모니터링 <br> CA-56: 고객 Lockbox 고객 승인 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2020년 12월 24일 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: 고객 Lockbox 요청 | 2020년 12월 24일 |