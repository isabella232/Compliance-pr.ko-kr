---
title: DoD(국방부) 영향 수준 2(IL2)
description: Microsoft가 IL2(국방부) 영향 수준 2(IL2) 표준을 충족하는 방법을 알아보습니다.
keywords: Microsoft 365, 규정 준수, 제안
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 0c44d77772eef6321d716aa87f34d0472401fb30092dde324120e2d9d82a1a3d
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288227"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>DoD(국방부) 영향 수준 2(IL2)

## <a name="dod-il2-overview"></a>DoD IL2 개요

DISA(Defense Information Systems Agency)는 DoD 클라우드 컴퓨팅 보안 요구 사항 [가이드(SRG)의](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)개발 및 유지 관리 업무를 담당하는 미국 DoD(국방부)의 기관입니다. SRG는 DoD가 클라우드 서비스 공급자(CSP)의 보안 상태를 평가하는 데 사용하는 기준 보안 요구 사항을 정의하여 CSP가 DoD 임무를 호스팅할 수 있는 PA(DoD Provisional Authorization)를 부여하는 결정을 지원합니다. 이전에 게시된 DoD 클라우드 보안 모델(CSM)을 통합, 위임 및 다시 사용하며 DoD RMF(위험 관리 프레임워크)에 매핑됩니다.

DISA는 CSP 사용을 계획하고 승인하는 DoD 기관 및 부서를 안내합니다. 또한 CSP 제품에서 DoD 표준 준수에 대한 문서를 제공하는 인증 프로세스인 SRG를 준수하는지 평가합니다. 적절한 경우 DoD PAS(Provisional Authorizations)를 적용하기 때문에 DoD 기관 및 지원 조직은 전체 승인 프로세스를 거치지 않고도 클라우드 서비스를 사용하여 시간 및 노력을 절약할 수 있습니다.

상용 클라우드 컴퓨팅 서비스 획득 및 사용에 대한  업데이트된 지침에 관한 [2014년 12월 15일 DoD CIO memo는](https://www.esi.mil/contentview.aspx?id=585) 'FedRAMP가 모든 DoD 클라우드 서비스에 대한 최소 보안 기준 역할을 할 것'으로 설명되어 있습니다. SRG는 모든 IL(정보 영향 수준)에서 FedRAMP 보통 기준을 사용하며 일부에서는 높은 기준을 고려합니다.

[SRG 섹션 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* 보안 제어의 DoD 사용 IL2 정보는 섹션 5.6.2에 설명된 직원 보안 요구 사항을 준수하는 경우 최소한 FedRAMP 보통 PA 및 DoD 수준 2 PA를 보유하는 CSP에서 호스팅될 수 있습니다. 그러나 이 방법을 통해 CSP가 임무 소유자가 요구하는 다른 보안 및 통합 요구 사항을 충족하지는 못합니다. [SRG 섹션 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2* 위치 및 분리 요구 사항에 따라 DoD IL2 PA에는 IL2 PA에 대한 요구 사항이 추가로 평가되지 않습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- 엔드포인트용 Microsoft Defender
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 미국 정부, Office 365 미국 정부 - 높음
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 및 DoD IL2

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure DoD IL2 서비스를 참조하세요.](/azure/compliance/offerings/offering-dod-il2)

## <a name="office-365-and-dod-il2"></a>Office 365 및 DoD IL2

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **GCC** | 작업 피드 서비스, Bing 서비스, Delve, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |
| **GCC High** | 작업 피드 서비스, Bing 서비스, Delve, Exchange Online Protection, Exchange Online, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |

### <a name="resources"></a>리소스

- [Microsoft 정부 솔루션](https://www.microsoft.com/enterprise/government)
- [DoD 클라우드 컴퓨팅 보안 요구 사항 가이드](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP 문서](https://www.fedramp.gov/documents/)
- 정보 시스템 및 조직을 위한 [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) 위험 관리 *프레임워크:* 보안 및 Life-Cycle 대한 시스템 관리 접근 방식
- 정보 시스템 및 조직에 대한 [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) 보안 및 개인 정보 *보호 컨트롤*
- DoD IT(DoD Information Technology)에 대한 DoD 명령 [8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework(RMF)*
