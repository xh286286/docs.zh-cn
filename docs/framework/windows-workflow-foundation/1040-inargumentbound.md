---
title: 1040 - InArgumentBound
ms.date: 03/30/2017
ms.assetid: 7dfaad1b-36c0-4575-84c1-31d63b0eaf5d
ms.openlocfilehash: 04a61892ea817d5168ccbfccf68c0b74ee43e983
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96238946"
---
# <a name="1040---inargumentbound"></a><span data-ttu-id="833ce-102">1040 - InArgumentBound</span><span class="sxs-lookup"><span data-stu-id="833ce-102">1040 - InArgumentBound</span></span>

## <a name="properties"></a><span data-ttu-id="833ce-103">属性</span><span class="sxs-lookup"><span data-stu-id="833ce-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="833ce-104">ID</span><span class="sxs-lookup"><span data-stu-id="833ce-104">ID</span></span>|<span data-ttu-id="833ce-105">1040</span><span class="sxs-lookup"><span data-stu-id="833ce-105">1040</span></span>|  
|<span data-ttu-id="833ce-106">关键字</span><span class="sxs-lookup"><span data-stu-id="833ce-106">Keywords</span></span>|<span data-ttu-id="833ce-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="833ce-107">WFActivities</span></span>|  
|<span data-ttu-id="833ce-108">级别</span><span class="sxs-lookup"><span data-stu-id="833ce-108">Level</span></span>|<span data-ttu-id="833ce-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="833ce-109">Verbose</span></span>|  
|<span data-ttu-id="833ce-110">通道</span><span class="sxs-lookup"><span data-stu-id="833ce-110">Channel</span></span>|<span data-ttu-id="833ce-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="833ce-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="833ce-112">描述</span><span class="sxs-lookup"><span data-stu-id="833ce-112">Description</span></span>  

 <span data-ttu-id="833ce-113">指示已绑定 In 自变量。</span><span class="sxs-lookup"><span data-stu-id="833ce-113">Indicates an In argument has been bound.</span></span>  
  
## <a name="message"></a><span data-ttu-id="833ce-114">消息</span><span class="sxs-lookup"><span data-stu-id="833ce-114">Message</span></span>  

 <span data-ttu-id="833ce-115">Activity“%2”、DisplayName“%3”、InstanceId“%4”中的 In 自变量“%1”已经与值 %5 绑定。</span><span class="sxs-lookup"><span data-stu-id="833ce-115">In argument '%1' on Activity '%2', DisplayName: '%3', InstanceId: '%4' has been bound with value: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="833ce-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="833ce-116">Details</span></span>  
  
|<span data-ttu-id="833ce-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="833ce-117">Data Item Name</span></span>|<span data-ttu-id="833ce-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="833ce-118">Data Item Type</span></span>|<span data-ttu-id="833ce-119">描述</span><span class="sxs-lookup"><span data-stu-id="833ce-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="833ce-120">InArgument</span><span class="sxs-lookup"><span data-stu-id="833ce-120">InArgument</span></span>|<span data-ttu-id="833ce-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-121">xs:string</span></span>|<span data-ttu-id="833ce-122">InArgument 的名称。</span><span class="sxs-lookup"><span data-stu-id="833ce-122">The name of the InArgument.</span></span>|  
|<span data-ttu-id="833ce-123">活动</span><span class="sxs-lookup"><span data-stu-id="833ce-123">Activity</span></span>|<span data-ttu-id="833ce-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-124">xs:string</span></span>|<span data-ttu-id="833ce-125">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="833ce-125">The type name of the activity.</span></span>|  
|<span data-ttu-id="833ce-126">DisplayName</span><span class="sxs-lookup"><span data-stu-id="833ce-126">DisplayName</span></span>|<span data-ttu-id="833ce-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-127">xs:string</span></span>|<span data-ttu-id="833ce-128">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="833ce-128">The display name of the activity.</span></span>|  
|<span data-ttu-id="833ce-129">InstanceId</span><span class="sxs-lookup"><span data-stu-id="833ce-129">InstanceId</span></span>|<span data-ttu-id="833ce-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-130">xs:string</span></span>|<span data-ttu-id="833ce-131">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="833ce-131">The instance id of the activity.</span></span>|  
|<span data-ttu-id="833ce-132">值</span><span class="sxs-lookup"><span data-stu-id="833ce-132">Value</span></span>|<span data-ttu-id="833ce-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-133">xs:string</span></span>|<span data-ttu-id="833ce-134">绑定到 InArgument 的值。</span><span class="sxs-lookup"><span data-stu-id="833ce-134">The value bound to the InArgument.</span></span>|  
|<span data-ttu-id="833ce-135">应用程序域</span><span class="sxs-lookup"><span data-stu-id="833ce-135">AppDomain</span></span>|<span data-ttu-id="833ce-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="833ce-136">xs:string</span></span>|<span data-ttu-id="833ce-137">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="833ce-137">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
