---
title: 데이터 폐기 Microsoft 365
description: 데이터 센터 디스크 드라이브 및 서버의 재생, 폐기 Microsoft 365 Microsoft 정책에 대한 개요입니다.
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
hideEdit: true
ms.openlocfilehash: bf7769852a41e8f78724c64e9a189ba7652c8f95a4cb71db1d5a7c3d286892e5
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288706"
---
# <a name="data-destruction-in-microsoft-365"></a>데이터 폐기 Microsoft 365

## <a name="physical-data-destruction"></a>물리적 데이터 폐기

Microsoft는 디스크 드라이브의 재생 및 폐기와 실패하거나 서버를 폐기하는 데 사용할 수 있는 데이터 처리 표준 정책을 제공합니다. 모든 Microsoft 365 디스크 드라이브를 다시 사용하기 전에 Microsoft는 National Institute of Standards and Technology Special Publication 800-88(NIST[SP 800-88 Guidelines for Media Sanitization)에](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)따라 물리적 소진 프로세스를 수행합니다. 모든 디스크 Microsoft 365 BitLocker 볼륨 수준 암호화를 사용하여 암호화하기 때문에 기술적으로 NIST SP 800-88 규격 삭제는 필요하지 않습니다. 그렇지만 Microsoft는 이 프로세스를 수행하고 있습니다.

데이터 센터에서 사용되는 실패한 Microsoft 365 ISO 프로세스를 통해 물리적으로 폐기 및 감사됩니다. 자산 유형은 적절한 폐기 방법을 결정합니다. 초기화할 수 없는 하드 드라이브의 경우 Microsoft는 파기 프로세스를 사용하여 미디어를 파기하고 정보 복구를 불가능하게 렌더링합니다. 예를 들어 디스크는 물리적으로 폐기되거나 폐기되거나 소진됩니다. Microsoft는 파기 기록을 모두 유지하며, 소멸된 서버 내에서 다시 사용되는 서버에서 유사한 소 Microsoft 365. 이러한 지침에는 전자적 및 물리적인 적정화가 모두 수반됩니다.

각 데이터 센터는 현장 물리적 소멸 프로세스를 사용하여 디스크를 폐기합니다. 디스크 폐기로 지정된 저장소 미디어에 대한 보안 보관은 데이터 센터의 각 영역에 있습니다. 각 보안 Bin 스테이션에는 비디오 모니터링 감시가 있습니다. 폐기 Bin 용량이 약 50%에 도달하면 사이트 서비스 팀은 물리적 보안 팀에 연락하여 제거를 조정합니다. 사이트 서비스 직원 및 보안 Office 안전한 폐기 저장소를 제거하고 지정된 보안 저장소 영역에 저장합니다. 폐기 중에 데이터 관련 장치 처리를 다루는 정책 및 절차는 컴퓨터의 폐기 승인 조건을 보장하는 절차를 포함하여 정기적으로 테스트됩니다.

데이터 폐기 프로세스에서 디스크는 NIST 800-88(가능한 경우)을 준수하는 방식으로 지워진 다음 산업 파기기에 배치되고 물리적으로 철거됩니다. Microsoft는 NIST SP 800-88 일관된 정리/삭제, 자산 소멸, 암호화, 정확한 인벤토리링, 추적 및 전송 중에 보유 체인 보호를 사용하여 데이터 센터에서 나가는 자산에 대한 책임은 유지 관리합니다. 이 프로세스는 닫힌 회로 TV를 통해 모니터링하며 완료 시 폐기 인증서가 발급됩니다.

Microsoft는 EPS(Extreme [Protocol Solutions)의](https://www.enterprisedataerasure.com/) 데이터 삭제 단위를 사용합니다. EPS 소프트웨어는 정리 및 제거/보안 지우기를 위한 NIST SP 800-88 요구 사항을 지원합니다. 정리 또는 폐기 전에 Microsoft 자산 관리자가 인벤토리를 생성합니다. 공급업체가 폐기에 사용되는 경우 공급업체는 폐기된 각 자산에 대한 파기 인증서를 제공합니다. 이 인증서는 자산 관리자가 검증합니다.

## <a name="virtual-data-destruction"></a>가상 데이터 폐기

Microsoft는 데이터 처리 정책 및 절차에 따라 서비스 테넌트 간에 데이터가 부적절하게 공유되거나 서비스에서 하드한 후에 액세스할 수 있는 가능성을 방지할 수 있습니다. 한 테넌트의 서비스에서 삭제된 데이터는 다른 서비스 테넌트에서 액세스할 수 없습니다. 이는 원본으로 사용할 수 있는 실제 저장소가 하나라도 다시 재배치된 경우에도 해당됩니다. 이는 가상 환경을 확장하는 데 사용되는 여러 가상화 및 조각화 기술, 각 서비스 테넌트 내의 응용 [](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)프로그램의 활성 삭제 동작(예: 페이지 비우기) 및 필요한 미디어 및 응용 프로그램 콘텐츠 암호화 프로세스의 결과입니다.