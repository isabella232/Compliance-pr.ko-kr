---
title: 공급자 관리 개요
description: Microsoft 365의 공급자 관리에 대해 자세히 알아보기
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e46a7d2121a3ed1f314a3126c51911248362ff59
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508841"
---
# <a name="supplier-management-overview"></a>공급자 관리 개요

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft에서 공급자와 관련 된 위험을 관리 하는 방법

Microsoft는 고객의 요구 사항을 충족 하는 데 도움이 되는 타사 기업 들과 협력 합니다. 이러한 타사 회사는 suppliers 또는 subprocessors 라고 합니다. Microsoft의 공급자 보안 및 개인 정보 보호는 Microsoft와 협력 하 여 온라인 서비스를 제공 하는 모든 공급 업체에 대 한 엔터프라이즈 전체의 요구 사항 집합인 [SSPA (보안 정보 보호 보증) 프로그램](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)을 통해 관리 됩니다. SSPA 프로그램은 공급자 기반에 대 한 포괄적인 거 버 넌 스 및 관리를 제공 하지만 Microsoft 365와 같은 개별 업무 단위는 해당 공급자에 대 한 추가 요구 사항을 유지할 수 있습니다.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft의 공급자 보안 및 개인 정보 보호 (SSPA) 프로그램에서 고객 데이터를 보호할 방법

SSPA는 Microsoft 조달, 회사 외부 및 법적 고 지 및 회사 보안 간의 파트너 관계를 유지 하 여 공급자가 Microsoft의 개인 정보 및 보안 원칙을 준수 하도록 합니다. SSPA의 범위에는 개인 데이터 나 Microsoft 기밀 데이터를 처리 하는 모든 공급자가 포함 됩니다. SSPA 프로그램 등록에는 Microsoft의 DPR (데이터 보호 요구)을 준수 하는 기능이 포함 되어 있습니다. DPR은 계약 시작을 Microsoft와 함께 사용 하기 전에 공급자가 구현 해야 하는 보안 및 개인 정보 보호 컨트롤로 구성 됩니다. 모든 등록 된 공급자가 DPR을 매년 준수 하도록 자체 보증 합니다.

DPR 요구 사항은 6 개의 고유한 데이터 처리 범주를 기반으로 하며, 공급자는 SSPA에서 등록의 일부로 승인 될 수 있습니다. 이러한 범주는 공급자가 Microsoft에 제공 하는 서비스와 관련 된 위험을 식별 하는 데 사용 됩니다. 공급자의 데이터 처리 프로필은 적절 한 데이터 보호를 제공 하기 위해 범위 내에서 고려 되는 DPR 컨트롤을 결정 합니다. 더 높은 위험으로 간주 되는 데이터를 처리 하는 공급자는 모든 DPR 요구 사항을 준수 해야 하며, 준수에 대 한 독립적인 확인을 제공 해야 할 수도 있습니다. Microsoft 구매 도구는 해당 공급자의 조달을 허용 하기 전에 해당 하는 모든 공급자의 SSPA 상태를 검증 합니다 (DPR의 해당 부분에 대 한 준수 포함).

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>어떤 유형의 하위 프로세서가 Microsoft에 서비스를 제공 하나요?

' Subprocessor '는 microsoft에서 microsoft에 게 제공 되는 microsoft 개인 데이터의 처리를 포함 하는 타사 제품입니다. Microsoft의 하위 프로세서는 세 가지 고유한 범주로 나뉩니다. 각각은 SSPA를 사용 하 여 Microsoft의 고객 데이터를 처리할 수 있도록 규정 준수를 보여 주어 야 합니다.

- **기술** 하위 프로세서는 특정 Microsoft online services를 제공 하는 데 사용 되는 기술을 제공 합니다. 고객이 이러한 서비스 중 하나를 배포 하는 경우 해당 서비스에 대해 식별 된 하위 프로세서는 고객 데이터 또는 개인 데이터를 처리, 저장 또는 액세스 하는 동시에 해당 서비스를 제공 하는 데 도움이 될 수 있습니다.
- **보조** 하위 프로세서는 온라인 서비스를 지원, 작동 및 유지 관리 하는 서비스를 제공 합니다. 고객이 이러한 서비스 중 하나를 배포 하는 경우에는 보조 서비스를 제공 하면서 제한 된 고객 데이터 또는 개인 데이터를 처리, 저장 또는 액세스 하는 하위 프로세서가 있을 수 있습니다.
- **직원 업그레이드** 하위 프로세서는 두 가지 다른 양식을 사용 합니다. 두 시나리오에서 개인 데이터는 microsoft 시스템의 microsoft 시설에만 존재 하며 microsoft 정책 및 감독의 영향을 받습니다.

    - 첫 번째 직원 형태는 Microsoft online services를 지원 하 고 운영 하 고 유지 관리 하는 직원을 제공 합니다. 이러한 하위 프로세서는 업무를 수행 하는 동안 고객 데이터 또는 개인 데이터에 노출 될 수 있습니다. 예를 들어 하위 프로세서는 Microsoft 서버에서 원격 문제 해결을 수행할 수 있으며,이 작업을 수행 하는 동안 서버 크래시 덤프 로그의 고객 데이터 조각에 노출 될 수 있습니다.
    - 두 번째 형태의 직원 업그레이드에는 microsoft online services를 지원, 운영 및 유지 관리 하기 위해 Microsoft 정규 직원 들과 공동 작업을 하는 하위 프로세서가 포함 됩니다. 이러한 하위 프로세서는 Microsoft 정규 직원과 함께 작업 하는 동안 pseudonymized 데이터에 노출 될 수 있습니다.

기술 및 보조 하위 프로세서는 Microsoft의 DPR (데이터 보호 요구)을 준수 하는 액세스 제어를 구현 하는 데 필요 합니다. 이러한 요구 사항은 Microsoft에서 온라인 서비스 약관 (OST)에 고객에 게 주는 계약을 충족 하거나 초과 합니다. 직원 업그레이드 작업을 수행 하는 공급자는 Microsoft 정규 직원 들에 게 동일한 액세스 제어를 받을 수 있습니다.

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft 온보드 공급자는 어떻게 되나요?

타사 공급자는 온 보 딩 프로세스의 일부로 Microsoft 마스터 계약에 서명 하는 데 필요 합니다. 이 규약은 Microsoft와 해당 공급자 간의 관계를 제어 하며, 공급자 관계를 일관 되 게 관리할 것을 보장 합니다. 온 보 딩의 일부로, 공급자는 SSPA에 등록 하 고 모든 데이터 처리 범주에 대해 승인 되기 전에 해당 하는 모든 요구 사항을 완료 해야 합니다. Microsoft business 유닛은 계약에 대 한 데이터 처리 활동이 공급자가 승인 된 데이터 처리 범주와 일치 하는 경우 공급자와의 계약만 만들 수 있습니다.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft에서 데이터를 처리 하는 공급자의 변경 사항을 고객에 게 알리는 방법

Microsoft Online 서비스에서 DPA (데이터 보호 추 록)에 따라 Microsoft는 모든 하위 프로세서 추가를 알리는 알림 기간에 대 한 추가 약정을 사용 합니다. 알림 시간 프레임은 Microsoft를 대신 하 여 하위 프로세서에서 처리할 데이터 유형에 따라 달라 집니다. DPA에 명시 된 바와 같이, Microsoft는 고객 데이터를 처리 하는 모든 새 하위 프로세서 앞에 최소 6 개월 전에 고객에 게 알림을 제공 하는 작업을 커밋합니다. 기타 모든 개인 데이터에 대해 Microsoft는 30 일 이상의 알림을 제공 합니다. 공지는 [Microsoft Online Services 하위 프로세서 목록의](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)업데이트를 통해 제공 됩니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 공급자 관리와 관련 된 컨트롤의 유효성 검사를 보려면 아래 표를 참조 하세요.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: 시스템 interconnections <br> IA-4: 식별자 관리 <br> PS-6: 액세스 계약 <br> PS-7: 타사 직원 보안 <br> SA-4: 합병 프로세스 <br> SA-9: 외부 정보 시스템 서비스 <br> SA-12: 보급 체인 보호 | 2020 년 9 월 24 일 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A 15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A 15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A 8.1: 공개 되 고 계약 된 PII 처리 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-53: 타사 모니터링 | 2019년 9월 30일 |

## <a name="resources"></a>리소스

- [공급자 보안 개인 정보 및 보증 프로그램](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
