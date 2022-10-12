---
title: 2022년 9월의 새로운 기능 - Project Operations Lite 배포
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations Lite 배포의 2022년 9월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621287"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022년 9월의 새로운 기능 - Project Operations Lite 배포

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.46.0.60의 Project Operations

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

| 기능 영역 | 기능 이름 | 자세한 정보 |
| --- | --- | --- |
| 영업 기회 관리 | **견적의 수정 및 활성화**<br>Project Operations는 영업 프로세스를 완벽하게 지원합니다. 프로젝트 견적을 활성화하여 견적이 읽기 전용이고 검토 중인 상태를 나타낼 수 있습니다. 활성화된 견적을 수정하여 개정 번호가 증가된 새 견적을 생성할 수 있습니다. 활성화된 프로젝트 견적 또는 견적 개정은 성공 또는 실패로 종료될 수 있습니다. | [프로젝트 견적 활성화 및 수정](/dynamics365/project-operations/sales/activation-and-revision) |
| 청구 및 가격 책정 | **표준 시간대에 구애 받지 않는 가격 기본값 설정**<br>Project Operations는 모든 프로젝트 실제에 대한 표준 시간대에 구애 받지 않는 날짜 개념을 도입했습니다. 새로운 필드인 **거래 날짜** 는 이제 분개장 항목과 실제에서 사용할 수 있으며 거래가 발생한 날짜를 저장하는 데 사용되지만 해당 날짜를 협정 세계시로 변환하지 않습니다. 이 날짜는 가격 기본값 설정 및 송장 생성과 같은 다운스트림 프로세스에 사용됩니다. | <p>[프로젝트 기반 추정 및 실제 원가율 결정](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[프로젝트 기반 추정 및 실제에 대한 판매 가격 결정](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| 청구 및 가격 책정 | **Project Operations에서 가격 조정 적용 날짜 재정의**<br>가격 조정 적용 날짜는 가격표의 특정 가격을 무시하거나 변경할 수 있는 방법을 제공합니다. | [가격 조정 적용 날짜](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 시간 및 경비 | **전역 승인자**<br>이 기능을 사용하면 프로젝트 또는 프로젝트의 팀 구성원 상태에 관계없이 ISV(독립 소프트웨어 공급업체) 및 중앙 집중식 승인이 가능합니다. | [보안 및 승인](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2754422 | 프로젝트가 Dataverse에 복사될 때 재료 및 비용 견적은 Dynamics 365 Finance로 흐르지 않습니다. |
| 시간 및 경비 | 2787409 | 유효하지 않은 승인자는 비프로젝트 시간 입력을 승인할 수 있습니다. |
| 영업 기회 관리 | 2788907 | 플래그가 포함된 주문 라인의 고유성 검증에 대한 오류 메시지가 업데이트되었습니다. |
| 시간 및 경비 | 2842253 | 시간 승인을 위한 Null 예외 처리. |
| 청구 및 가격 책정 | 2844181 | 상관 관계 ID를 가져오지 못하면 송장 생성이 차단됩니다. |
| 청구 및 가격 책정 | 2876628 | QLD, CLD - 추정 가격표 해결은 가격표의 기존 날짜 범위 필드를 사용해야 합니다. |
| 하도급 계약 | 2893222 | 하도급 계약 내용에 대해 역할이 지정되지 않은 경우 모든 역할에 대해 팀 구성원에서 해당 내용을 선택할 수 있어야 합니다. |
