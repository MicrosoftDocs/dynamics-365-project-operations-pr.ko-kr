---
title: 경비 관리 매개 변수
description: 다음 매개 변수는 경비 관리의 동작을 제어합니다.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: af49187a3ad530919376fbfdb5a0fbc288b7c28c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080096"
---
# <a name="expense-management-parameters"></a>경비 관리 매개 변수

[!include [banner](../includes/banner.md)]

-----------------------------

매개 변수는 경비 관리의 일반 동작을 제어합니다.

### <a name="general"></a>일반

| **필드**                                                | **설명**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **표준 마일리지 비율**                             | 마일리지 경비 상환 비율을 입력합니다. 여행 경비로 환급되는 금액을 계산하기 위해 요금에 경비에 입력된 마일리지를 곱합니다.                       |
|**지급된 개인 경비**                             | 개인으로 분류된 신용 카드 거래 금액을 지불할 책임이 있는 사람을 선택합니다.                                                                                                     |
|**드릴백에 대한 전체 경비 보고서 표시**               | 경비 보고서가 전기될 때 생성된 특정 바우처에 대한 원본 문서의 세부 사항을 볼 때 경비 보고서에 대한 모든 경비를 표시하려면 이 옵션을 선택합니다.              |
|**여행 사전 승인은 필수입니다.**                 | 직원이 경비 보고서를 제출하기 전에 출장 요청을 제출하고 승인하도록 하려면 이 옵션을 선택합니다.                                                                    |
|**전기하기 전에 배포 편집 허용**            | 경비 보고서 배포를 전기하기 전에 편집할 수 있는지 여부를 선택합니다.                                                                                                                 |
|**경비 관리 정책 평가**                     | 경비 정책 위반 여부를 판별하기 위해 경비 평가 시기를 선택합니다. 경비 항목을 입력하고 저장하거나 경비를 승인을 위해 제출할 때 위반에 대해 경비를 확인할 수 있습니다. 필요한 영수증에 대한 정책 규칙은 경비 라인이 저장될 때 확인됩니다.                   |
|**회사간 경비 라인 허용**                         | 경비 보고서 내에 다른 법인의 경비를 입력할 수 있는지 여부를 선택합니다.                                                                                                          |
|**신용 카드 경비에 대한 환율 편집 허용** | 사용자가 가져온 신용 카드 경비의 환율을 편집할 수 있도록 하려면 이 옵션을 선택합니다.                                                                        |
|**표시할 멀티레벨 계층 구조 필드**                  | 경비 보고서 워크플로 할당 유형이 계층으로 설정되고 계층 선택이 경비 멀티레벨 승인 계층을 사용하도록 설정된 경우 표시할 승인자 필드를 선택합니다. 워크플로에 멀티레벨 승인 계층 구조가 사용되는 경우 선택한 필드가 경비 보고서에 표시되고 편집할 수 있습니다. |
|**직원 신용 카드 번호 입력(2017년 7월 업데이트)**     | 직원용 **신용 카드** 페이지의 **카드 ID** 필드에 15자 또는 16자리 숫자를 입력하고 저장할 수 있는지 여부를 선택합니다.                                                                          |

### <a name="financial"></a>금융업

| **필드**                                                            | **설명**     |
|----------------------------------------------------------------------|------------------------------------|
|**원장 일일 분개장 이름**                                         | 승인된 경비 보고서가 전기되는 원장 분개장 이름을 선택합니다.            |
|**경비에서 세금 공제 가능**                                  | 적격 경비에 대한 경비 세금 공제를 활성화하려면 이 옵션을 선택합니다. 미국 판매세 및 사용세 규칙이 활성화된 경우 이 옵션을 활성화할 수 없습니다.      |
|**즉시 현금 서비스 전기**                                     | 지급 및 이체 프로세스가 완료될 때 승인된 현금 서비스를 전기하려면 이 옵션을 선택합니다. 이 옵션을 선택하지 않으면 지급 및 이체 프로세스에서 전기되지 않은 일반 분개장이 생성됩니다. |
|**전기 중 정확한 회계 날짜**                             | 현재 기간이 보류 중이거나 마감된 경우 경비가 전기될 때 회계 일자를 갱신하려면 이 옵션을 선택합니다. 회계 날짜는 다음 개설 기간으로 설정됩니다.   |
|**결제 방법에 지정된 상쇄 계정을 기반으로 거래 그룹화 허용**      | 경비에 대한 결제 방법에 지정된 상쇄 계정을 기반으로 경비 보고서에 대한 경비 트랜잭션을 요약하려면 이 옵션을 선택합니다.   
|**세금 포함**                                                   | 기본적으로 경비 금액에 판매세를 포함하려면 이 옵션을 선택합니다.             |
|**출장 요청 마감 시 처분 제한 해제**            | 승인된 출장 요청이 마감될 때 처분 제한 자금을 해제하려면 이 옵션을 선택합니다.                                                                                   |
|**예산 등록 및 프로젝트 예산에 대한 예산 초과시 출장 요청 제출 허용** | 직원이 예산 등록부에 설정된 허용 예산이나 프로젝트에 허용된 예산을 초과하는 승인을 위해 출장 요청을 제출할 수 있도록 하려면 이 옵션을 선택합니다.            |
|**예산 등록 및 프로젝트 예산에 대한 예산 초과시 경비 보고서 제출 허용**    | 직원이 예산 등록에 설정된 허용 예산이나 프로젝트에 허용된 예산을 초과는 승인을 위해 경비 보고서를 제출할 수 있도록 하려면 이 옵션을 선택합니다.                |
|**예산 등록의 경우에만 예산 초과시 경비 보고서 승인 허용**                | 승인자가 예산 등록에 설정된 허용 예산을 초과하는 경비 보고서를 승인할 수 있도록 하려면 이 옵션을 선택합니다.                                                                       |

### <a name="per-diem"></a>일비

| **필드**                             | **설명**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**일비에 대한 최소 시간**           | 출장 관련 경비에 대해 일비를 받기 위해 직원이 하루에 일해야 하는 기본 최소 시간을 입력합니다.  이 값은 일비 요율 계층의 최소 시간 필드의 경우에만 기본값으로 사용됩니다.                                                                                      |
|**식사 비율**                          | **다음으로 식사 감소 계산** 필드가 **하루 식사 유형** 또는 **하루 식사 횟수** 중 하나로 설정되면 출장 관련 경비의 첫날과 마지막 날에 사용되는 식사에 대한 일비 기본 비율을 입력합니다. 첫날과 마지막 날의 근무일은 표준 근무일보다 짧을 수 있습니다. 따라서, 이러한 날의 일비 금액은 표준 금액과 다를 수 있습니다. 비율이 0(영)으로 설정된 경우 첫날과 마지막 날의 공제는 0.00이 됩니다. |
|**호텔 비율**                        | 출장 관련 비용의 첫날과 마지막 날에 사용되는 호텔의 일비 기본 비율을 입력합니다. 첫날과 마지막 날의 근무일은 표준 근무일보다 짧을 수 있습니다. 따라서, 이러한 날의 일비 금액은 표준 금액과 다를 수 있습니다. 비율이 0(영)으로 설정된 경우 첫날과 마지막 날의 공제는 0.00이 됩니다.                                              |
|**기타 비율**                        | 출장 관련 비용의 첫날과 마지막 날에 사용되는 기타 경비의 일비 기본 비율을 입력합니다. 첫날과 마지막 날의 근무일은 표준 근무일보다 짧을 수 있습니다. 따라서, 이러한 날의 일비 금액은 표준 금액과 다를 수 있습니다. 비율이 0(영)으로 설정된 경우 첫날과 마지막 날의 공제는 0.00이 됩니다.                                                                                                     |
|**아침 식사 비율 감소** | 아침 식사로 일비가 감소되는 금액을 입력합니다. 예를 들어, 직원이 무료 아침 식사를 받는 경우 일비 금액을 10% 줄일 수 있습니다.                               |
|**점심 식사 비율 감소**    | 점심 식사로 일비가 감소되는 금액을 입력합니다. 예를 들어, 직원이 무료 점심 식사를 받는 경우 일비 금액을 15% 줄일 수 있습니다.                                       |
|**저녁 식사 비율 감소**   | 저녁 식사로 일비가 감소되는 금액을 입력합니다. 예를 들어, 직원이 무료 저녁 식사를 받는 경우 일비 금액을 25% 줄일 수 있습니다.                                     |
|**다음으로 식사 감소 계산**         | 감소가 여행 당 또는 일일 식사 유형을 기반으로 하는지 또는 하루에 허용되는 식사 수를 기반으로 하는지 여부를 선택하여 시스템에서 일비 식사 감소를 계산하는 방법을 지정합니다.|
|**일비 반올림**                  | 일비 경비에 사용되는 반올림 유형을 선택합니다. 일반 반올림을 선택하면 금액이 0.50인 일비 경비는 1.00으로 반올림되고, 금액이 0.50 미만인 일비 경비는 0.00으로 반내림됩니다.                                                                                              |
|**일비 계산 기준**         | 일비 금액이 역일 기준인지 24시간 기준인지 선택합니다.       |

### <a name="fax-cover-pages"></a>팩스 표지

| **필드**                      | **설명**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **설명**                   | 직원이 경비 보고서와 관련된 영수증을 보내는 데 사용되는 팩스 표지를 만들 때 따라야 하는 지침을 입력합니다. 사용자 언어에 따라 표시될 언어별 텍스트를 입력하려면 **번역** 단추를 클릭합니다. |
|**사용자 ID(바코드 정보)** | 팩스 표지에 사용되는 바코드에 직원의 고유 식별자를 저장하려면 이 옵션을 선택합니다.                 |
|**바코드**                      | 팩스 표지에 사용되는 바코드를 선택합니다. 경비 관리에서는 바코드 39 및 128이 지원됩니다.               |

### <a name="anti-corruption"></a>반부패

|                 <strong>필드</strong>                 |                                                                                                                                                                                            <strong>설명</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>반부패 증명 표시</strong>  | 새 경비 보고서를 생성할 때 반부패 텍스트를 표시하려면 이 옵션을 선택합니다. 그런 다음 경비 보고서에서 반부패 증명을 선택해야 하는 경우 특정 경비 범주를 활성화할 수 있습니다. 예를 들어, 공무원 경비와 관련된 선물 범주의 경우 직원이 경비가 공무원과 관련된 회사 정책을 충족하는지 확인해야 할 수 있습니다. |
| <strong>제출자를 위한 반부패 메시지</strong> |                                                                                             새 경비 보고서를 생성할 때 직원에게 표시될 텍스트를 입력합니다. 사용자 언어에 따라 표시될 언어별 텍스트를 입력하려면 <strong>번역</strong> 단추를 클릭합니다.                                                                                             |
| <strong>승인자를 위한 반부패 메시지</strong>  |                                                                                             새 경비 보고서를 생성할 때 승인자에게 표시될 텍스트를 입력합니다. 사용자 언어에 따라 표시될 언어별 텍스트를 입력하려면 <strong>번역</strong> 단추를 클릭합니다.                                                                                             |
