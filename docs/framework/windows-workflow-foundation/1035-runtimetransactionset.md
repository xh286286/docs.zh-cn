---
title: 1035 - RuntimeTransactionSet
ms.date: 03/30/2017
ms.assetid: 03b37de9-778c-4beb-b0e3-de73ece6088e
ms.openlocfilehash: b8bf8431c4e2b82c6aac95820eb45de2a404e976
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294269"
---
# <a name="1035---runtimetransactionset"></a><span data-ttu-id="d83e8-102">1035 - RuntimeTransactionSet</span><span class="sxs-lookup"><span data-stu-id="d83e8-102">1035 - RuntimeTransactionSet</span></span>

## <a name="properties"></a><span data-ttu-id="d83e8-103">属性</span><span class="sxs-lookup"><span data-stu-id="d83e8-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d83e8-104">ID</span><span class="sxs-lookup"><span data-stu-id="d83e8-104">ID</span></span>|<span data-ttu-id="d83e8-105">1035</span><span class="sxs-lookup"><span data-stu-id="d83e8-105">1035</span></span>|  
|<span data-ttu-id="d83e8-106">关键字</span><span class="sxs-lookup"><span data-stu-id="d83e8-106">Keywords</span></span>|<span data-ttu-id="d83e8-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="d83e8-107">WFRuntime</span></span>|  
|<span data-ttu-id="d83e8-108">级别</span><span class="sxs-lookup"><span data-stu-id="d83e8-108">Level</span></span>|<span data-ttu-id="d83e8-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="d83e8-109">Verbose</span></span>|  
|<span data-ttu-id="d83e8-110">通道</span><span class="sxs-lookup"><span data-stu-id="d83e8-110">Channel</span></span>|<span data-ttu-id="d83e8-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="d83e8-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d83e8-112">描述</span><span class="sxs-lookup"><span data-stu-id="d83e8-112">Description</span></span>  

 <span data-ttu-id="d83e8-113">指示活动已设置为运行时事务。</span><span class="sxs-lookup"><span data-stu-id="d83e8-113">Indicates an activity has set the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d83e8-114">消息</span><span class="sxs-lookup"><span data-stu-id="d83e8-114">Message</span></span>  

 <span data-ttu-id="d83e8-115">运行时事务已由 Activity "%1"、DisplayName "%2"、InstanceId "%3" 设置。</span><span class="sxs-lookup"><span data-stu-id="d83e8-115">The runtime transaction has been set by Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="d83e8-116">执行操作与 Activity "%4"、DisplayName "%5"、InstanceId "%6" 隔离。</span><span class="sxs-lookup"><span data-stu-id="d83e8-116">Execution isolated to Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d83e8-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="d83e8-117">Details</span></span>  
  
|<span data-ttu-id="d83e8-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d83e8-118">Data Item Name</span></span>|<span data-ttu-id="d83e8-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d83e8-119">Data Item Type</span></span>|<span data-ttu-id="d83e8-120">描述</span><span class="sxs-lookup"><span data-stu-id="d83e8-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d83e8-121">活动</span><span class="sxs-lookup"><span data-stu-id="d83e8-121">Activity</span></span>|<span data-ttu-id="d83e8-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-122">xs:string</span></span>|<span data-ttu-id="d83e8-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="d83e8-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="d83e8-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d83e8-124">DisplayName</span></span>|<span data-ttu-id="d83e8-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-125">xs:string</span></span>|<span data-ttu-id="d83e8-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d83e8-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="d83e8-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="d83e8-127">InstanceId</span></span>|<span data-ttu-id="d83e8-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-128">xs:string</span></span>|<span data-ttu-id="d83e8-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="d83e8-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="d83e8-130">IsolatedActivity</span><span class="sxs-lookup"><span data-stu-id="d83e8-130">IsolatedActivity</span></span>|<span data-ttu-id="d83e8-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-131">xs:string</span></span>|<span data-ttu-id="d83e8-132">事务隔离到的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="d83e8-132">The type name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="d83e8-133">IsolatedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="d83e8-133">IsolatedActivityDisplayName</span></span>|<span data-ttu-id="d83e8-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-134">xs:string</span></span>|<span data-ttu-id="d83e8-135">事务隔离到的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d83e8-135">The display name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="d83e8-136">IsolatedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="d83e8-136">IsolatedActivityInstanceId</span></span>|<span data-ttu-id="d83e8-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-137">xs:string</span></span>|<span data-ttu-id="d83e8-138">事务隔离到的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="d83e8-138">The instance id of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="d83e8-139">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d83e8-139">AppDomain</span></span>|<span data-ttu-id="d83e8-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="d83e8-140">xs:string</span></span>|<span data-ttu-id="d83e8-141">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d83e8-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
