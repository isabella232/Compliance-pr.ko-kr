---
title: 온-프레미스 파일 공유 GDPR
description: 온-프레미스 Windows Server 파일 공유에서 GDPR(일반 데이터 보호 규정) 요구 사항을 해결하는 방법을 알아봅니다.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 9c281b6096512f65f20286948addc32127278b98
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948490"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a>온-프레미스 Windows Server 파일 공유

파일 공유에 권장되는 기본 방법입니다.

-   Azure Information Protection을 사용하여 중요한 데이터를 레이블 지정합니다.

-   Azure Information Protection 스캐너를 사용하여 데이터를 찾습니다.

파일 공유에 권장되는 방식에는 이러한 단계가 포함됩니다.

1.  **Azure Information Protection 스캐너를 설치하고 구성합니다.**

    -   사용할 중요한 데이터 형식을 결정합니다.

    -   사용할 로컬 폴더 및 네트워크 공유를 지정합니다.

2.  **검색 주기를 완료합니다.**

    -   검색 모드에서 스캐너를 실행하고 검색 결과의 유효성을 검사합니다.

    -   필요에 따라 조건 및 중요한 정보 유형을 최적화합니다.

    -   레이블 자동 적용의 예상된 영향을 평가합니다.

3.  **Azure Information Protection 스캐너를 실행하여 적격 문서에 레이블을 적용합니다**.

4.  **보호하려면:**

    -   Exchange 데이터 손실 방지 규칙을 구성하여 원하는 레이블로 문서를 보호합니다.

    -   권한을 사용하여 파일에 액세스할 수 있는 사람을 제한해야 합니다.

5.  **모니터링하려면 Windows Server 로그를 SIEM 도구와 통합합니다.**

    -   데이터 주체 요청을 위한 개인 데이터를 찾으려면 Azure Information Protection 스캐너를 사용합니다. SharePoint Server 검색을 구성하여 파일 공유를 크롤링할 수도 있습니다.

Azure Information Protection 스캐너를 사용하여 개인 데이터를 찾고 레이블 지정하는 방법에 대한 자세한 내용은 [AIP 스캐너 배포]](/azure/information-protection/deploy-aip-scanner)를 참조하세요.

조건을 위한 스캐너 구성 및 Office 365 DLP(데이터 손실 방지) 중요한 정보 유형의 사용에 대한 자세한 내용은 [Azure Information Protection의 자동 및 권장 분류를 위한 조건을 구성하는 방법](/information-protection/deploy-use/configure-policy-classification)을 참조하세요. 새 Office 365 중요한 정보 유형은 스캐너에서 즉시 사용할 수 없으며 사용자 지정 중요한 정보 유형은 스캐너에서 사용할 수 없습니다.
