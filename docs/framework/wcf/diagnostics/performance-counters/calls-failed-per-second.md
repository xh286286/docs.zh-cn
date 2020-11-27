---
title: Calls Failed Per Second（每秒失败的调用次数）
ms.date: 03/30/2017
ms.assetid: e4ef3773-f650-4876-99cf-4d0c02aa03d4
ms.openlocfilehash: d3eafc4b31f0e62093a972b7c9f2325a3648d21b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96285455"
---
# <a name="calls-failed-per-second"></a><span data-ttu-id="9004a-102">Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="9004a-102">Calls Failed Per Second</span></span>

<span data-ttu-id="9004a-103">计数器名称：Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="9004a-103">Counter Name: Calls Failed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="9004a-104">描述</span><span class="sxs-lookup"><span data-stu-id="9004a-104">Description</span></span>  

 <span data-ttu-id="9004a-105">该操作中每秒钟出现未处理异常的调用数目。</span><span class="sxs-lookup"><span data-stu-id="9004a-105">Number of calls with unhandled exceptions in this operation in a second.</span></span>  
  
 <span data-ttu-id="9004a-106">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="9004a-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="9004a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="9004a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="9004a-108">此操作中每次出现未处理的异常时，此计数器都会递增。</span><span class="sxs-lookup"><span data-stu-id="9004a-108">This counter is incremented every time there is an unhandled exception in this operation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9004a-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9004a-109">See also</span></span>

- [<span data-ttu-id="9004a-110">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="9004a-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
