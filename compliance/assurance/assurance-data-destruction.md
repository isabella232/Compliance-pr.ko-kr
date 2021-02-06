---
title: Microsoft 365의 데이터 폐기
description: Microsoft 365 데이터 센터 디스크 드라이브 및 서버의 재생, 폐기 또는 폐기에 대한 Microsoft 정책 개요
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
ms.openlocfilehash: d97c5f1be6bf09a772244aac14086171643af89e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120677"
---
# <a name="data-destruction-in-microsoft-365"></a>Microsoft 365의 데이터 폐기

## <a name="physical-data-destruction"></a>물리적 데이터 폐기

Microsoft는 디스크 드라이브의 재생 및 폐기 및 실패 또는 사용 중지를 다루는 데이터 처리 표준 정책을 제공합니다. Microsoft 365 디스크 드라이브를 다시 사용하기 전에 Microsoft는 National Institute of Standards and Technology Special Publication 800-88(NIST[SP 800-88 Guidelines for Media Sanitization)와](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)일관된 물리적 소실 프로세스를 수행합니다. Microsoft 365의 모든 디스크 드라이브는 BitLocker 볼륨 수준 암호화를 사용하여 암호화하기 때문에 기술적으로는 NIST SP 800-88 규격 삭제가 필요하지 않습니다. 그러나 Microsoft는 이 프로세스를 수행합니다.

Microsoft 365 데이터 센터에서 사용되는 실패한 디스크는 ISO 프로세스를 통해 물리적으로 파기 및 감사됩니다. 자산 유형에 따라 적절한 폐기 수단이 결정됩니다. 지워질 수 없는 하드 드라이브의 경우 Microsoft는 파기 프로세스를 사용하여 미디어를 폐기하고 정보 복구를 불가능하게 합니다. 예를 들어 디스크는 물리적으로 파기되거나, 불이 나거나, 소진됩니다. Microsoft는 파기에 대한 모든 기록을 보존하고 Microsoft 365 내에서 다시 사용되는 서버에서 유사한 소멸 프로세스를 수행하고 있습니다. 이러한 지침에는 전자 및 물리적인 모든 것이 있습니다.

각 데이터 센터는 현장 물리적 소멸 프로세스를 사용하여 디스크를 폐기합니다. 디스크 폐기로 지정된 저장소 미디어에 대한 보안 보관은 데이터 센터의 각 영역에 있습니다. 각 보안 Bin 스테이션에는 비디오 모니터링 감시가 있습니다. 폐기 Bin 용량이 약 50%에 도달하면 사이트 서비스 팀은 물리적 보안 팀에 연락하여 제거를 조정합니다. 사이트 서비스 직원과 보안 사무소는 보안 폐기 저장소를 제거하고 지정된 보안 저장소 영역에 저장합니다. 폐기 중에 데이터 관련 장치 처리를 다루는 정책 및 절차는 기계의 파기 승인 조건을 보장하는 절차를 포함하여 정기적으로 테스트됩니다.

데이터 폐기 프로세스에서 디스크는 NIST 800-88(가능한 경우)을 준수하는 방식으로 삭제된 다음 산업 파기기에 배치되고 물리적으로 철거됩니다. Microsoft는 전송 중에 NIST SP 800-88의 일관된 정리/삭제, 자산 소멸, 암호화, 정확한 인벤토리링, 추적 및 보호를 사용하여 데이터 센터에서 나가는 자산에 대한 책임은 유지 관리합니다. 이 프로세스는 닫힌 회로 TV를 통해 모니터링하며 완료 시 폐기 인증서가 발급됩니다.

Microsoft는 EPS(Extreme Protocol Solutions)의 데이터 [지우기](https://www.enterprisedataerasure.com/) 단위를 사용합니다. EPS 소프트웨어는 정리 및 제거/보안 삭제에 대한 NIST SP 800-88 요구 사항을 지원합니다. 정리 또는 폐기 전에 Microsoft 자산 관리자가 인벤토리를 생성합니다. 공급업체를 파기하는 데 사용되는 경우 공급업체는 폐기된 각 자산에 대한 파기 인증서를 제공합니다. 이 인증서는 자산 관리자가 검증합니다.

## <a name="virtual-data-destruction"></a>가상 데이터 폐기

Microsoft는 서비스 테넌트 간에 데이터가 부적절하게 공유되거나 서비스에서 하드한 후 액세스할 수 있는 가능성을 보호하기 위해 데이터의 효과적인 가상 파기 문제를 처리하는 데이터 처리 정책 및 절차를 제공합니다. 한 테넌트의 서비스에서 삭제된 데이터는 다른 서비스 테넌트가 액세스할 수 없습니다. 이는 원본으로 사용할 수 있는 실제 저장소가 하나라도 다시 재배치된 경우에도 해당됩니다. 이는 가상 환경을 확장하는 데 사용되는 여러 가상화 및 조각화 기술, 각 서비스 테넌트 내의 응용 [](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)프로그램의 활성 삭제 동작(예: 페이지 비우기) 및 필요한 미디어 및 응용 프로그램 콘텐츠 암호화 프로세스의 복합적인 결과입니다.