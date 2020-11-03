---
title: 경비 관리 모바일 작업 영역
description: 이 주제는 경비 관리 모바일 작업 영역에 대한 정보를 제공합니다. 이 작업 영역에서는 사용자가 영수증을 캡처하고 업로드할 수 있으므로 나중에 경비 보고서에 첨부할 수 있습니다. 또한 사용자는 첨부된 영수증을 사용하여 비용 라인을 신속하게 생성하고 비용 보고서를 생성 및 관리할 수 있습니다.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 080c086dc4059d8efe5075162aabf70ac1068a21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080211"
---
# <a name="expense-management-mobile-workspace"></a>경비 관리 모바일 작업 영역

[!include [banner](../includes/banner.md)]

이 주제는 **경비 관리** 모바일 작업 영역에 대한 정보를 제공합니다. 이 작업 영역에서는 사용자가 영수증을 캡처하고 업로드할 수 있으므로 나중에 경비 보고서에 첨부할 수 있습니다. 또한 사용자는 첨부된 영수증을 사용하여 비용 라인을 신속하게 생성하고 비용 보고서를 생성 및 관리할 수 있습니다. 또한 승인자는 **경비 관리** 모바일 작업 영역을 사용하여 할당된 경비 보고서를 보고 해당 경비 보고서를 승인하거나 거부할 수 있습니다.


이 모바일 작업 영역은 Dynamics 365 Unified Ops 모바일 앱과 함께 사용하기 위한 것입니다.


## <a name="overview"></a>개요

많은 조직에서는 직원이 환급을 위해 제출하는 여행 관련 또는 비즈니스 관련 경비 보고서에 영수증 사본을 첨부하도록 요구합니다. **경비 관리** 모바일 작업 영역을 사용하면 첨부된 영수증 사진을 사용하여 선택한 모바일 장치에서 새로운 비용 라인을 빠르게 만들 수 있습니다. 또는 사용자는 영수증 사진을 캡처한 다음 나중에 경비 보고서에 첨부할 수 있습니다. 직원은 또한 비용 보고서를 작성 및 관리한 다음 모바일 장치를 사용하여 승인 및 상환을 위해 제출할 수 있습니다.


특히 **경비 관리** 모바일 작업 영역을 통해 사용자는 다음 작업을 수행할 수 있습니다.

- 영수증 사진을 찍어 Dynamics 365 Finance에 업로드합니다. 그런 다음 나중에 해당 사진을 경비 보고서에 첨부할 수 있습니다.
- 캡처된 영수증으로 파일을 업로드합니다. 그런 다음 나중에 해당 파일을 경비 보고서에 첨부할 수 있습니다.
- 첨부된 영수증을 사용하여 신규 비용 라인을 생성합니다. 그런 다음 나중에 경비 보고서에 개별 항목을 추가하고 승인 및 환급을 위해 제출할 수 있습니다.

다음 기능을 사용할 수 있습니다.

- 새 경비 보고서를 만듭니다.
- 신용 카드 거래 및 이전에 생성된 기타 경비를 경비 보고서에 첨부합니다.
- 경비 보고서에 대한 새 경비를 생성합니다.
- 영수증 사진을 찍거나 파일을 캡처된 영수증으로 업로드하여 경비 보고서에 대한 모든 비용에 영수증을 첨부합니다.
- 회사의 경비 정책에 따라 경비에 게스트 목록을 추가합니다.
- 회사의 경비 정책에 따라 경비를 항목별로 구분합니다.
- 승인 및 상환을 위해 경비 보고서를 제출합니다.
- 할당된 승인자인 경우 경비 보고서를 승인하거나 거부합니다.

## <a name="prerequisites"></a>필수 구성 요소
필수 구성 요소는 조직에 배포된 버전에 따라 다릅니다.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance를 사용하는 경우 필수 구성 요소 
Finance가 조직에 배포된 경우 시스템 관리자는 **경비 관리** 모바일 작업 영역을 게시해야 합니다. 지침은 [모바일 작업 영역 게시](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace)를 참조하십시오.

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
<td>KB 4019015를 구현합니다.</td>
<td>시스템 관리자</td>
<td>KB 4019015는 <strong>경비 관리</strong> 모바일 작업 영역이 포함된 X++ 업데이트 또는 메타데이터 핫픽스입니다. KB 4019015를 구현하려면 시스템 관리자가 다음 단계를 따라야 합니다.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Microsoft Dynamics Lifecycle Services(LCS)에서 메타데이터 핫픽스를 다운로드합니다</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">메타데이터 핫픽스를 설치합니다</a>.</li>
<li><strong>ApplicationSuite</strong> 및 <strong>ExpenseMobile</strong> 모델을 포함하는 <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">배포 가능한 패키지를 생성</a>한 다음 배포 가능한 패키지를 LCS에 업로드합니다.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">배포 가능한 패키지를 적용합니다</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>경비 관리</strong> 모바일 작업 영역을 게시합니다.</td>
<td>시스템 관리자</td>
<td><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">모바일 작업 영역 게시</a>를 참조하십시오.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations 모바일 앱을 다운로드하여 설치합니다.
Dynamics 365 Unified Ops 모바일 앱 다운로드 및 설치:

- [Android 휴대폰의 경우](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhones의 경우](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>모바일 앱에 로그인
1. 모바일 장치에서 앱을 시작합니다.
2. Dynamics 365 URL을 입력합니다.
4. 처음 로그인하면 사용자 이름과 암호를 입력하라는 메시지가 표시됩니다. 자격 증명을 입력합니다.
5. 로그인하면 회사에서 사용할 수 있는 작업 영역이 표시됩니다. 시스템 관리자가 나중에 새 작업 영역을 게시하는 경우 모바일 작업 영역 목록을 새로 고쳐야 합니다.


[![당겨서 새로 고침](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>경비 관리 모바일 작업 영역을 사용하여 영수증 캡처

1. 모바일 장치에서 **경비 관리** 작업 영역을 엽니다.
2. **영수증 캡처** 를 선택합니다.
3. **사진 찍기** 또는 **이미지 선택** 을 선택합니다.
4. 다음 단계 중 하나를 수행합니다.

    - **사진 찍기** 를 선택한 경우 다음 단계를 수행하십시오.

        1. 영수증 사진을 찍을 수 있도록 모바일 장치의 카메라로 이동합니다. 사진 촬영이 끝나면 **확인** 을 선택하여 사진을 수락합니다.
        2. 선택 사항: 사진의 이름을 입력하고 메모를 입력합니다.

    - **이미지 선택** 을 선택한 경우 다음 단계를 수행하십시오.

        1. 목록에서 이미지를 선택합니다.
        2. 선택 사항: 이미지의 이름을 입력하고 메모를 입력합니다.

5. **완료** 를 선택합니다.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>경비 관리 모바일 작업 영역을 사용하여 경비를 신속하게 입력합니다.
1. 모바일 장치에서 **경비 관리** 작업 영역을 엽니다.
2. **빠른 경비 입력** 을 선택합니다.
3. 경비 범주를 선택합니다. 오프라인 사용을 위해 앱에 로드된 경비 범주 목록이 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 범주가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 경비 범주별로 검색하거나 경비 유형으로 검색하도록 전환합니다.
4. 경비의 트랜잭션 날짜를 입력합니다.
5. 선택 사항: 비경비에 대한 판매자를 입력합니다.
6. 경비 금액을 입력합니다.
7. 경비의 통화를 선택합니다. 오프라인 사용을 위해 앱에 로드된 통화 코드 목록이 표시됩니다. 기본적으로 400개의 통화가 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 통화가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 통화별로 검색하거나 이름으로 검색하도록 전환합니다.
8. **사진 찍기** 또는 **이미지 선택** 을 선택합니다.
9. 다음 단계 중 하나를 수행합니다.

    - **사진 찍기** 를 선택한 경우 영수증 사진을 찍을 수 있도록 모바일 장치의 카메라로 이동합니다. 사진 촬영이 끝나면 **확인** 을 선택하여 사진을 수락합니다.
    - **이미지 선택** 을 선택한 경우 목록에서 이미지를 선택합니다.

10. **완료** 를 선택합니다.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>경비 관리 모바일 작업 영역을 사용하여 경비 보고서를 승인합니다(2017년 7월 업데이트를 사용하는 경우).
1. 모바일 장치에서 **경비 관리** 작업 영역을 엽니다.
2. **경비 승인** 은 승인을 위해 할당된 경비 보고서의 수를 보여줍니다. 이 숫자는 약 30분마다 업데이트됩니다. **경비 승인** 을 선택합니다.

    승인을 위해 할당된 경비 보고서의 목록이 표시됩니다.
    
3. 경비 세부 사항을 보려면 경비 보고서를 선택합니다.
4. 경비 세부 사항을 보려면 경비를 선택합니다. 경비에 대해 표시되는 정보에는 영수증, 게스트 및 항목 세부 정보가 포함됩니다.
5. 다시 **경비 보고서** 페이지에서 경비 보고서를 승인할지 거부할지를 선택합니다.
6. 승인 조치에 대한 설명을 입력합니다.
7. **완료** 를 선택합니다.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>새 경비 보고서를 만들고 경비 관리 모바일 작업 영역을 사용하여 승인을 받기 위해 제출합니다(2017년 7월 업데이트를 사용하는 경우).
1. 모바일 장치에서 **경비 관리** 작업 영역을 엽니다.
2. **경비 입력** 을 선택합니다.
3. **새로운 보고서** 를 클릭하거나 목록에서 기존 경비 보고서를 선택합니다.
4. 새 경비 보고서의 경우 목적과 사용 가능한 추가 정보를 입력합니다. 이 정보는 회사에 대한 경비 관리 구성 방식에 따라 다릅니다.
5. **완료** 를 선택합니다.
6. 신용 카드 거래와 같은 기존 경비를 경비 보고서에 추가하려면 **첨부** 를 선택합니다.
7. 목록에서 하나 이상의 경비를 선택합니다.
8. **완료** 를 선택합니다.
9. 경비 보고서에 새 경비를 추가하려면 **새 경비** 를 선택합니다.
10. 경비 범주를 선택합니다. 오프라인 사용을 위해 앱에 로드된 경비 범주 목록이 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 범주가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 경비 범주별로 검색하거나 경비 유형으로 검색하도록 전환합니다.
11. 선택 사항: 비경비에 대한 판매자를 입력합니다.
12. 경비의 트랜잭션 날짜를 입력합니다.
13. 경비 금액을 입력합니다.
14. 경비의 통화를 선택합니다. 오프라인 사용을 위해 앱에 로드된 통화 코드 목록이 표시됩니다. 기본적으로 400개의 통화가 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 통화가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 통화별로 검색하거나 이름으로 검색하도록 전환합니다.
15. **완료** 를 선택합니다.
16. 경비에 더 많은 세부 정보를 추가하려면 **세부 사항 추가** 를 선택합니다. 사용 가능한 필드는 회사의 경비 관리 구성에 따라 다릅니다.
17. 회사 정책에 경비 영수증이 필요한 경우 **영수증** 을 선택하고 다음 단계를 수행하십시오.

    1. **영수증 캡처** 또는 **영수증 첨부** 를 선택합니다.
    2. 다음 단계 중 하나를 수행합니다.

        - **영수증 캡처** 를 선택한 경우 다음 단계를 수행하십시오.

            1. **사진 찍기** 또는 **이미지 선택** 을 선택합니다.
            2. 다음 단계 중 하나를 수행합니다.

                - **사진 찍기** 를 선택한 경우 다음 단계를 수행하십시오.

                    1. 영수증 사진을 찍을 수 있도록 모바일 장치의 카메라로 이동합니다. 사진 촬영이 끝나면 **확인** 을 선택하여 사진을 수락합니다.
                    2. 선택 사항: 사진의 이름을 입력하고 메모를 입력합니다.

                - **이미지 선택** 을 선택한 경우 다음 단계를 수행하십시오.

                    1. 목록에서 이미지를 선택합니다.
                    2. 선택 사항: 이미지의 이름을 입력하고 메모를 입력합니다.

            3.  **완료** 를 선택합니다.

        - **영수증 첨부** 를 선택한 경우 다음 단계를 수행하십시오.

            1.  목록에서 하나 이상의 이미지를 선택합니다.
            2.  **완료** 를 선택합니다.

    3. **뒤로** 단추를 눌러 경비 세부 정보로 돌아갑니다.

18. 회사 정책에 경비 게스트가 필요한 경우 **게스트** 를 선택하고 다음 단계를 수행하십시오.

    1. **게스트** , **이전 게스트** 또는 **동료** 를 선택합니다.
    2. 다음 단계 중 하나를 수행합니다.

        - **게스트** 를 선택한 경우 다음 단계를 수행하십시오.

            1. 게스트의 이름을 입력합니다.
            2. 선택 사항: 게스트의 조직 및/또는 국가를 입력합니다.
            3. 선택 사항: 게스트의 제목을 입력합니다.
            4. **완료** 를 선택합니다.

        - **이전 게스트** 를 선택한 경우 다음 단계를 수행하십시오.

            1. 목록에서 하나 이상의 이전 게스트를 선택합니다. 오프라인 사용을 위해 앱에 로드된 이전 경비 보고서에 추가한 이전 게스트 목록이 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 이전 게스트가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 이름으로 검색하거나 조직, 국가 또는 제목으로 검색하도록 전환합니다.
            2. **완료** 를 선택합니다.

        - **동료** 를 선택한 경우 다음 단계를 수행하십시오.

            1. 목록에서 한 명 이상의 동료를 선택합니다. 오프라인 사용을 위해 앱에 로드된 동료 목록이 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 동료가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 이름으로 검색하거나 회사 또는 제목으로 검색하도록 전환합니다.
            2. **완료** 를 선택합니다.

    3. **뒤로** 단추를 눌러 경비 세부 정보로 돌아갑니다.

19. 회사 정책에 경비를 항목별로 구분해야 하는 경우 **항목별 구분** 을 선택하고 다음 단계를 수행하십시오.

    1. 항목별로 구분할 첫 번째 날짜를 선택합니다.
    2. **항목화 추가** 를 선택합니다.
    3. 경비 항목화를 위한 하위 범주를 선택합니다. 오프라인 사용을 위해 앱에 로드된 경비 하위 범주 목록이 표시됩니다. 기본적으로 50개의 항목이 로드되지만 개발자가 이 수를 변경할 수 있습니다. 자세한 내용은 [모바일 플랫폼](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)을 참조하십시오. 하위 범주가 목록에 없으면 **검색** 을 선택하여 온라인 검색을 수행합니다. 경비 하위 범주 이름으로 검색합니다.
    4. 항목화에 대한 트랜잭션 금액을 입력합니다.
    5. 필요한 경우 트랜잭션 날짜를 수정합니다.
    6. **완료** 를 선택합니다.
    7. 선택한 날짜에 대한 모든 항목화 추가를 완료할 때까지 앞의 단계를 반복합니다.
    8. 추가 날짜의 경우 **다음 날로 복사** 를 선택하여 항목화를 다음 날로 복사할 수 있습니다. 또는 항목화할 날짜를 선택한 다음 첫 번째 날짜와 마찬가지로 항목화를 추가할 수 있습니다.
    9. 경비 항목화를 완료한 후 **뒤로** 단추를 눌러 경비 세부 정보로 돌아갑니다.

20. **뒤로** 단추를 눌러 **경비 보고서** 페이지로 돌아갑니다.
21. 모든 비용을 추가할 때까지 앞의 단계를 반복합니다.
22. **제출** 을 선택합니다.
23. 승인자에 대한 설명을 입력합니다.
24. **완료** 를 선택합니다.