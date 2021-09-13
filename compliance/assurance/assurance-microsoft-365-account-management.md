---
title: Microsoft 365
description: 계정 관리에 대해 Microsoft 365
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
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160238"
---
# <a name="account-management-in-microsoft-365"></a>Microsoft 365

Microsoft는 대부분의 Microsoft 365 작업을 자동화하는 시스템 및 제어에 많은 투자를 하면서 서비스 담당자의 서버 및 고객 데이터에 대한 직접 액세스의 필요성을 의도적으로 제한하고 있습니다. 서비스 및 소프트웨어가 서비스를 운영합니다. 이 구조를 통해 Microsoft는 대규모로 Microsoft 365 관리할 수 있으며 내부 및 외부 위협의 위험을 최소화할 수 있습니다. Microsoft는 모든 사람이 서비스 및 고객 데이터에 Microsoft 365 위협이 될 수 있다는 가정 하에 액세스 제어에 접근합니다. 이러한 이유로 ZSA(Zero Standing Access) 원칙은 조직에서 사용하는 전체 액세스 제어 구조의 토대를 Microsoft 365.

기본적으로 Microsoft 직원은 조직의 모든 환경 또는 고객 Microsoft 365 액세스할 수 없습니다. 이는 서비스 팀 직원이 좁은 작업 및 시간 범위로 권한 있는 액세스 권한을 얻을 수 있는 강력한 검사 및 승인 시스템을 통해서만 수행됩니다. Microsoft Microsoft 365는 이 시스템을 통해 서비스 직원 및 공격자가 무단 액세스 권한을 얻거나 악의적 또는 우발적인 손상을 입히거나 사용자와 고객에게 악의적인 Microsoft 서비스 가능성을 크게 줄일 수 있습니다.

## <a name="account-types"></a>계정 유형

Microsoft 365 계정의 세 가지 범주인 서비스 팀 계정, 서비스 계정 및 고객 계정을 사용하여 모든 조직 임무 및 비즈니스 기능을 충족합니다. 이러한 계정을 관리하는 것은 Microsoft와 고객 간의 공유 책임입니다. Microsoft는 Microsoft 제품 및 서비스를 운영하고 지원하는 데 사용되는 서비스 팀 및 서비스 계정을 모두 관리합니다. 고객 계정은 고객이 관리하며 내부 액세스 제어 요구 사항에 맞게 계정 액세스를 조정할 수 있도록 합니다.

![계정에 대한 공유 책임](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Microsoft 관리 계정

**서비스 팀 계정은** 서비스 팀 Microsoft 365 개발하고 유지 관리하는 데 Microsoft 365 사용됩니다. 이러한 계정은 Microsoft 365 서비스에 대한 권한이 없는 대신 임시 및 제한된 권한 액세스를 요청하여 지정된 작업 기능을 수행하는 데 사용할 수 있습니다. 모든 서비스 팀 계정이 동일한 작업을 수행할 수 있는 것은 아니며, RBAC(역할 기반 액세스 제어)를 사용하여 업무 분리가 적용됩니다. 역할은 서비스 팀 구성원과 해당 계정에 특정 직무를 수행하는 데 필요한 최소 액세스만 하도록 합니다. 또한 서비스 팀 계정은 자신의 작업에 대한 승인자 역할을 할 수 있는 여러 역할에 속할 수 없습니다.

**서비스 계정은** Microsoft 365 프로세스를 통해 다른 서비스와 통신할 때 인증하는 데 사용됩니다. 서비스 팀 계정에 특정 직원의 직무를 수행하는 데 필요한 최소 액세스 권한만 부여된 경우 서비스 계정에는 의도한 용도에 필요한 최소 액세스 권한만 부여됩니다. 또한 특정 요구를 충족하도록 설계된 여러 유형의 서비스 계정이 있습니다. 하나의 Microsoft 365 서비스 계정이 여러 개 있을 수 있습니다. 각각 수행할 역할이 서로 다를 수 있습니다.

## <a name="customer-managed-accounts"></a>고객 관리 계정

**고객 계정은** Microsoft 365 서비스에 액세스하는 데 사용되어 각 고객이 담당하는 유일한 계정입니다. 보안 환경을 유지 관리하기 위해 조직의 계정을 만들고 관리하는 것은 고객의 의무입니다. 고객 계정 관리는 AAD(Azure Active Directory Active Directory)를 통해 수행되거나, 사내 AD(Active Directory)와 페더된 상태입니다. 각 고객에게는 충족해야 하는 고유한 액세스 제어 요구 사항이 있으며 고객 계정은 각 고객에게 개별 요구 사항을 충족할 수 있는 권한을 부여합니다. 고객 계정은 고객 조직 외부의 데이터에 액세스할 수 없습니다.

## <a name="service-team-account-management"></a>서비스 팀 계정 관리

Microsoft 365 IDM(ID 관리)이라는 계정 관리 시스템을 사용하여 수명 주기 동안 서비스 팀 계정을 관리합니다. IDM은 자동화된 확인 프로세스와 관리자 승인을 조합하여 서비스 팀 계정 액세스와 관련된 보안 요구 사항을 적용합니다.

서비스 팀 구성원은 자동으로 서비스 팀 계정을 얻지 못하며, 먼저 자격 요구 사항을 충족하고 권한이 부여된 관리자의 승인을 구해야 합니다. 서비스 팀 계정에 자격을 제공하려면 서비스 팀 직원이 먼저 고용 [전](assurance-pre-employment-screening.md)직원 [](assurance-cloud-background-check.md)심사, 클라우드 배경 검사 및 모든 표준 및 필수 역할 기반 교육을 완료해야 합니다. 모든 자격 요구 사항이 충족되면 서비스 팀 계정에 대한 요청을 수행할 수 있으며 권한이 부여된 관리자가 승인해야 합니다.

![직원 심사 프로세스](../media/assurance-personnel-screening-process.png)

또한 IDM은 서비스 팀 계정을 유지 관리하는 데 필요한 주기적인 재시도 및 교육을 추적합니다. Microsoft 클라우드 배경 검사는 2년마다 완료해야 합니다. 모든 교육 자료는 매년 검토해야 합니다. 만료 날짜까지 이러한 요구 사항 중 하나를 충족하지 못하면 자격이 해지되고 서비스 팀 계정이 자동으로 비활성화됩니다.

또한 서비스 팀 계정 자격은 직원 이전 및 종료에 의해 [자동으로 업데이트됩니다.](assurance-employee-transfer-termination.md) HRIS(인사 정보 시스템)에서 변경한 내용은 IDM이 조치를 취하기 위해 트리거하며, 이는 상황에 따라 다릅니다. 다른 서비스 팀으로 이전하는 직원은 자격에 대한 만료 날짜가 설정되어 있으며 자격 유지 관리 요청은 서비스 팀 구성원이 제출하고 새 관리자가 승인해야 합니다. 해지된 직원은 모든 자격이 자동으로 해지되고 해당 서비스 팀 계정이 마지막 날에 비활성화됩니다. 긴급한 계정 해지 요청이 자발적으로 종료될 수 있습니다.

기본적으로 서비스 팀 계정은 정기적인 문제 해결에 사용되는 광범위한 시스템 메타데이터에 대한 읽기 권한이 제한됩니다. 또한 기준 서비스 팀 계정은 사용자 또는 고객 데이터에 대한 권한 있는 액세스를 Microsoft 365 없습니다. 서비스 팀 구성원이 특정 작업 및 작업을 수행할 수 있는 상승된 권한을 요청할 수 있도록 서비스 팀 계정을 역할에 추가하려면 다른 요청을 해야 합니다.
