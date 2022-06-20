---
title: 시간에 대한 공급업체 송장 라인
description: 이 문서에서는 하도급업체가 입력한 시간 비용에 대한 공급업체 송장 라인을 기록하는 방법을 설명합니다.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927551"
---
# <a name="vendor-invoice-lines-for-time"></a>시간에 대한 공급업체 송장 라인

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Microsoft Dynamics 365 Project Operations의 공급업체 송장은 시간에 대한 공급업체 송장 라인을 가질 수 있습니다. 프로젝트 관리자는 시간 동안 공급업체 송장 라인을 사용하여 프로젝트에 대한 하도급업체 시간 비용을 기록할 수 있습니다.

시간에 대한 공급업체 송장 라인은 시간에 대한 하도급 계약 내용을 참조하거나 참조하지 않을 수 있습니다. 시간에 대한 공급업체 송장 라인이 하도급 계약을 참조하는 경우 프로젝트 관리자는 하도급업체가 기록하고 프로젝트의 프로젝트 관리자가 승인한 시간과 공급업체 송장 라인에서 송장을 발행하는 시간을 일치시키고 확인할 수 있습니다.

다음 표에서는 시간의 공급업체 송장 라인에 대한 정보를 제공합니다.

| 필드 | Description | 기능적 영향 |
| --- | --- | --- |
| Name | 식별에 도움이 되는 공급업체 송장 라인의 이름입니다. | 이 이름은 공급업체 송장 라인을 기반으로 하는 모든 조회에서 첫 번째 열로 표시됩니다. |
| Description | 공급업체 송장 라인에서 공급업체가 송장을 발행하는 서비스에 대한 간략한 설명입니다. | None |
| 하도급 계약 | 서비스가 원래 주문된 하도급 계약입니다. | 공급업체 송장에 대한 하도급 계약이 선택되면 공급업체 송장의 모든 라인이 해당 선택 사항을 상속합니다. 공급업체 송장에는 다른 하도급 계약을 참조하는 공급업체 송장 라인이 있을 수 없습니다. |
| 하도급 계약 내용 | 서비스가 주문된 하도급 계약 내용입니다. 선택할 수 있는 하도급 계약 내용 목록은 선택한 하도급 계약 내용으로 제한됩니다. | 시간에 대한 공급업체 송장 라인에서 하도급 계약 내용을 선택하면 **프로젝트**, **역할** 및 **예약 가능한 리소스** 필드의 기본값이 하도급 계약 내용의 해당 필드에서 입력됩니다. 선택한 하도급 계약 내용의 **프로젝트**, **역할** 및 **예약 가능** 필드에 값이 있는 경우 공급업체 송장 라인의 해당 필드 값은 해당 값과 다를 수 없습니다. |
| 거래일 | 공급업체 송장 라인의 실제 비용이 프로젝트에 기록되는 날짜입니다. | None |
| 거래 등급 | 기본값은 **시간** 입니다. | 값 **시간** 은 공급업체 송장 라인이 하청업체 시간의 송장 금액을 기록하는 데 사용되고 있음을 나타냅니다. |
| Project | 청구되는 서비스가 사용된 프로젝트의 이름입니다. | 이 필드는 필수 필드이기 때문에 비워 둘 수 없습니다. |
| 작업 | 청구되는 서비스가 사용된 프로젝트 작업의 이름입니다. 이 필드는 프로젝트가 선택된 경우에만 사용할 수 있습니다. 프로젝트 작업 선택은 선택 사항입니다. | 이 필드를 비워두면 프로젝트 관리자는 공급업체 송장 라인을 프로젝트의 모든 작업에 대해 하도급업체 리소스가 기록한 시간과 일치시킬 수 있습니다. 공급업체 송장 라인이 하도급 계약 내용을 참조하지 않고 이 필드를 공백으로 두면 공급업체 송장 라인에서 생성된 실제 비용이 청구되지 않은 실제 판매 금액에 연결되지 않습니다. 이 경우 작업 기반 청구가 설정되면 비용이 최종 고객에게 청구되지 않을 수 있습니다. |
| 역할 | 시간이 청구되는 하도급 계약 리소스의 역할입니다. | 이 필드는 시간이 공급업체 송장에 청구되는 하도급 계약 리소스가 수행하는 역할을 지정합니다. |
| 예약 가능한 리소스 | 시간이 청구되는 하도급업체의 이름입니다. 예약 가능한 리소스는 선택 사항입니다. | 이 필드를 비워두면 프로젝트 관리자는 공급업체 송장 라인에서 공급업체에 속한 리소스가 기록하는 시간과 공급업체 송장 라인을 일치시킬 수 있습니다. |
| 수량 | 송장 라인에 공급업체가 송장을 발행하는 시간을 입력합니다. |None |
| 단위 그룹 | 기본값은 **시간 단위 그룹** 이며, 변경할 수 없습니다. | None |
| 단위 | 기본값은 시간 단위 그룹의 기본 시간 단위입니다. 이 값을 변경하여 일 또는 주와 같은 시간 단위 그룹의 모든 단위를 구매할 수 있습니다. | **역할** 및 **단위** 값의 조합은 공급업체 송장 라인의 **단가** 필드에 대한 기본값 또는 계산된 값으로 사용됩니다. |
| 단가 | 기본 단가는 공급업체 송장 라인의 거래 일자에 적용할 수 있는 프로젝트 가격 목록의 **역할** 및 **단가** 값의 조합을 사용합니다. | 해당 프로젝트 가격 목록의 가격이 공급업체 송장 라인의 단위와 다른 단위로 설정된 경우 시스템은 단위 변환을 사용하여 단위당 가격을 계산합니다. |
| 소계 | **수량** 필드와 **단가** 필드 모두에 값을 입력한 경우 이 읽기 전용 필드는 *Quantity* &times; *단가* 로 계산됩니다. 필드 중 하나 또는 둘 모두가 비어 있는 경우 이 필드에 값을 입력할 수 있습니다. | None |
| 판매세 | 판매세 금액을 입력합니다. | None |
| 총 금액 | 세금을 포함한 공급업체 송장 라인의 총액입니다. 이 필드는 *소계*  +  *판매세* 로 계산됩니다. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]