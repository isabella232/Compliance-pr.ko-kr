---
title: 공급자 관리 개요
description: Microsoft 365의 공급자 관리에 대해 자세히 알아보십시오.
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
ms.openlocfilehash: 4da4775332989c4a40738777dfae7318e27086f0
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787377"
---
# <a name="supplier-management-overview"></a>공급자 관리 개요

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft는 공급자와 관련된 위험을 어떻게 관리하나요?

고객의 요구 사항을 충족하는 데 도움을 줄 수 있도록 타사와 Microsoft 파트너가 협력합니다. 이러한 타사를 공급업체 또는 하위 처리기라고 합니다. Microsoft의 공급자 보안 및 개인 정보 보호는 Microsoft와 파트너가 온라인 서비스를 제공하기 위해 Microsoft와 파트너가 있는 모든 공급자에 대한 엔터프라이즈 전체 요구 사항 집합인 [SSPA(공급자](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)보안 및 개인 정보 보호) 프로그램에서 관리합니다. SSPA 프로그램은 공급자 기반에 대한 포괄적인 거버넌스 및 관리를 제공하나 Microsoft 365와 같은 개별 사업부는 공급업체에 대한 추가 요구 사항을 유지할 수 있습니다.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft의 공급자 보안 및 개인 정보 보호(SSPA) 프로그램에서 고객 데이터를 보호하는 방법

SSPA는 공급자가 Microsoft의 개인 정보 및 보안 원칙을 준수하도록 Microsoft 조달, 회사 외부 및 법률 업무 및 회사 보안 간의 파트너 관계입니다. SSPA의 범위는 개인 데이터 또는 Microsoft 기밀 데이터를 처리 하는 모든 공급자를 다를 수 있습니다. SSPA 프로그램 등록에는 Microsoft의 DPR(데이터 보호 요구 사항)을 준수하는 것이 포함됩니다. DPR은 Microsoft와 계약된 작업을 시작하기 전에 공급자가 구현해야 하는 보안 및 개인 정보 보호 제어로 구성됩니다. 등록된 모든 공급자는 매년 DPR을 준수하는지 자체적으로 규명합니다.

DPR 요구 사항은 공급자가 SSPA 등록의 일부로 승인할 수 있는 6가지 데이터 처리 범주에 따라 범위가 지정됩니다. 이러한 범주는 공급자가 Microsoft에 제공하는 서비스와 관련된 위험을 식별하는 데 사용됩니다. 공급자의 데이터 처리 프로필은 적절한 데이터 보호를 제공하기 위해 범위 내로 고려되는 DPR 컨트롤을 지정합니다. 더 높은 위험으로 간주되는 데이터를 처리하는 공급자는 모든 DPR 요구 사항을 준수해야 하며 독립적인 규정 준수 확인을 제공해야 할 수도 있습니다. Microsoft 구매 도구는 해당 공급자의 조달을 허용하기 전에 DPR의 적용 가능한 부분 준수를 포함하여 모든 공급자의 SSPA 상태의 유효성을 검사합니다.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Microsoft에 서비스를 제공하는 하위 처리기 유형은 무엇입니까?

'하위 프로세서'는 Microsoft가 처리자인 Microsoft 개인 데이터 처리를 포함해야 하는 업무를 처리하는 타사입니다. Microsoft의 하위 처리기는 세 가지 범주로 구분됩니다. 각각은 Microsoft를 대신하여 고객 데이터를 처리하기 전에 SSPA 준수를 입증해야 합니다.

- **기술** 하위 처리기는 특정 Microsoft 온라인 서비스를 제공하는 데 사용되는 기술을 제공합니다. 고객이 이러한 서비스 중 하나를 배포하는 경우 해당 서비스에 대해 식별된 하위 처리기는 해당 서비스를 제공하는 동안 고객 데이터 또는 개인 데이터를 처리, 저장 또는 액세스할 수 있습니다.
- **보조** 하위 처리기는 온라인 서비스를 지원, 운영 및 유지 관리하는 서비스를 제공합니다. 고객이 이러한 서비스 중 하나를 배포하는 경우 식별된 하위 처리기는 보조 서비스를 제공하는 동안 제한된 고객 데이터 또는 개인 데이터를 처리, 저장 또는 액세스할 수 있습니다.
- **직원 증강** 하위 처리기는 두 가지 형식을 취합니다. 두 시나리오에서 개인 데이터는 Microsoft 시설, Microsoft 시스템에만 상주하며 Microsoft 정책 및 감독을 따라야 합니다.

    - 첫 번째 형태의 직원 보강은 Microsoft 온라인 서비스를 지원, 운영 및 유지 관리하는 직원을 제공합니다. 책임을 이행하는 동안 이러한 하위 처리기는 고객 데이터 또는 개인 데이터에 노출될 수 있습니다. 예를 들어 하위 처리기는 Microsoft 서버에서 원격 문제 해결을 수행할 수 있으며, 이렇게 하는 동안 서버 크래시 덤프 로그의 고객 데이터 일부에 노출될 수 있습니다.
    - 두 번째 직원 보강 형식에는 Microsoft 정규 직원과 함께 Microsoft 온라인 서비스를 지원, 운영 및 유지 관리하기 위해 함께 작업하는 하도원업체가 있습니다. 이러한 하위 처리기는 Microsoft 정규 직원과 함께 작업의 일부로 가명 처리된 데이터에 노출될 수 있습니다.

Microsoft의 DPR(데이터 보호 요구 사항)에 따라 액세스 제어를 구현하려면 기술 및 보조 하위 처리기가 필요합니다. 이러한 요구 사항은 Microsoft가 OST(온라인 서비스 약관)에서 고객에게 확정한 계약을 충족하거나 초과합니다. 직원 보강 작업을 수행하는 공급업체는 Microsoft 정규 직원에 대해 동일한 액세스 제어가 적용될 수 있습니다.

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft는 공급자를 어떻게 온보드하나요?

타사 공급자는 등록 프로세스의 일부로 Microsoft 마스터 계약에 서명해야 합니다. 이 계약은 Microsoft와 해당 공급자 간의 관계를 관리하고 공급자 관계의 일관된 관리를 보장합니다. 등록의 일부로 공급자는 SSPA에 등록하고 모든 데이터 처리 범주에 대해 승인을 되기 전에 적용 가능한 모든 요구 사항을 완료해야 합니다. Microsoft 사업부는 계약에 대한 데이터 처리 활동이 공급업체가 승인된 데이터 처리 범주와 일치하는 경우 공급자와의 계약만 만들 수 있습니다.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft는 데이터를 처리한 공급업체에 대한 변경 내용을 고객에게 어떻게 알릴 수 있나요?

Microsoft 온라인 서비스 데이터 보호 부록(DPA)에 따라 Microsoft는 모든 하위 처리기 추가에 대한 알림 기간과 관련하여 추가 약정을 합니다. 알림 기간은 하위 프로세스가 Microsoft를 대신하여 처리하게 될 데이터의 형식에 따라 다릅니다. DPA에 앞서 Microsoft는 고객 데이터를 처리하게 될 새 하위 처리기에서 최소 6개월 전에 고객에게 통지를 제공하겠다. 다른 모든 개인 데이터의 경우 Microsoft는 최소 30일간의 통지를 제공합니다. 하위 처리기 목록의 Microsoft Online Services [알림이 제공됩니다.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 공급자 관리와 관련된 컨트롤의 유효성 검사는 아래 표를 참조하세요.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: 시스템 상호 연결 <br> IA-4: 식별자 관리 <br> PS-6: 액세스 계약 <br> PS-7: 타사 직원 보안 <br> SA-4: 취득 프로세스 <br> SA-9: 외부 정보 시스템 서비스 <br> SA-12: 공급망 보호 | 2020년 9월 24일 |
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: 공급자 관계의 정보 보안 | 2020년 2월 22일 |
| [ISO 27018(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: 하도급 하도급 PII 처리 공개 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: 타사 모니터링 | 2020년 12월 24일 |

## <a name="resources"></a>리소스

- [공급자 보안 개인 정보 보호 및 보증 프로그램](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
