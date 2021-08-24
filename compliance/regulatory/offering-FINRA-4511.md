---
title: 미국 FINRA(금융산업규제당국) 규칙 4511(c) 미국
description: 독립적인 평가 회사가 Azure 및 Office 365 FINRA 규칙 4511 레코드 보존 및 변경 불가능한 저장소 요구 사항을 충족하는 데 도움이 될 수 있는 것으로 확인했습니다.
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
ms.openlocfilehash: e5c253fe5a2b4995dffc7059717d74fecdc73935
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479770"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>미국 FINRA(금융산업규제당국) 규칙 4511(c) 미국

## <a name="about-finra-rule-4511"></a>FINRA 규칙 4511

FINRA(금융산업규제당국)는 미국 내 4,500개가 넘는 증권 회사를 감독하는 증권 회사를 규제하는 최대 독립 기관입니다. [](https://www.finra.org/#/) 미국 의회는 "브로커 대리점 산업이 공정하고 정직하게 작동할 수 있는지 확인하여 미국의 투자를 보호할 수 있습니다."

2011년 미국 SEC(Security and Exchange Commission)는 전자 저장소 미디어에 대한 책 및 기록의 보존을 규정하는 SEC 규칙의 FINRA 채택을 승인했습니다. [FINRA 규칙 4511(c)은](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) 'FINRA 규칙에 따라 필요한 모든 책과 기록을 SEA(Securities Exchange Act) 규칙 17a-4를 준수하는 형식 및 미디어로 보존해야 합니다."를 지정합니다.

또한 FINRA 규칙 4511(c)은 기업이 해당 FINRA 또는 SEA 규칙에 따라 지정된 보존 기간이 없는 서적 및 기록을 최소 6년 동안 보존해야 합니다. 실제로 책과 기록이 계정과 연계된 경우 보존 기간은 계정이 폐쇄된 후 6년이 됩니다. 그렇지 않은 경우 보존 기간은 해당 책 및 레코드가 만들어진 후 6년 동안입니다.

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft 및 FINRA 규칙 4511(c)

세계에서 가장 높은 규제 대상 산업 중 하나를 대표하는 금융 서비스 고객은 금융 거래의 보존 및 관련 통신과 같은 복잡한 조항이 지울 수 없는 비규화 및 수정할 수 없는 상태로 규정됩니다. 그중에는 전자 저장소 미디어에 책 및 기록을 보유하기로 한 규제 기관에 대한 엄격한 요구 사항을 규정하는 FINRA(금융 산업 규제 기관)의 규칙 4511이 있습니다. 저장된 레코드는 지정된 보존 기간이 끝날 때까지 변경하거나 삭제할 수 없는 변조 방지 기능을 제공해야 합니다.

Microsoft Azure 보존 잠금을 Storage Blob을 Microsoft Office 365 Blob을 사용하면 금융 기관이 FINRA 규칙 4511(c)의 불연속 저장소 요구 사항을 충족하는 데 도움이 됩니다.

## <a name="microsoft-azure"></a>Microsoft Azure

FINRA 규칙 4511(c)을 사용하여 Azure 규정 준수를 평가하기 위해 Microsoft는 레코드 관리 및 정보 거버넌스를 전문으로 하는 독립적인 평가 회사인 Cohasset Associates를 보유했습니다. 결과 보고서인 [SEC 17a-4(f) & CFTC 1.31(c-d)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)준수 평가: Microsoft Azure Storage 는 SEC 규칙 17a-4(f)의 형식 및 미디어 요구 사항에 지연되는 FINRA 규칙 4511(c)에 대한 Azure 규정 준수를 다룰 수 있습니다.

Cohasset은 WORM(지우기 불가능 및 다시 쓰지 못함) 형식으로 시간 기반 Bl [Storage ob을](/azure/storage/blobs/storage-blob-immutable-storage) 보존하는 데 사용되는 경우 정책 잠금 옵션을 사용하여 Azure 변경 불가능 Blob이 관련 FINRA 저장소 요구 사항을 충족하는지 확인했습니다. 각 Blob(레코드)은 필요한 보존 기간이 만료되고 관련 법적 보존이 릴리스될 때까지 수정, 덮어 사용 또는 삭제되지 않습니다.

중요한 워크로드를 보유한 소프트웨어 공급자 및 파트너는 이제 Azure 변경 불가능 Blob Storage 저장소 보존 및 변경 불가능한 저장소를 위한 원스톱 쇼핑 클라우드 솔루션으로 사용할 수 있습니다. 이제 금융 기관은 규정을 준수하면서 이러한 기능을 활용하는 자체 응용 프로그램을 구축할 수 있습니다.

## <a name="microsoft-365"></a>Microsoft 365

[FINRA 규칙 4511(c)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) 요구 사항의 경우 Cohasset은 Microsoft 365 중개인을 포함하여 규제된 고객이 레코드 보존에 대한 SEC 요구 사항을 준수하는 데 도움이 되는 방식으로 데이터를 저장할 수 있도록 하는 보관 기능을 Microsoft 365 유효성을 검사했습니다. 전자 메일의 Microsoft 365 기능은 전자 메일, 음성 메일, 공유 문서, 인스턴트 메시지 및 타사 데이터를 포함하여 광범위한 데이터를 보존하는 데 도움이 됩니다. 특히, Microsoft 365 보관을 통해 고객은 전역 또는 세분화 메시징 보존 정책을 설정하여 정의된 기간 동안 및 그 이상 기간 동안 데이터를 다시 덮어 사용할 수 없는 지울 수 없는 형식으로 저장할 수 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA 규칙 4511(c)

- [SEC 17a-4(f) & CFTC 1.31(c-d) 준수 평가 Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA 규칙 4511(c)

[Office 365, 데이터 보존 및 SEC 규칙 17a-4 규정 준수의 보관](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>구현 방법

- **금융 서비스 규정:** 클라우드 컴퓨팅 및 Microsoft 온라인 서비스에 대한 주요 미국 규제 원칙의 규정 준수 맵입니다. [자세한 정보](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **위험 평가 및 규정 준수 가이드**: Microsoft 클라우드 서비스의 위험 평가 및 규제 기관의 알림에 대한 거버넌스 모델을 만들 수 있습니다. [자세한 정보](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **금융 유스케이스**: 금융 서비스용 Azure 솔루션을 구축하기 위한 유스케이스 개요, 자습서 및 기타 리소스.. [자세한 정보](/azure/industry/financial/)

## <a name="resources"></a>리소스

- [Microsoft 금융 서비스 준수 프로그램](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Microsoft 비즈니스 클라우드 서비스 및 금융 서비스](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure에서의 금융 서비스 규정 준수](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 금융 서비스 클라우드 위험 평가 도구](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 보존 정책](/office365/securitycompliance/retention-policies)
- [Microsoft 금융 서비스 블로그](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
