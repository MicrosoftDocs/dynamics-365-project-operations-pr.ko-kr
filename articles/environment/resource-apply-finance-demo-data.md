---
title: Finance Cloud 호스팅 환경에 데모 데이터 적용
description: 이 항목에서는 Project Operations의 데모 데이터를 Dynamics 365 Finance 클라우드 호스팅 환경에 적용하는 방법을 설명합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289872"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Finance Cloud 호스팅 환경에 데모 데이터 적용

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

> [!IMPORTANT]
> 이 항목은 Microsoft Dynamics 365 Finance 버전 10.0.13에만 적용되며 클라우드 호스팅 환경에서만 수행할 수 있습니다. 환경에 품질 업데이트를 적용하기 **전에** 이 항목의 단계를 완료하십시오.

1. LCS 프로젝트에서 **환경 세부 정보** 페이지를 엽니다. RDP(원격 데스크톱 프로토콜)를 사용하여 환경에 연결하는 데 필요한 세부 정보가 포함되어 있습니다.

![ 환경 세부 정보](./media/1EnvironmentDetails.png)

강조 표시된 자격 증명의 첫 번째 집합은 로컬 계정 자격 증명이며 원격 데스크톱 연결에 대한 하이퍼링크를 포함합니다. 자격 증명에는 환경 관리자 사용자 이름과 암호가 포함됩니다. 두 번째 자격 증명 집합은 이 환경에서 SQL Server에 로그인하는 데 사용됩니다.

2. **로컬 계정** 의 하이퍼링크로 환경에 원격 연결하고 **로컬 계정 자격 증명** 을 사용하여 인증합니다.
3. **인터넷 정보 서비스** > **응용 프로그램 풀** > **AOSService** 로 이동하고 서비스를 중지합니다. SQL 데이터베이스를 계속 교체할 수 있도록 이 시점에서 서비스를 중지합니다.

![AOS 중지](./media/2StopAOS.png)

4. **서비스** 로 이동하고 다음 두 항목을 중지합니다.

- Microsoft Dynamics 365 Unified Operations: 일괄 처리 관리 서비스
- Microsoft Dynamics 365 Unified Operations: 데이터 가져오기 내보내기 프레임워크

![서비스 중지](./media/3StopServices.png)

5. Microsoft SQL Server Management Studio를 엽니다. SQL 서버 자격 증명으로 로그인하고 LCS의 **환경 세부 정보** 페이지에서 axdbadmin 사용자 및 암호를 사용합니다.

![SQL Server Management Studio](./media/4SSMS.png)

6. 개체 탐색기 **데이터베이스** 에서 **AXDB** 를 찾습니다. 데이터베이스를 [다운로드 센터](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)에 있는 새 데이터베이스로 교체합니다. 
7. 원격으로 연결된 VM에 zip 파일을 복사하고 zip 콘텐츠를 추출합니다.
8. SQL Server Management Studio에서 **AxDB** 를 마우스 오른쪽 단추로 클릭한 다음 **과제** > **복원** > **데이터베이스** 를 선택합니다.

![데이터베이스 복원](./media/5RestoreDatabase.png)

9. **원본 장치** 를 선택하고 복사한 zip에서 추출한 파일로 이동합니다.

![원본 장치](./media/6SourceDevice.png)

10. **옵션** 을 선택한 다음 **기존 데이터베이스 덮어쓰기** 및 **대상 데이터베이스에 대한 기존 연결 닫기** 를 선택합니다. 
11. **확인** 을 선택합니다.

![설정 복원](./media/7RestoreSetting.png)

AXDB 복원이 성공했다는 확인 메시지가 표시됩니다. 이 확인을 받은 후 SQL Services Management Studio를 닫을 수 있습니다.

12. **인터넷 정보 서비스** > **응용 프로그램 풀** > **AOSService** 로 다시 이동하고 AOSService를 시작합니다.
13. **서비스** 로 이동하고 이전에 중지한 두 서비스를 시작합니다.

14. 이 VM에서 AdminUserProvisioning 도구를 찾습니다. K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 아래에서 찾습니다.
15. **이메일 주소** 필드에서 사용자 주소를 사용하여 .ext 파일을 실행합니다. 
16. **제출** 을 선택합니다.

![관리 사용자 프로비전](./media/8AdminUserProvisioning.png)

완료하는 데 몇 분 정도 걸립니다. 관리 사용자가 성공적으로 업데이트되었다는 확인 메시지를 받아야 합니다.

17. 마지막으로 관리자 권한으로 명령 프롬프트를 실행하고 iisreset을 수행합니다.

![IIS 초기화](./media/9IISReset.png)

18. 원격 데스크톱 세션을 닫고 LCS **환경 세부 정보** 페이지를 사용하여 환경에 로그인하여 예상대로 작동하는지 확인합니다.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]