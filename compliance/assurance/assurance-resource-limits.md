---
title: Microsoft 365 리소스 제한
description: 이 문서에서는 응용 프로그램 내에서 다양한 응용 프로그램의 리소스 제한에 대한 정보를 Microsoft 365.
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
ms.openlocfilehash: 764259e22b23ecc7cea363283fc313a94875a2d1
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481790"
---
# <a name="service-resource-limits"></a>서비스 리소스 제한 사항

리소스 제한은 할당량(제한) 및 제한을 사용하여 적용됩니다. Azure Active Directory(Azure AD) 및 개별 Microsoft 365 둘 다를 사용 합니다. 제한은 서비스별 제한으로, 시간이 지날 때 새로운 기능이 추가될 때 변경됩니다. 다양한 서비스의 현재 제한에 대한 자세한 내용은 다음 항목을 참조하십시오.

- [Azure AD 서비스 제한 사항](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online 제한](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint 온라인 소프트웨어 경계 및 제한](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [비즈니스용 Skype 제한](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST API 및 속도 제한](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway의 파일 크기 제한](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

이러한 제한 외에도 Azure AD 및 서비스 전체에서 여러 제한 메커니즘이 Microsoft 365. Microsoft 데이터 센터의 네트워크 리소스가 서비스를 사용하는 광범위한 고객 집합에 최적화되어 있는 경우 서비스 내의 스로틀은 특히 중요합니다. 다음과 같은 스로틀 메커니즘이 있습니다.

- Azure AD 및 Microsoft 365 기능은 단일 사용자가 수행할 수 있는 트랜잭션 또는 동시 호출(스크립트 또는 코드로)의 수를 제한하는 사용자 수준 제한 기능을 제공합니다.
- 기본 PowerShell 스로틀 정책은 테넌트 만들기 시 각 테넌트에 할당됩니다. 이러한 설정은 단일 관리자가 열 수 있는 최대 동시 PowerShell 세션 수와 같은 다른 항목에 영향을 미치게 됩니다.
- 각 Exchange Online EWS 클라이언트 작업에 맞게 조정된 기본 Exchange 웹 서비스(EWS) 정책과 모든 Outlook 클라이언트에 적용되는 제한이 있습니다.
