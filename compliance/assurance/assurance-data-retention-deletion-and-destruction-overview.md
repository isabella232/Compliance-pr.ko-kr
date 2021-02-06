---
title: Microsoft 365의 데이터 보존, 삭제 및 폐기
description: 데이터 보존, 삭제 및 폐기와 관련하여 Microsoft 365에 대한 Microsoft 정책의 개요입니다.
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 025e2c422c05dbffdf5a510f93809beaed3fe09d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120657"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Microsoft 365의 데이터 보존, 삭제 및 폐기

Microsoft는 Microsoft 365에 대한 데이터 처리 표준 정책을 사용하여 고객 데이터가 지우고 나면 보존되는 기간을 지정합니다. 일반적으로 고객 데이터가 삭제되는 두 가지 시나리오가 있습니다.

- **활성 삭제:** 테넌트에 활성 구독이 있으며 사용자 또는 관리자가 데이터를 삭제하거나 관리자가 사용자를 삭제합니다.
- **수동 Deletion:** 테넌트 구독이 종료됩니다.

## <a name="data-retention"></a>데이터 보존

이러한 각 삭제 시나리오에 대해 다음 표에는 데이터 범주 및 분류별로 최대 데이터 보존 기간이 표시됩니다.

| 데이터 범주 | 데이터 분류 | 설명 | 예제 | 보존 기간 |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| 고객 데이터 | 고객 콘텐츠| 관리자 및 사용자가 직접 제공/만든 콘텐츠 <br><br> Microsoft 365의 서비스를 사용할 때 Microsoft 데이터 센터에 만들어 저장되는 모든 텍스트, 소리, 비디오, 이미지 파일 및 소프트웨어가 포함됩니다. | 사용자가 데이터를 작성하도록 허용하는 가장 일반적으로 사용되는 Microsoft 365 응용 프로그램의 예로는 Word, Excel, PowerPoint, Outlook 및 OneNote가 있습니다. <br><br> 고객 콘텐츠에는 고객 소유/제공 암호(암호, 인증서, 암호화 키, 저장소 키)도 포함됩니다. | **활성 지우기 시나리오:** 30일 이상 <br><br> **수동 지우기 시나리오:** 180일 이상 |
| 고객 데이터 | 최종 사용자 식별 정보(EUII) | Microsoft 서비스의 사용자를 식별하는 데 사용할 수 있는 데이터입니다. EUII에 고객 콘텐츠가 포함되지 않습니다. | 사용자 이름 또는 표시 이름(DOMAIN\UserName) <br><br> 사용자 계정 이름(name@domain) <br><br>  사용자별 IP 주소 | **활성 지우기 시나리오:** 180일 이상(테넌트 관리자 작업만 해당) <br><br> **수동 지우기 시나리오:** 180일 이상 |
| 개인 데이터 <br> (고객 데이터에 포함되지 않은 데이터) | 최종 사용자 가명 식별자(EUPI) | Microsoft에서 만든 식별자(Microsoft 서비스 사용자)입니다. 매핑 테이블과 같은 다른 정보와 결합된 EUPI는 최종 사용자를 식별합니다. <br><br> EUPI는 고객이 업로드하거나 만든 정보를 포함하지 않습니다. | 사용자 GUID, PUID 또는 SID <br><br> 세션 ID | **활성 지우기 시나리오:** 30일 이상 <br><br> **수동 지우기 시나리오:** 180일 이상 |

## <a name="subscription-retention"></a>구독 보존

활성 구독 기간에 구독자는 Microsoft 365에 저장된 고객 데이터를 액세스, 추출 또는 삭제할 수 있습니다. 유료 구독이 종료되거나 종료되면 Microsoft는 구독자가 데이터를 추출할 수 있도록 90일 동안 제한된 기능 계정으로 Microsoft 365에 저장된 고객 데이터를 보존합니다. 90일의 보존 기간이 끝나면 Microsoft는 계정을 사용하지 않도록 설정하고 고객 데이터를 삭제합니다. Microsoft 365 구독이 만료되거나 종료된 후 180일이 지난 후 Microsoft는 계정을 사용하지 않도록 설정하고 계정에서 모든 고객 데이터를 삭제합니다. 모든 데이터의 최대 보존 기간이 경과하면 데이터는 상업적으로 읽을 수 없는 렌더링됩니다.

무료 평가판의 경우 계정이 대부분의 국가 및 지역에서 30일 동안 유예 상태가 됩니다. 이 유예 기간 동안 Microsoft 365를 구매할 수 있습니다. Microsoft 365를 구입하지 않기로 결정한 경우 평가판을 취소하거나 유예 기간이 만료되고 평가판 계정 정보와 데이터가 삭제되도록 놔둘 수 있습니다.

## <a name="expedited-deletion"></a>Expedited Deletion

구독의 경우 구독자는 Microsoft 지원에 문의하여 프로비전을 취소하는 지원을 요청할 수 있습니다. 이 프로세스에서는 관리자가 Microsoft에서 제공하는 잠금 코드를 입력하고 3일 후에 모든 사용자 데이터가 삭제됩니다. 여기에는 SharePoint Online 및 Exchange Online의 데이터가 보류되거나 비활성 사서함에 저장됩니다.

프로비전 취소에 대한 자세한 내용은 구독 취소를 [참조하세요.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>관련 링크

- [데이터 폐기](assurance-data-destruction.md)
- [Office 365의 불변성](assurance-data-immutability.md)
- [Exchange Online 데이터 삭제](assurance-exchange-online-data-deletion.md)
- [SharePoint Online 데이터 삭제](assurance-sharepoint-online-data-deletion.md)
