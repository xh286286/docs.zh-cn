---
title: SYSLIB0006 警告
description: 了解有关生成编译时警告 SYSLIB0006 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 222b669a8a0260713e85721e6031144bb7bda5cc
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94440655"
---
# <a name="syslib0006-threadabort-is-not-supported"></a><span data-ttu-id="59ae0-103">SYSLIB0006：不支持 Thread.Abort</span><span class="sxs-lookup"><span data-stu-id="59ae0-103">SYSLIB0006: Thread.Abort is not supported</span></span>

<span data-ttu-id="59ae0-104">从 .NET 5.0 开始，以下 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="59ae0-104">The following APIs are marked obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="59ae0-105">使用这些 API 会在编译时生成警告 `SYSLIB0006`。</span><span class="sxs-lookup"><span data-stu-id="59ae0-105">Use of these APIs generates warning `SYSLIB0006` at compile time.</span></span>

- <xref:System.Threading.Thread.Abort?displayProperty=nameWithType>
- <xref:System.Threading.Thread.Abort(System.Object)?displayProperty=nameWithType>

## <a name="workarounds"></a><span data-ttu-id="59ae0-106">工作区</span><span class="sxs-lookup"><span data-stu-id="59ae0-106">Workarounds</span></span>

<span data-ttu-id="59ae0-107">使用 <xref:System.Threading.CancellationToken> 中止对工作单元的处理，而不是调用 <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="59ae0-107">Use a <xref:System.Threading.CancellationToken> to abort processing of a unit of work instead of calling <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="59ae0-108">以下示例说明了 <xref:System.Threading.CancellationToken> 的用法。</span><span class="sxs-lookup"><span data-stu-id="59ae0-108">The following example illustrates the use of <xref:System.Threading.CancellationToken>.</span></span>

```csharp
void ProcessPendingWorkItemsNew(CancellationToken cancellationToken)
{
    if (QueryIsMoreWorkPending())
    {
        // If the CancellationToken is marked as "needs to cancel",
        // this will throw the appropriate exception.
        cancellationToken.ThrowIfCancellationRequested();

        WorkItem work = DequeueWorkItem();
        ProcessWorkItem(work);
    }
}
```

[!INCLUDE [suppress-syslib-warning](../../../includes/suppress-syslib-warning.md)]

## <a name="see-also"></a><span data-ttu-id="59ae0-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59ae0-109">See also</span></span>

- [<span data-ttu-id="59ae0-110">Thread.Abort 已过时 - 中断性变更</span><span class="sxs-lookup"><span data-stu-id="59ae0-110">Thread.Abort is obsolete - breaking change</span></span>](3.1-5.0.md#threadabort-is-obsolete)
- [<span data-ttu-id="59ae0-111">托管线程中的取消</span><span class="sxs-lookup"><span data-stu-id="59ae0-111">Cancellation in managed threads</span></span>](../../standard/threading/cancellation-in-managed-threads.md)
