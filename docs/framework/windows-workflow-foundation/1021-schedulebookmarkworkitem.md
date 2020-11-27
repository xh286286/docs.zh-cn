---
title: 1021 - ScheduleBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 2e0da311-b219-4637-9460-90cdafcc4ecd
ms.openlocfilehash: 42ed23654622e29df8ffc210c8d5ba572fa69fd4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275344"
---
# <a name="1021---schedulebookmarkworkitem"></a><span data-ttu-id="6bdd8-102">1021 - ScheduleBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="6bdd8-102">1021 - ScheduleBookmarkWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="6bdd8-103">属性</span><span class="sxs-lookup"><span data-stu-id="6bdd8-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6bdd8-104">ID</span><span class="sxs-lookup"><span data-stu-id="6bdd8-104">ID</span></span>|<span data-ttu-id="6bdd8-105">1021</span><span class="sxs-lookup"><span data-stu-id="6bdd8-105">1021</span></span>|  
|<span data-ttu-id="6bdd8-106">关键字</span><span class="sxs-lookup"><span data-stu-id="6bdd8-106">Keywords</span></span>|<span data-ttu-id="6bdd8-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="6bdd8-107">WFRuntime</span></span>|  
|<span data-ttu-id="6bdd8-108">级别</span><span class="sxs-lookup"><span data-stu-id="6bdd8-108">Level</span></span>|<span data-ttu-id="6bdd8-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="6bdd8-109">Verbose</span></span>|  
|<span data-ttu-id="6bdd8-110">通道</span><span class="sxs-lookup"><span data-stu-id="6bdd8-110">Channel</span></span>|<span data-ttu-id="6bdd8-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="6bdd8-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="6bdd8-112">描述</span><span class="sxs-lookup"><span data-stu-id="6bdd8-112">Description</span></span>  

 <span data-ttu-id="6bdd8-113">指示已安排 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-113">Indicates a BookmarkWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="6bdd8-114">消息</span><span class="sxs-lookup"><span data-stu-id="6bdd8-114">Message</span></span>  

 <span data-ttu-id="6bdd8-115">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-115">A BookmarkWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="6bdd8-116">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="6bdd8-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="6bdd8-117">Details</span></span>  
  
|<span data-ttu-id="6bdd8-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="6bdd8-118">Data Item Name</span></span>|<span data-ttu-id="6bdd8-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="6bdd8-119">Data Item Type</span></span>|<span data-ttu-id="6bdd8-120">描述</span><span class="sxs-lookup"><span data-stu-id="6bdd8-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="6bdd8-121">活动</span><span class="sxs-lookup"><span data-stu-id="6bdd8-121">Activity</span></span>|<span data-ttu-id="6bdd8-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-122">xs:string</span></span>|<span data-ttu-id="6bdd8-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="6bdd8-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="6bdd8-124">DisplayName</span></span>|<span data-ttu-id="6bdd8-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-125">xs:string</span></span>|<span data-ttu-id="6bdd8-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="6bdd8-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="6bdd8-127">InstanceId</span></span>|<span data-ttu-id="6bdd8-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-128">xs:string</span></span>|<span data-ttu-id="6bdd8-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="6bdd8-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="6bdd8-130">BookmarkName</span></span>|<span data-ttu-id="6bdd8-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-131">xs:string</span></span>|<span data-ttu-id="6bdd8-132">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="6bdd8-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="6bdd8-133">BookmarkScope</span></span>|<span data-ttu-id="6bdd8-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-134">xs:string</span></span>|<span data-ttu-id="6bdd8-135">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="6bdd8-136">应用程序域</span><span class="sxs-lookup"><span data-stu-id="6bdd8-136">AppDomain</span></span>|<span data-ttu-id="6bdd8-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="6bdd8-137">xs:string</span></span>|<span data-ttu-id="6bdd8-138">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="6bdd8-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
