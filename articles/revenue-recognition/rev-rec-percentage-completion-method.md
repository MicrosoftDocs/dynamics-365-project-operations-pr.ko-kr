---
title: 고정 가격 수익 프로젝트 추정
description: 이 문서에서는 프로젝트의 고정 가격 수익에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928394"
---
# <a name="fixed-price-revenue-estimate-projects"></a>고정 가격 수익 프로젝트 추정 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Microsoft Dataverse의 Dynamics 365 Project Operations에서 다음 특성을 사용하여 프로젝트 계약 내용을 생성할 때 시스템은 고정 가격 수익 추정 프로젝트를 자동으로 생성합니다. 이 프로젝트의 정보는 다음을 기반으로 합니다.

  - 고정 가격 청구 방법.
  - 관련 프로젝트.
  - **프로젝트 계약 내용** 페이지의 **송장 일정** 탭에 정의된 하나 이상의 중요 시점.

## <a name="review-fixed-price-revenue-estimates-projects"></a>고정 가격 수익 추정 프로젝트 검토
고정 가격 수익 추정 프로젝트를 검토하려면 다음 단계를 완료하십시오.

1. Dynamics 365 Finance 환경에서 **프로젝트 관리 및 회계** > **프로젝트** > **고정 가격 수익 추정 프로젝트** 로 이동합니다.
2. 보려는 프로젝트를 선택하고 **추정 프로젝트 ID** 를 두 번 클릭하여 레코드를 열고 프로젝트의 세부 사항을 검토합니다.
3. **프로젝트** 탭을 확장합니다. **선택한 프로젝트** 그리드에 하나의 프로젝트가 표시됩니다. 시스템은 프로젝트 계약 내용과 연관된 프로젝트이므로 이를 기본 프로젝트로 사용합니다. 
4. 연결을 변경하려면 추가 프로젝트를 선택하고 **선택한 프로젝트** 그리드에 추가합니다. 이 그리드에서 여러 프로젝트를 선택한 경우 선택한 모든 프로젝트에 대해 프로젝트 완료율 및 예상 수익이 함께 계산됩니다.

  프로젝트 비용, 수익 프로필, 비용 템플릿 및 기간 코드는 수동으로 설정할 수 있습니다. 수동으로 설정하지 않은 경우 프로젝트 비용 및 수익 프로필에 대해 구성된 규칙을 사용하여 프로젝트에 대한 첫 번째 추정 계산 중에 값이 기본값으로 설정됩니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]