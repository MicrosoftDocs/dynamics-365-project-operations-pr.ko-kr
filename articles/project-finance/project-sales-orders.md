---
title: 시간 및 자재 프로젝트에 대한 프로젝트 판매 주문
description: 이 항목은 시간 및 자재 프로젝트에 대한 프로젝트 기반 판매 주문을 생성하는 방법을 설명합니다.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753230"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>시간 및 자재 프로젝트에 대한 프로젝트 판매 주문

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

이 항목은 프로젝트에 대한 판매 주문을 생성하는 방법을 설명합니다. 판매 주문은 **시간 및 재료** 유형의 프로젝트에 대해서만 생성할 수 있습니다.

시간 및 자재 프로젝트에 프로젝트 계약의 여러 자금 출처가 있는 경우 **프로젝트 관리 및 회계 매개 변수**페이지의 **자금 출처가 여러 개인 프로젝트에 대한 판매 주문 허용** 매개 변수를 활성화해야 합니다. 

> [!NOTE]
> - 여러 자금 출처가 있는 프로젝트 판매 주문에 대한 지원은 애플리케이션 릴리스 10.0.2 이상부터 사용할 수 있습니다.
> - 여러 자금 출처가 있는 프로젝트 판매 주문에 대한 지원을 활성화하는 매개 변수는 2020년 4월 릴리스 웨이브에서 제거되며 그 이후에는 기능이 항상 활성화됩니다.

다음 두 가지 방법으로 프로젝트 기반 판매 주문을 생성할 수 있습니다.

- 프로젝트로 이동합니다. 작업 창에서 **관리 > 품목 작업 > 판매 주문**을 선택합니다. 프로젝트 정보는 기본적으로 프로젝트의 판매 주문으로 설정됩니다. 프로젝트 계약에 둘 이상의 자금 출처가 있는 경우 판매 주문에 대한 고객을 설정하려면 자금 출처를 선택해야 합니다. 프로젝트에 자금 출처가 하나만 있는 경우 고객이 자동으로 설정됩니다.
- **모든 판매 주문** 목록 페이지로 이동하고 새 판매 주문을 만듭니다. 판매 주문에 대한 프로젝트를 선택해야 합니다. 프로젝트를 선택한 후 고객은 자금 출처에서 설정되거나 프로젝트 계약에 자금 출처가 여러 개인 경우 자금 출처를 선택해야 합니다.

