---
title: ID 및 액세스 관리 개요
description: Microsoft 365의 ID 및 액세스 관리에 대해 자세히
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
ms.openlocfilehash: c07801fe5ef571ddb4c9efcbfe04a7b3e5faedb6
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787477"
---
# <a name="identity-and-access-management-overview"></a>ID 및 액세스 관리 개요

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365는 무단 또는 악의적인 액세스로부터 프로덕션 시스템을 어떻게 보호하나요?

Microsoft 365는 Microsoft 엔지니어가 고객 콘텐츠에 액세스하지 않고도 서비스를 운영할 수 있도록 디자인됩니다. 기본적으로 Microsoft 365 엔지니어는 고객 콘텐츠에 대한 ZSA(Zero Standing Access)를 사용할 수 있으며 프로덕션 환경에 대한 권한 있는 액세스는 없습니다. Microsoft 365는 JIT(Just-In-Time), JEA(Just-Enough-Access) 모델을 사용하여 Microsoft 365를 지원하기 위해 이러한 액세스가 필요한 경우 서비스 팀 엔지니어에게 프로덕션 환경에 대한 임시 액세스 권한을 제공합니다. JIT 액세스 모델은 기존의 영구적 관리 액세스를 엔지니어가 필요한 경우 권한 있는 역할로 임시 권한 상승을 요청하는 프로세스로 대체합니다.

프로덕션 서비스 요청을 지원하기 위해 서비스 팀에 할당된 엔지니어는 IDM(ID 관리 도구)을 통해 서비스 팀 계정에 대한 자격을 요청합니다. 자격 요청은 일련의 직원 검사를 트리거하여 엔지니어가 모든 클라우드 심사 요구 사항을 통과하고, 필요한 교육을 완료하고, 계정 생성 전에 적절한 관리 승인을 받았는지 확인합니다. 모든 자격 요구 사항을 충족해야만 요청된 환경에 대해 서비스 팀 계정을 만들 수 있습니다.

서비스 팀 계정은 상주 관리자 권한을 부여하거나 고객 콘텐츠에 대한 액세스 권한을 부여하지 않습니다. 엔지니어가 Microsoft 365 서비스를 지원하기 위해 추가 액세스 권한이 필요한 경우 Lockbox라는 액세스 관리 도구를 사용하여 필요한 리소스에 대한 임시 액세스 권한을 요청합니다. Lockbox는 할당된 작업을 완료하는 데 필요한 최소 권한, 자원 및 시간으로 높은 액세스 권한을 제한합니다. 승인된 검토자가 JIT 액세스 요청을 승인하면 엔지니어에게 할당된 작업을 완료하는 데 필요한 권한만 있는 임시 계정이 부여됩니다. 이 임시 계정에는 다단계 인증이 필요하며 승인된 기간이 만료되면 자동으로 삭제됩니다.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365는 프로덕션 시스템에 대한 원격 액세스를 어떻게 처리하나요?

Microsoft 365 시스템 구성 요소는 운영 팀과 지리적으로 분리된 데이터 센터에 저장됩니다. 데이터 센터 직원은 Microsoft 365 시스템에 논리적으로 액세스할 수 없습니다. 따라서 Microsoft 365 서비스 팀 담당자는 원격 액세스를 통해 환경을 관리합니다. Microsoft 365를 지원하기 위해 원격 액세스가 필요한 서비스 팀 직원은 권한 있는 관리자의 승인 후에만 원격 액세스 권한을 부여받습니다. 모든 원격 액세스는 보안 원격 연결에 FIPS 140-2 호환 TLS를 사용 합니다.

Microsoft 365는 서비스 팀 원격 액세스를 위해 SAW(Secure Admin Workstations)를 사용하여 Microsoft 365 환경의 손상을 방지합니다. 이러한 Workstations는 USB 포트를 잠그고 SAW에서 사용할 수 있는 소프트웨어를 환경 지원에 필요한 것으로 제한하는 등 의도적 또는 의도하지 않은 프로덕션 데이터 손실을 방지하도록 특별히 설계되었습니다. SAW는 Microsoft 엔지니어가 고객 데이터의 악의적 또는 부수적인 손상을 감지하고 방지하기 위해 면밀하게 추적 및 모니터링됩니다.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Customer Lockbox는 고객 콘텐츠에 대해 추가 보호 기능을 추가하는 방법

고객은 고객 Lockbox를 사용하도록 설정하여 콘텐츠에 액세스 제어 수준을 더 추가할 수 있습니다. Lockbox 권한 상승 요청에 고객 콘텐츠 액세스가 포함되는 경우 고객 Lockbox는 승인 워크플로의 마지막 단계로 고객의 승인을 요구합니다. 이렇게 하면 조직에서 이러한 요청을 승인하거나 거부할 수 있으며 고객에게 직접 액세스 제어를 제공합니다. 고객이 고객 Lockbox 요청을 거부하면 요청된 콘텐츠에 대한 액세스가 거부됩니다. 고객이 특정 기간 내에 요청을 거부하거나 승인하지 않으면 Microsoft에서 고객 콘텐츠에 대한 액세스 권한을 얻지 못하면 요청이 자동으로 만료됩니다. 고객이 요청을 승인하면 문제 해결 작업을 완료하기 위해 할당된 시간이 만료되면 Microsoft의 고객 콘텐츠에 대한 임시 액세스가 자동으로 기록, 감사 가능 및 해지됩니다.

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. ID 및 액세스 제어와 관련된 컨트롤의 유효성을 검사하기 위해 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-3: 액세스 적용 <br> AC-5: 업무 분리 <br> AC-6: 최소 권한 <br> AC-17: 원격 액세스 | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: 액세스 제어의 비즈니스 요구 사항 <br> A.9.2: 사용자 액세스 관리 <br> A.9.3: 사용자 책임 <br> A.9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A.15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: 사용자 액세스 관리 <br> A.9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A.15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한이 부여된 액세스 <br> CA-36: 원격 액세스 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: 공유 계정 정책 <br> CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한이 부여된 액세스 <br> CA-36: 원격 액세스 <br> CA-53: 타사 모니터링 <br> CA-56: 고객 Lockbox 고객 승인 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2020년 12월 24일 |
| [SOC 3(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: 고객 Lockbox 요청 | 2020년 12월 24일 |