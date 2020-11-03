---
title: 수동 견적 송장 만들기
description: 이 항목은 Project Operations에서 수동 견적 송장 만들기에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080281"
---
# <a name="creating-a-manual-proforma-invoice"></a>수동 견적 송장 만들기

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Dynamics 365 Project Operations에서 견적 송장은 필요에 따라 수동으로 생성할 수 있습니다. **프로젝트 계약** 목록 페이지 또는 **프로젝트 계약** 세부 정보 페이지에서 수동으로 견적 송장을 생성할 수 있습니다.

##  <a name="project-contracts-list-page"></a>프로젝트 계약 목록 페이지

**프로젝트 계약** 목록 페이지에서 하나 이상의 프로젝트 계약을 선택하고 선택한 모든 레코드에 대한 송장을 생성합니다.

시스템은 선택한 프로젝트 계약 중 오늘 날짜 이전의 **송장 준비** 백 로그가 있는 계약이 있는지 확인합니다. 이러한 계약에서 시스템은 초안 견적 송장을 생성합니다. 프로젝트 계약에 여러 고객이 있는 경우 고객당 하나의 송장이 생성되고 프로젝트 계약당 여러 송장이 생성될 수 있습니다.

생성된 모든 프로젝트 송장은 **영업** 영역의 **청구** 섹션에 있는 **송장** 페이지에 있습니다.

## <a name="project-contract-details-page"></a>프로젝트 계약 세부 정보 페이지

견적 송장은 특정 프로젝트 계약에 대한 송장을 생성하는 **프로젝트 계약** 세부 정보 페이지에서 생성할 수도 있습니다. 시스템은 프로젝트 계약에 오늘 날짜 이전의 **송장 발부 준비 완료** 백로그가 있는지 확인합니다. 이러한 계약에서 시스템은 각 계약 내용의 고객 수를 기반으로 견적 송장 초안을 생성합니다.

하나의 견적 송장이 생성되면 **송장** 페이지가 열립니다. 해당 프로젝트 계약에 대해 생성된 송장이 여러 개 있는 경우 **송장** 목록 페이지가 열리고 생성된 모든 송장이 표시됩니다.
