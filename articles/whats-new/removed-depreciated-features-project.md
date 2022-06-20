---
title: Dynamics 365 Project Operations에서 제거되었거나 사용되지 않는 기능
description: 이 문서에서는 Dynamics 365 Project Operations에서 제거되었거나 제거 예정인 기능에 대해 설명합니다.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921494"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Dynamics 365 Project Operations에서 제거되었거나 사용되지 않는 기능

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 처리 및 재고/생산 기반 시나리오를 위한 Project Operations_

이 문서에서는 Dynamics 365 Project Operations에서 제거되었거나 제거 예정인 기능에 대해 설명합니다.

- *제거된* 기능은 더 이상 제품에서 사용할 수 없습니다.
- *사용되지 않는* 기능은 활성 개발 상태가 아니며 향후 업데이트에서 제거될 수 있습니다.

이 목록은 이러한 기능 제거 및 지원 중단을 대비하는 데 도움을 드리기 위해 작성되었습니다.

> [!NOTE]
> 금융 및 운영 앱의 개체에 대한 자세한 정보는 [**기술 참조 보고서**](/dynamics/s-e/global/axtechrefrep_61)에서 찾을 수 있습니다. 이러한 보고서의 여러 버전을 비교하여 금융 및 운영 앱의 각 버전에서 변경되거나 제거된 개체에 대해 알아볼 수 있습니다.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operations 2022년 3월 릴리스에서 제거되거나 더 이상 사용되지 않는 기능

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>프로젝트 관리 및 회계 "항상 조정 트랜잭션 생성" 매개 변수

| &nbsp; | &nbsp; |
|--------|--------|
| **지원 중단/제거 이유** | 감사 목적을 위해 조정 트랜잭션이 필요합니다. 지원 중단 후 이 매개 변수는 숨겨집니다. 시스템은 매개 변수가 **예** 로 설정된 경우 현재와 같이 항상 조정 트랜잭션을 생성합니다. |
| **다른 기능으로 대체됩니까?** | 없음 |
| **영향을 받는 제품 영역** | 애플리케이션 |
| **배포 옵션** | 생산/재고 시나리오에 대한 Project Operations |
| **상태** | 더 이상 사용되지 않음: 2023년 3월 1일까지 조정 트랜잭션이 항상 생성되도록 매개 변수를 숨기고 시스템 동작을 변경합니다. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>프로젝트 관리 및 회계 "조정 날짜를 새 프로젝트 날짜로 사용" 매개 변수

| &nbsp; | &nbsp; |
|--------|--------|
| **지원 중단/제거 이유** | 이 매개 변수는 원래 회계 기간이 닫힐 때 조정을 허용하는 데 사용되었습니다. 그러나 트랜잭션의 회계 날짜를 구성하면 개설 기간의 첫 번째 날짜로 변경할 수 있으므로 더 이상 필요하지 않습니다. 프로젝트 날짜는 트랜잭션이 발생한 날짜를 나타내므로 변경하면 안 됩니다. |
| **다른 기능으로 대체됩니까?** | 없음 |
| **영향을 받는 제품 영역** | 애플리케이션 |
| **배포 옵션** | 생산/재고 시나리오에 대한 Project Operations |
| **상태** | 더 이상 사용되지 않음: 2023년 3월 1일까지 매개 변수를 숨기고 조정 시 프로젝트 날짜가 변경되지 않도록 시스템 동작을 변경합니다. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>재고/프로덕션 기반 시나리오에 대한 Project Operations의 리소스 요청 워크플로

| &nbsp; | &nbsp; |
|--------|--------|
| **지원 중단/제거 이유** | 낮은 사용량 및 트랜잭션 볼륨 제한으로 인해 더 이상 사용되지 않습니다. |
| **다른 기능으로 대체됩니까?** | 없음 |
| **영향을 받는 제품 영역** | 애플리케이션 |
| **배포 옵션** | 생산/재고 시나리오에 대한 Project Operations |
| **상태** | 더 이상 사용되지 않음: 2023년 3월 1일까지 워크플로를 사용하여 프로젝트에 대한 리소스를 요청하는 옵션을 비활성화합니다. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>헤더 및 라인 보기가 없는 프로젝트 송장 제안 페이지

| &nbsp; | &nbsp; |
|--------|--------|
| **지원 중단/제거 이유** | **헤더 및 라인 보기와 함께 프로젝트 송장 제안 및 송장 일지 양식 사용** 기능 키와 함께 도입된 페이지의 개선 사항으로 인해 더 이상 사용되지 않습니다. |
| **다른 기능으로 대체됩니까?** | 네 |
| **영향을 받는 제품 영역** | 애플리케이션 |
| **배포 옵션** | 생산/비축 시나리오를 위한 Project Operations; 리소스/비재고 시나리오에 대한 Project Operations |
| **상태** | 더 이상 사용되지 않음: 2023년 3월 1일까지 이전(레거시) 페이지를 끄고 기본적으로 **헤더 및 라인 보기와 함께 프로젝트 송장 제안 및 송장 분개장 양식 사용** 기능 키를 켭니다. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Project Operations 2021년 12월 릴리스에서 제거되거나 더 이상 사용되지 않는 기능

### <a name="collaboration-workspaces"></a>공동 작업 작업 영역

[공동 작업 작업 영역 생성 또는 연결(프로젝트)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **지원 중단/제거 이유** | 사용량이 적어 더 이상 사용되지 않습니다. 리소스/비재고 시나리오에 대해 Project Operations를 사용하는 고객은 [ Office 그룹과의 공동 작업](../project-management/collaboration-groups.md)을 활용할 수 있습니다. |
| **다른 기능으로 대체됩니까?** | 없음 |
| **영향을 받는 제품 영역** | 애플리케이션  |
| **배포 옵션** | 생산/재고 시나리오에 대한 Project Operations |
| **상태** | 더 이상 사용되지 않음: 2022년 12월 1일까지 공동 작업 작업 영역을 더 이상 지원하지 않을 계획입니다. |
