---
title: DoD(국방부) 영향 수준 5(IL5)
description: Microsoft가 IL5(국방부) IL5(영향 수준 5) 표준을 충족하는 방법을 학습합니다.
keywords: Microsoft 365, 규정 준수, 제품
ms.localizationpriority: medium
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
ms.openlocfilehash: c0c987dc5fbe2bee60508f0fab7dbdb8dce97857
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482843"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>DoD(국방부) 영향 수준 5(IL5)

## <a name="dod-il5-overview"></a>DoD IL5 개요

DISA(Defense Information Systems Agency)는 DoD 클라우드 컴퓨팅 보안 요구 사항 [가이드(SRG)의](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)개발 및 유지 관리 업무를 담당하는 미국 DoD(국방부)의 기관입니다. SRG는 DoD가 클라우드 서비스 공급자(CSP)의 보안 상태를 평가하는 데 사용하는 기준 보안 요구 사항을 정의하여 CSP가 DoD 임무를 호스팅할 수 있는 PA(DoD Provisional Authorization)를 부여하는 결정을 지원합니다. 이전에 게시된 DoD 클라우드 보안 모델(CSM)을 통합, 위임 및 다시 사용하며 DoD RMF(위험 관리 프레임워크)에 매핑됩니다.

DISA는 CSP 사용을 계획하고 승인하는 DoD 기관 및 부서를 안내합니다. 또한 CSP 제품에서 DoD 표준 준수에 대한 문서를 제공하는 인증 프로세스인 SRG를 준수하는지 평가합니다. 적절한 경우 DoD PAS(Provisional Authorizations)를 적용하기 때문에 DoD 기관 및 지원 조직은 전체 승인 프로세스를 거치지 않고도 클라우드 서비스를 사용하여 시간 및 노력을 절약할 수 있습니다.

[SRG 섹션 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) 정보 영향 수준에 *따라* IL5 정보는 다음을 다 설명합니다.

- IL4에서 제공한 것보다 높은 수준의 보호가 필요한 CUI(제어된 미분분 정보)
    - [CUI 레지스트리는](https://www.archives.gov/cui) 임원 분기에 의해 보호되는 특정 정보 범주를 제공합니다. 예를 들어 CUI 범주 목록에는 20개 이상의 범주 그룹이 [포함됩니다.](https://www.archives.gov/cui/registry/category-list)
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *비연속* 시스템 및 조직에서 제어된 미분분 정보 보호는 연방 기관이 비연속 조직과 수립한 계약 또는 기타 계약에 연방 기관을 위해 고안되었습니다.

- NSS(국가 보안 시스템)
    - 정보 시스템을 국가 보안 시스템으로 식별하기 위한 [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)  지침은 NSS의 정의를 제공합니다.
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems에서는* 연방 기관이 국가 보안 정보를 분류하기 위해 적용해야 하는 보안 표준에 대한 지침을 제공합니다.

상용 클라우드 컴퓨팅 서비스 획득 및 사용에 대한  업데이트된 지침에 관한 [2014년 12월 15일 DoD CIO memo는](https://www.esi.mil/contentview.aspx?id=585) 'FedRAMP가 모든 DoD 클라우드 서비스에 대한 최소 보안 기준 역할을 할 것'으로 설명되어 있습니다. SRG는 모든 IL(정보 영향 수준)에서 FedRAMP 보통 기준을 사용하며 일부에서는 높은 기준을 고려합니다.

[SRG 섹션 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *FedRAMP* 보안 제어의 DoD 사용에 대해 DoD FedRAMP+ 컨트롤 및 C/CS(제어 향상)와 SRG의 요구 사항으로 보완된 FedRAMP High PA는 IL5에서 DoD PA를 수여하는 데 대한 CSP를 평가하는 데 사용되었습니다. FedRAMP High PA의 기초로 사용되는 C/CE 기준에 상관없이, IL5에서 DoD PA를 수여하기 전에 추가 고려 사항 및/또는 요구 사항을 평가하고 승인해야 합니다. 특히, [SRG 섹션 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+ 보안 컨트롤/개선* 사항 표 2에서는 DoD IL5 PA에 FedRAMP High 기준을 초과하는 추가 C/C/C 10개가 필요하다고 설명했습니다.

또한 [SRG 섹션 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5* 위치 및 분리 요구 사항에 따라 수준 5 PA에 대해 다음 요구 사항을 충족해야 합니다.

- DoD와 연방 정부 테넌트/임무 간의 가상/논리적 분리만으로 충분합니다. 테넌트/임무 시스템 간의 가상/논리적 분리가 필요합니다.
- DoD/비연방 정부 테넌트(즉, 공용, 로컬/주 정부 테넌트)와 물리적으로 분리해야 합니다.
- CSP는 DoD 및 커뮤니티 정보에 대한 잠재적인 액세스를 미국 시민인 CSP 직원으로 제한합니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure
- Dynamics 365 고객 서비스
- 엔드포인트용 Microsoft Defender(이전의 Microsoft Defender Advanced Threat Protection)
- Microsoft Graph
- Microsoft Stream
- Office 365 US Government Defense
- Power Automate(과거 Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 및 DoD IL5

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure DoD IL5 제공을 참조하세요.](/azure/compliance/offerings/offering-dod-il5)

## <a name="office-365-and-dod-il5"></a>Office 365 및 DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **DoD** | 작업 피드 서비스, Bing 서비스, Exchange Online, Exchange Online Protection, 지능형 서비스, Microsoft Teams, Office 365 고객 포털, Office Online, Office 서비스 인프라, Office 사용 현황 보고서, 비즈니스용 OneDrive, 사용자 카드, SharePoint Online, 비즈니스용 Skype, Windows Ink |

### <a name="attestation-documents"></a>Attestation documents

미국 정부 고객은 패키지 액세스 Office 365 제출하여 FedRAMP 마켓플레이스에서 직접 미국방부 [FedRAMP](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) 설명서를 요청할 수 있습니다. FedRAMP에서 직접 FedRAMP 보안 패키지에 액세스하려면 .gov 또는 .mil 전자 메일 주소가 있어야 합니다.

SSP(시스템 보안 계획), 지속적인 모니터링 보고서, POA M(작업 계획 및 중요 시점) 등을 비롯한 FedRAMP 및 DoD 설명서를 선택하면 서비스 보안 포털 감사 보고서 \& [- FedRAMP 보고서](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) 섹션에서 NDA 및 보류 중인 액세스 권한 부여를 보류 중인 고객이 사용할 수 있습니다. Microsoft 계정 담당자에게 지원을 요청하세요.

### <a name="resources"></a>리소스

- [Microsoft 정부 솔루션](https://www.microsoft.com/enterprise/government)
- [DoD 클라우드 컴퓨팅 보안 요구 사항 가이드](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP 문서](https://www.fedramp.gov/documents/)
- DoD IT(DoD Information Technology)에 대한 DoD 명령 [8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework(RMF)*
- 정보 시스템 및 조직을 위한 [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) 위험 관리 *프레임워크:* 보안 및 Life-Cycle 대한 시스템 관리 접근 방식
- 정보 시스템 및 조직에 대한 [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) 보안 및 개인 정보 *보호 컨트롤*
- 정보 시스템을 국가 보안 시스템으로 식별하기 위한 [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *지침*
- 국가 보안 시스템에 대한 [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) 보안 분류 및 제어 *선택*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) 비연산 시스템 및 조직에서 제어된 *미분분 정보 보호*
- CUI(제어된 분류되지 않은 정보) [레지스트리](https://www.archives.gov/cui) 및 CUI [범주 목록입니다.](https://www.archives.gov/cui/registry/category-list)
