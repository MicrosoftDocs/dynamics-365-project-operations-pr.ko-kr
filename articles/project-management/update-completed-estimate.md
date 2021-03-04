---
title: 완료 시 추정 비용 업데이트
description: 이 항목은 프로젝트에 대한 노력의 예측 업데이트에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127211"
---
# <a name="update-estimate-at-completion"></a>완료 시 추정 비용 업데이트

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

프로젝트 관리자는 작업에 대한 원래 예상을 수정하는 것이 일반적입니다. 프로젝트 재추정은 프로젝트의 현재 상태를 고려할 때 프로젝트 관리자의 예상에 대한 인식입니다. 하지만, 프로젝트 관리자가 기본 수치를 변경하는 것은 권장하지 않습니다. 프로젝트 기본 수치는 프로젝트의 일정 및 비용에 대해 구비된 실제 자원이며, 모든 프로젝트 이해 관계자가 동의했기 때문입니다.

프로젝트 관리자가 작업에 대한 작업량을 다시 프로젝트할 수 있는 방법에는 두 가지가 있습니다.

- 작업에 실제 남은 작업량의 새 예상값으로 기본 완료 추정 비용(ETC)을 재정의합니다. 
- 작업의 실제 진행률의 새 예상값으로 기본 진행률을 재정의합니다.

이러한 각 접근 방식은 작업의 ETC, 작업 완료 시 추정 비용(EAC) 및 진행률을 다시 계산하고 작업에 추정된 작업량 차이를 발생하게 됩니다. 요약 작업에 대한 EAC, ETC 및 진행률 비율이 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]