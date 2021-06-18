---
title: 리소스/생산 기반 시나리오에 대한 2021년 3월 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 항목은 리소스/생산 기반 시나리오에 대한 Project Operations의 2021년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: andchoi
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: d1a4658c8eec23f6816b58de42d785d769050b07
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997024"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>리소스/생산 기반 시나리오에 대한 2021년 3월 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 리소스/생산 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.17의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능
이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

  - [프로젝트 송장 제안서 성능](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>품질 업데이트

| 기능 영역                        | 참조 번호 | 품질 업데이트                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 프로젝트 관리 및 회계 | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | 트랜잭션이 재계산된 후에는 음수로 게시된 프로젝트 거래가 업데이트되지 않습니다.                                                                                                                      |
| 프로젝트 관리 및 회계 | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | 자금 출처에 할당된 트랜잭션 또는 송장이 없는 경우 자금 출처 삭제가 가능해야 합니다.                                                                                                           |
| 프로젝트 관리 및 회계 | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | 실제 추정 트랜잭션에는 이전 기간의 경비 및 항목 트랜잭션이 표시되지 않습니다.                                                                                                       |
| 프로젝트 관리 및 회계 | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | 프로젝트 항목 요구 사항의 패킹 슬립에 대한 원장 설명 값이 올바르지 않습니다.                                                                                                              |
| 프로젝트 관리 및 회계 | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | 프로젝트에 대해 분개장이 전기될 때 재무 차원은 바우처의 직원 및 항목에서 선택되지 않습니다.                                                                               |
| 프로젝트 관리 및 회계 | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | 프로젝트 송장 합계에서 라인 순 금액이 갱신되면 전기된 거래의 조정된 금액으로 판매 금액이 채워집니다.                                                                               |
| 프로젝트 관리 및 회계 | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | **공급업체 송장 지불시 지불** 페이지에서 공급업체 송장 라인을 검토할 때 송장이 프로젝트 ID 참조를 선택하지 않습니다.                                                                                                   |
| 프로젝트 관리 및 회계 | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 자금 출처가 여러 개인 고정 가격 프로젝트의 **계정** 페이지에서 계약 금액이 올바르지 않습니다.                                                                                                  |
| 프로젝트 관리 및 회계 | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | 고정 가격 프로젝트에서 발생한 매출은 제거가 전기된 후에도 조정되지 않습니다.                                                                                                                                |
| 프로젝트 관리 및 회계 | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | 프로젝트 판매 주문이 송장 제안을 통해 송장이 발행될 때 신용장 상태가 업데이트되지 않습니다.                                                                                                  |
| 프로젝트 관리 및 회계 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 구매 주문서에 송장이 발행되고 송장에 조달 범주와 품목이 포함된 경우 고객은 잘못된 계정 정보를 받게 됩니다.                                                                                              |
| 프로젝트 관리 및 회계 | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | 반복 배치 작업을 통해 생성된 프로젝트 송장 제안에는 금액이 0인 중복 트랜잭션이 있습니다.                                                                                                  |
| 프로젝트 관리 및 회계 | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | 프로젝트 손익 보고서를 실행하는 동안 오류 제한 검사를 제거합니다.                                                                                                                                  |
| 프로젝트 관리 및 회계 | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | 회사 간 재충전을 통해 전기된 비용은 **시간 및 재료 프로젝트 코드** 에서 **비용 전기** 기능을 사용할 때 손익 항목을 표시하지 않습니다.                                                         |
| 프로젝트 관리 및 회계 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | **송장 상태** 고정 가격 프로젝트에 대해 게시된 프로젝트 트랜잭션의 필터가 작동하지 않습니다.                                                                                                   |
| 프로젝트 관리 및 회계 | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | 중복된 대리인 레코드로 인해 작업표 항목이 중복됩니다.                                                                                                                                           |
| 프로젝트 관리 및 회계 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 역 추정 제거가 **주기적** 으로 작동하지 않습니다.                                                                                                                                                 |
| 프로젝트 관리 및 회계 | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | 범위가 추가되면 **프로젝트 관리 및 회계** 모듈의 **트랜잭션 조정** 옵션에서 적절한 데이터를 선택할 수 없습니다. **추가** 필터는 무시됩니다.                      |
| 프로젝트 관리 및 회계 | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | 작업을 기록한 후에는 생산 주문의 상태를 재설정할 수 없습니다.                                                                                                              |
| 프로젝트 관리 및 회계 | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | 프로젝트에서 자동 예약 및 CTP(Capable-to-Promise)가 있는 항목은 예약되지 않습니다.                                                                                                                      |
| 프로젝트 관리 및 회계 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **회계 조정** 기능은 **수동 입력 허용 안함** 이 선택된 원장 계정에 문제가 일으킵니다.                                                                     |
| 프로젝트 관리 및 회계 | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | 추정이 제거되면 프로젝트 명세서의 **실제 수익 - 판매액** 필드에 값이 표시되지 않아야 합니다.                                                                                 |
| 프로젝트 관리 및 회계 | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | 역할 가격 책정이 있는 프로젝트 조정에서 비용 및 판매 가격이 올바르지 않습니다.                                                                                                                        |
| 프로젝트 관리 및 회계 | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | Project Operations에서 부분 보유자 수정 후 보유자 수정 송장이 작동하지 않습니다.                                                                                                                   |
| 프로젝트 관리 및 회계 | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | **링크 제거** 옵션은 내부 거래 구매 주문을 취소하는 경우에만 활성화되어야 합니다.                                                                                                                                          |
| 프로젝트 관리 및 회계 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - 회사 간 프로젝트 송장 발행의 판매 가치 전기가 예상치 못한 계정을 선택함.                                                                                                                  |
| 프로젝트 관리 및 회계 | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | 청구서 제안서에 신용 메모용으로 선택된 항목이 포함되어 있는 경우 청구 규칙의 수수료가 다시 계산되지 않습니다.                                                                                            |
| 프로젝트 관리 및 회계 | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | Federal Awards Inquiry 지출 일정에는 경비 트랜잭션에 대해 프로젝트 송장 제안이 실행되지 않은 경우 영수증 금액이 표시됩니다.                                               |
| 프로젝트 관리 및 회계 | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | **잔액** 프로젝트 그룹이 있는 서비스 항목의 프로젝트 명세서에서 WIP 비용이 올바르지 않습니다.                                                                                               |
| 프로젝트 관리 및 회계 | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | 프로젝트와 관련된 무료 텍스트 송장은 수정할 수 없습니다.                                                                                                                                                  |
| 프로젝트 관리 및 회계 | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | 프로젝트 트랜잭션을 판매 가격 0으로 조정하면 송장 상태가 **청구 불가** 인 새 조정된 트랜잭션이 생성됩니다.                                                               |
| 프로젝트 관리 및 회계 | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | 동시에 여러 라인을 조정하는 경우 프로젝트 조정을 전기하는 동안 문제가 발생합니다.                                                                                                                               |
| 프로젝트 관리 및 회계 | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | 패킹 슬립을 전기한 후 제품 원가 및 품목 소요량이 변경되면 조정이 잘못된 원가 금액으로 전기됩니다.                                                                   |
| 프로젝트 관리 및 회계 | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | 직접 배송 구매 주문서의 재무 차원이 올바르지 않고 판매 주문 재무 차원으로 대체되었습니다.                                                              |
| 프로젝트 관리 및 회계 | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | 음수 수량 프로젝트 분개장 라인은 예측 수량이 0일 때 예측을 업데이트하지 않습니다.                                                                                        |
| 프로젝트 관리 및 회계 | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | Microsoft Excel을 사용하여 항목 요구 사항을 가져오려고 하면 영수증 날짜 오류가 발생합니다.                                                                                                                                                    |
| 프로젝트 관리 및 회계 | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | 공급업체 송장 트랜잭션에 대한 프로젝트 항목 트랜잭션 참조는 송장이 전기될 때 업데이트되지 않습니다.                                                                                               |
| 프로젝트 관리 및 회계 | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 프로젝트 송장 제안을 전기할 때 "선불 송장 차감이 추가될 때 트랜잭션이 보고 통화에서 균형을 이루지 않습니다"라는 오류가 발생할 수 있습니다.                                                                    |
| 프로젝트 관리 및 회계 | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | 프로젝트 레이아웃을 사용하는 경우 프로젝트 ID 및 프로젝트 이름은 **공급업체 결제 유지** 보고서에 입력되지 않습니다.                                                                                              |
| 프로젝트 관리 및 회계 | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 프로젝트가 데이터 엔터티를 통해 생성될 때 원장 전기 정렬 우선 순위가 올바르지 않습니다.                                                                                                                      |
| 프로젝트 관리 및 회계 | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | 공급업체 보유자가 있는 구매 주문을 기반으로 생성된 전기된 프로젝트 트랜잭션의 원가 금액이 올바르지 않습니다. 이로 인해 고정 가격 프로젝트에 대한 프로젝트 명세서 및 비용 관리에 잘못된 값이 생성됩니다. |
| 프로젝트 관리 및 회계 | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | 헤더가 업데이트될 때 프로젝트 판매 견적이 단가를 잘못 업데이트합니다.                                                                                                                    |
| 프로젝트 관리 및 회계 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations에서 보유자와 함께 작업할 때 선급금이 청구된 후 계약의 기본 프로젝트를 변경하면 나중에 차감에서 문제가 발생합니다.                                                                        |
| 프로젝트 관리 및 회계 | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | 공급업체 송장 및 프로젝트 판매 가격에 대한 송장 날짜 업데이트가 변경되었습니다.                                                                                                                                  |
| 프로젝트 관리 및 회계 | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 환율이 다른 내부 거래 트랜잭션을 조정할 때 문제가 발생합니다.                                                                                                                |
| 프로젝트 관리 및 회계 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 품목 요구 사항 및 구매 발주가 있는 약정 비용이 부분 제품 입고 및 부분 송장 발행이 있는 구매 발주 송장 프로세스에서 올바르지 않습니다.                                                |
| 프로젝트 관리 및 회계 | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | 추정이 환율로 반전되면 잘못된 값이 발생합니다.                                                                                                                                             |
| 프로젝트 관리 및 회계 | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | 시간 단위의 작업량은 작업 수준의 작업 분류 구조 템플릿에서 자동으로 지워집니다.                                                                                                                         |
| 프로젝트 관리 및 회계 | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | 견적 상태를 **손실** 로 업데이트하면 **생성됨** 또는 **전송됨** 상태로 시작한 모든 견적 상태가 **손실됨** 으로 업데이트됩니다.                 |
| 프로젝트 관리 및 회계 | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | 배달 날짜가 미래인 경우 판매 송장이 송장 제안에 표시되지 않습니다.                                                                                                                  |
| 프로젝트 관리 및 회계 | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | **프로젝트 항목 분개장 항목** 엔터티에 대한 비즈니스 논리가 변경되었습니다.                                                                                                                                          |
| 프로젝트 관리 및 회계 | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | 본지사 고객 송장의 발생 수익이 작업표 및 외화 재평가와 일치하지 않습니다.                                                                                 |
| 프로젝트 관리 및 회계 | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | 프로젝트 구매 요청 또는 프로젝트에서 프로젝트 구매 발주 라인의 납품 알림이 생성된 후 약정된 비용이 잘못 계산됩니다.                    |
| 프로젝트 관리 및 회계 | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | 프로젝트를 조정할 때 "재고 단위에서 재무 데이터가 업데이트되고 있지 않습니다"라는 오류가 발생할 수 있습니다.                                                                                                             |
| 프로젝트 관리 및 회계 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations에서 계약에서 프로젝트를 제거하면 필요한 경우 계약의 기본 프로젝트가 재설정되어야 합니다.                                                                                       |
| 프로젝트 관리 및 회계 | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | 사용세 적용시 프로젝트 비용 판매 가격이 잘못됩니다.                                                                                                                                         |
| 프로젝트 관리 및 회계 | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | 프로젝트 구매 발주 라인이 추가 송장으로 갱신될 때 잘못된 수량이 프로젝트 품목 소요량에 전기됩니다.                                                                                                 |
| 프로젝트 관리 및 회계 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations에서 회사 간 송장의 **라인 추가** 목록에 잘못된 비용 라인이 표시됩니다.                                                                                                |
| 프로젝트 관리 및 회계 | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | 송장 등록 및 송장 승인을 사용하여 트랜잭션을 전기하는 경우 **프로젝트 게시 트랜잭션** 페이지에서 **공급업체 계정** 필드가 비어 있습니다.                                                                  |
| 프로젝트 관리 및 회계 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 원래 프로젝트 날짜는 **새 프로젝트 날짜로 조정 날짜 사용** 이 **아니요** 로 설정된 경우 오류를 발생시키는 조정에서 고려되지 않습니다.                                                                     |
| 프로젝트 관리 및 회계 | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | 트랜잭션 통화가 회사 통화와 다른 경우 프로젝트 관련 일반 분개 및 비용 분개장의 판매 가격이 잘못 계산됩니다.                                     |
| 프로젝트 관리 및 회계 | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | 프로젝트 구매 주문서의 부분 송장에 대한 판매 거래가 바우처에 표시되지 않습니다.                                                                                                                          |
| 프로젝트 관리 및 회계 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 프로젝트 회계사 및 프로젝트 관리자 역할은 승인 그룹 설정으로 시간 분개를 만들 수 없습니다.                                                                                                         |
| 프로젝트 관리 및 회계 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Microsoft Excel을 사용하여 가져온 경비 보고서를 게시할 수 없습니다.                                                                                                                                                              |
| 프로젝트 관리 및 회계 | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | **메시지** 필드가 활성 상태가 아니므로 작업표 정책을 만들 수 없습니다.                                                                                                                               |
| 프로젝트 관리 및 회계 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 내부 트랜잭션 시나리오에서 공급업체 트랜잭션 취소가 허용되는 문제가 있습니다. 이는 공급업체 송장과 경비 보고서 모두에 적용됩니다.                                                                                 |
| 프로젝트 관리 및 회계 | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | 승인된 작업표의 배포는 재설정할 수 없습니다.                                                                                                                                                     |
| 프로젝트 관리 및 회계 | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | 시간 및 항목 분개에 대한 환율로 추정치를 반전할 때 잘못된 값이 발생합니다.                                                                                                                  |
| 프로젝트 관리 및 회계 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 프로젝트 조정이 간접 비용으로 판매 금액을 올바르게 업데이트하지 않습니다.                                                                                                                              |
| 프로젝트 관리 및 회계 | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | 시간 분개를 전기할 때 "차원 값이 지정되지 않았습니다"라는 오류 메시지가 나타납니다.                                                                                                                                  |
| 프로젝트 관리 및 회계 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 다른 통화를 사용하는 프로젝트 계약이 바우처의 회계 통화를 올바르게 계산하지 않습니다.                                                                                              |
| 프로젝트 관리 및 회계 | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | 본지사 작업표 WIP 전기에 잘못된 판매 WIP 계정이 사용되었습니다.                                                                                                                                     |
| 프로젝트 관리 및 회계 | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | 할인이 적용되고 창고가 업데이트될 때 프로젝트 견적이 가격을 잘못 계산합니다.                                                                                                       |
| 프로젝트 관리 및 회계 | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | 프로젝트 트랜잭션에서 품목 원가 조정을 사용한 후 재계산을 실행하면 "오류로 인해 재계산이 일시 중지됩니다"라는 오류 메시지가 발생합니다.                                                               |
| 프로젝트 관리 및 회계 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | 수익 발생시 청구 가능에서 청구 불가능으로 트랜잭션을 조정할 때 총계정 원장 항목이 생성되지 않습니다.                                                                                              |
| 프로젝트 관리 및 회계 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 프로젝트 공급업체 송장 보관 기능인 **비용 계산 사용** 이 켜져 있으면 **ProjTrans** 가 지불시 결제로 생성되지 않습니다.                                             |
| 프로젝트 관리 및 회계 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **송장 제안 생성** 페이지에 여러 문제가 있습니다.                                                                                                                                                     |
| 프로젝트 관리 및 회계 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations에서 **구매 계약** 페이지는 Project Operations와 통합된 금융 법인에 표시되지 않습니다.                                                                                             |
| 프로젝트 관리 및 회계 | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | 고급 분개는 **다음 개설 기간으로 회계 날짜 자동 설정** 옵션이 켜져 있어도 마감 기간의 회계 날짜로 전기할 수 없습니다.                                                |
| 프로젝트 관리 및 회계 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse 통합 오류로 인해 Project Operations에서 견적을 성공으로 변환할 수 없습니다.                                                                                                                                       |
| 프로젝트 관리 및 회계 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations에서 겹치는 계약 내용 및 트랜잭션 유형을 확인하기 때문에 계약 내용을 프로젝트 ID에 연관시키려고 하면 오류 메시지가 발생합니다.                                                |
| 프로젝트 관리 및 회계 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 는 다른 고객의 자금 출처 송장 주소를 설정할 수 있습니다.                                                                                                             |
| 프로젝트 관리 및 회계 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 페이지에서 리소스의 표준 조회는 10.0.15 업데이트 이후에 사용할 수 없습니다.                                                                                                                    |
| 프로젝트 관리 및 회계 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 프로젝트 그룹이 **잔액** 으로 설정된 경우 총계정 원장 바우처의 원장 계정 및 전기 유형이 올바르지 않고 비 재고 서비스 품목에 대한 구매 주문 바우처의 전기 유형이 올바르지 않습니다.                                 |
| 프로젝트 관리 및 회계 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | **상위 활동 선택 차단** 이 아니요로 설정되어 있어도 보류 중인 공급업체 송장에는 활동 번호가 표시되지 않습니다.                                                                    |
| 프로젝트 관리 및 회계 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Project Operations에서는 트랜잭션에 대한 전기 송장을 생성할 때 차원이 선택되지 않습니다.                                                                                                                   |
| 프로젝트 관리 및 회계 | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | 프로젝트 관리 및 회계에서 이전 가격의 우선 순위는 회사 간 작업표에 정확하게 반영되지 않습니다.                                                                            |
| 프로젝트 관리 및 회계 | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | 레거시 작업 분류 체계 (WBS) 클래스 방법 **ProjWBSUpdateController::updateOutlineNumbersAndPublishInPreOrder** 는 더 이상 사용되지 않습니다.                                                                                                   |

### <a name="regulatory-updates"></a>규제 업데이트
Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](/dynamics365/finance/localizations/regulatory-updates.md)를 참조하십시오. LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
