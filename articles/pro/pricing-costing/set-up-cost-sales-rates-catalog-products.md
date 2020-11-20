---
title: 카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트
description: 이 항목은 제품 카탈로그의 항목에 대한 비용 및 판매율을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176709"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_


Dynamics 365 Project Operations의 제품 카탈로그 항목에 대한 가격 설정은 Dynamics 365 Sales에서와 동일합니다.

Project Operations의 프로젝트에서 제품을 추정하거나 사용할 수 없기 때문에 견적 및 계약을 위해 프로젝트 가격표에 제품 카탈로그 가격을 설정할 필요가 없습니다.

제품 카탈로그 가격은 견적, 계약 또는 계정의 **제품 가격** 필드에서 설정해야 합니다. 이러한 엔터티의 프로젝트 가격표에서 제품 카탈로그 가격을 설정하지 마십시오. 프로젝트 가격표는 Project Operations에만 적용됩니다. 견적에서 계약으로 가격표를 복사하는 응용 프로그램별 비즈니스 로직이 있습니다. 결과는 계약별 프로젝트 가격표입니다. 견적서의 프로젝트 가격표가 너무 커지면 복사 작업으로 인해 견적 획득 프로세스가 지연될 수 있습니다. 제품 가격표는 계약에 대한 사용자 지정 가격표를 만들기 위해 복사되지 않습니다. 이는 제품 가격표가 견적 획득 프로세스의 성능에 영향을 미치지 않음을 의미합니다.
