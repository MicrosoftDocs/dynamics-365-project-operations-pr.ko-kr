---
title: 프로젝트 자원 예약 성능
description: 이 항목은 많은 프로젝트에 대한 리소스 스케줄링 성능을 개선하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080035"
---
# <a name="project-resource-scheduling-performance"></a>프로젝트 자원 예약 성능

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


리소스 스케줄링과 관련된 성능 문제는 프로젝트 수가 수천 개에 달할 때 발생할 수 있습니다. 리소스 예약 성능을 향상시키기 위해 사용자가 리소스 가용성 양식을 시작하는 데 걸리는 시간을 줄일 수 있는 기능을 사용할 수 있습니다. 특히 이것은 리소스 용량 롤업 동기화 프로세스를 제거하고 **ResProjectResource** 리소스 조회 속도를 높일 수 있습니다. **ResRollup** 테이블은 더 이상 사용되지 않습니다.

> [!IMPORTANT]
> 리소스 용량 롤업 동기화 프로세스 또는 **ResProjectResource** 테이블에 종속성이 있는 경우 이 기능을 사용하지 마십시오.

## <a name="enable-resource-scheduling-performance-enhancement"></a>리소스 스케줄링 성능 향상 활성화
리소스 스케줄링 성능 향상을 사용하려면 다음 단계를 완료하십시오.

1. **기능 관리** > **모두** 로 이동하고 기능 목록에서 **프로젝트 리소스 스케줄링 성능 향상 기능 사용** 을 찾습니다.
2. **지금 사용** 을 선택합니다.

> [!NOTE]
> 목록에서 기능을 찾을 수 없는 경우 **업데이트 확인** 을 선택하여 목록을 새로 고칩니다.

3. 브라우저를 새로 고친 다음 **프로젝트 관리 및 회계** > **주기적** > **프로젝트 리소스** > **모든 회사에서 리소스 캘린더 용량 동기화** 로 이동합니다.
4. **기존 용량 레코드 제거** 를  **예** 로 설정하여 이전 데이터를 제거합니다. 증분 데이터를 생성하려면 **아니요** 로 설정합니다.
5. **기간 코드** 필드에서 데이터를 생성해야 하는 기간을 선택합니다. 기간 코드를 선택하면 시작 날짜와 종료 날짜를 정의할 필요가 없습니다.
6. **기간 코드** 필드가 비어 있는 경우 데이터를 생성할 특정 시작 및 종료 날짜를 선택합니다.
7. **확인** 을 선택합니다.

 > [!NOTE]
 > 이것은 일반 데이터를 사용자 환경에 있는 모든 회사의 **ResCalendarCapacity** 테이블로 배포하며 하나의 법인에서만 실행하면 됩니다. 이 일괄 처리 작업의 데이터는 연관된 달력을 통해 리소스 용량을 계산하는 데 필요합니다.

8. **프로젝트 관리 및 회계** > **주기적** > **프로젝트 리소스** > **모든 회사의 프로젝트 리소스 채우기** 로 이동한 다음 **확인** 을 선택합니다. 이는 **ResProjectResource** , **ResCalendarDateTimeRange** 및 **ResEffectiveDateTimeRange** 테이블에 있는 일반 데이터를 위한 데이터 업그레이드 스크립트입니다. **PSAPRojSchedRole.RootActivity** 필드의 값도 업데이트됩니다. 이것이 실행되지 않으면 리소스 스케줄링 작업을 실행하려고 할 때 경고를 받게 됩니다.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>리소스 스케줄링 성능 향상 끄기

1. **기능 관리** > **모두** 로 이동하고 **프로젝트 리소스 스케줄링 성능 향상 기능 사용** 을 검색합니다.
2. 기능을 선택한 다음 **비활성화** 단추를 선택합니다.
3. 브라우저를 새로 고칩니다.
4. **프로젝트 관리 및 회계** > **주기적** > **용량 동기화** > **리소스 용량 롤업 동기화** 로 이동합니다.
5. **용량 롤업 동기화** 페이지에서 **기존 용량 레코드 제거** 를 **예** 로 설정하여 이전 데이터를 제거합니다. 증분 데이터를 생성하려면 **아니요** 로 설정합니다.
6. **기간 코드** 필드에서 데이터를 생성해야 하는 기간을 선택합니다. 기간 코드를 선택하면 시작 날짜와 종료 날짜를 정의할 필요가 없습니다.
7. **기간 코드** 필드가 비어 있는 경우 데이터를 생성할 특정 시작 및 종료 날짜를 선택합니다.
8. **확인** 을 선택합니다.

> [!NOTE]
> 이것은 일반 데이터를 사용자 환경에 있는 모든 회사의 **ResRollup** 테이블로 배포하며 하나의 법인에서만 실행하면 됩니다. 이 일괄 처리 작업은 모든 **리소스 가용성** 보기에 필요합니다. 이 일괄 처리 작업이 실행되지 않으면 **ResRollup** 데이터는 즉석에서 생성되므로 시간이 걸릴 수 있습니다.
