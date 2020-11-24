---
title: 如何：在 PLINQ 查询中控制排序
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PLINQ queries, how to control ordering
ms.assetid: c67eccc7-004d-4b2f-987e-919cbbd62ef7
ms.openlocfilehash: 88f19092b06e4dece202e880287bdb95e04d2f2d
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94817102"
---
# <a name="how-to-control-ordering-in-a-plinq-query"></a><span data-ttu-id="55a41-102">如何：在 PLINQ 查询中控制排序</span><span class="sxs-lookup"><span data-stu-id="55a41-102">How to: Control Ordering in a PLINQ Query</span></span>
<span data-ttu-id="55a41-103">这些示例展示了如何使用 <xref:System.Linq.ParallelEnumerable.AsOrdered%2A> 扩展方法控制 PLINQ 查询中的顺序。</span><span class="sxs-lookup"><span data-stu-id="55a41-103">These examples show how to control the ordering in a PLINQ query by using the <xref:System.Linq.ParallelEnumerable.AsOrdered%2A> extension method.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="55a41-104">这些示例主要用于演示用法，可能会或可能不会比相当的顺序 LINQ to Objects 查询快。</span><span class="sxs-lookup"><span data-stu-id="55a41-104">These examples are primarily intended to demonstrate usage, and may or may not run faster than the equivalent sequential LINQ to Objects queries.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55a41-105">示例</span><span class="sxs-lookup"><span data-stu-id="55a41-105">Example</span></span>  
 <span data-ttu-id="55a41-106">下面的示例暂留了源序列的顺序。</span><span class="sxs-lookup"><span data-stu-id="55a41-106">The following example preserves the ordering of the source sequence.</span></span> <span data-ttu-id="55a41-107">有时，这样做是有必要的；例如，一些查询运算符需要有序的源序列，才能生成正确结果。</span><span class="sxs-lookup"><span data-stu-id="55a41-107">This is sometimes necessary; for example some query operators require an ordered source sequence to produce correct results.</span></span>  
  
 [!code-csharp[PLINQ#12](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#12)]
 [!code-vb[PLINQ#12](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="55a41-108">示例</span><span class="sxs-lookup"><span data-stu-id="55a41-108">Example</span></span>  
 <span data-ttu-id="55a41-109">下面的示例展示了一些可能要求源序列应为有序的查询运算符。</span><span class="sxs-lookup"><span data-stu-id="55a41-109">The following example shows some query operators whose source sequence is probably expected to be ordered.</span></span> <span data-ttu-id="55a41-110">虽然这些运算符可以处理无序序列，但可能会生成意外结果。</span><span class="sxs-lookup"><span data-stu-id="55a41-110">These operators will work on unordered sequences, but they might produce unexpected results.</span></span>  
  
 [!code-csharp[PLINQ#14](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#14)]
 [!code-vb[PLINQ#14](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#14)]  
  
 <span data-ttu-id="55a41-111">若要运行此方法，请将它粘贴到 [PLINQ 数据样本](plinq-data-sample.md)项目的 PLINQDataSample 类中，再按 F5。</span><span class="sxs-lookup"><span data-stu-id="55a41-111">To run this method, paste it into the PLINQDataSample class in the [PLINQ Data Sample](plinq-data-sample.md) project and press F5.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55a41-112">示例</span><span class="sxs-lookup"><span data-stu-id="55a41-112">Example</span></span>  
 <span data-ttu-id="55a41-113">下面的示例展示了如何暂留查询第一部分的顺序，再删除顺序以提升 join 子句的性能，并对最终结果序列重新应用顺序。</span><span class="sxs-lookup"><span data-stu-id="55a41-113">The following example shows how to preserve ordering for the first part of a query, then remove the ordering to increase the performance of a join clause, and then reapply ordering to the final result sequence.</span></span>  
  
 [!code-csharp[PLINQ#15](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#15)]
 [!code-vb[PLINQ#15](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#15)]  
  
 <span data-ttu-id="55a41-114">若要运行此方法，请将它粘贴到 [PLINQ 数据样本](plinq-data-sample.md)项目的 PLINQDataSample 类中，再按 F5。</span><span class="sxs-lookup"><span data-stu-id="55a41-114">To run this method, paste it into the PLINQDataSample class in the [PLINQ Data Sample](plinq-data-sample.md) project and press F5.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55a41-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="55a41-115">See also</span></span>

- <xref:System.Linq.ParallelEnumerable>
- [<span data-ttu-id="55a41-116">并行 LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="55a41-116">Parallel LINQ (PLINQ)</span></span>](introduction-to-plinq.md)
