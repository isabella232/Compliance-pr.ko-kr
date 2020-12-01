---
title: ISO/IEC 27017:2015 정보 보안 통제를 위한 규약
description: Microsoft 클라우드 서비스는 정보 보안 통제를 위해 이 규약을 구현했습니다.
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
ms.openlocfilehash: b51d7879b0b20773f76ed194a0080b2ae88c1fb8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509508"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 정보 보안 통제를 위한 규약

## <a name="iso-iec-27017-overview"></a>ISO-IEC 27017 개요

ISO/IEC 27017:2015 행동 강령은 조직이 ISO/IEC 27002:2013 기반 클라우드 컴퓨팅 정보 보안 관리 시스템을 구현할 때 클라우드 서비스 정보 보안 제어를 선택하기 위한 참조 자료로 사용할 수 있도록 설계되었습니다. 또한 클라우드 서비스 공급자는 일반적으로 허용되는 보호 제어를 구현하기 위한 지침 문서로도 사용할 수 있습니다.

이 국제 표준은 ISO/IEC 27002에 기반한 클라우드별 구현 지침을 추가로 제공하며, 제어, 구현 지침 및 기타 정보에 대한 ISO/IEC 27002: 2013의 5-18 조항과 관련하여 클라우드별 정보 보안 위협 및 리스크를 해결하기 위한 추가적인 제어 기능을 제공합니다. 구체적으로, 이 표준은 ISO/IEC 27002에서 37개의 컨트롤에 대한 지침을 제공하며, ISO/IEC 27002에서 중복되지 않는 7개의 새로운 컨트롤을 특징으로 합니다. 이러한 새로운 컨트롤은 다음과 같은 중요한 영역을 다룹니다.

- 클라우드 컴퓨팅 환경에서의 공유 역할과 책임
- 계약 종료 시 클라우드 서비스 고객 자산의 제거와 반환
- 한 고객의 가상 환경과 다른 고객의 가상 환경의 분리 및 보호
- 비즈니스 요구를 충족하기 위한 가상 컴퓨터 강화 요구 사항
- 클라우드 컴퓨팅 환경의 관리 작업 절차
- 고객이 클라우드 컴퓨팅 환경 내의 관련 활동을 모니터링할 수 있도록 지원
- 가상 네트워크와 물리적 네트워크의 보안 관리 일관성 유지

## <a name="microsoft-and-isoiec-27017"></a>Microsoft와 ISO/IEC 27017

ISO/IEC 27017은 클라우드 서비스 제공자와 클라우드 서비스 고객 모두에게 지침을 제공하는 데 있어 독보적입니다. 또한 클라우드 서비스 고객에게 클라우드 서비스 제공자에게 무엇을 기대해야 하는지에 대한 실질적인 정보도 제공합니다. 고객은 클라우드의 공유 책임을 확실히 이해함으로써 ISO/IEC 27017의 직접적인 혜택을 누릴 수 있습니다.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 범위 내 클라우드 서비스

- [Azure, Azure Government, Azure Germany](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365, Dynamics 365 및 Dynamics 365 Germany](https://aka.ms/d365-compliance-list)
- Microsoft Defender Advanced Threat Protection
- Microsoft Graph
- Microsoft Healthcare Bot
- Intune
- Microsoft Managed Desktop
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power Automate(이전 Microsoft Flow) 클라우드 서비스
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, 및 Office 365 Germany
- 독립 실행형 서비스 혹은 Office 365 혹은 Dynamics 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 PowerApps 클라우드 서비스
- 독립 실행형 서비스 혹은 Office 365에 브랜딩된 플랜 또는 제품군에 포함된 형태로서의 Power BI 클라우드 서비스
- Power BI Embedded
- Microsoft Stream
- Office 365에서 적용되는 서비스에 대한 [자세한 목록](https://go.microsoft.com/fwlink/p/?linkid=2077751)보기

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

Microsoft 클라우드 서비스는 ISO/IEC 27001:2013에 대한 인증 프로세스의 일부로서 ISO/IEC 27017:2015 규약에 대해 1년에 한 번씩 감사를 받습니다.

- [Azure ISO 27017 인증서](https://aka.ms/azureiso27017cert)
- [Azure ISO 27017 평가 보고서](https://aka.ms/azureiso27017report)
- [Office 365: ISO 27001, 27018 및 27017 감사 평가 보고서](https://aka.ms/o365isoreport)

## <a name="frequently-asked-questions"></a>질문과 대답

이 표준은 누구에게 적용됩니까?

이 행동 강령은 클라우드 서비스 제공자와 클라우드 서비스 고객 모두에게 제어 및 구현 지침을 제공합니다. ISO/IEC 27002:2013과 유사한 형식으로 구성되어 있습니다.

**ISO/IEC 27017:2015에 대한 Microsoft의 규정 준수 정보는 어디에서 확인할 수 있습니까?**

Azure, Intune, Power BI에 대한 [ISO/IEC 27017:2015 인증서](https://aka.ms/azureiso27017)를 다운로드할 수 있습니다.

**우리 회사의 인증 프로세스에 Microsoft 서비스의 ISO/IEC 27017 규정 준수를 사용할 수 있나요?**

예. 귀사가 범위 내 모든 Microsoft 엔터프라이즈 클라우드 서비스에 구현된 구현에 대한 인증을 받으려는 경우 규정 준수 평가에서 Microsoft의 관련 인증을 사용할 수 있습니다. 그러나 사용자는 평가인을 참여시켜 규정 준수를 위한 구현 평가와 조직 내 통제 및 프로세스에 대한 평가를 수행할 책임이 있습니다.

**적용되는 감사 보고서 사본을 구하려면 어떻게 해야 합니까?**

[서비스 신뢰 포털](https://aka.ms/stphelp)은(는) 독립적인 타사 감사 보고서 및 기타 관련 설명서를 제공합니다. 포털을 사용하여 이 문서를 다운로드하고 검토하여 자체 규정 요구 사항에 대한 지원을 받을 수 있습니다.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)는 사용자 조직의 준수 상태를 이해하고 위험을 줄이기 위한 활동에 도움을 주는 [Microsoft 365 규정 준수 센터](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규정에 관한 평가를 작성하기 위한 프리미엄 문서 서식을 제공합니다. 준수 관리자의 **평가 문서 서식 페이지** 에서 문서 서식을 찾을 수 있습니다. [준수 관리자에서 평가를 빌드](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments)하는 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [ISO/IEC 27017:2015 규약](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Microsoft 온라인 서비스 사용 약관](https://aka.ms/Online-Services-Terms)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
