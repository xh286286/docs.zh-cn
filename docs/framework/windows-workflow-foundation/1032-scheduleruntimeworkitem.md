---
title: 1032 - ScheduleRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 54688101-becf-42f3-80ca-f53a7b527620
ms.openlocfilehash: da35201f2b3e3bc07e0b9139b0584ce37011e168
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294308"
---
# <a name="1032---scheduleruntimeworkitem"></a><span data-ttu-id="39d94-102">1032 - ScheduleRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="39d94-102">1032 - ScheduleRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="39d94-103">属性</span><span class="sxs-lookup"><span data-stu-id="39d94-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="39d94-104">ID</span><span class="sxs-lookup"><span data-stu-id="39d94-104">ID</span></span>|<span data-ttu-id="39d94-105">1032</span><span class="sxs-lookup"><span data-stu-id="39d94-105">1032</span></span>|  
|<span data-ttu-id="39d94-106">关键字</span><span class="sxs-lookup"><span data-stu-id="39d94-106">Keywords</span></span>|<span data-ttu-id="39d94-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="39d94-107">WFRuntime</span></span>|  
|<span data-ttu-id="39d94-108">级别</span><span class="sxs-lookup"><span data-stu-id="39d94-108">Level</span></span>|<span data-ttu-id="39d94-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="39d94-109">Verbose</span></span>|  
|<span data-ttu-id="39d94-110">通道</span><span class="sxs-lookup"><span data-stu-id="39d94-110">Channel</span></span>|<span data-ttu-id="39d94-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="39d94-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="39d94-112">描述</span><span class="sxs-lookup"><span data-stu-id="39d94-112">Description</span></span>  

 <span data-ttu-id="39d94-113">指示已安排 RuntimeWorkItem。</span><span class="sxs-lookup"><span data-stu-id="39d94-113">Indicates a RuntimeWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="39d94-114">消息</span><span class="sxs-lookup"><span data-stu-id="39d94-114">Message</span></span>  

 <span data-ttu-id="39d94-115">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了运行时工作项。</span><span class="sxs-lookup"><span data-stu-id="39d94-115">A runtime work item has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="39d94-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="39d94-116">Details</span></span>  
  
|<span data-ttu-id="39d94-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="39d94-117">Data Item Name</span></span>|<span data-ttu-id="39d94-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="39d94-118">Data Item Type</span></span>|<span data-ttu-id="39d94-119">描述</span><span class="sxs-lookup"><span data-stu-id="39d94-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="39d94-120">活动</span><span class="sxs-lookup"><span data-stu-id="39d94-120">Activity</span></span>|<span data-ttu-id="39d94-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="39d94-121">xs:string</span></span>|<span data-ttu-id="39d94-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="39d94-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="39d94-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="39d94-123">DisplayName</span></span>|<span data-ttu-id="39d94-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="39d94-124">xs:string</span></span>|<span data-ttu-id="39d94-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="39d94-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="39d94-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="39d94-126">InstanceId</span></span>|<span data-ttu-id="39d94-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="39d94-127">xs:string</span></span>|<span data-ttu-id="39d94-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="39d94-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="39d94-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="39d94-129">AppDomain</span></span>|<span data-ttu-id="39d94-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="39d94-130">xs:string</span></span>|<span data-ttu-id="39d94-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="39d94-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
