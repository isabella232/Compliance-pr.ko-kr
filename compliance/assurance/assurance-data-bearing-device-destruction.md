---
title: 데이터 포함 장치 폐기
description: 이 문서에서는 Microsoft 데이터 센터에 대한 데이터 관련 장치 폐기 프로세스에 대한 개요를 확인할 수 있습니다.
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160357"
---
# <a name="data-bearing-device-destruction"></a>데이터 포함 장치 폐기

## <a name="data-destruction-overview"></a>데이터 폐기 개요

Microsoft는 Microsoft 데이터 센터 내에서 DBD를 처리 및 관리하기 위한 DBD(데이터 관련 장치) 지침, 정책, 보안 요구 사항 및 절차를 제공합니다.

DBD는 고객 또는 독점 Microsoft 데이터를 저장할 수 있는 모든 저장 장치입니다.

- HDD(하드 디스크 드라이브)
- SSD(Solid-State Drive)
- USB 드라이브
- IO 가속기 카드
- SD/컴팩트 플래시 카드
- HSM 카드
- PCIe SSD 카드
- NVDIMM(비휘발성 이중 인라인 메모리 모듈)

Microsoft 데이터 센터 내에서 사용되는 실패한 DBD는 데이터 센터 캠퍼스 내에서 감사 및 폐기됩니다. 서비스에서 사용 중지된 자산은 해당 보안/개인 정보 요구 사항 및 자산 분류에 따라 적용 가능한 규칙, 법률 및 규정에 따라 폐기된 것으로 평가됩니다.

Microsoft는 데이터를 포함하는 DBD 및 자산에 대해 다음 세 가지 범주의 데이터 소각을 사용 합니다.

- **Clear**: 단순한 비공용 데이터 복구 기술에 대한 보호를 위해 모든 사용자 주소가 가능한 저장소 위치에서 데이터를 소진하는 데 도움이 되는 논리적 기술과 관련이 있습니다. 이러한 기술은 새 값으로 다시 쓰거나 메뉴 옵션을 사용하여 장치를 공장 상태로 다시 설정하는 방법(다시 쓰기가 지원되지 않는 경우)처럼 일반적으로 표준 읽기 및 쓰기 명령을 통해 저장소 장치에 적용됩니다.
- **제거:** 최첨단 실험실 기술을 사용하여 대상 데이터 복구를 비현실적으로 렌더링하는 물리적 또는 논리적 기술과 관련이 있습니다.
- **삭제:** 최첨단 실험실 기술을 사용하여 대상 데이터 복구를 지원하지 않습니다. 그 결과로 미디어를 데이터 저장에 사용할 수 없습니다.

삭제 및 삭제는 보안 그룹에서 승인한 도구 및 프로세스를 사용하여 수행됩니다. 레코드는 자산의 삭제 및 폐기에 보관됩니다. 클리어를 완료하지 못하는 장치는 성공적으로 제거되거나(자기 미디어에만 해당), 멀티 핀 펀치(SSD와 같은 치핑된 기반 보드용) 또는 폐기됩니다.

## <a name="clear"></a>지우기

사용 중지된 자산이 평가된 후 액세스할 수 없는 것으로 생각되면 승인된 데이터 삭제 솔루션에 의해 삭제됩니다. Microsoft 데이터 센터는 NIST SP-800-88 명확한 지침을 사용 합니다.

## <a name="purge"></a>제거

사이트 구성 및 장치 가용성에 따라 일부 장치는 폐기 전에 제거됩니다. 제거 장치에는 자기 미디어에 대한 NSA 승인 디거저와 솔리드 스테이트 미디어용 멀티 핀 펀치 장치가 포함됩니다. Microsoft 데이터 센터는 NIST SP-800-88 제거 지침을 사용 합니다.

## <a name="destroy"></a>폐기

사용 중지된 자산이 평가 및 접근성 있는 것으로 확인되면 NIST SP-800-88 지침을 충족하는 승인된 표준 운영 절차에 따라 해당 자산은 부재 중이 됩니다. 이러한 DBD는 최종적으로 관리 체인을 유지 관리하기 위해 물리적 및 논리적으로 추적됩니다.

각 Microsoft 데이터 센터는 현장 프로세스를 사용하여 실패 및 사용 중지된 DBD를 소진 및 처리합니다. 이 프로세스 동안 Microsoft 직원은 폐기 프로세스 전체에서 유지 관리 체인을 보장합니다.

## <a name="resources"></a>리소스

- [NIST 특수 발행물 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
