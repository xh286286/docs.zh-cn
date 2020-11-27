---
title: 每秒拒绝的排队消息数
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: 2b7686ee94ab051bc255bdb71681c8d1c473094c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96276199"
---
# <a name="queued-rejected-messages-per-second"></a><span data-ttu-id="7a65c-102">每秒拒绝的排队消息数</span><span class="sxs-lookup"><span data-stu-id="7a65c-102">Queued Rejected Messages Per Second</span></span>

<span data-ttu-id="7a65c-103">计数器名称：Queued Messages Rejected Per Second（每秒拒绝的排队消息数）。</span><span class="sxs-lookup"><span data-stu-id="7a65c-103">Counter Name: Queued Messages Rejected Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="7a65c-104">描述</span><span class="sxs-lookup"><span data-stu-id="7a65c-104">Description</span></span>  

 <span data-ttu-id="7a65c-105">此服务中每秒被排队传输拒绝的消息数。</span><span class="sxs-lookup"><span data-stu-id="7a65c-105">Number of messages that are rejected by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="7a65c-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="7a65c-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="7a65c-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="7a65c-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
