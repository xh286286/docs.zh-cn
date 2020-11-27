---
title: 1016 - CompleteCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 246929fb-6f14-440a-814b-cd8349350644
ms.openlocfilehash: a192ffe19777ca3e2e9784f6506a0c2929ced000
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275526"
---
# <a name="1016---completecompletionworkitem"></a><span data-ttu-id="3ff5d-102">1016 - CompleteCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="3ff5d-102">1016 - CompleteCompletionWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="3ff5d-103">属性</span><span class="sxs-lookup"><span data-stu-id="3ff5d-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3ff5d-104">ID</span><span class="sxs-lookup"><span data-stu-id="3ff5d-104">ID</span></span>|<span data-ttu-id="3ff5d-105">1016</span><span class="sxs-lookup"><span data-stu-id="3ff5d-105">1016</span></span>|  
|<span data-ttu-id="3ff5d-106">关键字</span><span class="sxs-lookup"><span data-stu-id="3ff5d-106">Keywords</span></span>|<span data-ttu-id="3ff5d-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="3ff5d-107">WFRuntime</span></span>|  
|<span data-ttu-id="3ff5d-108">级别</span><span class="sxs-lookup"><span data-stu-id="3ff5d-108">Level</span></span>|<span data-ttu-id="3ff5d-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="3ff5d-109">Verbose</span></span>|  
|<span data-ttu-id="3ff5d-110">通道</span><span class="sxs-lookup"><span data-stu-id="3ff5d-110">Channel</span></span>|<span data-ttu-id="3ff5d-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="3ff5d-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3ff5d-112">描述</span><span class="sxs-lookup"><span data-stu-id="3ff5d-112">Description</span></span>  

 <span data-ttu-id="3ff5d-113">指示 CompletionWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-113">Indicates a CompletionWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3ff5d-114">消息</span><span class="sxs-lookup"><span data-stu-id="3ff5d-114">Message</span></span>  

 <span data-ttu-id="3ff5d-115">父 Activity“%1”、DisplayName“'%2”、InstanceId“%3”已完成了 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-115">A CompletionWorkItem has completed for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="3ff5d-116">已完成的活动“%4”、DisplayName：“%5”、InstanceId：“%6”。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3ff5d-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="3ff5d-117">Details</span></span>  
  
|<span data-ttu-id="3ff5d-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3ff5d-118">Data Item Name</span></span>|<span data-ttu-id="3ff5d-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3ff5d-119">Data Item Type</span></span>|<span data-ttu-id="3ff5d-120">描述</span><span class="sxs-lookup"><span data-stu-id="3ff5d-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3ff5d-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="3ff5d-121">ParentActivity</span></span>|<span data-ttu-id="3ff5d-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-122">xs:string</span></span>|<span data-ttu-id="3ff5d-123">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="3ff5d-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="3ff5d-124">ParentDisplayName</span></span>|<span data-ttu-id="3ff5d-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-125">xs:string</span></span>|<span data-ttu-id="3ff5d-126">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="3ff5d-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="3ff5d-127">ParentInstanceId</span></span>|<span data-ttu-id="3ff5d-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-128">xs:string</span></span>|<span data-ttu-id="3ff5d-129">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="3ff5d-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="3ff5d-130">CompletedActivity</span></span>|<span data-ttu-id="3ff5d-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-131">xs:string</span></span>|<span data-ttu-id="3ff5d-132">已完成活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="3ff5d-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="3ff5d-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="3ff5d-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-134">xs:string</span></span>|<span data-ttu-id="3ff5d-135">已完成活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="3ff5d-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="3ff5d-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="3ff5d-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-137">xs:string</span></span>|<span data-ttu-id="3ff5d-138">已完成活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="3ff5d-139">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3ff5d-139">AppDomain</span></span>|<span data-ttu-id="3ff5d-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ff5d-140">xs:string</span></span>|<span data-ttu-id="3ff5d-141">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3ff5d-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
