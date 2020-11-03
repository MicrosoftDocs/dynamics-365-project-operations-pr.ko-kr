---
title: Project Service의 기존 필드를 가격 책정 차원으로 사용
description: 이 항목은 가격 책정 차원으로서 기존 Project Service 필드를 사용하는 것에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080130"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Project Service의 기존 필드를 가격 책정 차원으로 사용

Project Service Automation(PSA)의 **실제값** 엔터티에는 프로젝트 조직에서 리소스 기반 가격 책정을 위한 가격 책정 차원으로 사용할 수 있는 많은 필드가 있습니다. 예를 들어, 하나의 공통 필드가 **예약 가능한 리소스** 입니다. 청구 가능한 리소스가 20~30개 미만인 소규모 기업은 각 리소스에 특정한 청구서 및 비용 요율을 갖는 것이 더 간단한 방법입니다. 그러나 청구 가능한 인력이 증가함에 따라 리소스가 승격되거나 더 많은 경험을 얻거나 다른 기능 집합을 습득함에 따라 리소스 비용과 청구 요금이 달라지기 시작하면서 이를 유지하는 것이 비현실적일 수 있습니다. 이 방법은 여전히 특정 크기의 회사에서 작동하므로, 어떻게 기존 Project Service 필드를 가격 책정 차원으로 사용할 수 있는지를 이해하려면 [예약 가능한 리소스를 가격 책정 차원으로 사용](bookable-resource-pricing-dimension.md) 항목을 참조하십시오.

또 다른 예는 처리 카테고리의 예입니다. 고객과 구현자는 PSA의 처리 카테고리를 사용하여 작업을 분류하고 해당 필드를 사용하여 작업의 카테고리에 따라 가격과 비용을 책정하였습니다. 자세한 설명은 [처리 카테고리 를 가격 책정 차원으로 사용](transaction-category-pricing-dimension.md) 항목을 참조하십시오.