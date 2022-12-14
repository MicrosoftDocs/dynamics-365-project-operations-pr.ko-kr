---
title: 2022년 11월의 새로운 기능 - Project Operations Lite 배포
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations Lite 배포의 2022년 11월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831116"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>2022년 11월의 새로운 기능 - Project Operations Lite 배포

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.58.0.119의 Project Operations


## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2781818 | 자재 사용 로그의 가격을 기본값으로 설정하는 동안 키를 찾을 수 없는 오류가 발생했습니다. |
| 청구 및 가격 책정 | 2922373 | 견적 손실로 종료된 프로젝트에 견적 라인을 연결할 수 없습니다. |
| 청구 및 가격 책정 | 2943206 | 프로젝트 엔터티의 **계약 라인** 필드는 선택 사항이어야 합니다. |
| 청구 및 가격 책정 | 2953182 | 송장 수정에 대한 오류 메시지를 개선합니다.|
| 청구 및 가격 책정 | 2959500 | 손실된 견적과 이미 연결된 프로젝트 작업에 견적 라인을 연결할 수 없습니다.|
| 청구 및 가격 책정 | 2959560 | 특정 로케일에서 낙찰된 견적을 마감하는 동안 "이 고객은 이미 프로젝트 계약에 있습니다" 메시지가 수신되었습니다. |
| 청구 및 가격 책정 | 3031727 | 필수 필드 'msdyn_Company' is missing 오류로 인해 리소스 할당이 실패합니다. |
| 청구 및 가격 책정 | 3036905 | 소유 회사는 ProjectTeamMember에서 초기화되지 않습니다. |
| 영업 기회 관리 | 2763519 | EnsureProjectContractAllowsUpdates의 Null 참조 오류입니다. |
| 영업 기회 관리 | 2783798 | 견적 라인에서 프로젝트 견적을 가져올 때 비용 및 자재 견적에 대한 작업 설명이 누락됩니다.|
| 영업 기회 관리 | 2988635 | 견적에서 고객을 삭제할 때 오류 메시지 설명을 개선합니다. |
| 영업 기회 관리 | 3001191 | 청구 방법이 null로 지정된 기회에서 견적을 생성할 수 없습니다. |
| 업그레이드 | 3012324 | 이름에 Tab과 같은 제어 문자가 있는 프로젝트에서 프로젝트 변환에 실패했습니다. || 프로젝트 계획 및 추적 | 2790384 | Pending OperationSet 시간 제한이 너무 짧습니다. |
| 프로젝트 계획 및 추적 | 3044275 | 누락된 현지화: missingProjectSchedulerErrorMessage. |
| 프로젝트 계획 및 추적 | 3044277 | 스케줄러가 설정되지 않은 경우 Project Recon 그리드가 로드되지 않습니다.|
| 리소스 관리 | 2943153 | 추적 탭을 업데이트하여 기간에 대한 소수점 이하 두 자리를 표시합니다.|
| 하도급 계약 | 2932774 | 공급업체 송장 라인 읽기 전용 오류가 잘못 발생합니다. |
| 하도급 계약 | 2939556 | 공급업체 송장 헤더 상태는 활성 상태가 아닌 경우 초안 온라인 삭제로 설정하면 안 됩니다. |
| 시간 및 경비 | 2939998 | ProjOps에서 새로운 TESA 버전을 활용하세요. |
