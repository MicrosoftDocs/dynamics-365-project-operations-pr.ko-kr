---
title: Project Service Automation에서 Project Operations로의 기능 변경 사항
description: 이 문서에서는 Project Service Automation에서 Dynamics 365 Project Operations로 변경된 기능에 대한 개요를 제공합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925358"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Project Service Automation에서 Project Operations로의 기능 변경 사항

Dynamics 365 Project Service Automation에서 Dynamics 365 Project Operations Lite로의 업그레이드는 3단계로 제공됩니다. 이 문서는 업그레이드가 완료될 때 예상할 수 있는 주요 변경 사항에 대한 정보를 제공합니다.

| 업그레이드 전달 | 1단계 <br>(2022년 1월) | 2단계 <br>(2022년 4월 웨이브) | 3단계  |
|------------------|------------------------|---------------------------|---------------------------|
| 프로젝트의 작업 분할 구조(WBS)에 대한 종속성 없음. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS는 현재 지원되는 Project Operations 제한에 포함됩니다. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client에 대한 지원을 포함하여 현재 지원되는 Project Operations 한도를 벗어난 WBS. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>프로젝트 관리

사용자 경험에서 가장 중요한 변화는 프로젝트 계획 영역입니다. Project Operations는 [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5)에서 제공하는 일정 기능을 활용하여 작업 분할 구조(WBS)를 관리하기 위한 새로운 현대적 경험을 채택합니다.

## <a name="differences-in-the-scheduling-experience"></a>스케줄링 환경의 차이점

다음 표에는 Project Service Automation과 Project Operations 간의 일정 차이가 요약되어 있습니다.

|  일정 예약     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| 프로젝트 템플릿 - 프로젝트 생성 시 프로젝트 템플릿을 정의하고 적용하는 기능  |  &nbsp;    | :heavy_check_mark: |
| 데스크톱 클라이언트와 프로젝트 작업 분할 구조(WBS) 통합   |    &nbsp;  | :heavy_check_mark: |
| 제약 조건 - 다음 시간 이전에 시작하지 않고 다음 시간 이후에 종료하지 않음  | :heavy_check_mark: |   &nbsp;  |
| 이정표 - 기간이 0인 작업   | :heavy_check_mark:  |  &nbsp;  |
| 리소스 기반 작업은 할당된 리소스의 가용성을 존중합니다.   | :heavy_check_mark: |  &nbsp;    |
| 시간 단계별 편집 - 계획을 편집하고 매일 작업합니다.   |   &nbsp;  | :heavy_check_mark: |
| 자동/수동 스케줄링 - 프로젝트 스케줄링 엔진을 사용하여 작업을 자동 또는 수동으로 스케줄링 |  &nbsp; | :heavy_check_mark:  |
| 사용자 인터페이스에서 직접 대규모 프로젝트 편집: 편집 가능한 계획의 크기에는 제한이 없음  | 500개 작업 제한  | :heavy_check_mark:       |
| 완료율 - 작업 진행률 표시   | :heavy_check_mark:  |  &nbsp;  |
| [프로젝트 일정 모드](../project-management/scheduling-modes.md) - 프로젝트를 고정 단위, 고정 노력 또는 고정 기간으로 정의 | :heavy_check_mark: | &nbsp; |
| 타임라인 - 타임라인 보기를 구축 및 사용자 지정하여 일정 세부 정보를 시각화하고 이해 관계자와 소통합니다. | :heavy_check_mark:  | &nbsp; |
| 노력 기반 작업 - 작업을 노력 기반으로 스케줄링하기 위한 스케줄링 엔진 지원  | :heavy_check_mark:  | &nbsp; |
| **작업 정보** 대화 상자 - 대화 상자를 사용하여 작업 세부 정보 저장 | :heavy_check_mark:  |  &nbsp;  |
| 끌어서 놓기 - 작업을 여러 개 선택하고 WBS에서 위치를 수정 | :heavy_check_mark: | &nbsp;  |
| 유연한 영구 보기 - 작업 속성에 대한 보다 세분화된 보기 정의   | :heavy_check_mark:  | &nbsp; |
| WBS 정렬 및 필터링  | :heavy_check_mark:  | &nbsp; |
| 비 폭포형 프로젝트 납품에 대한 보드 보기  | :heavy_check_mark:   | &nbsp; |
| 타임라인 보기 - WBS를 시각화하고 편집하는 데 사용되는 대화식 Gantt 차트   | :heavy_check_mark:  | &nbsp; |
| 키보드 단축키 - 들여쓰기 또는 삽입과 같은 일반적인 작업에 키보드 단축키를 사용  | :heavy_check_mark:  |  &nbsp; |
| 다단계 실행 취소 - 전체 작업 집합을 되돌리고 다시 적용하여 변경의 영향을 완전히 이해하기 위해 가정 분석을 수행 | :heavy_check_mark: | &nbsp; |
| 잘라내기/복사/붙여넣기 - 애플리케이션 간 일정 내역 복사 및 붙여넣기를 통한 일정 개발 협업  | :heavy_check_mark: | &nbsp; |
| 작업 체크리스트 - 작업에 최대 20개의 체크리스트 항목 추가   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>프로젝트 계획

Project Operations의 **프로젝트** 페이지는 Project Service Automation의 **프로젝트** 페이지와 비교해 상당한 차이가 있습니다.

다음 작업은 1단계 업그레이드의 일부로 **프로젝트** 페이지에서 제거되었습니다.

  - **MS Project에서 열기**
  - **템플릿 만들기**
  - **MS Project에서 연결 해제**

Project Operations의 **프로젝트** 페이지에는 다음과 같은 새 탭이 포함됩니다.

- **예상 재료**
- **작업 청구 설정**

**상태** 탭이 제거되었으며 **상태** 필드는 이제 프로젝트의 일정 모드가 있는 **요약** 탭에 있습니다.

   ![프로젝트 페이지로 업데이트합니다.](media/projectform.png)

**일정** 탭의 이름이 **작업** 탭으로 변경되었으며 Project for the Web으로 새로운 프로젝트 계획 환경을 제공합니다.

   ![새 프로젝트 작업 탭.](media/tasktab.png)

## <a name="scheduling-modes"></a>예약 모드

Project Operations에 새로운 기능인 [예약 모드](../project-management/scheduling-modes.md)가 도입되었습니다. 기존의 모든 Project Service Automation 프로젝트는 기본적으로 Project Operations에서 **고정 기간** 으로 설정됩니다. 그러나 새 프로젝트의 기본값은 **설정** > **매개변수** > **매개변수** > **일정 예약 모드** 로 이동하여 관리할 수 있습니다.

   ![일정 예약 모드에 대한 프로젝트 매개 변수 설정.](media/projectparameter.png)

## <a name="project-planning-limits"></a>프로젝트 계획 제한

Project Operations는 모든 프로젝트 일정 작업을 위해 Project for the Web에 의존합니다. Project for the Web은 다음 표의 제한을 사용하여 작업 분할 구조를 관리합니다.

| **필드**                                          | **한도**             |
|----------------------------------------------------|-----------------------|
| 프로젝트의 최대 총 작업                  | 500                   |
| 프로젝트의 최대 총 기간               | 3650일(10년)  |
| 프로젝트의 최대 총 리소스              | 300                   |
| 프로젝트에 대한 최대 총 링크(후속자만 해당) | 600                   |
| 프로젝트의 최대 총 사용자 지정 필드          | 10                    |
| 최대 계층 구조 수준                            | 10 레벨             |
| 최대 링크(후속 업무 + 선행 업무)            | 20                    |
| 리프 작업의 최대 기간                      | 1250일             |
| 요약 작업의 최대 기간                 | 3650일(10년)  |
| 작업에 할당된 최대 리소스               | 20개 리소스          |
| 작업에 지원되는 날짜 범위                    | 1/1/2000 - 12/31/2149 |
| 검사 목록 항목                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>프로젝트 계획 확장 및 개발

Project Operations로 업그레이드한 후 프로젝트 일정 API를 사용하여 다음 엔터티에서 생성, 업데이트 및 삭제 작업을 실행해야 합니다.

|   엔터티 이름           |   엔터티 논리적 이름       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| 프로젝트 작업            | msdyn_projecttask           |
| 프로젝트 작업 종속성 | msdyn_projecttaskdependency |
| 리소스 할당     | msdyn_resourceassignment    |
| 프로젝트 버킷          | msdyn_projectbucket         |
| 프로젝트 팀 구성원     | msdyn_projectteam           |

현재 이러한 엔터티와 관련된 사용자 지정이 있는 경우 구현 지침은 [프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행](../project-management/schedule-api-preview.md)을 참조하십시오.

## <a name="data-model-changes"></a>데이터 모델 변경

업그레이드 단계 1의 일부로 데이터 모델에 변경 사항이 있습니다. 이러한 변경 사항은 주로 기존 엔터티에 대한 필드 변경 사항입니다. 1단계에서 엔터티 **msydn_project** 및 **msdyn_projectteam** 은 사용자 정의의 리팩토링입니다. 

> [!IMPORTANT]
> 이 섹션은 향후 업그레이드 단계가 완료되면 추가 엔터티로 업데이트됩니다.

다음 필드는 새 필드로 대체되었습니다.

|   Entity          |   기존 논리적 이름   |   새 논리적 이름    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

다음 필드가 추가되었습니다.

|   Entity          |   논리적 이름                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | 프로젝트 실제 요금 판매의 집계된 비용을 표시합니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_actualmaterialcost                     | 프로젝트 실제 재료 비용의 집계된 비용을 표시합니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_actualmaterialsales                    | 프로젝트 실제 재료 판매의 집계된 비용을 표시합니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | 이 프로젝트에 연결된 계약 내용입니다. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | 상관 관계 식별자와 관련된 **프로젝트 복사** 에 사용되는 내부 시스템 필드입니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_copyprojectsessionid                   | 세션 식별자와 관련된 **프로젝트 복사** 에 사용되는 내부 시스템 필드입니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_globalrevisiontoken                    | 프로젝트 일정 서비스의 마지막 동기화 xRM 글로벌 개정 토큰입니다. |
| msdyn_project     | msdyn_msprojectdocument                      | 프로젝트에 속한 Microsoft Project 문서입니다. |
| msdyn_project     | msdyn_plannedmaterialcost                    | 프로젝트에 대한 예정된 재료 비용의 집계입니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_plannedmaterialsales                   | 프로젝트에 대한 예정된 재료 판매의 집계입니다. Project Service Automation에서만 사용합니다. |
| msdyn_project     | msdyn_program                                | 이 프로젝트와 관련된 프로그램입니다. |
| msdyn_project     | msdyn_quotelineproject                       | 이 프로젝트에 연결된 견적 라인입니다. |
| msdyn_project     | msdyn_replaylogheader                        | 재생 로그의 머리글입니다. |
| msdyn_project     | msdyn_schedulemode                           | 프로젝트의 모든 작업에 사용되는 기본 일정 예약 모드입니다.  |
| msdyn_project     | msdyn_taskearlieststart                      | 프로젝트에서 작업의 가장 빠른 시작 날짜입니다.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 이 프로젝트 팀 구성원이 복사된 프로젝트 팀 구성원입니다. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | 새로 만든 일반 팀 구성원에 대한 리소스 요구 사항을 만들지 여부를 나타냅니다.  |
| msdyn_projectteam | msdyn_deletestatus                           | 프로젝트 일정 서비스에 삭제 요청이 전송되었는지와 예상 시간 창 내에 성공적으로 응답을 다시 보내는지 추적할 팀 구성원의 삭제 상태입니다. |
| msdyn_projectteam | msdyn_effortcompleted                        | 팀 구성원이 수행한 할당된 작업량을 추적합니다. |
| msdyn_projectteam | msdyn_effortremaining                        | 할당에 대해 팀 구성원이 아직 완료하지 못한 작업량을 추적합니다. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | 팀 구성원이 프로젝트 일정 서비스에 삭제 요청을 보낸 후 Microsoft Dataverse에서 팀 구성원이 실제로 삭제될 때까지의 대기 기간입니다.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | 팀 구성원 삭제 요청이 프로젝트 일정 서비스로 전송될 때 기록할 타임스탬프입니다. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 이 프로젝트 팀 구성원이 복사된 프로젝트 팀 구성원을 표시합니다.  |

## <a name="project-templates"></a>프로젝트 템플릿

Project Operations는 프로젝트 템플릿에 대한 지원을 제공하지 않습니다. 그러나 [프로젝트 복사 API](../project-management/dev-copy-project.md)를 사용하여 많은 핵심 기능을 복제할 수 있습니다.

## <a name="desktop-add-in-support"></a>데스크탑 추가 기능 지원

Microsoft Project 데스크톱 추가 기능에 대한 지원은 업그레이드의 처음 2단계에서 사용할 수 없습니다. 3단계에서 현재 지원되는 Project for the Web 제한보다 큰 프로젝트가 있는 고객은 데스크톱 추가 기능을 사용할 수 있습니다.

## <a name="editing-resource-assignment-contours"></a>리소스 할당 윤곽 편집

리소스 할당 윤곽을 편집하는 기능은 업그레이드 2단계를 사용할 수 있을 때 사용할 수 있습니다.

## <a name="billing-and-pricing"></a>청구 및 가격 책정

Project Operations에 다음과 같은 새로운 기능이 추가되었습니다. 이러한 기능은 본질적으로 추가적이며 Project Service Automation 데이터 모델에 영향을 주지 않습니다.

- [프로젝트 및 프로젝트 작업에 대한 재료 사용량 기록](../material/material-usage-log.md)
- [하도급 계약 관리](../pro/subcontracting/managing-subcontracts-overview.md)
- [선급금 및 보유자 기반 계약](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [초과하지 않는 상태 및 유효성 검사 계약](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [작업 기반 청구](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>더 이상 사용되지 않는 구성 요소

다음 표에는 더 이상 사용되지 않는 구성 요소 솔루션 업그레이드 이후로 이동되는 사용되지 않는 모든 필드가 나와 있습니다. 자세한 정보 및 솔루션 링크는 [Dynamics 365 Project Service Automation 3x부터 Project Operations 4x까지 더 이상 사용되지 않는 구성 요소](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution)를 참조하십시오.

### <a name="invoicedetail"></a>invoicedetail

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| 필드                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

