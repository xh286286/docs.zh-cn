---
title: 配置代码分析规则
description: 了解如何在分析器配置文件中配置代码分析规则。
ms.date: 09/24/2020
ms.topic: conceptual
no-loc:
- EditorConfig
ms.openlocfilehash: af2ebb74786f0ae884ffee4636765cae43fcb23f
ms.sourcegitcommit: 97405ed212f69b0a32faa66a5d5fae7e76628b68
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "96590485"
---
# <a name="configuration-options-for-code-analysis"></a><span data-ttu-id="e6da7-103">代码分析的配置选项</span><span class="sxs-lookup"><span data-stu-id="e6da7-103">Configuration options for code analysis</span></span>

<span data-ttu-id="e6da7-104">代码分析规则具有各种配置选项。</span><span class="sxs-lookup"><span data-stu-id="e6da7-104">Code analysis rules have various configuration options.</span></span> <span data-ttu-id="e6da7-105">这些选项在 [分析器配置文件](configuration-files.md) 中使用语法指定为键值对 `<option key> = <option value>` 。</span><span class="sxs-lookup"><span data-stu-id="e6da7-105">These options are specified as key-value pairs in an [analyzer configuration file](configuration-files.md) using the syntax `<option key> = <option value>`.</span></span>

<span data-ttu-id="e6da7-106">您要配置的最常见的选项是规则的严重性。</span><span class="sxs-lookup"><span data-stu-id="e6da7-106">The most common option you'll configure is a rule's severity.</span></span> <span data-ttu-id="e6da7-107">您可以为所有分析器规则（包括 [代码质量规则](quality-rules/index.md) 和 [代码样式规则](style-rules/index.md)）配置严重级别。</span><span class="sxs-lookup"><span data-stu-id="e6da7-107">You can configure severity level for all analyzer rules, including [code quality rules](quality-rules/index.md) and [code style rules](style-rules/index.md).</span></span>

<span data-ttu-id="e6da7-108">你还可以配置其他选项以自定义规则行为：</span><span class="sxs-lookup"><span data-stu-id="e6da7-108">You can also configure additional options to customize rule behavior:</span></span>

- <span data-ttu-id="e6da7-109">代码质量规则具有 [其他](code-quality-rule-options.md) 用于配置行为的选项，例如，要将规则应用到的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="e6da7-109">Code quality rules have [additional options](code-quality-rule-options.md) to configure behavior, such as which method names a rule should apply to.</span></span>
- <span data-ttu-id="e6da7-110">代码样式规则具有 [自定义代码样式选项](code-style-rule-options.md)。</span><span class="sxs-lookup"><span data-stu-id="e6da7-110">Code style rules have [custom code style options](code-style-rule-options.md).</span></span>
- <span data-ttu-id="e6da7-111">第三方分析器规则可以定义自己的配置选项，其中包含自定义的键名和值格式。</span><span class="sxs-lookup"><span data-stu-id="e6da7-111">Third party analyzer rules can define their own configuration options, with custom key names and value formats.</span></span>

<span data-ttu-id="e6da7-112">在 [分析器配置文件](configuration-files.md) 中配置特定规则严重性的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="e6da7-112">The syntax for configuring a specific rule's severity in an [analyzer configuration file](configuration-files.md) is as follows:</span></span>

```ini
dotnet_diagnostic.<rule ID>.severity = <severity>
```

## <a name="general-options"></a><span data-ttu-id="e6da7-113">常规选项</span><span class="sxs-lookup"><span data-stu-id="e6da7-113">General options</span></span>

<span data-ttu-id="e6da7-114">这些选项适用于整个代码分析。</span><span class="sxs-lookup"><span data-stu-id="e6da7-114">These options apply to code analysis as a whole.</span></span> <span data-ttu-id="e6da7-115">它们不能仅应用于一个或一组规则。</span><span class="sxs-lookup"><span data-stu-id="e6da7-115">They cannot be applied only to a single rule or set of rules.</span></span>

### <a name="exclude-generated-code"></a><span data-ttu-id="e6da7-116">排除生成的代码</span><span class="sxs-lookup"><span data-stu-id="e6da7-116">Exclude generated code</span></span>

<span data-ttu-id="e6da7-117">你可以通过将 `generated_code = true | false` 条目添加到 [配置文件](configuration-files.md)，将其他文件和文件夹作为生成的代码进行配置。</span><span class="sxs-lookup"><span data-stu-id="e6da7-117">You can configure additional files and folders to be treated as generated code by adding a `generated_code = true | false` entry to your [configuration file](configuration-files.md).</span></span> <span data-ttu-id="e6da7-118">.NET 代码分析器警告在生成的代码文件（如设计器生成的文件）上不有用，用户无法编辑这些文件来修复任何冲突。</span><span class="sxs-lookup"><span data-stu-id="e6da7-118">.NET code analyzer warnings aren't useful on generated code files, such as designer-generated files, which users can't edit to fix any violations.</span></span> <span data-ttu-id="e6da7-119">在大多数情况下，代码分析器会跳过生成的代码文件，而不报告这些文件的冲突。</span><span class="sxs-lookup"><span data-stu-id="e6da7-119">In most cases, code analyzers skip generated code files and don't report violations on these files.</span></span>

<span data-ttu-id="e6da7-120">默认情况下，具有特定文件扩展名或自动生成的文件标头的文件被视为生成的代码文件。</span><span class="sxs-lookup"><span data-stu-id="e6da7-120">By default, files with certain file extensions or auto-generated file headers are treated as generated code files.</span></span> <span data-ttu-id="e6da7-121">例如，以或结尾的文件名被 `.designer.cs` `.generated.cs` 视为生成的代码。</span><span class="sxs-lookup"><span data-stu-id="e6da7-121">For example, a file name ending with `.designer.cs` or `.generated.cs` is considered generated code.</span></span> <span data-ttu-id="e6da7-122">此配置选项允许您指定其他命名模式。</span><span class="sxs-lookup"><span data-stu-id="e6da7-122">This configuration option lets you specify additional naming patterns.</span></span>

<span data-ttu-id="e6da7-123">例如，若要将名称以结尾的所有文件视为 `.MyGenerated.cs` 生成的代码，请添加以下条目：</span><span class="sxs-lookup"><span data-stu-id="e6da7-123">For example, to treat all files whose name ends with `.MyGenerated.cs` as generated code, add the following entry:</span></span>

```ini
[*.MyGenerated.cs]
generated_code = true
```

## <a name="rule-specific-options"></a><span data-ttu-id="e6da7-124">特定于规则的选项</span><span class="sxs-lookup"><span data-stu-id="e6da7-124">Rule-specific options</span></span>

<span data-ttu-id="e6da7-125">特定于规则的选项可应用于单个规则、一组规则或所有规则。</span><span class="sxs-lookup"><span data-stu-id="e6da7-125">Rule-specific options can be applied to a single rule, a set of rules, or all rules.</span></span> <span data-ttu-id="e6da7-126">特定于规则的选项包括：</span><span class="sxs-lookup"><span data-stu-id="e6da7-126">The rule-specific options include:</span></span>

- [<span data-ttu-id="e6da7-127">规则严重性级别</span><span class="sxs-lookup"><span data-stu-id="e6da7-127">Rule severity level</span></span>](#severity-level)
- [<span data-ttu-id="e6da7-128">特定于 *代码质量规则的* 选项</span><span class="sxs-lookup"><span data-stu-id="e6da7-128">Options specific to *code-quality* rules</span></span>](code-quality-rule-options.md)

### <a name="severity-level"></a><span data-ttu-id="e6da7-129">严重性级别</span><span class="sxs-lookup"><span data-stu-id="e6da7-129">Severity level</span></span>

<span data-ttu-id="e6da7-130">下表显示了可为所有分析器规则（包括 [代码质量](quality-rules/index.md) 和 [代码样式](style-rules/index.md) 规则）配置的不同规则严重性。</span><span class="sxs-lookup"><span data-stu-id="e6da7-130">The following table shows the different rule severities that you can configure for all analyzer rules, including [code quality](quality-rules/index.md) and [code style](style-rules/index.md) rules.</span></span>

| <span data-ttu-id="e6da7-131">严重性</span><span class="sxs-lookup"><span data-stu-id="e6da7-131">Severity</span></span> | <span data-ttu-id="e6da7-132">生成时行为</span><span class="sxs-lookup"><span data-stu-id="e6da7-132">Build-time behavior</span></span> |
|-|-|
| `error` | <span data-ttu-id="e6da7-133">冲突显示为生成 *错误* 并导致生成失败。</span><span class="sxs-lookup"><span data-stu-id="e6da7-133">Violations appear as build *errors* and cause builds to fail.</span></span>|
| `warning` | <span data-ttu-id="e6da7-134">冲突显示为生成 *警告* ，但不会导致生成失败 (除非您将选项设置为 "将警告视为错误") 。</span><span class="sxs-lookup"><span data-stu-id="e6da7-134">Violations appear as build *warnings* but do not cause builds to fail (unless you have an option set to treat warnings as errors).</span></span> |
| `suggestion` | <span data-ttu-id="e6da7-135">冲突显示为生成 *消息* ，在 VISUAL Studio IDE 中显示为建议。</span><span class="sxs-lookup"><span data-stu-id="e6da7-135">Violations appear as build *messages* and as suggestions in the Visual Studio IDE.</span></span> |
| `silent` | <span data-ttu-id="e6da7-136">冲突对用户不可见。</span><span class="sxs-lookup"><span data-stu-id="e6da7-136">Violations aren't visible to the user.</span></span> |
| `none` | <span data-ttu-id="e6da7-137">完全禁止显示规则。</span><span class="sxs-lookup"><span data-stu-id="e6da7-137">Rule is suppressed completely.</span></span> |
| `default` | <span data-ttu-id="e6da7-138">使用规则的默认严重性。</span><span class="sxs-lookup"><span data-stu-id="e6da7-138">The default severity of the rule is used.</span></span> |

> [!TIP]
> <span data-ttu-id="e6da7-139">有关 Visual Studio 中规则严重性的详细信息，请参阅 [严重性级别](/visualstudio/ide/editorconfig-language-conventions#severity-levels)。</span><span class="sxs-lookup"><span data-stu-id="e6da7-139">For information about how rule severities surface in Visual Studio, see [Severity levels](/visualstudio/ide/editorconfig-language-conventions#severity-levels).</span></span>

#### <a name="scope"></a><span data-ttu-id="e6da7-140">范围</span><span class="sxs-lookup"><span data-stu-id="e6da7-140">Scope</span></span>

<span data-ttu-id="e6da7-141">若要设置单个规则的规则严重性，请使用以下语法。</span><span class="sxs-lookup"><span data-stu-id="e6da7-141">To set the rule severity for a single rule, use the following syntax.</span></span>

```ini
dotnet_diagnostic.<rule ID>.severity = <severity value>
```

<span data-ttu-id="e6da7-142">若要为某一类别的分析器规则设置默认规则严重性，请使用以下语法。</span><span class="sxs-lookup"><span data-stu-id="e6da7-142">To set the default rule severity for a category of analyzer rules, use the following syntax.</span></span>

```ini
dotnet_analyzer_diagnostic.category-<rule category>.severity = <severity value>
```

<span data-ttu-id="e6da7-143">若要为所有分析器规则设置默认规则严重性，请使用以下语法。</span><span class="sxs-lookup"><span data-stu-id="e6da7-143">To set the default rule severity for all analyzer rules, use the following syntax.</span></span>

```ini
dotnet_analyzer_diagnostic.severity = <severity value>
```

#### <a name="precedence"></a><span data-ttu-id="e6da7-144">优先级</span><span class="sxs-lookup"><span data-stu-id="e6da7-144">Precedence</span></span>

<span data-ttu-id="e6da7-145">如果有多个可应用于同一规则 ID 的严重性配置项，将按以下顺序选择优先级：</span><span class="sxs-lookup"><span data-stu-id="e6da7-145">If you have multiple severity configuration entries that can be applied to the same rule ID, precedence is chosen in the following order:</span></span>

- <span data-ttu-id="e6da7-146">单个规则按 ID 列出的条目优先于类别的条目。</span><span class="sxs-lookup"><span data-stu-id="e6da7-146">An entry for an individual rule by ID takes precedence over an entry for a category.</span></span>
- <span data-ttu-id="e6da7-147">类别的条目优先于所有分析器规则条目。</span><span class="sxs-lookup"><span data-stu-id="e6da7-147">An entry for a category takes precedence over an entry for all analyzer rules.</span></span>

<span data-ttu-id="e6da7-148">请考虑以下示例，其中 [CA1822](/visualstudio/code-quality/ca1822) 的类别为 "Performance"：</span><span class="sxs-lookup"><span data-stu-id="e6da7-148">Consider the following example, where [CA1822](/visualstudio/code-quality/ca1822) has the category "Performance":</span></span>

```ini
[*.cs]
dotnet_diagnostic.CA1822.severity = error
dotnet_analyzer_diagnostic.category-performance.severity = warning
dotnet_analyzer_diagnostic.severity = suggestion
```

<span data-ttu-id="e6da7-149">在前面的示例中，所有三个严重性条目都适用于 CA1822。</span><span class="sxs-lookup"><span data-stu-id="e6da7-149">In the preceding example, all three severity entries are applicable to CA1822.</span></span> <span data-ttu-id="e6da7-150">但是，使用指定的优先规则，基于第一个规则 ID 的条目将在下一条目上入选。</span><span class="sxs-lookup"><span data-stu-id="e6da7-150">However, using the specified precedence rules, the first rule ID-based entry wins over the next entries.</span></span> <span data-ttu-id="e6da7-151">在此示例中，CA1822 将具有有效的严重性 `error` 。</span><span class="sxs-lookup"><span data-stu-id="e6da7-151">In this example, CA1822 will have an effective severity of `error`.</span></span> <span data-ttu-id="e6da7-152">"性能" 类别中的所有其他规则都具有严重性 `warning` 。</span><span class="sxs-lookup"><span data-stu-id="e6da7-152">All other rules within the "Performance" category will have a severity of `warning`.</span></span>

<span data-ttu-id="e6da7-153">有关如何确定文件间优先级的信息，请参阅 [配置文件的优先级部分](configuration-files.md#precedence)。</span><span class="sxs-lookup"><span data-stu-id="e6da7-153">For information about how inter-file precedence is decided, see the [Precedence section of the Configuration files article](configuration-files.md#precedence).</span></span>
