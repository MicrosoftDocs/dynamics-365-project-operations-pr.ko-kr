---
title: 견적 닫기 - 라이트
description: 이 항목은 Project Operations의 견적 종료에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764872"
---
# <a name="close-a-quote---lite"></a>견적 닫기 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

프로젝트 견적은 성공 또는 실패로 마감될 수 있습니다. 견적에 대한 활성화 및 수정 작업이 Microsoft Dynamics 365 Project Operations에서 지원되지 않기 때문에 초안 견적을 마감할 수 있습니다.

## <a name="close-a-quote-as-won"></a>견적을 성공으로 종료

프로젝트 견적을 성공으로 마감하면 상태는 마감으로 설정되고 상태 설명은 성공이 됩니다. 견적을 종료하면 프로젝트 견적이 읽기 전용이 되고 견적 정보가 포함된 프로젝트 계약 초안이 생성됩니다. 마감된 견적은 다시 열 수 없기 때문에 확인 대화 상자에서 변경 사항을 확인합니다.

견적이 영업 기회에 첨부된 경우 영업 기회에 대한 다른 프로젝트 견적은 자동으로 실패로 종료됩니다.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>성공으로 견적 종료의 재정적 영향

초안 견적에 첨부되어 있는 동안 프로젝트의 시간에 대한 실제가 있는 경우 시간 또는 경비의 비용만 기록됩니다. 견적이 성공으로 종료된 후 응용 프로그램은 이전 실제 비용을 되돌리고 새로운 실제 비용을 다시 생성하여 비용을 리팩토링합니다. 응용 프로그램은 연관된 프로젝트 계약 내용의 청구 방법을 기반으로 이러한 실제 비용을 처리합니다. 실제 원가가 시간 및 재료 계약 내용을 참조하는 경우 견적이 마감되고 프로젝트 계약이 생성될 때 해당 미청구 판매 실제가 생성됩니다. 실제 원가가 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 프로젝트 계약 고객에 대한 분할 청구 규칙을 기반으로 하는 실제 원가 재처리를 중지합니다.

## <a name="closing-a-quote-as-lost"></a>견적을 실패로 종료:

프로젝트 견적을 실패로 마감하면 상태는 마감으로 설정되고 상태 설명은 실패가 됩니다. 견적을 종료하면 프로젝트 견적이 읽기 전용이 됩니다. 종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.

실패로 마감된 프로젝트 견적이 해당 라인의 프로젝트를 참조하는 경우 해당 프로젝트도 마감됨으로 표시됩니다. 그 날 이후의 모든 리소스 예약은 취소됩니다.

> [!NOTE]
> Project Operations에서 견적을 성공 또는 실패로 종료해도 영업 기회의 해당 상태에 영향을 주지 않으며 수동으로 종료할 때까지 계속 열려 있습니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]