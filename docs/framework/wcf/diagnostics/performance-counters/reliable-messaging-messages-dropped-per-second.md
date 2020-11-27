---
title: Reliable Messaging Messages Dropped Per Second（每秒丢弃的可靠消息传递消息数）
ms.date: 03/30/2017
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
ms.openlocfilehash: 1e6db155f21fb2443394bc3a65235d4e9539dab3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96276173"
---
# <a name="reliable-messaging-messages-dropped-per-second"></a><span data-ttu-id="bd385-102">Reliable Messaging Messages Dropped Per Second（每秒丢弃的可靠消息传递消息数）</span><span class="sxs-lookup"><span data-stu-id="bd385-102">Reliable Messaging Messages Dropped Per Second</span></span>

<span data-ttu-id="bd385-103">计数器名称：Reliable Messaging Sessions Dropped Per Second（每秒丢弃的可靠消息会话数）。</span><span class="sxs-lookup"><span data-stu-id="bd385-103">Counter Name: Reliable Messaging Sessions Dropped Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="bd385-104">描述</span><span class="sxs-lookup"><span data-stu-id="bd385-104">Description</span></span>  

 <span data-ttu-id="bd385-105">此服务上每秒钟丢弃的可靠传送消息总数。</span><span class="sxs-lookup"><span data-stu-id="bd385-105">Total number of reliable messaging messages that have been dropped in this service in a second.</span></span>  
  
 <span data-ttu-id="bd385-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="bd385-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="bd385-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="bd385-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
