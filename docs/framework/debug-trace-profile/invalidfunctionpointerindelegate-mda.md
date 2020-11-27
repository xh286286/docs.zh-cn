---
title: invalidFunctionPointerInDelegate MDA
description: 查看 invalidFunctionPointerInDelegate 托管调试助手 (MDA) ，如果传入了无效的函数指针以生成委托，则会调用它。
ms.date: 03/30/2017
helpviewer_keywords:
- invalidFunctionPointerInDelegate MDA
- managed debugging assistants (MDAs), invalid function pointer to delegates
- MDAs (managed debugging assistants), invalid function pointer to delegates
- function pointers, invalid
- marshaling, run-time errors
- managed debugging assistants (MDAs), marshaling
- MDAs (managed debugging assistants), marshaling
- invalid function pointers
ms.assetid: 99ae44f1-783e-49a9-9009-24f54bbd0f09
ms.openlocfilehash: 8072d35a45cb1e0590aa5533210d0e0f86913164
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96272613"
---
# <a name="invalidfunctionpointerindelegate-mda"></a><span data-ttu-id="3b00d-103">invalidFunctionPointerInDelegate MDA</span><span class="sxs-lookup"><span data-stu-id="3b00d-103">invalidFunctionPointerInDelegate MDA</span></span>

<span data-ttu-id="3b00d-104">如果在通过本机函数指针构造委托时传入的函数指针无效，将激活 `invalidFunctionPointerInDelegate` 托管调试助手 (MDA)。</span><span class="sxs-lookup"><span data-stu-id="3b00d-104">The `invalidFunctionPointerInDelegate` managed debugging assistant (MDA) is activated when an invalid function pointer is passed in to construct a delegate over a native function pointer.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="3b00d-105">症状</span><span class="sxs-lookup"><span data-stu-id="3b00d-105">Symptoms</span></span>  

 <span data-ttu-id="3b00d-106">使用通过函数指针实现的委托时，发生访问冲突或意外的内存中断。</span><span class="sxs-lookup"><span data-stu-id="3b00d-106">Access violations or unexpected memory corruption when using a delegate over a function pointer.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="3b00d-107">原因</span><span class="sxs-lookup"><span data-stu-id="3b00d-107">Cause</span></span>  

 <span data-ttu-id="3b00d-108">指定了无效的函数指针。</span><span class="sxs-lookup"><span data-stu-id="3b00d-108">An invalid function pointer was specified.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="3b00d-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="3b00d-109">Resolution</span></span>  

 <span data-ttu-id="3b00d-110">指定有效的函数指针</span><span class="sxs-lookup"><span data-stu-id="3b00d-110">Specify a valid function pointer</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="3b00d-111">对运行时的影响</span><span class="sxs-lookup"><span data-stu-id="3b00d-111">Effect on the Runtime</span></span>  

 <span data-ttu-id="3b00d-112">此 MDA 对 CLR 无任何影响。</span><span class="sxs-lookup"><span data-stu-id="3b00d-112">This MDA has no effect on the CLR.</span></span>  
  
## <a name="output"></a><span data-ttu-id="3b00d-113">输出</span><span class="sxs-lookup"><span data-stu-id="3b00d-113">Output</span></span>  

 <span data-ttu-id="3b00d-114">无效的函数指针。</span><span class="sxs-lookup"><span data-stu-id="3b00d-114">The invalid function pointer.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="3b00d-115">Configuration</span><span class="sxs-lookup"><span data-stu-id="3b00d-115">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <invalidFunctionPointerInDelegate />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3b00d-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b00d-116">See also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="3b00d-117">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="3b00d-117">Diagnosing Errors with Managed Debugging Assistants</span></span>](diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="3b00d-118">互操作封送处理</span><span class="sxs-lookup"><span data-stu-id="3b00d-118">Interop Marshaling</span></span>](../interop/interop-marshaling.md)
