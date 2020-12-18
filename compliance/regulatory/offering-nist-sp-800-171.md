---
title: NIST SP 800-171
description: Microsoft 클라우드 서비스는 비영리 정보 시스템에서 제어된 CUI(미분분 정보)를 보호하기 위한 NIST SP 800-171 지침을 준수합니다.
keywords: Microsoft 365, 규정 준수, 제안
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
ms.openlocfilehash: 51a09772498da0ffc4c7d135e8b9ae103364a984
ms.sourcegitcommit: 9d00734702fec0e76f6b001e31ff0a6eb60cae6f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/18/2020
ms.locfileid: "49712086"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>NIST SP 800-171

미국 NIST(National Institute of Standards and Technology)는 연방 기관의 정보 및 정보 시스템을 보호하기 위한 측정 표준 및 지침을 홍보하고 유지 관리합니다. CUI(제어된 미분석 정보) 관리에 관한 행정 명령 13556에 따라 비영리 정보 시스템 및 조직에서 제어된 미분석 정보를 보호하는 [NIST SP 800-171을](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)게시했습니다. CUI는 정부(또는 대신 엔터티)에서 만든 디지털 및 물리적 정보로 정의됩니다. 이 정보는 분류되지 않은 동안 여전히 중요하며 보호가 필요합니다.

NIST SP 800-171은 원래 2015년 6월에 게시된 후부터 진화하는 사이버 위협에 대응하여 여러 번 업데이트되었습니다. 비영리 정보 시스템 및 조직에 CUI를 안전하게 액세스, 전송 및 저장하는 방법에 대한 지침을 제공합니다. 요구 사항은 다음과 같은 네 가지 주요 범주로 분류됩니다.

- 관리 및 보호를 위한 제어 및 프로세스
- IT 시스템 모니터링 및 관리
- 최종 사용자를 위한 명확한 사례 및 절차
- 기술적 및 물리적 보안 조치 구현

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft 및 NIST SP 800-171

공인 타사 평가 조직인 Kratos Secureinfo 및 Coalfire는 범위 내 클라우드 서비스가 *CUI를* 처리하면 범위 내 클라우드 서비스가 NIST SP 800-171, 비공식 정보 시스템 및 조직에서 CUI(제어된 미분 분석 정보)를 보호하는 기준을 충족하는지 인증을 확정했습니다. [FedRAMP](offering-fedramp.md) 요구 사항을 Microsoft에서 구현하면 범위 내 클라우드 서비스가 이미 구현된 시스템 및 관행을 사용하여 NIST SP 800-171의 요구 사항을 충족하거나 초과할 수 있습니다.

NIST SP 800-171 요구 사항은 FedRAMP에서 사용하는 표준인 NIST SP 800-53의 하위 집합입니다. NIST SP 800-171의 부록 D는 범위 내 클라우드 서비스가 FedRAMP 프로그램에서 이미 평가되고 권한이 부여된 NIST SP 800-53의 관련 보안 컨트롤에 대한 CUI 보안 요구 사항을 직접 매핑합니다.

미국 정부 CUI(연구 기관, 컨설팅 회사, 제조 계약자)를 처리하거나 저장하는 모든 엔터티는 NIST SP 800-171의 엄격한 요구 사항을 준수해야 합니다. 이 테스트는 Microsoft의 범위 내 클라우드 서비스가 Microsoft가 완전한 준수를 보장하는 CUI 워크로드를 배포하는 고객을 수용할 수 있도록 합니다. 예를 들어 정보 시스템에서 범위 내 Microsoft 클라우드 서비스를 사용하여 '적용된 방어 정보'를 처리, 저장 또는 전송하는 모든 DoD 계약자는 NIST SP 800-171의 보안 요구 사항을 준수해야 하는 미 국방부 DFARS 조항을 충족합니다.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 범위 내 클라우드 서비스

- [Azure Government](https://aka.ms/AzureCompliance)
- [Azure Commercial](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [Dynamics 365 미국 정부](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 미국 GCC(정부 커뮤니티 클라우드), Office 365 GCC High 및 DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

- [NIST SP 800-171과의 Azure Government 규정 준수에 대한 의거](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>구현 방법

- [Azure Blueprint 샘플:](https://docs.microsoft.com/azure/governance/blueprints/samples/)NIST 기반 컨트롤을 준수하는 워크로드 구현에 대한 지원을 얻습니다.

## <a name="frequently-asked-questions"></a>질문과 대답

**조직에서 NIST SP 800-171과 함께 Microsoft 규정 준수를 사용할 수 있나요?**

예. Microsoft 고객은 자체 FedRAMP 및 NIST 위험 분석 및 자격 취득 노력의 일부로 FedRAMP 표준에 대해 독립적인 타사 평가 조직(3PAO)의 보고서에 설명된 감사 컨트롤을 사용할 수 있습니다. 이러한 보고서는 Microsoft가 범위 내 클라우드 서비스에서 구현한 컨트롤의 효율성을 시사합니다. 고객은 CUI 워크로드가 NIST SP 800-171 지침을 준수하는지 확인합니다.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험을 평가해 보세요.

[Microsoft 준수 관리자](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [Microsoft DoD 인증이 NIST 800-171 요구 사항을 충족합니다.](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 규정 준수가 사이버 보안 설명서로 시작](https://www.nist800171.com/)
- [Microsoft 클라우드 서비스 FedRAMP 권한 부여](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [OFFICE 365 GCC High를 통해 NIST 800-171 3.3 감사 및 책임](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft와 NIST 사이버 보안 프레임워크](offering-nist-csf.md)
- [Microsoft Government 클라우드](https://www.microsoft.com/enterprise/government)
- [Microsoft 보안 센터에 대한 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
