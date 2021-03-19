---
title: 경비 영수증 처리
description: 이 항목은 영수증에 대한 광학 문자 인식(OCR) 처리에 대한 정보를 제공합니다. 이 기능은 Microsoft Dynamics 365 Finance에서 경비 보고서를 작성할 때 사용자 경험을 개선하도록 설계되었습니다.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271811"
---
# <a name="expense-receipt-processing"></a>경비 영수증 처리

영수증에 대한 광학 문자 인식(OCR) 처리를 도입하여 경비 입력 기능이 강화되었습니다. 이 기능은 경비 보고서를 작성할 때 사용자 경험을 개선하도록 설계되었습니다.

## <a name="key-features"></a>주요 기능

- 영수증에서 판매자 이름, 날짜 및 총액이 추출됩니다.
- 이 기능은 첨부되지 않은 영수증을 첨부되지 않은 경비 트랜잭션과 일치시키려고 시도합니다.
- 영수증에서 수동으로 입력한 경비 트랜잭션을 생성할 수 있습니다.

## <a name="usage-examples"></a>사용법 예제

경비 보고서가 생성될 때 신용 카드 거래가 포함된 영수증을 자동으로 첨부하려면 다음을 수행하십시오.

  1. **경비 관리** 작업 영역을 엽니다.
  2. **영수증** 탭에서 첨부되지 않은 영수증이 있는지 확인합니다. **영수증** 탭에서 영수증을 업로드할 수도 있습니다.
  3. **경비** 탭에서 첨부되지 않은 경비가 있는지 확인합니다. 일반적으로 경비 관리자는 신용 카드 공급자로부터 이러한 경비를 가져옵니다.
  4. **새 경비 보고서** 를 선택합니다. 이제 경비 보고서를 작성할 때 경비와 영수증도 포함할 수 있습니다. 경비와 영수증을 모두 추가하면 경비에 대한 영수증의 자동 일치가 트리거됩니다.

경비를 생성하거나 영수증의 비용을 대응시키려면 다음을 수행하십시오.

  1. 경비 보고서의 **영수증** 탭에서 **영수증 추가** 를 선택하여 영수증을 첨부합니다.
  2. 영수증의 업로드된 이미지 아래에 **만들기** 및 **일치** 옵션이 있습니다.

      - **만들기** 를 선택하여 수동으로 입력한 경비 트랜잭션을 생성하고 영수증에서 추출된 값을 입력합니다.
      - **일치** 를 선택하는 경우 시스템은 기존 경비를 영수증과 일치 시키려고 합니다.

## <a name="installation"></a>설치

이 기능은 경비 경험을 단순화하기 위해 **재구상된 경비 보고서** 와 함께 사용됩니다. 이 기능은 Sandbox 및 Production인 Tier 2+ 환경에서만 사용할 수 있습니다.

이러한 고급 경비 기능을 사용하려면 Microsoft Dynamics 365 Finance용 경비 관리 서비스 추가 기능을 설치하고 인스턴스에서 기능을 켭니다. Microsoft Dynamics Lifecycle Services(LCS)의 프로젝트에서 추가 기능에 액세스할 수 있습니다.

1. LCS에 로그인하고 원하는 환경을 엽니다.
2. **전체 세부 사항** 으로 이동합니다.
3. **유지 관리** 를 선택하거나 **환경 추가 기능** 빠른 탭으로 스크롤합니다.
4. **새 추가 기능 설치** 를 선택합니다.
5. **경비 관리 서비스** 를 선택합니다.
6. 설치 가이드를 따르고 이용 약관에 동의합니다.
7. **설치** 를 선택합니다.

**기능 관리** 작업 영역에서 다음 기능을 켭니다.

- 재구상된 경비 보고서
- 영수증에서 경비 자동 일치 및 생성

이러한 기능을 켜면 다음 동작이 발생합니다.

- 기존 **경비 관리** 작업 영역이 새 작업 영역으로 바뀝니다.
- 경비 필드 가시성을 위한 새 메뉴 항목이 추가되었습니다.
- **경비 관리 > 내 경비 > 경비 보고서** 로 이동하여 계속해서 이전의 **경비 보고서** 페이지를 열 수 있습니다.
- 워크플로 및 모든 승인은 여전히 기존 비용 보고서 페이지로 이동합니다.
- 영수증은 Microsoft Azure Cognitive Services를 통해 처리되며 메타데이터가 추출 및 추가됩니다.
- 첨부되지 않은 일치 영수증을 포함하는 경비 보고서를 생성 할 수 있는 옵션이 추가되었습니다.
- 경비 보고서에 추가된 옵션을 사용하면 영수증에서 비용 라인을 생성하거나 기존 영수증을 기존 비용 라인에 일치시킬 수 있습니다.

재구상된 경비 보고서 기능에 대한 자세한 내용은 [재구상된 경비 보고서](ExpenseWorkspaceNew.md)를 참조하십시오.

## <a name="frequently-asked-questions"></a>자주 묻는 질문

**Microsoft는 모델에 내 데이터를 사용합니까?**

아니요, Microsoft는 영수증 처리 서비스를 위해 일반 기계 학습 모델을 구축했습니다. 이 모델은 업로드한 영수증을 기반으로 하지 않습니다.

**이 기능은 어디에서 사용 가능하고 처리됩니까?**

현재 미국이 지원됩니다.

**영수증은 어디로 갑니까?**

재무 부서는 Cognitive Services에 연락하여 필드 데이터를 추출합니다. Cognitive Services는 처리가 진행되는 동안 최대 24시간 동안 영수증 사본을 보관합니다. 처리가 완료되면 Cognitive Services에서 영수증을 제거합니다. 영수증은 여전히 Finance에 저장됩니다.

자세한 내용은 [Form Recognizer의 새로운 기능으로 영수증 이해 가능](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)을 참조하십시오.


[!INCLUDE[footer-include](../includes/footer-banner.md)]