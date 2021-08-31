---
title: SEC(증권 Exchange 위원회) 규칙 17a-4(f) 미국
description: 독립적인 평가 회사는 Azure 및 Office 365 금융 회사가 SEC 규칙 17a-4(f) 기록 보존 및 변경 불가능한 저장소 요구 사항을 충족하는 데 도움이 될 수 있는 것으로 확인했습니다.
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
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 70efe7749db2c6dd4ae0faa8ac22da6e87109c79
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2021
ms.locfileid: "58707127"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>SEC(증권 Exchange 위원회) 규칙 17a-4(f) 미국

## <a name="about-sec-rule-17a-4f"></a>SEC 규칙 17a-4(f)

미국 증권 Exchange [위원회(SEC)는](https://www.sec.gov/) 미국 연방 정부와 미국 증권 시장의 기본 감독 및 규제 기관의 독립 기관입니다. 연방 증권법에 대한 시행 기관을 주도하고, 새로운 증권 규칙을 제안하며, 증권 산업의 시장 규제를 규제합니다.

SEC는 전자 저장소 미디어에 책 및 기록을 보유하기로 한 규제 대상 기관에 대한 엄격한 명시적 요구 사항을 정의합니다. 증권 브로커-대리점에 대한 보존 기간을 포함한 기록 보관을 규제하기 위해 [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) 및 [17 CFR 240.17a-4를](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) 수립했습니다. 나중에 [SEC는](https://www.sec.gov/rules/interp/34-47806.htm) 특정 조건이 충족되는 한 책과 레코드를 전자 저장소 미디어에 보존할 수 있도록 2개의 해석 릴리스를 17개의 CFR 240.17a-4 단락(f)에 수정했습니다.

필요한 보존 기간 동안 레코드 변경 또는 삭제를 방지하는 경우 전자 저장소 시스템은 이러한 조건을 충족합니다. 보존 기간은 레코드 유형에 따라 3~6년마다 다르며, 즉시 접근성은 처음 2년 동안 관리됩니다. 또한 해석 릴리스 중 하나를 사용하려면 저장소 시스템이 SEC에서 설정한 보존 기간 이상으로 레코드를 보존하여 소계, 법적 보존 또는 기타 요구 사항을 준수할 수 있는 능력이 필요합니다.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft 및 SEC 규칙 17a-4(f)

세계에서 가장 높은 규제 대상 산업 중 하나를 대표하는 금융 서비스 고객은 금융 거래의 보존 및 관련 통신과 같은 복잡한 조항이 지울 수 없는 비규화 및 수정할 수 없는 상태로 규정됩니다. 가장 규약적인 것은 SEC(Security and Exchange Commission)의 규칙 17a-4(f)입니다. 이 규칙은 전자 저장소 미디어에 책 및 기록을 보유하기로 선택된 규제 대상 기관에 대한 엄격한 요구 사항을 규정합니다. 저장된 레코드는 지정된 보존 기간이 끝날 때까지 변경하거나 삭제할 수 없는 변조 방지 기능을 제공해야 합니다.

Microsoft Azure 보존 잠금을 Storage 정책 잠금 및 Microsoft Office 365 Blob을 사용하면 금융 기관이 SEC 규칙 17a-4(f)의 불연속 저장소 요구 사항을 충족하는 데 도움이 될 수 있습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>독립적인 평가

Azure 및 SEC Office 365 17a-4(f)를 준수하는지 평가하기 위해 Microsoft는 레코드 관리 및 정보 거버넌스를 전문으로 하는 독립적인 평가 회사인 Cohasset Associates를 보유했습니다.

### <a name="azure"></a>Azure

[Azure Blob](/azure/storage/blobs/storage-blob-immutable-storage) 저장소의 변경 불가능한 저장소를 사용하면 사용자가 WORM(다대다) 상태를 읽은 후 쓰기에 업무상 중요한 레코드를 저장할 수 있습니다. 이 상태는 사용자가 지정한 간격으로 데이터를 지울 수 없는 상태로 설정하고 수정할 수 없습니다. 보존 간격 동안 Blob을 만들어 읽을 수는 있지만 수정하거나 삭제할 수는 없습니다. 이러한 Azure 변경 불가능한 저장소 기능은 고객이 레코드 보존 요구 사항을 충족하는 데 도움이 될 수 있습니다.

Microsoft는 SEC 규칙 17a-4(f) 요구 사항을 준수하는 Azure Blob Storage 규정 준수를 위해 변경 불가능한 저장소를 평가하기 위해 레코드 관리 및 정보 거버넌스를 전문으로 하는 독립적인 타사 평가 회사를 보유했습니다. 결과 보고서 *[Cohasset Assessment: Microsoft Azure WORM](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* Storage 사용할 수 있습니다.

Azure Blob 기능의 변경 불가능한 Azure Storage 및 잠긴 시간 기반 정책  옵션을 사용하여 시간 기반 Blob(레코드)을 지울 수 없는 및 다시 기록할 수 없는 형식으로 유지하는 것이 평가자 의견입니다. SEC 규칙 17a-4(f), [FINRA 규칙 4511(c)의](offering-FINRA-4511.md)관련 저장소 요구 사항 및 [CFTC 규칙 1.31(c)-(d)의](offering-cftc-1-31-us.md)원칙 기반 요구 사항을 충족합니다. 

요청이 있는 경우 Microsoft는 고객이 전자 저장소 미디어를 사용하기 최소 *90일* 전에 지정된 검사 기관에 알리기 위해 SEC 17a-4(f)(2) 요구 사항을 충족하는 데 필요한 90일 서신을 제공합니다. 규정에 설명된 "구성원, 브로커 또는 대리점은 자체 표현을 제공하거나 선택한 저장소 미디어가 이 단락(f)(2)에 규정된 조건을 충족하는 적절한 전문 지식을 가지고 있는 다른 제3자 또는 저장소 미디어 공급업체로부터 자체 표현을 제공해야 합니다." SEC 규칙 17a-4에 대한 Microsoft Storage Media Services 의 Microsoft 의증을 얻기 위해 [](https://azure.microsoft.com/support/create-ticket/) [Azure](https://azure.microsoft.com/support/plans/) 지원 계획이 있는 고객은 Azure Portal에서 지원 티켓을 만들고 SEC 규칙 17a-4에 대한 의문서를 요청할 수 있습니다.  이 문서에서 Microsoft는 SEC 17a-4(f)(2) 요구 사항과 관련된 보증을 제공합니다.

### <a name="office-365"></a>Office 365

[SEC 17a-4(f)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) 요구 사항의 경우 Cohasset은 Microsoft 365 중개인을 포함하여 규제된 고객이 레코드 보존에 대한 SEC 요구 사항을 준수하는 데 도움이 되는 방식으로 데이터를 저장할 수 있도록 하는 보관 기능이 포함되어 있는 것으로 확인했습니다. 전자 메일의 Microsoft 365 기능은 전자 메일, 음성 메일, 공유 문서, 인스턴트 메시지 및 타사 데이터를 포함하여 광범위한 데이터를 보존하는 데 도움이 됩니다. 특히, Microsoft 365 보관을 통해 고객은 전역 또는 세분화 메시징 보존 정책을 설정하여 정의된 기간 동안 및 그 이상 기간 동안 데이터를 다시 덮어 사용할 수 없는 지울 수 없는 형식으로 저장할 수 있습니다.

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

### <a name="azure--sec-rule-17"></a>Azure & SEC 규칙 17

- [SEC 17a-4(f) & CFTC 1.31(c-d) 준수 평가 Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

Azure *지원이 있는* 지원 티켓을 Storage Media Services SEC 규칙 17a-4에 [](https://azure.microsoft.com/support/create-ticket/) 대한 Microsoft 전자 기술에 대한 Microsoft 의 [의거를 요청할 수 있습니다.](https://azure.microsoft.com/support/plans/) 이 인증 서신에서 Microsoft는 고객이 SEC 17a-4(f)(2) 요구 사항을 준수하는 데 도움이 되는 보증을 제공합니다.

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC 규칙 17

- [SEC 17a-4(f) 준수 평가: & SharePoint, OneDrive, Teams, Exchange 및 준수 센터를 비즈니스용 Skype](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>구현 방법

### <a name="financial-services-regulation"></a>금융 서비스 규정

클라우드 컴퓨팅 및 Microsoft 온라인 서비스에 대한 주요 미국 규제 원칙의 규정 준수 맵입니다. [자세한 정보](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>위험 평가 & 준수 가이드

Microsoft 클라우드 서비스의 위험 평가 및 규제 기관 알림에 대한 거버넌스 모델을 만들 수 있습니다. [자세한 정보](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>재무 사용 사례

사례 개요, 자습서 및 기타 리소스를 사용하여 금융 서비스에 대한 Azure 솔루션을 빌드합니다. [자세한 정보](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [Azure 규정 준수 문서](/azure/compliance/)
- [Azure는 규정 준수의 세계를 구현합니다.](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [SEC(증권 Exchange 위원회)](https://www.sec.gov/) [규칙 17a-4](https://www.sec.gov/rules/final/34-38245.txt)
- [Microsoft 클라우드 금융 서비스 리소스](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Microsoft 클라우드 금융 서비스 준수 프로그램](https://aka.ms/FSCP-Print)
- [클라우드 컴퓨팅 규정 원칙 및 Microsoft 온라인 서비스의 규정 준수 맵](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Microsoft 클라우드의 금융 기관을 위한 위험 평가 및 규정 준수 가이드](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [금융 서비스 산업 사용 사례](/azure/industry/financial/)
- [Microsoft Office 365, 데이터 보존 및 규칙 17a-4의 보관](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
