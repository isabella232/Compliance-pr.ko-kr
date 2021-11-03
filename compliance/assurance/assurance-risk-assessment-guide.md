---
title: Microsoft Cloud에 대한 위험 평가 가이드
description: Microsoft 클라우드의 위험 평가 가이드에 대해 자세히 알아보세요.
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
ms.openlocfilehash: df4b98f90c70bab3bd7f09e6312833d8a7ea768b
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678435"
---
# <a name="risk-assessment-guide-for-microsoft-cloud"></a>Microsoft Cloud에 대한 위험 평가 가이드

클라우드 위험 평가의 목표는 클라우드로의 마이그레이션을 고려한 시스템 및 데이터가 조직에 새로운 위험 또는 확인되지 않은 위험을 도입하지 않도록 하는 것입니다. 초점은 정보 처리의 기밀성, 무결성, 가용성 및 개인 정보 보호를 보장하고 식별된 위험을 허용된 내부 위험 임계값 미만으로 유지하는 것입니다.

공유 책임 모델에서 클라우드 서비스 공급자(CSP)는 클라우드의  보안 및 규정 준수를 공급자로 관리합니다. 고객은 요구 및 위험 허용 오차에  따라 클라우드에서 보안 및 규정 준수를 관리하고 구성할 책임이 있습니다.

![공유 책임 모델.](../media/assurance-shared-responsibility-model.png)

이 가이드에서는 공급업체 위험을 효율적으로 평가하는 방법과 Microsoft가 제공하는 리소스 및 도구를 사용하는 방법에 대한 모범 사례를 공유합니다.

## <a name="understand-shared-responsibility-in-the-cloud"></a>클라우드의 공유 책임 이해

클라우드 배포는 IaaS(Infrastructure as a Service), PaaS(Platform as a Service) 또는 SaaS(Software as a Service)로 분류될 수 있습니다. 해당 클라우드 서비스 모델에 따라 솔루션의 보안 제어에 대한 책임 수준이 CSP와 고객 간에 전환됩니다. 기존 온-프레미스 모델에서 고객은 전체 스택을 담당합니다. 클라우드로 전환할 때 모든 물리적 보안 책임은 CSP로 전송됩니다. 조직의 클라우드 서비스 모델에 따라 추가 책임이 CSP로 전환됩니다. 그러나 대부분의 서비스 모델에서 조직은 클라우드, 네트워크 연결, 계정 및 ID 및 데이터에 액세스하는 데 사용되는 장치를 계속 관리합니다. Microsoft는 고객이 전체 수명 주기 동안 데이터를 제어할 수 있도록 하는 서비스를 만드는 데 많은 투자를 합니다.

Microsoft 클라우드는 개발자SecOps와 자동화의 조합을 통해 운영 모델을 표준화하는 하이퍼스케일에서 운영됩니다. Microsoft 운영 모델에서는 기존 사내 운영 모델에 비해 위험에 접근하는 방식이 변경되어 위험 관리에 익숙하지 않은 컨트롤을 구현할 수 있습니다. 클라우드 위험 평가를 진행할 때 Microsoft의 목표는 모든 위험을 해결할 수 있도록 하는 것이지만 조직에서 수행한 동일한 제어를 구현할 필요는 없습니다. Microsoft는 다른 컨트롤 집합으로 동일한 위험을 해결할 수 있으며 클라우드 위험 평가에 반영해야 합니다. 강력한 예방 컨트롤을 디자인하고 구현하면 감지 및 수정 컨트롤에 필요한 작업의 많은 것을 줄일 수 있습니다. 예를 들어 Microsoft의 [ZSA(Zero Standing Access) 구현이 있습니다.](assurance-microsoft-365-service-engineer-access-control.md)

## <a name="adopt-a-framework"></a>프레임워크 채택

고객은 내부 위험 및 제어 프레임워크를 표준화된 방식으로 클라우드 위험을 해결하는 독립적인 프레임워크에 매핑하는 것이 좋습니다. 기존 내부 위험 평가 모델이 클라우드 컴퓨팅과 함께 제공된 특정 문제를 해결하지 않는 경우 광범위하게 채택된 표준화된 프레임워크를 활용하게 됩니다. 두 번째 이점은 Microsoft가 문서 및 도구에서 이러한 프레임워크에 대한 매핑을 제공하면 위험 평가를 가속화할 수 있습니다. 이러한 프레임워크의 [예로는 ISO 27001 정보](/compliance/regulatory/offering-iso-27001)보안 표준, [CIS 벤치마크](/compliance/regulatory/offering-cis-benchmark)및 [NIST SP 800-53이 있습니다.](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) Microsoft는 모든 CSP의 가장 포괄적인 규정 준수 제품 집합을 제공합니다. 자세한 내용은 Microsoft 규정 준수 [제품 을 참조하세요.](/compliance/regulatory/offering-home)

[Microsoft 준수 관리자를](/microsoft-365/compliance/compliance-manager) 사용하여 조직에 적용되는 산업 및 지역 규정을 준수하는지 평가하는 자체 평가를 만들 수 있습니다. 평가는 필요한 컨트롤, 개선 작업 및 해당되는 경우 평가 완료를 위한 Microsoft 작업이 포함된 평가 템플릿의 프레임워크를 사용하여 작성됩니다. Microsoft 작업의 경우 자세한 구현 계획과 최근 감사 결과가 제공됩니다. 이렇게 하면 Microsoft에서 특정 컨트롤이 구현되는 방식에 대한 사실 검색, 매핑 및 조사에 시간을 절약할 수 있습니다. 자세한 내용은 Microsoft 준수 관리자 문서를 참조하세요.

## <a name="understand-how-microsoft-operates-to-safeguard-your-data"></a>데이터를 보호하기 위해 Microsoft의 운영 방식 이해

고객은 클라우드에서 보안 및 규정 준수를 관리 및 구성하는 업무를 담당하며, CSP는 클라우드의 보안 및 규정 준수를 *관리합니다.* CSP가 책임을 효과적으로 해결하고 약속을 지킬 수 있도록 하는 한 가지 방법은 ISO 및 SOC와 같은 외부 감사 보고서를 검토하는 것입니다. Microsoft는 Service Trust Portal에서 인증된 대상이 외부 감사 보고서를 사용할 [수 있도록 합니다.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)

외부 감사 보고서 외에도 Microsoft는 고객이 다음 리소스를 활용하여 Microsoft의 운영 방식에 대해 깊이 있게 이해할 것을 적극 장려합니다.

- [On-Demand Learning 경로:](/learn/roles/auditor)Microsoft의 학습 플랫폼은 다양한 주제에 대한 수백 가지 학습 경로 및 모듈을 제공합니다. 그 중에서 Microsoft가 고객 데이터를 보호하는 방법을 알아보고 Microsoft의 기본 보안 및 개인 정보 보호 정책을 이해합니다. [](/learn/paths/audit-safeguard-customer-data/)

- [Microsoft 규정 준수에 대한 서비스](/compliance/#service-assurance)보증: Microsoft의 사례에 대한 문서는 더 쉽게 검토할 수 있도록 16개 도메인으로 분류됩니다. 각 도메인에는 Microsoft가 각 영역과 관련된 위험을 관리하는 방법을 캡처하는 개요가 포함되어 있습니다. 감사 테이블에는 Service Trust Portal에 저장된 최신 보고서, 관련 섹션, Microsoft 온라인 서비스에 대해 감사 보고서가 수행된 날짜에 대한 링크가 들어 있습니다. 사용 가능한 경우 타사 취약성 평가 및 비즈니스 연속성 계획 확인 보고서와 같은 제어 구현을 시연하는 아티팩트에 대한 링크가 제공됩니다. 감사 보고서와 마찬가지로 이러한 아티팩트는 STP에서 호스트되어 액세스하려면 인증이 요구됩니다.

| **도메인** |**설명** |
|:---------- |:-------------- |
| [**아키텍처**](assurance-architecture.md) | Microsoft 온라인 서비스의 디자인 및 기본 역할을 하는 보안 원칙 |
| [**감사 로깅**](assurance-audit-logging.md) | Microsoft가 보안 및 성능 모니터링을 가능한 로그를 캡처, 처리, 저장 및 보호하는 방법 |
| [**데이터 센터 보안**](assurance-datacenter-security.md) | Microsoft가 전 세계 Microsoft 온라인 서비스를 운영하는 방법을 제공하는 데이터 센터를 안전하게 운영하는 방법 |
| [**암호화 및 키 관리**](assurance-encryption.md) | 클라우드에 저장 및 처리되는 고객 커뮤니케이션 및 데이터의 암호화 보호입니다. |
| [**거버넌스**](assurance-governance.md) | Microsoft가 고객 약속 및 규정 준수 요구 사항을 충족하기 위해 기업 전체에서 보안 정책을 만들고, 배포하고, 업데이트하고, 적용하는 방법 |
| [**인적 리소스**](assurance-human-resources.md) | 선고 프로세스는 Microsoft에서 직원의 시간 전체에 걸쳐 안전하게 관리됩니다. |
| [**ID 및 액세스 관리**](assurance-identity-and-access-management.md) | 무단 또는 악의적인 액세스로부터 Microsoft 온라인 서비스 및 고객 데이터를 보호합니다. |
| [**인시던트 관리**](assurance-incident-management.md) | Microsoft가 모든 보안 및 개인 정보 보호 인시던트에 대비하고, 감지하고, 대응하고, 전달하는 데 사용하는 프로세스입니다. |
| [**네트워크 보안**](assurance-network-security.md) | Microsoft가 외부 공격으로부터 네트워크 경계를 보호하고 내부 네트워크를 관리하여 전파를 제한하는 방법 |
| [**개인 정보**](assurance-privacy.md) | Microsoft가 고객 데이터를 처리하고 보호하여 데이터 권한을 보존하는 방법 |
| [**복원력 및 연속성**](assurance-resiliency-and-continuity.md) | 서비스 가용성을 유지 관리하고 비즈니스 연속성 및 복구를 보장하는 데 사용되는 프로세스 및 기술입니다. |
| [**리스크 관리**](assurance-risk-management.md) | 기업 전체의 위험을 최소화하기 위해 취한 식별, 평가 및 작업입니다. |
| [**보안 개발 및 운영**](assurance-security-development-and-operation.md) | Microsoft가 해당 서비스가 수명 주기 동안 안전하게 설계, 실행 및 관리되도록 하는 방법 |
| [**보안 모니터링**](assurance-security-monitoring.md) | 권한이 없는 또는 악의적인 활동을 감지하고 직원에게 경고하기 위한 로그의 중앙 분석 |
| [**공급자 관리**](assurance-supplier-management.md) | Microsoft가 Microsoft 온라인 서비스를 지원할 타사를 화면하고 관리하는 방법 |
| [**취약성 관리**](assurance-vulnerability-management.md) | Microsoft가 취약성 및 맬웨어를 검색, 감지 및 해결하기 위해 사용하는 프로세스입니다. |

## <a name="resources"></a>리소스

- [Microsoft 클라우드의 금융 기관을 위한 위험 평가 및 규정 준수 가이드](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [집중 위험: Microsoft의 관점](https://azure.microsoft.com/mediahandler/files/resourcefiles/concentration-risk-perspectives-from-microsoft-/Concentration_Risk_Perspectives_092020.pdf)
- [서비스 보안 포털](https://servicetrust.microsoft.com/)
