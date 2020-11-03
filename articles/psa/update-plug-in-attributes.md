---
title: 새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트
description: 이 주제는 가격 책정 차원에 대한 플러그인 속성 업데이트에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080135"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트

> [!NOTE]
> Project Service Automation(PSA)의 견적 및 계약 기능을 사용하지 않는 경우에는 이 주제를 건너뛸 수 있습니다.

이 항목은 귀하가 본 주제의 [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities.md), [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](field-references.md), 및 [가격 책정 차원으로 맞춤 필드 설정](set-up-pricing-dimensions.md) 항목의 절차를 완료했다고 간주합니다. 이러한 절차를 완료하지 않은 경우 돌아가서 완료한 다음 이 항목으로 돌아오십시오.

프로젝트 견적 행을 위한 **견적 행** 페이지에 견적 행 내역이 생성되면 시스템은 배경에 두 개의 추산 행(하나는 추산 값의 원가측, 하나는 매출액측)을 만듭니다. 프로젝트 계약 행에도 마찬가지입니다.

원가 측면에서 수량 또는 필드를 변경하면 해당 변경이 매출액 측에 전파됩니다. 이는 가격 책정 차원을 변경한 후 다시 등록해야 하는 다음 플러그인으로 인해 가능합니다.

- PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.

다음 단계는 플러그인을 등록하는 프로세스를 설명합니다.

1. **PluginRegistrationTool** 을 열고 온라인 인스턴스에 접속합니다.
2. **검색** 을 클릭하고 업데이트할 플러그인을 검색합니다.

 ![검색 트리의 스크린샷](media/PRT-1.png)

3. 플러그인을 찾은 후 플러그인을 선택한 다음 **기본 양식에서 선택** 을 클릭합니다.

4. 업데이트할 플러그인의 단계를 선택하고 마우스 오른쪽 버튼으로 클릭한 다음 **업데이트** 를 선택합니다.

 ![업데이트할 플러그인의 스크린샷](media/PRT-2.png)
 
5. 업데이트 창에서 필터링 속성의 타원( **...** )을 클릭합니다.

 ![기존 단계 구성 정보 업데이트의 스크린샷](media/PRT-3.png)
 
6. 가격 책정 속성 확인란을 선택합니다.

 ![가격 속성에 대한 확인란 선택을 보여주는 스크린샷](media/PRT-4.png)

7. **OK** 를 클릭하여 페이지를 닫은 다음 **업데이트 단계** 를 선택합니다.

 !["업데이트 단계" 버튼을 보여주는 스크린샷](media/PRT-5.png)
 
8. 두 번째 플러그인 **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction** 을 위해 이 프로세스를 반복합니다.

9. 플러그인 등록 도구를 닫습니다.

