---
title: 1018 - StartCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 68b4fa1d-eee6-4a2a-8c16-7e9d89f08ab9
ms.openlocfilehash: c1558e19b0de2dc5d22d4356b0f80c35e5b4fbc1
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275500"
---
# <a name="1018---startcancelactivityworkitem"></a><span data-ttu-id="c7908-102">1018 - StartCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="c7908-102">1018 - StartCancelActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="c7908-103">属性</span><span class="sxs-lookup"><span data-stu-id="c7908-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c7908-104">ID</span><span class="sxs-lookup"><span data-stu-id="c7908-104">ID</span></span>|<span data-ttu-id="c7908-105">1018</span><span class="sxs-lookup"><span data-stu-id="c7908-105">1018</span></span>|  
|<span data-ttu-id="c7908-106">关键字</span><span class="sxs-lookup"><span data-stu-id="c7908-106">Keywords</span></span>|<span data-ttu-id="c7908-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="c7908-107">WFRuntime</span></span>|  
|<span data-ttu-id="c7908-108">级别</span><span class="sxs-lookup"><span data-stu-id="c7908-108">Level</span></span>|<span data-ttu-id="c7908-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="c7908-109">Verbose</span></span>|  
|<span data-ttu-id="c7908-110">通道</span><span class="sxs-lookup"><span data-stu-id="c7908-110">Channel</span></span>|<span data-ttu-id="c7908-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c7908-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c7908-112">描述</span><span class="sxs-lookup"><span data-stu-id="c7908-112">Description</span></span>  

 <span data-ttu-id="c7908-113">指示 CancelActivityWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="c7908-113">Indicates a CancelActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c7908-114">消息</span><span class="sxs-lookup"><span data-stu-id="c7908-114">Message</span></span>  

 <span data-ttu-id="c7908-115">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 CancelActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="c7908-115">Starting execution of a CancelActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c7908-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="c7908-116">Details</span></span>  
  
|<span data-ttu-id="c7908-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c7908-117">Data Item Name</span></span>|<span data-ttu-id="c7908-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c7908-118">Data Item Type</span></span>|<span data-ttu-id="c7908-119">描述</span><span class="sxs-lookup"><span data-stu-id="c7908-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c7908-120">活动</span><span class="sxs-lookup"><span data-stu-id="c7908-120">Activity</span></span>|<span data-ttu-id="c7908-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7908-121">xs:string</span></span>|<span data-ttu-id="c7908-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="c7908-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="c7908-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7908-123">DisplayName</span></span>|<span data-ttu-id="c7908-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7908-124">xs:string</span></span>|<span data-ttu-id="c7908-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c7908-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="c7908-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="c7908-126">InstanceId</span></span>|<span data-ttu-id="c7908-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7908-127">xs:string</span></span>|<span data-ttu-id="c7908-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="c7908-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="c7908-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c7908-129">AppDomain</span></span>|<span data-ttu-id="c7908-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7908-130">xs:string</span></span>|<span data-ttu-id="c7908-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c7908-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
