---
title: Microsoft 365 데이터 손상 처리
description: 이 문서에서는 데이터 손상에 대해 Microsoft 365 Microsoft가 데이터를 방지 및 복구하기 위해 취한 노력에 대해 설명하고 있습니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160294"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>데이터 손상을 Microsoft 365

대규모 클라우드 서비스를 실행하는 데 까다로울 수 있는 측면 중 하나는 데이터 및 독립적인 시스템이 많은 경우 데이터 손상을 처리하는 방법입니다. 데이터 손상은 다음으로 인해 발생할 수 있습니다.

- 응용 프로그램 또는 인프라 버그, 응용 프로그램 상태 일부 또는 전체 손상
- 데이터가 손실되거나 데이터를 읽지 못하게 하는 하드웨어 문제
- 휴먼 운영 오류
- 악의적인 해커 및 불만이 있는 직원
- 데이터가 일부 손실되는 외부 서비스의 인시던트

데이터 무결성의 복구력은 데이터 손상 인시던트 수가 줄어든다는 것을 의미하기 때문에 Microsoft는 데이터 손상 발생을 방지하기 위한 Microsoft 365 보호 메커니즘과 데이터 복구를 가능하게 하는 시스템 및 프로세스를 구축했습니다. 검사 및 프로세스는 다음을 포함하여 데이터 손상에 대한 탄력성 향상을 위한 엔지니어링 릴리스 프로세스의 다양한 단계 내에 있습니다.

- 시스템 디자인
- 코드 조직 및 구조
- 코드 검토
- 단위 테스트, 통합 테스트 및 시스템 테스트
- 트립 와이어 테스트/게이트

모든 Microsoft 365 환경에서 데이터 센터 간의 피어 복제를 통해 항상 모든 데이터의 라이브 복사본이 여러 개 있습니다. 표준 이미지 및 스크립트는 손실된 서버를 복구하는 데 사용하며, 복제된 데이터는 고객 데이터를 복원하는 데 사용됩니다. Microsoft는 기본 제공 데이터 복구 검사 및 프로세스로 인해 Microsoft 365 Online의 기본 제공 복제와 내부 코드 리포지토리 도구인 Source Depot를 사용하여 Microsoft 365 SharePoint 정보 시스템 설명서(보안 관련 설명서 포함)의 백업만 유지 관리합니다. 시스템 설명서는 SharePoint 온라인에 저장되고 원본 디포트에는 시스템 및 응용 프로그램 이미지가 포함되어 있습니다. 온라인 SharePoint 및 원본 디포 모두 버전 기능을 사용하며 거의 실시간으로 복제됩니다.
