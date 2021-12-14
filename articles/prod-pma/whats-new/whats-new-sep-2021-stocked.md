---
title: 2021년 9월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 재고/생산 기반 시나리오에 대한 Project Operations의 2021년 9월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815851"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>2021년 9월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 재고/생산 기반 시나리오에 대한 Project Operations_

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.21의 프로젝트 관리 및 회계
 
## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
|---|---|---|
| 프로젝트 관리 및 회계 | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | 구매 관리자 역할에 하나의 법인에 대한 액세스 권한이 부여되면 모든 법인의 모든 프로젝트에도 액세스할 수 있습니다. |
| 프로젝트 관리 및 회계 | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | 원래 프로젝트 송장에 대해 대변 메모가 정산되는 동안 부가가치세(VAT) 반올림 문제가 발생합니다. |
| 프로젝트 관리 및 회계 | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | 예산 확인을 위해 대체 프로젝트 예산을 사용합니다. |
| 프로젝트 관리 및 회계 | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | **판매 가격 시간** 가격 그룹은 프로젝트 견적에 대한 작업 분할 구조에서 계산되지 않습니다. |
| 프로젝트 관리 및 회계 | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | **견적 계산을 위해 프로젝트 계약 통화 활성화** 기능이 활성화되면 견적 제거가 실패합니다. |
| 프로젝트 관리 및 회계 | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | 프로젝트 경비 분개장의 판매세 그룹에 사용세가 사용되면 판매가 금액에 수량별 판매세 인수분해가 추가됩니다. |
| 프로젝트 관리 및 회계 | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | 구매 주문 송장에 공급업체 유지 및 선불이 적용될 때 마지막 지불에 대한 조건부 세금이 올바르게 계산되지 않았습니다. |
| 프로젝트 관리 및 회계 | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | 조정 추적은 기초 잔액 분개장에 대해 작동하지 않습니다. |
| 프로젝트 관리 및 회계 | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **기간별 프로젝트 예산 수정 할당** 이 모든 예산 기간에 걸쳐 분할됩니다. 할당이 제출되면 레코드가 지워지지 않습니다. |
| 프로젝트 관리 및 회계 | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | 총계정원장에 대한 WIP(진행 중인 작업) 전기에 잘못된 금액이 있습니다. |
| 프로젝트 관리 및 회계 | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | 프로젝트 시간 분개장 승인이 작동하지 않습니다. |
| 프로젝트 관리 및 회계 | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | 펀딩 한도가 표시되지 않은 경우 프로젝트 조정 판매 가격이 간접 비용으로 업데이트되지 않습니다. |
| 프로젝트 관리 및 회계 | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | 판매 테이블 헤더에 송장이 발행되고 기존 라인에 대한 지원 구매 발주가 완료되면 품목 요구 사항을 생성할 수 없습니다. |
| 프로젝트 관리 및 회계 | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | 다른 프로젝트에 대한 마일스톤이 있는 청구 규칙의 보존 금액은 마일스톤에 대해 선택된 해당 프로젝트 ID에 게시되지 않습니다. 대신 첫 번째 프로젝트와 함께 게시됩니다. |
| 프로젝트 관리 및 회계 | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | 송장 제안에서 **재무 차원 집합** 을 선택할 때 다음 오류가 발생합니다. "'Dynamics.AX.Application.FormIntControl' 유형의 개체를 'Dynamics.AX.Application.FormStringControl' 유형으로 캐스팅할 수 없습니다." |
| 프로젝트 관리 및 회계 | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **프로젝트 송장 보고서** 가 줄을 건너뜁니다. |
| 프로젝트 관리 및 회계 | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | 투자 프로젝트에 대한 비용 통제를 계산할 때 오류가 발생합니다. |
| 프로젝트 관리 및 회계 | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** 메서드가 성능 문제를 일으킵니다. |
| 프로젝트 관리 및 회계 | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | 오류 메시지는 "예기치 않은 오류"보다 명확해야 합니다. |
| 프로젝트 관리 및 회계 | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | 프로젝트 송장 전기 배치 작업은 송장 라인이 생성되지 않은 경우에도 송장 제안을 처리하고 전기합니다. |
| 프로젝트 관리 및 회계 | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | 공공 부문 라이선스 구성 키가 꺼져 있으면 반올림 문제가 발생합니다. 여러 기초 소스가 있는 계약의 작업표 시간에 잘못된 비용 또는 판매 가격이 생성됩니다. |
| 프로젝트 관리 및 회계 | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | 송장 발행된 프로젝트 구매 주문서의 프로젝트 판매 가격은 판매 가격 모델이 **기여율** 일 때 잘못 계산됩니다. |
| 프로젝트 관리 및 회계 | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | 시스템은 직원의 유효 노동률을 계산할 때 그 사이의 활동 일수를 고려하지 않습니다. |
| 프로젝트 관리 및 회계 | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | 다음 유효성 검사 오류로 인해 내부 거래 작업표에 전기 오류가 발생합니다. "법인에 대해 거래 파트너가 구성되지 않았습니다." |
| 프로젝트 관리 및 회계 | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | 경비 범주가 있는 구매 주문의 설명은 전기된 프로젝트 트랜잭션 목록에서 검색되지 않습니다. |
| 프로젝트 관리 및 회계 | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | 프로젝트에 전기된 항목 분개장에 잘못된 변환이 있습니다. |
| 프로젝트 관리 및 회계 | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | 펀딩 한도를 초과하여도 구매 주문 확인이 가능합니다. |
| 프로젝트 관리 및 회계 | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | 프로젝트 ID를 선택하면 무료 텍스트 송장의 **청구서 수정/취소** 섹션이 사라집니다. |
| 프로젝트 관리 및 회계 | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | 재고 품목이 포함된 프로젝트 판매 주문에서 프로젝트 송장 제안을 전기할 때 성능 문제가 있습니다. |
| 프로젝트 관리 및 회계 | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | 다음 오류가 발생하여 프로젝트 구매 송장을 게시할 수 없습니다. "AcDistProcessorProjectExtension.createForProjectRevenueLine 함수가 잘못 호출되었습니다." |
| 프로젝트 관리 및 회계 | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | 여러 하위 작업의 실행을 지원하기 위해 프로젝트 견적 일괄 작업 생성으로 업데이트합니다. |
| 프로젝트 관리 및 회계 | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | 워크플로가 **취소됨** 상태에서 멈추면 작업표 상태를 **초안** 으로 업데이트할 수 없습니다. |
| 프로젝트 관리 및 회계 | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | 여러 행이 있는 경우 유지 금액은 대변 메모 송장 제안서에서 계산되지 않습니다. |
| 프로젝트 관리 및 회계 | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | 구매 주문에서 생성된 송장의 금액을 변경하려고 하면 다음 오류가 발생합니다. "바우처의 거래가 XX/XX/XXXX에 따라 균형을 이루지 않습니다. (회계 통화: 0.00 - 보고 통화: 0.01)." |
| 프로젝트 관리 및 회계 | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | **GeneralJournalAccountEntry** 로 조인하기 때문에 프로젝트 송장 제안서가 일괄 모드로 전기되면 성능 문제가 있습니다. |
| 프로젝트 관리 및 회계 | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | 작업표를 전기할 때 성능 문제가 있습니다. |
| 프로젝트 관리 및 회계 | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | 모든 작업을 확장한 후 또는 단일 작업을 수동으로 확장한 후 작업 분할 구조의 비용 견적 계층이 올바르게 정렬되지 않았습니다. |
| 프로젝트 관리 및 회계 | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | **Excel에서 열기** 메뉴에 프로젝트 견적 Excel 템플릿을 추가할 수 없습니다. |
| 프로젝트 관리 및 회계 | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | 법인의 면세 번호가 인쇄된 프로젝트 송장에 포함되지 않습니다. |
| 프로젝트 관리 및 회계 | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | 프로젝트가 신용 한도와 관련하여 조정될 때 재고 단위 오류에서 재무 데이터가 업데이트되지 않습니다. |
| 프로젝트 관리 및 회계 | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | KB 461935를 적용한 후 연속 숫자 시퀀스로 전환하면 추정치를 게시할 수 없습니다. |
| 프로젝트 관리 및 회계 | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** 는 Android에 대한 프로젝트 작업표 모바일 앱이 응답을 중지하도록 합니다. |
| 프로젝트 관리 및 회계 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 송장 전기에서 취소된 WIP 값이 시간 입력에서 전기된 원래 WIP 값과 다릅니다. |
| 프로젝트 관리 및 회계 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 적용된 리테이너 사례의 경우 프로젝트에 대한 송장 수익이 전기될 때 바우처의 트랜잭션이 균형을 이루지 않습니다. |
| 프로젝트 관리 및 회계 | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **프로젝트 리소스 예약 성능 향상** 기능이 활성화되면 리소스 가용성 및 용량에 대해 소수 값이 잘못 반올림됩니다. |
| 프로젝트 관리 및 회계 | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | **여러 배치 작업을 사용하여 프로젝트 견적 생성** 기능이 활성화된 경우 여러 하위 작업이 있는 배치에서 견적 생성은 현재 기간에 대해서만 작동합니다. |
| 이동 및 경비 | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | 여행 요청 정책은 무시되고 워크플로는 오류 없이 승인됩니다. |
| 이동 및 경비 | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>모바일 경비 앱은 경비 라인에 다음 정보를 저장하지 않습니다.</p><ul><li>프로젝트 ID</li><li>경비 청구 가능 여부</li><li>활동 번호</li></ul> |
| 이동 및 경비 | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | 경비 라인에 영수증이 첨부되지 않은 경우에도 **첨부된 영수증** 필드가 **예** 로 설정됩니다. |
| 이동 및 경비 | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | 경비 범주를 **개인** 으로 변경하려고 하면 오류가 발생합니다. |
| 이동 및 경비 | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | 신용 카드 트랜잭션이 개인 경비로 분할된 후에는 영수증 첨부 및 상위 경비 편집이 불가능합니다. |
| 이동 및 경비 | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | 프로젝트 ID가 있는 내부 트랜잭션에 대한 경비 정책이 제대로 작동하지 않습니다. |
| 이동 및 경비 | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | 게시된 경비 보고서에 대한 게시 날짜 정보가 누락되었습니다. |
| 이동 및 경비 | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | 경비 모바일 앱에 결제 수단 문제가 있습니다. |
| 이동 및 경비 | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | 한 작업자에 대해 생성된 여행 요청은 대리인 날짜 이전에 다른 작업자의 경비 보고서에 사용할 수 있습니다. |
| 이동 및 경비 | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | 경비를 생성할 때 재무 차원 값에 대한 변경 사항은 **경비 관리** 작업 공간의 회계 배포 수준에서 올바르게 업데이트되지 않습니다. |
| 이동 및 경비 | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | 기본 경비 라인 승인 상태가 항목별 라인 워크플로우 승인 상태와 동기화되지 않습니다. |
| 이동 및 경비 | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | 경비 보고서를 전기하고 세금 공제가 활성화된 경우 오류가 발생합니다. |
| 이동 및 경비 | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | 대리인이 해고된 직원의 경비 문서를 삭제할 수 없습니다. |
| 이동 및 경비 | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | 경비 라인 삭제는 예상보다 시간이 오래 걸리고 성능에 영향을 미칩니다. |
| 이동 및 경비 | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** 는 **SourceDocumentLine** 만 삭제하기 때문에 고아 **TaxUncommitted** 레코드를 발생시킵니다. |
| 이동 및 경비 | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** 는 **trvExpTrans.ReferenceDataAreaId** 를 새 번호 시퀀스를 생성하기 위해 사용하지 않습니다. |

## <a name="regulatory-updates"></a>규제 업데이트

Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. Microsoft Dynamics LCS(Lifecycle Services)에 로그인하고 문제 검색 도구를 사용하여 계획된 규정 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가 또는 지역, 기능 유형 및 릴리스별로 검색할 수 있습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
