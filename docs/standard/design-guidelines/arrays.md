---
title: 数组
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], arrays
- arrays [.NET Framework], usage guidelines
- empty arrays
ms.assetid: 66a1b3d8-6f3f-4715-b235-e1ff95e32d8e
ms.openlocfilehash: 11c1d23af4cf599ba632144634947520a1647ae7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95701388"
---
# <a name="arrays"></a><span data-ttu-id="c4adc-102">数组</span><span class="sxs-lookup"><span data-stu-id="c4adc-102">Arrays</span></span>

<span data-ttu-id="c4adc-103">✔️确实更喜欢在公共 Api 中对数组使用集合。</span><span class="sxs-lookup"><span data-stu-id="c4adc-103">✔️ DO prefer using collections over arrays in public APIs.</span></span> <span data-ttu-id="c4adc-104">" [集合](guidelines-for-collections.md) " 部分提供了有关如何在集合和数组之间进行选择的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c4adc-104">The [Collections](guidelines-for-collections.md) section provides details about how to choose between collections and arrays.</span></span>

 <span data-ttu-id="c4adc-105">❌ 不要使用只读数组字段。</span><span class="sxs-lookup"><span data-stu-id="c4adc-105">❌ DO NOT use read-only array fields.</span></span> <span data-ttu-id="c4adc-106">字段本身是只读的并且不能更改，但可以更改数组中的元素。</span><span class="sxs-lookup"><span data-stu-id="c4adc-106">The field itself is read-only and can't be changed, but elements in the array can be changed.</span></span>

 <span data-ttu-id="c4adc-107">✔️考虑使用交错数组而不是多维数组。</span><span class="sxs-lookup"><span data-stu-id="c4adc-107">✔️ CONSIDER using jagged arrays instead of multidimensional arrays.</span></span>

 <span data-ttu-id="c4adc-108">交错数组是具有同样数组的元素的数组。</span><span class="sxs-lookup"><span data-stu-id="c4adc-108">A jagged array is an array with elements that are also arrays.</span></span> <span data-ttu-id="c4adc-109">构成元素的数组可以是不同的大小，从而减少某些数据集的浪费空间， (例如，稀疏矩阵) 与多维数组相比。</span><span class="sxs-lookup"><span data-stu-id="c4adc-109">The arrays that make up the elements can be of different sizes, leading to less wasted space for some sets of data (e.g., sparse matrix) compared to multidimensional arrays.</span></span> <span data-ttu-id="c4adc-110">此外，CLR 还会优化交错数组的索引操作，因此，在某些情况下，它们可能会表现出更好的运行时性能。</span><span class="sxs-lookup"><span data-stu-id="c4adc-110">Furthermore, the CLR optimizes index operations on jagged arrays, so they might exhibit better runtime performance in some scenarios.</span></span>

 <span data-ttu-id="c4adc-111">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="c4adc-111">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="c4adc-112">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="c4adc-112">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="c4adc-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4adc-113">See also</span></span>

- <xref:System.Array>
- [<span data-ttu-id="c4adc-114">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="c4adc-114">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="c4adc-115">使用准则</span><span class="sxs-lookup"><span data-stu-id="c4adc-115">Usage Guidelines</span></span>](usage-guidelines.md)
