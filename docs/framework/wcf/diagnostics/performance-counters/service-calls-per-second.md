---
title: 服务：Calls Per Second（每秒调用次数）
ms.date: 03/30/2017
ms.assetid: 6261d28d-d449-425a-b9fc-a4ee14079134
ms.openlocfilehash: 7e702d402909c4a85a2cb42c837e0813c4d9f841
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96252876"
---
# <a name="service-calls-per-second"></a><span data-ttu-id="16a1e-102">服务：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="16a1e-102">Service: Calls Per Second</span></span>

<span data-ttu-id="16a1e-103">计数器名称：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="16a1e-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="16a1e-104">描述</span><span class="sxs-lookup"><span data-stu-id="16a1e-104">Description</span></span>  

 <span data-ttu-id="16a1e-105">一秒内调用此服务的次数。</span><span class="sxs-lookup"><span data-stu-id="16a1e-105">Number of calls to this service in a second.</span></span>  
  
 <span data-ttu-id="16a1e-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="16a1e-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="16a1e-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)。其中，分子 (N) 代表上一个取样时间间隔内执行的操作数，而分母 (D) 代表上一个取样时间间隔内所用的滴答数，而 F 则是滴答频率。</span><span class="sxs-lookup"><span data-stu-id="16a1e-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) where the numerator (N) represents the number of operations performed during the last sample interval, the denominator (D) represents the number of ticks elapsed during the last sample interval, and F is the frequency of the ticks.</span></span>
