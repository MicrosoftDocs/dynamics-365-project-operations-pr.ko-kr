---
title: Project Service의 기존 필드를 가격 책정 차원으로 사용
description: 이 항목은 가격 책정 차원으로서 기존 Project Service 필드를 사용하는 것에 대한 정보를 제공합니다.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3d8251b4516b4598c9c92779c59b9609d8113ac9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580142"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Project Service의 기존 필드를 가격 책정 차원으로 사용

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation(PSA)의 **실제값** 엔터티에는 프로젝트 조직에서 리소스 기반 가격 책정을 위한 가격 책정 차원으로 사용할 수 있는 많은 필드가 있습니다. 예를 들어, 하나의 공통 필드가 **예약 가능한 리소스** 입니다. 청구 가능한 리소스가 20~30개 미만인 소규모 기업은 각 리소스에 특정한 청구서 및 비용 요율을 갖는 것이 더 간단한 방법입니다. 그러나 청구 가능한 인력이 증가함에 따라 리소스가 승격되거나 더 많은 경험을 얻거나 다른 기능 집합을 습득함에 따라 리소스 비용과 청구 요금이 달라지기 시작하면서 특정 비율을 유지하는 것이 비현실적일 수 있습니다. 이 방법은 여전히 특정 크기의 회사에서 작동하므로, 어떻게 기존 Project Service 필드를 가격 책정 차원으로 사용할 수 있는지를 이해하려면 [예약 가능한 리소스를 가격 책정 차원으로 사용](bookable-resource-pricing-dimension.md)을 참조하십시오.

또 다른 예는 처리 카테고리의 예입니다. 고객과 구현자는 PSA의 처리 카테고리를 사용하여 작업을 분류하고 해당 필드를 사용하여 작업의 카테고리에 따라 가격과 비용을 책정하였습니다. 자세한 설명은 [처리 카테고리 를 가격 책정 차원으로 사용](transaction-category-pricing-dimension.md) 항목을 참조하십시오.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
