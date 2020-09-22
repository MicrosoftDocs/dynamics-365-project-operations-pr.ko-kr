---
title: 작업 및 프로젝트 팀에 일반 예약 가능한 리소스 할당
description: 이 항목은 작업 및 프로젝트 팀에 일반 리소스를 예약하는 것에 대한 정보를 제공합니다.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753371"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

프로젝트에 명명된 리소스 또는 실제 리소스를 예약하고 할당하는 것 외에도 프로젝트 작업에 일반 리소스를 할당할 수 있습니다. 이러한 리소스는 프로젝트에 명명된 리소스로 충원할 준비가 될 때까지 명명된 리소스를 위한 자리 표시자 역할을 할 수 있습니다. 

1. Project Service Automation(PSA)에서 **프로젝트** 페이지를 열고 **스케줄** 탭에서 스케줄의 **리소스** 셀에 일반 리소스의 직함을 입력합니다. 또는 셀의 **리소스** 아이콘을 클릭하여 리소스 선택기를 연 다음 만들려는 일반 리소스의 이름을 입력합니다.

![일반 팀원 생성 및 할당](media/RM-how-to-9.png)

그러면 **빠른 생성: 프로젝트 팀원** 패널이 열립니다. 

2. 일반 리소스 팀원의 역할 및 조직 단위를 입력한 다음 **저장**을 클릭합니다.

![일반 팀원 빠른 생성](media/RM-how-to-10.png)

3. 새 일반 리소스 팀원을 만든 후 작업에 할당합니다. 해당 일반 리소스를 작업 스케줄의 다른 작업에 계속 할당할 수 있습니다.

![기존 일반 팀원을 작업에 할당](media/RM-how-to-11.png)

4. 일반 리소스를 할당한 후 리소스 요건을 생성하고 리소스 관리자에게 리소스 요청을 직접 예약하거나 제출하여 리소스 요건을 충족할 수 있습니다.

![일반 팀원에 대한 요건 생성](media/RM-how-to-12.png)

팀원 그리드에서 위에서 설명한 대로 리소스 선택기를 사용할 수 있을 뿐만 아니라 일반 리소스를 직접 추가할 수도 있습니다. 리소스는 **빠른 생성: 프로젝트 팀원** 패널에 지정된 시작/종료 날짜 및 할당 방법에 근거한 리소스 요건과 함께 추가됩니다.

일반 팀원을 직접 추가한 다음 일반 리소스에 요구되는 시간보다 더 많은 작업을 할당하는 경우 차이점을 확인할 수 있습니다. **요건 생성**을 클릭해 요건을 다시 생성하여 요구되는 시간을 할당과 균형을 맞춥니다.

또한 팀 그리드에서 **리소스 요건** 링크를 클릭하여 요건을 열고 기능, 선호 리소스 등을 추가할 수 있습니다.

![리소스 요구 사항](media/RM-how-to-13.png)

