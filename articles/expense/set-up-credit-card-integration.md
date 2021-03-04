---
title: 신용 카드 통합 설정
description: 이 항목은 경비 관련 신용 카드 거래를 가져오고 유지하는 방법을 설명합니다.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120866"
---
# <a name="set-up-credit-card-integration"></a>신용 카드 통합 설정

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

경비 관련 신용 카드 거래는 반복되는 일정에 따라 자동으로 가져오도록 설정할 수 있습니다. 또는 필요에 따라 트랜잭션을 수동으로 가져올 수 있습니다. 신용 카드 거래는 신용 카드 거래 데이터 엔터티를 통해 가져옵니다.

## <a name="import-credit-card-transactions"></a>신용 카드 거래 가져오기

1. **신용 카드 거래** 페이지에서 **트랜잭션 가져오기** 를 선택합니다. 처음으로 데이터 관리를 여는 경우 계속하기 전에 시스템에서 데이터 엔터티 목록을 업데이트해야 합니다.
2. **이름** 필드에 가져오기 작업의 고유한 설명을 입력합니다.
3. **소스 데이터 형식** 필드에서 가져올 신용 카드 거래가 포함된 파일 형식을 선택합니다.
4. **업로드** 를 선택한 다음 가져올 파일을 찾아 선택합니다.
5. 파일이 업로드된 후 타일에서 **지도 보기** 링크를 선택하여 신용 카드 거래 파일과 신용 카드 거래 데이터 항목의 열 매핑을 확인합니다. 매핑 오류가 있거나 매핑을 변경해야 하는 경우 **매핑 시각화** 탭 또는 **매핑 세부 정보** 탭 중 하나에서 매핑을 변경합니다.
6. 신용 카드 거래를 자동화하려면 **반복 데이터 작업 만들기** 를 선택합니다. 그런 다음 신용 카드 거래를 가져와야 하는 빈도를 정의하는 반복을 설정할 수 있습니다. 완료되면 **확인** 을 선택합니다.
7. 지금 선택한 파일을 가져오려면 **가져오기** 를 선택합니다.
8. 가져오는 동안 오류가 발생하면 실행 로그 또는 스테이징 데이터를 보고 성공적인 가져오기를 보장하기 위해 수정해야 하는 오류를 확인할 수 있습니다.

> [!NOTE]
> 둘 이상의 파일 형식을 가져와야 하는 경우 각 형식 유형에 대해 별도의 가져오기 작업을 만들어야 합니다.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>퇴직한 직원에 대한 신용 카드 거래 재지정

직원 레코드가 종료되면 직원의 AD DS(Active Directory 도메인 서비스) 계정이 비활성화됩니다. 그러나 여전히 비용을 지불하고 상환해야 하는 활성 신용 카드 거래가 있을 수 있습니다. **신용 카드 거래** 페이지에서 관련 사원이 종료된 신용 카드 거래에 대해 사원을 재지정할 수 있습니다.

하나 이상의 신용 카드 거래를 선택한 다음 **거래 재지정** 을 선택합니다. 그런 다음 신용 카드 거래를 지정할 다른 사원을 선택할 수 있습니다. 신용 카드 거래가 재지정된 후 지출 보고서로 선택되고 지출 보고서 상환을 위한 일반적인 프로세스를 통해 지불될 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]