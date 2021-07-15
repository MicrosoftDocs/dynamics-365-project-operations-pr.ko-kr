---
title: 리소스/생산 기반 시나리오에 대한 2021년 7월 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 항목은 재고/생산 기반 시나리오에 대한 2021년 7월 Project Operations에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334567"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>리소스/생산 기반 시나리오에 대한 2021년 7월 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 재고/생산 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.20의 프로젝트 관리 및 회계
 
### <a name="quality-updates"></a>품질 업데이트
                                                                                                                                                                                  
| 기능 영역                      | 참조 번호| 품질 업데이트                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 프로젝트 관리 및 회계 | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | 구매 요청의 비용 약정 레코드는 구매 요청 발행에서 구매 주문이 릴리스되는 즉시 지워집니다.                                                                           |
| 프로젝트 관리 및 회계 | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | 예산 검증은 구매 요청에서 두 번 발생합니다. 이 중복은 구매 요청을 마감할 수 없고 해당 구매 주문이 생성되지 않음을 의미합니다.                                                                                                                        |
| 프로젝트 관리 및 회계 | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | 반올림 문제로 인해 **청구할 비율** 청구 규칙을 완료할 수 없습니다.                                                                              |
| 프로젝트 관리 및 회계 | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | 트랜잭션을 조정하고 백분율에 소수가 있으면 비용 및 판매 가격이 올바르게 조정되지 않습니다.                                      |
| 프로젝트 관리 및 회계 | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | 회계 소스 탐색기는 활동이 다른 여러 작업표 라인의 단일 작업표 라인에 대한 시간을 표시합니다.                                      |
| 프로젝트 관리 및 회계 | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | 저장된 보기 및 작업표 행 세부사항 개인화로 인해 시스템은 작업표를 열려고 할 때 항상 목록의 첫 번째 작업표에 대한 세부사항을 엽니다.  |
| 프로젝트 관리 및 회계 | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | 프로젝트 루트 노드가 사라지고 작업 분할 구조 레코드가 가져오기 후에 삭제됩니다.                                                                                             |
| 프로젝트 관리 및 회계 | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | 품목 소요량에서 품목이 부분적으로 입고 및 출고되면 시스템이 잘못된 예산 소비 잔액을 업데이트합니다. |
| 프로젝트 관리 및 회계 | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | 프로젝트 유보 구매 주문이 **총계** 창 또는 **보류 중인 송장** 그리드에 총계를 올바르게 표시하지 않습니다.                                                                  |
| 프로젝트 관리 및 회계 | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | 재고를 마감할 때 프로젝트 품목 원가 조정은 손익 계정 대신 잔액 계정에 전기됩니다.                                                            |
| 프로젝트 관리 및 회계 | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | 프로젝트에 게시된 트랜잭션 전표 및 견적 전표는 회계 통화로 USD를 사용하지만 금액은 CAD 등가물을 보여줍니다.              |
| 프로젝트 관리 및 회계 | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | 품목 요구 사항 및 구매 주문과 함께 약정된 비용이 부품 제품 수령 및 부품 송장이 포함된 구매 주문 송장 프로세스에서 잘못되었습니다.       |
| 프로젝트 관리 및 회계 | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | 프로젝트 조정이 간접 비용으로 판매 금액을 올바르게 업데이트하지 않습니다.                                                                                    |
| 프로젝트 관리 및 회계 | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **작업표** 테이블에 **작업자/리소스** 보기와 정의된 관계가 없습니다.                                                                                   |
| 프로젝트 관리 및 회계 | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | 회사 간 작업표의 드롭다운 메뉴에서 선택하면 **활동 번호** 필드를 채울 수 없습니다.                                                                 |
| 프로젝트 관리 및 회계 | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | **프로젝트 게시된 트랜잭션**, **송장 제안 생성** 또는 **송장 제안서** 페이지에는 개인화된 **목적** 또는 **활동 설명** 필드를 추가할 수 없습니다.  |
| 프로젝트 관리 및 회계 | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | 데이터 관리(**ProjSalesItemRequirementEntity**)를 사용하여 품목 소요량을 생성할 때 잘못된 배송 날짜 제어가 제공됩니다.                                              |
| 프로젝트 관리 및 회계 | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Finance에서 프로젝트 계약 ID를 선택하면 기존 프로젝트 계약을 여는 대신 Project Operations 통합 환경에서 페이지를 열어 새 레코드를 생성합니다.                                                                                                                 |
| 프로젝트 관리 및 회계 | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  레이블, "@SYS4083080"("입력한 값에 해당하는 고유한 작업자 레코드를 찾을 수 없습니다.")는 덴마크어로 번역되지 않습니다.                                |
| 프로젝트 관리 및 회계 | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | **품목 판매세 그룹** 송장 제안에서 필드를 편집할 수 없습니다.                                                                               |
| 프로젝트 관리 및 회계 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 약정 비용이 공제할 수 없는 세액으로 과대계상되었습니다.                                                                                                    |
| 프로젝트 관리 및 회계 | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | 여러 프로젝트와 다양한 재무 차원이 포함된 본지사 작업표를 전기하면 총계정원장에 예상치 못한 값이 생성됩니다.                             |
| 프로젝트 관리 및 회계 | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | 동시에 실행 중인 **준비에서 가져오기** 주기적 프로세스의 여러 인스턴스로 인해 송장 제안 라인이 중복됩니다.                                      |
| 프로젝트 관리 및 회계 | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | 신용 메모 송장 제안 게시에 오류가 있어 바우처의 거래가 균형을 이루지 않습니다.    |
| 프로젝트 관리 및 회계 | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | 보류 보류 중 송장이 릴리스된 후 프로젝트 약정 비용이 올바르지 않게 됩니다.                                                                             |
| 프로젝트 관리 및 회계 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 세금이 회사 통화와 다른 통화인 경우 프로젝트 판매 주문에 대한 대변 메모를 생성할 수 없습니다.                                      |
| 프로젝트 관리 및 회계 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 계약을 삭제하면 고객과 연결된 주소도 삭제됩니다.                                                                                     |
| 프로젝트 관리 및 회계 | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | 음수 시간 트랜잭션 수정으로 인한 송장 제안은 게시할 수 없습니다.                                                                    |
| 이동 및 경비                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | 세금이 경비 보고서에서 다르게 계산됩니다.                                                                                                                  |
| 이동 및 경비                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | 릴리스 업데이트 **DB72_Expense.updateTrvExpTransProjTransId()** 가 새 번호 시퀀스를 생성하도록 **trvExpTrans.ReferenceDataAreaId** 를 허용하지 않습니다.                    |
| 이동 및 경비                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | 제출된 금액이 필수 필드에 표시되지 않습니다.                                                                                                             |
| 이동 및 경비                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | 재구성된 경비 사용자 인터페이스를 사용하여 경비 보고서에 경비를 첨부하는 성능이 향상되었습니다.                                                            |
| 이동 및 경비                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | 게시된 경비 보고서를 삭제할 수 있습니다.                                                                                           |
| 이동 및 경비                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | 경비 정책 메시지가 여러 번 표시됩니다.                                                                                                       |
| 이동 및 경비                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **결제 방법** 필드가 **새로운 경비** 창에 포함됩니다.                                                                                                      |
| 이동 및 경비                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | 워크플로를 찾을 수 없는 경우 **경비 문서 상태 재설정** 도구는 경비 보고서 상태를 **초안** 으로 재설정해야 합니다. 

### <a name="regulatory-updates"></a>규제 업데이트
Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. 또한 LCS(Lifecycle Services)에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
