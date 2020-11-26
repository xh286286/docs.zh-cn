---
title: 1013 - CompleteExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 31fc57b3-ef2f-48f0-a5de-b4e2c5c9ded7
ms.openlocfilehash: 654f961088c371ab53e4a81f40e3c63335efb1a8
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239583"
---
# <a name="1013---completeexecuteactivityworkitem"></a><span data-ttu-id="6b0da-102">1013 - CompleteExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="6b0da-102">1013 - CompleteExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="6b0da-103">属性</span><span class="sxs-lookup"><span data-stu-id="6b0da-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6b0da-104">ID</span><span class="sxs-lookup"><span data-stu-id="6b0da-104">ID</span></span>|<span data-ttu-id="6b0da-105">1013</span><span class="sxs-lookup"><span data-stu-id="6b0da-105">1013</span></span>|  
|<span data-ttu-id="6b0da-106">关键字</span><span class="sxs-lookup"><span data-stu-id="6b0da-106">Keywords</span></span>|<span data-ttu-id="6b0da-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="6b0da-107">WFRuntime</span></span>|  
|<span data-ttu-id="6b0da-108">级别</span><span class="sxs-lookup"><span data-stu-id="6b0da-108">Level</span></span>|<span data-ttu-id="6b0da-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="6b0da-109">Verbose</span></span>|  
|<span data-ttu-id="6b0da-110">通道</span><span class="sxs-lookup"><span data-stu-id="6b0da-110">Channel</span></span>|<span data-ttu-id="6b0da-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="6b0da-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="6b0da-112">描述</span><span class="sxs-lookup"><span data-stu-id="6b0da-112">Description</span></span>  

 <span data-ttu-id="6b0da-113">指示 ExecuteActivityWorkItem 已完成</span><span class="sxs-lookup"><span data-stu-id="6b0da-113">Indicates an ExecuteActivityWorkItem has completed</span></span>  
  
## <a name="message"></a><span data-ttu-id="6b0da-114">消息</span><span class="sxs-lookup"><span data-stu-id="6b0da-114">Message</span></span>  

 <span data-ttu-id="6b0da-115">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 ExecuteActivityWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="6b0da-115">An ExecuteActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="6b0da-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="6b0da-116">Details</span></span>  
  
|<span data-ttu-id="6b0da-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="6b0da-117">Data Item Name</span></span>|<span data-ttu-id="6b0da-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="6b0da-118">Data Item Type</span></span>|<span data-ttu-id="6b0da-119">描述</span><span class="sxs-lookup"><span data-stu-id="6b0da-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="6b0da-120">活动</span><span class="sxs-lookup"><span data-stu-id="6b0da-120">Activity</span></span>|<span data-ttu-id="6b0da-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b0da-121">xs:string</span></span>|<span data-ttu-id="6b0da-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="6b0da-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="6b0da-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b0da-123">DisplayName</span></span>|<span data-ttu-id="6b0da-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b0da-124">xs:string</span></span>|<span data-ttu-id="6b0da-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="6b0da-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="6b0da-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="6b0da-126">InstanceId</span></span>|<span data-ttu-id="6b0da-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b0da-127">xs:string</span></span>|<span data-ttu-id="6b0da-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="6b0da-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="6b0da-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="6b0da-129">AppDomain</span></span>|<span data-ttu-id="6b0da-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b0da-130">xs:string</span></span>|<span data-ttu-id="6b0da-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="6b0da-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
