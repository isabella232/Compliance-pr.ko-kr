---
title: Microsoft 365 엔지니어링에 대한 내부 Microsoft 365 로깅
description: 이 문서에서는 엔지니어링 팀의 내부 로깅이 작동하는 Microsoft 365 있습니다.
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
ms.openlocfilehash: 20a21fe0d67f8986ec6e89b8ecbfd2915f9b8245
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947216"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 엔지니어링에 대한 내부 로깅

Microsoft는 고객이 사용할 수 있는 이벤트 및 로그 데이터 외에도 microsoft 엔지니어가 사용할 수 있는 내부 로그 데이터 Microsoft 365 유지 관리합니다. 여러 유형의 로그 데이터가 Microsoft 365 서버에서 NRT(거의 실시간) 분석을 위한 독점 보안 모니터링 솔루션으로 업로드되어 장기 저장소를 위한 내부 Cosmos(big data computing Service)에 업로드됩니다. 이 데이터 전송은 ODL(Office Data Loader)이라는 전용 자동화 도구를 사용하여 승인된 포트 및 프로토콜에서 FIPS 140-2 유효성이 검사된 TLS 연결을 통해 발생합니다. 감사 레코드를 Microsoft 365 데 사용되는 도구는 원래 감사 레코드 콘텐츠 또는 시간 순서를 영구적으로 또는 돌이할 수 없는 변경을 허용하지 않습니다.

서비스 팀은 Cosmos 저장소로 사용하여 응용 프로그램 사용 현황을 분석하고 시스템 및 운영 성능을 측정하고 문제나 보안 문제를 나타낼 수 있는 비정상 및 패턴을 검색합니다. 각 서비스 팀은 다음을 포함하는 기준을 업로드합니다.

- 이벤트 로그
- AppLocker 로그
- 성능 데이터
- System Center 데이터
- 통화 정보 기록
- 환경 품질 데이터
- IIS 웹 서버 로그
- SQL Server 로그
- Syslog 데이터
- 보안 감사 로그

업로드하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용하여 테넌트 정보 및 최종 사용자 식별 가능 정보와 같은 고객 데이터가 포함된 모든 필드를 제거하고 해당 필드를 해시 값으로 대체합니다. 스크러빙된 로그는 Cosmos 및 성능 지표에 대한 로그를 분석하는 NRT 보안 모니터링 솔루션에 업로드됩니다. 감사 로그 데이터 보존 기간은 Cosmos 팀에 의해 결정됩니다. 대부분의 감사 로그 데이터는 보안 인시던트 조사를 지원하고 규정 보존 요구 사항을 충족하기 위해 90일 이상 보존됩니다.

사용자 Microsoft 365 데이터에 대한 액세스는 Cosmos 권한이 있는 직원으로 제한됩니다. Microsoft는 감사 로그 관리를 감사 기능을 담당하는 보안 팀 구성원의 제한된 하위 집합으로 제한합니다. 보안 팀은 보안 팀에 대한 관리자 액세스 권한이 Cosmos 모든 변경 내용이 기록 및 감사됩니다.

NRT 분석 후 각 서비스 팀은 데이터 상관 관계, 대화형 쿼리 및 데이터 분석을 위해 분석 도구 및 대시보드를 사용할 수 있습니다. 이러한 보고서는 서비스의 전반적인 성능을 모니터링하고 개선하는 데 사용됩니다.
