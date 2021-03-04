---
title: 연방지원금 지출계획 조회
description: 이 항목은 연방지원금 지출계획 조회에 대한 정보를 제공합니다.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080036"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>연방지원금 지출계획 조회

[!include [banner](../includes/banner.md)]

관리 예산처 회람 A-133에 따르면, 연방 기금을 받는 기관은 단일 감사라고도 하는 감사 요건의 적용을 받습니다. 감사 프로세스는 연방 지원금의 수입 및 지출을 반복적으로 보고하는 데 사용됩니다. 단일 감사 보고서에는 SEFA(연방지원금 지출계획)가 포함됩니다.

연방지원금 지출계획 조회에는 연방 정부 지원 목록(CFDA) 제목과 번호, 보조금 번호, 보조금 연도, 보조금을 제공하는 연방 기관 이름 및 도관 기업(pass-through entity)의 이름이 포함됩니다. 조회는 특정 기간 동안 가능합니다. 일반적으로 이 기간은 회계 연도인 재무 제표 기간과 동일합니다.

조회에는 선택한 날짜 범위의 예상 날짜가 있는 보조금이 포함됩니다. 조회의 **교부 기관** 열에는 보조금 고객 또는 도관 보조금의 경우 교부 기관이 표시됩니다. 도관 보조금의 경우 **도관 기관** 열에는 보조금 고객이 표시됩니다. 보조금이 도관 보조금이 아닌 경우 **도관 기관** 열은 비어 있습니다.

## <a name="set-up-the-cfda-clusters"></a>CFDA 클러스터 설정

연방지원금 지출계획 조회의 CFDA 번호와 연관될 수 있는 CFDA 클러스터를 설정해야 합니다.

1. **프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 연방 정부 지원 목록 클러스터** 로 이동합니다.
2. **새로 만들기** 를 선택하여 CFDA 클러스터를 만듭니다.
3. 클러스터 이름을 입력합니다.
4. **저장** 을 선택하여 변경 내용을 저장합니다.

## <a name="set-up-cfda-numbers"></a>CFDA 번호 설정

보조금에 추가할 수 있는 CFDA 번호를 설정하고 연방지원금 지출계획 조회에 포함해야 합니다.

1. **프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 연방 정부 지원 목록 번호** 로 이동합니다.
2. **새로 만들기** 를 선택하여 CFDA 번호를 만듭니다.
3. **번호** 열에 CFDA 번호를 입력합니다.
4. **Tab** 키를 누릅니다.
5. **설명** 열에 CFDA 제목을 입력합니다.
6. **Tab** 키를 누릅니다.
7. 선택 사항: **프로그램 클러스터** 필드에서 적절한 CFDA 클러스터를 추가합니다.
8. **저장** 을 선택하여 변경 내용을 저장합니다.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>연방지원금 지출계획 조회에 대해 보고할 보조금 설정

1. **프로젝트 관리 및 회계 \> 보조금 \> 보조금** 으로 이동하고 기존 보조금을 선택합니다.
2. **설정** 빠른 탭의  **연방 정부 지원 목록** 필드에서 CFDA 번호를 할당합니다. 보조금의 CFDA 번호는 보고할 CFDA 클러스터를 결정합니다.
3. **연락처 정보** 빠른 탭에서 다음 단계에 따라 교부 기관 정보를 입력합니다.

    1. **보조금 고객** 필드에 보조금을 담당하는 고객을 입력합니다. 기존 보조금의 경우 이 정보가 이미 입력되었을 수 있습니다.
    2. 보조금 고객이 자금 제공자인지 여부를 표시합니다. 보조금 고객이 자금 제공자인 경우 **도관** 확인란을 선택 취소 상태로 둡니다. 다른 고객이 자금 제공자이고 보조금 고객이 자금 지출 및 추적을 담당하는 경우 **도관** 확인란을 선택합니다.

4. 이전 단계에서 **도관** 확인란을 선택한 경우 **교부 기관** 필드에 보조금을 제공한 고객을 입력합니다. 교부 기관과 보조금 고객은 동일한 고객일 수 없습니다.

다음은 도관 보조금의 예입니다.

연방 정부가 주를 위한 인프라 프로젝트에 자금을 지원했습니다. 연방 정부가 주에 지출할 자금을 제공했습니다. 이 경우 연방 정부가 교부 기관이고 주가 보조금 고객입니다.

> [!NOTE] 
> 이 기능을 처음 켜면 보조금에 있는 기존 번호를 사용하여 초기 CFDA 번호가 입력됩니다.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>보조금 유형에 따라 SEFA 보고에서 보조금 제외

1.  **프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 보조금 유형** 으로 이동합니다.
2.  **기본 정보** 빠른 탭에서  **연방지원금 지출계획에서 제외** 확인란을 선택합니다.
3. **저장** 을 선택하여 변경 내용을 저장합니다.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>연방지원금 지출계획 조회 실행

1. **프로젝트 관리 및 회계 \> 조회 및 보고 \> 보조금 조회 \> 연방지원금 지출계획** 으로 이동합니다.
2. **매개 변수** 에서 다음 단계를 수행합니다.

    1. **날짜 간격** 필드에서 날짜 간격에 대한 코드를 선택합니다. 또는 **시작 날짜** 및 **종료 날짜** 필드에서 날짜 간격을 정의합니다.
    2. 선택 사항: 청구된 트랜잭션만 조회에 수익으로 포함하려면 **청구된 수익만 포함** 옵션을 **예** 로 설정합니다.

## <a name="columns"></a>열

연방지원금 지출계획 조회에는 다음 열이 포함됩니다.

- 연방 정부 지원 목록 클러스터 이름
- 교부 기관
- 도관 기관
- 보조금 이름
- 보조금 ID
- 보조금 신청 ID
- 연방 정부 지원 목록
- 영수증
- 지출


[!INCLUDE[footer-include](../includes/footer-banner.md)]