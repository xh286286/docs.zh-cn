---
title: 如何：从任务中返回值
description: 了解如何使用 System.Threading.Tasks.Task<TResult> 类型从 .NET 中的 Result 属性返回值。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to return a value
ms.assetid: c4bc0f44-eba2-4e96-9e03-1cc787461e61
ms.openlocfilehash: c7a4a683545c9ef0448d9cdce769aae79215aecf
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94825606"
---
# <a name="how-to-return-a-value-from-a-task"></a><span data-ttu-id="d904f-103">如何：从任务中返回值</span><span class="sxs-lookup"><span data-stu-id="d904f-103">How to: Return a Value from a Task</span></span>
<span data-ttu-id="d904f-104">此示例演示如何使用 <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> 类型，以返回 <xref:System.Threading.Tasks.Task%601.Result%2A> 属性的值。</span><span class="sxs-lookup"><span data-stu-id="d904f-104">This example shows how to use the <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> type to return a value from the <xref:System.Threading.Tasks.Task%601.Result%2A> property.</span></span> <span data-ttu-id="d904f-105">它要求 C:\Users\Public\Pictures\Sample Pictures\ 目录存在，并且该目录包含文件。</span><span class="sxs-lookup"><span data-stu-id="d904f-105">It requires that the C:\Users\Public\Pictures\Sample Pictures\ directory exists, and that it contains files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d904f-106">示例</span><span class="sxs-lookup"><span data-stu-id="d904f-106">Example</span></span>  
 [!code-csharp[TPL#10](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl/cs/returnavalue10.cs#10)]
 [!code-vb[TPL#10](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl/vb/10_returnavalue.vb#10)]  
  
 <span data-ttu-id="d904f-107"><xref:System.Threading.Tasks.Task%601.Result%2A> 属性将阻止调用线程，直到任务完成。</span><span class="sxs-lookup"><span data-stu-id="d904f-107">The <xref:System.Threading.Tasks.Task%601.Result%2A> property blocks the calling thread until the task finishes.</span></span>  
  
 <span data-ttu-id="d904f-108">若要了解如何将一个 <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> 的结果传递到延续任务，请参阅[使用延续任务链接任务](chaining-tasks-by-using-continuation-tasks.md)。</span><span class="sxs-lookup"><span data-stu-id="d904f-108">To see how to pass the result of one <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> to a continuation task, see [Chaining Tasks by Using Continuation Tasks](chaining-tasks-by-using-continuation-tasks.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d904f-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="d904f-109">See also</span></span>

- [<span data-ttu-id="d904f-110">基于任务的异步编程</span><span class="sxs-lookup"><span data-stu-id="d904f-110">Task-based Asynchronous Programming</span></span>](task-based-asynchronous-programming.md)
- [<span data-ttu-id="d904f-111">PLINQ 和 TPL 中的 Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="d904f-111">Lambda Expressions in PLINQ and TPL</span></span>](lambda-expressions-in-plinq-and-tpl.md)
