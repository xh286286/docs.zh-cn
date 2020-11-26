---
title: 224 - MessageThrottleAtSeventyPercent
ms.date: 03/30/2017
ms.assetid: 82bbbfd7-10d2-41fd-805d-2443b0c1b96b
ms.openlocfilehash: 26b860b88313a971960a65b599562ef1ccb4e7da
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96243516"
---
# <a name="224---messagethrottleatseventypercent"></a><span data-ttu-id="ae162-102">224 - MessageThrottleAtSeventyPercent</span><span class="sxs-lookup"><span data-stu-id="ae162-102">224 - MessageThrottleAtSeventyPercent</span></span>

## <a name="properties"></a><span data-ttu-id="ae162-103">属性</span><span class="sxs-lookup"><span data-stu-id="ae162-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ae162-104">ID</span><span class="sxs-lookup"><span data-stu-id="ae162-104">ID</span></span>|<span data-ttu-id="ae162-105">224</span><span class="sxs-lookup"><span data-stu-id="ae162-105">224</span></span>|  
|<span data-ttu-id="ae162-106">关键字</span><span class="sxs-lookup"><span data-stu-id="ae162-106">Keywords</span></span>|<span data-ttu-id="ae162-107">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="ae162-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="ae162-108">Level</span><span class="sxs-lookup"><span data-stu-id="ae162-108">Level</span></span>|<span data-ttu-id="ae162-109">警告</span><span class="sxs-lookup"><span data-stu-id="ae162-109">Warning</span></span>|  
|<span data-ttu-id="ae162-110">通道</span><span class="sxs-lookup"><span data-stu-id="ae162-110">Channel</span></span>|<span data-ttu-id="ae162-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="ae162-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ae162-112">描述</span><span class="sxs-lookup"><span data-stu-id="ae162-112">Description</span></span>  

 <span data-ttu-id="ae162-113">当超出某个主服务中止值时，将发出 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="ae162-113">When one of the main service throttles has been exceeded, the `MessageThrottleExceeded` event is emitted.</span></span> <span data-ttu-id="ae162-114">当活动峰值变慢且当前中止值达到当前限制值的 70% 时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ae162-114">When the spike of activity slows and the current value of the throttle is at 70 percent of the current limit then this event is emitted.</span></span> <span data-ttu-id="ae162-115">请注意，仅在活动变慢时才发出一次此事件。</span><span class="sxs-lookup"><span data-stu-id="ae162-115">Note that this event is only emitted once as the activity is slowing.</span></span> <span data-ttu-id="ae162-116">如果当前值在 70% 标记的附近波动（例如，70,69,70,71,70,69），则只有第一次出现的 70% 会导致发出事件。</span><span class="sxs-lookup"><span data-stu-id="ae162-116">If the current value hovers at the 70 percent mark, (for example, 70,69,70,71,70,69), only the first occurrence of 70 percent results in an event.</span></span> <span data-ttu-id="ae162-117">在发出此事件后，如果将来出现超出中止值的情况，则也会导致发出 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="ae162-117">After this event is emitted, future occurrences of exceeding the throttle's limit result in a `MessageThrottleExceeded` event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ae162-118">消息</span><span class="sxs-lookup"><span data-stu-id="ae162-118">Message</span></span>  

 <span data-ttu-id="ae162-119">“%2”的“%1”中止值为 70%%。</span><span class="sxs-lookup"><span data-stu-id="ae162-119">The '%1' throttle limit of '%2' is at 70%%.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ae162-120">详细信息</span><span class="sxs-lookup"><span data-stu-id="ae162-120">Details</span></span>  
  
|<span data-ttu-id="ae162-121">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ae162-121">Data Item Name</span></span>|<span data-ttu-id="ae162-122">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ae162-122">Data Item Type</span></span>|<span data-ttu-id="ae162-123">描述</span><span class="sxs-lookup"><span data-stu-id="ae162-123">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ae162-124">中止值名称</span><span class="sxs-lookup"><span data-stu-id="ae162-124">Throttle Name</span></span>|`xs:string`|<span data-ttu-id="ae162-125">超过的中止值的名称。</span><span class="sxs-lookup"><span data-stu-id="ae162-125">The name of the throttle that has been exceeded.</span></span> <span data-ttu-id="ae162-126">`MaxConcurrentCalls`、`MaxConcurrentInstances` 或 `MaxConcurrentSessions`。</span><span class="sxs-lookup"><span data-stu-id="ae162-126">Either `MaxConcurrentCalls`, `MaxConcurrentInstances`, or `MaxConcurrentSessions`,</span></span>|  
|<span data-ttu-id="ae162-127">限制</span><span class="sxs-lookup"><span data-stu-id="ae162-127">Limit</span></span>|`xs:long`|<span data-ttu-id="ae162-128">当前配置的中止值限制。</span><span class="sxs-lookup"><span data-stu-id="ae162-128">The currently configured limit of the throttle.</span></span>|  
|<span data-ttu-id="ae162-129">HostReference</span><span class="sxs-lookup"><span data-stu-id="ae162-129">HostReference</span></span>|`xs:string`|<span data-ttu-id="ae162-130">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="ae162-130">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="ae162-131">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="ae162-131">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="ae162-132">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="ae162-132">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="ae162-133">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ae162-133">AppDomain</span></span>|`xs:string`|<span data-ttu-id="ae162-134">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ae162-134">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
