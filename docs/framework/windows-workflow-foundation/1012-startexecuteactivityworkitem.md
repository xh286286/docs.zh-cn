---
title: 1012 - StartExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 29e9b1c6-c5d7-4b58-b59d-a06a923d3c80
ms.openlocfilehash: b9cfceb12d56f93c0f9726849e34f4333f1399ac
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239635"
---
# <a name="1012---startexecuteactivityworkitem"></a><span data-ttu-id="59b3b-102">1012 - StartExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="59b3b-102">1012 - StartExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="59b3b-103">属性</span><span class="sxs-lookup"><span data-stu-id="59b3b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="59b3b-104">ID</span><span class="sxs-lookup"><span data-stu-id="59b3b-104">ID</span></span>|<span data-ttu-id="59b3b-105">1012</span><span class="sxs-lookup"><span data-stu-id="59b3b-105">1012</span></span>|  
|<span data-ttu-id="59b3b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="59b3b-106">Keywords</span></span>|<span data-ttu-id="59b3b-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="59b3b-107">WFRuntime</span></span>|  
|<span data-ttu-id="59b3b-108">级别</span><span class="sxs-lookup"><span data-stu-id="59b3b-108">Level</span></span>|<span data-ttu-id="59b3b-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="59b3b-109">Verbose</span></span>|  
|<span data-ttu-id="59b3b-110">通道</span><span class="sxs-lookup"><span data-stu-id="59b3b-110">Channel</span></span>|<span data-ttu-id="59b3b-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="59b3b-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="59b3b-112">描述</span><span class="sxs-lookup"><span data-stu-id="59b3b-112">Description</span></span>  

 <span data-ttu-id="59b3b-113">指示 ExecuteActivityWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="59b3b-113">Indicates an ExecuteActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="59b3b-114">消息</span><span class="sxs-lookup"><span data-stu-id="59b3b-114">Message</span></span>  

 <span data-ttu-id="59b3b-115">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="59b3b-115">Starting execution of an ExecuteActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="59b3b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="59b3b-116">Details</span></span>  
  
|<span data-ttu-id="59b3b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="59b3b-117">Data Item Name</span></span>|<span data-ttu-id="59b3b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="59b3b-118">Data Item Type</span></span>|<span data-ttu-id="59b3b-119">描述</span><span class="sxs-lookup"><span data-stu-id="59b3b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="59b3b-120">活动</span><span class="sxs-lookup"><span data-stu-id="59b3b-120">Activity</span></span>|<span data-ttu-id="59b3b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="59b3b-121">xs:string</span></span>|<span data-ttu-id="59b3b-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="59b3b-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="59b3b-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="59b3b-123">DisplayName</span></span>|<span data-ttu-id="59b3b-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="59b3b-124">xs:string</span></span>|<span data-ttu-id="59b3b-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="59b3b-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="59b3b-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="59b3b-126">InstanceId</span></span>|<span data-ttu-id="59b3b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="59b3b-127">xs:string</span></span>|<span data-ttu-id="59b3b-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="59b3b-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="59b3b-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="59b3b-129">AppDomain</span></span>|<span data-ttu-id="59b3b-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="59b3b-130">xs:string</span></span>|<span data-ttu-id="59b3b-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="59b3b-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
