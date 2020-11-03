---
title: 예약 할당 방법
description: 이 항목은 프로젝트 운영에서 예약 할당 방법이 작동하는 방식에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080002"
---
# <a name="booking-allocation-methods"></a>예약 할당 방법

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

팀원을 **팀** 탭의 프로젝트에 직접 추가하거나 스케줄 게시판의 프로젝트나 요건에 대한 리소스를 예약하는 경우에는 몇 가지 다른 예약 할당 방법을 사용할 수 있습니다. 이 항목은 각 방법의 작동 방식 및 리소스 초과 예약으로 이어질 수 있는 방법을 설명합니다.

## <a name="booking-allocation-methods"></a>예약 할당 방법

사용할 수 있는 6가지 예약 할당 방법이 있습니다.

- [전체 생산 능력](#full)
- [남은 생산 능력](#remaining)
- [백분율 생산 능력](#percentage)
- [균등 분배 시간](#evenly)
- [초기 단계 이익 배분 시간](#front)
- [없음](#none)

### <a name="full-capacity"></a><a name="full"></a>전체 생산 능력 
전체 능력 방법은 지정한 종료 날짜에서 시작 날짜까지 리소스의 전체 능력을 예약합니다. 예컨대, 리소스에 1일 8시간, 일주일에 5일을 설정하는 달력이 있는 경우 5 근무일을 포함하는 시작 및 종료 날짜를 설정하면 리소스가 40시간 동안 예약됩니다. 예약은 리소스의 남은 능력에 관계 없이 이루어집니다. 리소스가 해당 기간 동안 다른 프로젝트에 이미 예약된 경우, 40시간이 추가 시간으로 예약되어 초과 예약을 초래할 수 있습니다.

### <a name="remaining-capacity"></a><a name="remaining"></a>남은 생산 능력
잔여 능력 방법은 일정 게시판을 사용하여 프로젝트에 직접 예약하는 경우에만 사용할 수 있습니다. 이 방법은 지정된 날짜 범위 내에서 리소스의 사용 가능한 능력을 예약합니다. 예컨대, 리소스가 주당 40시간의 능력을 가지고 있고 이미 일주일에 10시간을 예약한 경우, 같은 주에 예약하면 해당 주의 남은 30시간 동안 예약이 발생합니다.

### <a name="percentage-capacity"></a><a name="percentage"></a>백분율 생산 능력
백분율 생산 능력 방법은 지정한 종료 날짜에서 시작 날짜까지 능력의 백분율로 리소스를 예약합니다. 예컨대, 리소스에 1일 8시간, 일주일에 5일을 설정하는 달력이 있는 경우 50% 능력의 5 근무일을 포함하는 시작 및 종료 날짜를 설정하면 리소스가 20시간 예약됩니다. 일일 개별 예약은 기간 전체에 걸쳐 균등하게 분포됩니다(이 예에서는 하루 4시간). 예약은 리소스의 남은 능력에 관계 없이 이루어집니다. 리소스가 해당 기간 동안 다른 프로젝트에 이미 예약된 경우, 20시간이 추가 시간으로 예약되어 초과 예약을 초래할 수 있습니다.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>균등 분배 시간
균분 시간 방법은 지정된 시간 동안 리소스를 예약하여 지정된 시작 날짜부터 종료 날짜까지 매일 균등하게 시간을 분배합니다. 예컨대, 5일에 걸쳐 20시간 리소스를 예약하는 경우 이 방법은 하루에 4시간씩 20시간을 균등하게 분배합니다. 예약은 리소스의 남은 능력에 관계 없이 이루어집니다. 리소스가 해당 기간 동안 다른 프로젝트에 이미 예약된 경우, 20시간이 추가 시간으로 예약되어 초과 예약을 초래할 수 있습니다.

### <a name="front-load-hours"></a><a name="front"></a>초기 단계 이익 배분 시간
프론트 로드 시간 방법은 지정된 시간 수를 위해 리소스를 예약하는데, 지정된 시작 날짜부터 종료 날짜에 걸쳐 일당 시간을 프론트 로딩합니다. 프론트 로딩은 리소스의 사용 가능한 능력을 "첫 번째로 소비되는" 순서로 사용합니다. 예컨대, 리소스의 작업 스케줄이 하루 8시간, 주당 5일이고 현재 예약이 없는 경우, 5 근무일 동안 20시간 리소스를 예약하면 다음 일일 예약 패턴이 생성됩니다. 

|                           |    1일    |    2일    |    3일    |    4일    |    5일    |    합계    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **기존 예약**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **새 예약**          |    8        |    8        |    4        |    0        |    0        |    20       |

초기 단계 이익 배분 방법은 기존 예약과 가용 능력을 고려합니다. 예를 들어, 동일한 리소스에 이미 작업 주에 20시간의 예약이 있는 경우 새 예약은 다음과 같이 남은 능력을 사용합니다.

|                     | 1일 | 2일 | 3일 | 4일 | 5일 | 합계 |
|---------------------|-------|-------|-------|-------|-------|-------|
| **기존 예약** | 8     | 8     | 4     | 0     | 0     | 20    |
| **새 예약**       | 0     | 0     | 4     | 8     | 8     | 20    |

가용 능력이 고려되기 때문에 리소스에 예약으로 흡수될 수 있는 남은 능력이 없는 경우 오류 메시지가 표시될 수 있습니다. 이 방법에서는 초과 예약할 수 없습니다.

### <a name="none"></a><a name="none"></a>없음
없음 방법은 프로젝트 내의 **팀** 탭에서 예약하는 경우에만 사용할 수 있습니다. 이 방법은 리소스를 프로젝트의 팀 구성원으로 추가하지만 리소스의 능력을 흡수하는 예약은 생성하지 않습니다. 이 방법은 프로젝트를 만들 때 기본 프로젝트 관리자 팀 구성원이 추가될 때 사용됩니다. 프로젝트를 생성한 프로젝트 관리자 사용자는 기본적으로 프로젝트에 추가되므로 프로젝트 엔터티 레코드에는 소유자가 있고 프로젝트에는 한 명의 승인자가 있습니다. 이 사용자에게는 예약이 없기 때문에 리소스를 예약하려면 삭제한 다음 다른 할당 방법을 사용하여 다시 추가하거나 작업에 리소스를 추가한 다음 **조정** 탭에서 **예약 연장** 을 사용하여 할당을 위한 예약을 만들 수 있습니다.

## <a name="allocation-methods-that-lead-to-overbooking"></a>초과 예약으로 이어지는 할당 방법
요약하면, 다음 할당 방법은 리소스가 이미 다른 프로젝트(또는 다른 작업 주문 또는 예약 가능 엔터티)에서 커밋된 경우 초과 예약으로 이어집니다.

- 전체 능력
- 백분율 능력
- 균등 분배 시간

이러한 세 가지 할당 방법 중 하나를 사용하면 리소스가 초과 예약되었다는 메시지가 표시되지 않습니다. 초과 예약을 수정하려면 스케줄 게시판을 사용해야 합니다.