---
title: 추가 파라미터 설정 구성
description: 추가 파라미터를 구성하는 방법(Project Service)
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290772"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="fcd9a-103">추가 파라미터 구성(Project Service)</span><span class="sxs-lookup"><span data-stu-id="fcd9a-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fcd9a-104">이전 토픽에서 항목을 구성하고 나면 프로젝트에 사용할 추가 프로젝트 파라미터를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="fcd9a-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 처음 설치하면 파라미터 설정을 만들어 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]가 작동하기 위해 필요한 모든 레코드를 먼저 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="fcd9a-106">이제 다시 앞으로 돌아가 해당 설정에 대한 추가 필드를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="fcd9a-107">다음과 같은 설정을 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="fcd9a-108">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="fcd9a-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="fcd9a-109">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="fcd9a-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="fcd9a-110">근무 시간 템플릿</span><span class="sxs-lookup"><span data-stu-id="fcd9a-110">Work hours template</span></span>  
  
-   <span data-ttu-id="fcd9a-111">가격표</span><span class="sxs-lookup"><span data-stu-id="fcd9a-111">Price list</span></span>  
 
<span data-ttu-id="fcd9a-112">이 단계에서 원하는 리소스 할당 유형 또한 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="fcd9a-113">**중앙**.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-113">**Central**.</span></span> <span data-ttu-id="fcd9a-114">리소스 관리자만 프로젝트에 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="fcd9a-115">**혼합**.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-115">**Hybrid**.</span></span> <span data-ttu-id="fcd9a-116">자원 관리자, 프로젝트 관리자 및 거래처 관리자가 프로젝트에 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="fcd9a-117">프로젝트 파라미터를 설정하려면</span><span class="sxs-lookup"><span data-stu-id="fcd9a-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="fcd9a-118">**Project Service > 파라미터** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="fcd9a-119">(처음 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 설치할 때 만든) 구성하려는 파라미터 설정을 클릭하거나 **새로 만들기** 를 클릭하여 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="fcd9a-120">**일반** 영역에서 프로젝트 파라미터에 대한 모든 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="fcd9a-121">**가격표 영역** 에서 **+** 를 클릭하여 가격표를 추가하고, **프로젝트 파라미터 가격표** 드롭다운 목록에서 가격표를 선택한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="fcd9a-122">화면 오른쪽 아래 모서리에서 **저장** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="fcd9a-123">올바르게 작동하려면 Project Service에 대해 프로젝트 매개 변수 레코드를 유지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="fcd9a-124">이 레코드는 삭제하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="fcd9a-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fcd9a-125">See Also</span></span>  
 [<span data-ttu-id="fcd9a-126">리소스 설정</span><span class="sxs-lookup"><span data-stu-id="fcd9a-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]