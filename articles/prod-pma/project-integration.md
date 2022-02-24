---
title: Microsoft Project Client 통합
description: 프로젝트 일정을 계획하고 유지하는 것은 복잡할 수 있으므로 프로젝트 관리자는 이 작업을 관리하는 데 도움이 되는 도구를 사용해야 합니다. Microsoft Project Client와의 통합은 프로젝트 작업 분할 구조를 열고 관리할 수 있도록 지원합니다.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080113"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client 통합

[!include [banner](../includes/banner.md)]

프로젝트 일정을 계획하고 유지하는 것은 복잡할 수 있으므로 프로젝트 관리자는 이 작업을 관리하는 데 도움이 되는 도구를 사용해야 합니다. Microsoft Project Client와의 통합은 프로젝트 작업 분할 구조를 열고 관리할 수 있도록 지원합니다. 프로젝트 관리자는 변경 사항을 Dynamics 365 Finance 프로젝트 작업 분할 구조에 다시 게시할 수 있습니다.

> [!NOTE]
> 7월 업데이트(버전 10.0.4)를 사용하는 경우 KB 4054797 및 4055884를 설치해야 합니다.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project Client 추가 기능 구성
Microsoft Project Client와의 통합을 활성화하려면 Microsoft Dynamics 365 추가 기능은 사용자의 클라이언트 Microsoft Project 애플리케이션에 설치해야 합니다. 이것은 **프로젝트 관리 작업 공간** 을 열어 수행됩니다.

•    작업 영역의 **연결** > **설정** 섹션에서 **프로젝트 클라이언트 추가 기능 구성** 을 클릭합니다.

•   메시지가 표시되면 **열기** 를 클릭한 다음 **실행** 을 클릭합니다.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Project Client에서 기존 초안 작업 분할 구조를 열고 편집합니다.
Dynamics 365 Finance의 프로젝트에서 작업 분할 구조가 이미 생성된 경우 작업 분할 구조가 초안 상태인 경우 Microsoft Project Client 응용 프로그램에서 작업 분할 구조를 열 수 있습니다. **프로젝트** 페이지에서 열려면 **계획** 탭에서 **Microsoft Project에서 열기** 링크를 클릭합니다. 이 페이지는 **Microsoft Dynamics 365** 탭에서 **열기** 를 클릭하여 Microsoft Project Client 애플리케이션 내에서 열 수도 있습니다. 목록에서 **법인** 과 **계획** 을 선택합니다.

> [!NOTE]
> Internet Explorer를 브라우저로 사용하는 경우 **저장** 을 클릭하여 파일을 다운로드한 위치에서 수동으로 엽니다. 또는 **저장 후 열기** 를 클릭하여 Microsoft Project Client에서 파일을 엽니다. 저장할 때 파일 이름을 바꾸지 마십시오.

Microsoft Project Client를 사용하여 파일을 편집하기 전에 체크아웃해야 합니다. **Microsoft Dynamics 365** 탭에서 **체크아웃** 을 클릭합니다. 이렇게 하면 다른 사용자가 Finance 내에서 동시에 작업 분할 구조를 편집할 수 없습니다. 편집을 완료한 후 작업 분할 구조를 게시하려면 **Microsoft Dynamics 365** 탭에서 **체크인** 을 클릭합니다.

프로젝트 팀이 이미 Finance의 프로젝트에 추가된 경우 리소스 목록이 팀 구성원으로 채워집니다. 프로젝트 팀이 아직 프로젝트에 추가되지 않은 경우 **Microsoft Dynamics 365** 탭에서 **리소스** 단추를 클릭하여 리소스를 선택하고 Microsoft Project Client 내에서 팀을 구성할 수 있습니다. 

다음 데이터는 체크인 프로세스의 일부로 Finance에 다시 동기화됩니다.

•   작업 이름

•   시작 날짜

•   완료 날짜

•   선행 업무

•   리소스 이름

•   범주

•   리소스 범주

•   근무 시간

•   메모

•   우선 순위

> [!NOTE]
> Microsoft Project Client 파일에 다른 열을 추가하면 파일에 저장되지 않으며 파일을 다시 열 때 표시되지 않습니다.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client를 사용하여 기존 프로젝트에 대한 작업 분할 구조 만들기
Microsoft Project Client를 사용하여 새 작업 분할 구조를 만들려면 다음 단계를 수행하십시오.


1.  Microsoft Project Client를 엽니다.

2.  **Microsoft Dynamics 365** 탭에서 **열기** 를 클릭합니다.

3.  엔터티에 대한 **법인** 을 선택합니다.

4.  **프로젝트** 를 선택합니다.

5.  **Microsoft Dynamics 365** 탭에서 **체크아웃** 을 클릭합니다.

6.  Finance에 게시할 준비가 되면 **Microsoft Dynamics 365** 탭에서 **체크인** 을 클릭합니다.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client를 사용하여 기존 프로젝트에 대한 기존 작업 분할 구조를 대체
Microsoft Project Client를 사용하여 새 작업 분할 구조를 만들고 기존 프로젝트의 기존 작업 분할 구조를 바꾸려면 다음 단계를 수행하십시오.

1.  Microsoft Project Client를 엽니다.

2.  Microsoft Project Client에서 일정을 만듭니다.

3.  **Microsoft Dynamics 365** 탭에서 **변경 사항 저장** > **기존 프로젝트 바꾸기** 를 클릭합니다.

4.  엔터티에 대한 **법인** 을 선택합니다.

5.  **프로젝트** 를 선택합니다.

6.  **확인** 을 클릭합니다.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Microsoft Project Client 내에서 새 프로젝트 만들기


1.  Microsoft Project Client를 엽니다.

2.  Microsoft Project Client에서 일정을 만듭니다.

3.  **Microsoft Dynamics 365** 탭에서 **변경 사항 저장** > **새 프로젝트에 저장** 을 클릭합니다.

4.  엔터티에 대한 **법인** 을 선택합니다.

5.  필요안 경우 **프로젝트 ID** 를 입력합니다.

6.  **프로젝트 이름** 을 입력합니다.

7.  **프로젝트 유형**, **프로젝트 그룹** 그리고 **프로젝트 계약 ID** 를 선택합니다. 또는 **새로 만들기** 를 클릭하여 새 프로젝트 계약을 생성할 수 있습니다.

8.  리소스 조달에 사용할 **일정** 을 선택합니다.

11. **확인** 을 클릭합니다.
