---
title: 1020 - CreateBookmark
ms.date: 03/30/2017
ms.assetid: 4bee948d-816f-4803-85cc-3883b5e23d10
ms.openlocfilehash: 8c9c20fd4fb74f80779c1d2ef8f29ac3d44050d9
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275370"
---
# <a name="1020---createbookmark"></a><span data-ttu-id="0c724-102">1020 - CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="0c724-102">1020 - CreateBookmark</span></span>

## <a name="properties"></a><span data-ttu-id="0c724-103">属性</span><span class="sxs-lookup"><span data-stu-id="0c724-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0c724-104">ID</span><span class="sxs-lookup"><span data-stu-id="0c724-104">ID</span></span>|<span data-ttu-id="0c724-105">1020</span><span class="sxs-lookup"><span data-stu-id="0c724-105">1020</span></span>|  
|<span data-ttu-id="0c724-106">关键字</span><span class="sxs-lookup"><span data-stu-id="0c724-106">Keywords</span></span>|<span data-ttu-id="0c724-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0c724-107">WFRuntime</span></span>|  
|<span data-ttu-id="0c724-108">级别</span><span class="sxs-lookup"><span data-stu-id="0c724-108">Level</span></span>|<span data-ttu-id="0c724-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="0c724-109">Verbose</span></span>|  
|<span data-ttu-id="0c724-110">通道</span><span class="sxs-lookup"><span data-stu-id="0c724-110">Channel</span></span>|<span data-ttu-id="0c724-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0c724-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0c724-112">描述</span><span class="sxs-lookup"><span data-stu-id="0c724-112">Description</span></span>  

 <span data-ttu-id="0c724-113">指示已为活动创建了书签。</span><span class="sxs-lookup"><span data-stu-id="0c724-113">Indicates a bookmark has been created for an activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0c724-114">消息</span><span class="sxs-lookup"><span data-stu-id="0c724-114">Message</span></span>  

 <span data-ttu-id="0c724-115">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 创建了书签。</span><span class="sxs-lookup"><span data-stu-id="0c724-115">A Bookmark has been created for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="0c724-116">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="0c724-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0c724-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0c724-117">Details</span></span>  
  
|<span data-ttu-id="0c724-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0c724-118">Data Item Name</span></span>|<span data-ttu-id="0c724-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0c724-119">Data Item Type</span></span>|<span data-ttu-id="0c724-120">描述</span><span class="sxs-lookup"><span data-stu-id="0c724-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0c724-121">活动</span><span class="sxs-lookup"><span data-stu-id="0c724-121">Activity</span></span>|<span data-ttu-id="0c724-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-122">xs:string</span></span>|<span data-ttu-id="0c724-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="0c724-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="0c724-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c724-124">DisplayName</span></span>|<span data-ttu-id="0c724-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-125">xs:string</span></span>|<span data-ttu-id="0c724-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="0c724-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="0c724-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="0c724-127">InstanceId</span></span>|<span data-ttu-id="0c724-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-128">xs:string</span></span>|<span data-ttu-id="0c724-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="0c724-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="0c724-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="0c724-130">BookmarkName</span></span>|<span data-ttu-id="0c724-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-131">xs:string</span></span>|<span data-ttu-id="0c724-132">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="0c724-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="0c724-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="0c724-133">BookmarkScope</span></span>|<span data-ttu-id="0c724-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-134">xs:string</span></span>|<span data-ttu-id="0c724-135">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="0c724-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="0c724-136">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0c724-136">AppDomain</span></span>|<span data-ttu-id="0c724-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c724-137">xs:string</span></span>|<span data-ttu-id="0c724-138">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0c724-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
