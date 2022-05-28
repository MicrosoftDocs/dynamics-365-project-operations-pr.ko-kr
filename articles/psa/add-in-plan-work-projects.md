---
title: Project Service 추가 기능을 사용하여 Microsoft Project의 작업 계획
description: 이 항목은 Microsoft Project Service를 위한 Microsoft Project 추가 기능을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1b1c9861f2a3fbb62b29ccad272dab28dc766439
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728012"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Project Service 추가 기능을 사용하여 Microsoft Project의 작업 계획

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]으로 쉽게 예상을 비롯한 프로젝트 계획을 수행할 수 있습니다. 작업을 정의하여 최종 제안서를 제출할 때 비용, 노력 및 영업 가치를 명확하게 할 수 있습니다.  

[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]을 설치하여 익숙한 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 환경에서 작업을 계획할 수 있습니다. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]의 강력한 계획 및 관리 기능을 사용한 다음 Project Service Automation에서 프로젝트 계획을 업데이트합니다.  

> [!IMPORTANT]
> - SharePoint 문서 관리를 사용하여 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트의 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일을 저장하려면 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 관리자가 문서 관리를 활성화해야 합니다. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]은 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional 에디션과만 호환됩니다.  

## <a name="download-and-install-the-add-in"></a>추가 기능 다운로드 및 설치  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 로그인 정보를 준비합니다. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]로 연결하기 위해 이 정보가 필요합니다.  

1.  다운로드 센터에서 지원되는 Project Service 버전 [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) 또는 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)를 위한 추가 기능을 다운로드할 수 있습니다.  

2.  다운로드 링크를 선택합니다.  

3.  다운로드가 완료되면 **예** 를 선택하여 추가 기능을 설치합니다.  

## <a name="configure-the-add-in"></a>추가 기능 구성  

1. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 열고 **Project Service** 탭을 선택합니다.  

2. **연결** 을 선택합니다.  

3. 로그인 정보를 입력하고 **로그인** 을 선택합니다.  

   이제 이 추가 기능을 사용할 수 있습니다.  

## <a name="read-from-a-template"></a>템플릿에서 읽기  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 만든 템플릿에서 읽어와 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]로 복사하여 프로젝트 계획을 시작할 수 있습니다. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [프로젝트 템플릿 만들기(Project Service Automation)](../psa/create-project-template.md)  

1.  **Project Service** 탭에서 **읽기** > **Project Service Automation 프로젝트 템플릿** 을 선택합니다.  

2.  목록에서 프로젝트 템플릿을 선택하고 **열기** 를 선택합니다.  

    > [!NOTE]
    >  기본적으로 템플릿에서 Project로 복사하는 작업은 수동으로 예약하도록 설정됩니다.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>프로젝트 리소스에 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 역할 할당  

1.  프로젝트를 열고 **작업** 리본을 선택합니다.  

2. **Gantt 차트** 메뉴를 선택한 후 **리소스 시트** 를 선택합니다.  

3. 리소스 시트에서 **Project Service 리소스 역할** 드롭다운 메뉴를 선택하고 Project Service Automation 역할을 선택합니다.  

## <a name="staff-your-project-with-resources"></a>리소스를 사용하여 프로젝트 팀 구성  

1.  Project Service 탭에서 행을 선택하고 **리소스 찾기** 를 선택합니다.  

2.  **리소스 예약** 화면에서 프로젝트에 사용할 리소스를 선택합니다.  

3.  **예약** 을 선택하고 **확인** 을 선택합니다.  

## <a name="publish-your-project"></a>프로젝트 게시  
프로젝트 계획이 완료되면 다음 단계는 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 프로젝트를 가져와 게시하는 것입니다.  

프로젝트는 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]으로 가져옵니다. 가격 산정 및 팀 생성 프로세스가 적용됩니다. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 프로젝트를 열어 팀, 프로젝트 추정, 작업 분할 구조가 생성된 것을 확인합니다. 다음 표에서는 결과를 찾을 수 있는 위치를 보여 줍니다.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt 차트**   | [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **작업 분할 구조 화면** 으로 가져옵니다. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **리소스 시트** |   [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **프로젝트 팀 구성원** 화면으로 가져옵니다.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **사용 용도**    |    [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **프로젝트 추정** 화면으로 가져옵니다.     |

**프로젝트를 가져오고 게시하려면**  
1. **Project Service** 탭에서 **게시** > **새 Project Service Automation 프로젝트** 로 이동합니다.  

2. **Project Service에 새 프로젝트로 게시** 대화 상자에 **프로젝트 이름** 을 입력하고 **고객** 을 선택합니다.  

3. 추가적으로 **Project Service Automation에 프로젝트 계획 연결** 을 선택하여 계획 Project 파일을 Project Service Automation에 연결합니다.  

4. **게시** 를 선택합니다.  

   Project 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결하면 Project 파일이 마스터 파일이 되고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 작업 분할 구조가 읽기 전용으로 설정됩니다.  프로젝트 계획을 수정하려면 이를 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만들고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 업데이트로 게시해야 합니다.  

## <a name="edit-a-project-thats-been-imported"></a>가져온 프로젝트 편집  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]으로 가져온 프로젝트 계획 변경은 두 가지 옵션이 있습니다.  

- 마스터 파일을 열고 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 편집합니다.  

- 파일 연결을 해제하고 Project Service에서 바로 편집합니다. 기본적으로 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 업로드된 프로젝트는 잠겨있으므로 Project에서만 편집할 수 있습니다. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 파일을 편집하려면 파일의 연결을 해제해야 합니다.  

### <a name="edit-in-pn_microsoft_project"></a>[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 편집  

1. 메인 메뉴에서 **Project Service** > **프로젝트** 로 이동합니다.  

2. 프로젝트 목록에서 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만든 프로젝트를 엽니다.  

3. 리본 메뉴에서 **MS Project에서 열기** 를 선택합니다. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 연결된 마스터 파일이 열립니다.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>파일 연결을 해제하고 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service에서 편집  

1. 메인 메뉴에서 **Project Service** > **프로젝트** 로 이동합니다.  

2. 프로젝트 목록에서 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만든 프로젝트를 엽니다.  

3. 리본 메뉴에서 **MS Project에서 연결 해제** 를 선택합니다.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Project 파일을 SharePoint 또는 Office 그룹에 업로드  
 Project 파일을 SharePoint에 업로드하면 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트의 관련 문서에서 찾을 수 있습니다.  관리자가 SharePoint 문서 관리를 구성하고 프로젝트 엔터티에 대해 이를 활성화해야 합니다. 

 또한 Office 그룹을 설정한 경우 Project 파일을 [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]에 업로드할 수 있습니다.

### <a name="upload-a-file-for-sharepoint"></a>SharePoint용 파일 업로드  

1. 메인 메뉴에서 **Project Service** > **업로드** 로 이동합니다.  

2. **Project Service Automation 프로젝트 문서에** 를 선택합니다.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기 허용** 대화 상자에서 **예** 또는 **아니요** 를 선택합니다.  

   - **예** 를 선택하면 Project Service Automation에서 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 를 선택하여 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 시작하고 SharePoint 문서 라이브러리에서 Project 파일을 로드할 수 있습니다.  

   - **아니요** 를 선택하면 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 링크가 작동하지 않습니다.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일은 특정 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트에 대해 **문서** 아래의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 찾을 수 있습니다.  

### <a name="upload-a-file-for-office-groups"></a>Office 그룹에 대해 파일 업로드  

1. 메인 메뉴에서 **Project Service** > **업로드** 로 이동합니다.  

2. **Project Service Automation 프로젝트 문서에** 를 선택합니다.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기 허용** 대화 상자에서 **예** 또는 **아니요** 를 선택합니다.  

   - **예** 를 선택하면 Project Service Automation에서 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 를 선택하여 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 시작하고 SharePoint 문서 라이브러리에서 Project 파일을 로드할 수 있습니다.  

   - **아니요** 를 선택하면 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 링크가 작동하지 않습니다.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일은 특정 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트에 대해 **문서** 아래의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 찾을 수 있습니다.  

## <a name="publish--your-project-as-a-template"></a>프로젝트를 템플릿으로 게시  
 프로젝트를 저장한 다음 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 프로젝트 템플릿으로 저장하여 다시 사용할 수 있습니다. 프로젝트 템플릿은 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 다시 사용할 수 있는 프로젝트 계획입니다. 자세한 내용은 [프로젝트 템플릿 만들기(Project Service Automation)](../psa/create-project-template.md)를 참조하십시오. 

1. **Project Service** 탭에서 **게시** > **새 Project Service Automation 프로젝트 템플릿** 으로 이동합니다.  

2. **Project Service 템플릿에 새 프로젝트로 게시** 대화 상자에 **프로젝트 템플릿 이름** 을 입력합니다.  

3. 추가적으로 **Project Service Automation에 프로젝트 계획 연결** 을 선택하여 계획 Project 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결합니다.  

4. **게시** 를 선택합니다.  

Project 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결하면 Project 파일이 마스터 파일이 되고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 템플릿에서 작업 분할 구조가 읽기 전용으로 설정됩니다.  프로젝트 계획을 수정하려면 이를 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만들고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 업데이트로 게시해야 합니다.

## <a name="read-a-resource-loaded-schedule"></a>리소스 로드 일정 읽기

Project Service Automation에서 프로젝트를 읽을 때 리소스의 일정이 데스크톱 클라이언트에 동기화되지 않습니다. 작업 기간, 노력 또는 종료에 차이가 있는 경우 리소스와 데스크톱 클라이언트에 동일한 작업 시간 템플릿 달력이 프로젝트에 적용되지 않았기 때문일 수 있습니다.


## <a name="data-synchronization"></a>데이터 동기화
이 섹션의 표에서는 Project Service Automation과 Microsoft Project 데스크톱 추가 기능 간의 엔터티 데이터 동기화에 대한 정보를 제공합니다.

### <a name="project-task-entity-table"></a>프로젝트 작업 엔터티 테이블
다음 표에는 Project Service Automation과 Microsoft Project 데스크톱 추가 기능 간에 프로젝트 작업 데이터가 동기화되는 방법이 나와 있습니다.

| **엔터티** | **필드** | **Microsoft Project - Project Service Automation** | **Project Service Automation - Microsoft Project** |
| --- | --- | --- | --- |
| 프로젝트 작업 | 기한 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 예상 작업량 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | MS Project 클라이언트 ID | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 상위 작업 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | Project | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 프로젝트 작업 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 프로젝트 작업 이름 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 리소스 조달 단위(v3.0에서 더 이상 사용되지 않음) | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 예정 기간 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | 시작 날짜 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 | WBS ID | 동기화됨 | 동기화되지 않음 |

### <a name="team-member-entity-table"></a>팀 구성원 엔터티 테이블
다음 표에는 Project Service Automation과 Micros 간에 팀 구성원 엔터티 데이터가 동기화되는 방법이 나와 있습니다.

| **엔터티** | **필드** | **Microsoft Project - Project Service Automation** | **Project Service Automation - Microsoft Project** |
| --- | --- | --- | --- |
| 팀 구성원 | MS Project 클라이언트 ID | 동기화됨 | 동기화되지 않음 |
| 팀 구성원 | 위치 이름 | 동기화됨 | 동기화되지 않음 |
| 팀 구성원 | 프로젝트 | 동기화됨 | 동기화됨 |
| 팀 구성원 | 프로젝트 팀 | 동기화됨 | 동기화됨 |
| 팀 구성원 | 리소스 조달 단위 | 동기화되지 않음 | 동기화됨 |
| 팀 구성원 | 역할 | 동기화되지 않음 | 동기화됨 |
| 팀 구성원 | 근무 시간 | 동기화되지 않음 | 동기화되지 않음 |

### <a name="resource-assignment-entity-table"></a>리소스 할당 엔터티 테이블
다음 표에는 Project Service Automation과 Micros 간에 리소스 할당 엔터티 데이터가 동기화되는 방법이 나와 있습니다.

| **엔터티** | **필드** | **Microsoft Project - Project Service Automation** | **Project Service Automation - Microsoft Project** |
| --- | --- | --- | --- |
| 리소스 할당 | 시작 날짜 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 시간 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | MS Project 클라이언트 ID | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 계획된 작업 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | Project | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 프로젝트 팀 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 리소스 할당 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 작업 | 동기화됨 | 동기화되지 않음 |
| 리소스 할당 | 종료 날짜 | 동기화됨 | 동기화되지 않음 |

### <a name="project-task-dependencies-entity-table"></a>프로젝트 작업 종속성 엔터티 테이블
다음 표에는 Project Service Automation과 Micros 간에 프로젝트 작업 종속성 엔터티 데이터가 동기화되는 방법이 나와 있습니다.

| **엔터티** | **필드** | **Microsoft Project - Project Service Automation** | **Project Service Automation - Microsoft Project** |
| --- | --- | --- | --- |
| 프로젝트 작업 종속성 | 프로젝트 작업 종속성 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 종속성 | 링크 유형 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 종속성 | 선행 업무 작업 | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 종속성 | Project | 동기화됨 | 동기화되지 않음 |
| 프로젝트 작업 종속성 | 후속 업무 작업 | 동기화됨 | 동기화되지 않음 |

### <a name="additional-resources"></a>추가 리소스
 [프로젝트 관리자 가이드](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
