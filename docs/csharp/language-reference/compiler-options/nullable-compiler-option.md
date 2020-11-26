---
description: -nullable（C# 编译器选项）
title: -nullable（C# 编译器选项）
author: IEvangelist
ms.author: dapine
ms.date: 06/04/2020
f1_keywords:
- /nullable
helpviewer_keywords:
- nullable compiler option [C#]
- /nullable compiler option [C#]
- -nullable compiler option [C#]
ms.openlocfilehash: 68857d0cb4d0cd1177506e0b7ce897d2cfc3aa5b
ms.sourcegitcommit: 30e9e11dfd90112b8eec6406186ba3533f21eba1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2020
ms.locfileid: "95099219"
---
# <a name="-nullable-c-compiler-options"></a><span data-ttu-id="1d57a-103">-nullable（C# 编译器选项）</span><span class="sxs-lookup"><span data-stu-id="1d57a-103">-nullable (C# Compiler Options)</span></span>

<span data-ttu-id="1d57a-104">使用“-nullable”选项可指定可为空上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-104">The **-nullable** option lets you specify the nullable context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d57a-105">语法</span><span class="sxs-lookup"><span data-stu-id="1d57a-105">Syntax</span></span>

```console
-nullable[+ | -]
-nullable:{enable | disable | warnings | annotations}
```

## <a name="arguments"></a><span data-ttu-id="1d57a-106">自变量</span><span class="sxs-lookup"><span data-stu-id="1d57a-106">Arguments</span></span>

<span data-ttu-id="1d57a-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="1d57a-107">`+` &#124; `-`</span></span>  
<span data-ttu-id="1d57a-108">指定 `+` 或“-nullable”会使编译器启用可为空上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-108">Specifying `+`, or **-nullable**, causes the compiler to enable nullable context.</span></span> <span data-ttu-id="1d57a-109">指定 `-`（等效于未指定“-nullable”）会禁用可为空上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-109">Specifying `-`, which is in effect if you don't specify **-nullable**, disables nullable context.</span></span>

<span data-ttu-id="1d57a-110">`enable` &#124；`disable` &#124；`warnings` &#124；`annotations`</span><span class="sxs-lookup"><span data-stu-id="1d57a-110">`enable` &#124; `disable` &#124; `warnings` &#124; `annotations`</span></span>  
<span data-ttu-id="1d57a-111">指定可为空上下文选项。</span><span class="sxs-lookup"><span data-stu-id="1d57a-111">Specifies the nullable context option.</span></span> <span data-ttu-id="1d57a-112">与 `+` 或 `-` 类似，若要启用和禁用，只需允许更细粒度的可为空上下文特异性。</span><span class="sxs-lookup"><span data-stu-id="1d57a-112">Similar to `+` or `-`, to enable and disable, but allows for more granularity of nullable context specificity.</span></span> <span data-ttu-id="1d57a-113">`enable` 参数（等效于指定 -nullable）会启用可为空的上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-113">The `enable` argument, which is in effect the same as if you specify **-nullable**, enables the nullable context.</span></span> <span data-ttu-id="1d57a-114">指定 `disable` 将禁用可为空上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-114">Specifying `disable` will disable nullable context.</span></span> <span data-ttu-id="1d57a-115">如果提供 `warnings` 参数 -nullable:warnings，则将启用可为空警告上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-115">When providing the `warnings` argument, **-nullable:warnings**, the nullable warning context is enabled.</span></span> <span data-ttu-id="1d57a-116">如果指定 `annotations` 参数 -nullable:annotations，则将启用可为空注释上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-116">When specifying the `annotations` argument, **-nullable:annotations**, the nullable annotation context is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d57a-117">备注</span><span class="sxs-lookup"><span data-stu-id="1d57a-117">Remarks</span></span>

<span data-ttu-id="1d57a-118">流分析用于在可执行代码中推断变量的为空性。</span><span class="sxs-lookup"><span data-stu-id="1d57a-118">Flow analysis is used to infer the nullability of variables within executable code.</span></span> <span data-ttu-id="1d57a-119">推断出的变量的为空性与变量声明的为空性无关。</span><span class="sxs-lookup"><span data-stu-id="1d57a-119">The inferred nullability of a variable is independent of the variable's declared nullability.</span></span> <span data-ttu-id="1d57a-120">即使有条件地省略方法调用，也会对其进行分析。</span><span class="sxs-lookup"><span data-stu-id="1d57a-120">Method calls are analyzed even when they're conditionally omitted.</span></span> <span data-ttu-id="1d57a-121">例如，发布模式下的 <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="1d57a-121">For instance, <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> in release mode.</span></span>

<span data-ttu-id="1d57a-122">采用以下特性进行注释的方法调用也将影响流分析：</span><span class="sxs-lookup"><span data-stu-id="1d57a-122">Invocation of methods annotated with the following attributes will also affect flow analysis:</span></span>

- <span data-ttu-id="1d57a-123">简单的前提条件：<xref:System.Diagnostics.CodeAnalysis.AllowNullAttribute> 和 <xref:System.Diagnostics.CodeAnalysis.DisallowNullAttribute></span><span class="sxs-lookup"><span data-stu-id="1d57a-123">Simple pre-conditions: <xref:System.Diagnostics.CodeAnalysis.AllowNullAttribute> and <xref:System.Diagnostics.CodeAnalysis.DisallowNullAttribute></span></span>
- <span data-ttu-id="1d57a-124">简单的后置条件：<xref:System.Diagnostics.CodeAnalysis.MaybeNullAttribute> 和 <xref:System.Diagnostics.CodeAnalysis.NotNullAttribute></span><span class="sxs-lookup"><span data-stu-id="1d57a-124">Simple post-conditions: <xref:System.Diagnostics.CodeAnalysis.MaybeNullAttribute> and <xref:System.Diagnostics.CodeAnalysis.NotNullAttribute></span></span>
- <span data-ttu-id="1d57a-125">有条件后置条件：<xref:System.Diagnostics.CodeAnalysis.MaybeNullWhenAttribute> 和 <xref:System.Diagnostics.CodeAnalysis.NotNullWhenAttribute></span><span class="sxs-lookup"><span data-stu-id="1d57a-125">Conditional post-conditions: <xref:System.Diagnostics.CodeAnalysis.MaybeNullWhenAttribute> and <xref:System.Diagnostics.CodeAnalysis.NotNullWhenAttribute></span></span>
- <span data-ttu-id="1d57a-126"><xref:System.Diagnostics.CodeAnalysis.DoesNotReturnIfAttribute>（例如 <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> 的 `DoesNotReturnIf(false)`）和 <xref:System.Diagnostics.CodeAnalysis.DoesNotReturnAttribute></span><span class="sxs-lookup"><span data-stu-id="1d57a-126"><xref:System.Diagnostics.CodeAnalysis.DoesNotReturnIfAttribute> (for example, `DoesNotReturnIf(false)` for <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>) and <xref:System.Diagnostics.CodeAnalysis.DoesNotReturnAttribute></span></span>
- <xref:System.Diagnostics.CodeAnalysis.NotNullIfNotNullAttribute>
- <span data-ttu-id="1d57a-127">成员后置条件：<xref:System.Diagnostics.CodeAnalysis.MemberNotNullAttribute.%23ctor(System.String)> 和 <xref:System.Diagnostics.CodeAnalysis.MemberNotNullAttribute.%23ctor(System.String[])></span><span class="sxs-lookup"><span data-stu-id="1d57a-127">Member post-conditions: <xref:System.Diagnostics.CodeAnalysis.MemberNotNullAttribute.%23ctor(System.String)> and <xref:System.Diagnostics.CodeAnalysis.MemberNotNullAttribute.%23ctor(System.String[])></span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d57a-128">全局可为空上下文不适用于生成的代码文件。</span><span class="sxs-lookup"><span data-stu-id="1d57a-128">The global nullable context does not apply for generated code files.</span></span> <span data-ttu-id="1d57a-129">无论此设置如何，都会针对标记为“已生成”的任何源文件禁用可为空上下文。</span><span class="sxs-lookup"><span data-stu-id="1d57a-129">Regardless of this setting, the nullable context is *disabled* for any source file marked as generated.</span></span> <span data-ttu-id="1d57a-130">可采用四种方法将文件标记为“已生成”：</span><span class="sxs-lookup"><span data-stu-id="1d57a-130">There are four ways a file is marked as generated:</span></span>
>
> 1. <span data-ttu-id="1d57a-131">在 .editorconfig 中，在应用于该文件的部分中指定 `generated_code = true`。</span><span class="sxs-lookup"><span data-stu-id="1d57a-131">In the .editorconfig, specify `generated_code = true` in a section that applies to that file.</span></span>
> 1. <span data-ttu-id="1d57a-132">将 `<auto-generated>` 或 `<auto-generated/>` 放在文件顶部的注释中。</span><span class="sxs-lookup"><span data-stu-id="1d57a-132">Put `<auto-generated>` or `<auto-generated/>` in a comment at the top of the file.</span></span> <span data-ttu-id="1d57a-133">它可以位于该注释中的任意行上，但注释块必须是该文件中的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="1d57a-133">It can be on any line in that comment, but the comment block must be the first element in the file.</span></span>
> 1. <span data-ttu-id="1d57a-134">文件名以 TemporaryGeneratedFile_ 开头</span><span class="sxs-lookup"><span data-stu-id="1d57a-134">Start the file name with *TemporaryGeneratedFile_*</span></span>
> 1. <span data-ttu-id="1d57a-135">文件名用以 .designer.cs、.generated.cs、.g.cs 或 .g.i.cs 结尾   。</span><span class="sxs-lookup"><span data-stu-id="1d57a-135">End the file name with *.designer.cs*, *.generated.cs*, *.g.cs*, or *.g.i.cs*.</span></span>
>
> <span data-ttu-id="1d57a-136">生成器可以选择使用 [`#nullable`](../preprocessor-directives/preprocessor-nullable.md) 预处理器指令。</span><span class="sxs-lookup"><span data-stu-id="1d57a-136">Generators can opt-in using the [`#nullable`](../preprocessor-directives/preprocessor-nullable.md) preprocessor directive.</span></span>

### <a name="to-set-this-compiler-option-in-a-project"></a><span data-ttu-id="1d57a-137">在项目中设置此编译器选项</span><span class="sxs-lookup"><span data-stu-id="1d57a-137">To set this compiler option in a project</span></span>

<span data-ttu-id="1d57a-138">编辑 .csproj 文件，将 `<Nullable>` 标记添加到 `Project/PropertyGroup` 层次结构中：</span><span class="sxs-lookup"><span data-stu-id="1d57a-138">Edit the *.csproj* file to add the `<Nullable>` tag within a `Project/PropertyGroup` hierarchy:</span></span>

```xml
<Project Sdk="...">

  <PropertyGroup>
    <Nullable>enable</Nullable>
  </PropertyGroup>

</Project>
```

## <a name="see-also"></a><span data-ttu-id="1d57a-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d57a-139">See also</span></span>

- [<span data-ttu-id="1d57a-140">C# 编译器选项</span><span class="sxs-lookup"><span data-stu-id="1d57a-140">C# Compiler Options</span></span>](./index.md)
- [<span data-ttu-id="1d57a-141">`#nullable` 预处理器指令</span><span class="sxs-lookup"><span data-stu-id="1d57a-141">`#nullable` preprocessor directive</span></span>](../preprocessor-directives/preprocessor-nullable.md)
- [<span data-ttu-id="1d57a-142">可为空引用类型</span><span class="sxs-lookup"><span data-stu-id="1d57a-142">Nullable reference types</span></span>](../../nullable-references.md)
