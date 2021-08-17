---
title: 작업 분할 구조 템플릿에서 역할 설정
description: 이 항목은 작업 분할 구조 템플릿에 대한 역할 정보 설정에 대한 정보를 제공합니다.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c84015c46f0a8c9d3d48be1b995d4bdd7fd8ee25b240f455bbe2031f42adc0f5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008909"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>작업 분할 구조 템플릿에서 역할 설정

[!include [banner](../includes/banner.md)]

프로젝트 관리자는 새 프로젝트용 WBS(작업 분할 구조)를 만들 때 적용할 수 있는 WBS 템플릿을 설정할 수 있습니다. 프로젝트 관리자는 템플릿을 만들 때 역할을 추가할 수 있습니다. 다음 절차에 따라 WBS 템플릿에 역할을 할당합니다.

1. **프로젝트 관리 및 회계** > **설정** > **프로젝트** > **작업 분할 구조 템플릿** 을 선택합니다.
2. 선택한 WBS 템플릿에 대한 **세부 정보** 를 선택합니다.
3. 목록에서 작업을 선택한 다음 **역할** 필드에서 작업에 할당할 역할을 선택합니다.

## <a name="work-with-a-wbs"></a>WBS에 대한 작업

새 WBS를 만들거나 기존 WBS 템플릿에서 WBS를 복사할 수 있습니다. 프로젝트 관리자는 WBS의 새 작업에 역할을 할당하여 리소스를 쉽게 관리할 수 있습니다. 리소스를 획득한 후 또는 작업을 수행할 확인된 리소스가 식별된 후 역할을 교체할 수 있습니다. 이러한 유연성 덕분에 프로젝트 관리자는 다음 작업을 수행할 수 있습니다.

- WBS 작업 패키지에 필요한 리소스 수를 식별합니다.
- 프로젝트 비용을 추정합니다.
- 예비 예산을 결정합니다.
- 역할 및 리소스를 기반으로 활동 기간을 추정합니다.
- 사용 가능한 프로젝트 정보를 기반으로 몇 가지 프로젝트 관리 계획을 개발합니다.

리소싱 기능을 더 잘 사용하기 위해 WBS에 추가 옵션이 추가되었습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>옵션</th>
<th>설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>리소스 할당</td>
<td>WBS의 작업에 할당된 리소스, 날짜, 시간 및 예약 유형을 봅니다.</td>
</tr>
<tr class="even">
<td>팀 자동 생성</td>
<td>작업과 관련된 역할을 사용하여 계획된 리소스를 자동으로 추가합니다. Finance는 역할에 기반한 다중 기준 의사 결정 분석을 사용하여 계획된 리소스를 자동으로 제안합니다. WBS의 작업에 대한 역할 및 노력(시간)을 설정한 후 구조가 해제된 후 <strong>팀 자동 생성</strong>을 선택합니다. 필요한 수의 계획된 리소스가 WBS 및 <strong>프로젝트 및 팀 일정</strong>탭에 추가됩니다 .</td>
</tr>
<tr class="odd">
<td>리소스(드롭다운 목록)</td>
<td><strong>리소스 할당 시작</strong> 페이지에서 지정된 기간에 따라 확정 예약 또는 가예약할 리소스를 선택할 수 있습니다. 보기 설정을 조정하여 리소스 활동 기간을 보고 설정할 수 있습니다. 다음 옵션을 사용하여 작업 패키지 수준에서 리소스를 선택하고 할당할 수 있습니다.
<ul>
<li><strong>수락</strong> – 작업에 할당된 자원의 변경 사항을 확인합니다.</li>
<li><strong>취소</strong> – 작업에 할당된 자원의 변경 사항을 취소합니다.</li>
<li><strong>자동 할당</strong> – 일치하는 역할이 있는 사용 가능한 인력이 있는 리소스가 자동으로 선택되고 선택한 작업에 할당됩니다.</li>
</ul></td>
</tr>
</tbody>
</table>

1. **모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트를 선택합니다.
2. **계획** > **활동** > **작업 분할 구조** 를 선택합니다.
3. **신규** 를 선택하여 다음 수준 1 활동을 WBS에 추가합니다.

    - 시작
    - 계획
    - 실행 중
    - 모니터링 및 제어
    - 종료

4. 다음 그림과 같이 날짜와 노력(시간)을 설정합니다.

    [![날짜와 노력 설정.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. **시작** 작업 줄을 선택한 다음 **역할** 필드에서 **수석 프로젝트 관리자** 를 선택합니다.
6. **게시** 를 선택합니다.
7. 같은 줄의 **리소스** 필드에서 **Daniel Goldschmidt** 를 선택한 다음 **수락** 을 선택합니다.
8. **계획** 작업 줄을 선택한 다음 **역할** 필드에서 **비즈니스 분석가** 를 선택합니다.
9. **게시** 를 선택한 다음 **팀 자동 생성** 을 선택합니다.
10. 표시되는 메시지 상자에서 **예** 를 선택합니다.
11. **리소스** 필드에서 값이 **비즈니스 분석가 1** 인지 확인합니다.
12. **비즈니스 분석가 1** 리소스의 경우 조회를 열고 **리소스 할당 시작** 을 선택합니다. 그런 다음 작업에 대한 작업자를 선택합니다.
13. **소프트 할당** &gt; **전체 용량** 을 선택합니다.

    > [!NOTE] 
    > 리소스 수가 1로 남아 있으므로 지정된 리소스가 이제 2라는 경고를 받지 않습니다.

14. **작업 분할 구조** 페이지에서 WBS에서 리소스 할당을 확인한 다음 **저장** 을 선택합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]