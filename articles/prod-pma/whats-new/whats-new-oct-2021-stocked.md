---
title: 2021년 10월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 재고/생산 기반 시나리오에 대한 Project Operations의 2021년 10월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 03491ccab855e48819fccf4c9d2b584fd87cb4ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576048"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>2021년 10월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 재고/생산 기반 시나리오에 대한 Project Operations_

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.22의 프로젝트 관리 및 회계
 
## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
|--------------|------------------|----------------|
| 프로젝트 관리 및 회계 | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | 본지사 고객 송장이 전기될 때 프로젝트 WIP(Work In Process) 및 미지급 수익 금액이 올바르게 취소되지 않습니다. |
| 프로젝트 관리 및 회계 | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **열린 트랜잭션이 있는 경우 프로젝트 종료 방지** 기능이 작동하지 않습니다. |
| 프로젝트 관리 및 회계 | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | 자유 텍스트 송장의 청구 분류는 해당 기능이 활성화된 경우 프로젝트의 차원을 자동으로 채우지 않습니다. |
| 프로젝트 관리 및 회계 | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | 본지사 이외의 시나리오에서는 프로젝트 송장이 전기될 때 WIP 및 미지급 수익 금액이 올바르게 취소되지 않습니다. |
| 프로젝트 관리 및 회계 | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Microsoft Excel 추가 기능이 프로젝트 경비 분개장과 함께 사용되고 **상계 계정 유형** 필드가 **프로젝트** 로 설정되면 차변 및 대변 값이 전환됩니다. |
| 프로젝트 관리 및 회계 | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | 프로젝트 트랜잭션에 전기된 금액은 재고 품목을 포함하고 **UseTax** 가 표시된 경우에 공제할 수 없는 세액이 있는 프로젝트 구매 발주에서 과대계상됩니다. |
| 프로젝트 관리 및 회계 | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | 시스템은 금액을 프로젝트 손익 보고서와 프로젝트 WIP 보고서로 나눕니다. |
| 프로젝트 관리 및 회계 | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | 부분적으로 반품된 품목 요구 사항이 조정된 후 현재고가 올바르지 않습니다. |
| 프로젝트 관리 및 회계 | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | 리소스 이름은 Microsoft Project에서 편집할 때 Project Operations에서 중복됩니다. |
| 프로젝트 관리 및 회계 | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | 지급 계정 본지사 보류 중인 공급업체 송장 비용이 있는 본지사 경비 보고서는 먼저 **프로젝트 WIP 비용** 전기 유형에 전기됩니다. 그러나 처리 중 예상 관련 비용은 예상 **본지사 비용** 전기 유형이 아닌 **프로젝트 비용** 전기 유형으로 전기됩니다. |
| 프로젝트 관리 및 회계 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 프로젝트 경비 트랜잭션의 공급업체 유보금 결과는 표시되지 않습니다. |
| 프로젝트 관리 및 회계 | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | 작업표는 거래 통화의 거래 금액을 모든 회계 분배 및 일반 분개 할당 항목에서 지정된 소수점 이하 자릿수로 반올림해야 합니다. |
| 프로젝트 관리 및 회계 | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | 프로젝트 품목 요구 사항의 수량은 계획 주문이 확정되면 자동으로 업데이트됩니다. |
| 프로젝트 관리 및 회계 | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | 바우처 번호, 트랜잭션 유형 공급업체 잔액 및 거래처 번호는 구매 주문의 선불 송장에서 되돌릴 수 없습니다. |
| 프로젝트 관리 및 회계 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 공급업체 송장 통합이 켜져 있으면 회사 간 공급업체 송상이 손상됩니다. |
| 프로젝트 관리 및 회계 | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | 프로젝트 경비 분개장을 만들 때 비용 금액은 **신용** 필드에 표시됩니다. |
| 프로젝트 관리 및 회계 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 프로젝트 송장의 지불 조건이 예상대로 작동하지 않습니다. |
| 프로젝트 관리 및 회계 | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | 일련 번호가 연속으로 설정된 경우 작업표 바우처를 재사용할 수 있습니다. |
| 프로젝트 관리 및 회계 | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | 프랑스: **수동 보유 금액** 논리가 프로젝트 계약 송장 제안서의 **자동 보유 금액** 논리와 일치하지 않습니다. |
| 프로젝트 관리 및 회계 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 공급업체 보유가 해제되면 전표 전기에 잘못된 추가 행이 있습니다. |
| 프로젝트 관리 및 회계 | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **송장 제안 생성** 페이지의 **송장 날짜** 필드가 변경되면 "개체 참조가 개체의 인스턴스로 설정되지 않았습니다." 오류가 발생할 수 있습니다. |
| 프로젝트 관리 및 회계 | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | **TSLine** 워크플로에서 작업표를 승인하려고 하면 오류가 발생하며 작업표 정책이 토요일과 일요일에 있습니다. |
| 프로젝트 관리 및 회계 | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | 송장 제안서의 송장 합계를 계산할 때 기초 잔액 프로젝트 항목 유형은 **송장 제안서 트랜잭션 요약** 에서 제외됩니다. |
| 프로젝트 관리 및 회계 | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | 프로젝트 생산 주문의 소비 비용이 0(영)인 경우 추정하려고 하면 "0으로 나누려고 시도했습니다." 오류가 발생합니다. |
| 프로젝트 관리 및 회계 | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Android용 프로젝트 작업표 모바일 앱이 응답을 멈춥니다. 이 문제는 **TimeEntryDataManager ArgumentNullException** 과 관련이 있습니다. |
| 프로젝트 관리 및 회계 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | 계정에 차원이 없기 때문에 전기할 때 Project Operations 통합 분개장이 실패합니다. 그러나 차원이 누락된 계정은 전기 중인 계정이 아닙니다. |
| 프로젝트 관리 및 회계 | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | **전기 비용** 페이지의 **선택** 대화 상자에서 제거될 때 검색에서 **ToDate** 필터가 지워지지 않습니다. |
| 프로젝트 관리 및 회계 | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **모든 배포 재설정** 이 실패하고 **시간만** 유형의 프로젝트에 대해 생성된 작업표에 대한 오류를 표시합니다. |
| 프로젝트 관리 및 회계 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 조달 범주가 항목에 할당된 경우 보류 중인 공급업체 송장에서 **프로젝트** 탭을 편집할 수 없습니다. |
| 프로젝트 관리 및 회계 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse에 로그인하지 않은 경우 탐색 창이 없습니다. |
| 프로젝트 관리 및 회계 | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | 본지사 프로젝트 조정 트랜잭션의 경우 대상 회사에 문제가 있습니다. |
| 프로젝트 관리 및 회계 | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | 프로젝트에 대한 약정 비용은 구매 주문이 총계정원장의 **구매 주문 연말 프로세스** 에서 처리된 경우 잘못된 수량 및 비용 가격을 계산합니다. |
| 프로젝트 관리 및 회계 | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | 품질 주문이 있는 프로젝트 생산 주문이 완료된 것으로 보고되면 "재고 트랜잭션으로 표시된 가상 트랜잭션이 없습니다." 오류가 발생합니다. |
| 프로젝트 관리 및 회계 | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | 프로젝트 관련 지급 계정 송장이 전기되면 다음 오류가 발생합니다. "열거된 텍스트 프로젝트 - 비용 - 항목이 존재하지 않습니다." |
| 프로젝트 관리 및 회계 | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | 수동으로 수익을 발생시키면 간접 비용이 두 배가 됩니다. |
| 프로젝트 관리 및 회계 | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | 수익 발생 및 WIP 전기는 트랜잭션을 생성하지 않습니다. |
| 프로젝트 관리 및 회계 | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | 수신된 프로젝트 구매 주문이 있는 경우 표준 원가 항목에 대해 보류 중인 가격 활성화가 실패합니다. |
| 프로젝트 관리 및 회계 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 송장 전기에서 취소된 WIP 값이 시간 입력에서 전기된 원래 WIP 값과 다릅니다. |
| 프로젝트 관리 및 회계 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 바우처의 트랜잭션이 균형을 이루지 않는 적용된 리테이너 사례의 경우 프로젝트 송장 수익에 대한 전기 문제가 있습니다. |
| 프로젝트 관리 및 회계 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 송장 제안이 전기된 후 견적을 생성하면 Project Operations에서 수정 라인 가져오기가 차단됩니다. |
| 프로젝트 관리 및 회계 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 완전히 청구된 마일스톤 레코드의 수정은 불가능해야 합니다. |
| 프로젝트 관리 및 회계 | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | 자동 청구를 사용하는 경우 작업표에 대한 본지사 고객 송장을 전기할 수 없으며 오류 메시지가 표시됩니다. |
| 프로젝트 관리 및 회계 | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | 하위 프로젝트의 주소가 올바르게 업데이트되지 않았습니다. |
| 프로젝트 관리 및 회계 | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | 품목 요구 사항의 비용 가격이 통합 구매 주문의 구매 가격으로 업데이트됩니다. |
| 프로젝트 관리 및 회계 | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | 구매 가격이 업데이트되고 매개 변수 **변경 관리 활성화** 가 활성화된 후 게시된 비용이 올바르지 않습니다. |
| 이동 및 경비 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 모든 사용자 경비는 경비 모바일 앱에서 범주를 검색할 때 볼 수 있습니다. |
| 이동 및 경비 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 신용 카드 트랜잭션에서 생성된 비용으로 전기된 공급업체 트랜잭션 및 판매세 거래 금액이 올바르지 않습니다. |
| 이동 및 경비 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 경비 보고서 페이지를 새로 고칠 때 관련 없는 경고 메시지가 표시됩니다. |
| 이동 및 경비 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 임시 승인자를 삭제한 후 워크플로를 통해 다시 제출하면 잘못된 임시 승인자가 사용됩니다. |
| 이동 및 경비 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 마일리지 설정과 관련된 게시 오류가 발생합니다. |
| 이동 및 경비 | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | 본지사 경비에 대한 경비 보고서에 첨부되지 않은 트랜잭션이 다시 추가될 때 분배는 법인을 업데이트하지 않습니다. |

### <a name="regulatory-updates"></a>규제 업데이트

금융 및 운영 앱의 규정 업데이트에 대한 자세한 내용은 [규정 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. Microsoft Dynamics LCS(Lifecycle Services)에 로그인하고 문제 검색 도구를 사용하여 계획된 규정 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가 또는 지역, 기능 유형 및 릴리스별로 검색할 수 있습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
