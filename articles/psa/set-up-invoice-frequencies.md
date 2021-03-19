---
title: 송장 빈도 설정
description: 송장 빈도를 설정하는 방법(Project Service)
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 21baa270c307aaee584d6ea1c6d133a48dcbe485
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282521"
---
# <a name="set-up-invoice-frequencies-project-service"></a><span data-ttu-id="3e652-103">송장 빈도 설정(Project Service)</span><span class="sxs-lookup"><span data-stu-id="3e652-103">Set up invoice frequencies (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="3e652-104">송장 빈도는 지정 주기에 따라 클라이언트에게 청구하는 빈도를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-104">invoice frequencies determine how often you bill your clients, and on which day of the time period you specify.</span></span> <span data-ttu-id="3e652-105">월간, 격주간, 주간처럼 클라이언트에게 청구할 때 사용할 각 기간에 대한 송장 빈도를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-105">Set up an invoice frequency for each time period you plan to use for billing your clients, such as monthly, biweekly, or weekly.</span></span>  
  
1.  <span data-ttu-id="3e652-106">**Project Service > 송장 빈도** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-106">Go to **Project Service > Invoice Frequencies**.</span></span>  
  
2.  <span data-ttu-id="3e652-107">**새로 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-107">Click **New**.</span></span>  
  
3.  <span data-ttu-id="3e652-108">**일반** 영역에서, **이름** 에 송장 빈도에 대한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-108">In the **General** area, enter a name for the invoice frequency in **Name**.</span></span>  
  
4.  <span data-ttu-id="3e652-109">**기간** 에서 **월간**, **격주간** 또는 **주간** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-109">In **Period**, select **Monthly**, **Biweekly**, or **Weekly**.</span></span>  
  
5.  <span data-ttu-id="3e652-110">월간 또는 격주간으로 기간을 지정한 경우, **실행 일 수** 에서 지정된 기간마다(주중, 주말 상관없음) 청구서를 발행할 **기간 일 수** 를 선택하거나 **기간 일 수(평일)** 을 선택하여 해당 기간 내 정해진 주중 날짜에 맞춰 청구서를 발행합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-110">If you specified a period of monthly or biweekly, in **Days of run**, select **Day of period** to invoice on the specified day of the period (whether weekday or weekend), or select **Weekday of period** to invoice on the specified weekday of the period.</span></span>  
  
6.  <span data-ttu-id="3e652-111">월간으로 기간을 지정한 경우, **매월 실행** 에서 청구서를 발행하려는 월간 회수를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-111">If you specified a period of monthly, in **Runs per month**, select the number of times per month you want to run the invoice.</span></span>  
  
7.  <span data-ttu-id="3e652-112">**송장 빈도 정보** 영역에, 필요에 따라 '일' 또는 '주중' 세부 내용을 변경하여 송장이 지정한 정확한 날 또는 평일에 발행되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-112">In the **Invoice Frequency Details** area, change the day or weekday details as necessary to make sure the invoice runs on the correct day or weekday of the period you specified.</span></span>  
  
8.  <span data-ttu-id="3e652-113">업을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3e652-113">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3e652-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e652-114">See Also</span></span>  
 [<span data-ttu-id="3e652-115">Project Service 구성</span><span class="sxs-lookup"><span data-stu-id="3e652-115">Configure Project Service</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]