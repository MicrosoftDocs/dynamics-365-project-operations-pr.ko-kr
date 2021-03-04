---
title: 인건비 및 비용에 대한 표준 비용 구성
description: 이 항목은 프로젝트의 인건비 및 비용에 대한 표준 비용을 설정하는 방법을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080109"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>인건비 및 비용에 대한 표준 비용 구성

[!include [banner](../../includes/banner.md)]

이 항목은 프로젝트의 인건비 및 비용에 대한 표준 비용을 설정하는 방법을 설명합니다. 이 작업은 USSI 데이터 집합을 사용합니다.

1. 탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 원가(시간)** 로 이동합니다.
2. **새로 만들기** 를 선택합니다.
3. **유효 날짜** 필드에 날짜를 입력합니다.
4. **원가** 필드에 숫자를 입력합니다. 프로젝트 범주에 대한 표준 원가를 설정하거나 작업자 번호, 프로젝트 번호, 범주, 날짜 또는 이들의 조합으로 원가를 설정할 수 있습니다. 적용되는 원가는 세부 수준이 가장 높은 원가입니다.  
5. **저장** 을 선택합니다.
6. 탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 판매 가격(시간)** 으로 이동합니다.
7. **새로 만들기** 를 선택합니다.
8. **유효 날짜** 필드에 날짜를 입력합니다.
9. **유효 기간** 필드에서 옵션을 선택합니다.
10. **가격 책정** 필드에 숫자를 입력합니다. 시간 거래 또는 프로젝트 범주에 대한 표준 판매 가격을 설정할 수 있습니다. 작업자 번호, 프로젝트 번호, 범주, 트랜잭션 날짜 또는 이들의 조합으로 판매 가격을 설정할 수도 있습니다. 작업자가 시간 저널에 트랜잭션을 입력할 때 적용되는 실제 판매 가격은 세부 수준이 가장 높은 판매 가격입니다. 예를 들어 일반 판매 가격과 작업자별 판매 가격이 모두 설정된 경우 작업자별 판매 가격이 사용됩니다.  
11. **저장** 을 선택합니다.
12. 창을 닫습니다.
13. 탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 원가(경비)** 로 이동합니다.
14. **새로 만들기** 를 선택합니다.
15. **유효 날짜** 필드에 날짜를 입력합니다.
16. **원가** 필드에 숫자를 입력합니다. 여러 필드를 채울 수 있지만 이는 레코드를 저장하는 데 필요한 최소값입니다.  
17. **저장** 을 선택합니다.
18. 탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 판매 가격(경비)** 으로 이동합니다.
19. **새로 만들기** 를 선택합니다.
20. **유효 날짜** 필드에 날짜를 입력합니다.
21. **유효 기간** 필드에서 옵션을 선택합니다.
22. **가격 책정** 필드에 숫자를 입력합니다. 작업자가 경비 저널에 트랜잭션을 입력할 때 적용되는 실제 판매 가격은 세부 수준이 가장 높은 판매 가격입니다. 예를 들어 일반 및 작업자별 판매 가격이 모두 설정된 경우 작업자별 판매 가격이 사용됩니다.  
23. **저장** 을 선택합니다.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]