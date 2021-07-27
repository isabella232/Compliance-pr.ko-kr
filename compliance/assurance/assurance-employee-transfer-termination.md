---
title: Microsoft 직원 전근 및 고용 종료
description: Microsoft 직원 이전 및 종료 프로세스에 대해 Microsoft 365
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
ms.openlocfilehash: 4a71ab3ddf6688df5480a8f260e004778aa6212b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573363"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Microsoft 직원 전근 및 고용 종료

Microsoft는 다른 모든 조직과 마찬가지로 정상적인 비즈니스 운영의 일부로 직원 이전 및 종료를 처리합니다. 직원이 직위를 변경하거나 퇴사할 때 부적절한 액세스를 시기적절하게 해지해야 합니다. 효율적으로 액세스 변경 및 액세스 해지가 수행될 수 있도록 Microsoft는 표준화된 절차 및 자동화된 프로세스를 사용하여 HRIS(인사 정보 시스템)를 IDM(ID 관리) 시스템과 조정합니다. 이 두 시스템 간의 자동화된 오케스트레이션은 운영 일관성을 유지하고, Microsoft의 온라인 서비스 및 데이터를 보호하고, 권한 크리프를 방지하고, 내부자 위협과 관련된 위험을 줄이는 데 필수적입니다.

Microsoft 온라인 서비스는 엔지니어를 위해 프로덕션 환경에 대한 관리 액세스 권한 없이 작동하도록 설계되었습니다. Microsoft는 JIT(Just-In-Time), JEA(Just-Enough-Access) 모델을 사용하여 엔지니어에게 필요할 때 서비스를 지원하는 데 필요한 임시 액세스 권한을 제공합니다. JIT 액세스를 위해 서비스 팀 계정을 요청하고 사용하려면 엔지니어가 IDM 도구를 통해 자격을 요청하고 유지 관리해야 합니다. 직원이 양도 또는 해지되면 해당 서비스 팀 계정 및 관련 자격이 부적절한 액세스를 방지하기 위해 자동으로 수정됩니다.

## <a name="transfer-and-reassignment"></a>전송 및 재할당

직원 이전은 직원의 상사에 의해 이전 트랜잭션 요청을 통해 시작됩니다. 관리자는 재지정을 만들고 제안서 프로세스에 대해 전역 인재 인수에 참여합니다. 직원이 새 역할에 대한 제안을 수락하면 HR 서비스는 HR 핵심 도구의 이전을 완료하여 IDM이 모든 직원의 자격에 대한 만료 날짜를 설정하게 합니다. 직원은 요청을 제출하고 새 관리자로부터 승인을 받아 자격을 유지해야 합니다. 요청을 제출하거나 관리자 승인을 받지 못하면 전달된 직원의 자격이 해지됩니다. 특정 보안이 포함된 전송의 경우 시스템 액세스 및 보안 그룹 구성원 자격이 새 역할을 반영하도록 즉시 다시 평가됩니다.

## <a name="termination"></a>종료

Microsoft는 명확하게 정의된 정책 및 절차를 사용하여 직원이 해고될 때 Microsoft 시스템 및 리소스에 대한 물리적 및 논리적 액세스를 즉시 취소합니다. 직원이 통지를 하면 직원의 상사는 종료 날짜를 HRIS에 입력합니다. 직원의 마지막 작업일 다음에 HRIS는 직원을 종료된 것으로 표시하고 정보를 IDM에 공유하여 모든 서비스 팀 계정 및 자격을 자동으로 제거합니다.

자발적 종료의 경우 HR은 직원의 관리자와 함께 적절한 단계에 따라 직원을 종료하고 취소합니다. 자발적 종료와 마찬가지로 종료 정보는 유효 날짜 조정, 액세스 제거와 같은 필요한 단계와 함께 HRIS에 입력됩니다. 및 역할 전환과 상대적인 다른 모든 단계
