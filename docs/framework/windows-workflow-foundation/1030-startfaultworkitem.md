---
title: 1030 - StartFaultWorkItem
ms.date: 03/30/2017
ms.assetid: e1601fb9-0bc6-4dbe-816f-f24914063d34
ms.openlocfilehash: 52034f7cc7c6f6749fbbbf06db9267ecb6279ee1
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96281854"
---
# <a name="1030---startfaultworkitem"></a><span data-ttu-id="89121-102">1030 - StartFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="89121-102">1030 - StartFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="89121-103">属性</span><span class="sxs-lookup"><span data-stu-id="89121-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="89121-104">ID</span><span class="sxs-lookup"><span data-stu-id="89121-104">ID</span></span>|<span data-ttu-id="89121-105">1030</span><span class="sxs-lookup"><span data-stu-id="89121-105">1030</span></span>|  
|<span data-ttu-id="89121-106">关键字</span><span class="sxs-lookup"><span data-stu-id="89121-106">Keywords</span></span>|<span data-ttu-id="89121-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="89121-107">WFRuntime</span></span>|  
|<span data-ttu-id="89121-108">级别</span><span class="sxs-lookup"><span data-stu-id="89121-108">Level</span></span>|<span data-ttu-id="89121-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="89121-109">Verbose</span></span>|  
|<span data-ttu-id="89121-110">通道</span><span class="sxs-lookup"><span data-stu-id="89121-110">Channel</span></span>|<span data-ttu-id="89121-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="89121-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="89121-112">描述</span><span class="sxs-lookup"><span data-stu-id="89121-112">Description</span></span>  

 <span data-ttu-id="89121-113">指示 FaultWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="89121-113">Indicates a FaultWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="89121-114">消息</span><span class="sxs-lookup"><span data-stu-id="89121-114">Message</span></span>  

 <span data-ttu-id="89121-115">开始为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 执行 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="89121-115">Starting execution of a FaultWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="89121-116">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="89121-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="89121-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="89121-117">Details</span></span>  
  
|<span data-ttu-id="89121-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="89121-118">Data Item Name</span></span>|<span data-ttu-id="89121-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="89121-119">Data Item Type</span></span>|<span data-ttu-id="89121-120">描述</span><span class="sxs-lookup"><span data-stu-id="89121-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="89121-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="89121-121">FaultActivity</span></span>|<span data-ttu-id="89121-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-122">xs:string</span></span>|<span data-ttu-id="89121-123">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="89121-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="89121-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="89121-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="89121-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-125">xs:string</span></span>|<span data-ttu-id="89121-126">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="89121-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="89121-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="89121-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="89121-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-128">xs:string</span></span>|<span data-ttu-id="89121-129">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="89121-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="89121-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="89121-130">ExceptionActivity</span></span>|<span data-ttu-id="89121-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-131">xs:string</span></span>|<span data-ttu-id="89121-132">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="89121-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="89121-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="89121-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="89121-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-134">xs:string</span></span>|<span data-ttu-id="89121-135">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="89121-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="89121-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="89121-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="89121-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-137">xs:string</span></span>|<span data-ttu-id="89121-138">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="89121-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="89121-139">异常</span><span class="sxs-lookup"><span data-stu-id="89121-139">Exception</span></span>|<span data-ttu-id="89121-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-140">xs:string</span></span>|<span data-ttu-id="89121-141">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="89121-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="89121-142">应用程序域</span><span class="sxs-lookup"><span data-stu-id="89121-142">AppDomain</span></span>|<span data-ttu-id="89121-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="89121-143">xs:string</span></span>|<span data-ttu-id="89121-144">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="89121-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
