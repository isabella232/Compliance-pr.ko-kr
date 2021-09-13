---
title: EAR(미국 수출 관리 규정)
description: Microsoft 클라우드 서비스는 미국 EAR(수출 관리 규정)를 준수하는 고객이 규정 준수 요구 사항을 충족하고 수출 제어 위험을 관리하는 데 도움이 됩니다.
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
ms.openlocfilehash: 859067495b6811b2264ab3a379f305d428771bce
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160117"
---
# <a name="us-export-administration-regulations-ear"></a>EAR(미국 수출 관리 규정)

## <a name="about-the-ear"></a>About the EAR

미국 상무부는 [BIS(Bureau of Industry and Security)를 통해 EAR(수출](https://www.bis.doc.gov/)관리 규정)를 적용합니다. EAR는 상업용 및 군용 목적과 특정 방어 항목에 모두 사용할 수 있는 '이중 사용' 항목을 포함하여 대부분의 상업용 제품, 소프트웨어 및 기술의 수출 및 재수출에 대한 제어를 광범위하게 제어하고 부과합니다.

BIS 지침은 데이터 또는 소프트웨어가 클라우드에 업로드되거나 사용자 노드 간에 전송될 때 클라우드 공급자가 아닌 고객은 해당 데이터 또는 소프트웨어에 대한 전송, 저장 및 액세스가 EAR를 준수하는지 보장할 책임이 있는 '수출자'입니다.

[BIS에](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)따라 , *export는* 보호된 기술 또는 기술 데이터를 미국의 외계인에게 전송하거나 해당 릴리스를 미국의 외계인에게 전송하는 것을 지칭합니다(내보내기로도 *지칭).* EAR는 광범위하게 다음을 관리합니다.

- 미국에서 내보낼 수 있습니다.
- 미국 원주민 콘텐츠의 일부를 최소화하는 부분보다 많은 미국 원시  항목 및 특정 외래 원산지 항목을 다시 내보내거나 다시 전달합니다.
- 다른 국가의 개인에게 전송 또는 공개.

EAR가 적용된 항목은 각 항목에 고유한 [ECCN(내보내기](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)제어 분류 번호)이 할당된 CCL(상거래 제어 목록)에서 찾을 수 있습니다. CCL에 나열되지 않은 항목은 EAR99로 지정되고 대부분의 EAR99 상업용 제품에는 라이선스를 내보낼 필요가 없습니다. 그러나 항목의 대상, 최종 사용자 또는 최종 사용에 따라 EAR99 항목도 BIS 내보내기 라이선스가 필요할 수 있습니다.

2016년 6월에 게시된 최종 규칙은 FIPS 140-2의 유효성을 검사한 암호화 모듈을 사용하여 종단간 암호화되고 의도적으로 군 수출이 허가된 국가 또는 러시아 페더레이션에 저장되지 않은 경우, 미분 분석되지 않은 기술 데이터 및 소프트웨어의 전송 및 저장에도 EAR 라이선스 요구 사항이 적용되지 않는다는 것이 명확히 설명되었습니다. [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)

## <a name="microsoft-and-the-ear"></a>Microsoft 및 EAR

Microsoft 기술, 제품 및 서비스는 미국 EAR(수출 관리 규정)의 적용을 따릅니다. EAR에 대한 준수 인증은 없는 반면, Microsoft Azure, Microsoft Azure Government 및 Microsoft Office 365 Government(GCCHigh 및 DoD 환경)는 EAR의 수출 제어 위험을 관리하고 규정 준수 요구 사항을 충족하는 데 도움이 되는 중요한 기능 및 도구를 제공합니다.

EAR를 적용하는 미국 상무부는 Microsoft와 같은 클라우드 서비스 공급자가 아닌 고객이 자체 고객 데이터의 수출자인 것으로 간주되는 입장을 취했습니다. 대부분의 고객 데이터는 EAR 수출 제어가 적용된 '기술' 또는 '기술 데이터'로 간주되지 않는 반면, Microsoft 범위 내 클라우드 서비스는 고객이 발생할 수 있는 수출 제어 위험을 관리하고 크게 완화할 수 있도록 구조화됩니다. Microsoft는 일반적으로 전용적으로는 안 되지만 적격 고객에게는 정부 클라우드 서비스를 사용하는 것이 좋습니다. 적절한 계획을 수립하면 고객은 다음 도구와 자체 내부 절차를 사용하여 미국 수출 제어를 완전하게 준수할 수 있습니다.

- **데이터 위치의 컨트롤입니다.** 고객은 데이터가 저장되는 위치에 대한 가시성을 확보하고 강력한 도구에 액세스하여 저장소를 제한할 수 있습니다. 따라서 데이터가 미국에 저장되도록 보장하고 미국 외부의 제어된 기술 또는 기술 데이터 전송을 최소화할 수 있습니다. 또한 고객 데이터는 데이터가 '의도적으로 저장되는 위치'에 대한 EAR 금지와 일치하여 준수되지 않는 위치에 저장되지 않습니다. 25개 그룹 D:5 국가 또는 러시아 페더링에 Azure 데이터 센터가 없습니다.
- **종단-종단 암호화.** EAR에 지정된 물리적 저장소 위치에 대한 종단-종단-종단 암호화 안전한 하버를 활용하면 Microsoft 범위 내 클라우드 서비스는 수출 제어 위험으로부터 보호할 수 있는 암호화 기능을 제공합니다. 또한 고객에게 전송 [](https://aka.ms/Azure-Encryption-Overview) 중 및 미사용 데이터를 암호화하는 다양한 옵션과 암호화 옵션 중에서 선택할 수 있는 유연성을 제공합니다.
- **권한이 없는 것으로 보인 내보내기 를 방지하기 위한 도구 및 프로토콜입니다.** 또한 암호화를 사용하면 EAR에서 잠재적으로 것으로 생각되는 내보내기(또는 다시 내보내기)로부터 보호할 수 있습니다. 미국이 아닌 사용자가 암호화된 데이터에 액세스할 수 있는 경우에도 암호화된 동안 데이터를 읽거나 이해할 수 없는 경우에는 아무 것도 노출되지 않습니다. 따라서 제어된 데이터의 '릴리스'가 없습니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure 및 Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Government(GCC-High 및 DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>구현 방법

EAR에 따라 의무를 평가하는 고객을 위한 미국 수출 제어 및 지침 개요.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>자주 하는 질문

**Microsoft 클라우드 서비스를 사용할 때 내보내기 제어를 준수하기 위해 무엇을 해야 하나요?**

EAR에서 데이터가 Microsoft 클라우드와 같은 클라우드 서버에 업로드될 때 클라우드 서비스 공급자가 아닌 데이터를 소유한 고객은 수출자인 것으로 간주됩니다. 이러한 이유로 데이터 소유자, 즉 Microsoft 고객인 경우 Microsoft 클라우드의 사용이 미국 수출 제어를 암시하는 방법을 신중하게 평가하고 사용 또는 저장하려는 데이터 중 어떤 데이터가 EAR 제어가 적용될 수 있는지, 그 경우 어떤 컨트롤이 적용되는지 결정해야 합니다. Azure 및 [](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) Office 365 [](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) 클라우드 서비스가 어떻게 고객이 미국 수출 제어를 완전하게 준수하는지 보장하는 방법에 대해 자세히 알아보하세요.

**Microsoft 기술, 제품 및 서비스는 EAR의 적용을 하나요?**

대부분의 Microsoft 기술, 제품 및 서비스는 다음 중 하나에 있습니다.

- EAR의 적용을 을(를) 따라야 하여 상거래 제어 목록에 없는 ECCN이 없습니다.
- 또는 EAR99 또는 5D992 대량 시장은 Microsoft의 자체 분류를 받을 자격이 있으며 라이선스가 없는 비허용 국가로 NLR(라이선스 필요 없음)으로 내보낼 수 있습니다.

즉, 일부 Microsoft 제품에 라이선스가 필요할 수도, 필요하지 않을 수도 있는 ECCN이 할당되어 있습니다. EAR 또는 법률 자문에게 문의하여 수출 목적에 적합한 라이선스 유형 및 적격 국가를 결정하십시오.

**EAR와 ITAR(International Traffic in Arms Regulations)의 차이점은 무엇입니까?**

가장 광범위한 응용 프로그램을 적용하는 주요 미국 수출 컨트롤은 미국 상무부에서 관리하는 EAR입니다. EAR는 상업용 응용 프로그램과 군용 응용 프로그램이 모두 있는 이중 용도 항목과 상업용 응용 프로그램이 있는 항목에 적용할 수 있습니다.

또한 미국은 ITAR과 같이 가장 중요한 항목 및 기술을 제어하는 별도의 보다 전문화된 수출 제어 규정을 품고 있습니다. 미국 국무부는 관련 기술 데이터를 포함하여 많은 군, 방어 및 인텔리전스 항목('방위 문서'라고도 알려진)의 수출, 임시 가져오기, 다시 내보내기 및 전송에 대한 제어를 부과합니다.

## <a name="resources"></a>리소스

- [Microsoft 제품 내보내기: 개요](https://www.microsoft.com/exporting/overview.aspx)
- [Microsoft 제품 내보내기: FAQ](https://www.microsoft.com/exporting/faq.aspx)
- [Microsoft 제품 내보내기: 제품 업데이트](https://www.microsoft.com/exporting/exporting-information.aspx)
- [암호화에 대한 내보내기 제한](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft 및 FIPS 140-2](offering-fips-140-2.md)
- [Microsoft 및 ITAR](offering-itar.md)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
