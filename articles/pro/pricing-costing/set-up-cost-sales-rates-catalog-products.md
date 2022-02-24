---
title: 카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트
description: 이 항목은 제품 카탈로그의 항목에 대한 비용 및 판매율을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764563"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_


Dynamics 365 Project Operations의 제품 카탈로그 항목에 대한 가격 산정 설정은 Dynamics 365 Sales와 동일합니다.

Project Operations에서는 제품을 추정하거나 프로젝트에 사용할 수 없으므로 견적 및 계약을 위해 제품 카탈로그 가격을 프로젝트 가격 목록에 설정할 필요가 없습니다.

견적, 계약 또는 계정의 **제품 가격** 필드를 사용하여 제품 카탈로그 가격을 설정합니다. 프로젝트 가격 목록에서 제품 카탈로그 가격을 설정하지 마십시오. 프로젝트 가격표는 Project Operations에만 적용됩니다. 응용 프로그램별 비즈니스 로직은 견적에서 계약으로 가격 목록을 복사합니다. 결과는 계약별 프로젝트 가격표입니다. 견적서의 프로젝트 가격표가 너무 커지면 복사 작업으로 인해 견적 획득 프로세스가 지연될 수 있습니다. 제품 가격표는 계약에 대한 사용자 지정 가격표를 만들기 위해 복사되지 않습니다. 복사가 필요하지 않기 때문에 견적 프로세스의 성능에 영향을 주지 않습니다.
