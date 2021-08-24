---
title: PCI(Payment Card Industry) DSS(Data Security Standard)
description: Azure, SharePoint Online 및 비즈니스용 OneDrive는 Payment Card Industry Data Security 표준 수준 1 버전 3.2를 준수합니다.
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
ms.openlocfilehash: 09c18fce6544984a7e9d639e68d0f0201c584768
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482863"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>PCI(Payment Card Industry) DSS(Data Security Standard)

## <a name="pci-dss-overview"></a>PCI DSS 개요

PCI(Payment Card Industry) DSS(Data Security Standard)는 신용 카드 데이터에 대한 통제를 강화하여 사기를 방지하도록 고안된 글로벌 정보 보안 표준입니다. 모든 규모의 조직은 Visa, MasterCard, American Express, Discover, JCB(Japan Credit Bureau) 등 5개 주요 신용 카드 브랜드의 결제 카드를 수락하는 경우 PCI DSS 표준을 따라야 합니다. 지불 및 카드 소유자 데이터를 저장, 처리 또는 전송하는 모든 조직은 PCI DSS를 준수해야 합니다.

## <a name="microsoft-and-pci-dss"></a>Microsoft와 PCI DSS

Microsoft는 승인된 QSA(Qualified Security Assessor)를 사용하여 연간 PCI DSS 평가를 완료했습니다. 감사자는 인프라, 개발, 운영, 관리, 지원 및 범위 내 서비스 검증을 포함하여 Microsoft Azure, 비즈니스용 Microsoft OneDrive 및 Microsoft SharePoint Online 환경을 검토했습니다. PCI DSS는 거래량을 기준으로 네 가지 규정 준수 수준을 지정합니다. Azure, 비즈니스용 OneDrive, SharePoint Online은 PCI DSS 버전 3.2의 서비스 공급자 수준 1(최고 거래량이 연간 6백만 건 이상)의 규정 준수 인증을 획득했습니다.

평가는 AoC(Attestation on Compliance)로 제공되며 이는 고객이 열람 가능하고 QSA에서 발행한 Report on Compliance (RoC)에서 볼 수 있습니다. 규정 준수에 대한 유효 기간은 감사를 통과하여 평가자로부터 AoC를 받은 시점부터 AoC에 서명한 날짜가 포함된 연도의 말일까지입니다. 

카드 데이터 전용 네트워크(CDE) 또는 카드 처리 서비스를 개발하려는 고객은 많은 기본적인 부분에서 이러한 검증을 사용할 수 있습니다. 이를 통해 자체적으로 PCI DSS 인증을 얻기 위한 관련된 작업과 비용을 줄일 수 있습니다.

Azure, 비즈니스용 OneDrive, SharePoint Online의 PCI DSS 규정 준수 상태가 고객이 이러한 플랫폼에서 빌드하거나 호스팅하는 서비스에 대한 PCI DSS 인증으로 자동으로 전환되는 것은 아닙니다. 고객은 일부 PCI DSS 요구 사항을 준수하는지 확인해야 할 책임이 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- Azure 및 Azure Government
- Intune
- Microsoft Cloud App Security
- [엔드포인트용 Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- 비즈니스용 OneDrive 및 SharePoint Online(미국에만 해당)
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 PowerApps 클라우드 서비스
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power Automate(이전 Microsoft Flow) 클라우드 서비스
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure, Dynamics 365 및 PCI DSS

Azure, Dynamics 365 및 기타 온라인 서비스 규정 준수에 대한 자세한 내용은 [Azure PCI DSS 제품](/azure/compliance/offerings/offering-pci-dss)을 참조하세요.

## <a name="office-365-and-pci-dss"></a>Office 365 및 PCI DSS

### <a name="office-365-cloud-environments"></a>Office 365 클라우드 환경

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 적용 가능성 및 범위 내 서비스

다음 표를 사용하여 Office 365 서비스 및 구독의 적용 가능성을 확인하세요.

| **적용 가능성** | **범위 내 서비스** |
|:------------------|:----------------------|
| **상업용** | 비즈니스용 OneDrive(미국), SharePoint Online |

### <a name="office-365-audit-reports-and-certificates"></a>Office 365 감사, 보고서 및 인증

- [비즈니스용 OneDrive 및 SharePoint Online PCI DSS 준수 증명(AoC)](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a>자주하는 질문

**AoC(Attestation on Compliance) 표지 페이지에 ‘2018년 6월’이 표시된 이유는 무엇인가요?**

표지 페이지의 날짜 2018년 6월은 AoC 서식 파일이 게시된 날짜입니다. 평가 날짜는 2조를 참조하세요. 

**PA DSS와 PCI DSS는 서로 어떤 관계인가요?**

PA DSS(Payment Application Data Security Standard)는 PCI DSS를 준수하고, Visa의 지불 응용 프로그램 모범 사례를 대체하고, 다른 주요 카드 발급자의 규정 준수(compliance) 요건을 통합하는 요건 모음입니다. 소프트웨어 공급업체에서는 PA DSS에 따라 카드 인증 또는 결제 프로세스의 일환으로 카드 소유자 지불 데이터를 저장, 처리 또는 전송하는 타사 응용 프로그램을 개발할 수 있습니다. 소매업체에서는 PCI DSS 규정을 효율적으로 준수하려면 PA DSS 인증 응용 프로그램을 사용해야 합니다. PA DSS는 Azure에 적용되지 않습니다.

**전표 매입업체란 무엇인가요? Azure는 매입업체를 이용하나요?**

전표 매입업체란 결제 카드 거래를 처리하는 은행 또는 기타 기관입니다. Azure는 카드 결제 처리 서비스를 제공하지 않으므로 전표 매입업체를 이용하지 않습니다.

**PCI DSS는 어떤 회사 및 판매자에게 적용되나요?**

거래의 규모나 수에 상관없이 카드 소유자 데이터를 수락, 전송 또는 저장하는 모든 회사에 적용됩니다. 즉, 고객이 신용 카드 또는 직불 카드를 사용하여 회사에 지불하는 경우 PCI DSS 요구 사항이 적용됩니다. 기업은 12개월 동안의 총 거래량을 기준으로 네 가지 수준 중 하나로 검증됩니다. 연간 처리하는 거래 건수가 600만 건 초과인 기업은 수준 1, 100만 ~ 600만 건인 기업은 수준 2, 2만 ~ 1백만 건인 기업은 수준 3, 2만 건 미만인 기업은 수준 4에 해당합니다.

**비즈니스용 OneDrive 및 SharePoint Online가 미국 이외의 지역에서 PCI DSS를 준수할 계획이 있나요?**

현재 비즈니스용 OneDrive 및 SharePoint Online은 미국(US)에서만 PCI-DSS를 준수합니다. Microsoft는 미국 이외의 지역에 대한 요구 사항과 타임라인을 평가하고 다른 지역이 로드맵에 추가되면 업데이트를 제공할 것입니다.

**비즈니스용 OneDrive 및 SharePoint Online 범위 내에 어떤 것이 있나요?**

현재 비즈니스용 OneDrive 및 SharePoint Online에 업로드된 파일과 문서만 PCI DSS를 준수합니다.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험을 평가해 보세요.

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

### <a name="resources"></a>리소스

- [PCI 보안 표준 심의회(영문)](https://www.pcisecuritystandards.org/)
- [PCI 데이터 보안 표준(영문)](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [PCI DSS 빠른 참조 설명서(영문)](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
