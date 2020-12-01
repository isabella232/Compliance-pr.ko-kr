---
title: Id 및 액세스 관리 개요
description: Microsoft 365의 id 및 액세스 관리에 대해 자세히 알아보기
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507835"
---
# <a name="identity-and-access-management-overview"></a>Id 및 액세스 관리 개요

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365에서 프로덕션 시스템을 무단 또는 악의적인 액세스 로부터 보호 하는 방법

Microsoft 365은 Microsoft의 엔지니어가 고객 콘텐츠에 액세스 하지 않고 서비스를 운영할 수 있도록 설계 되었습니다. 기본적으로 Microsoft 365 엔지니어는 고객 콘텐츠에 대 한 액세스 (ZSA)를 포함 하 고 프로덕션 환경에 대 한 액세스 권한이 없습니다. Microsoft 365에서는 JIT (Just-in-time) 액세스 (JEA) 모델을 사용 하 여 서비스 팀 엔지니어에 게 Microsoft 365를 지원 하기 위해 프로덕션 환경에 대 한 임시 권한 있는 액세스 권한을 제공 합니다. JIT 액세스 모델은 일반 영구 관리 액세스를 엔지니어가 필요한 경우 권한 있는 역할에 임시로 상승 시킬 수 있는 프로세스로 대체 합니다.

서비스 팀에 게 할당 된 엔지니어가 IDM (Id 관리 도구)를 통해 서비스 팀 계정의 프로덕션 서비스 요청 자격을 지원 합니다. 자격에 대 한 요청은 엔지니어가 모든 클라우드 차단 요구 사항을 통과 하 고, 필요한 교육을 완료 했으며, 계정 만들기 전에 적절 한 관리 승인을 받은 것을 확인 하기 위한 일련의 담당자를 확인 합니다. 모든 자격 요건을 충족 해야 요청한 환경에 대 한 서비스 팀 계정을 만들 수 있습니다.

서비스 팀 계정에는 필요한 관리자 권한 또는 고객 콘텐츠에 대 한 액세스 권한을 부여 하지 않습니다. 엔지니어가 Microsoft 365 서비스를 지원 하기 위해 추가 액세스를 필요로 하는 경우에는 Lockbox 라는 access 관리 도구를 사용 하 여 필요한 리소스에 대해 임시로 상승 된 액세스 권한을 요청 합니다. Lockbox는 할당 된 작업을 완료 하는 데 필요한 최소 권한, 리소스 및 시간에 대해 승격 된 액세스를 제한 합니다. 권한 있는 검토자가 JIT 액세스 요청을 승인 하는 경우 엔지니어에 게 할당 된 작업을 완료 하는 데 필요한 권한만 있는 임시 계정이 부여 됩니다. 이 임시 계정에는 다단계 인증이 필요 하며 승인 된 기간이 만료 되 면 자동으로 삭제 됩니다.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365에서 프로덕션 시스템에 대 한 원격 액세스를 처리 하는 방법

Microsoft 365 시스템 구성 요소는 운영 팀과 지리적으로 구분 된 데이터 센터에 보관 됩니다. 데이터 센터 직원은 Microsoft 365 시스템에 논리적으로 액세스할 수 없습니다. 따라서 Microsoft 365 서비스 팀 직원은 원격 액세스를 통해 환경을 관리 합니다. Microsoft 365를 지원 하기 위해 원격 액세스를 필요로 하는 서비스 팀 직원은 권한 있는 관리자의 승인을 받은 후에만 원격 액세스를 허용 합니다. 모든 원격 액세스는 보안 원격 연결에 FIPS 140-2 호환 TLS를 사용 합니다.

Microsoft 365는 Microsoft 365 환경이 손상 되지 않도록 보호 하기 위해 서비스 팀 원격 액세스용 SAWs (보안 관리자 워크스테이션)를 사용 합니다. 이러한 워크스테이션은 USB 포트를 잠그고 환경을 지 원하는 데 필요한 것으로 볼 때 사용할 수 있는 소프트웨어를 제한 하는 등의 프로덕션 데이터를 의도적으로 또는 실수로 손실 하지 않도록 하기 위해 특별히 설계 되었습니다. SAWs는 Microsoft 엔지니어가 고객 데이터를 악의적으로 또는 실수로 손상 시 키도를 감지 하 고 모니터링 하기 위해 면밀 하 게 추적 및 모니터 됩니다.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>고객 Lockbox가 고객 콘텐츠에 대 한 추가 보호 기능을 추가 하는 방법은 무엇 인가요?

고객은 고객 Lockbox를 사용 하 여 콘텐츠에 추가 수준의 액세스 제어를 추가할 수 있습니다. Lockbox 권한 상승 요청이 고객 콘텐츠에 대 한 액세스를 포함 하는 경우 고객 Lockbox는 승인 워크플로의 최종 단계로 고객의 승인을 받아야 합니다. 이를 통해 조직은 이러한 요청을 승인 또는 거부 하 고 고객에 게 직접 액세스 제어를 제공 하는 옵션을 제공할 수 있습니다. 고객이 고객 Lockbox 요청을 거부 하면 요청 된 콘텐츠에 대 한 액세스가 거부 됩니다. 고객이 특정 기간 내에 요청을 거부 하거나 승인 하지 않으면 Microsoft가 고객 콘텐츠에 대 한 액세스 권한을 획득 하지 않고 요청이 자동으로 만료 됩니다. 고객이 요청을 승인 하는 경우 문제 해결 작업을 완료 하기 위해 할당 된 시간이 만료 되 면 Microsoft의 일시적으로 고객 콘텐츠에 대 한 액세스가 기록 되 고, 감사 가능 하며, 자동으로 해지 됩니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. Id 및 액세스 제어와 관련 된 컨트롤의 유효성 검사에 대 한 자세한 내용은 다음 표를 참조 하십시오.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: 계정 관리 <br> AC-3: 액세스 적용 <br> AC-5: 의무 분리 <br> AC-6: 최소 권한 <br> AC-17: 원격 액세스 | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A 9.1: 액세스 제어의 비즈니스 요구 사항 <br> A 9.2: 사용자 액세스 관리 <br> 9.3: 사용자 책임 <br> -9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A 15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A 9.2: 사용자 액세스 관리 <br> -9.4: 시스템 및 응용 프로그램 액세스 제어 <br> A 15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한 있는 액세스 <br> CA-36: 원격 액세스 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32: 공유 계정 정책 <br> CA-33: 계정 수정 <br> CA-34: 사용자 인증 <br> CA-35: 권한 있는 액세스 <br> CA-36: 원격 액세스 <br> CA-53: 타사 모니터링 <br> CA-56: 고객 Lockbox 고객 승인 <br> CA-57: 고객 Lockbox Microsoft 관리 승인 <br> CA-58: 고객 Lockbox 서비스 요청 <br> CA-59: 고객 Lockbox 알림 <br> CA-61: JIT 검토 및 승인 | 2019년 9월 30일 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | \ EC-15: 고객 Lockbox 요청 | 2019년 9월 30일 |