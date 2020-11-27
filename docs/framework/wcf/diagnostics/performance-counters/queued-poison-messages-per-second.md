---
title: 每秒排队病毒消息数
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: 1e515a81580bd9773841bee4230288d8c7d12216
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96276225"
---
# <a name="queued-poison-messages-per-second"></a><span data-ttu-id="03d4a-102">每秒排队病毒消息数</span><span class="sxs-lookup"><span data-stu-id="03d4a-102">Queued Poison Messages Per Second</span></span>

<span data-ttu-id="03d4a-103">计数器名称：Queued Poison Messages Per Second（每秒排队病毒消息数）。</span><span class="sxs-lookup"><span data-stu-id="03d4a-103">Counter Name: Queued Poison Messages Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="03d4a-104">描述</span><span class="sxs-lookup"><span data-stu-id="03d4a-104">Description</span></span>  

 <span data-ttu-id="03d4a-105">此服务中每秒由排队传输标记为病毒消息的消息数。</span><span class="sxs-lookup"><span data-stu-id="03d4a-105">Number of messages that are marked poisoned by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="03d4a-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="03d4a-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="03d4a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="03d4a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
