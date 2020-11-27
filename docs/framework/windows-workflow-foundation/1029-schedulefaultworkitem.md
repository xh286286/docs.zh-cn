---
title: 1029 - ScheduleFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 3a56b29e-f740-459d-8576-d81e58bf5a03
ms.openlocfilehash: 5c109607b2d353d3d4a5a693f29ab66bb76c8398
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275084"
---
# <a name="1029---schedulefaultworkitem"></a><span data-ttu-id="9ff87-102">1029 - ScheduleFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="9ff87-102">1029 - ScheduleFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="9ff87-103">属性</span><span class="sxs-lookup"><span data-stu-id="9ff87-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9ff87-104">ID</span><span class="sxs-lookup"><span data-stu-id="9ff87-104">ID</span></span>|<span data-ttu-id="9ff87-105">1029</span><span class="sxs-lookup"><span data-stu-id="9ff87-105">1029</span></span>|  
|<span data-ttu-id="9ff87-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9ff87-106">Keywords</span></span>|<span data-ttu-id="9ff87-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="9ff87-107">WFRuntime</span></span>|  
|<span data-ttu-id="9ff87-108">级别</span><span class="sxs-lookup"><span data-stu-id="9ff87-108">Level</span></span>|<span data-ttu-id="9ff87-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="9ff87-109">Verbose</span></span>|  
|<span data-ttu-id="9ff87-110">通道</span><span class="sxs-lookup"><span data-stu-id="9ff87-110">Channel</span></span>|<span data-ttu-id="9ff87-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="9ff87-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9ff87-112">描述</span><span class="sxs-lookup"><span data-stu-id="9ff87-112">Description</span></span>  

 <span data-ttu-id="9ff87-113">指示已安排 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9ff87-113">Indicates a FaultWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9ff87-114">消息</span><span class="sxs-lookup"><span data-stu-id="9ff87-114">Message</span></span>  

 <span data-ttu-id="9ff87-115">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9ff87-115">A FaultWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="9ff87-116">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="9ff87-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9ff87-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="9ff87-117">Details</span></span>  
  
|<span data-ttu-id="9ff87-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9ff87-118">Data Item Name</span></span>|<span data-ttu-id="9ff87-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9ff87-119">Data Item Type</span></span>|<span data-ttu-id="9ff87-120">描述</span><span class="sxs-lookup"><span data-stu-id="9ff87-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9ff87-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="9ff87-121">FaultActivity</span></span>|<span data-ttu-id="9ff87-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-122">xs:string</span></span>|<span data-ttu-id="9ff87-123">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="9ff87-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="9ff87-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="9ff87-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="9ff87-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-125">xs:string</span></span>|<span data-ttu-id="9ff87-126">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9ff87-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="9ff87-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="9ff87-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="9ff87-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-128">xs:string</span></span>|<span data-ttu-id="9ff87-129">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="9ff87-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="9ff87-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="9ff87-130">ExceptionActivity</span></span>|<span data-ttu-id="9ff87-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-131">xs:string</span></span>|<span data-ttu-id="9ff87-132">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="9ff87-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="9ff87-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="9ff87-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="9ff87-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-134">xs:string</span></span>|<span data-ttu-id="9ff87-135">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9ff87-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="9ff87-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="9ff87-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="9ff87-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-137">xs:string</span></span>|<span data-ttu-id="9ff87-138">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="9ff87-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="9ff87-139">异常</span><span class="sxs-lookup"><span data-stu-id="9ff87-139">Exception</span></span>|<span data-ttu-id="9ff87-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-140">xs:string</span></span>|<span data-ttu-id="9ff87-141">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="9ff87-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="9ff87-142">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9ff87-142">AppDomain</span></span>|<span data-ttu-id="9ff87-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff87-143">xs:string</span></span>|<span data-ttu-id="9ff87-144">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9ff87-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
