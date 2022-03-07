---
title: 프로젝트 구매 주문
description: 이 문서에서는 프로젝트에 대한 구매 주문을 생성하는 데 사용할 수 있는 다양한 방법에 대해 설명합니다. 사용하는 방법은 구매 주문의 목적과 구매한 항목이 소비되고 프로젝트에 청구되는 시기에 따라 다릅니다.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5de28f3844b802a980c811411cae75549c697538f89e8c3d2495ea171a188524
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008999"
---
# <a name="purchase-orders-for-a-project"></a>프로젝트 구매 주문

[!include [banner](../includes/banner.md)]

이 문서에서는 프로젝트에 대한 구매 주문을 생성하는 데 사용할 수 있는 다양한 방법에 대해 설명합니다. 사용하는 방법은 구매 주문의 목적과 구매한 항목이 소비되고 프로젝트에 청구되는 시기에 따라 다릅니다.

### <a name="methods-for-creating-a-purchase-order"></a>구매 주문 생성 방법

다음 방법 중 하나를 사용하여 프로젝트 관리 및 회계에서 구매 주문을 생성할 수 있습니다. 구매 주문의 목적에 따라 구매 주문이 소비되는 시기와 항목이 프로젝트에 청구되는 시기가 결정됩니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>방법</th>
<th>용도</th>
<th>품목 소비</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>프로젝트에서 구매 주문을 직접 만듭니다.</td>
<td>프로젝트에서 소비하기 위해 이 방법을 사용하여 외부 공급업체로부터 품목을 구매합니다. 두 가지 방법으로 구매 주문을 만들 수 있습니다.
<ul>
<li>프로젝트 자체에서. 이 경우 프로젝트는 구매 주문에 대해 이미 정의되어 있습니다.</li>
<li>프로젝트 구매 주문으로 이동합니다. 구매 주문을 생성할 공급업체와 프로젝트를 모두 선택해야 합니다.</li>
</ul></td>
<td>공급업체 송장이 업데이트되면 항목이 소비됩니다.</td>
</tr>
<tr class="even">
<td>판매 주문에서 구매 주문을 만듭니다.</td>
<td>이 방법을 사용하여 프로젝트에서 판매 주문을 생성할 때 품목을 구매합니다.</td>
<td>판매 주문이 고객에게 청구될 때 품목이 소비됩니다.</td>
</tr>
<tr class="odd">
<td>품목 요구 사항에서 구매 주문을 생성합니다.</td>
<td>이 방법을 사용하여 프로젝트에서 품목 요구 사항을 생성할 때 품목을 구매합니다.</td>
<td>품목 요구 사항 패킹 슬립이 업데이트될 때 품목이 소비됩니다.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> 공급업체 송장 또는 패킹 슬립을 업데이트할 때 품목 요구 사항에 대한 패킹 슬립을 업데이트하라는 메시지가 표시됩니다.

자세한 내용은 [품목 요구 사항에서 구매 주문에 대한 품목 수령](tasks/receive-items-purchase-order-item-requirement.md)을 참조하십시오.



[!INCLUDE[footer-include](../includes/footer-banner.md)]