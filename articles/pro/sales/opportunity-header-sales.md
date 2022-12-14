---
title: 프로젝트 영업 기회에 대한 헤더 세부 사항
description: 이 문서에서는 프로젝트 기반 거래 및 프로젝트 기반 영업 기회 라인에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec332e2fb97436d7ec3d31b75ee2383edcb5c7e4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824588"
---
# <a name="header-details-for-project-opportunities"></a>프로젝트 영업 기회에 대한 헤더 세부 사항

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

영업 기회 헤더는 프로젝트 기반 영업 기회의 모든 라인에 적용되는 프로젝트 기반 트랜잭션에 대한 전체 정보를 캡처합니다.

Dynamics 365 Project Operations의 프로젝트 기반 영업 기회는 Dynamics 365 Sales의 영업 기회에 대한 확장입니다. 이러한 확장은 프로젝트 기반 영업 기회에 고유하고 필요한 추가 기능을 제공합니다. 이러한 확장에는 프로젝트 기반 영업 기회에서 사용할 수 있는 새 필드 및 리본 작업이 포함될 수 있습니다. 영업에서 사용할 수 있는 일부 필드, 기능 및 기본값 설정 논리는 Project Operations에서 사용할 수 없습니다.

다음 표에는 Project Operations에 고유하거나 영업 기회의 동작에 몇 가지 중요한 변경 사항이 있는 프로젝트 기반 영업 기회의 필드가 포함되어 있습니다.

| **필드** | **위치** | **설명** | **다운스트림 영향** |
| --- | --- | --- | --- |
| 종류 | 일반 탭(숨김) | 이 옵션 집합 필드에는 다음 옵션이 있습니다.</br>- 작업 기반(Project Operations가 설치된 경우에만 사용 가능)</br>- 항목 기반(Project Operations 및 Sales가 설치된 경우에만 사용 가능)</br>- 서비스 유지 보수 기반(Field Service가 설치된 경우 사용 가능) | Project Operations를 사용하는 경우 이 필드 값은 영업 기회를 프로젝트 기반으로 분류하는 **작업 기반** 으로 자동 설정됩니다. 이 거래에 대한 다운스트림 판매 프로세스에서 모든 프로젝트별 확장 및 기능을 활성화하려면 영업 기회는 프로젝트 기반이어야 합니다. |
| 연락처 | 일반 탭 | 이 거래에 대한 고객의 기본 연락처를 참조합니다. | |
| 계정 | 일반 탭 | 고객의 회사 또는 거래처 레코드에 대한 참조입니다. | |
| 거래처 관리자 | 일반 탭 | 이 프로젝트 기반 영업 기회에 대한 거래처 관리자의 이름입니다. | 거래처 관리자는 이 프로젝트 완료를 통해 고객과의 관계를 관리할 책임이 있습니다. 거래처 관리자와 연결된 예약 가능한 리소스 레코드를 기반으로 계약 단위의 기본값이 정해집니다. |
| 계약 단위 | 일반 탭 | 이 거래와 관련된 프로젝트 또는 프로젝트의 제공을 담당하는 조직 구성 단위입니다. | 계약 단위는 거래가 완료된 후 프로젝트를 완료할 회사의 부서입니다. 모든 계약 단위에는 통화가 있으며 이 통화는 프로젝트 중에 발생한 예상 비용과 실제 비용을 보고하는 데 사용됩니다. |

영업 기회의 **요약** 탭에 있는 다른 모든 필드와 섹션의 경우 [영업 기회 만들기 또는 편집(영업 및 영업 허브)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)을 참조하십시오.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
