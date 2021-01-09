---
title: 감사 로깅 개요
description: Microsoft 365의 감사 로깅에 대해 자세히
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
ms.openlocfilehash: 6e32e089a5b42f846a332e32218959fef5103615
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787507"
---
# <a name="audit-logging-overview"></a>감사 로깅 개요

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365는 감사 로깅을 어떻게 사용하나요?

Microsoft 365는 감사 로깅을 통해 제품 및 서비스에서 권한이 없는 활동을 감지하고 Microsoft 직원에게 책임 제공 감사 로그는 시스템 구성 변경 및 액세스 이벤트에 대한 세부 정보를 캡처하고, 활동의 책임자, 활동이 언제 및 어디에서 진행된지, 활동의 결과를 식별하는 세부 정보를 제공합니다. 자동화된 로그 분석은 의심스러운 동작의 거의 실시간 검색을 지원합니다. 잠재적인 인시던트는 추가 조사를 위해 Microsoft 365 보안 대응 팀으로 에스컬레이터됩니다.

Microsoft 365 내부 감사 로깅은 다음 등의 다양한 원본에서 로그 데이터를 캡처합니다.

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

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365는 감사 로그를 중앙에서 관리하고 보고하는 방법

다양한 유형의 로그 데이터는 Microsoft 365 서버에서 Cosmos라는 내부의 큰 데이터 컴퓨팅 서비스로 업로드됩니다. 각 서비스 팀은 집계 및 분석을 위해 해당 서버에서 Cosmos 데이터베이스에 감사 로그를 업로드합니다. 이 데이터 전송은 ODL(Office 데이터 로더)이라는 독점 자동화 도구를 사용하여 승인된 포트 및 프로토콜에서 FIPS 140-2 유효성이 검사된 TLS 연결을 통해 전송됩니다.

서비스 팀은 Cosmos의 데이터에 대해 범위가 지정한 쿼리를 실행하여 로그 상관 관계, 경고 및 보고를 실행합니다. 예를 들어 Microsoft 365 보안 팀은 Cosmos의 데이터를 독점 이벤트 로그 파서와 함께 사용하여 Microsoft 365 프로덕션 환경에서 가능한 의심스러운 활동에 대한 로그 데이터 상관 관계, 경고 보내기 및 실행 가능한 보고서를 생성합니다. 이 데이터의 보고서는 취약점을 수정하고 서비스의 전반적인 성능을 개선하는 데 사용됩니다.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365는 감사 로그를 어떻게 보호하나요?

Microsoft 365에서 감사 레코드를 수집 및 처리하기 위해 사용되는 도구는 원래 감사 레코드 콘텐츠 또는 시간 순서를 영구적으로 또는 돌이할 수 없는 변경을 허용하지 않습니다. Cosmos에 저장된 Microsoft 365 데이터에 대한 액세스는 승인된 직원으로 제한됩니다. Microsoft 365는 감사 기능을 담당하는 서비스 팀 구성원의 제한된 하위 집합으로 감사 기능 관리를 제한합니다. 이러한 팀 구성원은 Cosmos에서 데이터를 수정하거나 삭제할 수 없습니다. Cosmos에 대한 로깅 메커니즘에 대한 모든 변경 내용이 기록 및 감사됩니다. 감사 로그는 인시던트 조사를 지원하고 규정 요구 사항을 충족하기에 충분히 오래 보존됩니다. Cosmos의 정확한 감사 로그 데이터 보존 기간은 서비스 팀에 의해 결정됩니다. 대부분의 감사 로그 데이터는 90일 이상 보존됩니다.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365는 감사 로그에 캡처될 수 있는 최종 사용자 식별 정보를 어떻게 보호하나요?

데이터를 Cosmos로 업로드하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용하여 테넌트 정보 및 최종 사용자 식별 가능 정보와 같은 고객 데이터가 포함된 모든 필드를 난청하고 이러한 필드를 해시 값으로 바환합니다. The anonymized and hashed logs are rewritten and then uploaded into Cosmos.

## <a name="related-external-regulations--certifications"></a>인증에 & 관련 외부 규정

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수하는지 정기적으로 감사됩니다. 감사 로깅과 관련된 컨트롤의 유효성 검사를 위해 다음 표를 참조합니다.

| **외부 감사** | **섹션** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP(Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: 감사 이벤트 <br> AU-3: 감사 레코드의 콘텐츠 <br> AU-4: 저장소 용량 감사 <br> AU-5: 감사 처리 실패에 대한 응답 <br> AU-6: 검토, 분석 및 보고 감사 <br> AU-7: 감사 감소 및 보고서 생성 <br> AU-8: 타임스탬프 <br> AU-9: 감사 정보 보호  <br> AU-10: 부인되지 않은 <br> AU-11: 감사 레코드 보존 <br> AU-12: 감사 생성  | 2020년 9월 24일 | 
| [ISO 27001/27002(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: 로깅 및 모니터링 | 2020년 2월 22일 |
| [ISO 27017(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용성 설명](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [인증](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: 로깅 및 모니터링 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: 데이터 센터 로깅 <br> CA-60: 감사 로깅 | 2020년 12월 24일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: 데이터 센터 로깅 <br> CA-60: 감사 로깅 | 2020년 12월 24일|