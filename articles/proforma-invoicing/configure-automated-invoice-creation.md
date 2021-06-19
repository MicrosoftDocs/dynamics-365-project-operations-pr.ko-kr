---
title: 자동 송장 만들기 구성
description: 이 항목은 시스템이 송장을 자동으로 생성하도록 구성하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005349"
---
# <a name="configure-automatic-invoice-creation"></a>자동 송장 만들기 구성

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_


Dynamics 365 Project Operations에서 자동 송장 실행을 구성하려면 다음 단계를 완료하십시오.

1. **설정** > **일괄 작업** 으로 이동합니다.
2. 일괄 처리 작업을 만들고 **Project Operations 생성 송장** 이름을 지정합니다. 일괄 처리 작업의 이름에는 "송장 만들기"라는 단어가 포함되어야 합니다.
3. **작업 유형** 필드에서 **없음** 을 선택합니다. 기본적으로 **일일 빈도** 및 **활성** 옵션은 **예** 로 설정됩니다.
4. **워크플로 실행** 을 선택합니다. **레코드 보기** 대화 상자에는 세 가지 워크플로가 표시됩니다.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. **ProcessRunCaller** 를 선택한 다음 **추가** 를 선택합니다.
6. 다음 대화 상자에서 **확인** 을 선택합니다. **절전** 워크플로 뒤에 **프로세스** 워크플로가 있습니다.

  > [!NOTE]
  > 5단계에서 **ProcessRunner** 를 선택할 수도 있습니다. 그런 다음 **확인** 을 선택하면 **프로세스** 워크플로가 **절전** 워크플로를 뒤따릅니다.

**ProcessRunCaller** 및 **ProcessRunner** 워크플로는 송장을 만듭니다. **ProcessRunCaller** 는 **ProcessRunner** 를 호출합니다. **ProcessRunner** 는 실제로 송장을 만드는 워크플로입니다. 송장을 만들어야 하는 모든 계약 내용을 통해 해당 라인에 대한 송장을 만듭니다. 송장을 만들어야 하는 계약 내용을 확인하려면 작업 계약 내용에 대한 송장 실행 날짜를 확인합니다. 한 계약에 속한 계약 내용에 동일한 송장 실행 날짜가 있는 경우 트랜잭션은 두 개의 송장 라인이 있는 하나의 송장에 결합됩니다. 송장을 만들 트랜잭션이 없는 경우 작업에서 송장 만들기를 건너뜁니다.

**ProcessRunner** 가 완료되면 **ProcessRunCaller** 를 호출하고 종료 시간을 제공하면, 닫힙니다. 그런 다음 **ProcessRunCaller** 는 지정된 종료 시간에서 24시간 동안 실행되는 타이머를 시작합니다. 타이머가 끝나면 **ProcessRunCaller가** 닫힙니다.

송장을 만들기 위한 일괄 처리 작업은 되풀이 작업입니다. 이 일괄 처리 프로세스가 여러 번 실행되는 경우 작업의 여러 인스턴스가 만들어지고 오류가 발생합니다. 따라서 일괄 처리 프로세스를 한 번만 시작해야 하며 실행이 중지된 경우에만 다시 시작해야 합니다.

> [!NOTE]
> 일괄 처리 송장 발행은 송장 스케줄에 의해 구성된 프로젝트 계약 라인에 대해서만 실행됩니다. 고정 가격 청구 방법이 있는 계약 내용에는 이정표가 구성되어 있어야 합니다. 시간 및 자재 청구 방법이 있는 프로젝트 계약 내용에는 날짜 기반 송장 일정을 설정해야 합니다. 프로젝트 기반 계약 내용에도 동일하게 적용됩니다.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]