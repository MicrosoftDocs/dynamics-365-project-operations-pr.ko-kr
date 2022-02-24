---
title: 프로젝트 계약 확인
description: 이 항목은 Project Operations에서 계약을 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128291"
---
# <a name="confirm-a-project-contract"></a>프로젝트 계약 확인

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations의 프로젝트 계약은 이유가 **확인됨** 인 경우 활성화되고 이유가 **손실** 인 경우 마감될 수 있습니다. 프로젝트 계약을 확인하면 상태가 **초안** 에서 **활성** 으로 업데이트되고 상태 설명은 **확인됨** 이 됩니다. 활성 또는 마감된 계약은 편집하거나 다시 열 수 없습니다. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>프로젝트 계약 확인의 재정적 영향

프로젝트 계약이 확인되면 응용 프로그램은 이전의 실제 비용을 되돌리고 새로운 실제 비용을 생성하여 비용을 다시 계산합니다. 그러면 연관된 프로젝트 계약 내용의 청구 방법에 따라 새 실제 비용이 처리됩니다. 실제 비용이 시간 및 재료 계약 내용을 참조하는 경우 응용 프로그램은 해당 청구되지 않은 실제 판매를 자동으로 다시 생성합니다. 실제 비용이 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 실제 비용 재처리를 중지합니다.

초과하지 않는 한도, 청구 가능성 설정, 실제 항목에 대한 가격 및 비용이 평가되고 확인 프로세스의 일부로 업데이트됩니다.

## <a name="close-a-project-contract-as-lost"></a>프로젝트 계약을 손실로 마감

프로젝트 계약을 손실로 마감하면 계약 상태가 **마감** 으로 업데이트되고 상태 설명은 **손실** 이 됩니다. 프로젝트 계약은 읽기 전용이 됩니다. 마감된 프로젝트 계약을 다시 열 수 없기 때문에 변경이 완료되기 전에 확인 대화 상자가 제공됩니다.

손실로 마감된 프로젝트 계약이 해당 라인의 프로젝트를 참조하는 경우 해당 프로젝트도 마감된 것으로 표시됩니다. 그 날 이후의 모든 리소스 예약은 취소됩니다. 송장에 아직 없는 프로젝트 계약의 청구되지 않은 실제 판매는 취소됩니다.

> [!NOTE]
> Dynamics 365 Project Operations에서 프로젝트 계약을 손실로 마감해도 관련 영업 기회의 상태에 영향을 주지 않습니다. 영업 기회는 열린 상태로 유지되며 수동으로 닫아야 합니다.
