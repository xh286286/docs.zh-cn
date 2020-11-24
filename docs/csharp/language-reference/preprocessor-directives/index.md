---
description: C# 预处理器指令
title: C# 预处理器指令
ms.date: 07/20/2015
f1_keywords:
- cs.preprocessor
helpviewer_keywords:
- preprocessor directives [C#]
- keywords [C#], preprocessor directives
ms.assetid: f2406090-b244-4f7e-ab72-3698fefed724
ms.openlocfilehash: 1269522b2687b76292f7b796a4ffc8095f23442e
ms.sourcegitcommit: 30e9e11dfd90112b8eec6406186ba3533f21eba1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2020
ms.locfileid: "95099056"
---
# <a name="c-preprocessor-directives"></a><span data-ttu-id="b30c4-103">C# 预处理器指令</span><span class="sxs-lookup"><span data-stu-id="b30c4-103">C# preprocessor directives</span></span>

<span data-ttu-id="b30c4-104">本节介绍了以下 C# 预处理器指令：</span><span class="sxs-lookup"><span data-stu-id="b30c4-104">This section contains information about the following C# preprocessor directives:</span></span>

- [<span data-ttu-id="b30c4-105">#if</span><span class="sxs-lookup"><span data-stu-id="b30c4-105">#if</span></span>](./preprocessor-if.md)
- [<span data-ttu-id="b30c4-106">#else</span><span class="sxs-lookup"><span data-stu-id="b30c4-106">#else</span></span>](./preprocessor-else.md)
- [<span data-ttu-id="b30c4-107">#elif</span><span class="sxs-lookup"><span data-stu-id="b30c4-107">#elif</span></span>](./preprocessor-elif.md)
- [<span data-ttu-id="b30c4-108">#endif</span><span class="sxs-lookup"><span data-stu-id="b30c4-108">#endif</span></span>](./preprocessor-endif.md)
- [<span data-ttu-id="b30c4-109">#define</span><span class="sxs-lookup"><span data-stu-id="b30c4-109">#define</span></span>](./preprocessor-define.md)
- [<span data-ttu-id="b30c4-110">#undef</span><span class="sxs-lookup"><span data-stu-id="b30c4-110">#undef</span></span>](./preprocessor-undef.md)
- [<span data-ttu-id="b30c4-111">#warning</span><span class="sxs-lookup"><span data-stu-id="b30c4-111">#warning</span></span>](./preprocessor-warning.md)
- [<span data-ttu-id="b30c4-112">#error</span><span class="sxs-lookup"><span data-stu-id="b30c4-112">#error</span></span>](./preprocessor-error.md)
- [<span data-ttu-id="b30c4-113">#line</span><span class="sxs-lookup"><span data-stu-id="b30c4-113">#line</span></span>](./preprocessor-line.md)
- [<span data-ttu-id="b30c4-114">#nullable</span><span class="sxs-lookup"><span data-stu-id="b30c4-114">#nullable</span></span>](./preprocessor-nullable.md)
- [<span data-ttu-id="b30c4-115">#region</span><span class="sxs-lookup"><span data-stu-id="b30c4-115">#region</span></span>](./preprocessor-region.md)
- [<span data-ttu-id="b30c4-116">#endregion</span><span class="sxs-lookup"><span data-stu-id="b30c4-116">#endregion</span></span>](./preprocessor-endregion.md)
- [<span data-ttu-id="b30c4-117">#pragma</span><span class="sxs-lookup"><span data-stu-id="b30c4-117">#pragma</span></span>](./preprocessor-pragma.md)
- [<span data-ttu-id="b30c4-118">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="b30c4-118">#pragma warning</span></span>](./preprocessor-pragma-warning.md)
- [<span data-ttu-id="b30c4-119">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="b30c4-119">#pragma checksum</span></span>](./preprocessor-pragma-checksum.md)

<span data-ttu-id="b30c4-120">请参阅各个主题了解更多信息和示例。</span><span class="sxs-lookup"><span data-stu-id="b30c4-120">See the individual topics for more information and examples.</span></span>

<span data-ttu-id="b30c4-121">尽管编译器没有单独的预处理器，但本节中所述指令的处理方式与有预处理器时一样。</span><span class="sxs-lookup"><span data-stu-id="b30c4-121">Although the compiler doesn't have a separate preprocessor, the directives described in this section are processed as if there were one.</span></span> <span data-ttu-id="b30c4-122">这些指令用于帮助条件编译。</span><span class="sxs-lookup"><span data-stu-id="b30c4-122">They are used to help in conditional compilation.</span></span> <span data-ttu-id="b30c4-123">不同于 C 和 C++ 指令，不能使用这些指令来创建宏。</span><span class="sxs-lookup"><span data-stu-id="b30c4-123">Unlike C and C++ directives, you cannot use these directives to create macros.</span></span>

<span data-ttu-id="b30c4-124">预处理器指令必须是一行中唯一的说明。</span><span class="sxs-lookup"><span data-stu-id="b30c4-124">A preprocessor directive must be the only instruction on a line.</span></span>

## <a name="see-also"></a><span data-ttu-id="b30c4-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="b30c4-125">See also</span></span>

- [<span data-ttu-id="b30c4-126">C# 参考</span><span class="sxs-lookup"><span data-stu-id="b30c4-126">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b30c4-127">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="b30c4-127">C# Programming Guide</span></span>](../../programming-guide/index.md)
