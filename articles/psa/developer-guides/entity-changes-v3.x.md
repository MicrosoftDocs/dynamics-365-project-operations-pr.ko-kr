---
title: 엔터티, 컨트롤 및 사용자 인터페이스 변경 (Project Service Automation 3.x)
description: 이 항목은 Microsoft Dynamics Project Service Automation 3.x의 솔루션 변경에 대해 설명합니다.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 2d93e5eaae7cff302be1cb2e96e3f45c24739b0c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080247"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>엔터티, 컨트롤 및 사용자 인터페이스 변경 (Project Service Automation 3.x)
Microsoft Dynamics Project Service Automation (PSA) 3.x가 릴리스되면서 엔터티, 컨트롤, 뷰 및 사용자 인터페이스가 많이 변경되었습니다. 이 주제는 그러한 중요 변경 사항에 대한 정보를 제공합니다.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>판매 문서, 판매 문서 행, 판매 문서 행 내역 엔터티에 대한 상위-하위 관계
버전 3.0 이전에 릴리스된 버전의 Dynamics 365 Project Service Automation(PSA)에서는 판매 문서, 판매 문서 행, 판매 문서 행 내역 엔터티들 사이의 관계 중 일부는 관련 엔터티의 GUID의 문자열 표현을 보유할 문자열 필드를 통해 구현되었습니다. 이는 그러한 관계가 일반적 Dynamics CRM 엔티티 관계와 유사하게 기능하도록 하기 위해 그리고 문자열 필드가 조회 필드처럼 기능하도록 하기 위해 해당 솔루션의 서버측 및 클라이언트측에 상당한 맞춤 코드를 요구한 플랫폼 제한 때문이었습니다.

PSA 3.0은 판매 문서와 판매 문서 행 엔터티 사이의 새 엔터티 관계를 활용하도록 업데이트되었습니다.

조회 필드를 사용하여 엔터티에 대한 참조를 나타낼 수 있으므로 이전 버전에서 관련 엔터티의 GUID 문자열 값을 보유한 필드는 더 이상 필요하지 않으므로 단종되었습니다. 레거시 문자열 필드가 정의하는 관계를 취급하는 맞춤 클라이언트측 및 서버측 코드도 단종되었습니다.

### <a name="entity-schema-changes"></a>엔터티 스키마 변경
다음 표는 단종된 문자열 필드와 해당 엔터티를 위한 새로운 조회 필드의 일대일 목록입니다. 

 엔터티 |   단종된 필드(문자열) | 새 필드 (조회)
--- | --- | ---
청구서 내역 (청구서 행) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (실제값) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (프로젝트 계약 행 청구서 스케줄) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (프로젝트 계약 행 이정표) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (사실) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (청구서 행 내역) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (분개장 행) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (프로젝트 계약서 행 리소스 카테고리) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (프로젝트 계약서 행 내역) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (프로젝트 계약서 행 처리 카테고리) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (프로젝트 계약서 행 처리 분류) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (견적 행 청구 스케줄) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (견적 행 리소스 카테고리) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (견적 행 이정표) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (견적 행 내역) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (견적 행 처리 카테고리) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (견적 행 처리 분류) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (주문 행) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>단종된 맞춤 보기 및 컨트롤
다음 맞춤 보기 및 컨트롤과 관련 아티팩트가 단종되었습니다.

- 청구 가능성 보기.
- 견적 행을 위한 **프로젝트 정보** 페이지에 견적 행 내역을 표시하기 위한 맞춤 그리드 컨트롤입니다.
- 판매 주문 행을 위한 **프로젝트 정보** 페이지에 프로젝트 계약서 행 내역을 표시하기 위한 맞춤 그리드 컨트롤입니다.

> [!NOTE]
> 단종된 리소스의 전체 목록은 [Project Service Automation v3.x에서 단종된 웹 리소스](../developer-guides/web-resources-deprecated-v3.x.md)를 참조하십시오

## <a name="unified-client-interface-app-module"></a>통합 클라이언트 인터페이스 앱 모듈
통합 클라이언트 인터페이스(UCI) 앱 모듈이 도입되면서 시스템에서 PSA 사이트 맵 항목이 제거되었습니다.  
UCI 앱 모듈에는 양식의 PSA 버전만 포함되므로 영업 기회, 견적, 주문, 청구서에 대한 양식 전환과 관련된 기능이 더 이상 필요하지 않으므로 단종되었습니다.  

다음 웹 리소스가 단종되었습니다:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> 단종된 리소스의 전체 목록은 [Project Service Automation v3.x에서 단종된 웹 리소스](../developer-guides/web-resources-deprecated-v3.x.md)를 참조하십시오.


