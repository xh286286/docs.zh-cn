---
title: 终结点：Calls Per Second（每秒调用次数）
ms.date: 03/30/2017
ms.assetid: ca0fc06d-d68f-4236-bd5f-c7ff6214acdd
ms.openlocfilehash: 3c9f9882be935474ec187e2829e8e1e58b091afa
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96253149"
---
# <a name="endpoint-calls-per-second"></a><span data-ttu-id="49eed-102">终结点：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="49eed-102">Endpoint: Calls Per Second</span></span>

<span data-ttu-id="49eed-103">计数器名称：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="49eed-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="49eed-104">描述</span><span class="sxs-lookup"><span data-stu-id="49eed-104">Description</span></span>  

 <span data-ttu-id="49eed-105">一秒内对此终结点的调用次数。</span><span class="sxs-lookup"><span data-stu-id="49eed-105">Number of calls to this endpoint in a second.</span></span>  
  
 <span data-ttu-id="49eed-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="49eed-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="49eed-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="49eed-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
