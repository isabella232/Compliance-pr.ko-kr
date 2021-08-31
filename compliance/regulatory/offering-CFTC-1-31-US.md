---
title: CFTC(상품선물거래위원회) 규칙 1.31(c-d) 미국
description: 독립적인 평가 회사에서 Azure 및 Office 365 CFTC 규칙 1.31 레코드 보존 및 변경 불가능한 저장소 요구 사항을 충족하는 데 도움이 될 수 있는 것으로 확인했습니다.
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
ms.openlocfilehash: 8bb9f380d57e932576c969f10512f508de7c6ada
ms.sourcegitcommit: 70efe7749db2c6dd4ae0faa8ac22da6e87109c79
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2021
ms.locfileid: "58707137"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>CFTC(상품선물거래위원회) 규칙 1.31(c-d) 미국

## <a name="about-cftc-rule-13c-d"></a>CFTC 규칙 1.3(c-d)

[독립적인](https://www.cftc.gov/) 미국 연방 기관인 CFTC(상품선물거래위원회)는 상품선물 및 옵션 시장과 최근의 스왑 시장을 규제합니다.  
  
오래 지속된 CFTC 규칙 1.31은 SEC 규칙 17a-4(f)에서 설정한 레코드 보존 요구 사항을 정의합니다. 또한 전자 기록은 5년 동안 유지 관리해야 하며, 처음 2년 동안 원본에 '쉽게 액세스할 수 있는' 유지를 지정하고, 전체 보존 기간 동안 위원회 또는 미국의 안전보안국(US Department ofSies)의 검사에 사용할 수 있도록 지정합니다.  
  
2017년에 [CFTC는](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)레코드 유지 관리 방법의 유연성을 향상하는 덜 규범적인 원칙 기반 표준을 채택하기 위해 해당 기록 관리 규정을 수정하고 현대화하는 규칙을 수정했습니다. 이 개정을 통해 규칙은 보다 기술 중립적이 되도록 하여 규제 대상 기관이 '기록 관리 프로세스의 안정성을 보장합니다'는 세이프가드를 유지하면서 비즈니스에 가장 적합한 기술을 선택할 수 있도록 합니다. 수정된 규칙은 조직이 원본 레코드를 2년 동안 유지 관리해야 하는 요구 사항을 제거하지만 5년의 유지 관리 기간을 유지하여 CFTC와 SEC 모두에서 규제하는 기업에 대한 관행을 조정합니다.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft 및 CFTC 규칙 1.31(c-d)

세계에서 가장 높은 규제 대상 산업 중 하나를 대표하는 금융 서비스 고객은 금융 거래의 보존 및 관련 통신과 같은 복잡한 조항이 지울 수 없는 비규화 및 수정할 수 없는 상태로 규정됩니다. 가장 규정적인 한 가지는 전자 저장소 미디어에 책 및 기록을 보유하기로 한 규제 기관에 대한 엄격한 요구 사항을 규정하는 미국 CFTC(상품선물거래위원회)의 규칙 1.31입니다. 저장된 레코드는 지정된 보존 기간이 끝날 때까지 변경하거나 삭제할 수 없는 변조 방지 기능을 제공해야 합니다. Microsoft Azure 보존 잠금을 Storage 정책 잠금 및 Microsoft Office 365 Blob을 사용하면 금융 기관이 CFTC 규칙 1.31(c-d)의 저장소 요구 사항을 충족하는 데 도움이 될 수 있습니다.

### <a name="microsoft-azure"></a>Microsoft Azure

CFTC 규칙 1.31(c-d)을 준수하는 Azure 규정 준수를 평가하기 위해 Microsoft는 레코드 관리 및 정보 거버넌스를 전문으로 하는 독립적인 평가 회사인 Cohasset Associates를 보유했습니다. 결과 보고서에서 [CFTC 1.31(c) (d)](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)준수 평가: Microsoft Azure Storage , Cohasset은 WORM(지우기 불가능 및 다시 쓰지 못함) 형식으로 시간 기반 Bl [Storage ob을](/azure/storage/blobs/storage-blob-immutable-storage) 보존하는 데 사용되는 경우 정책 잠금 옵션을 사용하여 Azure 변경 불가능 Blob이 CFTC 규칙의 원칙 기반 요구 사항을 충족하는지 확인했습니다. 각 Blob(레코드)은 필요한 보존 기간이 만료되고 관련 법적 보존이 릴리스될 때까지 수정, 덮어 사용 또는 삭제되지 않습니다. 중요한 워크로드가 있는 소프트웨어 공급자 및 파트너는 이제 Azure 변경 불가능 Blob Storage 보존을 위한 원스톱 쇼핑 클라우드 솔루션으로 사용할 수 있습니다. 이제 금융 기관은 규정을 준수하면서 이러한 기능을 활용하는 자체 응용 프로그램을 구축할 수 있습니다.

### <a name="microsoft-365"></a>Microsoft 365

[CFTC 1.31(c)-(d)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) 요구 사항의 경우 Cohasset은 Microsoft 365 중개인을 포함하여 규제된 고객이 레코드 보존에 대한 SEC 요구 사항을 준수하는 데 도움이 되는 방식으로 데이터를 저장할 수 있도록 하는 보관 기능이 포함되어 있는 것으로 확인했습니다. 전자 메일의 Microsoft 365 기능은 전자 메일, 음성 메일, 공유 문서, 인스턴트 메시지 및 타사 데이터를 포함하여 광범위한 데이터를 보존하는 데 도움이 됩니다. 특히, Microsoft 365 보관을 통해 고객은 전역 또는 세분화 메시징 보존 정책을 설정하여 정의된 기간 동안 및 그 이상 기간 동안 데이터를 다시 덮어 사용할 수 없는 지울 수 없는 형식으로 저장할 수 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

- [Azure & CFTC 규칙 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) 준수 평가 Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)
- Office 365 & CFTC 규칙 1.31: Office 365, 데이터 보존 및 SEC 규칙 17a-4 규정 준수의 보관

## <a name="how-to-implement"></a>구현 방법

- [금융 서비스 규정:](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)클라우드 컴퓨팅 및 Microsoft 온라인 서비스에 대한 주요 미국 규제 원칙의 규정 준수 맵입니다.
- [위험 평가 & 준수 가이드](https://aka.ms/RiskGovernanceGuide): Microsoft 클라우드 서비스의 위험 평가 및 규제 기관의 알림에 대한 거버넌스 모델을 만들 수 있습니다.
- [금융 유스케이스](/azure/industry/financial/): 금융 서비스용 Azure 솔루션을 구축하기 위한 유스케이스 개요, 자습서 및 기타 리소스..

## <a name="resources"></a>리소스

- [Microsoft 금융 서비스 준수 프로그램](https://aka.ms/FSCP-Print)
- [Microsoft 비즈니스 클라우드 서비스 및 금융 서비스](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Azure에서의 금융 서비스 규정 준수](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365 보존 정책](/office365/securitycompliance/retention-policies)
- [Microsoft 금융 서비스 블로그](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
