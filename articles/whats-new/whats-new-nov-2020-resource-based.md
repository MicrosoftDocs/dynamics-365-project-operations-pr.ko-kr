---
title: 2020년 11월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2020년 11월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f8e9bce6612e617785264470b7946ffc4795a621
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291852"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020년 11월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- CDS 환경 버전 4.4.0.70의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.14의 프로젝트 관리 및 회계

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>리소스/비 재고 기반 시나리오에 대한 Project Operations로 업데이트

### <a name="project-operations-on-cds"></a>CDS의 Project Operations

| 기능 영역                 | 참조 번호 | 품질 업데이트                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  영업 기회 관리       | 2036993          | 견적 라인 유형이 **모든 작업** 일 때 낙찰 견적에서 추정 라인 및 리소스 지정 계약 내용이 업데이트됩니다.                                                 |
| 청구 및 가격 책정          | 2070392          | 송장의 프로젝트 계약 내용은 **송장 트랜잭션 새로 고침** 을 선택할 때마다 증가합니다.                                                                         |
| 프로젝트 계획             | 2043336          | 프로젝트 팀 구성원 레코드를 삭제할 수 없습니다.                                                                                                                                  |
| 프로젝트 계획             | 2046013          | 로드 중 또는 시간 단계 유형 변경시 태그 열 추정에 대한 일관되지 않은 동작.                                                                                   |
| 프로젝트 계획             | 2046647          | 프로젝트 팀 구성원으로부터 리소스 요구 사항이 생성되면 시작 및 종료 시간이 한 시간씩 단축됩니다.                                                                      |
| 프로젝트 계획             | 2053879          | (예정된 CDS 롤아웃에 따라) PublishUnassignedAssignments는 "ConditionOperator.In에 전달된 값이 비어 있습니다."라는 오류가 발생하면 작업 저장 시도를 중단합니다.                       |
| 프로젝트 계획             | 2055501          | **프로젝트 시작 날짜** 가 비어 있으면 일정이 실패합니다.                                                                                                      |
| 프로젝트 계획             | 2066817          | **작업** 탭의 인물 선택기를 사용하여 일반 리소스를 만들 수 없습니다.                                                                                                   |
| 프로젝트 계획             | 2067034          | **작업 세부 정보** 페이지에서는 **세부 정보 보기** 단추를 사용할 수 없습니다.                                                                                                       |
| 리소스 관리          | 2046667          | 모든 리소스가 충족된 후에도 일반 팀 구성원은 삭제되지 않습니다.                                                                                                    |
| 시간 및 빠른 경비 입력 | 2047499          | 시간 입력 페이지에서 **새로 만들기** 단추를 클릭하면 **새 이메일 서명** 페이지가 열립니다.                                                                                               |
| 시간 및 빠른 경비 입력 | 2059859          | 경비 항목을 생성할 때 예기치 않은 팝업이 열립니다.                                                                                                                         |
| 기타                        | 2044181          | (구매 주문서 제거) msdyn_ProjectServiceCore_Patch 및 msdyn Project 서비스 핵심 솔루션을 제거하려고 하면 "레코드를 사용할 수 없습니다"라는 오류가 발생합니다.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계 개요

| 기능 영역        | 참조 번호 | 품질 업데이트                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 수익 인식 | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | 계약이 외화를 사용하고 완료 방법에 대한 작업 진행률을 사용하는 경우 프로젝트 예상 완료율이 잘못되었습니다.                     |
| 수익 인식 | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | **실제 비용** 완료 방법으로 추정을 전기할 수 없습니다.                                                                                                    |
| 수익 인식 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 회사 통화와 트랜잭션 통화가 다른 경우 바우처 불균형 오류로 인해 제거가 실패합니다.                                              |
| 경비 관리  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | 관리자가 아닌 사용자의 경우 **프로젝트 ID** 와 **경비 범주** 같은 경비 라인 열에 대한 조회 값이 데이터 커넥터 프레임에 올바르게 표시되지 않습니다. |
| 경비 관리  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | 경비 범주에 대해 라인 속성 기본값이 표시되지 않습니다.                                                                                                         |
| 경비 관리  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | 경비 통합에는 경비 보고서의 라인 속성이 포함되어야 합니다.                                                                                             |
| 송장 발행           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | FD 조합의 유효성을 확인하지 않았다는 오류 메시지로 인해 프로젝트 송장 제안을 전기할 수 없습니다.                                                    |
| 송장 발행           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | **송장** 세부 정보 페이지에서 트랜잭션을 볼 수 없습니다.                                                                                                              |
| 송장 발행           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | 송장 제안 라인을 삭제할 수 있습니다.                                                                                                                                  |
| 프로젝트 회계  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **예측** 메뉴 항목을 **프로젝트** 목록 페이지에서 볼 수 없습니다.                                                                                                   |
| 프로젝트 회계  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **프로젝트 명세서**   > **트랜잭션 및 예측** 을 열 수 없습니다.                                                                                                       |
| 프로젝트 회계  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **회계 조정** 은 송장 청구된 프로젝트 트랜잭션에는 사용할 수 없습니다.                                                                                                  |
| 프로젝트 회계  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | 회계 세부 사항은 **통합** 분개장이 전기될 때 **ProjCDSActualsImport** 테이블에 포함되지 않습니다.                                                  |
| 프로젝트 회계  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 프로젝트 예측 항목은 리소스 할당을 제거한 다음 읽을 때 두 배가 됩니다.                                                                            |
| 프로젝트 회계  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | 프로젝트 ID 링크를 선택해도 CDS 딥 링크 URL이 열리지 않습니다.                                                                                                         |
| 프로젝트 회계  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | CDS에서 작업의 시작 날짜를 업데이트할 수 없습니다.                                                                                                                           |
| 프로젝트 회계  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | 이 기능을 활성화하면 CDS 통합 없이는 여러 계약 내용이 불가능합니다.                                                                                   |

### <a name="regulatory-updates"></a>규제 업데이트
Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]