---
title: 57398 - MaxInstancesExceeded
ms.date: 03/30/2017
ms.assetid: f943d209-dfeb-43e5-b572-c9a06217936e
ms.openlocfilehash: bd490aad24fba4550bc778799cd6f836dcfd466c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96289173"
---
# <a name="57398---maxinstancesexceeded"></a><span data-ttu-id="4d82f-102">57398 - MaxInstancesExceeded</span><span class="sxs-lookup"><span data-stu-id="4d82f-102">57398 - MaxInstancesExceeded</span></span>

## <a name="properties"></a><span data-ttu-id="4d82f-103">属性</span><span class="sxs-lookup"><span data-stu-id="4d82f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4d82f-104">ID</span><span class="sxs-lookup"><span data-stu-id="4d82f-104">ID</span></span>|<span data-ttu-id="4d82f-105">57398</span><span class="sxs-lookup"><span data-stu-id="4d82f-105">57398</span></span>|  
|<span data-ttu-id="4d82f-106">关键字</span><span class="sxs-lookup"><span data-stu-id="4d82f-106">Keywords</span></span>|<span data-ttu-id="4d82f-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="4d82f-107">WFServices</span></span>|  
|<span data-ttu-id="4d82f-108">Level</span><span class="sxs-lookup"><span data-stu-id="4d82f-108">Level</span></span>|<span data-ttu-id="4d82f-109">警告</span><span class="sxs-lookup"><span data-stu-id="4d82f-109">Warning</span></span>|  
|<span data-ttu-id="4d82f-110">通道</span><span class="sxs-lookup"><span data-stu-id="4d82f-110">Channel</span></span>|<span data-ttu-id="4d82f-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="4d82f-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4d82f-112">描述</span><span class="sxs-lookup"><span data-stu-id="4d82f-112">Description</span></span>  

 <span data-ttu-id="4d82f-113">指示系统达到为限制“MaxConcurrentInstances”设置的限制值。</span><span class="sxs-lookup"><span data-stu-id="4d82f-113">Indicates the system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4d82f-114">消息</span><span class="sxs-lookup"><span data-stu-id="4d82f-114">Message</span></span>  

 <span data-ttu-id="4d82f-115">系统达到为限制“MaxConcurrentInstances”设置的限制值。</span><span class="sxs-lookup"><span data-stu-id="4d82f-115">The system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span> <span data-ttu-id="4d82f-116">此限制的限制值设置为 %1。</span><span class="sxs-lookup"><span data-stu-id="4d82f-116">Limit for this throttle was set to %1.</span></span> <span data-ttu-id="4d82f-117">可通过修改 serviceThrottle 元素中的特性“maxConcurrentInstances”或修改行为 ServiceThrottlingBehavior 的“MaxConcurrentInstances”属性来更改限制值。</span><span class="sxs-lookup"><span data-stu-id="4d82f-117">Throttle value can be changed by modifying attribute 'maxConcurrentInstances' in serviceThrottle element or by modifying 'MaxConcurrentInstances' property on behavior ServiceThrottlingBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4d82f-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="4d82f-118">Details</span></span>  
  
|<span data-ttu-id="4d82f-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="4d82f-119">Data Item Name</span></span>|<span data-ttu-id="4d82f-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="4d82f-120">Data Item Type</span></span>|<span data-ttu-id="4d82f-121">描述</span><span class="sxs-lookup"><span data-stu-id="4d82f-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4d82f-122">“属性”</span><span class="sxs-lookup"><span data-stu-id="4d82f-122">Name</span></span>|<span data-ttu-id="4d82f-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="4d82f-123">xs:string</span></span>|<span data-ttu-id="4d82f-124">项的名称。</span><span class="sxs-lookup"><span data-stu-id="4d82f-124">The name of the item.</span></span>|  
|<span data-ttu-id="4d82f-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="4d82f-125">AppDomain</span></span>|<span data-ttu-id="4d82f-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="4d82f-126">xs:string</span></span>|<span data-ttu-id="4d82f-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="4d82f-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
