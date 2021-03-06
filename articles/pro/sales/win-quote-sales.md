---
title: 견적 종료
description: 이 항목은 Project Operations의 견적 종료에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896199"
---
# <a name="close-quotes"></a>견적 종료 

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

프로젝트 견적은 성공 또는 실패로 마감될 수 있습니다. 견적에 대한 활성화 및 수정 작업은 Microsoft Dynamics 365 Project Operations에서 지원되지 않으므로 초안 견적을 종료할 수 있습니다.

## <a name="close-a-quote-as-won"></a>견적을 성공으로 종료

프로젝트 견적을 성공으로 종료하면 상태가 종료됨으로 설정되고 상태 설명이 성공으로 설정된 견적이 종료됩니다. 견적을 종료하면 프로젝트 견적이 읽기 전용이 되고 견적 정보가 포함된 프로젝트 계약 초안이 생성됩니다. 종료된 견적은 확인 대화 상자를 다시 열 수 없습니다. 종료된 견적을 다시 열 수 없고 변경 사항을 되돌릴 수 없기 때문에 변경이 완료되기 전에 확인 대화 상자가 있습니다.

견적이 영업 기회에 첨부된 경우 영업 기회에 대한 다른 프로젝트 견적은 자동으로 실패로 종료됩니다.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>성공으로 견적 종료의 재정적 영향

초안 견적에 첨부되어 있는 동안 프로젝트에 기록된 시간에 대한 실제 값이 있는 경우 시간 또는 경비의 비용만 기록됩니다. 견적이 성공으로 종료된 후 응용 프로그램은 이전 실제 비용을 되돌리고 새로운 실제 비용을 다시 생성하여 비용을 리팩토링합니다. 응용 프로그램은 연관된 프로젝트 계약 내용의 청구 방법을 기반으로 이러한 실제 비용을 처리합니다. 실제 비용이 시간 및 재료 계약 내용을 참조하는 경우 시스템은 견적이 종료되고 프로젝트 계약이 생성될 때 해당 미 청구 판매 실적을 자동으로 생성합니다. 실제 비용이 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 프로젝트 계약 고객에 대한 분할 청구 규칙에 따라 실제 비용 재처리를 중지합니다.

## <a name="closing-a-quote-as-lost"></a>견적을 실패로 종료:

프로젝트 견적을 실패로 종료하면 상태가 종료됨으로 설정되고 상태 설명은 실패로 설정됩니다. 견적을 종료하면 프로젝트 견적이 읽기 전용이 됩니다. 종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.

실패로 종료된 프로젝트 견적에 해당 라인에서 참조된 프로젝트가 있는 경우 해당 프로젝트도 종료됨으로 표시되고 해당 날짜 이후의 모든 리소스 예약이 취소됩니다.

> [!NOTE]
> Project Operations에서 견적을 성공 또는 실패로 종료해도 영업 기회의 해당 상태에 영향을 주지 않으며 수동으로 종료할 때까지 계속 열려 있습니다.
