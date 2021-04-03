---
title: Microsoft 365 보고 기능
description: Azure Active Directory 및 Exchange Online을 포함하여 Microsoft 365 내의 다양한 보고 기능에 대해 자세히 알아보십시오.
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
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2cc91f650dcaf5fdafd9f32f3c6991976b49ea04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497508"
---
# <a name="microsoft-365-reporting-features"></a>Microsoft 365 보고 기능

Microsoft 365의 보고 기능은 Azure AD(Azure Active Directory), Exchange Online, 장치 관리, 관리 검토 및 DLP(데이터 손실 방지)에 대한 다양한 감사 보고서를 제공합니다. 이러한 보고서는 Microsoft 365 활동 보고서와는 다릅니다.

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 보고서 대시보드

Microsoft 365 관리 센터 미리 보기의 보고서 대시보드에는 Microsoft 365의 사용 활동이 표시됩니다. Microsoft 365 전역 관리자 또는 Exchange Online, SharePoint Online 또는 비즈니스용 Skype 관리자는 해당 서비스의 사용 현황에 대한 세부적인 정보를 얻을 수 있습니다. 예를 들어 특정 Microsoft 365 서비스의 사용자 수, 엔터프라이즈용 Microsoft 365 앱(이전 명명된 Office 365 ProPlus)을 활성화한 사용자 수, 조직을 통해 흐르는 메일의 양. 지난 7일, 30일, 90일 및 180일 동안 보고서를 사용할 수 있습니다.

사용 가능한 보고서는 다음과 같습니다.

- [전자 메일 활동 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office 정품 인증 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online 사이트 사용 현황 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [비즈니스용 OneDrive 사용 현황 보고서](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer 활동 보고서](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [비즈니스용 Skype 활동 보고서](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [비즈니스용 Skype 피어 투 피어 활동 보고서](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [비즈니스용 Skype 회의 이끌이 보고서](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [비즈니스용 Skype 회의 참가자 활동 보고서](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

자세한 내용은 [Microsoft 365](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)관리 센터의 활동 보고서를 참조하세요.

## <a name="azure-ad-reports"></a>Azure AD 보고서

Microsoft 365는 인증 및 ID 관리에 Azure AD를 사용 합니다. Microsoft 365 관리자는 Azure에서 생성된 보고서를 사용하여 비정상적인 활동 및 데이터에 대한 무단 액세스를 식별합니다. Azure AD의 액세스 및 사용 현황 보고서를 사용하여 조직의 디렉터리 무결성 및 보안을 볼 수 있습니다. 이 정보를 사용하여 가능한 보안 위험을 식별하고 완화할 수 있습니다.

Azure AD 보고서를 Microsoft Excel로 내보낼 수 있으며 Microsoft 365의 다른 데이터와 상호 관련될 수 있습니다. 예를 들어 감사 로그 검색 결과를 통해 액세스, 인증 및 응용 프로그램 수준 활동에 대한 정보를 얻을 수 있습니다. 고급 이상 및 리소스 사용 현황 보고서는 Azure AD Premium에서 사용할 수 있습니다. 이러한 고급 보고서는 보안 자세를 개선하고 장치 액세스 및 응용 프로그램 사용에 대한 분석을 적용하여 잠재적인 위협에 대응하는 데 도움이 됩니다. 자세한 내용은 [Azure Active Directory 보고 를 참조하세요.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Exchange Online 감사 보고서

Exchange Online 감사 보고서에는 사서함 액세스 및 관리자가 Exchange Online 테넌트에 대해 변경한 내용에 대한 세부 정보가 포함됩니다. 사서함 감사를 사용하면 다음 표의 작업을 사용하여 보고서를 실행하고 Exchange Online 감사 로그를 내보낼 수 있습니다.

> [!NOTE]
> 감사된 이벤트가 해당 사서함에 대한 감사 로그에 저장될 수 있도록 각 사서함에 대해 사서함 감사 로깅을 사용하도록 설정해야 합니다. 사서함에 대해 사서함 감사 로깅을 사용하도록 설정하지 않은 경우 해당 사서함에 대한 이벤트가 감사 로그에 저장되지 않습니다. 사서함 감사 보고서에는 나타나지 않습니다. 자세한 내용은 사서함 감사 [사용 을 참조하세요.](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)

| 작업  | 설명 |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [비 소유자 사서함 액세스 보고서 실행](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | 사서함 소유자가 액세스할 수 있는 사서함 목록을 표시 합니다. 이 보고서에는 사서함에 액세스한 사용자, 사서함에서 수행한 작업 및 작업이 성공한지 여부에 대한 정보가 포함되어 있습니다. |
| [사서함 감사 로그 내보내기](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | 사서함 감사 로그에는 사서함 소유자가 다른 사용자가 수행한 사서함의 액세스 및 작업에 대한 정보가 포함되어 있습니다. 관리자는 날짜 범위와 함께 사서함을 지정하여 보고서를 생성할 수 있습니다. 로그는 XML로 내보내고 메시지에 첨부된 후 관리자가 결정한 특정 사용자에게 전송됩니다. |
| [관리자 역할 그룹 보고서 실행](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | 관리자 역할 그룹은 사용자에게 관리 권한을 할당합니다. 이러한 권한을 통해 사용자는 암호 다시 설정, 사서함 만들기 또는 수정, 다른 사용자에게 관리자 권한 할당 등의 관리 작업을 수행할 수 있습니다. 관리자 역할 그룹 보고서에는 구성원 추가 또는 제거를 비롯한 역할 그룹에 대한 변경 내용이 표시됩니다. |
| [관리자 감사 로그 보기](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | 관리자 감사 로그 보고서에는 Exchange Online 관리자가 수행한 모든 기능 만들기, 업데이트 및 삭제가 나열됩니다. 로그 항목은 실행된 cmdlet, 사용된 매개 변수, cmdlet을 실행한 사용자 및 영향을 받은 개체에 대한 정보를 제공합니다. |
| [사서함 콘텐츠 검색 및 보류](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | 사서함에 대한 eDiscovery 또는 In-Place 보류 In-Place 변경에 대한 세부 정보를 제공합니다. |
| [관리자 감사 로그 내보내기](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | 관리자 감사 로그는 Exchange Online에서 생성, 업데이트 및 삭제와 같은 특정 관리 작업을 기록합니다. 로그의 결과는 XML로 내보내지며 관리자는 이 로그를 사용자 집합에게 보내기 위해 선택할 수 있습니다. |
| [사서함 단위 소송 보존 보고서 실행](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | 사서함에 대한 소송 보류 설정에 대한 변경 내용에 대한 세부 정보를 제공합니다. |
| [외부 관리자 감사 로그 보기 및 내보내기](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | 외부 관리자가 수행한 작업에 대한 세부 정보가 들어 있습니다. 이 항목에서는 실행된 cmdlet, 사용된 매개 변수 및 Exchange Online에서 개체를 만들거나 수정하거나 삭제하는 작업에 대한 정보를 제공합니다. |

## <a name="device-compliance-reports"></a>장치 준수 보고서

Microsoft 365용 기본 이동성 및 보안을 사용하여 구독에 연결된 모바일 장치를 관리하고 보호할 수 있습니다. 회사 전자 메일, 일정, 연락처 및 문서에 액세스하는 데 사용되는 모바일 장치는 직원들이 언제 어디서나 작업할 수 있도록 하는 데 중요한 역할을 합니다. 조직의 정보를 보호하는 것이 중요합니다. Microsoft 365용 기본 모바일 및 보안을 사용하여 장치 보안 정책 및 액세스 규칙을 설정할 수 있습니다. 분실하거나 도난당한 경우 Microsoft 365의 기본 이동성 및 보안을 사용하여 모바일 장치를 지울 수도 있습니다.

기본 모바일 및 보안 준수 보고서는 Microsoft 365 데이터에 액세스하는 모바일 장치를 보호하기 위해 조직에서 설정한 정책에 대한 개요를 제공합니다. 이 보고서를 통해 준수 상태, 보고된 위반, 차단된 장치 및 보안 정책의 결과로 지워진 장치 수를 필터링할 수 있습니다. 자세한 내용은 [Microsoft 365의 기본 이동성 및 보안 개요를 참조하세요.](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)

## <a name="data-loss-prevention"></a>데이터 손실 방지

DLP 정책은 조직에서 정보의 보안 및 흐름을 관리하는 데 도움이 됩니다. 콘텐츠에 대한 액세스를 차단하거나, 데이터를 암호화하거나, 응용 프로그램 내 DLP 정책 팁을 사용하여 사용자에게 정책 및 정책 위반을 알리는 정책을 설정할 수 있습니다. DLP 보고서는 정책 및 규칙 일치, 다시 규정 및 가긍성 수에 대한 정보를 제공합니다.

Microsoft 365 관리 센터를 사용하여 DLP 정책에서 검색된 메시지 수에 대한 정보를 볼 수 있습니다. DLP 보고서는 보내고 받은 메일에 대한 정책 및 규칙 일치에 대한 정보를 제공합니다. Exchange 관리 센터를 사용하여 지난 24시간 이내에 각 정책에 대한 일치 횟수, 다시 설정 및 가짓 긍정 수를 볼 수도 있습니다. Excel 보고서를 다운로드하는 경우 메시지를 보낸 사람, 특정 일, 트리거된 정책 일치 등의 세부 정보를 볼 수 있습니다. 자세한 내용은 DLP 정책 [검색에 대한 보고서 보기를 참조하세요.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>엔터프라이즈의 Yammer 감사

Yammer Enterprise는 관리자에게 Yammer 데이터 내보내기 [API를](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)통해 Yammer 네트워크에서 사용자 활동 데이터를 내보내거나 Yammer 네트워크 관리 페이지를 통해 수동으로 내보낼 수 있는 기능을 제공합니다. 로그 내보내기 권한은 로그의 네트워크 관리자로 Yammer. (모든 Microsoft 365 전역 관리자는 네트워크 Yammer 있습니다.)

다음 데이터를 내보낼 수 있습니다.

| 파일 이름 | 설명 |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | 네트워크의 모든 새 사용자, 보류 중인 사용자 및 일시 중단된 사용자 |
| Messages.csv | 네트워크의 모든 메시지 |
| Files.csv(메타데이터) | 파일 이름, 파일 API URL, 업로더 ID, 업로드한 메타데이터 등 |
| Files.csv(원본 파일) | 사용자가 파일로 업로드한 원본 파일의 zip Yammer |
| Topics.csv | 네트워크에서 만든 항목 |
| Pages.csv | 네트워크의 사용자가 만든 페이지(메모) |
| Admins.csv | 네트워크에서 확인된 모든 관리자 |
| Networks.csv | 모든 Yammer 외부 네트워크 |

Yammer 엔터프라이즈 데이터는 Microsoft 365 활동 보고서를 통해서도 사용할 수 있습니다. 또한 Yammer Microsoft 365 관리 활동 API를 통해 추가 로깅을 노출하고 Power BI를 사용하여 데이터를 추론하는 기능을 적극적으로 사용 중입니다. 이러한 기능에 대한 자세한 내용은 [Office](https://fasttrack.microsoft.com/roadmap?filters=yammer) 로드맵을 참조하세요.
