---
title: 프로젝트 범주 구성
description: 이 항목에서는 프로젝트 범주 설정에 대한 정보를 제공합니다.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 94b66feef4164f3cd52d5fe917071647f731b047
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591550"
---
# <a name="configure-project-categories"></a>프로젝트 범주 구성

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Project Operations는 프로젝트의 수익과 경비를 분류하는 강력한 기능을 제공합니다. 범주는 프로젝트 트랜잭션을 보고 및 분석하고 총계정 원장에 전기하는 기능을 제공합니다.

다음 다이어그램은 트랜잭션 범주, 공유 범주 및 프로젝트 범주 간의 상관 관계를 보여줍니다. 

트랜잭션 범주는 프로젝트 트랜잭션의 기본 그룹입니다. 해당 그룹 내에는 응용 프로그램과 모듈간에 공유할 수 있는 공유 범주 집합이 있습니다. 더 자세히 살펴보면 프로젝트 범주는 가장 세분화된 범주 수준입니다. 프로젝트 범주는 법인, 모듈 및 응용 프로그램에 따라 다릅니다.

![트랜잭션 범주, 공유 범주 및 프로젝트 범주 간의 상관 관계.](media/project-categories.png)

## <a name="transaction-categories"></a>트랜잭션 범주

트랜잭션 범주는 프로젝트 트랜잭션에 대한 기본 그룹을 나타내며 회사 또는 트랜잭션 유형과 관련이 없습니다. 예를 들어 Contoso Robotics는 디자인, 여행, 설치 및 서비스 트랜잭션 범주를 사용하여 프로젝트 트랜잭션을 그룹화합니다.

트랜잭션 범주는 Project Operations 모듈에서 정의됩니다. 
1. **설정** \>**트랜잭션 범주** 로 이동하여 양식을 엽니다. 
2. **새로 만들기** 를 선택하거나 **Excel에서 가져오기** 를 선택하여 새 트랜잭션 범주를 만듭니다.

## <a name="shared-categories"></a>공유 범주

Dynamics 365는 공유 범주 개념을 사용하여 Dynamics 365 Finance, Dynamics 365 Supply Chain 및 Dynamics 365 Project Operations와 같은 다양한 애플리케이션에서 비용을 분류합니다. 생성된 각 트랜잭션 범주에 대해 Project Operations는 시간, 경비, 요금 및 품목의 네 가지 관련 공유 범주를 자동으로 생성합니다. **프로젝트 관리 및 회계** \> **설정** \> **범주** \> **공유 범주** 로 이동하여 공유 범주를 검토하고 조정할 수 있습니다.

## <a name="project-categories"></a>프로젝트 범주

프로젝트 범주는 가장 세분화된 범주 구성 수준을 나타내며 프로젝트 회계사가 각 회사에 대해 별도로 구성해야 합니다.

1. **프로젝트 관리 및 회계** \> **설정** \> **범주** \> **프로젝트 범주** 로 이동합니다.
2. **새로 만들기** 를 선택합니다.
3. 이전 섹션에서 만든 공유 범주의 **범주 ID** 를 선택합니다. Project Operations에서는 트랜잭션 범주와 연관된 공유 범주만 사용할 수 있습니다.
4. 범주 그룹을 선택합니다.

## <a name="category-groups"></a>범주 그룹

범주 그룹은 관련 프로젝트 범주 간에 속성(주로 프로필 게시)을 공유하는 데 사용됩니다. 각 트랜잭션 유형에 대해 하나 이상의 범주 그룹이 있어야 하며 각 프로젝트 범주에는 그룹이 지정됩니다.

Project Operations의 전기 사양은 프로젝트 비용 및 수익 프로필 규칙, 프로젝트 범주 및 범주 그룹에 의해 정의됩니다. **프로젝트 관리 및 회계** \> **설정** \> **범주** \> **범주 그룹** 으로 이동하여 범주 그룹을 설정할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]