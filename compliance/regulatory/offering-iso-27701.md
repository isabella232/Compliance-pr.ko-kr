---
title: ISO/IEC 27701 개인 정보 관리 시스템(PIMS)
description: 글로벌 데이터 처리 공급 체인 내의 컨트롤러 및 프로세서 간의 개인 정보 보호 책임 및 규정 준수를 지원하기 위한 ISO/IEC 27701 표준입니다.
keywords: Microsoft 365, 규정 준수, 제안
localization_priority: Priority
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
ms.openlocfilehash: 5f25347be42a34764ff78106700f7132d377bc54
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508460"
---
# <a name="isoiec-27701-privacy-information-management-system-pims"></a>ISO/IEC 27701 PIMS(개인 정보 관리 시스템)

## <a name="privacy-information-management-system-pims-overview"></a>개인 정보 관리 시스템(PIMS) 개요

유럽연합의 GDPR(일반 데이터 보호 규정)은 전 세계적으로 개인 정보 보호 규제 및 규정 준수의 새로운 시대를 열었습니다. GDPR을 모델로 한 더 많은 개인 정보 보호 규정이 여러 관할 지역에서 제정되었습니다(시장/산업 또는 물리적 위치). 따라서 조직은 증가하는 개인 정보 보호 규정의 준수를 보장하기 위해 정책과 절차를 구현해야 합니다. 또한, 데이터 수집과 처리가 급격히 증가하고 있는 급속한 디지털 전환의 중심에 있습니다. 데이터와 관련된 데이터 볼륨 및 규제 요구사항이 동시에 증가함에 따라 모든 유형의 조직에서 규정 준수가 점점 더 복잡해지고 있습니다.

새로운 국제 표준 [ISO/IEC 27701 PIMS(개인정보 관리 시스템)](https://www.iso.org/standard/71670.html)(이전의 제도 기간 중 ISO/IEC 27552로 알려져 있음)는 조직이 개인정보 보호 규제 요건을 조정할 수 있도록 지원합니다. 이 표준은 GDPR을 비롯한 다양한 규정에 따라 매핑될 수 있는 포괄적인 운영 제어 기능을 간략히 설명합니다. 일단 매핑되면 PIMS 운영 통제는 개인 정보 보호 전문가에 의해 구현되고 내부 또는 제3자 감사인에 의해 감사되어 인증 및 포괄적인 적합성 증거를 얻습니다.

## <a name="compliance-challenges"></a>규정 준수 문제

공급업체가 PIMS에 대해 인증을 받을 것으로 예상하는 것은 조직의 규모에 관계없이 공급업체와 파트너의 책임 있는 개인 정보 보호 관행을 확립하는 데 효과적입니다. ISO/IEC 27701은 다음과 같은 세 가지 주요 규정 준수 과제를 해결합니다.

- **조율할 규정 요구 사항이 너무 많음**: 법용 운영 제어 집합을 사용하여 여러 규제 요구 사항을 조정하는 것이 일관되고 효율적인 구현를 가능하게 합니다.
- **규정을 통해 규정을 감사하는 데 너무 많은 비용이 듦**: 감사자(내부 및 제3자)는 하나의 감사 주기 내에서 범용 운영 제어 집합을 사용하여 규제 준수를 평가할 수 있습니다.
- **증명을 사용하지 않는 규정 준수 약속은 잠재 위험 요소가 있음**: 개인 정보 이동을 포함한 상업적 계약이 규정 준수에 대한 인증을 보증할 수 있습니다.

## <a name="too-many-regulatory-requirements-to-juggle"></a>조율할 규정 요구 사항이 너무 많음

ISO/IEC 27701은 컨트롤러 및 프로세서에 대한 GDPR의 관련 요구사항에 따라 매핑된 표준의 작동 제어를 포함하는 부속서를 포함합니다. 이 매핑은 개인 정보 보호 규정이 ISO 프레임워크로 어떻게 운영될 수 있는지를 보여주는 예에 불과합니다. 다른 규정과의 추가 매핑을 사용할 수 있고 검증이 완료되면 표준의 운영 통제를 규제 검토에서 구현으로 직접 전송할 수 있습니다. 이 범용 프레임워크를 통해 조직은 '바퀴를 재발명'하지 않고도 관련 규제 요건을 안정적으로 운영할 수 있습니다. 개인 정보 보호 커뮤니티가 다른 규정을 매핑하고 기존 매핑을 검증할 수 있도록 하기 위해 보류 중인 오픈 소스 프로젝트가 진행 중입니다. 향후 발표를 계속 지켜봐 주세요.

## <a name="too-costly-to-audit-regulation-by-regulation"></a>규정을 통해 규정을 감사하는 데 너무 많은 비용이 듦

현 상황에 대한 개략적인 설명부터 살펴 보겠습니다. 다양한 관할 지역에서 개인정보 보호규제가 더 많이 시행됨에 따라, 준수 여부를 입증해야 한다는 압력도 가중될 것입니다. 그러나 모든 규정에서 고유한 감사를 요구하면 상이한 규제 인증 비용이 엄청나게 증가합니다. 또한 PIMS는 범용 운영 제어의 개요를 설명함으로써 여러 규제 요구사항에 대해 감사하고 잠재적으로 인증할 수 있는 범용 준수 프레임워크를 간략히 설명합니다.

공식적인 GDPR 인증은 유럽 규제 당국에 의해 보류 중인 승인 결정을 요구한다는 점을 인식하는 것이 중요합니다. PIMS와 GDPR의 정렬은 명백하지만, PIMS 인증은 규제 결정이 확정될 때까지 공식적인 GDPR 인증으로서가 아니라 GDPR 규정 준수의 증거로 받아들여야 합니다.

## <a name="promises-of-compliance-without-proof-is-potentially-risky"></a>증명을 사용하지 않는 규정 준수 약속은 잠재 위험 요소가 있음

오늘날의 조직에서는 파트너 조직이나 공동 컨트롤러, 클라우드 공급업체와 같은 프로세서, 동일한 프로세서를 지원하는 벤더와 같은 하위 프로세서와 같은 비즈니스 파트너의 긴밀한 네트워크를 통해 복잡한 데이터 전송을 수행합니다. 이 네트워크의 모든 부분에서 규정을 준수하지 않을 경우 공급망 전체에 걸쳐 규정 준수 문제가 발생할 수 있습니다. 이 부분에서 규정 준수에 대한 검증은 이러한 조직 간의 계약 조건에 의해 제공되는 보장 이상의 가치가 있을 수 있습니다. 세계경제는 이러한 조직의 대부분이 전 세계에 분산되어 있다고 규정하므로, ISO의 국제 표준을 사용하여 네트워크 전체에 걸쳐 규정 준수를 관리하는 것이 실용적입니다.

이러한 규정 준수에 의존하여 표준 인증의 중요성이 높아집니다. 모든 기업과 조직이 이러한 인증을 획득해야 하는 것은 아니지만, 대부분은 인증을 획득하는 파트너와 공급업체로부터 혜택을 받을 수 있습니다. 특히 민감한 데이터 처리량이나 많은 양의 데이터 처리가 수반되는 경우에는 더욱 그렇습니다.

## <a name="building-blocks-of-the-standard"></a>표준의 구성 요소

PIMS는 가장 널리 채택된 정보 보안 관리 국제 표준 중 하나인 [ISO/IEC 27001](offering-iso-27001.md) 위에 구축되었습니다. 조직에서 ISO/IEC 27001에 대해 이미 잘 알고 있다면 PIMS의 새로운 개인 정보 보호 제어를 통합하는 것이 논리적이고 더 효율적입니다. 이는 두 가지 모두에 대한 구현과 감사가 비용이 적게 들고 달성하기 쉽다는 것을 의미합니다.

ISO/IEC 27001 및 PIMS의 주요 사항:

- ISO/IEC 27001는 세계에서 가장 많이 사용되는 ISO 표준 중 하나로, 많은 회사가 이미 그에 대한 인증을 획득했습니다.
- PIMS에는 개인 정보 보호 및 보안 사이의 차이를 파악하는 데 도움이 되는 새로운 컨트롤러와 프로세서별 제어가 포함되어 있습니다. 이는 조직의 두 가지 별도의 기능일 수 있는 요소 간의 통합 지점을 제공합니다.
- 프라이버시는 보안에 따라 다릅니다. 마찬가지로 PIMS는 보안 관리를 위해 ISO/IEC 27001에 의존합니다. PIMS 인증은 ISO/IEC 27001 인증의 연장선상에서 취득해야 하며, 독립적으로 취득할 수 없습니다.

## <a name="what-should-your-organization-do-with-pims"></a>조직은 PIMS로 무엇을 해야 하나요?

조직의 규모와 컨트롤러 또는 프로세서에 관계없이 조직은 자신의 조직에 대한 인증을 추구하거나 비즈니스 요구사항에 따라 공급업체 또는 공급업체에 인증을 요청하는 것을 고려해야 합니다. 이는 특히 민감한 또는 많은 양의 개인 데이터를 처리하는 프로세서, 하위 프로세서 및 공동 컨트롤러에 적용됩니다. 어떤 경우에도 조직은 자체 제품 및 서비스에 대한 인증이 적합한지 판단하기 위해 비즈니스 요구사항을 평가해야 합니다.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 범위 내 클라우드 서비스

- Azure, Azure Government, Azure Germany
- Azure DevOps Services
- Microsoft Cloud App Security
- Dynamics 365, Dynamics 365 Government, Dynamics 365 Germany
- Microsoft Graph
- Microsoft Healthcare Bot
- Intune
- Microsoft Managed Desktop
- Power Automate(과거 Microsoft Flow)
- PowerApps
- Power BI
- Power BI Embedded
- Power Virtual Agents
- Microsoft Stream
- Microsoft 위협 전문가
- Windows Defender Advanced Threat Protection

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

- [Azure, Dynamics 365 및 온라인 서비스: ISO27701 인증](https://aka.ms/azureiso27701cert)
- [Azure, Dynamics 365 및 온라인 서비스: ISO27701 평가 보고서](https://aka.ms/azureiso27701report)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)는 사용자 조직의 준수 상태를 이해하고 위험을 줄이기 위한 활동에 도움을 주는 [Microsoft 365 규정 준수 센터](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규정에 관한 평가를 작성하기 위한 프리미엄 문서 서식을 제공합니다. 준수 관리자의 **평가 문서 서식 페이지** 에서 문서 서식을 찾을 수 있습니다. [준수 관리자에서 평가를 빌드](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments)하는 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [구매에 대한 ISO/IEC 27701(PIMS)](https://www.iso.org/standard/71670.html)
- [PIMS에 대한 BSI 백서 및 콘텐츠](https://www.bsigroup.com/globalassets/localfiles/en-gb/data-protection/bsi_privacy_matters_white_paper-web.pdf)
- [PIMS 소개 비디오](https://www.microsoft.com/videoplayer/embed/RE3uaQJ)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
