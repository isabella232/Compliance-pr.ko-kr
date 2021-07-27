---
title: Microsoft 365 SharePoint 온라인 데이터 Deletion
description: 삭제된 콘텐츠가 저장되는 위치와 SharePoint 기간 등 온라인에서 데이터 삭제가 작동하는 방식에 대해 자세히 알아보겠습니다.
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6968cc318a625676195460814a9e264dada8605e
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573866"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>SharePoint 온라인 데이터 Microsoft 365

SharePoint 온라인에서는 개체를 응용 프로그램 데이터베이스 내에 추상화 코드로 저장합니다. 사용자가 파일을 SharePoint Online에 업로드하면 해당 파일이 분해되어 응용 프로그램 코드로 변환되어 여러 데이터베이스의 여러 테이블에 저장됩니다. SharePoint Online에서는 고객이 업로드하는 모든 콘텐츠가 청크로 끊어지고 암호화되고(잠재적으로 여러 AES 256비트 키를 사용하여) 데이터 센터에 분산됩니다. 청크 및 암호화 프로세스에 대한 자세한 내용은 Microsoft 클라우드의 암호화를 [참조하세요.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

SharePoint Online에서 항목은 원래 위치에서 삭제한 시간부터 93일 동안 보존됩니다. 다른 사용자가 해당 사이트에서 삭제하거나 해당 삭제를 비우지 않는 한 전체 시간 동안 사이트 Recycle Bin에 유지됩니다. 이 경우 항목은 사이트 모음 Recycle Bin으로 이동하여 나머지 93일 동안 유지됩니다. 삭제된 항목을 복원하는 데 대한 자세한 내용은 사이트 모음의 휴지 SharePoint 복원 및 사이트 [모음](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) 휴지방에서 삭제된 항목 복원을 [참조하세요.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) 온라인에서 재활용 보관 보관 시간을 구성할 SharePoint 없습니다.

사이트 모음을 삭제하면 모음에 있는 사이트 계층 구조와 사이트 내의 모든 콘텐츠도 삭제됩니다.

- 문서 및 문서 라이브러리
- 목록 및 목록 데이터
- 사이트 구성 설정
- 사이트 또는 해당 하위 사이트와 관련된 역할 및 보안 정보
- 최상위 웹 사이트의 하위 사이트, 해당 콘텐츠 및 사용자 정보

사이트 모음을 실수로 삭제한 경우 전역 또는 SharePoint 관리 센터를 사용하여 사이트 모음을 복원할 SharePoint 있습니다.

삭제된 사이트 모음은 93일 동안 보존됩니다. 93 일이 지나면 목록, 라이브러리, 페이지, 모든 하위 사이트를 포함 한 사이트와 해당 콘텐츠 및 설정이 영구적으로 삭제 됩니다.

영구 삭제는 사용자가 사이트 모음의 삭제된 항목을 제거하거나, 보존 및 백업 기간이 만료되거나, [관리자가 Remove-SPODeletedSite cmdlet을](/powershell/module/sharepoint-online/remove-spodeletedsite)사용하여 사이트 모음을 영구적으로 삭제할 때 발생합니다. 사용자가 SharePoint Online에서 콘텐츠를 영구적으로 삭제하거나 삭제하면 삭제된 청크의 모든 암호화 키도 삭제됩니다. 이전에 삭제된 청크를 저장한 디스크의 블록은 사용되지 않은 것으로 표시되어 다시 사용할 수 있습니다.
