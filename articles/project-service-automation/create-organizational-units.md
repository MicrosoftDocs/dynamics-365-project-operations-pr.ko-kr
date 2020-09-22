---
title: 조직 구성 단위 만들기
description: 조직 단위를 만드는 방법(Project Service)
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f27cfd9d-1265-40e6-b19e-5d02c3d91ca6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2712c8a22d97148b5481be3cb5cced1746ea08e8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753213"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="3aed4-103">조직 단위 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="3aed4-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3aed4-104">회사에서 지리, 기능 또는 다른 지역에 따라 컨설팅 업무를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="3aed4-105">컨설팅 업무를 반영하는 조직 구성 단위를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="3aed4-106">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 조직 단위는 회사의 다른 그룹이나 부서와 다른 급여를 받는 유급 리소스를 채용하는 전문 서비스 회사의 그룹 또는 부서입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3aed4-107">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 조직 구성 단위는 [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]의 업무 단위와 별개입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="3aed4-108">업무 단위는 [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] 정보에 대한 액세스 수준에 영향을 미치는 보안 구조의 성격이 강하며, 일반적으로 모회사 및 자회사 또는 부서 등의 회사 부서를 중심으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="3aed4-109">조직 구성 단위는 컨설팅 회사가 지리적 위치(예: EMEA, LATAM), 기능(예: 제품 개발 또는 IT 아웃소싱), 기타 파라미터별로 다른 업무를 분류하는 방식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="3aed4-110">**Project Service > 조직 단위**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="3aed4-111">**새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="3aed4-112">**일반** 영역에서 **이름**란에 조직 단위 이름을 입력한 후, 필요에 따라 다른 필드를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-112">In the **General** area, enter a name for the organization unit in **Name**, and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="3aed4-113">**저장**을 클릭하여 레코드를 만들면 계속 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="3aed4-114">**원가 목록** 아래 **+** 를 클릭하여 가격표를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-114">Under **Cost Price Lists**, click **+** to add a price list.</span></span> <span data-ttu-id="3aed4-115">여기에서 **비용** 컨텍스트로만 가격표를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="3aed4-116">**이름** 필드의 **검색** 단추를 클릭하고 이 조직 단위에서 사용할 수 있게 하려는 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="3aed4-117">필요에 따라 계속해서 가격표를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="3aed4-118">업을 마쳤으면, 화면 우측 하단의 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed4-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3aed4-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3aed4-119">See Also</span></span>  
 [<span data-ttu-id="3aed4-120">Project Service Automation 구성</span><span class="sxs-lookup"><span data-stu-id="3aed4-120">Configure Project Service Automation</span></span>](../project-service/configure.md)
