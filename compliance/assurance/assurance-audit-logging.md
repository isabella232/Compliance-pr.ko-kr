---
title: 감사 로깅 개요
description: Microsoft 365의 감사 로깅에 대해 자세히 알아보기
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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508625"
---
# <a name="audit-logging-overview"></a>감사 로깅 개요

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365이 감사 로깅을 사용 하는 방법은 무엇 인가요?

Microsoft 365에서는 감사 로깅을 활용 하 여 해당 제품 및 서비스에서 승인 되지 않은 활동을 검색 하 고 Microsoft 담당자에 게 책임을 부여 합니다. 감사 로그는 시스템 구성 변경 및 액세스 이벤트에 대 한 세부 정보를 캡처하여 활동을 담당 하는 사람, 활동이 발생 한 시간 및 위치, 활동의 결과를 식별 하는 세부 정보를 포함 합니다. 자동 로그 분석은 의심 스러운 동작에 대 한 실시간 검색을 지원 합니다. 향후 조사를 위해 잠재적인 사고가 Microsoft 365 보안 대응 팀으로 에스컬레이션 됩니다.

Microsoft 365 내부 감사 로깅은 다음과 같은 다양 한 원본의 로그 데이터를 캡처합니다.

- 이벤트 로그
- AppLocker 로그
- 성능 데이터
- System Center data
- 통화 정보 기록
- 경력 데이터 품질
- IIS 웹 서버 로그
- SQL Server 로그
- Syslog 데이터
- 보안 감사 로그

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365이 어떻게 감사 로그를 집중 하 고 보고 하나요?

다양 한 유형의 로그 데이터가 Microsoft 365 서버에서 Cosmos 라는 내부 대규모 데이터 컴퓨팅 서비스로 업로드 됩니다. 각 서비스 팀은 집계 및 분석을 위해 각 서버의 감사 로그를 Cosmos 데이터베이스에 업로드 합니다. 이 데이터 전송은 Office Data Loader (ODL) 라는 전용 자동화 도구를 사용 하 여 승인 된 포트 및 프로토콜에서 FIPS 140-2 유효성 검사 TLS 연결을 통해 수행 됩니다.

서비스 팀은 로그 상관 관계, 경고 및 보고를 위해 Cosmos에서 데이터에 대해 범위가 지정 된 쿼리를 실행 합니다. 예를 들어 Microsoft 365 보안 팀은 Cosmos의 데이터를 전용 이벤트 로그 파서와 함께 사용 하 여 Microsoft 365 프로덕션 환경에서 의심 스러운 작업에 대 한 로그 데이터를 연결 하 고, 알림을 보내고, 문제를 해결 하기 위한 보고서를 생성 합니다. 이 데이터의 보고서는 취약성을 수정 하 고 서비스의 전반적인 성능을 향상 시키는 데 사용 됩니다.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365에서 감사 로그를 보호 하는 방법

Microsoft 365에서 감사 레코드를 수집 하 고 처리 하는 데 사용 되는 도구는 원본 감사 레코드 콘텐츠 또는 시간 순서에 영구 또는 되돌릴 수 없는 변경을 허용 하지 않습니다. Cosmos에 저장 된 Microsoft 365 데이터에 대 한 액세스 권한이 권한 있는 담당자 에게만 제한 됩니다. Microsoft 365에서는 감사 기능을 담당 하는 서비스 팀 구성원의 제한 된 하위 집합에 대 한 감사 기능 관리를 제한 합니다. 이러한 팀 구성원은 Cosmos에서 데이터를 수정 하거나 삭제할 수 없으며 Cosmos에 대 한 로깅 메커니즘에 대 한 모든 변경 내용이 기록 및 감사 됩니다. 감사 로그는 문제 조사를 지원 하 고 규정 요구 사항을 충족 하기 위해 충분히 오랫동안 보존 됩니다. Cosmos에서 감사 로그 데이터 보존의 정확한 기간은 서비스 팀에 따라 결정 됩니다. 대부분의 감사 로그 데이터는 90 일 이상 보존 됩니다.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365에서 감사 로그에 캡처할 수 있는 최종 사용자 식별 가능 정보를 보호 하는 방법은 무엇 인가요?

Cosmos에 데이터를 업로드 하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용 하 여 테 넌 트 정보, 최종 사용자 식별 정보 등의 고객 데이터가 포함 된 모든 필드를 해시 값으로 바꿉니다. 익명 및 해시 된 로그가 다시 작성 된 다음 Cosmos에 업로드 됩니다.

## <a name="related-external-regulations--certifications"></a>관련 된 외부 규정 & 인증

Microsoft의 온라인 서비스는 외부 규정 및 인증을 준수 하기 위해 정기적으로 감사 됩니다. 감사 로깅과 관련 된 컨트롤의 유효성 검사에 대해서는 다음 표를 참조 하십시오.

| **외부 감사** | **단면** | **최신 보고서 날짜** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: 감사 이벤트 <br> AU-3: 감사 레코드의 내용 <br> AU-4: 저장소 용량 감사 <br> AU-5: 감사 처리 실패에 대 한 응답 <br> AU-6: 감사 검토, 분석 및 보고 <br> AU-7: 감사 감소 및 보고서 생성 <br> AU-8: 타임 스탬프 <br> AU-9: 감사 정보 보호  <br> AU-10: 부인 외 <br> AU-11: 감사 레코드 보존 <br> AU-12: 감사 생성  | 2020 년 9 월 24 일 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4: 로깅 및 모니터링 | 2020년 2월 22일 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [적용 가능성의 문](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [자격](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4: 로깅 및 모니터링 | 2020년 2월 22일 |
| [SOC 1(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: 데이터 센터 로깅 <br> CA-60: 감사 로깅 | 2019년 9월 30일 |
| [SOC 2(Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: 데이터 센터 로깅 <br> CA-60: 감사 로깅 | 2019년 9월 30일 |