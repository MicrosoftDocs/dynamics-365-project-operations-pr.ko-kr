---
title: 리소스/생산 기반 시나리오에 대한 2021년 4월 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 항목은 리소스/생산 기반 시나리오에 대한 Project Operations의 2021년 4월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: andchoi
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 42b4da3a77d56891454d094cd771575ff9bff081
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589618"
---
# <a name="whats-new-or-changed-in-project-operations-april-2021-for-stockedproduction-based-scenarios"></a>리소스/생산 기반 시나리오에 대한 2021년 4월 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 리소스/생산 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.18의 프로젝트 관리 및 회계
 
### <a name="quality-updates"></a>품질 업데이트
                                                                                                                                                                                  
| 기능 영역                      | 참조 번호| 품질 업데이트                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 프로젝트 관리 및 회계 | [534393](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534393) | **프로젝트 정렬** 그리드에 오류가 발생합니다.                                                                                                                                                      |
| 프로젝트 관리 및 회계 | [542850](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542850) | 프로젝트 구매 주문에서 단가 및 수량이 수정된 후 약정된 금액이 과장되어 있습니다.                                                                                    |
| 프로젝트 관리 및 회계 | [543645](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543645) | **ProjParameters** 변수가 선언되었지만 사용되기 전에 레코드 버퍼가 할당되지 않았습니다.                                                                                     |
| 프로젝트 관리 및 회계 | [543674](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543674) | **ResRollup** 테이블이 삭제되면 **모든 회사의 프로젝트 리소스 채우기** 일괄 작업이 실행됩니다.                                                                          |
| 프로젝트 관리 및 회계 | [544417](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544417) | **구매 발주 라인 V2** 엔터티를 사용하여 구매 주문 필드에서 **프로젝트 판매 가격** 필드를 업데이트할 때 문제가 있습니다..                                                                           |
| 프로젝트 관리 및 회계 | [547652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547652) | ID 번호에 따라 하위 프로젝트를 생성할 수 없습니다.   "함수 Global:: int642int가 잘못 호출되었습니다." 오류가 발생합니다.                                         |
| 프로젝트 관리 및 회계 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 고객은 동일한 송장에 조달 범주 및 품목이 있는 구매 주문을 송장 발행할 때 잘못된 계정을 받습니다.                                                                      |
| 프로젝트 관리 및 회계 | [509920](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509920) | 간접 비용이 있는 프로젝트 트랜잭션을 청구 가능에서 청구 불가능으로 다시 청구 가능으로 조정하면 WIP가 올바르게 정산되지 않습니다.                                       |
| 프로젝트 관리 및 회계 | [511274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511274) | 판매 주문에서 보존 및 총 할인을 사용할 때 송장 금액이 올바르지 않습니다.                                                                                          |
| 프로젝트 관리 및 회계 | [511315](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511315) | 다른 트랜잭션 유형을 선택하더라도 라인 세부 정보의 주소 이름은 변경되지 않습니다.                                                                           |
| 프로젝트 관리 및 회계 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 품목 요구 사항 및 구매 발주가 있는 약정 비용이 부품 제품 입고 및 부품 송장 발행이 있는 구매 발주 송장 프로세스에서 올바르지 않습니다.                       |
| 프로젝트 관리 및 회계 | [524226](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524226) | 프로젝트의 재무 차원이 변경되면 구매 주문서 헤더에 변경 사항이 반영되지 않습니다.                                                                                                  |
| 프로젝트 관리 및 회계 | [524979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524979) | 생성된 **고정 가격 프로젝트** 보고서가 비어 있습니다.                                                                                                         |
| 프로젝트 관리 및 회계 | [529445](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529445) | 송장은 **지불시 결제** 페이지에서 공급업체 송장을 검토할 때 프로젝트 ID 참조를 선택하지 않습니다.                                                                          |
| 프로젝트 관리 및 회계 | [529982](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529982) | 범주가 올바르게 기본 설정되지 않았으므로 **HR 관리자** 역할의 한 법인에 대해 제한된 액세스 권한을 가진 사용자의 작업 표 항목이 올바르지 않습니다.                                         |
| 프로젝트 관리 및 회계 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 원래 프로젝트 날짜는 **새 프로젝트 날짜로 조정 날짜 사용** 필드가 **아니요** 로 설정된 경우 오류를 발생시키는 조정에서 고려되지 않습니다.                                             |
| 프로젝트 관리 및 회계 | [530788](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530788) | 일괄 처리를 사용하여 프로젝트 견적을 계산하면 결과가 올바르지 않습니다.                                                                                                         |
| 프로젝트 관리 및 회계 | [530834](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530834) | 프로젝트 계약에 사용된 금액이 프로젝트의 미적용 금액과 일치하지 않습니다.                                                                             |
| 프로젝트 관리 및 회계 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 프로젝트 회계사 및 프로젝트 관리자 역할은 승인 그룹 설정으로 한 시간 분개를 만들 수 없습니다.                                                                                 |
| 프로젝트 관리 및 회계 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Microsoft Excel에서 가져온 경비 분개장을 전기할 수 없습니다.                                                                                                                                       |
| 프로젝트 관리 및 회계 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 공급업체 송장 및 경비 보고서를 포함하여 내부 거래 시나리오에서 공급업체 트랜잭션 취소가 허용됩니다.                                                                     |
| 프로젝트 관리 및 회계 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 프로젝트 조정이 간접 비용으로 판매 금액을 올바르게 업데이트하지 않습니다.                                                                                                    |
| 프로젝트 관리 및 회계 | [534869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534869) | 고정 가격 프로젝트 송장에 대한 신용 메모가 생성되고 납품 단위 청구 규칙을 사용하는 경우 릴리스된 단위는 재청구에 사용할 수 없습니다. |
| 프로젝트 관리 및 회계 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 통화가 다른 프로젝트 계약은 품목 분개장 또는 송장 제안에서 회계 통화를 올바르게 계산하지 않습니다.                                                   |
| 프로젝트 관리 및 회계 | [537158](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537158) | 구매 발주 라인의 프로젝트를 변경하여 품목 소요량을 이전합니다.                                                                                                                          |
| 프로젝트 관리 및 회계 | [540603](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540603) | 예측에서 프로젝트 예산으로 가져오면 금액이 잘못됩니다.                                                                                                                    |
| 프로젝트 관리 및 회계 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5406222) | 청구 가능에서 청구 불가능으로 트랜잭션을 조정할 때 총계정 원장 항목이 생성되지 않습니다.                                                                                            |
| 프로젝트 관리 및 회계 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 기능 키인 **프로젝트 공급업체 송장 보관 기간에 대한 비용 계산 기능 사용** 이 켜져 있는 경우 지불시 결제를 사용하여 프로젝트 트랜잭션이 생성되지 않습니다.                  |
| 프로젝트 관리 및 회계 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **송장 제안 생성** 페이지에 여러 문제가 있습니다.                                                                                                                             |
| 프로젝트 관리 및 회계 | [543390](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543390) | **모든 프로젝트** 페이지에 새 언어 코드가 있는 목록이 표시되지 않습니다.                                                                                                            |
| 프로젝트 관리 및 회계 | [543803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543803) | 예산이 두 번 이상 수정되면 프로젝트 예산 잔액의 승인되지 않은 예산 금액이 올바르지 않습니다.                                                                |
| 프로젝트 관리 및 회계 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | **구매 계약** 페이지는 Project Operations와 통합된 금융 법인에 표시되지 않습니다.                                                                               |
| 프로젝트 관리 및 회계 | [545456](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545456) | 올바른 바우처 날짜가 프로젝트 시간 분개장 항목에 업로드되지 않습니다.                                                                                                            |
| 프로젝트 관리 및 회계 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 리소스 기반 시나리오의 Project Operations에서 통합 오류로 인해 견적을 성공으로 변환할 수 없습니다.                                                                      |
| 프로젝트 관리 및 회계 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations에서 겹치는 계약 내용 및 거래 유형을 확인하기 때문에 계약 내용과 프로젝트 ID 사이에 연관을 생성하려고 하면 오류 메시지가 표시됩니다.                        |
| 프로젝트 관리 및 회계 | [546949](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546949) | **리소스/프로젝트 검증 그룹** 페이지의 **ProjValEmplProjSetup** 표에 14,000개 이상의 레코드가 있는 경우 페이지에 성능 문제가 있습니다.                                                                     |
| 프로젝트 관리 및 회계 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 는 다른 고객의 자금 출처 송장 주소를 설정할 수 있습니다.                                                                                   |
| 프로젝트 관리 및 회계 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 리소스의 표준 조회는 10.0.15 릴리스 이후에 사용할 수 없습니다.                                                                                          |
| 프로젝트 관리 및 회계 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 구매 발주 송장 전표의 원장 계정 및 전기 유형이 서비스 품목에 대해 일치하지 않습니다. 프로젝트 그룹은 **잔액** 으로 설정되고 원장 계정이 올바르지 않습니다.                   |
| 프로젝트 관리 및 회계 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | **상위 활동 선택 차단** 이 **아니요** 로 설정되어 있어도 보류 중인 공급업체 송장에는 활동 번호가 표시되지 않습니다.                                            |
| 프로젝트 관리 및 회계 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | **프로젝트** > **예산** > **개정** > **새로 만들기** > **가져오기** 탐색 경로를 사용하면 시스템은 모든 프로젝트에 대한 프로젝트 예산 개정을 생성합니다.                                                            |
| 프로젝트 관리 및 회계 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) | 트랜잭션 및 회계 통화가 다른 트랜잭션을 조정할 때 잘못된 전기 및 총계정 원장 입력이 발생합니다.                                                                        |
| 프로젝트 관리 및 회계 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 트랜잭션에 대한 전기 송장을 생성할 때 차원이 포함되지 않습니다.                                                                                                   |
| 프로젝트 관리 및 회계 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | **PurchTotals.purchNewTotalAmount()** 성능 문제를 일으키는 구매 주문과 연결되지 않은 보류 중인 공급업체 송장을 만들 때 메서드가 호출됩니다.                    |
| 이동 및 경비                | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 마일리지 설정과 관련된 게시 오류가 있습니다.                                                                                                                                          |
| 이동 및 경비                | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | 외화 경비 트랜잭션에 대한 **개인으로 분할** 이 작동하지 않습니다.                                                                                                         |
| 이동 및 경비                | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 경비 범주 드롭 다운 메뉴는 **대리인** 이 리소스로 설정되었는지에 관계 없이 잘못된 범주를 표시합니다.                                         |
| 이동 및 경비                | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | 리소스/범주 검증 오류로 인해 회사 간 경비 보고서를 저장할 수 없습니다.                                                                                             |
| 이동 및 경비                | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 경비 보고서 전기의 잘못된 마일리지 계산에 분할 라인이 있습니다.                                                                                                        |
| 이동 및 경비                | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 판매세가 포함되어 있고 결제 방법의 오프셋 계정 유형이 **작업자** 와 같은 경우 회사 간 경비 보고서를 전기할 수 없습니다.                                                   |
| 이동 및 경비                | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** 데이터 엔터티 및 엔터티와 연결된 고유 인덱스에 대한 변경 사항을 롤백했습니다.                                                                                            |
| 이동 및 경비                | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 소스 문서 라인 생성 및 업데이트를 지원하기 위해 경비 보고서의 특정 지점에 로깅이 추가되었습니다.                                                                                           |
| 이동 및 경비                | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 판매세가 대상 법인에 전기되는 경우 본지사 시나리오에 잘못된 보조 원장 분개가 제공됩니다.                                              |
| 이동 및 경비                | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations에서 지출 추정치는 재무에서 삭제될 때 Dataverse에서 삭제되지 않습니다.                                                                                         |
| 이동 및 경비                | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 경비 범주가 비 프로젝트 범주인 경우 **경비** 페이지에 선택된 재무 차원은 경비 보고서에 복사되지 않습니다.                                          |

### <a name="regulatory-updates"></a>규제 업데이트
금융 및 운영 앱의 규정 업데이트에 대한 자세한 내용은 [규정 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
