---
title: 1022 - StartBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 4415fbdb-0329-4019-803f-aea66e75f3da
ms.openlocfilehash: ca1f4244fb1a5144cb2d86eaacb9b31137d317c2
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275331"
---
# <a name="1022---startbookmarkworkitem"></a><span data-ttu-id="d1992-102">1022 - StartBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="d1992-102">1022 - StartBookmarkWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="d1992-103">属性</span><span class="sxs-lookup"><span data-stu-id="d1992-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d1992-104">ID</span><span class="sxs-lookup"><span data-stu-id="d1992-104">ID</span></span>|<span data-ttu-id="d1992-105">1022</span><span class="sxs-lookup"><span data-stu-id="d1992-105">1022</span></span>|  
|<span data-ttu-id="d1992-106">关键字</span><span class="sxs-lookup"><span data-stu-id="d1992-106">Keywords</span></span>|<span data-ttu-id="d1992-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="d1992-107">WFRuntime</span></span>|  
|<span data-ttu-id="d1992-108">级别</span><span class="sxs-lookup"><span data-stu-id="d1992-108">Level</span></span>|<span data-ttu-id="d1992-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="d1992-109">Verbose</span></span>|  
|<span data-ttu-id="d1992-110">通道</span><span class="sxs-lookup"><span data-stu-id="d1992-110">Channel</span></span>|<span data-ttu-id="d1992-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="d1992-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d1992-112">描述</span><span class="sxs-lookup"><span data-stu-id="d1992-112">Description</span></span>  

 <span data-ttu-id="d1992-113">指示 BookmarkWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="d1992-113">Indicates a BookmarkWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d1992-114">消息</span><span class="sxs-lookup"><span data-stu-id="d1992-114">Message</span></span>  

 <span data-ttu-id="d1992-115">开始为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 执行 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="d1992-115">Starting execution of a BookmarkWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="d1992-116">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="d1992-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d1992-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="d1992-117">Details</span></span>  
  
|<span data-ttu-id="d1992-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d1992-118">Data Item Name</span></span>|<span data-ttu-id="d1992-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d1992-119">Data Item Type</span></span>|<span data-ttu-id="d1992-120">描述</span><span class="sxs-lookup"><span data-stu-id="d1992-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d1992-121">活动</span><span class="sxs-lookup"><span data-stu-id="d1992-121">Activity</span></span>|<span data-ttu-id="d1992-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-122">xs:string</span></span>|<span data-ttu-id="d1992-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="d1992-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="d1992-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d1992-124">DisplayName</span></span>|<span data-ttu-id="d1992-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-125">xs:string</span></span>|<span data-ttu-id="d1992-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d1992-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="d1992-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="d1992-127">InstanceId</span></span>|<span data-ttu-id="d1992-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-128">xs:string</span></span>|<span data-ttu-id="d1992-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="d1992-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="d1992-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="d1992-130">BookmarkName</span></span>|<span data-ttu-id="d1992-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-131">xs:string</span></span>|<span data-ttu-id="d1992-132">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="d1992-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="d1992-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="d1992-133">BookmarkScope</span></span>|<span data-ttu-id="d1992-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-134">xs:string</span></span>|<span data-ttu-id="d1992-135">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="d1992-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="d1992-136">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d1992-136">AppDomain</span></span>|<span data-ttu-id="d1992-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1992-137">xs:string</span></span>|<span data-ttu-id="d1992-138">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1992-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
