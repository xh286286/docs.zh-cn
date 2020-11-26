---
title: 1009 - ActivityScheduled
ms.date: 03/30/2017
ms.assetid: 307e38b6-d47e-47a4-9708-e74d8314b1a1
ms.openlocfilehash: 812531d4206dfee20f183b9461330e71263b0bf8
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239765"
---
# <a name="1009---activityscheduled"></a><span data-ttu-id="4beaa-102">1009 - ActivityScheduled</span><span class="sxs-lookup"><span data-stu-id="4beaa-102">1009 - ActivityScheduled</span></span>

## <a name="properties"></a><span data-ttu-id="4beaa-103">属性</span><span class="sxs-lookup"><span data-stu-id="4beaa-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4beaa-104">ID</span><span class="sxs-lookup"><span data-stu-id="4beaa-104">ID</span></span>|<span data-ttu-id="4beaa-105">1009</span><span class="sxs-lookup"><span data-stu-id="4beaa-105">1009</span></span>|  
|<span data-ttu-id="4beaa-106">关键字</span><span class="sxs-lookup"><span data-stu-id="4beaa-106">Keywords</span></span>|<span data-ttu-id="4beaa-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="4beaa-107">WFRuntime</span></span>|  
|<span data-ttu-id="4beaa-108">Level</span><span class="sxs-lookup"><span data-stu-id="4beaa-108">Level</span></span>|<span data-ttu-id="4beaa-109">信息</span><span class="sxs-lookup"><span data-stu-id="4beaa-109">Information</span></span>|  
|<span data-ttu-id="4beaa-110">通道</span><span class="sxs-lookup"><span data-stu-id="4beaa-110">Channel</span></span>|<span data-ttu-id="4beaa-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="4beaa-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4beaa-112">描述</span><span class="sxs-lookup"><span data-stu-id="4beaa-112">Description</span></span>  

 <span data-ttu-id="4beaa-113">指示正在安排某一活动的执行。</span><span class="sxs-lookup"><span data-stu-id="4beaa-113">Indicates an activity is being scheduled for execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4beaa-114">消息</span><span class="sxs-lookup"><span data-stu-id="4beaa-114">Message</span></span>  

 <span data-ttu-id="4beaa-115">父 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了子 Activity“%4”、DisplayName“%5”、InstanceId“%6”。</span><span class="sxs-lookup"><span data-stu-id="4beaa-115">Parent Activity '%1', DisplayName: '%2', InstanceId: '%3' scheduled child Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4beaa-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="4beaa-116">Details</span></span>  
  
|<span data-ttu-id="4beaa-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="4beaa-117">Data Item Name</span></span>|<span data-ttu-id="4beaa-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="4beaa-118">Data Item Type</span></span>|<span data-ttu-id="4beaa-119">描述</span><span class="sxs-lookup"><span data-stu-id="4beaa-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4beaa-120">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="4beaa-120">ParentActivity</span></span>|<span data-ttu-id="4beaa-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-121">xs:string</span></span>|<span data-ttu-id="4beaa-122">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4beaa-122">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="4beaa-123">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="4beaa-123">ParentDisplayName</span></span>|<span data-ttu-id="4beaa-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-124">xs:string</span></span>|<span data-ttu-id="4beaa-125">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4beaa-125">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="4beaa-126">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="4beaa-126">ParentInstanceId</span></span>|<span data-ttu-id="4beaa-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-127">xs:string</span></span>|<span data-ttu-id="4beaa-128">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="4beaa-128">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="4beaa-129">ChildActivity</span><span class="sxs-lookup"><span data-stu-id="4beaa-129">ChildActivity</span></span>|<span data-ttu-id="4beaa-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-130">xs:string</span></span>|<span data-ttu-id="4beaa-131">所安排子活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4beaa-131">The type name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="4beaa-132">ChildDisplayName</span><span class="sxs-lookup"><span data-stu-id="4beaa-132">ChildDisplayName</span></span>|<span data-ttu-id="4beaa-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-133">xs:string</span></span>|<span data-ttu-id="4beaa-134">所安排子活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4beaa-134">The display name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="4beaa-135">ChildInstanceId</span><span class="sxs-lookup"><span data-stu-id="4beaa-135">ChildInstanceId</span></span>|<span data-ttu-id="4beaa-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-136">xs:string</span></span>|<span data-ttu-id="4beaa-137">所安排子活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="4beaa-137">The instance id of the scheduled child activity.</span></span>|  
|<span data-ttu-id="4beaa-138">应用程序域</span><span class="sxs-lookup"><span data-stu-id="4beaa-138">AppDomain</span></span>|<span data-ttu-id="4beaa-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="4beaa-139">xs:string</span></span>|<span data-ttu-id="4beaa-140">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="4beaa-140">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
