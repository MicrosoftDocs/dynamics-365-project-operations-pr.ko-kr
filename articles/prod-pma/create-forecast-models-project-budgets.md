---
title: 프로젝트 예산에 대한 예측 모델 만들기
description: 이 항목은 남은 예산에 대한 예측 모델을 만드는 방법을 설명합니다.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 992dd74524ae6a7c329612a125d60bebfcbe7dd2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683638"
---
# <a name="create-forecast-models-for-project-budgets"></a>프로젝트 예산에 대한 예측 모델 만들기 

[!include [banner](../includes/banner.md)]

이 항목은 남은 예산에 대한 예측 모델을 만드는 방법을 설명합니다. 예산 통제가 적용되는 프로젝트는 원래 예산과 잔여 예산의 두 가지 유형을 사용합니다. 프로젝트 예산을 생성할 때 **예측 모델** 페이지에서 생성된 원래 및 잔여 예산 예측 모델을 지정해야 합니다. 프로젝트 예산을 약정하면 지정된 모델을 기반으로 하는 프로젝트 예산이 생성됩니다.

> [!NOTE]
> 예산 통제에 사용되는 예측 모델은 하위 모델을 갖거나 하위 모델로 사용할 수 없습니다.

1. **프로젝트 관리 및 회계** > **설정** > **예측**  > **예측 모델** 을 선택합니다.
2. **새로 만들기** 를 선택하여 새 예측 모델을 만든 다음 새 모델의 모델 ID 번호와 이름을 입력합니다. 
3. **중지됨** 옵션을 **예** 로 설정하여 예측 모델에 대한 예측 라인의 변경을 방지합니다. 
4. 모델이 연관된 예측 라인이 총계정 원장에서 현금 흐름 예측을 생성해야하는 경우 **현금 흐름 예측에 포함** 을 **예** 로 설정합니다. 
5. 프로젝트 날짜를 송장 날짜로 사용하려면 **예측 송장 날짜** 를 **예** 로 설정합니다. 
6. **예산 유형** 필드에서 다음 모델 유형 중 하나를 선택합니다.

   - **원래 예산**: 초기 예산 생성 및 승인시 약정된 최초 예산 금액을 사용합니다.
   - **남은 예산**: 프로젝트 기간 동안 남은 예산 금액을 사용합니다. 이 예측 모델의 잔액은 실제 거래에 의해 감소되고 예산 수정에 의해 증가 또는 감소합니다.
   - **이월**: 프로젝트에 대한 이월 예산 금액을 사용합니다. 이월은 사용되지 않은 예산 금액을 회계 연도에서 다른 회계 연도로 이전하기 위해 실행할 수 있는 선택적 프로세스입니다.

7. 다음 옵션을 필수로 설정합니다.

   - 프로젝트 날짜를 송장 날짜로 사용하려면 **예측 송장 날짜** 를 활성화합니다.
   - **WIP로 예측** 을 활성화하여 진행 중인 작업(WIP)을 기준으로 예측한 다음 WIP 유형을 선택합니다. 
   - 기본 **예산 유형** 을 **없음** 으로 유지하거나 새 유형을 입력합니다. 레코드를 변경한 후에는 예산 유형을 변경할 수 없습니다.     
    > [!NOTE]
    > 기본 예산 유형을 변경하면 다른 모든 옵션을 업데이트에 사용할 수 없으며 이 예측 모델을 재사용할 수 없습니다. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]