---
title: 如何：在管道中使用阻塞集合的数组
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- thread-safe collections, blocking collections in pipeline
ms.assetid: a39c7ec3-3ad7-4f4d-8fe4-b3e9dbabe2ed
ms.openlocfilehash: a79cd13af19a8f67fd5a96ce80dc899ca6f07516
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94824995"
---
# <a name="how-to-use-arrays-of-blocking-collections-in-a-pipeline"></a><span data-ttu-id="31e6a-102">如何：在管道中使用阻塞集合的数组</span><span class="sxs-lookup"><span data-stu-id="31e6a-102">How to: Use Arrays of Blocking Collections in a Pipeline</span></span>
<span data-ttu-id="31e6a-103">下面的示例演示如何将 <xref:System.Collections.Concurrent.BlockingCollection%601?displayProperty=nameWithType> 对象的数组与静态方法（如 <xref:System.Collections.Concurrent.BlockingCollection%601.TryAddToAny%2A> 和 <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny%2A>）配合使用，在组件之间实现快速而灵活的数据传输。</span><span class="sxs-lookup"><span data-stu-id="31e6a-103">The following example shows how to use arrays of <xref:System.Collections.Concurrent.BlockingCollection%601?displayProperty=nameWithType> objects with static methods such as <xref:System.Collections.Concurrent.BlockingCollection%601.TryAddToAny%2A> and <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny%2A> to implement fast and flexible data transfer between components.</span></span>  
  
## <a name="example"></a><span data-ttu-id="31e6a-104">示例</span><span class="sxs-lookup"><span data-stu-id="31e6a-104">Example</span></span>  
 <span data-ttu-id="31e6a-105">下面的示例演示基本管道实现，在此实现中，每个对象同时获取输入集合中的数据、转换该数据并将该数据传递到输出集合。</span><span class="sxs-lookup"><span data-stu-id="31e6a-105">The following example demonstrates a basic pipeline implementation in which each object is concurrently taking data from the input collection, transforming it, and passing it to the output collection.</span></span>  
  
 [!code-csharp[CDS_BlockingCollection#07](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example07.cs#07)]
 [!code-vb[CDS_BlockingCollection#07](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/bcpipeline.vb#07)]  
  
## <a name="see-also"></a><span data-ttu-id="31e6a-106">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31e6a-106">See also</span></span>

- <xref:System.Collections.Concurrent?displayProperty=nameWithType>
- [<span data-ttu-id="31e6a-107">线程安全集合</span><span class="sxs-lookup"><span data-stu-id="31e6a-107">Thread-Safe Collections</span></span>](index.md)
