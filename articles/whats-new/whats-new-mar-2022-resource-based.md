---
title: 2022년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2022년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910914"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.30.0.99의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.25의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

일비는 이제 새롭고 새롭게 재구상된 현대적인 경비 작업 영역에서 지원됩니다. 일비를 사용하는 회사는 이 기능을 사용하여 사용자에게 일비 경비를 제출하고 상환하는 쉬운 방법을 제공할 수 있습니다. 자세한 내용은 [일비 경비](../expense/per-diem-expenses.md)를 참조하십시오.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 목록은 Project Operations 2022년 3월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| **엔터티 맵** | **업데이트된 버전** | **댓글** |
| --- | --- | --- |
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn\_projectvendorinvoicelines) | 1.0.0.3 | Dataverse의 공급업체 송장 라인 엔터티와 일치하도록 매핑이 업데이트되었습니다. <br>매핑 버전 1.0.0.4를 활성화하지 마십시오. 다음 월간 업데이트에서 Finance 환경 버전 10.0.26과 함께 사용할 수 있습니다. |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 시간 및 경비 | 2388011 | 일괄 승인 중에 시간 입력 제출자에게 거부 의견을 표시합니다. |
| 프로젝트 계획 및 추적 | 2495294 | **작업 세부 정보** 페이지에서는 프로젝트 세부 정보를 편집할 수 없어야 합니다. |
| 청구 및 가격 책정 | 2499605 | 견적 마일스톤에서 생성된 계약 마일스톤이 읽기 전용으로 잘못 표시됩니다. |
| 프로젝트 계획 및 추적 | 2506050 | 저장할 변경 사항이 없으면 작업 집합이 1시간 동안 보류 상태로 유지됩니다. 그런 다음 집합은 **실패** 로 잘못 표시되지만 즉시 완료되어야 합니다. |
| 청구 및 가격 책정 | 2507401 | 잘못된 캐싱으로 인해 기본 계약 단위가 프로젝트에 잘못 입력됩니다. |
| 청구 및 가격 책정 | 2541660 | 이중 쓰기의 **판매 주문 생성 유효성 검사** 는 프로젝트 기반 주문에만 사용해야 합니다. |
| 청구 및 가격 책정 | 2552745 | 분할 청구 규칙을 설정한 고객 간에 세금이 분할되지 않습니다. |
| 청구 및 가격 책정 | 2558859 | 가격 책정 차원을 설정할 때 오류 메시지가 개선되었습니다. |
| 청구 및 가격 책정 | 2558933 | **msdyn\_project** 가 가격 차원으로 추가되면 **프로젝트 견적에서 가져오기** 가 실패합니다. |
| 청구 및 가격 책정 | 2559101 | 프로젝트 매개 변수 삭제가 차단되지 않고 문제가 발생합니다. |
| 영업 기회 관리 | 2570390 | 이중 쓰기 플러그인은 견적, 주문 및 영업 기회에 대한 계정 유형이 정확하지 않은 경우에도 **고객** 이 되도록 강제합니다. |
| 청구 및 가격 책정 | 2586097 | 분할 청구 비용 실제 값은 프로젝트가 프로젝트 계약 내용에서 제거될 때 취소되지 않습니다. |
| 청구 및 가격 책정 | 2589619 | 직접 입력 자재에 대한 세금은 청구되지 않은 실제 판매액과 송장으로 전달됩니다. |
| 영업 기회 관리 | 2594015 | **Net60** 지불 조건이 있는 고객의 경우 견적을 낙찰로 마감할 수 없습니다. |
| 프로젝트 계획 및 추적 | 2595841 | Project for the Web에서 사용자는 새 리소스 요청을 만들 때 누락된 **msdyn\_actualstart** 에 대한 오류 메시지를 받습니다. |
| 시간 및 경비 | 2602511 | 시간 항목에 대한 **거부한 사람** 필드에 기명 사용자 대신 **시스템** 이 거부자로 표시됩니다. |
| 시간 및 경비 | 2602528 | 프로젝트 승인자는 승인자로 나열되지 않은 프로젝트의 시간을 승인할 수 있습니다. |
| 청구 및 가격 책정 | 2608550 | 수정 송장은 원본에 변경 사항이 없어도 확정할 수 있습니다. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | **카테고리 ID** 필드에서 Finance 및 Project Operations 간에 허용된 길이가 일치하지 않습니다. |
| 프로젝트 관리 및 회계 | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | **계정 송장 발행** 필드가 **손익** 으로 설정되고 **완료 비율** 원칙이 사용되는 경우 고정 가격 프로젝트를 제거할 수 없습니다. |
| 프로젝트 관리 및 회계 | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Project Operations 통합 분개장의 경비 라인에 대한 프로젝트 설정에서 잘못된 기본 판매세 그룹이 입력되었습니다. |
| 프로젝트 관리 및 회계 | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Project Operations과 통합 배포에서 프로젝트 송장 제안 헤더 차원을 편집할 수 없습니다. |
| 프로젝트 관리 및 회계 | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | 회사 간 공급업체 송장은 Dataverse와 통합되어서는 안 됩니다. |
| 프로젝트 관리 및 회계 | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | 고객 잔액 통화와 보고 통화가 일치하지 않습니다. |
| 프로젝트 관리 및 회계 | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | 고객이 모든 송장에 대해 보류 중인 경우에도 프로젝트 송장을 전기할 수 있습니다. |
| 프로젝트 관리 및 회계 | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | **헤더** 및 **라인** 보기가 있는 프로젝트 송장 제안서에는 **모든 라인 삭제** 버튼이 없습니다. |
| 프로젝트 관리 및 회계 | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | 공급업체 송장을 전기할 때 다음 오류가 발생합니다. "송장에 대한 회계 날짜는 관련 구매 주문과 동일한 회계 연도여야 합니다. 구매 발주 연말 프로세스를 실행하거나 날짜를 현재 회계 연도로 변경하십시오." |
| 이동 및 경비 | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | 여행 요청의 약정 비용이 릴리스된 후 프로젝트에 대한 약정 비용이 릴리스되지 않습니다. |
| 이동 및 경비 | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | 경비 보고서를 제출할 때 다음 오류가 발생합니다. "스택 추적: 회사가 존재하지 않습니다." |
| 이동 및 경비 | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | 프로젝트에서 **분개장 활동 필요** 매개변수가 선택되면 기본값 **프로젝트 ID** 가 지출 보고서에 입력되지 않습니다. |
| 이동 및 경비 | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | 리소스/비재고 시나리오에 대한 Project Operations에서 **사후 경비** 버튼이 올바르게 작동하지 않습니다. |
| 이동 및 경비 | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | 승객이 포함된 마일리지 경비 보고서의 경우 **마일당 요금** 에 문제가 있습니다. |
| 이동 및 경비 | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | **마일리지 등급** 경비 범주에서 서로 다른 두 가지 차량 유형을 사용하는 경우 직원의 경비 마일리지 비율이 올바르게 합산되지 않습니다. |
| 이동 및 경비 | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | 여행 요청 라인의 **프로젝트** 필드에 대한 조회는 프로젝트의 올바른 목록을 반환하지 않습니다. |
| 이동 및 경비 | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **검토 중인 마일리지** 는 경비 보고서에 대한 경고를 표시합니다. |
| 이동 및 경비 | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | 경비 OCR 서비스의 URL 문제로 영수증 OCR(광학 문자 인식) 서비스가 작동하지 않습니다. |
| 이동 및 경비 | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **반복 경비를 신속하게 항목화하는 기능** 기능이 활성화된 경우 경비 보고서의 항목화 라인에 있는 금액은 **항목화** 페이지가 열릴 때마다 금액이 변경됩니다. |
| 이동 및 경비 | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | 중간 목록에 두 명 이상의 승인자가 있는 경우 경비 보고서를 삭제할 수 없습니다. |

## <a name="removed-and-deprecated-features"></a>제거되었고 사용되지 않는 기능

[Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](removed-depreciated-features-project.md) 문서에서는 Dynamics 365 Project Operations의 제거되었거나 더 이상 사용되지 않는 기능을 설명합니다.

- 제거된 기능은 더 이상 제품에서 사용할 수 없습니다.
- 더 이상 사용되지 않는 기능은 현재 개발 중이 아니며 향후 업데이트에서 제거될 수 있습니다.

사용 중단 발표는 제품에서 기능이 제거되기 12개월 전에 [Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](removed-depreciated-features-project.md) 문서에 표시됩니다.

컴파일 시간에만 영향을 미치지만 샌드박스 및 프로덕션 환경과 바이너리 호환되는 주요 변경 사항의 경우 사용 중단 시간은 12개월 미만입니다. 일반적으로 이러한 변경 사항은 컴파일러에 대해 수행해야 하는 기능 업데이트입니다.
