---
title: 데모 설정 및 구성 데이터 적용 - 라이트
description: 이 문서에서는 Project Operations에 대한 데모 설정 및 구성 데이터를 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409999"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operations의 데모 설정 및 구성 데이터 적용 - 라이트 

_**Lite 배포 - 견적 송장 거래_



## <a name="prerequisites"></a>전제 조건

구성을 시작하기 전에 Dynamics 365 Project Operations용으로 프로비저닝된 Dataverse 환경이 있어야 합니다.


## <a name="instructions"></a>지침

1. [마스터 데이터 패키지](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip)를 다운로드합니다. 
2. 폴더 *ProjOpsSampleSetupData - CE only CMT* 로 이동하고 실행 파일 *DataMigrationUtility* 를 실행합니다.
3. Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기** 를 선택한 다음 **계속** 을 선택합니다.

    ![구성 마이그레이션.](./media/1ConfigurationMigration.png)

4. CMT 마법사의 2페이지에서 **Microsoft 365** 를 **배포 유형** 으로 선택합니다.
5. **사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.
6. 테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인** 을 선택합니다.

   ![구성 로그인.](./media/2ConfigurationSignin.png)

7. 3페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인** 을 선택합니다.
8. 4페이지에서 압축을 푼 폴더 *ProjOpsSampleSetupData - CE only CMT* 에서 zip 파일 *SampleSetupAndConfigData* 를 선택합니다.

   ![압축 파일.](./media/3ZipFile.png)

   ![파일 선택.](./media/4SelectAFile.png)

9. Zip 파일을 선택한 후 **데이터 가져오기** 를 선택합니다.

   ![데이터 가져오기.](./media/5ImportData.png)

10. 가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다. 가져오기가 완료되면 CMT 마법사를 종료합니다. 
11. 조직에서 다음 18개 항목의 데이터를 확인합니다.

    -   통화
    -   어카운트
    -   조직 구성 단위
    -   연락처
    -   단위
    -   단위 그룹
    -   가격표
    -   프로젝트 한도 가격표 
    -   송장 빈도
    -   예약 가능한 리소스 범주
    -   거래 범주
    -   경비 범주
    -   역할 가격
    -   거래 범주 가격
    -   특징
    -   예약 가능한 리소스
    -   예약 가능한 리소스 범주 연결
    -   예약 가능한 리소스 특징

    ![가져오기 완료.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
