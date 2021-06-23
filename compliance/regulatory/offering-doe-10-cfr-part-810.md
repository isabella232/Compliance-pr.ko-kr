---
title: US DoE 10 CFR Part 810
description: 미국 DoE 10 CFR Part 810의 수출 제어 요구 사항을 준수하는 고객은 Azure Government를 사용할 수 있습니다.
keywords: Microsoft 365, 규정 준수, 제품
localization_priority: None
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087547"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft 및 DoE 10 CFR 파트 810

Microsoft Azure 정부는 다음 두 가지 인증을 통해 미국 DoE(에너지부) 10 CFR Part 810의 수출 제어 요구 사항을 준수하는 고객을 지원할 수 있습니다.

- JAB(합동 인증 위원회)에서 발행한 P-ATO(High Provisional Authorization to Operate)
- DoD(국방부) 국방 정보 시스템 기관의 수준 4 및 5 임시 권한

FedRAMP는 Azure Government가 엄격한 NIST 컨트롤을 사용하여 설계된 컴퓨팅, 저장소 및 네트워킹과 같은 핵심 인프라 및 가상화 기술 및 서비스를 제공할 수 있는 적절한 기준을 제공합니다. 이러한 설정은 고객 데이터 분리 요구 사항을 충족하고 고객의 사내 환경에 대한 보안 연결을 가능하게 하는 데 도움이 됩니다.

또한 Azure Government는 Azure 클라우드와 물리적으로 분리된 미국 정부 커뮤니티 클라우드입니다. Azure 운영 담당자 사이에서 선별된 미국 시민으로 정보 및 시스템에 대한 액세스를 제한하는 특정 제어를 포함하여 미국 정부의 특정 배경 심사 요구 사항에 대한 추가 보증을 제공합니다.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 범위 내 클라우드 서비스

- [Azure Government](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>구현 방법

- [NERC CIP 표준 &](https://aka.ms/AzureNERC)클라우드 컴퓨팅: Azure 또는 Azure Government에 작업을 배포하는 전기 유틸리티 및 등록된 엔터티에 대한 지침입니다.

## <a name="about-doe-10-cfr-part-810"></a>DoE 10 CFR Part 810

미국 에너지부(DoE) 수출 제어 규정 [10 CFR Part 810은](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) 미분분 기술 및 지원의 수출을 관리합니다. 미국에서 내보낼 선구 기술은 선행 목적으로만 사용되도록 보장합니다. 수정된 제810부(최종 규칙)는 2015년 3월에 적용된 것으로 국가보안국에서 [관리합니다.](https://www.energy.gov/nnsa/national-nuclear-security-administration) 섹션 810.6에서는 특정 DoE 권한 부여가 '일반적으로 승인된' 중요한 기술의 지원 프로비전 및 전송과 특정 승인이 필요한 경우(예: 강화 및 고수 생산과 같은 중요한 유해 기술에 대한 지원의 경우)에 필요하도록 규정합니다.

## <a name="frequently-asked-questions"></a>질문과 대답

**미국 규율 규제 위원회의 10 CFR 제110조 규정이 Azure Government에 적용하나요?**

아니요. [NRC(미국](https://www.nrc.gov/) 지민 규제 위원회)는 [10 CFR Part 110에](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/)따라 시설 시설 및 관련 장비 및 재료의 수출 및 수입을 규제합니다. [](https://www.nrc.gov/about-nrc/ip/export-import.html) NRC는 DoE 관할권에 속하는 이러한 항목과 관련된 기술 및 지원을 규제하지 않습니다. 따라서 NRC 10 CFR Part 110 규정은 Azure Government에 적용되지 않습니다.

**DoE 10 CFR Part 810을 준수하고 있는 증거를 제공하면 어떻게 하나요?**

조직에서 Azure Government에 데이터를 배포하는 경우 Azure Government FedRAMP High P-ATO를 적절하게 제한된 방식으로 데이터를 처리하고 있는 증거로 사용할 수 있습니다. 그러나 클라우드 서비스 사용을 포함하여 자체 시스템의 DoE 권한 부여를 받고 있는 것은 사용자 책임입니다.

**Azure Government에 배포된 데이터를 분류하는 데는 어떤 책임이 있나요?**

Azure Government에 데이터를 배포하는 고객은 자체 보안 분류 프로세스를 담당합니다. DoE 내보내기 제어를 적용하는 고객 데이터의 경우 미국 원자력법의 148조에 의해 수립된 UCNI(Unclassified Controled Classification Information) 컨트롤에 의해 분류 시스템이 보강됩니다. [](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)

## <a name="resources"></a>리소스

- [Azure 클라우드 서비스 및 미국 수출 제어](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft 및 FedRAMP](offering-fedramp.md)
- [Microsoft 및 DoD](offering-dod-disa-l2-l4-l5.md)
- [Microsoft Government 클라우드](https://www.microsoft.com/enterprise/government)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
