---
title: 리소스 할당 만들기
description: 이 항목은 일반 및 명명된 리소스 할당 만들기에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906237"
---
# <a name="create-resource-assignments"></a>리소스 할당 만들기

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


리소스 할당은 프로젝트 팀 구성원을 리프 노드 작업에 직접 연결하는 것입니다. 이 항목은 리소스를 할당하는 다른 방법에 대한 정보를 제공합니다.

## <a name="create-a-generic-team-member-through-task-assignment"></a>작업 할당을 통한 일반 팀원 생성


작업 할당을 통해 일반 팀 구성원을 만들 때 자리 표시자 또는 일반 리소스를 만듭니다. 이 일반 리소스는 궁극적으로 작업을 수행하려는 명명된 리소스의 특성을 설명합니다. 그런 다음 명명된 리소스를 검색하고 예약하는 데 사용되는 요건을 생성하거나 요건을 사용하여 요청을 제출합니다.

1. 작업의 일정 그리드에서 **리소스** 셀에 있는 리소스 아이콘을 선택합니다.
2. 자리 표시자 리소스 이름으로 사용할 이름을 입력합니다. 예: 프로그램 관리자.
3. **생성**을 선택하고 **프로젝트 팀원 빠른 생성** 필드에서 일반 리소스에 대한 역할을 설정합니다.
4. 작업에 대한 **리소스 선택기**에서 리소스를 선택하여 필요하면 이 자리 표시자 리소스에 작업을 할당합니다. **팀원** 아래에 리소스가 나열됩니다.
5. 일반 리소스 할당을 마쳤으면 **팀** 탭에서 일반 리소스를 선택하고 **요구 사항 생성**을 선택하여 일반 리소스에 대한 리소스 요구 사항을 만듭니다.
6. 일반 리소스에 대해 **예약**을 선택한 다음 일정 게시판을 사용하여 실제 리소스를 찾고 예약합니다. 리소스 관리자가 이행 요구 사항을 제출할 수도 있습니다.
7. 명명된 리소스를 사용하여 일반 리소스가 완전히 충족되면(부분 리소스 요구 사항 충족으로 리소스 할당이 발생하지 않음) 일반 리소스가 팀에서 제거됩니다. 일반 리소스에 대한 작업 할당은 일반 리소스의 리소스 요구 사항을 충족하는 명명된 리소스에 할당됩니다.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>예약 가능한 모든 리소스 목록에서 명명된 리소스 할당

**리소스 선택기**의 검색 상자를 사용하여 예약 가능한 모든 활성 리소스를 검색하고 리프 노드 작업에 할당할 수 있습니다. 이 방법으로 할당된 리소스는 예약 없이 팀에 추가됩니다. 이는 팀원을 추가하고 **없음**을 할당 방법으로 선택하는 것과 유사합니다. 리소스는 **팀**, **리소스 할당** 및 **조정** 탭에 할당 및 예약 부족만 있는 리소스로 표시됩니다. 가용성을 사용하려면 예약합니다.

1. 작업 그리드, 게시판 또는 시간 표시줄에서 **할당 대상** 셀로 이동합니다.
2. 검색 상자에 이름을 입력합니다. 이름에 대한 검색 결과는 **리소스 선택기**의 **기타 리소스**에 표시됩니다.
3. 작업에 할당할 리소스를 선택하거나 **기타 팀 리소스** 아래에서 리소스 이름을 선택합니다.
