---
title: 네트워크 보안
description: Microsoft 365의 네트워크 보안에 대한 자세한 정보
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e246cc3c84a17fe697baea29eda285599832b0fa
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787434"
---
# <a name="network-security-overview"></a>네트워크 보안 개요

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365는 네트워크 경계를 어떻게 보호하나요?

Microsoft 365는 네트워크 기반 공격의 자동화된 감지 및 방지, 특수 방화벽 장치, 스팸 방지 및 맬웨어 방지 보호를 위한 EOP(Exchange Online Protection)를 포함하여 네트워크 경계를 보호하기 위한 여러 전략을 사용하고 있습니다. 또한 Microsoft 365는 프로덕션 환경을 논리적으로 격리된 네트워크 세그먼트로 분리하고 세그먼트 간에 필요한 통신만 허용합니다. 네트워크 트래픽은 경계 지점에서 추가 네트워크 방화벽을 사용하여 네트워크 공격을 감지, 방지 및 완화하는 데 도움이 됩니다.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365는 DDoS 공격을 어떻게 방어하나요?

Microsoft의 대규모 인터넷 상태는 분산된 DDoS(서비스 거부) 공격의 부정적인 영향으로부터 이를 분배합니다. 각 Microsoft 365 서비스의 분산된 인스턴스와 각 서비스에 대한 여러 경로는 시스템에 대한 DDoS 공격의 영향을 제한합니다. 이러한 중복성은 Microsoft 365가 DDoS 공격을 잘 아는 능력을 향상하고 DDoS 공격이 서비스 가용성에 영향을 미치기 전에 DDoS 공격을 감지하고 완화하는 데 사용할 수 있는 시간을 증가합니다.

Microsoft의 중복 시스템 아키텍처 외에도 Microsoft는 정교한 감지 및 완화 도구를 사용하여 DDoS 공격에 대응합니다. 특수 용도의 방화벽은 네트워크로 경계를 넘기기 전에 원치 않는 트래픽을 모니터링하고 삭제하여 네트워크 경계 내부에 있는 시스템에 대한 스트레스를 줄입니다. 클라우드 서비스를 더욱 보호하기 위해 Microsoft는 Microsoft Azure의 일부로 배포된 DDoS 방어 시스템을 활용합니다. Azure DDoS 방어 시스템은 외부 및 다른 Azure 테넌트의 공격을 견디기 위해 고안된 것입니다.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365는 온라인 서비스를 통해 업로드 또는 전송되는 스팸 및 맬웨어로부터 사용자를 어떻게 보호하나요?

Microsoft 365는 Exchange Online 및 SharePoint Online과 같은 악성 코드에 대한 벡터가 될 수 있는 서비스에 맬웨어 방지 보호 기능을 구축합니다. EOP(Exchange Online Protection)는 시스템에 들어오고 나갈 때 모든 전자 메일 및 전자 메일 첨부 파일에서 맬웨어를 검사하여 감염된 메시지와 첨부 파일이 배달되지 않도록 합니다. 고급 스팸 필터링은 인바운드 및 아웃바운드 메시지에 자동으로 적용되어 고객 조직이 스팸을 받고 보내지 못하도록 합니다. 이 보호 계층은 피싱 공격과 같이 원치 않는 전자 메일이나 권한이 없는 전자 메일을 활용하는 공격으로부터 보호합니다. SharePoint Online은 동일한 바이러스 검색 엔진을 사용하여 업로드된 파일에 맬웨어를 선택적으로 검사합니다. 파일이 감염된 것으로 표시된 경우 사용자는 클라이언트 끝점을 보호하기 위해 파일을 다운로드하거나 동기화할 수 없습니다.

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 네트워크 보안과 관련된 컨트롤의 유효성 검사는 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: 서비스 거부 보호 <br> SC-7: 경계 보호 <br> SI-2: 결함 수정 <br> SI-3: 악성 코드 보호 <br> SI-8: 스팸 방지 | 2020년 9월 24일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 취약점 검사 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: 취약점 검사 <br> CA-45: 맬웨어 방지 | 2020년 12월 24일 |