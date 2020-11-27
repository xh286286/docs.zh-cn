---
title: ETW Events in the .NET Framework
description: 请参阅文章链接，了解 Windows 的事件跟踪 (.NET 中的 ETW) 。 ETW 是高性能、低开销且可扩展的跟踪系统。
ms.date: 03/30/2017
helpviewer_keywords:
- .NET Framework ETW events
- ETW events in the .NET Framework
ms.assetid: d186276f-6afb-4dfd-bf3c-4251edc2c299
ms.openlocfilehash: c8eaec37689d4c62b1faf53364ff63012b99106f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96263615"
---
# <a name="etw-events-in-the-net-framework"></a><span data-ttu-id="af4c5-104">ETW Events in the .NET Framework</span><span class="sxs-lookup"><span data-stu-id="af4c5-104">ETW Events in the .NET Framework</span></span>

<span data-ttu-id="af4c5-105">Windows 事件跟踪 (ETW) 是 Windows 操作系统提供的高性能、低开销的可缩放跟踪系统。</span><span class="sxs-lookup"><span data-stu-id="af4c5-105">Event tracing for Windows (ETW) is a high-performance, low-overhead, scalable tracing system provided by Windows operating systems.</span></span> <span data-ttu-id="af4c5-106">它可补充 .NET Framework 所提供的分析和调试支持，可用于排除各种问题。</span><span class="sxs-lookup"><span data-stu-id="af4c5-106">It supplements the profiling and debugging support provided by the .NET Framework and can be used to troubleshoot a variety of scenarios.</span></span>  
  
 <span data-ttu-id="af4c5-107">在 .NET Framework 中，ETW 事件跟踪适用于公共语言运行时 (CLR)、[任务并行库](../../standard/parallel-programming/task-parallel-library-tpl.md)和 [并行 LINQ (PLINQ)](../../standard/parallel-programming/introduction-to-plinq.md)。</span><span class="sxs-lookup"><span data-stu-id="af4c5-107">In the .NET Framework, ETW event tracing is available for the common language runtime (CLR), the [Task Parallel Library](../../standard/parallel-programming/task-parallel-library-tpl.md), and [Parallel LINQ (PLINQ)](../../standard/parallel-programming/introduction-to-plinq.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="af4c5-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="af4c5-108">In This Section</span></span>  

 [<span data-ttu-id="af4c5-109">任务并行库和 PLINQ 中的 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="af4c5-109">ETW Events in Task Parallel Library and PLINQ</span></span>](etw-events-in-task-parallel-library-and-plinq.md)  
 <span data-ttu-id="af4c5-110">介绍如何分析并行应用程序代码。</span><span class="sxs-lookup"><span data-stu-id="af4c5-110">Describes how to profile parallel application code.</span></span>  
  
 [<span data-ttu-id="af4c5-111">公共语言运行时中的 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="af4c5-111">ETW Events in the Common Language Runtime</span></span>](etw-events-in-the-common-language-runtime.md)  
 <span data-ttu-id="af4c5-112">介绍 CLR ETW 事件如何补充公共语言运行时所提供的分析和调试支持。</span><span class="sxs-lookup"><span data-stu-id="af4c5-112">Describes how CLR ETW events supplement the profiling and debugging support provided by the common language runtime.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af4c5-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af4c5-113">See also</span></span>

- [<span data-ttu-id="af4c5-114">CLR ETW 事件</span><span class="sxs-lookup"><span data-stu-id="af4c5-114">CLR ETW Events</span></span>](clr-etw-events.md)
- [<span data-ttu-id="af4c5-115">任务并行库 (TPL)</span><span class="sxs-lookup"><span data-stu-id="af4c5-115">Task Parallel Library (TPL)</span></span>](../../standard/parallel-programming/task-parallel-library-tpl.md)
- [<span data-ttu-id="af4c5-116">并行 LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="af4c5-116">Parallel LINQ (PLINQ)</span></span>](../../standard/parallel-programming/introduction-to-plinq.md)
