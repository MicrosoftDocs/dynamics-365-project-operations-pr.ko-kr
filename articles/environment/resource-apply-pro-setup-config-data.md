---
title: Common Data Service에서 구성 데이터 설정 및 적용
description: 이 항목은 Project Operations에서 구성 데이터를 설정하고 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26f49ad3b9fb08824071699128f8b907ec98bb54505c6fea3c97288cbaf31633
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986634"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Common Data Service에서 구성 데이터 설정 및 적용 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>필수 조건

Common Data Service(CDS)에서 데이터 구성을 시작하기 전에 다음 전제 조건이 충족되어야 합니다.

1.  CDS 환경 및 Project Operations을 위한 Dynamics 365 Finance 환경을 프로비저닝합니다.
2.  Dynamics 365 Finance의 법인 정보는 CDS 환경에 공유됩니다. 즉 CDS의 **회사** 법인에는 다음과 같은 회사 기록이 있습니다.
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>설정 및 구성 데이터 설치

1. [설정 및 구성 데이터 패키지](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)를 다운로드, 차단 해제 및 압축 해제합니다.
2. 압축이 풀린 폴더로 이동하여 *DataMigrationUtility* 실행 파일을 실행합니다.
3. Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기** 를 선택한 다음 **계속** 을 선택합니다.

![구성 마이그레이션.](./media/1ConfigurationMigration.png)

4. CMT 마법사의 2페이지에서 **Microsoft 365** 를 **배포 유형** 으로 선택합니다.
5. **사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.
6. 테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인** 을 선택합니다.

![구성 로그인.](./media/2ConfigurationSignin.png)

7. 3 페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인** 을 선택합니다.
8. 4 페이지에서 압축을 푼 폴더에서 zip 파일 *SampleSetupAndConfigData* 를 선택합니다.

![Zip 파일 선택.](./media/3ZipFile.png)

![파일 선택.](./media/4SelectAFile.png)

9. Zip 파일을 선택한 후 **데이터 가져오기** 를 선택합니다.

![데이터 가져오기.](./media/5ImportData.png)

10. 가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다. 가져오기가 완료되면 CMT 마법사를 종료합니다. 
11. 조직에서 다음 26개 항목의 데이터를 확인합니다.

  - 통화
  - 계정 차트
  - 회계 달력
  - 통화 환율 유형
  - 지불 날짜
  - 지불 일정
  - 지불 조건
  - 조직 구성 단위
  - 연락처
  - 세금 그룹
  - 고객 그룹
  - 공급업체 그룹
  - 단위
  - 단위 그룹
  - 가격표
  - 프로젝트 한도 가격표
  - 송장 빈도
  - 예약 가능한 리소스 범주
  - 거래 범주
  - 경비 범주
  - 역할 가격
  - 거래 범주 가격
  - 특징
  - 예약 가능한 리소스
  - 예약 가능한 리소스 범주 연결
  - 예약 가능한 리소스 특징

![가져오기 완료.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations 구성 업데이트

1. CE 환경으로 이동합니다. [Power Platform 관리 센터](https://admin.powerplatform.microsoft.com/environments)를 열고 환경을 선택한 다음 **환경 열기** 를 선택하면 찾을 수 있습니다. 

![환경 열기.](./media/7OpenEnvironment.png)

2. **프로젝트** > **리소스** 로 이동한 다음 **새로 만들기** 를 선택하여 사용자를 위해 예약 가능한 리소스를 만듭니다.

![예약 가능한 리소스.](./media/8BookableResources.png)

3. **일반** 탭에서 관리 사용자를 선택합니다. 시간대가 현재 있는 시간대와 일치하는지 확인합니다. 

![새 예약 가능한 리소스.](./media/9NewBookableResource.png)

4. **스케줄링** 탭의 **회사** 필드에서 **USPM** 회사를 선택한 다음 **저장** 을 선택합니다. 

![일정 탭.](./media/10SchedulingTab.png)

5. **작업 시간** 탭을 선택합니다.  

![근무 시간.](./media/11WorkHours.png)

6. 일정에서 값을 두 번 클릭하고 **편집** > **시리즈의 모든 이벤트** 를 선택합니다. 

![작업 일정.](./media/12WorkCalendar.png)

7. 근무 시간을 8시간 근무일로 변경하고 주말을 휴무일로 표시하고 시간대가 자신의 시간대와 일치하는지 확인합니다. 
8. **저장 후 닫기** 를 선택합니다.

![일정 업데이트.](./media/13UpdateCalendar.png)

9. **설정** > **일정 템플릿** 으로 이동하고 **새로 만들기** 를 선택합니다.
 
 ![일정 템플릿.](./media/14CalendarTemplates.png)
 
 10. 이름을 입력하고 생성한 템플릿 리소스를 선택한 다음 **저장** 을 선택합니다. 
 
 ![일정 템플릿 저장.](./media/15SaveCalendarTemplate.png)
 
 11. **매개 변수** 로 이동하고 레코드를 두 번 클릭합니다. 
 
 ![프로젝트 매개 변수.](./media/16ProjectParameters.png)
 
12. 다음 필드를 업데이트합니다.

 - **기본 회사**: USPM
 - **기본 조직 단위**:Contoso Robotics Global
 - **송장 빈도**: 일곱째 날과 마지막 날
 - **근무 시간 템플릿**: 생성한 템플릿으로 변경합니다.

13. **저장** 을 선택합니다. 

![업데이트된 프로젝트 매개 변수.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
