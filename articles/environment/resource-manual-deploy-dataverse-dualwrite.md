---
title: 이중 쓰기를 지원하는 Project Operations Dataverse 앱 수동 배포
description: 이 문서에서는 이중 쓰기를 지원하도록 Project Operations Dataverse 앱을 수동으로 배포하는 방법을 설명합니다.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a25e2a59f1c069057c6689825ce52b13d842af71
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028572"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>이중 쓰기를 지원하는 Project Operations Dataverse 앱 수동 배포

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서에서는 이중 쓰기를 지원하도록 Microsoft Dataverse에 Microsoft Dynamics 365 Project Operations를 수동으로 배포하는 방법을 설명합니다. Project Operations는 환경의 구성을 감지하고 전제 조건이 충족되는 경우 이중 쓰기에 대한 추가 지원을 추가합니다.

Microsoft Dynamics LCS(Lifecycle Services)를 통해 배포하는 동안 이 문서의 지침을 따랐다면 Microsoft Power Platform 통합(이전에는 Common Data Service 환경으로 알려짐) 배포를 건너뛸 수 있습니다.

이중 쓰기를 지원하도록 Dataverse에 Project Operations를 배포하는 프로세스는 네 가지 주요 단계로 이루어집니다.

1. [이중 쓰기를 지원하는 Dataverse에서 새로운 환경 만들기](#create).
2. [환경에 이중 쓰기 사전 요구 사항 추가](#prerequisites).
3. [Project Operations Dataverse 앱 추가](#dataverse).
4. [환경을 연결](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>이중 쓰기를 지원하는 Dataverse에서 새로운 환경 만들기

이 절차를 완료하려면 관리자로 로그인해야 합니다.

1. [Power Platform 관리 센터](https://admin.powerplatform.com)를 열고 관리자로 로그인합니다.
2. 새 환경을 만들고 이름을 지정합니다.
3. 환경 유형을 선택합니다. 평가판 제안에 가입한 경우 **평가판(구독 기반)** 을 선택합니다.
4. 배포 지역을 확인합니다.
5. **이 환경에 대한 데이터베이스 만들기** 옵션을 활성화합니다. 
6. 언어를 확인한 다음 통화가 금융 및 운영 앱의 통화와 일치하는지 확인합니다.
7. **Dynamics 365 앱** 옵션을 활성화하고 **이 앱 자동 배포** 필드가 **없음** 으로 설정되어 있는지 확인합니다.
8. 보안 그룹이 필요한 경우 보안 그룹을 추가합니다.
9. **저장** 을 선택하여 환경을 만듭니다.
10. 배포가 완료되고 환경이 **준비** 상태에 도달할 때까지 기다립니다.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>환경에 이중 쓰기 사전 요구 사항 추가

이중 쓰기 지원에는 **회사** 엔터티와 같은 주요 엔터티에 추가되는 추가 필드가 포함됩니다. 기존 환경에 이중 쓰기 지원을 추가하는 경우 지원을 활성화하려면 데이터를 업데이트해야 할 수 있습니다. 데이터를 부트스트랩하는 방법에 대한 자세한 내용은 [회사 데이터 부트스트랩](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)을 참조하십시오. 이중 쓰기에 대한 자세한 내용은 [이중 쓰기 시스템 요구 사항](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)을 참조하십시오.

이중 쓰기 사전 요구 사항을 환경에 추가하려면 이 절차를 완료하십시오.

1. 방금 만든 환경을 열고 **리소스** \> **Dynamics 365 앱** 으로 이동합니다.
2. 앱 목록에서 **이중 쓰기 코어 솔루션** 을 선택하고 설치합니다.
3. 설치가 완료될 때까지 기다립니다. 그런 다음 앱 목록에서 **이중 쓰기 애플리케이션 오케스트레이션 솔루션** 을 선택하고 설치합니다.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Project Operations Dataverse 앱 추가

Project Operations를 설치하기 전에 이전 절차를 완료한 경우에만 이 절차를 완료할 수 있습니다. 설치하는 동안 시스템은 환경 구성을 분석하고 필요한 경우 이중 쓰기 지원을 추가합니다.

1. 이전에 만든 환경을 열고 **리소스** \> **Dynamics 365 앱** 으로 이동합니다.
2. 앱 목록에서 **Microsoft Dynamics 365 Project Operations** 를 선택하고 설치합니다.

## <a name="link-your-environments"></a><a name="link"></a>환경을 연결

Dataverse 환경이 배포되면 금융 및 운영 앱에서 링크를 설정할 수 있습니다. [이중 쓰기 마법사를 사용하여 환경 연결](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)의 단계를 따릅니다.
