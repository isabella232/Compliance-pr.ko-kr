---
title: 인터넷 보안 센터 (CIS) 벤치마크
description: 인터넷 보안 센터 (CIS)는 Microsoft 제품 및 서비스에 대한 일련의 벤치마크를 발표했습니다.
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
ms.openlocfilehash: 18da1f6b422327f42dc517fa0f9c8abe9c91e253
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948206"
---
# <a name="center-for-internet-security-cis-benchmarks"></a>인터넷 보안 센터 (CIS) 벤치마크

## <a name="about-cis-benchmarks"></a>CIS 벤치마크 정보

[인터넷 보안 센터](https://www.cisecurity.org/)는 '사이버 방어를 위한 모범 사례 솔루션을 식별, 개발, 검증, 홍보 및 유지하는' 사명을 가진 비영리 단체입니다. 전세계 정부, 기업 및 학계의 사이버 보안 및 IT 전문가의 전문 지식을 바탕으로 합니다. CI 벤치 마크, 제어 및 강화된 이미지를 비롯한 표준 및 모범 사례를 개발하기 위해 합의된 의사 결정 모델을 따릅니다.  
  
[CIS 벤치 마크](https://www.cisecurity.org/cis-benchmarks/)는 시스템을 안전하게 구성하는 데 유용한 구성 기준과 모범 사례입니다. 각 지침 권장 사항은 조직이 사이버 방어 기능을 개선하는 데 도움이 되도록 개발된 하나 이상의 [CIS 컨트롤](https://www.cisecurity.org/controls/)을 참조합니다. CIS 컨트롤은 NIST 사이버 보안 프레임워크 (CSF) 및 NIST SP 800-53, ISO 27000 표준 시리즈, PCI DSS, HIPAA 등을 포함하여 다양한 표준 및 규제 프레임워크에 매핑됩니다.  
  
각 벤치마크는 2 단계의 합의 검토를 거칩니다. 첫 번째는 초기 개발 과정에서 전문가들이 벤치마크에 대한 합의에 도달할 때까지 작업 초안을 논의, 작성 및 테스트하기 위해 소집할 때 이루어집니다. 두 번째 단계에서는 벤치마크가 게시된 후 컨센서스팀이 인터넷 커뮤니티의 피드백을 검토하여 벤치마크에 통합합니다.  
  
CIS 벤치마크는 두 가지 수준의 보안 설정을 제공합니다.

- **레벨 1** 은 모든 시스템에서 구성 할 수 있는 필수 기본 보안 요구 사항을 권장하며 서비스 중단 또는 기능 저하가 거의 또는 전혀 발생하지 않아야 합니다.
- **레벨 2** 는 일부 보안 기능이 저하될 수 있는 더 높은 보안이 필요한 환경에 대한 보안 설정을 권장합니다.

[CIS 강화 이미지](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/)는 레벨 1 또는 레벨 2 CIS 벤치마크 프로필로 강화된 CIS 벤치 마크를 기반으로 안전하게 구성된 가상 머신 이미지입니다. 강화는 시스템을 사이버 공격에 취약하게 만드는 잠재적인 취약점을 제한하여 무단 액세스, 서비스 거부 및 기타 사이버 위협으로부터 보호하는 프로세스입니다.

## <a name="microsoft-and-the-cis-benchmarks"></a>Microsoft와 CIS 벤치마크

인터넷 보안 센터 (CIS)는 Microsoft Azure 및 Microsoft 365 Foundations 벤치마크, Windows 10 벤치마크 및 Windows Server 2016 벤치마크를 포함한 Microsoft 제품 및 서비스에 대한 벤치마크를 발표했습니다. [CIS Microsoft Azure Foundations 벤치마크](https://www.cisecurity.org/benchmark/azure/)는 Azure를 통합하는 솔루션을 개발, 배포, 평가 또는 보호하려는 고객을 위한 것입니다. 이 문서에서는 Azure에 대한 보안 기준 구성을 설정하기 위한 규범적인 지침을 제공합니다.
  
CIS 벤치마크는 사이버 공격으로부터 IT 시스템 및 데이터를 방어하기 위한 보안 표준으로 국제적으로 인정받고 있습니다. 수천 개의 기업에서 사용하는 보안 기준 구성을 설정하기 위한 규정 지침을 제공합니다. 시스템 및 응용 프로그램 관리자, 보안 전문가 및 Microsoft 제품 및 서비스를 사용하여 솔루션을 개발하는 사용자는 이러한 모범 사례를 사용하여 응용 프로그램의 보안을 평가하고 향상시킬 수 있습니다.  
  
모든 CIS 벤치마크와 마찬가지로 Microsoft 벤치 마크는 소프트웨어 개발, 감사 및 준수, 보안 연구, 운영, 정부 및 법률에 걸친 다양한 배경을 가진 주제 전문가의 의견을 바탕으로 합의 검토 프로세스를 사용하여 만들어졌습니다. Microsoft는 이러한 CIS 노력의 결과로 핵심 파트너가 되었습니다. 예를 들어, Office 365는 나열된 서비스에 대해 테스트를 거쳤으며 그 결과 Microsoft 365 Foundations 벤치마크는 계정 및 인증, 데이터 관리, 응용 프로그램 권한, 저장소 및 기타 보안 정책 영역을 포괄하는 적절한 보안 정책을 설정하기 위한 광범위한 권장 사항을 다룹니다.  
  
Microsoft 제품 및 서비스에 대한 벤치마크 외에도 CIS는 CIS 벤치마크를 충족하도록 구성되고 Microsoft Azure Marketplace에서 사용할 수 있는 [CIS 강화 이미지](https://www.cisecurity.org/cis-hardened-images/microsoft/)를 Azure에 게시했습니다. 이러한 이미지에는 Windows Server 2016 및 Windows Server 2019용 CIS 강화 이미지와 여러 버전의 Linux가 포함됩니다. Azure Marketplace에서 사용할 수 있는 모든 CIS 강화 이미지는 Microsoft Azure에서 실행되도록 인증되었습니다. [CIS](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/)에 명시된 내용에 따르면, ‘Microsoft Azure 퍼블릭 클라우드, 클라우드 OS 네트워크를 통해 서비스 공급자가 호스트하는 Microsoft 클라우드 플랫폼 및 고객이 관리하는 온-프레미스 프라이빗 클라우드 Windows Server Hyper-V 배포와의 호환성에 대해 사전 테스트를 거쳤습니다.’

[CIS 강화 이미지](https://www.cisecurity.org/cis-hardened-images/)는 레벨 1 또는 레벨 2 CIS 벤치마크 프로필로 강화된 CIS 벤치 마크를 기반으로 안전하게 구성된 가상 머신 이미지입니다. 강화는 시스템을 사이버 공격에 취약하게 만드는 잠재적인 취약점을 제한하여 무단 액세스, 서비스 거부 및 기타 사이버 위협으로부터 보호하는 프로세스입니다. CIS 강화 이미지는 Azure와 Azure Government 모두에서 사용할 수 있습니다.

추가 고객 지원을 위해 Microsoft는 리소스, 역할 기반 액세스 제어 및 정책을 프로비전하기 위한 Azure Resource Manager 템플릿과 같은 구성 가능한 아티팩트를 사용하여 반복 가능한 방식으로 클라우드 환경을 배포 및 업데이트하는 데 도움이 되는 서비스인 [Azure Blueprints](https://azure.microsoft.com/services/blueprints/)를 제공합니다. Azure Blueprints를 통해 프로비전된 리소스는 조직의 표준, 패턴 및 규정 준수 요구 사항을 준수합니다. Azure Blueprints의 가장 중요한 목표는 클라우드 환경에서 규정 준수 및 사이버 보안 위험 관리를 자동화하는 것입니다. CIS Azure Foundations 벤치마크 권장 사항을 구현해야 하는 모든 Azure 기반 아키텍처에 대한 핵심 정책 세트를 배포하는 데 도움이 되도록 Microsoft는 [CIS Microsoft Azure Foundations 벤치마크용 Azure Blueprint](/azure/governance/blueprints/samples/cis-azure-1-3-0)를 게시했습니다. 아키텍처에 할당되면 할당된 정책 정의를 준수하는지 Azure Policy에서 리소스를 평가합니다.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 범위 내 클라우드 플랫폼 및 서비스

- [Azure 및 Azure Government](https://aka.ms/AzureCompliance)
- [Office 및 Microsoft 365](https://aka.ms/o365-compliance-framework)
- SQL Server
- Windows 10
- Windows Server 2016

## <a name="audits-reports-and-certificates"></a>감사, 보고서 및 인증서

Microsoft 제품 및 서비스에 대한 [CIS 벤치마크 전체 목록](https://www.cisecurity.org/cis-benchmarks/)을 받으세요.

- [CIS Azure Foundations 벤치마크](https://www.cisecurity.org/benchmark/azure/)
- [CIS Microsoft 365 Foundations 벤치마크](https://www.cisecurity.org/benchmark/microsoft_office/)
- [Windows 10 벤치마크](https://www.cisecurity.org/benchmark/microsoft_windows_desktop/)
- [Windows Server 2016 벤치마크](https://www.cisecurity.org/benchmark/microsoft_windows_server/)

## <a name="how-to-implement"></a>구현 방법

- [Azure 용 CIS 벤치마크](https://azure.microsoft.com/mediahandler/files/resourcefiles/cis-microsoft-azure-foundations-security-benchmark/CIS_Microsoft_Azure_Foundations_Benchmark_v1.0.0.pdf): Azure의 보안 기준 구성을 설정하기 위한 규정 지침을 받으세요.  
- [Microsoft 365 보안 로드맵](/microsoft-365/security/office-365-security/security-roadmap): 이 로드맵을 따르면 데이터 침해 또는 계정 손상 가능성을 최소화합니다.
- [Windows 보안 기준](/windows/security/threat-protection/windows-security-baselines): 조직에서 보안 기준을 효과적으로 사용하려면 다음 지침을 따르세요.
- [CIS 컨트롤 클라우드 도우미 가이드](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/): CIS Controls 버전 7의 보안 모범 사례를 클라우드 환경에 적용하는 방법에 대한 지침을 받으세요.

## <a name="frequently-asked-questions"></a>자주하는 질문

**CIS 벤치마크 설정을 따르면 응용 프로그램의 보안이 보장되나요?**

CIS 벤치마크는 범위 내 Microsoft 제품 및 서비스를 채택하는 모든 사용자를 위한 기본 보안 수준을 설정합니다. 그러나 이는 가능한 모든 보안 구성 및 아키텍처의 전체 목록이 아닌 시작점으로 간주해야합니다. 각 조직은 여전히 특정 상황, 작업 부하 및 규정 준수 요구사항을 평가하고 그에 따라 환경을 조정해야합니다.

**CIS 벤치마크는 얼마나 자주 업데이트 되나요?**

수정된 CIS 벤치 마크 릴리스는 이를 개발한 IT 전문가 커뮤니티와 벤치마크가 지원하는 기술 릴리스 일정에 따라 변경됩니다. CIS는 새로운 벤치마크 및 기존 벤치마크에 대한 업데이트를 알리는 월별 보고서를 배포합니다. 이를 받으려면 [CIS Workbench](https://workbench.cisecurity.org/)(무료)에 등록하고 프로필에서 뉴스 레터 수신을 선택합니다.

**누가 Microsoft CIS 벤치마크 개발에 기여했나요?**

CIS는 '벤치마크는 주제 전문가, 기술 공급업체, 공공 및 민간 CIS 벤치마크 커뮤니티 구성원 및 CIS 벤치마크 개발팀의 너그러운 자원 봉사 노력을 통해 개발되었습니다.'라고 말합니다. 예를 들어 [CIS Microsoft Azure Foundations Benchmark v1.0.0 Now Available](https://www.cisecurity.org/blog/cis-microsoft-azure-foundations-benchmark-v1-0-0-now-available/)에서 Azure 기여자 목록을 찾을 수 있습니다.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="resources"></a>리소스

- [Azure 규정 준수 문서](/azure/compliance/)
- [Azure는 규정 준수의 세계를 구현합니다.](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Microsoft 365, 규정 준수, 제품](/compliance/regulatory/offering-home)
- [Microsoft 보안 센터의 규정 준수](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [CIS Microsoft Azure Foundations 벤치마크](https://www.cisecurity.org/benchmark/azure/)는 Azure 보안을 위한 단계별 체크리스트를 제공합니다.
- [Microsoft Azure의 CIS 강화 이미지](https://www.cisecurity.org/cis-hardened-images/microsoft/)는 Azure 인증을 받았으며 CIS 벤치마크의 보안 권장 사항에 맞게 사전 구성되었습니다.  Azure 및 Azure Government 모두에서 사용할 수 있습니다.
- [CIS Microsoft Azure Foundations 벤치마크용 Azure Blueprint](/azure/governance/blueprints/samples/cis-azure-1-3-0)는 고객이 CIS Azure Foundations 벤치마크 권장 사항을 구현해야 하는 모든 Azure 기반 아키텍처에 대한 핵심 정책 세트를 배포하는 데 도움이 됩니다.
- [Azure Policy 권장 사항 매핑](/azure/governance/policy/samples/cis-azure-1-3-0)은 위의 청사진에 포함된 정책 정의와 이러한 정책 정의가 CIS Microsoft Azure Foundations 벤치마크의 규정 준수 도메인 및 컨트롤에 매핑되는 방식에 대한 세부 정보를 제공합니다. 아키텍처에 할당되면 Azure Policy에서 할당된 정책 정의를 준수하지 않는지에 대해 리소스를 평가합니다.
- [CIS 컨트롤 클라우드 도우미 가이드](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/)는 CIS Controls 버전 7의 보안 모범 사례를 클라우드 환경에 적용하는 방법에 대한 지침을 제공합니다.
- [CIS Microsoft 365 Foundations 벤치마크](https://www.cisecurity.org/benchmark/microsoft_office/)는 Microsoft 365의 보안 기준 구성을 설정하기 위한 규범적 지침을 제공합니다.
- [Windows 10 보안 정책 설정](/windows/security/threat-protection/security-policy-settings/security-policy-settings)
- [Windows 10 Enterprise 보안](/windows/security/index)
