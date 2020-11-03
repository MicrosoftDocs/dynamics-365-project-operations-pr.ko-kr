---
title: 내부 프로젝트에 대한 회계 구성
description: 이 항목은 Project Operations의 내부 프로젝트에 대한 회계 절차를 설정하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079986"
---
# <a name="configure-accounting-for-internal-projects"></a>내부 프로젝트에 대한 회계 구성

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

내부 프로젝트를 통해 회사는 고객에게 청구되지 않는 활동과 관련된 비용을 추적할 수 있습니다. 내부 프로젝트의 예는 다음과 같습니다.

- 모바일 앱과 같은 제품을 개발하고 개발과 관련된 비용을 추적합니다.
- 사전 판매 시간 및 비용 관리. 이 사전 판매 내부 프로젝트는 견적이 성사되면 나중에 청구 가능한 프로젝트로 변환할 수 있습니다.

Dynamics 365 Project Operations의 계약과 연결되지 않은 모든 프로젝트는 내부 프로젝트로 처리됩니다. 프로젝트 비용 및 수익 프로필은 프로젝트에 대한 회계 규칙을 결정하는 데 사용되지 않습니다. 내부 프로젝트 비용은 항상 손익 원칙을 사용하여 전기됩니다. 전기를 위한 원장 계정은 **원장 전기 설정** 페이지에서 정의됩니다.

- 시간 트랜잭션은 **비용** 계정을 차변 처리하고 **급여 할당** 계정을 대변 처리하여 전기됩니다.
- 경비 트랜잭션은 **비용** 계정을 차변 처리하고 **경비에 대한 상쇄 계정** 계정을 대변 처리하여 전기됩니다.

트랜잭션이 프로젝트에 전기된 후 프로젝트가 프로젝트 계약과 연관된 경우 시스템은 누적된 모든 트랜잭션을 취소하고 새로운 청구 가능 트랜잭션을 생성합니다. 청구 가능 트랜잭션은 각 프로젝트 비용 및 수익 프로필에 정의된 회계 규칙을 따릅니다.


