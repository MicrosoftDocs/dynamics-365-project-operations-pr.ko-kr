---
title: 프로젝트 복사
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트 복사에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574438"
---
# <a name="copy-a-project"></a>프로젝트 복사

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations를 사용하면 **프로젝트** 양식에서 **프로젝트 복사** 를 선택하여 새 프로젝트를 빠르게 빌드할 수 있습니다. 프로젝트를 복사하려면 복사할 프로젝트를 연 다음 **프로젝트 복사** 를 선택합니다. 이 작업은 다음을 복사합니다.

- 프로젝트 속성 
- 작업 분할 구조
- 프로젝트 팀 구성원
- 프로젝트 추정
- 프로젝트 경비 추정치
- 프로젝트 재료 추정
- 프로젝트 검사 목록
- 프로젝트 버킷

## <a name="project-properties"></a>프로젝트 속성

프로젝트가 복사되면 다음 필드의 값이 복사됩니다.

| 필드 | 비재고 자재용 Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| 고객 님 | :heavy_check_mark: | :heavy_check_mark: | |
| 일정 템플릿 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 통화 | :heavy_check_mark: | :heavy_check_mark: | |
| 계약 단위 | :heavy_check_mark: | :heavy_check_mark: | |
| 담당 회사 | :heavy_check_mark: | | |
| 프로젝트 관리자 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| 전체 프로젝트 상태 | :heavy_check_mark: | :heavy_check_mark: | |
| 댓글 | :heavy_check_mark: | :heavy_check_mark: | |
| 추정 | :heavy_check_mark: | :heavy_check_mark: | |
| <p>예상 시작 날짜</p><p><strong>참고:</strong> 이 필드는 복사본에서 프로젝트가 생성된 날짜를 지정합니다. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>예상 완료 날짜</p><p><strong>참고:</strong> 이 필드의 날짜는 복사본에서 만들어진 새 프로젝트의 시작 날짜를 기준으로 조정됩니다.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| 작업량(시간) | :heavy_check_mark: | :heavy_check_mark: | |
| 예상 노동 비용 | :heavy_check_mark: | :heavy_check_mark: | |
| 예상 경비 비용 | :heavy_check_mark: | :heavy_check_mark: | |
| 예상 재료 비용 | | :heavy_check_mark: | |

> [!NOTE]
> 프로젝트 복사는 장기 실행 작업입니다. 프로젝트 레코드, 관련 속성 및 많은 관련 엔터티도 복사됩니다. 작업의 장기 실행 특성으로 인해 복사가 시작된 후 복사 작업이 완료될 때까지 편집을 위해 대상 프로젝트 페이지가 잠깁니다.

## <a name="work-breakdown-structure"></a>작업 분할 구조

프로젝트를 복사하면 전체 리소스 로드 작업 분할 구조가 복사됩니다. 명명된 리소스가 일반 리소스로 대체됩니다. 명명된 리소스의 작업 시간이 일반 리소스와 동일하지 않은 경우 일정이 다시 계산되고 작업 기간이 변경될 수 있습니다.

## <a name="project-team-members"></a>프로젝트 팀 구성원

원본 프로젝트에서 프로젝트 팀을 복사하면 일반 리소스가 복사됩니다. 일반 리소스 배정은 원본 프로젝트에서와 같이 관리됩니다. 명명된 리소스는 일반 팀 구성원으로 변환됩니다.

> [!NOTE]
> 팀 구성원 및 할당은 Project for the Web에서 복사되지 않습니다.

## <a name="estimates"></a>추정

프로젝트를 복사하면 소스 프로젝트에서 리소스, 경비 및 자재 견적 라인이 복사됩니다. 

프로젝트 복사에 프로그래밍 방식으로 액세스하는 방법에 대한 자세한 내용은 [프로젝트 복사로 프로젝트 템플릿 개발](dev-copy-project.md)을 참조하십시오.

## <a name="quotes-and-contracts"></a>견적 및 계약

견적 및 계약은 대상 프로젝트에 연결되지 않습니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
