---
title: 1031 - CompleteFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 95f4ccb0-6be4-41f3-9330-fae43165828f
ms.openlocfilehash: 557155fab35a37bdbaa45efb26d6bc025ad825c4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96281828"
---
# <a name="1031---completefaultworkitem"></a><span data-ttu-id="4f469-102">1031 - CompleteFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="4f469-102">1031 - CompleteFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="4f469-103">属性</span><span class="sxs-lookup"><span data-stu-id="4f469-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4f469-104">ID</span><span class="sxs-lookup"><span data-stu-id="4f469-104">ID</span></span>|<span data-ttu-id="4f469-105">1031</span><span class="sxs-lookup"><span data-stu-id="4f469-105">1031</span></span>|  
|<span data-ttu-id="4f469-106">关键字</span><span class="sxs-lookup"><span data-stu-id="4f469-106">Keywords</span></span>|<span data-ttu-id="4f469-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="4f469-107">WFRuntime</span></span>|  
|<span data-ttu-id="4f469-108">级别</span><span class="sxs-lookup"><span data-stu-id="4f469-108">Level</span></span>|<span data-ttu-id="4f469-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="4f469-109">Verbose</span></span>|  
|<span data-ttu-id="4f469-110">通道</span><span class="sxs-lookup"><span data-stu-id="4f469-110">Channel</span></span>|<span data-ttu-id="4f469-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="4f469-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4f469-112">描述</span><span class="sxs-lookup"><span data-stu-id="4f469-112">Description</span></span>  

 <span data-ttu-id="4f469-113">指示 FaultWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="4f469-113">Indicates a FaultWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4f469-114">消息</span><span class="sxs-lookup"><span data-stu-id="4f469-114">Message</span></span>  

 <span data-ttu-id="4f469-115">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 FaultWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="4f469-115">A FaultWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="4f469-116">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="4f469-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4f469-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="4f469-117">Details</span></span>  
  
|<span data-ttu-id="4f469-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="4f469-118">Data Item Name</span></span>|<span data-ttu-id="4f469-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="4f469-119">Data Item Type</span></span>|<span data-ttu-id="4f469-120">描述</span><span class="sxs-lookup"><span data-stu-id="4f469-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4f469-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="4f469-121">FaultActivity</span></span>|<span data-ttu-id="4f469-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-122">xs:string</span></span>|<span data-ttu-id="4f469-123">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4f469-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="4f469-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="4f469-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="4f469-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-125">xs:string</span></span>|<span data-ttu-id="4f469-126">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4f469-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="4f469-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="4f469-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="4f469-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-128">xs:string</span></span>|<span data-ttu-id="4f469-129">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="4f469-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="4f469-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="4f469-130">ExceptionActivity</span></span>|<span data-ttu-id="4f469-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-131">xs:string</span></span>|<span data-ttu-id="4f469-132">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4f469-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="4f469-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="4f469-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="4f469-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-134">xs:string</span></span>|<span data-ttu-id="4f469-135">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4f469-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="4f469-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="4f469-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="4f469-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-137">xs:string</span></span>|<span data-ttu-id="4f469-138">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="4f469-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="4f469-139">异常</span><span class="sxs-lookup"><span data-stu-id="4f469-139">Exception</span></span>|<span data-ttu-id="4f469-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-140">xs:string</span></span>|<span data-ttu-id="4f469-141">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="4f469-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="4f469-142">应用程序域</span><span class="sxs-lookup"><span data-stu-id="4f469-142">AppDomain</span></span>|<span data-ttu-id="4f469-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="4f469-143">xs:string</span></span>|<span data-ttu-id="4f469-144">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="4f469-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
