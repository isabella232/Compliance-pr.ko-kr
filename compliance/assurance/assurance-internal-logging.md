---
title: Microsoft 365 엔지니어링용 Microsoft 365 내부 로깅
description: 이 문서에서는 Microsoft 365 엔지니어링 팀에 대한 내부 로깅의 작동 방식에 대한 설명을 찾아보아야 합니다.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497070"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 엔지니어링에 대한 내부 로깅

고객이 사용할 수 있는 이벤트 및 로그 데이터 외에도 Microsoft 365 엔지니어가 사용할 수 있는 내부 로그 데이터 수집 시스템도 있습니다. Microsoft 365 서버에서 Cosmos라는 내부의 빅 데이터 컴퓨팅 서비스로 다양한 유형의 로그 데이터가 업로드됩니다. 각 서비스 팀은 집계 및 분석을 위해 해당 서버에서 Cosmos 데이터베이스로 감사 로그를 업로드합니다. 이 데이터 전송은 ODL(Office 데이터 로더)이라는 독점 자동화 도구를 사용하여 특별히 승인된 포트 및 프로토콜에서 FIPS 140-2 유효성이 검사된 TLS 연결을 통해 발생합니다. 감사 레코드를 수집하고 처리하기 위해 Microsoft 365에서 사용되는 도구는 원래 감사 레코드 콘텐츠 또는 시간 순서를 영구적으로 또는 돌이할 수 없는 변경을 허용하지 않습니다.

서비스 팀은 Cosmos를 중앙 리포지토리로 사용하여 응용 프로그램 사용 현황 분석을 수행하고, 시스템 및 운영 성능을 측정하고, 문제나 보안 문제를 나타낼 수 있는 비정상 및 패턴을 검색합니다. 각 서비스 팀은 분석할 콘텐츠에 따라 다음과 같은 기본 로그를 Cosmos에 업로드합니다.

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

Cosmos에 데이터를 업로드하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용하여 테넌트 정보 및 최종 사용자 식별 가능 정보와 같은 고객 데이터가 포함된 필드를 난청하고 해당 필드를 해시 값으로 바환합니다. The anonymized and hashed logs are rewritten and then uploaded into Cosmos. 서비스 팀은 상관 관계, 경고 및 보고를 위해 Cosmos의 데이터에 대해 범위가 지정한 쿼리를 실행합니다. Cosmos의 감사 로그 데이터 보존 기간은 서비스 팀에 의해 결정됩니다. 대부분의 감사 로그 데이터는 보안 인시던트 조사를 지원하고 규정 보존 요구 사항을 충족하기 위해 90일 이상 보존됩니다.

Cosmos에 저장된 Microsoft 365 데이터에 대한 액세스는 승인된 직원으로 제한됩니다. Microsoft는 감사 기능을 담당하는 서비스 팀 구성원의 제한된 하위 집합으로 감사 기능 관리를 제한합니다. 이러한 팀 구성원은 Cosmos에서 데이터를 수정하거나 삭제할 수 없습니다. Cosmos에 대한 로깅 메커니즘에 대한 모든 변경 내용이 기록 및 감사됩니다.

각 서비스 팀은 특정 응용 프로그램이 특정 분석을 수행하도록 권한을 부여하여 분석을 위해 로그 데이터에 액세스합니다. 예를 들어 Microsoft 365 보안 팀은 Cosmos의 데이터를 독점 이벤트 로그 파서로 사용하여 Microsoft 365 프로덕션 환경에서 의심스러운 활동과 관련, 경고 및 실행 가능한 보고서를 생성합니다. 이 데이터의 보고서는 취약점을 수정하고 서비스의 전반적인 성능을 개선하는 데 사용됩니다. 특정 경고 또는 보고서에 추가 조사가 필요한 경우 서비스 담당자는 데이터를 Microsoft 365 서비스로 다시 가져올 수 있도록 요청할 수 있습니다. Cosmos에서 가져오는 특정 로그는 암호화되어 있으며 서비스 담당자는 암호 해독 키에 액세스할 수 없습니다. 대상 로그는 프로그래밍적으로 암호 해독 서비스를 통해 전달되며, 암호 해독 서비스는 범위가 지정한 서비스 담당자에게 반환됩니다. 이 연습에서 발견된 모든 취약점은 Microsoft의 표준 보안 인시던트 관리 채널을 사용하여 보고 및 에스컬레이터됩니다.
