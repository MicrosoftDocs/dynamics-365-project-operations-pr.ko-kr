---
title: 2021년 12월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 12월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c4869f3ab06ec80d620ec51bb4f0429412cd4d00
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943031"
---
# <a name="whats-new-december-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 12월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.27.0.195, 4.27.0.242의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.23의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

- 시스템 관리자를 위한 개선된 문제 해결. 사용자가 프로젝트를 열 수 없는 경우 관리자는 [프로젝트 일정 로그](../project-management/schedule-api-logs.md)에서 Project for the Web에서 생성된 라이선스와 관련 없는 오류를 검토할 수 있습니다.
- [Microsoft Project for the Web에서 작업 검사 목록 사용](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for the Web에서 검사 목록을 작업에 추가하여 특정 항목을 추적할 수 있습니다.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 계획 및 추적 | 2392596 | 일정 API는 이제 **남은 작업량**, **완료된 작엽량** 및 **완료율** 필드에 대한 업데이트를 허용합니다. |
| 계획 및 추적 | 2478497 | 일정 API의 **활동 번호** 및 **작업 ID** 필드는 시스템에서 자동 번호 지정을 사용하여 채우기 때문에 입력 시 비어 있을 수 있습니다.|
| 시간 및 경비 | 2468135 | 승인 재시도 횟수가 5회에서 3회로 줄었습니다. |
| 시간 및 경비 | 2468188 | **Annotation** 엔터티의 **notetext** 속성에서 로그 텍스트가 최대 길이를 초과하는 문제를 수정했습니다. |
| 청구 및 가격 책정 | 2488698 | 환경 설정에 재무에서 채워진 원장 엔터티 레코드가 누락된 경우 발생하는 오류 메시지가 업데이트되었습니다. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [587187](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D587187&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225501421%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=qpKECMgKZe9sHGVZUhBxs%2F4ou3fXIiFFg2amMTJ6t9U%3D&amp;reserved=0) | 본지사 수익 계정은 판매세 그룹이 포함되지 않은 **모두 - 전체 라인** 만 고려합니다. |
| 프로젝트 관리 및 회계 | [599568](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599568&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225600986%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=IudfEjWmkNeiTsWmR%2Fu2oR0CnnCkffAshvqZJuF76q8%3D&amp;reserved=0) | 직선 추정치가 잘못 계산되었습니다. |
| 프로젝트 관리 및 회계 | [602728](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227094434%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Q2%2BveFHlGrzg4QHtqcgeqjyZSQkmpr%2Fku7oObKHMB9g%3D&amp;reserved=0) | 적용된 보유자 사례에서 프로젝트 송장 수익에 대한 전기 발행으로 인해 바우처의 거래가 균형을 이루지 않습니다. |
| 프로젝트 관리 및 회계 | [610906](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610906&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=xDBnz10T71GmOZt78ooFK3SYvmTLoC5fj1OftYNYDpY%3D&amp;reserved=0) | Project Operations 실제와의 통합을 위한 성능 개선. |
| 프로젝트 관리 및 회계 | [618670](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D618670&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227203949%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PqvHsTGLcQ3bYbUlzYABYhl7J9v2zbnjcOgm%2FTvXB20%3D&amp;reserved=0) | 시간 비용 트랜잭션이 **원장 전혀 없음** 또는 **원장 없음** 으로 전기된 경우 사용자는 청구서를 작성할 수 없습니다. |
| 프로젝트 관리 및 회계 | [623818](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D623818&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227303517%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=LAfdEiuKG8DoGk8O48MRLuaKYDINhCyMAtrlpGvVAw0%3D&amp;reserved=0) | 저널 게시 중 하나가 실패하고 나머지 저널이 처리되지 않으면 배치 작업이 실패합니다.  |
| 이동 및 경비 | [575378](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575378&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225451644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3tW0ngQqcz8pdNFY8FVuFlsgv3l73HMgeQTLbzIAAOg%3D&amp;reserved=0) | 미첨부 비용 승인 상태는 변경될 수 있습니다. |
| 이동 및 경비 | [592997](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D592997&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225521336%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=0leQsokHcl2NLqePFXC6%2BuH1V5UNRWUIPx0wTUaB4vg%3D&amp;reserved=0) | 워크플로에 제출된 경비 보고서를 사용하면 새로운 경비 라인을 생성할 수 있습니다. |
| 이동 및 경비 | [594853](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D594853&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225541248%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=5PINC45EBeV8PC0Cvtt0QPPJn0VYQ%2FRCjBmlEsZJCq4%3D&amp;reserved=0) | 경비 보고서에서 미전기 경비 라인을 재설정할 수 있습니다. |
| 이동 및 경비 | [599821](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599821&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225610944%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=eb2CAb8L9IUDxDoukDcZQxNyI3TNQtFO%2FcjycucNj44%3D&amp;reserved=0) | 경비 소유자가 직원인 미첨부 경비가 있는 경우 경비 현금 서비스 기능을 활성화할 수 없습니다. |
| 이동 및 경비 | [601446](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601446&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225650767%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Z4CBMqrmYtlIEBWxzMEBf%2BXu5dlst7NnKcQ62yoV%2BWM%3D&amp;reserved=0) | 여행 요청이 null로 설정된 경우 비용 헤더에서 **IsPreAuthorized** 를 활성화하면 안 됩니다. |
| 이동 및 경비 | [601753](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601753&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225660718%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PVwbDhH5uqGJJZTNLddsHYlHsCknK%2FC%2FY%2Btg6fu8heo%3D&amp;reserved=0) | **경비 관리** 의 **청구 가능** 필드 비용은 경비가 저장되면 지워집니다. |
| 이동 및 경비 | [602009](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602009&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225680636%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=t3m29Vkxx8g96CvaDz%2FRzuciP2doP2xejomPl440wNs%3D&amp;reserved=0) | **과세에서 제외** 가 선택된 하위 범주가 있는 항목을 삭제하면 **세금 포함** 슬라이더가 경비 보고서에 대해 **아니요** 로 이동합니다. |
| 이동 및 경비 | [607516](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D607516&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225849894%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2BceTskfUl1kTe2XHk6QSYu9UN%2FE%2F9nP2gv20kVweURA%3D&amp;reserved=0) |회계 이벤트가 비어 있고 회계 상태가 올바르지 않습니다. |
| 이동 및 경비 | [617801](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617801&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919226337756%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=L69x65xY6LQDS1u2sUbVX5QKEYgbDh6lld2Pm%2BSsUyI%3D&amp;reserved=0) | 비용이 신용 카드 거래에서 분할될 때 워크플로가 비용 보고서를 올바르게 평가하지 않습니다. |
| 이동 및 경비 | [575295](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575295&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227074518%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=FyrzO1Yx%2BWLfw5arIrFiW07QZC%2F%2BpUk3ekx3g66X8bE%3D&amp;reserved=0) | 공급업체 은행 거래에 대한 잘못된 보고 통화 금액은 경비 보고서의 마감 기간에 전기됩니다. |
| 이동 및 경비 | [610910](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610910&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=P6wVchjx9GcH7nZ07yg3%2FuEFht6Df7Ew5Z4hSL%2BQ8oY%3D&amp;reserved=0) | 새로워진 경비 보고서 기능에서 경비가 생성될 때 지불 방법이 변경되더라도 비용 라인에 대해 기본 지불 방법이 채워집니다. |
| 이동 및 경비 | [617146](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617146&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227193996%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=134C%2BXGuzA8GmM7ZjWYaiYQfNqnV9a1mEKuzrh0hzpw%3D&amp;reserved=0) | 영수증 정책이 활성화된 경우 경비 보고서를 제출할 수 없습니다. |
| 이동 및 경비 | [619783](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D619783&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227243778%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=pV1rLgOniDy3hXMHAtXeD9o4ZPTmyhZHd7O7zCUpLLs%3D&amp;reserved=0) | 경비 보고서를 제출할 때 다음 오류가 발생합니다. **스택 추적: 회사가 존재하지 않습니다**. |
| 이동 및 경비 | [620773](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D620773&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227253737%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2B5ZZAsXV%2FM29%2Byg6JoGzwJFRa1Fi4NDj4BB38ZeYTH0%3D&amp;reserved=0) | 본지사 경비 라인을 사용하면 첨부되지 않은 거래가 경비 보고서에 다시 추가될 때 분배가 법인을 업데이트하지 않습니다. |
| 이동 및 경비 | [621967](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D621967&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227273644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=RdiupzmL8Dp8nqQIHu9rGMTdJ%2FVVhqN5EIP5uFYS2W4%3D&amp;reserved=0) | 공급업체 거래에서 보고 통화로 표시된 판매 가격 및 금액이 가져온 신용 카드 거래를 사용하여 외화로 생성되고 프로젝트와 연결된 경비 보고서에서 잘못 계산됩니다. |
