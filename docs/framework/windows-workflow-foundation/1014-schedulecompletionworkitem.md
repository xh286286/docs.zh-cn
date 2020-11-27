---
title: 1014 - ScheduleCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 84203735-478d-42d8-a320-c175dbddcb38
ms.openlocfilehash: 7fd93683851c5a8c4ab253272c3f2129b3f0bb49
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275552"
---
# <a name="1014---schedulecompletionworkitem"></a><span data-ttu-id="41588-102">1014 - ScheduleCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="41588-102">1014 - ScheduleCompletionWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="41588-103">属性</span><span class="sxs-lookup"><span data-stu-id="41588-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="41588-104">ID</span><span class="sxs-lookup"><span data-stu-id="41588-104">ID</span></span>|<span data-ttu-id="41588-105">1014</span><span class="sxs-lookup"><span data-stu-id="41588-105">1014</span></span>|  
|<span data-ttu-id="41588-106">关键字</span><span class="sxs-lookup"><span data-stu-id="41588-106">Keywords</span></span>|<span data-ttu-id="41588-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="41588-107">WFRuntime</span></span>|  
|<span data-ttu-id="41588-108">级别</span><span class="sxs-lookup"><span data-stu-id="41588-108">Level</span></span>|<span data-ttu-id="41588-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="41588-109">Verbose</span></span>|  
|<span data-ttu-id="41588-110">通道</span><span class="sxs-lookup"><span data-stu-id="41588-110">Channel</span></span>|<span data-ttu-id="41588-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="41588-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="41588-112">描述</span><span class="sxs-lookup"><span data-stu-id="41588-112">Description</span></span>  

 <span data-ttu-id="41588-113">指示已安排 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="41588-113">Indicates a CompletionWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="41588-114">消息</span><span class="sxs-lookup"><span data-stu-id="41588-114">Message</span></span>  

 <span data-ttu-id="41588-115">已为父 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="41588-115">A CompletionWorkItem has been scheduled for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="41588-116">已完成的活动“%4”、DisplayName：“%5”、InstanceId：“%6”。</span><span class="sxs-lookup"><span data-stu-id="41588-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="41588-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="41588-117">Details</span></span>  
  
|<span data-ttu-id="41588-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="41588-118">Data Item Name</span></span>|<span data-ttu-id="41588-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="41588-119">Data Item Type</span></span>|<span data-ttu-id="41588-120">描述</span><span class="sxs-lookup"><span data-stu-id="41588-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="41588-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="41588-121">ParentActivity</span></span>|<span data-ttu-id="41588-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-122">xs:string</span></span>|<span data-ttu-id="41588-123">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="41588-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="41588-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="41588-124">ParentDisplayName</span></span>|<span data-ttu-id="41588-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-125">xs:string</span></span>|<span data-ttu-id="41588-126">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="41588-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="41588-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="41588-127">ParentInstanceId</span></span>|<span data-ttu-id="41588-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-128">xs:string</span></span>|<span data-ttu-id="41588-129">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="41588-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="41588-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="41588-130">CompletedActivity</span></span>|<span data-ttu-id="41588-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-131">xs:string</span></span>|<span data-ttu-id="41588-132">已完成活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="41588-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="41588-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="41588-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="41588-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-134">xs:string</span></span>|<span data-ttu-id="41588-135">已完成活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="41588-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="41588-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="41588-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="41588-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-137">xs:string</span></span>|<span data-ttu-id="41588-138">已完成活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="41588-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="41588-139">应用程序域</span><span class="sxs-lookup"><span data-stu-id="41588-139">AppDomain</span></span>|<span data-ttu-id="41588-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="41588-140">xs:string</span></span>|<span data-ttu-id="41588-141">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="41588-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
