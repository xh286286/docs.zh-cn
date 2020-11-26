---
description: '#可为空 - C# 参考'
title: '#可为空 - C# 参考'
ms.date: 11/18/2020
f1_keywords:
- '#nullable'
helpviewer_keywords:
- '#nullable directive [C#]'
ms.openlocfilehash: 4c114a09f29769fcc824bcdabdc1d523e33f199d
ms.sourcegitcommit: 30e9e11dfd90112b8eec6406186ba3533f21eba1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2020
ms.locfileid: "95099444"
---
# <a name="nullable-c-reference"></a><span data-ttu-id="c364f-103">#nullable（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="c364f-103">#nullable (C# Reference)</span></span>

<span data-ttu-id="c364f-104">`#nullable` 预处理器指令将设置可为空注释上下文和可为空警告上下文 。</span><span class="sxs-lookup"><span data-stu-id="c364f-104">The `#nullable` preprocessor directive sets the *nullable annotation context* and *nullable warning context*.</span></span> <span data-ttu-id="c364f-105">此指令控制是否可为空注释是否有效，以及是否给出为 Null 性警告。</span><span class="sxs-lookup"><span data-stu-id="c364f-105">This directive controls whether nullable annotations have effect, and whether nullability warnings are given.</span></span> <span data-ttu-id="c364f-106">每个上下文要么处于已禁用状态，要么处于已启用状态 。</span><span class="sxs-lookup"><span data-stu-id="c364f-106">Each context is either *disabled* or *enabled*.</span></span>

<span data-ttu-id="c364f-107">可在项目级别（C# 源代码之外）指定这两个上下文。</span><span class="sxs-lookup"><span data-stu-id="c364f-107">Both contexts can be specified at the project level (outside of C# source code).</span></span> <span data-ttu-id="c364f-108">`#nullable` 指令控制注释和警告上下文，并优先于项目级设置。</span><span class="sxs-lookup"><span data-stu-id="c364f-108">The `#nullable` directive controls the annotation and warning contexts and takes precedence over the project-level settings.</span></span> <span data-ttu-id="c364f-109">指令会设置其控制的上下文，直到另一个指令替代它，或直到源文件结束为止。</span><span class="sxs-lookup"><span data-stu-id="c364f-109">A directive sets the context(s) it controls until another directive overrides it, or until the end of the source file.</span></span>

<span data-ttu-id="c364f-110">指令的效果如下所示：</span><span class="sxs-lookup"><span data-stu-id="c364f-110">The effect of the directives is as follows:</span></span>

- <span data-ttu-id="c364f-111">`#nullable disable`：将可为空注释和警告上下文设置为“已禁用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-111">`#nullable disable`: Sets the nullable annotation and warning contexts to *disabled*.</span></span>
- <span data-ttu-id="c364f-112">`#nullable enable`：将可为空注释和警告上下文设置为“已启用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-112">`#nullable enable`: Sets the nullable annotation and warning contexts to *enabled*.</span></span>
- <span data-ttu-id="c364f-113">`#nullable restore`：将可为空注释和警告上下文还原为项目设置。</span><span class="sxs-lookup"><span data-stu-id="c364f-113">`#nullable restore`: Restores the nullable annotation and warning contexts to project settings.</span></span>
- <span data-ttu-id="c364f-114">`#nullable disable annotations`：将可为空注释上下文设置为“已禁用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-114">`#nullable disable annotations`: Sets the nullable annotation context to *disabled*.</span></span>
- <span data-ttu-id="c364f-115">`#nullable enable annotations`：将可为空注释上下文设置为“已启用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-115">`#nullable enable annotations`: Sets the nullable annotation context to *enabled*.</span></span>
- <span data-ttu-id="c364f-116">`#nullable restore annotations`：将可为空注释上下文还原为项目设置。</span><span class="sxs-lookup"><span data-stu-id="c364f-116">`#nullable restore annotations`: Restores the nullable annotation context to project settings.</span></span>
- <span data-ttu-id="c364f-117">`#nullable disable warnings`：将可为空警告上下文设置为“已禁用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-117">`#nullable disable warnings`: Sets the nullable warning context to *disabled*.</span></span>
- <span data-ttu-id="c364f-118">`#nullable enable warnings`：将可为空警告上下文设置为“已启用”。</span><span class="sxs-lookup"><span data-stu-id="c364f-118">`#nullable enable warnings`: Sets the nullable warning context to *enabled*.</span></span>
- <span data-ttu-id="c364f-119">`#nullable restore warnings`：将可为空警告上下文还原为项目设置。</span><span class="sxs-lookup"><span data-stu-id="c364f-119">`#nullable restore warnings`: Restores the nullable warning context to project settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="c364f-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c364f-120">See also</span></span>

- [<span data-ttu-id="c364f-121">C# 参考</span><span class="sxs-lookup"><span data-stu-id="c364f-121">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="c364f-122">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="c364f-122">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="c364f-123">C# 预处理器指令</span><span class="sxs-lookup"><span data-stu-id="c364f-123">C# Preprocessor Directives</span></span>](./index.md)
