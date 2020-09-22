---
title: 조직 구성 단위
description: 이 항목은 Dynamics 365 Project Service Automation의 조직 구성 단위에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753370"
---
# <a name="organizational-units"></a><span data-ttu-id="f0562-103">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="f0562-103">Organizational units</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f0562-104">Dynamics 365 Project Service Automation, 조직 구성 단위는 비용 요금이 있는 청구 가능한 리소스를 사용하는 전문 서비스 회사의 고유한 그룹 또는 부서입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-104">Dynamics 365 Project Service Automation, an organizational unit is a distinct group or division in a professional services company that employs billable resources that have cost rates.</span></span>

<span data-ttu-id="f0562-105">다양한 실무 영역이나 비즈니스 라인에서 기술 리소스를 사용하는 전문 서비스 회사의 경우 한 실무 영역이나 비즈니스 라인에서 역할을 채우는 비용은 다른 실무 영역이나 비즈니스 라인에서 역할을 채우는 비용과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-105">For professional services companies that employ technical resources in various practice areas or business lines, the cost to fill a role in one practice area or business line might differ from the cost to fill a role in another practice area or business line.</span></span> <span data-ttu-id="f0562-106">개념 조직 구성 단위는 이러한 역할에 대해 고유한 비용 구조를 가지는 회사의 부서에서 청구 가능한 역할 집합을 그룹화하는 방법을 제공하여 이 시나리오에서 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-106">The concept  organizational units helps in this scenario by providing a way to group a set of billable roles in a division of a company that has a distinct cost structure for these roles.</span></span>

## <a name="key-attributes-and-associations-of-organizational-units"></a><span data-ttu-id="f0562-107">주요 속성 및 조직 구성 단위의 연결</span><span class="sxs-lookup"><span data-stu-id="f0562-107">Key attributes and associations of organizational units</span></span>

<span data-ttu-id="f0562-108">PSA에서 PSA의 조직 구성 단위에는 특정 통화 및 특정 비용 가격표가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-108">In PSA, an organizational unit in PSA has a specific currency and specific cost price lists.</span></span>

<span data-ttu-id="f0562-109">조직 구성 단위의 통화는 비용을 추적하는 데 사용되는 기본 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-109">The currency of an organizational unit is the primary currency that is used to track costs.</span></span>

<span data-ttu-id="f0562-110">하나 이상의 비용 가격표는 각 조직 구성 단위에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-110">One or more cost price lists can be attached to each organizational unit.</span></span> <span data-ttu-id="f0562-111">PSA는 조직 구성 단위에 연결할 수 있는 가격표에 다음과 같은 제한을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-111">PSA puts the following limitations on the price lists that can be attached to an organizational unit:</span></span>

- <span data-ttu-id="f0562-112">가격표는 조직 구성 단위의 통화여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-112">Price lists must be in the currency of the organizational unit</span></span>
- <span data-ttu-id="f0562-113">가격표는 비용 가격표여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-113">Price lists must be of cost price lists</span></span>

<span data-ttu-id="f0562-114">또한 리소스 엔터티의 조직 구성 단위에 대한 특성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-114">In addition, there is an attribute for the organizational unit on the Resource entity.</span></span> <span data-ttu-id="f0562-115">각 리소스는 한 조직 구성 단위에만 할당될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-115">Each resource can be assigned to one organizational unit.</span></span>

## <a name="roles-of-organizational-units"></a><span data-ttu-id="f0562-116">조직 구성 단위의 역할</span><span class="sxs-lookup"><span data-stu-id="f0562-116">Roles of organizational units</span></span>

<span data-ttu-id="f0562-117">조직 구성 단위는 PSA에서 두 가지 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-117">The organizational unit plays two roles in PSA:</span></span>

- <span data-ttu-id="f0562-118">**계약 단위** - 판매에 성공하고 고객에게 작업 및 서비스 제공을 관리하는 책임이 있는 회사 그룹 또는 부서를 대표하는 조직 구성 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-118">**Contracting unit** – The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> <span data-ttu-id="f0562-119">계약 단위는 **영업 기회**, **견적**, **프로젝트 계약** 및 **프로젝트** 페이지의 헤더 섹션에 있는 **계약 단위** 필드로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-119">The contracting unit is identified by the **Contracting Unit** field in the header section of the **Opportunity**, **Quote**, **Project Contract**, and **Project** pages.</span></span>
- <span data-ttu-id="f0562-120">**리소스 단위** - 리소스가 속하거나 할당된 조직 구성 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-120">**Resourcing unit** – The organizational unit that a resource belongs to or is assigned to.</span></span> <span data-ttu-id="f0562-121">이 조직 구성 단위는 SOW(작업 명세서) 및 계약 단위가 소유한 프로젝트에 대한 일부 역할에 대한 리소스를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-121">This organizational unit can provide its resources for some roles on statements of work (SOWs) and projects that are owned by the contracting unit.</span></span>

> ![계약 단위 및 리소스 조달 단위](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a><span data-ttu-id="f0562-123">조직 구성 단위 FAQ</span><span class="sxs-lookup"><span data-stu-id="f0562-123">Organizational unit FAQs</span></span>

<span data-ttu-id="f0562-124">다음은 조직 구성 단위에 대한 몇 가지 질문입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-124">Here are some of the most frequently asked questions about organizational units.</span></span>

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a><span data-ttu-id="f0562-125">PSA의 조직 구성 단위 엔터티는 Dynamics 365에 이미 있는 조직 구성 엔터티와 어떻게 관련이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-125">How is the Organizational Unit entity in PSA related to the Organization entity that already exists in Dynamics 365?</span></span>

<span data-ttu-id="f0562-126">Microsoft Dynamics 365의 조직 구성 엔터티는 전체 Dynamics 365 인스턴스의 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-126">The Organization entity in Microsoft Dynamics 365 represents the name of a global Dynamics 365 instance.</span></span> <span data-ttu-id="f0562-127">이 이름은 일반적으로 글로벌 기업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-127">This name is usually the name of the global enterprise.</span></span>

<span data-ttu-id="f0562-128">조직 구성 단위 엔터티는 글로벌 엔터프라이즈의 그룹 또는 부서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-128">The Organizational Unit entity represents a group or division in the global enterprise.</span></span> <span data-ttu-id="f0562-129">이 그룹 또는 부서에는 해당 역할에 대한 역할 집합과 비용 가격표가 있으며 이러한 역할 및 가격표는 엔터프라이즈의 다른 그룹 또는 부서의 역할 및 가격표와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-129">This group or division has a set of roles and a cost price list for those roles, and those roles and price list differ from the roles and price list of other groups or divisions in the enterprise.</span></span>

<span data-ttu-id="f0562-130">PSA가 설치되면 조직에 따라 기본 조직 구성 단위가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-130">When PSA is installed, a default organizational unit is created based on the organization.</span></span> <span data-ttu-id="f0562-131">모든 기존 리소스는 기본 조직 구성 단위에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-131">All existing resources are assigned to the default organizational unit.</span></span> <span data-ttu-id="f0562-132">새 Active Directory 사용자 또는 리소스를 Dynamics 365로 가져오는 경우, 사용자 가져오기 프로세스는 이를 PSA의 기본 조직 구성 단위에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-132">If any new Active Directory users or resources are imported into Dynamics 365, the user import process assigns them to the default organizational unit in PSA.</span></span>
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a><span data-ttu-id="f0562-133">조직 구성 단위 엔터티는 비즈니스 단위 엔터티와 어떻게 다릅니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-133">How does the organizational unit entity differ from the business unit entity?</span></span>

<span data-ttu-id="f0562-134">Dynamics 365에서 비즈니스 단위 엔터티는 보안 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-134">In Dynamics 365, the Business Unit entity is a security construct.</span></span> <span data-ttu-id="f0562-135">비즈니스 단위와 사용자를 연결하면 사용자가 액세스할 수 있는 엔터티 및 엔터티 레코드가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-135">The association of a user with a business unit determines the entities and entity records that the user has access to.</span></span> <span data-ttu-id="f0562-136">또한 사용자가 해당 엔터티 레코드에 대해 가지고 있는 권한(생성, 읽기, 쓰기, 삭제, 추가, 다음에 추가, 할당 또는 공유)을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-136">It also determines the permissions (Create, Read, Write, Delete, Append, Append To, Assign, or Share) that the user has for those entity records.</span></span>

<span data-ttu-id="f0562-137">조직 구성 단위 엔터티는 할당된 직원에 대해 고유한 비용 비율이 있는 회사 그룹 또는 부서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-137">The Organizational Unit entity represents a company group or division that has distinct cost rates for employees that are assigned to it.</span></span> <span data-ttu-id="f0562-138">조직 구성 단위와 리소스의 연결은 프로젝트 참여에 대한 리소스 비용을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-138">The association of a resource with an organizational unit determines the resource's cost to a project engagement.</span></span>

<span data-ttu-id="f0562-139">Dynamics 365를 구현할 때 사업부의 계층 구조에 대한 보안 권한 부여와 사업부에 사용자를 할당하는 데 최적화합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-139">When you implement Dynamics 365, optimize security authorization for the hierarchy of business units and the assignment of users to business units.</span></span> <span data-ttu-id="f0562-140">일반적으로 동일한 레코드 집합에 액세스해야 하는 모든 사용자를 동일한 사업부에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-140">Assign all users who must typically access the same set of records to the same business unit.</span></span> <span data-ttu-id="f0562-141">조직 구성 단위는 보안 권한 부여 또는 액세스에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-141">The organizational unit has no effect on security authorization or access.</span></span>

#### <a name="example-of-organizational-units-and-business-units"></a><span data-ttu-id="f0562-142">조직 구성 단위 및 사업부의 예</span><span class="sxs-lookup"><span data-stu-id="f0562-142">Example of organizational units and business units</span></span>

<span data-ttu-id="f0562-143">Contoso, Ltd.는 번창하는 Microsoft 기술 방법을 가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-143">Contoso, Ltd. has a thriving Microsoft technology practice.</span></span> <span data-ttu-id="f0562-144">인과 해원은 모두 C\# 개발자이지만, 해원은 미국에 있는 반면 인은 인도에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-144">Prakash and Tricia are both C\# developers, but Tricia is in the United States, whereas Prakash is in India.</span></span> <span data-ttu-id="f0562-145">대부분의 프로젝트 계약에는 Contoso India 및 Contoso US의 리소스가 필요하며 인과 해원은 이 방법 영역의 프로젝트에 동일한 수준의 보안 액세스가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-145">Most of the project engagements require resources from Contoso India and Contoso US, and Prakash and Tricia require the same level of security access to projects in this practice area.</span></span> <span data-ttu-id="f0562-146">그러나 Contoso India의 개발자 비용은 Contoso US의 개발자 비용과 크게 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-146">However, the cost of developers from Contoso India differs significantly from the cost of developers from Contoso US.</span></span>

<span data-ttu-id="f0562-147">다음은 Dynamics 365 및 PSA를 사용하여 이 시나리오를 디자인하는 최적의 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-147">Here is an optimal way to design for this scenario by using Dynamics 365 and PSA.</span></span>

1. <span data-ttu-id="f0562-148">Microsoft 기술 방법을 사업부로 만들고 인과 해원을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-148">Create the Microsoft technology practice as a business unit, and associate Prakash and Tricia with it.</span></span> <span data-ttu-id="f0562-149">이러한 방식으로 두 직원이 해당 방법 영역의 모든 프로젝트에 동일한 수준의 보안 액세스를 갖도록 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-149">In this way, you help guarantee that both employees have the same level of security access to any projects in that practice area.</span></span> <span data-ttu-id="f0562-150">둘 다 진행 상황을 확인하고 시간, 비용 및 작업 업데이트를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-150">They both will be able to check progress and report time, expenses, and task updates.</span></span> 
2. <span data-ttu-id="f0562-151">프로젝트 비용이 올바르게 반영되도록 두 개의 조직 구성 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-151">Create two organizational units to hel guarantee that the cost to the project is correctly reflected.</span></span> 
3. <span data-ttu-id="f0562-152">해원을 Contoso US과 연결하고 인을 Contoso India와 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-152">Associate Tricia wtih Contoso US and associate Prakash with Contoso India.</span></span>
4. <span data-ttu-id="f0562-153">두 조직 구성 단위에 적절한 비용 가격표을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-153">Assign appropriate cost price lists to both organizational units.</span></span> <span data-ttu-id="f0562-154">이러한 방식으로 인과 해원 프로젝트에 기록된 비용이 Contoso US와 Contoso India 간의 비용 차이를 정확하게 반영하도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-154">TIn this way, you help guarantee that the costs that are recorded on the project for Prakash and Tricia accurately reflect the difference in costs between Contoso US and Contoso India.</span></span>

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a><span data-ttu-id="f0562-155">조직 구성 단위가 Dynamics 365의 판매 영역과 관련이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-155">Are organizational units related to sales territories in Dynamics 365?</span></span>

<span data-ttu-id="f0562-156">영업권역과 조직 구성 단위 간에는 연결 또는 관계가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-156">There is no association or relationship between sales territories and organizational units.</span></span> <span data-ttu-id="f0562-157">영업권역은 일반적으로 판매가 발생하는 지리적 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-157">A sales territory is typically a geographical area where sales occur.</span></span> <span data-ttu-id="f0562-158">영업 가격표는 각 영업권역에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-158">A sales price list can be associated with each sales territory.</span></span>

<span data-ttu-id="f0562-159">조직 구성 단위는 회사의 내부 그룹 또는 부서로, 다른 부서 또는 외부 고객에게 판매하는 일련의 역할에 대한 비용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-159">An organizational unit is an internal group or division in the company that tracks costs for a set of roles that it sells to other divisions or to external customers.</span></span>

#### <a name="example-of-organizational-units-and-sales-territories"></a><span data-ttu-id="f0562-160">조직 구성 단위 및 영업권역의 예</span><span class="sxs-lookup"><span data-stu-id="f0562-160">Example of organizational units and sales territories</span></span>

<span data-ttu-id="f0562-161">Contoso, Ltd.는 Contoso US 및 Contoso India 두 개의 개발 센터를 가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-161">Contoso, Ltd. has two development centers: Contoso US and Contoso India.</span></span> <span data-ttu-id="f0562-162">자원 비용은 이 두 개발 센터 간에 크게 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-162">Costs of resources differ greatly between these two development centers.</span></span>

<span data-ttu-id="f0562-163">Contoso는 라틴 아메리카, 북아메리카, 아시아 태평양, 서유럽 및 중동과 같은 많은 국제 시장에서 IT 서비스를 판매하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-163">Contoso sells its IT services in many international markets, such as Latin America, North America, Asia-Pacific, Western Europe, and the Middle East.</span></span> <span data-ttu-id="f0562-164">동일한 프로젝트 역할에 대한 청구 요금은 이러한 시장마다 크게 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-164">Bill rates for the same project roles can vary widely across these markets.</span></span>

<span data-ttu-id="f0562-165">Contoso US 및 Contoso India는 조직 구성 단위로 설정해야 하며, 각 조직 구성 단위에는 자체 비용 가격표가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-165">Contoso US and Contoso India should be set up as organizational units, and each organizational unit should have its own cost price list.</span></span> <span data-ttu-id="f0562-166">아시아 태평양, 라틴 아메리카, 북아메리카, 서유럽 및 중동은 판매 지역으로 설정되어야 하며, 각 영업권역에는 자체 영업 가격표가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-166">Asia-Pacific, Latin America, North America, Western Europe, and the Middle East should be set up as sales territories, and each sales territory should have its own sales price list.</span></span>

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a><span data-ttu-id="f0562-167">가격표와 조직 구성 단위의 연관성에 제한이 있는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-167">Why is there a restriction on the association of price lists with organizational units?</span></span> 

<span data-ttu-id="f0562-168">영업 가격은 일반적으로 서비스가 판매되는 지리적 영역 또는 시장에 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-168">Sales pricing is usually unique to the geographical areas or markets where services are sold.</span></span> <span data-ttu-id="f0562-169">회사의 내부 부서에는 일반적으로 동일한 유형의 서비스에 대한 자체 가격표가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-169">Internal divisions of a company don't usually have their own sales pricing for the same type of services.</span></span> <span data-ttu-id="f0562-170">그러나 내부 부서는 고용하는 사람들의 기술과 그들이 운영하는 지역의 노동 조건에 따라 판매 된 상품 (COGS)의 다른 비용을 가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-170">However, internal divisions have a different cost of goods sold (COGS), depending on the skills of the people that they employ and the labor conditions of the region where they operate.</span></span> <span data-ttu-id="f0562-171">조직 구성 단위는 회사의 내부 부서로 모델링되므로 비용 가격표만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-171">Because organizational units are modeled as internal divisions of a company, they can have only cost price lists.</span></span>

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a><span data-ttu-id="f0562-172">영업 가격표를 조직 구성 단위로 연결할 수 없는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-172">Why can’t we associate sales price lists to organizational units?</span></span>

<span data-ttu-id="f0562-173">PSA에서 영업 가격표는 고객 및 판매 지역과 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-173">In PSA, sales price lists can be associated with customers and sales territories.</span></span> <span data-ttu-id="f0562-174">영업 기회, 견적, 프로젝트 계약 및 프로젝트와 같은 트랜잭션 엔터티는 고객 계정 또는 영업권역에 연결된 영업 가격표를 사용하여 프로젝트 참여에 대한 청구서 비율 및 잠재적 수익을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-174">Transactional entities like Opportunity, Quote, Project Contract, and Project use sales price lists that are attached to the customer account or the sales territory to determine bill rates and potential revenue on the project engagement.</span></span>

<span data-ttu-id="f0562-175">비용 가격표는 조직 구성 단위와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-175">Cost price lists are associated with organizational units.</span></span> <span data-ttu-id="f0562-176">영업 기회, 견적, 프로젝트 계약 및 프로젝트와 같은 트랜잭션 엔터티는 계약 단위에 연결된 영업 가격표를 사용하여 프로젝트 계약에 대한 비용을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-176">Transactional entities like Opportunity, Quote, Project Contract, and Project use cost price lists that are attached to the contracting unit to determine costs to a project engagement.</span></span>

### <a name="are-organizational-units-hierarchical-in-psa"></a><span data-ttu-id="f0562-177">조직 구성 단위가 PSA에서 계층적입니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-177">Are organizational units hierarchical in PSA?</span></span>

<span data-ttu-id="f0562-178">번호</span><span class="sxs-lookup"><span data-stu-id="f0562-178">No.</span></span> <span data-ttu-id="f0562-179">PSA의 현재 릴리스에서 조직 구성 단위는 계층적이지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-179">In the current release of PSA, organizational units are not hierarchical.</span></span> <span data-ttu-id="f0562-180">즉, 다음을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-180">This means that you can’t:</span></span>

- <span data-ttu-id="f0562-181">계층 구조를 통과하는 기본 비용 가격에 대한 패턴을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-181">Configure a pattern for defaulting cost prices that traverses up a hierarchy.</span></span> 
- <span data-ttu-id="f0562-182">조직 구성 단위 계층 구조의 여러 수준에서 롤업된 수익 또는 비용을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-182">Report revenue or cost rolled up at different levels of the organizational unit hierarchy.</span></span>

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a><span data-ttu-id="f0562-183">우리는 비용 센터, 부서 및 청구 사무실의 복잡하고 다단계 계층 구조를 갖춘 대규모 다국적 기업입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-183">We're a big multinational firm with a complex, multilevel hierarchy of cost centers, divisions, and billing offices.</span></span> <span data-ttu-id="f0562-184">이 버전의 Project Service 앱에서 조직 구성 단위 개념을 최대한 활용하려면 어떻게 해야 할까요?</span><span class="sxs-lookup"><span data-stu-id="f0562-184">How can we make the best use of the organizational unit concept in this version of the Project Service app?</span></span>

<span data-ttu-id="f0562-185">비용 센터, 부서, 청구 사무실 등의 복잡한 계층 구조가 있는 경우 해당 계층의 리프 노드를 고유한 조직 구성 단위로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-185">When you have a complex hierarchy of cost centers, divisions, billing offices, etc., set up the leaf nodes of that hierarchy as distinct organizational units.</span></span>
<span data-ttu-id="f0562-186">다음 예제에서는 일반적인 계층 구조를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-186">The following example shows a typical hierarchy:</span></span>

<span data-ttu-id="f0562-187">**Contoso India**</span><span class="sxs-lookup"><span data-stu-id="f0562-187">**Contoso India**</span></span>

  - <span data-ttu-id="f0562-188">SAP 방법</span><span class="sxs-lookup"><span data-stu-id="f0562-188">SAP Practice</span></span> 

    - <span data-ttu-id="f0562-189">기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-189">Technical Consultants</span></span> 
    - <span data-ttu-id="f0562-190">기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-190">Functional Consultants</span></span> 
    
  - <span data-ttu-id="f0562-191">Microsoft 기술 방법</span><span class="sxs-lookup"><span data-stu-id="f0562-191">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="f0562-192">기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-192">Technical Consultants</span></span>
    - <span data-ttu-id="f0562-193">기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-193">Functional Consultants</span></span> 
    
<span data-ttu-id="f0562-194">**Contoso US**</span><span class="sxs-lookup"><span data-stu-id="f0562-194">**Contoso US**</span></span>

 - <span data-ttu-id="f0562-195">SAP 방법</span><span class="sxs-lookup"><span data-stu-id="f0562-195">SAP Practice</span></span> 

    - <span data-ttu-id="f0562-196">기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-196">Technical Consultants</span></span> 
    - <span data-ttu-id="f0562-197">기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-197">Functional Consultants</span></span> 
    
 - <span data-ttu-id="f0562-198">Microsoft 기술 방법</span><span class="sxs-lookup"><span data-stu-id="f0562-198">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="f0562-199">기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-199">Technical Consultants</span></span> 
    - <span data-ttu-id="f0562-200">기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-200">Functional Consultants</span></span> 
 
<span data-ttu-id="f0562-201">계층 구조가 비슷하면 다음과 같이 플랫 목록으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-201">If your hierarchy is similar, you must set it up as a flat list, as shown here:</span></span>
- <span data-ttu-id="f0562-202">Contoso India - SAP 방법 - 기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-202">Contoso India - SAP Practice - Technical Consultants</span></span> 
- <span data-ttu-id="f0562-203">Contoso India - SAP 방법 - 기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-203">Contoso India - SAP Practice - Functional Consultants</span></span>       
- <span data-ttu-id="f0562-204">Contoso India - Microsoft 기술 방법 기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-204">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="f0562-205">Contoso India - Microsoft 기술 방법 기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-205">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="f0562-206">Contoso US - SAP 방법 - 기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-206">Contoso US - SAP Practice - Technical Consultants</span></span>  
- <span data-ttu-id="f0562-207">Contoso US - SAP 방법 - 기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-207">Contoso US - SAP Practice - Functional Consultants</span></span>  
- <span data-ttu-id="f0562-208">Contoso US - Microsoft 기술 방법 - 기술 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-208">Contoso US - Microsoft Technology Practice - Technical Consultants</span></span> 
- <span data-ttu-id="f0562-209">Contoso US - Microsoft 기술 방법 - 기능 컨설턴트</span><span class="sxs-lookup"><span data-stu-id="f0562-209">Contoso US - Microsoft Technology Practice - Functional Consultants</span></span>

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a><span data-ttu-id="f0562-210">우리는 하나의 부서로 운영되는 작은 전문 서비스 회사입니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-210">We're a small professional services company that operates as only one division.</span></span> <span data-ttu-id="f0562-211">PSA의 현재 버전에서 조직 구성 단위 개념을 가장 잘 사용할 수 있는 방법은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-211">How can we best use the organizational unit concept in the current version of PSA?</span></span>

<span data-ttu-id="f0562-212">회사에서 하나의 비용 가격표가 있는 하나의 단위로 운영되는 경우, 조직 구성 단위를 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-212">If your company operates as one unit that has one cost price list, you don't have to set up any organizational units.</span></span> <span data-ttu-id="f0562-213">PSA 설치 중에, Dynamics 365는 조직과 이름이 같은 하나의 기본 조직 구성 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-213">During PSA installation, Dynamics 365 creates one default organizational unit that has the same name as the organization.</span></span> <span data-ttu-id="f0562-214">기본적으로 모든 사용자는 이 조직 구성 단위에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-214">By default, all users are assigned to this organizational unit.</span></span> <span data-ttu-id="f0562-215">시스템에서 조직 단위를 선택해야 할 때마다, 기본적으로 이 조직 구성 단위가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-215">Whenever the system requires that an organizational unit be selected, this organizational unit is selected by default.</span></span>

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a><span data-ttu-id="f0562-216">견적 또는 프로젝트 계약 내용에서 프로젝트를 만들 때 기본 계약 단위는 견적 또는 프로젝트 계약에서 비롯됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-216">When a project is created from a quote or project contract line, the default contracting unit comes from the quote or project contract.</span></span> <span data-ttu-id="f0562-217">견적 또는 프로젝트 계약과 같은 판매 엔터티 보다 먼저 프로젝트를 만든 경우 기본 계약 단위는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f0562-217">If a project is created before sales entities such as quote or project contract, what is the default contracting unit?</span></span>

<span data-ttu-id="f0562-218">프로젝트를 자체적으로 만들 때 프로젝트의 기본 계약 단위는 프로젝트를 만드는 사용자를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-218">When a project is created on its own, the default contracting unit of the project is based on the user who creates it.</span></span> <span data-ttu-id="f0562-219">해당 사용자는 기본 프로젝트 관리자이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-219">That user is also the default project manager.</span></span> <span data-ttu-id="f0562-220">프로젝트가 견적 또는 프로젝트 계약과 같은 판매 엔터티에 매핑되는 경우 프로젝트의 계약 단위는 대신 영업 엔터티를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-220">If the project is mapped to a sales entity such as a quote or project contract, the contracting unit on the project is based on the sales entity instead.</span></span> <span data-ttu-id="f0562-221">이 경우 계약 단위가 변경된 경우 비용 견적 변경을 계산하는 데 비용 가격표가 사용되므로 프로젝트 예상 값이 다시 계산될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-221">In this case, project estimates might be recalculated, because the cost price list is used to calculate the cost estimate changes if the contracting unit is changed.</span></span> <span data-ttu-id="f0562-222">영업 가격표는 견적의 프로젝트 가격표와 동기화되도록 변경될 판매 예상 값을 계산하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-222">The sales price list is used to calculate the sales estimates that will be changed so that they are in sync with the project price list on the quote.</span></span>

<span data-ttu-id="f0562-223">프로젝트의 **계약 단위** 및 **통화** 필드는 프로젝트가 매핑되는 판매 엔터티(견적 또는 프로젝트 계약)의 값과 동기화되어야 하기 때문에 편집을 위해 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="f0562-223">The **Contracting Unit** and **Currency** fields on the project are locked for editing, because they must be in sync with the values on the sales entity (quote or project contract) that the project is mapped to.</span></span>
