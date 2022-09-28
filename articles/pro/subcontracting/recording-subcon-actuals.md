---
title: 하도급 계약 구성 요소에 대한 시간, 경비, 재료 사용량 기록
description: 이 문서에서는 하도급 계약 구성 요소의 프로젝트에 기록된 시간, 비용 및 재료 사용량을 Microsoft Dynamics 365 Project Operations에서 추적하는 방법에 대해 설명합니다.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522522"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>하도급 계약 구성 요소에 대한 프로젝트의 시간, 경비, 재료 사용량 기록

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

이 문서에서는 하도급 계약 구성 요소의 프로젝트에 기록된 시간, 비용 및 재료 사용량을 Microsoft Dynamics 365 Project Operations에서 추적하는 방법에 대해 설명합니다.

## <a name="costing-for-subcontractor-time-on-projects"></a>프로젝트의 하청업체 시간 비용 계산
Project Operations에서 계약 작업자는 직원과 유사한 방식으로 프로젝트에 시간을 기록할 수 있습니다. 프로젝트 및/또는 프로젝트 작업에 시간을 입력할 때 계약 작업자는 특정 하도급 계약 및 하도급 계약 내용을 선택할 수 있습니다.

계약 작업자가 제출한 시간이 승인되면 하도급 계약 구매 가격표의 **역할 가격** 섹션에서 해당 계약직 리소스에 대해 설정된 단가를 사용하여 프로젝트 비용을 기록합니다.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>프로젝트의 하도급 계약 경비 비용 계산
프로젝트에 발생한 경비를 입력할 때 경비 입력에서 하도급 계약 및 하도급 계약 내용을 선택할 수 있습니다. 

이 경비 항목이 제출되고 승인되면 하도급 계약에 있는 구매 가격표의 **범주 가격** 섹션에서 해당 거래 범주에 대해 설정된 단가를 기준으로 경비 비용이 프로젝트에 기록됩니다.

## <a name="costing-for-subcontracted-materials-on-projects"></a>프로젝트의 하도급 계약 자쟈 비용 계산
프로젝트에 자재 사용을 입력할 때 재료 사용 로그에서 하도급 계약 및 하도급 계약 내용을 선택할 수 있습니다. 자재 사용 로그를 제출하고 승인하면 하도급 계약 가격표의 **가격표 항목** 섹션에서 해당 제품에 대해 설정된 단가를 기준으로 자재 비용이 프로젝트에 기록됩니다.

자재 사용량은 프로젝트의 직접 입력 제품에 대해서도 기록될 수 있습니다. 이러한 유형의 자재 사용은 하도급 계약 및 하도급 계약 내용에 연결할 수도 있습니다. 직접 입력 제품의 자재 사용량을 기록할 때 직접 입력 제품의 단가를 입력해야 합니다. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
