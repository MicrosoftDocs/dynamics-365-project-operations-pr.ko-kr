---
title: 단위 및 단위 그룹
description: 이 항목은 Dynamics 365 Project Operations에서 단위 및 단위 그룹을 만드는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080175"
---
# <a name="units-and-unit-groups"></a>단위 및 단위 그룹

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

단위는 제품 또는 서비스를 판매하는 수량 또는 규격입니다. 예를 들어, 정원 소모품을 판매하는 경우 씨앗을 패킷, 박스 또는 팔레트 단위로 판매할 수 있습니다. 단위 그룹은 일한 여러 단위의 모음입니다.

이 항목의 단계를 완료하려면 시스템 관리자 또는 Sales Professional 관리자 역할에 할당되었거나 동등한 권한이 있는지 확인하십시오.

## <a name="create-a-unit-group"></a>단위 그룹 만들기

1. 사이트 맵에서 **단위** 를 선택합니다.
2. **신규** 를 선택하고 **단위 그룹 만들기** 대화 상자에 단위 이름을 입력합니다.
3. **기본 단위** 필드에 제품이 판매되는 가장 낮은 단위를 입력합니다. 예를 들어 "조각" 또는 "온스"를 입력할 수 있습니다.
4. **확인** 을 선택합니다.

## <a name="add-units-to-a-unit-group"></a>단위 그룹에 단위 추가

1. 단위 그룹을 열고 **관련** 탭에서 **단위** 를 선택합니다. 기본 단위가 이미 추가되어 있는 것을 확인할 수 있습니다.
2. **새 단취 추가** 를 선택하고 **빠른 만들기: 단위** 페이지에서 **이름** 필드에 단위의 이름을 입력합니다.
3. **수량** 필드에 단위에 포함될 수량을 입력합니다. 예를 들어, 한 박스에 2개가 있으면 "2"를 입력합니다. 
4. **기본 단위** 필드에서 단위에 대한 가장 낮은 측정 단위를 설정할 기본 단위를 선택합니다. 예를 들어 "Piece"를 선택할 수 있습니다.
5. **저장** 을 선택합니다.
