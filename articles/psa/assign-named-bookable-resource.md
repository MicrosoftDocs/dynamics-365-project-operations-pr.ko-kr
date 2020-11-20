---
title: 프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정
description: 이 항목은 프로젝트 팀에 명명된 리소스를 예약하는 것과 작업에 배정하는 방법에 대한 정보를 제공합니다.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130181"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

명명된 리소스를 팀에 직접 예약하여 프로젝트 팀에 추가할 수 있습니다. 이렇게 하려면 다음 단계를 완료합니다.

1. Project Service Automation에서 **프로젝트** 로 가서, 예약할 프로젝트 열기를 선택합니다.
2. **프로젝트** 페이지의 **팀** 탭에서 **신규** 를 클릭합니다. 

![팀 탭에서 팀원 추가](media/RM-how-to-1.png)

3. **프로젝트 팀원 빠른 생성** 대화 상자에서 예약 가능한 리소스를 선택합니다. **역할** 필드가 배정된 경우 리소스의 기본 역할로 채워집니다. 필요한 경우 역할을 변경할 수 있습니다. 
4. 리소스가 필요한 시작 날짜와 끝 날짜를 선택하고 리소스 능력의 배정 방법을 선택합니다. 
5. 팀원을 프로젝트 결재자로 지정하려면 **프로젝트 결재자** 필드에서 **예** 를 선택합니다. 즉, 팀원이 이 프로젝트를 위해 제출된 시간 및 경비 항목을 결재할 수 있습니다. 
6. **저장** 을 클릭합니다.

![빠른 생성 양식에 팀원 추가](media/RM-how-to-2.png)


이제 예약된 리소스를 프로젝트의 작업에 배정할 수 있습니다. **프로젝트** 페이지에서 **스케줄** 탭을 클릭하여 새 리소스에 작업을 배정합니다. 작업 그리드의 **리소스** 필드에서 시작된 리소스 선택기에 선택할 수 있는 팀원들이 표시됩니다.

![스케줄 탭의 작업에 팀원 배정](media/RM-how-to-3.png)

Project Service Automation (PSA)의 버전 3에서는 리소스 예약과 작업 배정이 밀접하게 결합되어 있지 않습니다. 즉, 스케줄에서 리소스 선택기를 사용할 때 프로젝트에서 예약이 다루는 것보다 더 많은 시간 동안 팀원에게 작업을 배정할 수 있습니다.
팀원 예약과 배정 사이의 차이점은 **팀** 탭에서 또는 **리소스 조정** 탭에서 확인할 수 있습니다. 또한 리소스에 대한 예약과 배정 사이의 차이를 보다 상세한 수준에서 조정할 수 있습니다.

![리소스 조정 탭](media/RM-how-to-4.png)

또한 **스케줄** 탭에서 리소스 선택기를 사용하여 아직 프로젝트 팀에 속하지 않은 예약 가능한 리소스를 검색하고 선택할 수 있습니다. 그들은 리소스 선택기에서 **기타 리소스** 로 표시됩니다.

![팀원이 아닌 리소스를 작업에 배정](media/RM-how-to-5.png)

이렇게 하면 리소스가 프로젝트 팀에 추가되고 작업에 배정되지만 예약은 생성되지 않습니다.

![배정되었지만 예약이 없는 팀원](media/RM-how-to-6.png)

**조정** 탭의 확장 예약 기능 또는 **스케줄 게시판** 을 사용하여 프로젝트에 리소스의 능력을 예약할 수 있습니다.

![리소스 조정 탭에서 팀원에 대한 예약 연장](media/RM-how-to-7.png)

프로젝트에 팀원을 예약한 후 예약 정비를 사용하거나 스케줄 게시판을 사용하여 예약을 직접 관리할 수 있습니다.
