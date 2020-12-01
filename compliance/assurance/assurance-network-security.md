---
title: 네트워크 보안
description: Microsoft 365의 네트워크 보안에 대해 자세히 알아보기
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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507760"
---
# <a name="network-security-overview"></a>네트워크 보안 개요

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365에서 네트워크 경계를 보호 하는 방법

Microsoft 365에서는 스팸 방지 및 맬웨어 방지 보호를 위해 네트워크 기반 공격, 특수 방화벽 장치 및 EOP (Exchange Online Protection)의 자동 검색 및 방지 기능을 비롯 하 여 네트워크 경계를 보호 하기 위한 여러 전략을 채택 하 고 있습니다. 또한 Microsoft 365는 세그먼트 간에 허용 되는 통신만 포함 하 여 프로덕션 환경을 논리적으로 격리 된 네트워크 세그먼트로 분리 합니다. 경계 점에서 추가 네트워크 방화벽을 사용 하 여 네트워크 트래픽을 보호 하 여 네트워크 공격을 감지, 방지 및 완화할 수 있습니다.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365이 DDoS 공격 으로부터 보호 하는 방법

Microsoft의 대규모 인터넷 소개는 여러 분산 서비스 거부 (DDoS) 공격에 부정적인 영향을 insulates 합니다. 각 Microsoft 365 서비스의 배포 된 인스턴스와 각 서비스에 대 한 여러 경로는 시스템에 대 한 DDoS 공격의 영향을 제한 합니다. 이러한 중복성을 통해 Microsoft 365의 DDoS 공격을 흡수 하 고 DDoS 공격을 검색 하 고 완화 하는 데 사용할 수 있는 시간이 증가 하기 전에 서비스 가용성에 영향을 줍니다.

Microsoft의 중복 시스템 아키텍처 외에도 Microsoft는 정교한 검색 및 완화 도구를 사용 하 여 DDoS 공격에 대응 합니다. 특수 용도의 방화벽은 경계를 네트워크에 통과 하기 전에 원치 않는 트래픽을 모니터링 하 고 삭제 하 여 네트워크 경계 내에 있는 시스템에 대 한 스트레스를 줄여줍니다. 클라우드 서비스를 추가로 보호 하기 위해 Microsoft는 Microsoft Azure의 일부로 배포 된 DDoS 방어 시스템을 활용 합니다. Azure DDoS 방어 시스템은 외부 및 기타 Azure 테 넌 트 로부터의 공격을 견딜 수 있도록 설계 되었습니다.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365이 온라인 서비스를 통해 업로드 되거나 전송 되는 스팸 및 맬웨어로부터 사용자를 보호 하는 방법

Microsoft 365는 맬웨어 방지 보호를 Exchange Online 및 SharePoint Online과 같은 악의적인 코드의 벡터로 될 수 있는 서비스에 구축 합니다. EOP (Exchange Online Protection)에서는 감염 된 메시지와 첨부 파일을 배달 하지 못하도록 맬웨어를 입력 하 고 종료 하는 모든 전자 메일 및 전자 메일로 해당 첨부 파일을 검사 합니다. 고급 스팸 필터링은 인바운드 및 아웃 바운드 메시지에 자동으로 적용 되므로 고객 조직에서 스팸을 수신 하 고 보내지 못하도록 방지할 수 있습니다. 이 보호 계층은 피싱 공격과 같이 원치 않거나 권한이 없는 전자 메일을 활용 하는 공격을 방지 합니다. SharePoint Online은 동일한 바이러스 검색 엔진을 사용 하 여 업로드 된 파일의 맬웨어를 선택적으로 검사 합니다. 파일이 감염 된 것으로 표시 되 면 사용자는 클라이언트 끝점을 보호 하기 위해 파일을 다운로드 하거나 동기화 할 수 없습니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 네트워크 보안과 관련 된 컨트롤의 유효성 검사에 대해서는 다음 표를 참조 하세요.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: 서비스 거부 보호 <br> SC-7: 경계 보호 <br> SI-2: 결함 치료 <br> SI-3: 악성 코드 보호 <br> SI-8: 스팸 방지 | 2020 년 9 월 24 일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: 취약성 검사 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: 취약성 검사 <br> CA-45: 맬웨어 방지 | 2019년 9월 30일 |