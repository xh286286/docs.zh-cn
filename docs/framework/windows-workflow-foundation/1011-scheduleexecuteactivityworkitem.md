---
title: 1011 - ScheduleExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: e503ae46-ad6b-4fcb-8c0e-146d59a8eff1
ms.openlocfilehash: dc209fc41dc6b076dfb897880f753be51f7fb0ce
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239687"
---
# <a name="1011---scheduleexecuteactivityworkitem"></a><span data-ttu-id="9536b-102">1011 - ScheduleExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="9536b-102">1011 - ScheduleExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="9536b-103">属性</span><span class="sxs-lookup"><span data-stu-id="9536b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9536b-104">ID</span><span class="sxs-lookup"><span data-stu-id="9536b-104">ID</span></span>|<span data-ttu-id="9536b-105">1011</span><span class="sxs-lookup"><span data-stu-id="9536b-105">1011</span></span>|  
|<span data-ttu-id="9536b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9536b-106">Keywords</span></span>|<span data-ttu-id="9536b-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="9536b-107">WFRuntime</span></span>|  
|<span data-ttu-id="9536b-108">级别</span><span class="sxs-lookup"><span data-stu-id="9536b-108">Level</span></span>|<span data-ttu-id="9536b-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="9536b-109">Verbose</span></span>|  
|<span data-ttu-id="9536b-110">通道</span><span class="sxs-lookup"><span data-stu-id="9536b-110">Channel</span></span>|<span data-ttu-id="9536b-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="9536b-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9536b-112">描述</span><span class="sxs-lookup"><span data-stu-id="9536b-112">Description</span></span>  

 <span data-ttu-id="9536b-113">指示已安排 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9536b-113">Indicates an ExecuteActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9536b-114">消息</span><span class="sxs-lookup"><span data-stu-id="9536b-114">Message</span></span>  

 <span data-ttu-id="9536b-115">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9536b-115">An ExecuteActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9536b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="9536b-116">Details</span></span>  
  
|<span data-ttu-id="9536b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9536b-117">Data Item Name</span></span>|<span data-ttu-id="9536b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9536b-118">Data Item Type</span></span>|<span data-ttu-id="9536b-119">描述</span><span class="sxs-lookup"><span data-stu-id="9536b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9536b-120">活动</span><span class="sxs-lookup"><span data-stu-id="9536b-120">Activity</span></span>|<span data-ttu-id="9536b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="9536b-121">xs:string</span></span>|<span data-ttu-id="9536b-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="9536b-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="9536b-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="9536b-123">DisplayName</span></span>|<span data-ttu-id="9536b-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="9536b-124">xs:string</span></span>|<span data-ttu-id="9536b-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9536b-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="9536b-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="9536b-126">InstanceId</span></span>|<span data-ttu-id="9536b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="9536b-127">xs:string</span></span>|<span data-ttu-id="9536b-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="9536b-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="9536b-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9536b-129">AppDomain</span></span>|<span data-ttu-id="9536b-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="9536b-130">xs:string</span></span>|<span data-ttu-id="9536b-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9536b-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
