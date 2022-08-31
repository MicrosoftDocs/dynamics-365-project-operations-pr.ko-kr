---
title: 계약 근로자와 하도급 계약 용량을 표시하도록 일정 게시판 구성
description: 이 문서에서는 프로젝트 리소스 요구 사항에 인력을 배치할 때 하도급 계약 리소스 용량을 표시하도록 Microsoft Dynamics 365 Project Operations의 일정 게시판을 구성하는 방법에 대해 설명합니다.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262225"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>계약 근로자와 하도급 계약 용량을 표시하도록 일정 게시판 구성 

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Microsoft Dynamics 365 Project Operations의 일정 게시판은 두 가지 방법으로 리소스 검색에 사용할 수 있습니다.

- 특정 프로젝트 기반 리소스 요구 사항의 컨텍스트 없이 일반 리소스 검색.
- 프로젝트 요구 사항이 제안된 리소스에 대한 컨텍스트를 제공하는 요구 사항별 리소스 검색입니다.

일정 게시판에 하도급 계약 리소스 용량 및 계약 작업자를 알리려면 일정 게시판 설정을 업데이트해야 합니다. 이러한 업데이트에는 다음이 포함됩니다. 
- 일반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.
- 요구 사항 기반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>일반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.
### <a name="update-filters-for-general-resource-search"></a>일반 리소스 검색용 업데이트 필터
리소스를 검색할 때 다음 중 일부 또는 전체를 지정하여 외부 리소스도 검색할 수 있도록 일정 게시판에서 사용 가능한 필터를 업데이트해야 합니다.
  - 작업자 유형(표시된 리소스가 계약직 작업자인지 직원이어야 하는지 여부).
  - 리소스가 속해야 하는 공급업체 회사입니다.
  - 특정 하도급 계약 또는 하도급 계약 내용에 속하는 리소스.
    
### <a name="update-retrieve-resource-query"></a>검색 리소스 쿼리 업데이트
검색에 사용되는 쿼리도 이러한 추가 필터 속성을 사용하도록 업데이트해야 합니다. 다음 단계를 사용하여 일반 리소스 검색을 위한 일정 게시판 구성을 업데이트합니다.  
1. 특정 일정 게시판에 대한 **일정 게시판 설정** 을 엽니다.
2. **일반 설정** 탭을 열고 **기타 설정** 으로 스크롤합니다.
3. 이 섹션의 설정 목록에서 **필터 레이아웃** 을 **Project Operations 라이트의 기본 필터 레이아웃** 으로 업데이트합니다.
4. **리소스 검색 쿼리** 를 **Project Operations 라이트에 대한 기본 리소스 검색 쿼리** 로 업데이트합니다.

![일반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>요구 사항 기반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.
### <a name="update-filters-for-requirement-specific-resource-search"></a>요구 사항 특정 리소스 검색용 업데이트 필터 
리소스를 검색할 때 다음 중 일부 또는 전체를 지정하여 외부 리소스도 검색할 수 있도록 일정 게시판에서 사용 가능한 필터를 업데이트해야 합니다.
 - 작업자 유형(표시된 리소스가 계약직 작업자인지 직원이어야 하는지 여부).
 - 리소스가 속해야 하는 공급업체 회사입니다.
 - 특정 하도급 계약 또는 하도급 계약 내용에 속하는 리소스.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>요구 사항별 리소스 검색을 위한 검색 리소스 쿼리 업데이트 
검색에 사용되는 쿼리도 이러한 추가 필터 속성을 사용하도록 업데이트해야 합니다. 다음 단계를 사용하여 요구 사항 기반 리소스 검색을 위한 일정 게시판 구성을 업데이트합니다.

1. 특정 일정 게시판에 대한 **일정 게시판 설정** 을 연 다음 **기본 설정 열기** 를 선택하여 요구 사항별 검색 설정을 엽니다.
2. **일반 설정** 탭을 열고 **기타 설정** 으로 스크롤합니다.
3. 이 섹션의 설정 목록에서 **필터 레이아웃** 을 **Project Operations 라이트의 기본 필터 레이아웃** 으로 업데이트합니다.
4. **리소스 검색 쿼리** 를 **Project Operations 라이트에 대한 기본 리소스 검색 쿼리** 로 업데이트합니다.
5. **일정 유형** 탭으로 이동하여 **프로젝트** 로 이동합니다.
6. **프로젝트** 설정에서 **일정 도우미 리소스 검색 쿼리** 를 **Project Operations 라이트의 기본 리소스 검색 쿼리** 로 업데이트하고 **일정 도우미 검색 제약 조건 쿼리** 를 **Project Operations 라이트의 기본 검색 제약 조건 쿼리** 로 업데이트합니다.

![요구 사항 기반 리소스 검색을 위한 일정 게시판 설정을 업데이트합니다.](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
