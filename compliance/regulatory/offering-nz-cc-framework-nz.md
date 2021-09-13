---
title: 뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 보호 고려 사항
description: Microsoft NZ는 뉴질랜드 클라우드 컴퓨팅 프레임워크에 게시된 질문을 해결합니다.
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
ms.openlocfilehash: 6785c459f8350714b8e4636a0f1a5dc9f4ff667d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160541"
---
# <a name="new-zealand-government-information-security-and-privacy-considerations-ispc"></a>뉴질랜드 정부 정보 보안 및 개인 정보 보호 고려 사항(ISPC)

## <a name="new-zealand-government-information-security-and-privacy-considerations-overview"></a>뉴질랜드 정부 정보 보안 및 개인 정보 보호 고려 사항 개요

2015년 10월 뉴질랜드 정부는 공공 부문에서 정보 기술을 사용하는 '클라우드 우선' 정책을 재확인하는 수정된 모든 정부 ICT 전략을 인정했습니다. 수정된 전략은 NZ 정부 최고 정보 책임자(GCIO)의 권한으로 개발 및 구현된 '클라우드 컴퓨팅 위험 및 보증 프레임워크'를 보유합니다.

정부는 클라우드 서비스를 평가하고 채택할 때 모든 뉴질랜드 주 정부 기관이 이 프레임워크 내에서 작업할 것으로 기대합니다. '클라우드 컴퓨팅 요구 사항'에서는 정부의 클라우드 정책 내역과 함께 클라우드 서비스를 채택할 때 기관이 해야 하는 작업을 간략하게 소개합니다.

GCIO는 NZ 정부 기관이 잠재적인 클라우드 솔루션에 대해 일관되고 강력한 실사 수행을 지원하기 위해 클라우드 [컴퓨팅: ISPC(정보](https://www.digital.govt.nz/dmsdocument/1~cloud-computing-information-security-and-privacy-considerations/html)보안 및 개인 정보 보호 고려 사항)를 게시했습니다. 이 문서에는 데이터 주권, 개인 정보, 보안, 거버넌스, 기밀성, 데이터 무결성, 가용성 및 인시던트 대응 및 관리에 초점을 맞추는 100개 이상의 질문이 포함되어 있습니다. ISPC는 클라우드 서비스 공급자가 공식적인 규정 준수를 입증해야 하는 NZ 정부 표준을 정의하지 않습니다. 그러나 문서에 설정된 많은 질문은 클라우드 서비스 공급자가 다양한 관련 표준을 준수하는 방식에 대한 이해의 중요성을 강조합니다.

## <a name="microsoft-and-new-zealand-government-cloud-computing-security-and-privacy-considerations"></a>Microsoft 및 뉴질랜드 정부 클라우드 컴퓨팅 보안 및 개인 정보 보호 고려 사항

기관이 Microsoft 엔터프라이즈 클라우드 서비스를 분석하고 평가할 수 있도록 Microsoft 뉴질랜드는 엔터프라이즈 클라우드 서비스가 Microsoft 클라우드 서비스가 '클라우드 컴퓨팅 ISPC'에 설정된 질문을 Microsoft 클라우드 서비스가 인증된 표준에 연결하여 해결 방법을 보여 주는 문서를 제작했습니다. 이러한 인증은 Microsoft가 개인 정보 및 보안 위험을 효과적으로 완화하고 데이터 주권 문제를 해결하기 위해 클라우드 서비스를 설계, 구축 및 운영하고 공공 부문 고객 모두에게 제공하는 방법의 핵심입니다. 클라우드 [컴퓨팅 ISPC에 대한 Azure](https://azure.microsoft.com/resources/microsoft-azure-response-to-nz-gcio-cloud-computing-information-security-privacy-considerations/) 응답은 고객이 다운로드할 수 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure 및 Azure Government
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Intune
- Office 365
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스

## <a name="office-365-and-ispc"></a>Office 365 및 ISPC

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | Exchange Online, SharePoint Online, 비즈니스용 Skype |

>[!Note]
>Microsoft NZ는 GCIO 팀과 함께 통합을 위한 참조 아키텍처를 개발하고 Exchange Online: SEEMail 통합 및 참조 아키텍처에 Office 365 참조 아키텍처를 개발하고 있습니다.

## <a name="frequently-asked-questions"></a>자주 묻는 질문

**프레임워크는 누구에게 적용하나요?**

GCIO 위임, 공공 및 비공용 서비스 부서, 20개 교육구 보건 위원회 및 7개 교육구 기관에 속하는 조직은 클라우드 서비스 사용을 결정할 때 프레임워크를 준수해야 합니다.

**기관에서 ICT 시스템의 인증 프로세스에서 이 프레임워크에 대한 Microsoft의 응답을 사용할 수 있나요?**

기관이 뉴질랜드 정보 보안 설명서에 따라 ICT 시스템의 인증 및 [](https://go.microsoft.com/fwlink/p/?linkid=2099496)인증을 획득해야 하는 경우 이러한 응답을 분석의 일부로 사용할 수 있습니다.

## <a name="resources"></a>리소스

- [해상에서 호스팅되는 Office 생산성 서비스에 대한 보안 요구 사항: Office 365](https://aka.ms/o365-gcio-conformance-guidance)
- [NZ Government ICT Strategy 2015](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [클라우드 컴퓨팅: ISPC(정보 보안 및 개인 정보 보호 고려 사항)](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [Microsoft 온라인 서비스 사용 약관](https://aka.ms/Online-Services-Terms)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a>클라우드 컴퓨팅 IPSC에 대한 Microsoft 응답

- [Azure](https://aka.ms/Azure-NZ-response)
- [Dynamics 365](https://www.microsoft.com/download/details.aspx?id=103390)
- [Intune](https://aka.ms/Intune-NZ-response)
- [Office 365](https://aka.ms/O365-NZ-Response)
- [Power BI](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)
