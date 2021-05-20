---
title: 프로젝트 송장 통합
description: 이 항목에서는 고객 송장에 대한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955787"
---
# <a name="project-invoice-integration"></a>프로젝트 송장 통합

이 항목에서는 고객 송장에 대한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.

Project Operations에서 프로젝트 관리자는 프로젝트 청구 백로그를 관리하고 Microsoft Dataverse에서 고객에 대한 견적 송장을 생성합니다. 이 견적 송장을 기반으로 수취 계정 담당자 또는 프로젝트 회계사가 고객 대면 송장을 생성합니다. 이중 쓰기 통합을 통해 견적 송장 세부 정보가 Finance and Operations 앱에 동기화됩니다. 고객 대면 송장이 전기된 후 시스템은 Dataverse의 관련 프로젝트 실적을 회계 세부 사항으로 업데이트합니다. 다음 그래픽은 이 통합에 대한 개략적인 개념적 개요를 제공합니다.

   ![프로젝트 송장 통합](./media/DW5Invoicing.png)

프로젝트 관리자가 Dataverse에서 견적 송장을 확인하면 견적 송장 헤더 정보가 이중 쓰기 테이블 맵인 **프로젝트 송장 제안 V2(송장)** 를 사용하여 Finance and Operations 앱에 동기화됩니다. Dataverse에서 Finance and Operations 앱으로의 단방향 통합입니다. Finance and Operations 앱에서 직접 프로젝트 송장 제안을 생성하거나 삭제하는 것은 지원되지 않습니다.

Dataverse의 송장 확인은 비즈니스 로직을 트리거하여 **실제** 엔터티에 청구 관련 레코드를 생성합니다. 이러한 레코드는 이중 쓰기 테이블 맵, **Project Operations 통합 실제(msdyn\_actuals)** 를 사용하여 Finance and Operations에 동기화됩니다. 자세한 내용은 [프로젝트 추정 및 실제](resource-dual-write-estimates-actuals.md)를 참조하십시오. 

프로젝트 송장 제안 라인은 주기적인 프로세스인 **준비에서 가져오기** 에 의해 생성됩니다. 이 프로세스는 **실제 준비** 테이블의 청구된 판매 실제 세부 정보를 기반으로 합니다. 자세한 내용은 [프로젝트 송장 제안 관리](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)를 참조하십시오. 
