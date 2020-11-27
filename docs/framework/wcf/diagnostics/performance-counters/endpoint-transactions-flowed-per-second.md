---
title: 终结点：Transactions Flowed Per Second（每秒流动的事务数）
ms.date: 03/30/2017
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
ms.openlocfilehash: b814d7ca9e286426289c611b3a6bf5a52c1b2335
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96256425"
---
# <a name="endpoint-transactions-flowed-per-second"></a><span data-ttu-id="e1ae2-102">终结点：Transactions Flowed Per Second（每秒流动的事务数）</span><span class="sxs-lookup"><span data-stu-id="e1ae2-102">Endpoint: Transactions Flowed Per Second</span></span>

<span data-ttu-id="e1ae2-103">计数器名称：Transactions Flowed Per Second（每秒流动的事务数）。</span><span class="sxs-lookup"><span data-stu-id="e1ae2-103">Counter Name: Transactions Flowed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e1ae2-104">描述</span><span class="sxs-lookup"><span data-stu-id="e1ae2-104">Description</span></span>  

 <span data-ttu-id="e1ae2-105">一秒内流向此终结点上的操作的事务数。</span><span class="sxs-lookup"><span data-stu-id="e1ae2-105">Number of transactions flowed to operations at this endpoint in a second.</span></span> <span data-ttu-id="e1ae2-106">只要发送到终结点的消息中出现事务 ID，此计数器即会递增。</span><span class="sxs-lookup"><span data-stu-id="e1ae2-106">This counter is incremented any time a transaction ID is present in a message sent to the endpoint.</span></span>  
  
 <span data-ttu-id="e1ae2-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="e1ae2-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="e1ae2-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="e1ae2-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
