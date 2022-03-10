---
title: 프로젝트 시간 항목 모바일 작업 영역
description: 이 주제는 프로젝트 시간 항목 모바일 작업 영역에 대한 정보를 제공합니다. 이 작업 영역을 통해 사용자는 모바일 장치를 사용하여 프로젝트를 입력하고 시간을 절약할 수 있습니다.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 04024cc005b67b8f4e5821b22be65cfd1822b2414c85e1fbb75c3b2ac4339dc4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989559"
---
# <a name="project-time-entry-mobile-workspace"></a>프로젝트 시간 항목 모바일 작업 영역

[!include [banner](../includes/banner.md)]

이 주제는 **프로젝트 시간 항목** 모바일 작업 영역에 대한 정보를 제공합니다. 이 작업 영역을 통해 사용자는 모바일 장치를 사용하여 프로젝트를 입력하고 시간을 절약할 수 있습니다.

이 모바일 작업 영역은 Dynamics 365 Unified Ops 모바일 앱과 함께 사용하기 위한 것입니다. 

## <a name="overview"></a>개요
일상 업무의 일부로 프로젝트 리소스는 종종 현장에 있거나 이동합니다. **프로젝트 시간 항목** 모바일 작업 영역을 통해 사용자는 선택한 모바일 장치에서 프로젝트에 대해 청구 가능 또는 청구 불가능 시간을 입력할 수 있습니다. 따라서 프로젝트 리소스는 언제 어디서나 시간 항목을 기록할 수 있습니다. 이미 기록된 시간 항목을 볼 수도 있습니다. 

특히 **프로젝트 시간 항목** 모바일 작업 영역에서 사용자는 다음 작업을 수행할 수 있습니다.

-   선택한 날짜에 대해 특정 작업에 소요한 시간을 입력합니다.
-   프로젝트 이름 또는 고객으로 검색하여 시간을 입력할 프로젝트를 찾습니다.
-   소비한 시간에 대한 범주와 활동을 지정합니다.
-   프로젝트에 대해 청구 가능 또는 청구 불가능으로 시간을 기록합니다.
-   선택적으로 외부 또는 내부 설명을 입력합니다.

## <a name="prerequisites"></a>필수 구성 요소
필수 구성 요소는 조직에 배포된 Microsoft Dynamics 365 버전에 따라 다릅니다.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance를 사용하는 경우 필수 구성 요소
Finance가 조직에 배포된 경우 시스템 관리자는 **프로젝트 시간 항목** 모바일 작업 영역을 게시해야 합니다. 지침은 [모바일 작업 영역 게시](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace)를 참조하십시오.

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>플랫폼 업데이트 3 이상과 함께 버전 1611을 사용하는 경우 필수 구성 요소
플랫폼 업데이트 3 이상의 버전 1611이 조직에 배포된 경우 시스템 관리자는 다음 필수 구성 요소를 완료해야 합니다. 

<table>
<thead>
<tr class="header">
<th>필수 구성 요소</th>
<th>역할</th>
<th>설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>KB 4018050을 구현합니다.</td>
<td>시스템 관리자</td>
<td>KB 4018050은 <strong>프로젝트 시간 항목</strong> 모바일 작업 영역이 포함된 X++ 업데이트 또는 메타데이터 핫픽스입니다. KB 4018050을 구현하려면 시스템 관리자가 다음 단계를 따라야 합니다.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services(LCS)에서 메타데이터 핫픽스를 다운로드합니다</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">메타데이터 핫픽스를 설치합니다</a>.</li>
<li><strong>ApplicationSuite</strong> 및 <strong>ProjectMobile</strong> 모델을 포함하는 <a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">배포 가능한 패키지를 생성</a>한 다음 배포 가능한 패키지를 LCS에 업로드합니다.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">배포 가능한 패키지를 적용합니다</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>프로젝트 시간 항목</strong> 모바일 작업 영역을 게시합니다.</td>
<td>시스템 관리자</td>
<td><a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">모바일 작업 영역 게시</a>를 참조하십시오.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>모바일 앱을 다운로드하여 설치합니다.

Finance and Operations 모바일 앱을 다운로드하여 설치합니다.

-   [Android 휴대폰의 경우](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhones의 경우](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>모바일 앱에 로그인
1.  모바일 장치에서 앱을 시작합니다.
2.  Dynamics 365 URL을 입력합니다.
3.  처음 로그인하면 사용자 이름과 암호를 입력하라는 메시지가 표시됩니다. 자격 증명을 입력합니다.
4.  로그인하면 회사에서 사용할 수 있는 작업 영역이 표시됩니다. 시스템 관리자가 나중에 새 작업 영역을 게시하는 경우 모바일 작업 영역 목록을 새로 고쳐야 합니다.

[![당겨서 새로 고침.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>프로젝트 시간 항목 모바일 작업 영역을 사용하여 시간 입력
1.  모바일 장치에서 **프로젝트 시간 항목** 작업 영역을 선택합니다.
2.  **시간 항목** 을 선택합니다. 현재 주의 일정 날짜가 표시됩니다.
3.  선택한 날짜에 대해 **작업** &gt; **새로운 항목** 을 선택합니다.
4.  기록할 시간 수를 입력합니다.
5.  시간 입력을 위한 프로젝트를 선택합니다. 오프라인 사용을 위해 앱에 로드된 프로젝트가 목록에 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)을 참조하십시오.
6.  프로젝트가 목록에 없으면 **검색** 을 선택합니다. 이름으로 검색하거나 프로젝트 이름 또는 고객으로 검색하도록 전환합니다.
7.  범주를 선택합니다. 오프라인 사용을 위해 앱에 로드된 범주가 목록에 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)을 참조하십시오.
8.  범주가 목록에 없으면 **검색** 을 선택합니다. 범주별로 검색하거나 범주 이름으로 검색하도록 전환합니다.
9.  활동을 선택하십시오. 오프라인 사용을 위해 앱에 로드된 활동이 목록에 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)을 참조하십시오.
10. 활동이 목록에 없으면 **검색** 을 선택합니다. 활동 번호로 검색하거나 용도별로 검색하도록 전환합니다.

11. 라인 속성을 선택합니다.
12. 선택적으로 외부 및 내부 설명을 입력합니다.
13. **완료** 를 선택합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]