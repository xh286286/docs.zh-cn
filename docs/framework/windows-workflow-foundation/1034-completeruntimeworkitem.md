---
title: 1034 - CompleteRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 45620011-8b04-4f87-ab5a-65b24145e17d
ms.openlocfilehash: 837adc9e143060284f2373a049bc9ad9c8cee336
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294282"
---
# <a name="1034---completeruntimeworkitem"></a><span data-ttu-id="7d0fe-102">1034 - CompleteRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="7d0fe-102">1034 - CompleteRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="7d0fe-103">属性</span><span class="sxs-lookup"><span data-stu-id="7d0fe-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7d0fe-104">ID</span><span class="sxs-lookup"><span data-stu-id="7d0fe-104">ID</span></span>|<span data-ttu-id="7d0fe-105">1034</span><span class="sxs-lookup"><span data-stu-id="7d0fe-105">1034</span></span>|  
|<span data-ttu-id="7d0fe-106">关键字</span><span class="sxs-lookup"><span data-stu-id="7d0fe-106">Keywords</span></span>|<span data-ttu-id="7d0fe-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7d0fe-107">WFRuntime</span></span>|  
|<span data-ttu-id="7d0fe-108">级别</span><span class="sxs-lookup"><span data-stu-id="7d0fe-108">Level</span></span>|<span data-ttu-id="7d0fe-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="7d0fe-109">Verbose</span></span>|  
|<span data-ttu-id="7d0fe-110">通道</span><span class="sxs-lookup"><span data-stu-id="7d0fe-110">Channel</span></span>|<span data-ttu-id="7d0fe-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="7d0fe-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7d0fe-112">描述</span><span class="sxs-lookup"><span data-stu-id="7d0fe-112">Description</span></span>  

 <span data-ttu-id="7d0fe-113">指示 RuntimeWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-113">Indicates a RuntimeWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7d0fe-114">消息</span><span class="sxs-lookup"><span data-stu-id="7d0fe-114">Message</span></span>  

 <span data-ttu-id="7d0fe-115">Activity“%1”、DisplayName“%2”、InstanceId“%3”的运行时工作项已经完成。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-115">A runtime work item has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7d0fe-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="7d0fe-116">Details</span></span>  
  
|<span data-ttu-id="7d0fe-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7d0fe-117">Data Item Name</span></span>|<span data-ttu-id="7d0fe-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7d0fe-118">Data Item Type</span></span>|<span data-ttu-id="7d0fe-119">描述</span><span class="sxs-lookup"><span data-stu-id="7d0fe-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7d0fe-120">活动</span><span class="sxs-lookup"><span data-stu-id="7d0fe-120">Activity</span></span>|<span data-ttu-id="7d0fe-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d0fe-121">xs:string</span></span>|<span data-ttu-id="7d0fe-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="7d0fe-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d0fe-123">DisplayName</span></span>|<span data-ttu-id="7d0fe-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d0fe-124">xs:string</span></span>|<span data-ttu-id="7d0fe-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="7d0fe-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="7d0fe-126">InstanceId</span></span>|<span data-ttu-id="7d0fe-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d0fe-127">xs:string</span></span>|<span data-ttu-id="7d0fe-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="7d0fe-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7d0fe-129">AppDomain</span></span>|<span data-ttu-id="7d0fe-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d0fe-130">xs:string</span></span>|<span data-ttu-id="7d0fe-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7d0fe-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
