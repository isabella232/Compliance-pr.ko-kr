---
title: Microsoft 클라우드 서비스의 감사 및 보고
description: Office 365, Microsoft 365 및 Service Assurance 내의 감사 및 보고 기능에 대한 개요입니다.
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
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120707"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Microsoft 클라우드 서비스의 감사 및 보고

Microsoft 클라우드 서비스에는 테넌트 내에서 사용자 및 관리 활동을 추적하는 데 사용할 수 있는 몇 가지 감사 및 보고 기능이 포함되어 있습니다. 예를 들어 Exchange Online 및 SharePoint Online 테넌트 구성 설정에 대한 변경 내용, 문서 및 기타 항목에 대한 사용자가 변경한 내용이 포함됩니다. Microsoft 클라우드 서비스에서 사용할 수 있는 감사 정보 및 보고서를 사용하여 사용자 환경을 보다 효과적으로 관리하고 위험을 완화하며 준수 의무를 이행할 수 있습니다.

## <a name="security--compliance-centers"></a>보안 & 준수 센터

[Microsoft 365 보안 &](https://protection.office.com)준수 센터, Microsoft [365](https://security.microsoft.com)보안 센터 및 [Microsoft 365](https://compliance.microsoft.com) 준수 센터는 조직의 데이터를 보호하기 위한 원스톱 포털로, 많은 감사 및 보고 기능을 포함합니다. 이러한 센터는 데이터 보호 또는 규정 준수 요구를 충족하고 사용자 및 관리자 활동을 감사하는 데 도움이 됩니다. 구독 관리자 계정을 사용하여 이러한 센터에 액세스할 수 있습니다.

이러한 센터에는 여러 기능에 액세스하기 위한 탐색 창이 포함되어 있습니다.

- **경고:** Cloud App Security를 사용하여 경고를 관리하고, 보안 관련 경고를 보고, 고급 경고를 [관리할 수 있습니다.](/cloud-app-security/what-is-cloud-app-security)
- **사용 권한:** 규정 준수 [](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) 관리자, eDiscovery 관리자 등의 권한을 조직의 사용자에게 할당하여 이러한 센터에서 작업을 수행할 수 있도록 합니다. 각 센터에서 대부분의 기능에 대한 사용 권한을 할당하지만 다른 사용 권한은 Exchange 관리 센터 및 SharePoint 관리 센터를 사용하여 구성해야 합니다.
- **위협 관리:** [Microsoft 365용 Basic Mobility and Security를](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)사용하여 장치 관리 정책을 [](/microsoft-365/compliance/data-loss-prevention-policies) 만들고 적용할 수 있으며, 조직의 DLP(데이터 손실 방지) 정책을 설정하여 전자 메일 필터링, 맬웨어 방지, DKIM(DomainKeys 식별 메일), 안전한 첨부 파일, 안전한 링크 및 OAuth 앱을 구성할 수 있습니다.
- **데이터 거버넌스:** 다른 시스템의 전자 메일 또는 SharePoint 데이터를 [Microsoft 365로](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)가져오고, [](/microsoft-365/compliance/retention-policies) [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)보관 사서함을 구성하고, 조직 내의 전자 메일 및 기타 콘텐츠에 대한 보존 정책을 설정할 수 있습니다.
- **검색 & 다음을 검색합니다.** Exchange Online [사서함,](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)그룹 및 공용 폴더, SharePoint Online 및 비즈니스용 [OneDrive에서](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) 작업을 빠르게 드릴다운할 수 있도록 콘텐츠 검색, 감사 [로그,](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)검지 및 eDiscovery 사례 관리 도구를 제공합니다.
- **보고서:** SharePoint Online, [](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) 비즈니스용 OneDrive, Exchange Online 및 Azure AD에 대한 보고서에 빠르게 액세스할 수 있습니다.
- **서비스 보증:** Microsoft가 Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune 및 기타 클라우드 서비스에 대한 글로벌 표준을 준수하는 방법에 대한 정보를 제공합니다. Microsoft 365의 타사 감사자에 의해 테스트 및 확인된 다양한 컨트롤에 대한 세부 정보를 제공하는 감사 컨트롤뿐만 아니라 타사 ISO, SOC 및 기타 감사 보고서에 대한 액세스도 포함됩니다.

## <a name="service-assurance"></a>Service Assurance

규제 대상 산업의 많은 조직은 광범위한 규정 준수 요구 사항을 준수해야 합니다. 자체 위험 평가를 수행하기 위해 고객은 종종 Microsoft 365가 데이터의 보안 및 개인 정보를 유지하는 방법에 대한 자세한 정보가 필요합니다. Microsoft는 클라우드 서비스에서 고객 데이터의 보안 및 개인 정보 보호를 보장하고 운영에 대한 투명한 보기와 독립적인 규정 준수 보고서 및 평가에 쉽게 액세스할 수 있도록 제공하여 고객 신뢰를 획득하기 위해 최선을 다하고 있습니다.

Service Assurance는 Microsoft가 Microsoft 365에서 고객 데이터의 보안, 개인 정보 보호 및 규정 준수를 유지하는 방법에 대한 운영 투명성 및 정보를 제공합니다. 여기에는 데이터 암호화, 데이터 탄력성, 보안 인시던트 관리 등의 Microsoft 365 항목에 대한 백서, FAQ 및 기타 자료 라이브러리와 함께 타사 감사 보고서가 포함됩니다. 고객은 이 정보를 사용하여 자체 규정 위험 평가를 수행할 수 있습니다. 규정 준수 담당자는 "Service Assurance 사용자" 역할을 할당하여 사용자에게 Service Assurance에 대한 액세스 권한을 부여할 수 있습니다. 테넌트 관리자는 독립 감사자와 같은 외부 사용자에게 [Microsoft](https://aka.ms/STP) STP(클라우드 서비스 신뢰 포털)를 통해 Service Assurance 대시보드의 정보에 대한 액세스 권한을 제공할 수도 있습니다.

## <a name="onedrive-for-business-admin-center"></a>비즈니스용 OneDrive 관리 센터

Microsoft OneDrive 관리 센터를 사용하면 조직의 비즈니스용 OneDrive 설정을 한 장소에서 쉽고 빠르게 관리할 수 있습니다. OneDrive 관리 센터를 사용하려면 해당 onedrive.com 액세스해야 합니다. 또한 조직의 전역 관리자 또는 SharePoint 관리자 역할이 있는 사용자 지정 관리자 되어야 합니다. 에서 비즈니스용 OneDrive 관리 센터에 [https://admin.onedrive.com](https://admin.onedrive.com/) 액세스합니다.

주요 기능에는 감사 로그 검색, DLP, 보존, eDiscovery 및 경고 작업과 같은 주요 시나리오에 대한 적절한 관리 센터 링크를 관리자에게 제공하는 준수 영역이 포함됩니다.

## <a name="related-links"></a>관련 링크

- [Microsoft 365 보고 기능](assurance-reporting-features.md)
- [Microsoft 365 엔지니어링에 대한 내부 로깅](assurance-internal-logging.md)
