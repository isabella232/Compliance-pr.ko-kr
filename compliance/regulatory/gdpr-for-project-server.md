---
title: Project Server GDPR
description: 온-프레미스 Project Server에서 유럽 연합 일반 개인정보보호법(GDPR) 요구 사항을 해결하는 방법을 알아봅니다.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 092bbe9e7abe0329e822b011d41b5db96f33d169606945f5801bc36771a1944c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292945"
---
# <a name="gdpr-for-project-server"></a>Project Server GDPR

Project Server는 사용자 지정 스크립트를 사용하여 Project Web App에서 사용자 데이터를 내보내고 수정합니다. 기본 프로세스는 다음과 같습니다.

1.  팜에서 Project Web App 사이트를 찾습니다.

2.  사용자를 포함하는 각 사이트에서 프로젝트를 찾습니다.

3.  검토할 데이터 형식을 내보내고 검토합니다.

4.  필요에 따라 데이터를 수정합니다.

이러한 단계는 아래 문서에 자세히 설명되어 있습니다.

- [Project Server에서 사용자 데이터 내보내기](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Project Server에서 사용자 데이터 삭제](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Project Server는 SharePoint Server와 SharePoint ULS 및 사용 현황 데이터베이스에 대한 로그 이벤트를 기반으로 구축되었습니다. 자세한 내용은 [SharePoint Server에 대한 GDPR](gdpr-for-sharepoint-server.md)을 참조하세요.
