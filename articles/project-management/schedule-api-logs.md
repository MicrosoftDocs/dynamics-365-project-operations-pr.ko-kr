---
title: 프로젝트 일정 로그
description: 이 항목은 프로젝트 일정 로그를 사용하여 프로젝트 일정 서비스 및 프로젝트 일정 API와 관련된 오류를 추적하는 데 도움이 되는 정보와 샘플을 제공합니다.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589526"
---
# <a name="project-scheduling-logs"></a>프로젝트 일정 로그

_**적용 대상:**: 리소스/비재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 발행 처리_, _Project for the Web_

Microsoft Dynamics 365 Project Operations는 [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5)을 기본 일정 엔진으로 사용합니다. 표준 Microsoft Dataverse 웹 API(응용 프로그래밍 인터페이스)를 사용하는 대신 Project Operations는 새로운 프로젝트 일정 API를 사용하여 프로젝트 작업, 리소스 할당, 작업 종속성, 프로젝트 버킷 및 프로젝트 팀 구성원을 생성, 업데이트 및 삭제합니다. 그러나 작성, 업데이트 또는 삭제 작업이 WBS(작업 분할 구조) 엔터티에서 프로그래밍 방식으로 실행되는 경우 오류가 발생할 수 있습니다. 이러한 오류와 작업 기록을 추적하기 위해 두 가지 새로운 관리 로그인 **작업 집합** 및 **프로젝트 일정 서비스(PSS)** 가 구현되었습니다. 이 로그에 액세스하려면 **설정** \> **일정 통합** 으로 이동하십시오.

다음 그림은 프로젝트 일정 로그의 데이터 모델을 보여줍니다.

![프로젝트의 일정 로그의 데이터 모델.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>작업 집합 로그

작업 집합 로그는 프로젝트, 프로젝트 작업, 리소스 할당, 작업 종속성, 프로젝트 버킷 또는 프로젝트 팀 구성원에 대해 하나 이상의 생성, 업데이트 또는 삭제 작업을 일괄적으로 실행하는 데 사용되는 작업 집합의 실행을 추적합니다. **작업 상태** 필드는 작업 집합의 전체 상태를 보여줍니다. 작업 집합 페이로드의 세부 정보는 관련 작업 집합 세부 정보 레코드에 캡처됩니다.

### <a name="operation-set"></a>작업 집합

다음 표는 **작업 집합** 엔터티와 관련된 필드를 보여줍니다.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | 작업 집합이 완료 또는 실패한 날짜/시간입니다.                                                | CompletedOn            |
| msdyn_correlationid   | 요청의 **correlationId** 값입니다.                                                                  | CorrelationId          |
| msdyn_description     | 작업 집합에 대한 설명입니다.                                                                        | Description            |
| msdyn_executedon      | 레코드가 실행된 날짜/시간입니다.                                                                       | 실행 일시            |
| msdyn_operationsetId  | 엔터티 인스턴스의 고유 식별자입니다.                                                                   | OperationSet           |
| msdyn_Project         | 작업 집합과 관련된 프로젝트입니다.                                                            | Project                |
| msdyn_projectid       | 요청의 **projectId** 값입니다.                                                                      | ProjectId(사용되지 않음) |
| msdyn_projectName     | 해당 없음.                                                                                              | 해당 없음         |
| msdyn_PSSErrorLog     | 작업 집합과 연결된 프로젝트 일정 서비스 오류 로그의 고유 식별자입니다. | PSS 오류 로그          |
| msdyn_PSSErrorLogName | 해당 없음.                                                                                              | 해당 없음         |
| msdyn_status          | 작업 집합의 상태입니다.                                                                             | Status                 |
| msdyn_statusName      | 해당 없음.                                                                                              | 해당 없음         |
| msdyn_useraadid       | 이 요청이 속한 사용자의 Azure Active Directory(Azure AD) 개체 ID입니다.                     | UserAADID              |

### <a name="operation-set-detail"></a>작업 집합 세부 정보

다음 표는 **작업 집합 세부 정보** 엔터티와 관련된 필드를 보여줍니다.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | 요청에 대해 직렬화된 Dataverse 필드입니다.                                            | CdsPayload            |
| msdyn_entityname           | 요청의 엔터티 이름입니다.                                                     | EntityName            |
| msdyn_httpverb             | 요청 방법입니다.                                                                         | HTTPVerb(더 이상 사용되지 않음) |
| msdyn_httpverbName         | 해당 없음.                                                                             | 해당 없음        |
| msdyn_operationset         | 이 레코드가 속하는 작업 집합의 고유 식별자입니다.                      | OperationSet          |
| msdyn_operationsetdetailId | 엔터티 인스턴스의 고유 식별자입니다.                                                  | OperationSet 세부 정보   |
| msdyn_operationsetName     | 해당 없음.                                                                             | 해당 없음        |
| msdyn_operationtype        | 작업 집합 세부 정보의 작업 유형입니다.                                             | OperationType         |
| msdyn_operationtypeName    | 해당 없음.                                                                             | 해당 없음        |
| msdyn_psspayload           | 요청에 대해 직렬화된 프로젝트 일정 서비스 필드입니다.                           | PssPayload            |
| msdyn_recordid             | 요청 레코드의 식별자입니다.                                                       | 레코드 ID             |
| msdyn_requestnumber        | 요청을 받은 순서를 식별하는 자동 생성 번호입니다. | 요청 번호        |

## <a name="project-scheduling-service-error-logs"></a>프로젝트 일정 서비스 오류 로그

프로젝트 일정 서비스 오류 로그는 프로젝트 일정 서비스가 **저장** 또는 **열기** 작업을 시도할 때 발생하는 오류를 캡처합니다. 이러한 로그가 생성되는 세 가지 시나리오가 지원됩니다.

- 사용자가 시작한 작업이 치명적으로 실패합니다(예: 권한 누락으로 인해 할당을 생성할 수 없음).
- 프로젝트 일정 서비스가 엔터티에서 프로그래밍 방식으로 생성, 업데이트, 삭제 또는 다른 계단식 작업을 수행할 수 없습니다.
- 레코드를 열지 못하면 사용자에게 오류가 발생합니다(예: 프로젝트가 열리거나 팀 구성원의 정보가 업데이트되는 경우).

### <a name="project-scheduling-service-log"></a>프로젝트 일정 서비스 로그

다음 표는 프로젝트 일정 서비스 로그에 포함된 필드를 보여줍니다.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | 예외의 호출 스택입니다.                                               | 호출 스택     |
| msdyn_correlationid | 오류의 상관 관계 ID입니다.                                               | CorrelationId  |
| msdyn_errorcode     | Dataverse 오류 코드 또는 HTTP 오류 코드를 저장하는 데 사용되는 필드입니다. | 오류 코드     |
| msdyn_HelpLink      | 공개 도움말의 링크입니다.                                       | 도움말 링크      |
| msdyn_log           | 프로젝트 일정 서비스의 로그입니다.                                   | 로그            |
| msdyn_project       | 오류 로그와 연관된 프로젝트입니다.                             | Project        |
| msdyn_projectName   | 작업 집합의 페이로드가 지속되는 경우 프로젝트의 이름입니다. | 해당 없음 |
| msdyn_psserrorlogId | 엔터티 인스턴스의 고유 식별자입니다.                                     | PSS 오류 로그  |
| msdyn_SessionId     | 프로젝트 세션 ID입니다.                                                        | 세션 ID     |

## <a name="error-log-cleanup"></a>오류 로그 정리

기본적으로 프로젝트 일정 서비스 오류 로그와 작업 집합 로그는 모두 90일마다 정리할 수 있습니다. 90일이 지난 모든 레코드는 삭제됩니다. 그러나 **프로젝트 매개변수** 페이지에서 **msdyn_StateOperationSetAge** 필드의 값을 변경함으로써 관리자는 정리 범위를 1일에서 120일 사이로 조정할 수 있습니다. 이 값을 변경하는 몇 가지 방법을 사용할 수 있습니다.

- 사용자 지정 페이지를 만들고 **부실 작업 집합 기간** 필드를 추가하여 **프로젝트 매개변수** 항목을 사용자 지정합니다.
- [WebApi 소프트웨어 개발 키트(SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)를 사용하는 클라이언트 코드를 사용합니다.
- 모델 기반 앱의 Xrm SDK **updateRecord** 메서드(클라이언트 API 참조)를 사용하는 서비스 SDK 코드를 사용합니다. Power Apps에는 **updateRecord** 메서드에 대한 설명과 지원되는 매개변수가 포함되어 있습니다.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
