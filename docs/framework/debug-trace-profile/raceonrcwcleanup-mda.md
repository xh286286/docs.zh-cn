---
title: raceOnRCWCleanup MDA
description: 查看 raceOnRCWCleanup 托管调试助手 (MDA) ，如果在另一个线程上或在 .NET 中释放线程堆栈上使用了 RCW，则激活该助手。
ms.date: 03/30/2017
helpviewer_keywords:
- RCW
- managed debugging assistants (MDAs), RCWs
- race on RCW cleanup
- MDAs (managed debugging assistants), RCWs
- RaceOnRCWCleanup MDA
- runtime callable wrappers
ms.assetid: bee1e9b1-50a8-4c89-9cd9-7dd6b2458187
ms.openlocfilehash: 393c5ea44108445a9a1a9d16e7d1d192eced5740
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96271442"
---
# <a name="raceonrcwcleanup-mda"></a><span data-ttu-id="6c74a-103">raceOnRCWCleanup MDA</span><span class="sxs-lookup"><span data-stu-id="6c74a-103">raceOnRCWCleanup MDA</span></span>

<span data-ttu-id="6c74a-104">当使用命令（如 <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A?displayProperty=nameWithType> 方法）发出一个调用来发布[运行时可调用包装](../../standard/native-interop/runtime-callable-wrapper.md) (RCW) 时，如果公共语言运行时 (CLR) 检测到该包装正在使用中，则激活 `raceOnRCWCleanup` 托管调试助手 (MDA)。</span><span class="sxs-lookup"><span data-stu-id="6c74a-104">The `raceOnRCWCleanup` managed debugging assistant (MDA) is activated when the common language runtime (CLR) detects that a [Runtime Callable Wrapper](../../standard/native-interop/runtime-callable-wrapper.md) (RCW) is in use when a call to release it is made using a command such as the <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="6c74a-105">症状</span><span class="sxs-lookup"><span data-stu-id="6c74a-105">Symptoms</span></span>  

 <span data-ttu-id="6c74a-106">使用 <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A> 或类似方法释放 RCW 期间或之后发生访问冲突或内存损坏。</span><span class="sxs-lookup"><span data-stu-id="6c74a-106">Access violations or memory corruption during or after freeing an RCW using <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A> or a similar method.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="6c74a-107">原因</span><span class="sxs-lookup"><span data-stu-id="6c74a-107">Cause</span></span>  

 <span data-ttu-id="6c74a-108">正在另一个线程中或释放线程堆栈中使用 RCW。</span><span class="sxs-lookup"><span data-stu-id="6c74a-108">The RCW is in use on another thread or on the freeing thread stack.</span></span>  <span data-ttu-id="6c74a-109">无法释放使用中的 RCW。</span><span class="sxs-lookup"><span data-stu-id="6c74a-109">An RCW that is in use cannot be released.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="6c74a-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="6c74a-110">Resolution</span></span>  

 <span data-ttu-id="6c74a-111">不要释放在当前或在其他线程中可能使用的 RCW。</span><span class="sxs-lookup"><span data-stu-id="6c74a-111">Do not free an RCW that could be in use either in the current or in other threads.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="6c74a-112">对运行时的影响</span><span class="sxs-lookup"><span data-stu-id="6c74a-112">Effect on the Runtime</span></span>  

 <span data-ttu-id="6c74a-113">此 MDA 对 CLR 无任何影响。</span><span class="sxs-lookup"><span data-stu-id="6c74a-113">This MDA has no effect on the CLR.</span></span>  
  
## <a name="output"></a><span data-ttu-id="6c74a-114">输出</span><span class="sxs-lookup"><span data-stu-id="6c74a-114">Output</span></span>  

 <span data-ttu-id="6c74a-115">描述错误的消息。</span><span class="sxs-lookup"><span data-stu-id="6c74a-115">A message describing the error.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="6c74a-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="6c74a-116">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <raceOnRCWCleanup/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6c74a-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c74a-117">See also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="6c74a-118">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="6c74a-118">Diagnosing Errors with Managed Debugging Assistants</span></span>](diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="6c74a-119">互操作封送处理</span><span class="sxs-lookup"><span data-stu-id="6c74a-119">Interop Marshaling</span></span>](../interop/interop-marshaling.md)
