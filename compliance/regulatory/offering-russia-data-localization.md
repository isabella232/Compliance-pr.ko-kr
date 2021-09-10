---
title: 러시아 개인 데이터 지역화 요구 사항
description: 러시아 시민의 개인 데이터 기록, 시스템화, 누적, 저장, 설명 및 추출을 러시아에 있는 Microsoft 서비스 및 데이터베이스에서 수집하는 방법을 알아보습니다.
keywords: Microsoft 365, 규정 준수, 제품
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 093ec578cd83dc6c52485101d232d9ccff88489e
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948401"
---
# <a name="russian-personal-data-localization-requirements"></a>러시아 개인 데이터 지역화 요구 사항

2015년 9월 1일 현재 개인 데이터 운영자로 간주되는 조직은 개인 데이터를 수집할 때 러시아 시민의 개인 데이터 기록, 시스템화, 누적, 저장, 설명(업데이트, 변경) 및 추출이 러시아에 있는 데이터베이스를 통해 수행되도록 해야 합니다('개인 데이터 지역화 요구 사항'). <sup>1</sup>

Microsoft 서비스(교육 기관을 포함하지만 이에 국한되지는 않는)(Microsoft Azure, Microsoft 365, Dynamics 365 및 Power Platform과 같은 개인 데이터 처리를 사용하도록 설정하는 조직(예: '고객'으로 지칭)은 러시아 외부의 데이터 처리 센터에서 제공됩니다(자세한 내용은 [Microsoft 보안](https://www.microsoft.com/trust-center)센터 방문).

고객 정보 시스템에서 처리한 정보의 유형 및 콘텐츠(예: Microsoft 클라우드 제품을 사용하는 시스템 포함)를 개인 데이터 정보 시스템('PDIS', 'ISPD')으로 생각할 수 있습니다. 고객이 처리된 정보의 아키텍처 및 Microsoft 서비스 통해 PDIS로 한정하는 시스템에서 PDIS를 사용하게 되는 경우 Microsoft는 아래에 지정된 사용 가능한 솔루션 중에서 특히 고객에게 고려할 수 있는 솔루션을 초대합니다. 고객에게 제공되는 모든 시나리오를 표준 비즈니스 제공에 대한 추가 옵션으로 사용할 수 있습니다.

이는 규정 준수를 담당하는 PDIS의 개인 데이터 운영자인 고객으로, 개인 데이터 지역화에 대한 해당 법적 요구 사항을 분석하고 평가하고 자체 재량에 따라 PDIS의 개인 데이터 처리가 러시아 개인 데이터 법률을 준수하도록 보장하는 충분한 조치를 결정해야 합니다. <sup>2</sup>

## <a name="subscribing-to-microsoft-services"></a>Microsoft 서비스

### <a name="microsoft-id-management"></a>Microsoft ID 관리

Microsoft는 고객을 초대하여 고객 지원에 대한 Microsoft 서비스. Microsoft Azure( Microsoft 365, Dynamics 365 및 Power Platform)는 CSP(Microsoft 클라우드 솔루션 공급자) 파트너를 통해 제공합니다. 자세한 내용은 이 [CSP 파트너 목록을 참조하세요.](https://pinpoint.microsoft.com/search?type=services&campaign=691)

### <a name="managing-user-identity-and-access-for-microsoft-services"></a>사용자 ID 및 액세스 관리 Microsoft 서비스

Microsoft 서비스, Microsoft Azure, Microsoft 365 dynamics 365 및 Power Platform과 같은 Microsoft Azure, Dynamics 365 및 Power Platform의 경우 사용자 확인 및 액세스 관리는 [Azure Active Directory(Azure Active Directory)를](https://azure.microsoft.com/services/active-directory/)통해 수행됩니다. Microsoft 고객이 Microsoft 클라우드 서비스(예: WINDOWS SERVER ACTIVE DIRECTORY(Windows Server Active Directory) 또는 기타 ID 관리 시스템)에 로컬 ID 관리 시스템을 사용하는 경우 고객은 Azure AD 서비스를 통해 이러한 시스템을 Azure Active Directory(Azure Active Directory)와 신속히 통합할 수 커넥트. 자세한 내용은 Azure AD 서비스 를 [커넥트.](/azure/active-directory/cloud-provisioning/) Microsoft 고객은 사용자를 관리하고 로컬 ID 시스템을 Azure AD와 통합하기 위해 타사 공급업체의 응용 프로그램 및 솔루션을 사용할 수도 있습니다.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Microsoft 준수 관리자를 사용하여 위험 평가

[Microsoft 준수 관리자](/microsoft-365/compliance/compliance-manager)는 조직의 준수 입장을 이해하고 위험을 줄이기 위한 조치를 취하도록 돕는 [Microsoft 365 규정 준수 센터](/microsoft-365/compliance/microsoft-365-compliance-center)의 기능입니다. 준수 관리자는 이 규제에 대한 평가를 빌드하기 위한 프리미엄 서식 파일을 제공합니다. 준수 관리자의 **평가 서식 파일** 페이지에서 서식 파일을 찾습니다. [준수 관리자의 평가 빌드](/microsoft-365/compliance/compliance-manager-assessments) 방법에 대해 알아봅니다.

## <a name="questions-and-support"></a>질문 및 지원

기술 및 청구 관련 질문은 아래 Microsoft 지원 리소스를 참조하세요. 추가 질문이나 설명은 Microsoft 개인 정보 팀에 [문의하세요.](https://support.microsoft.com/gp/privacy-page)

### <a name="microsoft-azure"></a>Microsoft Azure

- **웹** 사이트 : [Microsoft Azure 지원](https://aka.ms/GetAzureSupport)
- **무료:** 8 800 200 8001
- **로컬 통화:** 495 916 7171
- **온라인 지원:** [Azure Portal을](https://portal.azure.com) 통해 쿼리 제출

### <a name="microsoft-365"></a>Microsoft 365

- **무료:** 8 10 800 2548 1044
- **로컬 통화:** 499 922 8623
- **온라인 지원:** 관리 센터를 통해 쿼리 [제출](https://portal.office.com/)

### <a name="dynamics-365"></a>Dynamics 365

- **무료:** 8 10 800 2548 1044
- **로컬 통화:** 499 922 8623
- **온라인 지원:** [Dynamics](https://dynamics.microsoft.com/support/) 지원 포털을 통해 쿼리 제출

### <a name="power-platform"></a>Power Platform

- **무료:** 8 10 800 2548 1044
- **로컬 통화:** 499 922 8623
- **온라인 지원:** [Power Platform](/power-platform/admin/get-help-support) 지원을 통해 쿼리 제출

> [!NOTE]
> <sup>1</sup> 연방법 아니요. 242-FZ(2014년 12.31.2014년 12월 31일) '정보 및 통신 네트워크의 개인 데이터 처리 절차를 명확히 하는 데 관한 러시아 페더링 의 특정 입법 법률에 개정안을 입력합니다.' 날짜가 2014년 7월 21일입니다. <br>
> <sup>2</sup> 연방법 아니요. 152-FZ on Personal data as of 07.27. 2006<br>
