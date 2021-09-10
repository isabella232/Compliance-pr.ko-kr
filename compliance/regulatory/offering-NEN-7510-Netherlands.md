---
title: NEN 7510
description: 네덜란드의 조직은 NEN 7510 표준에 따라 환자 건강 데이터에 대한 통제력을 입증해야 합니다.
keywords: Microsoft 365, 규정 준수, 제안
ms.localizationpriority: high
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
ms.openlocfilehash: 438780ab33c99bae410218bdb54265093105c16b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948378"
---
# <a name="nen-7510"></a>NEN 7510

## <a name="nen-7510-overview"></a>NEN 7510 개요

환자 건강 정보를 처리하는 네덜란드의 조직은 NEN 7510 표준에 명시된 요구 사항과 일치하는 데이터 및 조직에 대한 통제력을 입증해야 합니다. Microsoft 자체는 NEN 7510의 적용을 받지 않지만 의료 부문의 클라우드 고객은 Microsoft 클라우드에 구축된 솔루션과 관련하여 NEN 7510을 준수하도록 해야 합니다. Microsoft 클라우드 서비스는 다양한 정기 인증 및 감사를 거치며 일부는 NEN 7510에 지정된 요구 사항과 밀접하게 관련된 요소를 포함합니다.

## <a name="microsoft-and-nen-75102011"></a>Microsoft와 NEN 7510:2011

Microsoft는 현재 인증 및 보장 진술문을 분석하고 [NEN 7510 커버리지 보고서](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports) (Service Trust Platform에서 사용 가능)를 작성했습니다. 이 보고서는 해당 인증 및 보장 진술문을 클라우드 서비스 제공 업체로서 Microsoft가 담당하는 NEN 7510 컨트롤에 매핑합니다. 이 문서는 고객이 환자 건강 정보의 저장 또는 처리를 위해 Microsoft 클라우드 서비스를 사용하여 NEN 7510을 준수하는지 확인하기 위해 구현해야 하는 다른 컨트롤을 결정하는 데 도움이 될 수 있습니다.

Azure 보안 및 규정 준수 청사진을 사용하여 NEN 7510 배포를 가속화하는 방법에 대해 알아보세요. [Microsoft 클라우드 다운로드 — Azure 및 Office 365 NEN7510-2011 Standard Coverage 사용자 가이드](https://aka.ms/Azure-NEN7510-2011)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure 및 Azure Government
- Intune
- Office 365

## <a name="office-365-and-iso-27001"></a>Office 365 및 ISO 27001

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | Azure Information Protection, Bookings, Delve, Exchange Online, Exchange Online, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Graph, Microsoft Teams, 웹용 Microsoft To-Do, MyAnalytics, Office 365 Cloud App Security, Office 365 그룹, Office 365 Video, 비즈니스용 OneDrive, Planner, Power Apps, Power Automate, Office 365용 Power BI, PowerApps, SharePoint Online, 비즈니스용 Skype, StaffHub, Stream, Sway, Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

- [Azure와 Office 365 NEN 7510:2011 Standard Coverage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a>질문과 대답

**Microsoft 클라우드 서비스를 사용하는 고객이 NEN 7510을 준수하나요?**

NEN 규정 준수를 입증하는 것은 의료 기관(‘고객’)의 책임입니다. 클라우드 서비스 공급 업체를 사용할 때, 고객은 일반적으로 공급 업체의 보증을 요구하고 자체(기타) 기술과 조직의 결정, 선택 및 프로세스를 추가합니다. 이러한 노력을 통해 NEN 7510 규정 준수에 대한 고객의 전반적인 평가가 이루어지며 검토 또는 인증을 위해 제 3의 감사관에게 제출할 수 있습니다. NEN 7510 적용 범위 보고서는 Microsoft 클라우드 서비스가 적용할 수있는 NEN 7510 컨트롤에 대한 통찰력을 제공하지만 종단간 규정 준수는 다루지 않습니다.

**Microsoft는 NEN 7510을 준수하나요?**

NEN 7510 규정 준수에 대한 책임은 Dutch Healthcare 조직에 적용됩니다. 조직은 정보보안 관리시스템을 구현하고 적절한 기술적 및 조직적 조치를 통해 위험을 해결해야 합니다. 클라우드 서비스 공급자 역할을 하는 Microsoft의 경우 NEN 7510 규정 준수는 목표가 아니며, 기술적으로도 가능하지 않습니다. 고객이 Microsoft 클라우드 서비스를 구현하거나 사용하는 경우 해당 서비스는 NEN 7510 평가 범위에 속할 수 있습니다. 그러나 조직에서 전체 NEN 7510 평가의 일부로 자체(기타) 컨트롤, 선택 및 프로세스를 추가해야 합니다. 이 보고서의 목적은 의료 기관이 NEN 7510을 준수하는 방식으로 Microsoft 클라우드 서비스를 채택할 수 있음을 보여주기 위한 것입니다.

**보고서에 100% 적용범위가 표시되지 않습니다. NEN 7510 규정 준수가 적합하지 않나요?**

Microsoft 클라우드 서비스는 Dutch Healthcare 내의 조직이 NEN 7510 규정 준수 요구를 충족할 수 있도록 많은 컨트롤을 제공합니다. 그러나 조직에서는 자체 구현 선택, 기타 기술 컨트롤 및 관리 프로세스를 통해 이러한 공급 업체 보증을 보완해야 합니다. 이 보고서는 적용 가능한 전체 컨트롤 목록에 대해 이미 94%이상의 직접적인 적용 범위를 보여줍니다. 나머지 컨트롤의 경우, Microsoft는 해당 컨트롤의 준수 여부를 보여주는 방법에 대한 보고서의 지침을 제공합니다.

> [!NOTE]
> 전체 컨트롤 목록을 구현하는 것이 NEN 7510의 주요 목적은 아닙니다 (Microsoft 온라인 서비스의 광범위한 적용 범위가 도움이 되더라도). NEN 7510은 조직이 어떤 통제가 적용 가능한지를 결정하기 위해 사용할 수 있는 리스크기반 정보보안 시스템의 구현을 의무화합니다.

**NEN 7510 커버리지 보고서는 법적 구속력이 있는 문서인가요?**

아니요. 고객의 내부 NEN 7510 보증 프로세스를 지원하는 도구이며 NEN 7510 준수가 실현 가능하다는 확신과 신뢰를 구축하는 데 도움이 됩니다. 보고서 (독립 감사인, KPMG가 만든)는 설명적인 지위를 가지며 법적 면책 조항을 포함합니다.

**Microsoft에서 보고서 비용을 지불했나요?**

Microsoft는 NEN 7510 표준의 글로벌 보증과 컨트롤간의 매핑을 만들었습니다. 그런 다음 Microsoft는 KPMG (독립 감사인)를 고용하여 NEN 7510에 대한 컨트롤 매핑에 대한 독립적인 검토를 수행하여 보고서를 작성했습니다.

**이 보고서를 공유할 수 있나요?**

이 보고서는 고객 정보 전용이며 Microsoft Service Trust Portal 이외의 다른 채널을 통해 복사 또는 공개되지 않을 것이라는 근거로 기밀 유지 계약 (NDA)에 따라 제공됩니다.

고객은 규정 준수 또는 보장 프로세스의 일부로 자체 내부 또는 외부 감사인을 사용하여 보고서를 공유할 수 있습니다.

## <a name="resources"></a>리소스

- [NEN 정보](https://www.nen.nl/About-NEN.htm)
- [NEN 7510:2011 표준](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
