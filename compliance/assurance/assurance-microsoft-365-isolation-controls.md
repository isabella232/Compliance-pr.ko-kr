---
title: Microsoft 365 격리 컨트롤
description: 2016년 8월 1일부로 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 312de9f1417ba6298898d47b2b7e05b5fa7034fe
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481900"
---
# <a name="microsoft-365-isolation-controls"></a>Microsoft 365 격리 컨트롤

Microsoft는 Microsoft의 다중 테넌트 아키텍처가 엔터프라이즈 수준의 보안Microsoft 365 기밀성, 개인 정보 보호, 무결성, 로컬, 국제 및 가용성 표준을 지원하도록 지속적으로 [작업합니다.](https://www.microsoft.com/trust-center/compliance/compliance-overview) Microsoft에서 제공하는 서비스의 규모와 범위는 사용자 개입이 많은 서비스를 관리하기 어렵고 Microsoft 365 비가치적입니다. Microsoft 365 서비스는 휴먼 터치 또는 고객 콘텐츠에 대한 액세스가 필요한 몇 가지 작업으로 각각 고도로 자동화된 글로벌 분산 데이터 센터를 통해 제공됩니다. 당사의 직원은 자동화된 도구와 매우 안전한 원격 액세스를 사용하여 이러한 서비스 및 데이터 센터를 지원하고 있습니다.

Microsoft 365 중요한 비즈니스 기능을 제공하고 전체 비즈니스 환경을 제공하는 여러 Microsoft 365 구성됩니다. 이러한 각 서비스는 자체 포함하며 서로 통합하도록 디자인됩니다. Microsoft 365 다음 원칙에 따라 디자인됩니다.

- 서비스 지향 아키텍처: 잘 정의된 비즈니스 기능을 제공하는 상호 연결 가능한 서비스 형태로 소프트웨어를 디자인하고 개발합니다.
- [운영 보안](https://www.microsoft.com/securityengineering/osa)보증 : [Microsoft](https://www.microsoft.com/sdl/default.aspx)보안 개발 수명 주기, Microsoft 보안 대응 센터, 사이버 보안 위협 [](https://www.microsoft.com/msrc)환경의 심층 인식을 포함하여 Microsoft 고유의 다양한 기능을 통해 얻은 지식을 통합하는 프레임워크입니다.

Microsoft 365 상호 운영되지만 서로 독립적으로 자율 서비스로 배포 및 운영될 수 있도록 설계 및 구현된 서비스입니다. Microsoft는 조직의 자산을 무단 또는 Microsoft 365 잘못 수정하거나 오용할 기회를 줄이기 위해 조직에 대한 책임 영역과 의무를 세분화합니다. Microsoft 365 팀은 포괄적인 역할 기반 액세스 제어 메커니즘의 일부로 역할을 정의했습니다.

## <a name="tenant-isolation"></a>테넌트 격리

클라우드 컴퓨팅의 주요 이점 중 하나는 많은 고객에 걸쳐 동시에 공유되는 공유 인프라의 개념으로 확장되는 경제성입니다. Microsoft는 클라우드 서비스의 다중 테넌트 아키텍처가 엔터프라이즈 수준 보안, 기밀성, 개인 정보 보호, 무결성 및 가용성 표준을 지원하도록 지속적으로 노력하고 있습니다.

Microsoft 클라우드 서비스는 모든 테넌트가 다른 모든 테넌트에 잠재적으로 악의적일 수 있는 것으로 가정하고, 한 테넌트의 작업이 다른 테넌트의 보안 또는 서비스에 영향을 미치거나 다른 테넌트의 콘텐츠에 액세스하지 못하도록 하는 보안 조치를 구현했습니다.

다중 테넌트 환경에서 테넌트 고리의 두 가지 주요 목표는 다음입니다.

- 테넌트 전체의 고객 콘텐츠 누출 또는 무단 액세스 방지 및
- 한 테넌트의 작업이 다른 테넌트의 서비스에 부정적인 영향을 주지 않도록 방지

고객이 Microsoft 365 Microsoft 365 서비스 또는 응용 프로그램을 타협하거나 다른 테넌트 또는 Microsoft 365 시스템 자체의 정보에 무단으로 액세스하지 못하게 방지하기 위해 여러 형태의 보호가 Microsoft 365 구현되었습니다.

- Microsoft 365 서비스에 대한 각 테넌트 내에서 고객 콘텐츠를 논리적으로 Azure Active Directory 권한 부여 및 역할 기반 액세스 제어를 통해 달성됩니다.
- SharePoint Online은 저장소 수준에서 데이터 고리 메커니즘을 제공합니다.
- Microsoft는 엄격한 물리적 보안, 백그라운드 심사 및 다계층 암호화 전략을 사용하여 고객 콘텐츠의 기밀성 및 무결성을 보호합니다. 모든 Microsoft 365 데이터 센터에는 생체 인식 액세스 제어가 있습니다. 물리적 액세스를 얻기 위해 대부분 팜 인쇄가 요구됩니다. 또한 모든 미국 기반 Microsoft 직원은 채용 프로세스의 일부로 표준 배경 검사를 성공적으로 완료해야 합니다. 관리 액세스에 사용되는 컨트롤에 대한 자세한 내용은 Microsoft 365 계정 Microsoft 365 [참조하세요.](assurance-microsoft-365-account-management.md)
- Microsoft 365 BitLocker, 파일당 암호화, TLS(전송 계층 보안) 및 IPsec(인터넷 프로토콜 보안)을 포함하여 미사용 고객 콘텐츠를 암호화하는 서비스 쪽 기술을 사용합니다. 암호화에 대한 자세한 내용은 Microsoft 365 데이터 암호화 [기술을 Microsoft 365.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)

위에 나열된 보호는 물리적으로만 제공된 위협 방지 및 완화 기능을 제공하는 강력한 논리적 차단 컨트롤을 제공합니다.

## <a name="resources"></a>리소스

- [2016년 8월 1일부로 Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [테넌트 경계 모니터링 및 테스트](assurance-monitoring-and-testing.md)
- [2016년 8월 1일부로 Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
