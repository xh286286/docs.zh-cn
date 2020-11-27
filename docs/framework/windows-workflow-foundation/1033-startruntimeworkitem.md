---
title: 1033 - StartRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 172b5346-9f3b-46ae-bc06-39872022376a
ms.openlocfilehash: 46a3dc8d313ec72ac90abc2e2e333b274dad2e4c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294295"
---
# <a name="1033---startruntimeworkitem"></a><span data-ttu-id="fe474-102">1033 - StartRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="fe474-102">1033 - StartRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="fe474-103">属性</span><span class="sxs-lookup"><span data-stu-id="fe474-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fe474-104">ID</span><span class="sxs-lookup"><span data-stu-id="fe474-104">ID</span></span>|<span data-ttu-id="fe474-105">2052</span><span class="sxs-lookup"><span data-stu-id="fe474-105">1033</span></span>|  
|<span data-ttu-id="fe474-106">关键字</span><span class="sxs-lookup"><span data-stu-id="fe474-106">Keywords</span></span>|<span data-ttu-id="fe474-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fe474-107">WFRuntime</span></span>|  
|<span data-ttu-id="fe474-108">级别</span><span class="sxs-lookup"><span data-stu-id="fe474-108">Level</span></span>|<span data-ttu-id="fe474-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="fe474-109">Verbose</span></span>|  
|<span data-ttu-id="fe474-110">通道</span><span class="sxs-lookup"><span data-stu-id="fe474-110">Channel</span></span>|<span data-ttu-id="fe474-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="fe474-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fe474-112">描述</span><span class="sxs-lookup"><span data-stu-id="fe474-112">Description</span></span>  

 <span data-ttu-id="fe474-113">指示 RuntimeWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="fe474-113">Indicates a RuntimeWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fe474-114">消息</span><span class="sxs-lookup"><span data-stu-id="fe474-114">Message</span></span>  

 <span data-ttu-id="fe474-115">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行运行时工作项。</span><span class="sxs-lookup"><span data-stu-id="fe474-115">Starting execution of a runtime work item for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fe474-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="fe474-116">Details</span></span>  
  
|<span data-ttu-id="fe474-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fe474-117">Data Item Name</span></span>|<span data-ttu-id="fe474-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fe474-118">Data Item Type</span></span>|<span data-ttu-id="fe474-119">描述</span><span class="sxs-lookup"><span data-stu-id="fe474-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fe474-120">活动</span><span class="sxs-lookup"><span data-stu-id="fe474-120">Activity</span></span>|<span data-ttu-id="fe474-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe474-121">xs:string</span></span>|<span data-ttu-id="fe474-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="fe474-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="fe474-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe474-123">DisplayName</span></span>|<span data-ttu-id="fe474-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe474-124">xs:string</span></span>|<span data-ttu-id="fe474-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="fe474-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="fe474-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="fe474-126">InstanceId</span></span>|<span data-ttu-id="fe474-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe474-127">xs:string</span></span>|<span data-ttu-id="fe474-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="fe474-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="fe474-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fe474-129">AppDomain</span></span>|<span data-ttu-id="fe474-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe474-130">xs:string</span></span>|<span data-ttu-id="fe474-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fe474-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
