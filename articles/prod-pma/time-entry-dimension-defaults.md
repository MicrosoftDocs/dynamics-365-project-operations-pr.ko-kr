---
title: 프로젝트 시간 항목에 대한 재무 차원 기본값 설정
description: 이 문서에서는 기본 재무 차원이 시간 항목에 적용되는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916572"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>프로젝트 시간 항목에 대한 재무 차원 기본값 설정

[!include [banner](../includes/banner.md)]

프로젝트 시간 항목에 재무 차원을 사용할 때 기본 차원 값은 다음 순서로 평가됩니다.

1. 리소스
2. Project
3. 자금 출처

예를 들어 리소스에 기본 차원이 지정된 경우 프로젝트에 대해 지정된 기본값보다 기본값이 적용됩니다. 마찬가지로 프로젝트에 기본 차원이 지정된 경우 자금 출처에 대해 지정된 기본값보다 기본값이 적용됩니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
