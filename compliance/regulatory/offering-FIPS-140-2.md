---
title: FIPS(Federal Information Processing Standard) 게시 140-2
description: Microsoft는 암호화 모듈이 미국 연방 정보 처리 표준을 준수하는지 인증합니다.
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
ms.openlocfilehash: 0e087393901b76a798c4a4ea3bef25fad8dcda84
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161021"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>FIPS(Federal Information Processing Standard) 게시 140-2

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2 표준 개요

FIPS(Federal Information Processing Standard) 발행물 140-2는 1996년 정보 기술 관리 재구성법의 5131조에 정의된 정보 기술 제품에서 암호화 모듈에 대한 최소 보안 요구 사항을 정의하는 미국 정부 표준입니다.

미국 [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) NIST(National Institute of Standards and Technology) 및 CCCS(Canadian Institute for Cyber Security)의 공동 노력인 CMVP(암호화 모듈 유효성  검사 프로그램)는 암호화 모듈의 보안 요구 사항(예: FIPS 140-2) 및 관련 FIPS 암호화 표준에 대한 암호화 모듈의 유효성을 검사합니다. FIPS 140-2 보안 요구 사항에는 암호화 모듈의 디자인 및 구현과 관련된 11개 영역이 포함됩니다. NIST 정보 기술 실험실은 모듈에서 FIPS 승인 암호화 알고리즘의 유효성을 검사하는 관련 프로그램을 운영합니다.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>FIPS 140-2 유효성 검사에 대한 Microsoft의 접근 방식

Microsoft는 2001년 표준이 시작된 이후 암호화 모듈의 유효성을 검사하여 140-2 요구 사항을 충족하기 위한 적극적인 약속을 유지하고 있습니다. Microsoft는 NIST(National Institute of Standards and Technology) CMVP(암호화 모듈 유효성 검사 [프로그램)에서](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) 암호화 모듈의 유효성을 검사합니다. 많은 클라우드 서비스를 포함한 여러 Microsoft 제품은 이러한 암호화 모듈을 사용합니다.

Microsoft Windows 모듈, 각 모듈에 대한 보안 정책 및 CMVP 인증서 세부 정보 카탈로그에 대한 기술 정보는 Windows 및 Windows [Server FIPS 140-2](https://aka.ms/AA6ehud)콘텐츠를 참조하세요.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

현재 CMVP FIPS 140-2 구현 지침에서는 클라우드 서비스 자체에 대한 FIPS 140-2 유효성 검사를 제외합니다. 클라우드 서비스 공급자는 클라우드 서비스를 구성하는 컴퓨팅 요소에 대해 FIPS 140 유효성이 검사된 암호화 모듈을 획득하고 작동하도록 선택할 수 있습니다. FIPS 140-2 유효성이 검사된 구성 요소가 포함된 Microsoft 온라인 서비스는 다음과 같습니다.

- Azure 및 Azure Government
- Dynamics 365 및 Dynamics 365 Government
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 및 FIPS 140-2

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure FIPS 140-2 제공을 참조하세요.](/azure/compliance/offerings/offering-fips-140-2)

## <a name="office-365-and-fips-140-2"></a>Office 365 및 FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| Office 365, GCC, GCC High, DoD | [FIPS 140-2 유효성 검사 참조](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>자주 묻는 질문

**'FIPS 140 유효성 검사' 및 'FIPS 140 호환'의 차이점은 무엇입니까?**

'FIPS 140 Validated'는 암호화 모듈 또는 모듈을 추가하는 제품이 FIPS 140-2 요구 사항을 충족하는 것으로 CMVP에 의해 유효성을 검사('인증')했다는 의미입니다. 'FIPS 140 호환'은 암호화 기능에 FIPS 140 유효성 검사 제품을 사용 하는 IT 제품에 대한 업계 용어입니다.

**Microsoft는 언제 FIPS 140 유효성 검사를 진행하나요?**

모듈 유효성 검사를 시작하는 케이던스가 Windows 10 서버의 기능 Windows 정렬됩니다. 소프트웨어 산업이 발전함에 따라 운영 체제가 월별 소프트웨어 업데이트와 함께 더 자주 릴리스됩니다. Microsoft는 기능 릴리스에 대한 유효성 검사를 진행하지만 릴리스 사이에는 암호화 모듈의 변경 내용을 최소화하기 위해 노력합니다.

**FIPS 140 유효성 검사에 포함되는 컴퓨터는 무엇입니까?**

Microsoft는 Windows 10 및 Windows 실행되는 하드웨어 구성의 대표 샘플에서 암호화 모듈의 유효성을 검사합니다. 일반적으로 환경에서 하드웨어를 사용하는 경우 유효성 검사 프로세스에 사용되는 샘플과 유사한 이 FIPS 140-2 유효성 검사를 수락하는 것이 일반적입니다.

**NIST 웹 사이트에는 여러 모듈이 나열되어 있습니다. 기관에 어떤 것이 적용되는지 어떻게 알 수 있나요?**

FIPS 140-2를 통해 유효성이 검사된 암호화 모듈을 사용하려면 사용하는 버전이 유효성 검사 목록에 나타나는지 확인해야 합니다. CMVP 및 Microsoft는 제품 릴리스별로 구성되는 유효성이 검사된 암호화 모듈 목록을 유지 관리하며, Windows 시스템에 설치되는 모듈을 식별합니다. 규격으로 시스템을 구성하는 데 대한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)

**인증서에 대한 'FIPS 모드에서 작동하는 경우'는 무엇을 의미하나요?**

이 주의는 FIPS 140-2 보안 정책과 일관된 방식으로 암호화 모듈을 사용하기 위해 필요한 구성 및 보안 규칙을 따라야 하다는 경고를 독자에게 알릴 수 있습니다. 각 모듈에는 자체 보안 정책(작동할 보안 규칙의 정확한 사양)이 있으며 승인된 암호화 알고리즘, 암호화 키 관리 및 인증 기술을 사용합니다. 보안 규칙은 각 모듈에 대한 보안 정책에서 정의됩니다. CMVP를 통해 유효성이 검사된 각 모듈에 대한 보안 정책에 대한 링크를 비롯한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)

**FedRAMP에 FIPS 140-2 유효성 검사가 필요합니까?**

예. FedRAMP(Federal Risk and Authorization Management Program)는 FIPS 유효성이 검사된 암호화 또는 NSA 승인 암호화 사용을 규정하는 [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 암호화 보호를 포함하여 [NIST SP 800-53 개정 4에](https://nvd.nist.gov/800-53/Rev4/)정의된 제어 기준을 활용합니다.

**기관의 인증 프로세스에서 Microsoft의 FIPS 140-2 준수를 사용할 수 있나요?**

FIPS 140-2를 준수하려면 암호화 모듈이 FIPS 승인 알고리즘만 사용하는지 확인을 포함하는 FIPS 승인된 작업 모드에서 실행하도록 시스템을 구성해야 합니다. 규격으로 시스템을 구성하는 데 대한 자세한 내용은 Windows 및 Windows [Server FIPS 140-2 콘텐츠를 참조하세요.](https://aka.ms/AA6ehud)

**FIPS 140-2와 일반 조건 간의 관계는 무엇입니까?**

서로 다르지만 상호 보완적인 두 가지 보안 표준입니다. FIPS 140-2는 소프트웨어 및 하드웨어 암호화 모듈의 유효성을 검사하도록 특별히 디자인된 반면, 공통 조건은 IT 소프트웨어 및 하드웨어 제품의 보안 기능을 평가하도록 디자인되었습니다. 일반적인 기준 평가는 종종 FIPS 140-2 유효성 검사를 사용하여 기본 암호화 기능이 제대로 구현되었는지 확인합니다.

### <a name="resources"></a>리소스

- [암호화 모듈에 대한 FIPS Pub 140-2 보안 요구 사항](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST 암호화 모듈 유효성 검사 프로그램](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server 및 FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
