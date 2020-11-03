---
title: 프로젝트 견적에서 여러 고객 관리
description: 이 항목은 프로젝트에 자금을 지원할 여러 고객이 포함된 견적 작업에 대한 정보를 제공합니다. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079952"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>프로젝트 견적에서 여러 고객 관리(영업)

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

프로젝트 견적은 제안서에 거래 자금을 조달할 여러 고객이 포함되는 시나리오를 지원합니다. 견적의 **요약** 탭에는 거래의 기본 고객을 식별하는 **잠재 고객** 필드가 있습니다. 거래에 대한 다른 고객은 프로젝트 견적의 **고객** 탭에서 설정할 수 있습니다.

프로젝트 견적의 **고객** 탭에 있는 모든 견적 고객은 견적에 대해 작성된 **새로운** 프로젝트 기반 견적 라인의 견적 라인 고객으로 기본적으로 지정됩니다. 기존 프로젝트 기반 견적 라인은 그 이후에 생성된 새 견적 고객 레코드를 상속하지 않습니다.

제품 기반 견적 라인은 견적의 **요약** 탭에 있는 **잠재 고객** 필드의 고객이기도 한 기본 고객에게 자동으로 연관됩니다.

견적 고객 및 견적 라인 고객은 견적을 받기 전에 언제든지 추가, 업데이트 또는 삭제할 수 있습니다.

## <a name="concept-of-a-primary-customer"></a>기본 고객의 개념

프로젝트 견적의 요약 탭에 잠재 고객으로 있는 고객이 견적의 기본 고객입니다. 견적의 고객 목록에서 기본 고객을 삭제하려고 하면 견적의 기본 고객 레코드를 삭제할 수 없다는 오류가 표시됩니다.

견적의 고객 목록에서 기본 고객을 업데이트해서는 안 됩니다. 그러나 견적의 **요약** 탭에서 잠재 고객을 변경하여 기본 고객에게 영향을 줄 수 있습니다. 이 필드가 **견적 요약** 에서 업데이트되면 새로 선택한 잠재 고객이 **기본** 플래그가 설정된 새 견적 고객으로 추가됩니다. 기존 잠재 고객은 여전히 견적의 고객입니다.

## <a name="create-update-or-delete-a-quote-customer-record"></a>견적 고객 레코드 생성, 업데이트 또는 삭제

**견적** 페이지의 **고객 견적** 탭에서 견적 고객을 생성, 업데이트 또는 삭제할 수 있습니다. 다음 표에 나열된 필드는 프로젝트 견적의 견적 고객 레코드에 있습니다.

| **필드** | **위치** | **관련성, 목적 및 지침** | **다운스트림 영향** |
| --- | --- | --- | --- |
| 계정 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 모든 활성 계정을 나열합니다. 이 필드는 레코드가 생성된 후 잠깁니다. 업데이트하려면 레코드를 삭제하고 다시 만듭니다. 실제를 기록했거나 견적 고객 레코드가 기본 고객인 경우 레코드를 삭제할 수 있습니다. | 견적 고객은 견적 라인이 생성될 때 견적 라인 고객으로 복사됩니다. 견적 고객은 견적이 성공하면 프로젝트 계약 고객에게도 복사됩니다. |
| 청구 분할 백분율 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 이 견적 고객에게 귀속될 각 미청구 판매 트랜잭션의 백분율을 나타냅니다. | 새 견적 라인과 프로젝트 계약 고객에 복사됩니다. |
| 청구지 연락처 이름 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 이것은 텍스트 필드이며 이 고객의 송장 담당자를 식별하는 데 사용되어야 합니다. 관련 계정 레코드에서 기본값이 설정됩니다. | 견적이 성공하면 프로젝트 계약 고객에게 복사되고 이 고객에 대해 생성된 송장의 청구지 연락처 이름 필드에 복사됩니다. |
| 청구지 이름 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 이 텍스트 필드는 이 고객의 송장 담당자를 식별하는 데 사용되어야 합니다. | 견적이 성공하면 프로젝트 계약 고객에게 복사되고 이 고객에 대해 생성된 송장의 **청구지 연락처 이름** 필드에 복사됩니다. |
| 지불 조건 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 관련 계정 레코드에서 기본 값을 갖는 옵션 집합입니다. | 견적이 성공하면 프로젝트 계약 고객에게 복사되고 이 고객에 대해 생성된 송장의 **청구지 연락처 이름** 필드에 복사됩니다. |
| 반올림 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 이 고객이 이 거래의 기본 반올림 고객인지 여부를 나타냅니다. | 견적을 받을 때 프로젝트 계약 고객에게 복사됩니다. |
| 초과 안 함 한도 | 견적 고객을 위한 **고객 견적** 탭 및 **기본** 과 **빨리 만들기** 양식의 편집 가능한 그리드. | 이 계약에 대해 이 고객에게 청구될 전체 금액에 대해 협상된 한도가 있는지 여부를 나타냅니다. | 견적을 받을 때 프로젝트 계약 고객에게 복사됩니다. |

## <a name="editing-billing-split-percentages"></a>청구 분할 비율 편집

인라인 그리드 편집 환경을 사용하여 청구 분할 비율을 편집할 수 있습니다. 청구 분할 비율의 합계가 100%가 아니면 오류가 발생합니다. 청구 분할 비율을 업데이트한 후 페이지를 새로 고쳐 오류를 제거합니다.

견적 고객의 하위 표에서 **균등 분배** 를 선택해 볼 수도 있습니다. 이 작업은 모든 견적 고객에게 청구 분할을 할당합니다. 반올림 계수가 있는 경우 반올림 고객에 추가됩니다. 견적 고객 중 하나는 항상 반올림 고객으로 태그가 지정됩니다. 이는 견적 고객 레코드에 **반올림** 플래그가 **예** 로 설정된 것을 의미합니다. 일반적으로 견적의 기본 고객이지만 변경할 수 있습니다.