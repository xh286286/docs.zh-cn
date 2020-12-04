---
title: 代码样式格式规则
description: 了解用于设置缩进、空格和新行的代码样式规则。
ms.date: 09/25/2020
ms.topic: reference
author: gewarren
ms.author: gewarren
dev_langs:
- CSharp
- VB
f1_keywords:
- IDE0055
- formatting rules
helpviewer_keywords:
- IDE0055
- formatting code style rules [EditorConfig]
- formatting rules
- EditorConfig formatting conventions
ms.openlocfilehash: 61e6f6a6afdc6aaf9710eef3143af8ae700ef612
ms.sourcegitcommit: 636af37170ae75a11c4f7d1ecd770820e7dfe7bd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/07/2020
ms.locfileid: "96590513"
---
# <a name="formatting-rules"></a><span data-ttu-id="9971c-103">格式设置规则</span><span class="sxs-lookup"><span data-stu-id="9971c-103">Formatting rules</span></span>

<span data-ttu-id="9971c-104">格式设置规则会影响 .NET 编程语言构造的缩进、空格和新行的对齐方式。</span><span class="sxs-lookup"><span data-stu-id="9971c-104">Formatting rules affect how indentation, spaces, and new lines are aligned around .NET programming language constructs.</span></span> <span data-ttu-id="9971c-105">这些规则分为以下几类：</span><span class="sxs-lookup"><span data-stu-id="9971c-105">The rules fall into the following categories:</span></span>

- <span data-ttu-id="9971c-106">[.Net 格式规则](#net-formatting-rules)：适用于 c # 和 Visual Basic 的规则。</span><span class="sxs-lookup"><span data-stu-id="9971c-106">[.NET formatting rules](#net-formatting-rules): Rules that apply to both C# and Visual Basic.</span></span> <span data-ttu-id="9971c-107">这些规则的 EditorConfig 选项名称以前缀开头 `dotnet_` 。</span><span class="sxs-lookup"><span data-stu-id="9971c-107">The EditorConfig option names for these rules start with `dotnet_` prefix.</span></span>
- <span data-ttu-id="9971c-108">[C # 格式设置规则](#c-formatting-rules)：仅特定于 c # 语言的规则。</span><span class="sxs-lookup"><span data-stu-id="9971c-108">[C# formatting rules](#c-formatting-rules): Rules that are specific to C# language only.</span></span> <span data-ttu-id="9971c-109">这些规则的 EditorConfig 选项名称以前缀开头 `csharp_` 。</span><span class="sxs-lookup"><span data-stu-id="9971c-109">The EditorConfig option names for these rules start with `csharp_` prefix.</span></span>

## <a name="rule-id-ide0055-fix-formatting"></a><span data-ttu-id="9971c-110">规则 ID： "IDE0055" (修复格式设置) </span><span class="sxs-lookup"><span data-stu-id="9971c-110">Rule ID: "IDE0055" (Fix formatting)</span></span>

<span data-ttu-id="9971c-111">所有格式设置选项都具有规则 ID `IDE0055` 和标题 `Fix formatting` 。</span><span class="sxs-lookup"><span data-stu-id="9971c-111">All formatting options have rule ID `IDE0055` and title `Fix formatting`.</span></span> <span data-ttu-id="9971c-112">使用以下配置行在 EditorConfig 文件中设置格式设置冲突的严重性。</span><span class="sxs-lookup"><span data-stu-id="9971c-112">Set the severity of a formatting violation in an EditorConfig file using the following configuration line.</span></span>

```ini
dotnet_diagnostic.IDE0055.severity = <severity value>
```

<span data-ttu-id="9971c-113">严重性值必须是 `warning` 或 `error` 才能 [在生成时强制执行](../overview.md#code-style-analysis)。</span><span class="sxs-lookup"><span data-stu-id="9971c-113">The severity value must be `warning` or `error` to be [enforced on build](../overview.md#code-style-analysis).</span></span> <span data-ttu-id="9971c-114">对于所有可能的严重性值，请参阅 [严重性级别](../configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="9971c-114">For all possible severity values, see [severity level](../configuration-options.md#severity-level).</span></span>

## <a name="option-format"></a><span data-ttu-id="9971c-115">选项格式</span><span class="sxs-lookup"><span data-stu-id="9971c-115">Option format</span></span>

<span data-ttu-id="9971c-116">格式设置规则的选项可在 EditorConfig 文件中指定，格式如下：</span><span class="sxs-lookup"><span data-stu-id="9971c-116">Options for formatting rules can be specified in an EditorConfig file with the following format:</span></span>

`rule_name = value`

<span data-ttu-id="9971c-117">对于许多规则，可为 `value` 指定 `true`（以此样式为首选项）或 `false`（不以此样式为首选项）。</span><span class="sxs-lookup"><span data-stu-id="9971c-117">For many rules, you specify either `true` (prefer this style) or `false` (do not prefer this style) for `value`.</span></span> <span data-ttu-id="9971c-118">对于其他规则，可指定值（如 `flush_left` 或 `before_and_after`）来说明在什么时间以及在什么位置应用此规则。</span><span class="sxs-lookup"><span data-stu-id="9971c-118">For other rules, you specify a value such as `flush_left` or `before_and_after` to describe when and where to apply the rule.</span></span> <span data-ttu-id="9971c-119">不需要指定严重性。</span><span class="sxs-lookup"><span data-stu-id="9971c-119">You don't specify a severity.</span></span>

## <a name="net-formatting-rules"></a><span data-ttu-id="9971c-120">.NET 格式设置规则</span><span class="sxs-lookup"><span data-stu-id="9971c-120">.NET formatting rules</span></span>

<span data-ttu-id="9971c-121">本节中的格式设置规则适用于 c # 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="9971c-121">The formatting rules in this section apply to both C# and Visual Basic.</span></span>

- [<span data-ttu-id="9971c-122">组织 using</span><span class="sxs-lookup"><span data-stu-id="9971c-122">Organize usings</span></span>](#organize-using-directives)
  - <span data-ttu-id="9971c-123">dotnet_sort_system_directives_first</span><span class="sxs-lookup"><span data-stu-id="9971c-123">dotnet_sort_system_directives_first</span></span>
  - <span data-ttu-id="9971c-124">dotnet_separate_import_directive_groups</span><span class="sxs-lookup"><span data-stu-id="9971c-124">dotnet_separate_import_directive_groups</span></span>

### <a name="organize-using-directives"></a><span data-ttu-id="9971c-125">组织 using 指令</span><span class="sxs-lookup"><span data-stu-id="9971c-125">Organize using directives</span></span>

<span data-ttu-id="9971c-126">这些格式设置规则与 `using` 指令和 `Imports` 语句的排序和显示有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-126">These formatting rules concern the sorting and display of `using` directives and `Imports` statements.</span></span>

<span data-ttu-id="9971c-127">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-127">Example *.editorconfig* file:</span></span>

```ini
# .NET formatting rules
[*.{cs,vb}]
dotnet_sort_system_directives_first = true
dotnet_separate_import_directive_groups = true
```

#### <a name="dotnet_sort_system_directives_first"></a><span data-ttu-id="9971c-128">dotnet\_sort\_system\_directives_first</span><span class="sxs-lookup"><span data-stu-id="9971c-128">dotnet\_sort\_system\_directives_first</span></span>

|<span data-ttu-id="9971c-129">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-129">Property</span></span>|<span data-ttu-id="9971c-130">值</span><span class="sxs-lookup"><span data-stu-id="9971c-130">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-131">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-131">**Option name**</span></span> | <span data-ttu-id="9971c-132">dotnet_sort_system_directives_first</span><span class="sxs-lookup"><span data-stu-id="9971c-132">dotnet_sort_system_directives_first</span></span> |
| <span data-ttu-id="9971c-133">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-133">**Applicable languages**</span></span> | <span data-ttu-id="9971c-134">C# 和 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9971c-134">C# and Visual Basic</span></span> |
| <span data-ttu-id="9971c-135">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-135">**Introduced version**</span></span> | <span data-ttu-id="9971c-136">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-136">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-137">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-137">**Option values**</span></span> | <span data-ttu-id="9971c-138">`true` - `System.*` `using` 按字母顺序排序指令，并将其放在其他 using 指令之前。</span><span class="sxs-lookup"><span data-stu-id="9971c-138">`true` - Sort `System.*` `using` directives alphabetically, and place them before other using directives.</span></span><br /><br /><span data-ttu-id="9971c-139">`false` -不要将 `System.*` `using` 指令放在其他 `using` 指令之前。</span><span class="sxs-lookup"><span data-stu-id="9971c-139">`false` - Do not place `System.*` `using` directives before other `using` directives.</span></span> |

<span data-ttu-id="9971c-140">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-140">Code examples:</span></span>

```csharp
// dotnet_sort_system_directives_first = true
using System.Collections.Generic;
using System.Threading.Tasks;
using Octokit;

// dotnet_sort_system_directives_first = false
using System.Collections.Generic;
using Octokit;
using System.Threading.Tasks;
```

#### <a name="dotnet_separate_import_directive_groups"></a><span data-ttu-id="9971c-141">dotnet\_separate\_import\_directive\_groups</span><span class="sxs-lookup"><span data-stu-id="9971c-141">dotnet\_separate\_import\_directive\_groups</span></span>

|<span data-ttu-id="9971c-142">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-142">Property</span></span>|<span data-ttu-id="9971c-143">值</span><span class="sxs-lookup"><span data-stu-id="9971c-143">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-144">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-144">**Option name**</span></span> | <span data-ttu-id="9971c-145">dotnet_separate_import_directive_groups</span><span class="sxs-lookup"><span data-stu-id="9971c-145">dotnet_separate_import_directive_groups</span></span> |
| <span data-ttu-id="9971c-146">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-146">**Applicable languages**</span></span> | <span data-ttu-id="9971c-147">C# 和 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9971c-147">C# and Visual Basic</span></span> |
| <span data-ttu-id="9971c-148">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-148">**Introduced version**</span></span> | <span data-ttu-id="9971c-149">Visual Studio 2017 版本 15.5</span><span class="sxs-lookup"><span data-stu-id="9971c-149">Visual Studio 2017 version 15.5</span></span> |
| <span data-ttu-id="9971c-150">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-150">**Option values**</span></span> | <span data-ttu-id="9971c-151">`true` - 在 `using` 指令组之间放置一个空白行。</span><span class="sxs-lookup"><span data-stu-id="9971c-151">`true` - Place a blank line between `using` directive groups.</span></span><br /><br /><span data-ttu-id="9971c-152">`false` - 不在 `using` 指令组之间放置空白行。</span><span class="sxs-lookup"><span data-stu-id="9971c-152">`false` - Do not place a blank line between `using` directive groups.</span></span> |

<span data-ttu-id="9971c-153">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-153">Code examples:</span></span>

```csharp
// dotnet_separate_import_directive_groups = true
using System.Collections.Generic;
using System.Threading.Tasks;

using Octokit;

// dotnet_separate_import_directive_groups = false
using System.Collections.Generic;
using System.Threading.Tasks;
using Octokit;
```

## <a name="c-formatting-rules"></a><span data-ttu-id="9971c-154">C # 格式设置规则</span><span class="sxs-lookup"><span data-stu-id="9971c-154">C# formatting rules</span></span>

<span data-ttu-id="9971c-155">本节中的格式设置规则仅适用于 C# 代码。</span><span class="sxs-lookup"><span data-stu-id="9971c-155">The formatting rules in this section apply only to C# code.</span></span>

- [<span data-ttu-id="9971c-156">换行符选项</span><span class="sxs-lookup"><span data-stu-id="9971c-156">Newline options</span></span>](#new-line-options)
  - <span data-ttu-id="9971c-157">csharp_new_line_before_open_brace</span><span class="sxs-lookup"><span data-stu-id="9971c-157">csharp_new_line_before_open_brace</span></span>
  - <span data-ttu-id="9971c-158">csharp_new_line_before_else</span><span class="sxs-lookup"><span data-stu-id="9971c-158">csharp_new_line_before_else</span></span>
  - <span data-ttu-id="9971c-159">csharp_new_line_before_catch</span><span class="sxs-lookup"><span data-stu-id="9971c-159">csharp_new_line_before_catch</span></span>
  - <span data-ttu-id="9971c-160">csharp_new_line_before_finally</span><span class="sxs-lookup"><span data-stu-id="9971c-160">csharp_new_line_before_finally</span></span>
  - <span data-ttu-id="9971c-161">csharp_new_line_before_members_in_object_initializers</span><span class="sxs-lookup"><span data-stu-id="9971c-161">csharp_new_line_before_members_in_object_initializers</span></span>
  - <span data-ttu-id="9971c-162">csharp_new_line_before_members_in_anonymous_types</span><span class="sxs-lookup"><span data-stu-id="9971c-162">csharp_new_line_before_members_in_anonymous_types</span></span>
  - <span data-ttu-id="9971c-163">csharp_new_line_between_query_expression_clauses</span><span class="sxs-lookup"><span data-stu-id="9971c-163">csharp_new_line_between_query_expression_clauses</span></span>
- [<span data-ttu-id="9971c-164">缩进选项</span><span class="sxs-lookup"><span data-stu-id="9971c-164">Indentation options</span></span>](#indentation-options)
  - <span data-ttu-id="9971c-165">csharp_indent_case_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-165">csharp_indent_case_contents</span></span>
  - <span data-ttu-id="9971c-166">csharp_indent_switch_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-166">csharp_indent_switch_labels</span></span>
  - <span data-ttu-id="9971c-167">csharp_indent_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-167">csharp_indent_labels</span></span>
  - <span data-ttu-id="9971c-168">csharp_indent_block_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-168">csharp_indent_block_contents</span></span>
  - <span data-ttu-id="9971c-169">csharp_indent_braces</span><span class="sxs-lookup"><span data-stu-id="9971c-169">csharp_indent_braces</span></span>
  - <span data-ttu-id="9971c-170">csharp_indent_case_contents_when_block</span><span class="sxs-lookup"><span data-stu-id="9971c-170">csharp_indent_case_contents_when_block</span></span>
- [<span data-ttu-id="9971c-171">间距选项</span><span class="sxs-lookup"><span data-stu-id="9971c-171">Spacing options</span></span>](#spacing-options)
  - <span data-ttu-id="9971c-172">csharp_space_after_cast</span><span class="sxs-lookup"><span data-stu-id="9971c-172">csharp_space_after_cast</span></span>
  - <span data-ttu-id="9971c-173">csharp_space_after_keywords_in_control_flow_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-173">csharp_space_after_keywords_in_control_flow_statements</span></span>
  - <span data-ttu-id="9971c-174">csharp_space_between_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-174">csharp_space_between_parentheses</span></span>
  - <span data-ttu-id="9971c-175">csharp_space_before_colon_in_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-175">csharp_space_before_colon_in_inheritance_clause</span></span>
  - <span data-ttu-id="9971c-176">csharp_space_after_colon_in_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-176">csharp_space_after_colon_in_inheritance_clause</span></span>
  - <span data-ttu-id="9971c-177">csharp_space_around_binary_operators</span><span class="sxs-lookup"><span data-stu-id="9971c-177">csharp_space_around_binary_operators</span></span>
  - <span data-ttu-id="9971c-178">csharp_space_between_method_declaration_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-178">csharp_space_between_method_declaration_parameter_list_parentheses</span></span>
  - <span data-ttu-id="9971c-179">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-179">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span></span>
  - <span data-ttu-id="9971c-180">csharp_space_between_method_declaration_name_and_open_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-180">csharp_space_between_method_declaration_name_and_open_parenthesis</span></span>
  - <span data-ttu-id="9971c-181">csharp_space_between_method_call_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-181">csharp_space_between_method_call_parameter_list_parentheses</span></span>
  - <span data-ttu-id="9971c-182">csharp_space_between_method_call_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-182">csharp_space_between_method_call_empty_parameter_list_parentheses</span></span>
  - <span data-ttu-id="9971c-183">csharp_space_between_method_call_name_and_opening_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-183">csharp_space_between_method_call_name_and_opening_parenthesis</span></span>
  - <span data-ttu-id="9971c-184">csharp_space_after_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-184">csharp_space_after_comma</span></span>
  - <span data-ttu-id="9971c-185">csharp_space_before_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-185">csharp_space_before_comma</span></span>
  - <span data-ttu-id="9971c-186">csharp_space_after_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-186">csharp_space_after_dot</span></span>
  - <span data-ttu-id="9971c-187">csharp_space_before_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-187">csharp_space_before_dot</span></span>
  - <span data-ttu-id="9971c-188">csharp_space_after_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-188">csharp_space_after_semicolon_in_for_statement</span></span>
  - <span data-ttu-id="9971c-189">csharp_space_before_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-189">csharp_space_before_semicolon_in_for_statement</span></span>
  - <span data-ttu-id="9971c-190">csharp_space_around_declaration_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-190">csharp_space_around_declaration_statements</span></span>
  - <span data-ttu-id="9971c-191">csharp_space_before_open_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-191">csharp_space_before_open_square_brackets</span></span>
  - <span data-ttu-id="9971c-192">csharp_space_between_empty_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-192">csharp_space_between_empty_square_brackets</span></span>
  - <span data-ttu-id="9971c-193">csharp_space_between_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-193">csharp_space_between_square_brackets</span></span>
- [<span data-ttu-id="9971c-194">换行选项</span><span class="sxs-lookup"><span data-stu-id="9971c-194">Wrap options</span></span>](#wrap-options)
  - <span data-ttu-id="9971c-195">csharp_preserve_single_line_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-195">csharp_preserve_single_line_statements</span></span>
  - <span data-ttu-id="9971c-196">csharp_preserve_single_line_blocks</span><span class="sxs-lookup"><span data-stu-id="9971c-196">csharp_preserve_single_line_blocks</span></span>
- [<span data-ttu-id="9971c-197">sing 指令选项</span><span class="sxs-lookup"><span data-stu-id="9971c-197">Using directive options</span></span>](#using-directive-options)
  - <span data-ttu-id="9971c-198">csharp_using_directive_placement</span><span class="sxs-lookup"><span data-stu-id="9971c-198">csharp_using_directive_placement</span></span>

### <a name="new-line-options"></a><span data-ttu-id="9971c-199">换行选项</span><span class="sxs-lookup"><span data-stu-id="9971c-199">New-line options</span></span>

<span data-ttu-id="9971c-200">这些格式设置规则与是否使用新行设置代码的格式有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-200">These formatting rules concern the use of new lines to format code.</span></span>

<span data-ttu-id="9971c-201">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-201">Example *.editorconfig* file:</span></span>

```ini
# CSharp formatting rules:
[*.cs]
csharp_new_line_before_open_brace = methods, properties, control_blocks, types
csharp_new_line_before_else = true
csharp_new_line_before_catch = true
csharp_new_line_before_finally = true
csharp_new_line_before_members_in_object_initializers = true
csharp_new_line_before_members_in_anonymous_types = true
csharp_new_line_between_query_expression_clauses = true
```

#### <a name="csharp_new_line_before_open_brace"></a><span data-ttu-id="9971c-202">csharp\_new\_line\_before\_open_brace</span><span class="sxs-lookup"><span data-stu-id="9971c-202">csharp\_new\_line\_before\_open_brace</span></span>

<span data-ttu-id="9971c-203">此规则与左大括号 `{` 应放在前面代码的同一行还是新行上有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-203">This rule concerns whether an open brace `{` should be placed on the same line as the preceding code, or on a new line.</span></span> <span data-ttu-id="9971c-204">对于此规则，指定“全部”、“无”或一个或多个码位元素，如方法或属性，从而定义此规则的应用时间   。</span><span class="sxs-lookup"><span data-stu-id="9971c-204">For this rule, you specify **all**, **none**, or one or more code elements such as **methods** or **properties**, to define when this rule should be applied.</span></span> <span data-ttu-id="9971c-205">若要指定多个代码元素，请使用逗号 (,) 分隔。</span><span class="sxs-lookup"><span data-stu-id="9971c-205">To specify multiple code elements, separate them with a comma (,).</span></span>

|<span data-ttu-id="9971c-206">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-206">Property</span></span>|<span data-ttu-id="9971c-207">值</span><span class="sxs-lookup"><span data-stu-id="9971c-207">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-208">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-208">**Option name**</span></span> | <span data-ttu-id="9971c-209">csharp_new_line_before_open_brace</span><span class="sxs-lookup"><span data-stu-id="9971c-209">csharp_new_line_before_open_brace</span></span> |
| <span data-ttu-id="9971c-210">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-210">**Applicable languages**</span></span> | <span data-ttu-id="9971c-211">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-211">C#</span></span> |
| <span data-ttu-id="9971c-212">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-212">**Introduced version**</span></span> | <span data-ttu-id="9971c-213">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-213">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-214">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-214">**Option values**</span></span> | <span data-ttu-id="9971c-215">`all` - 对于所有表达式，需要将大括号置于新行（“Allman”样式）。</span><span class="sxs-lookup"><span data-stu-id="9971c-215">`all` - Require braces to be on a new line for all expressions ("Allman" style).</span></span><br /><br /><span data-ttu-id="9971c-216">`none` - 对于所有表达式，需要将大括号置于同一行（“K&R”）。</span><span class="sxs-lookup"><span data-stu-id="9971c-216">`none` - Require braces to be on the same line for all expressions ("K&R").</span></span><br /><br /><span data-ttu-id="9971c-217">`accessors`、`anonymous_methods`、`anonymous_types`、`control_blocks`、`events`、`indexers`、`lambdas`、`local_functions`、`methods`、`object_collection_array_initializers`、`properties`、`types` - 对于指定的代码元素，需要将大括号置于新行（“Allman”样式）。</span><span class="sxs-lookup"><span data-stu-id="9971c-217">`accessors`, `anonymous_methods`, `anonymous_types`, `control_blocks`, `events`, `indexers`, `lambdas`, `local_functions`, `methods`, `object_collection_array_initializers`, `properties`, `types` - Require braces to be on a new line for the specified code element ("Allman" style).</span></span> |

<span data-ttu-id="9971c-218">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-218">Code examples:</span></span>

```csharp
// csharp_new_line_before_open_brace = all
void MyMethod()
{
    if (...)
    {
        ...
    }
}

// csharp_new_line_before_open_brace = none
void MyMethod() {
    if (...) {
        ...
    }
}
```

#### <a name="csharp_new_line_before_else"></a><span data-ttu-id="9971c-219">csharp\_new\_line\_before_else</span><span class="sxs-lookup"><span data-stu-id="9971c-219">csharp\_new\_line\_before_else</span></span>

|<span data-ttu-id="9971c-220">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-220">Property</span></span>|<span data-ttu-id="9971c-221">值</span><span class="sxs-lookup"><span data-stu-id="9971c-221">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-222">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-222">**Option name**</span></span> | <span data-ttu-id="9971c-223">csharp_new_line_before_else</span><span class="sxs-lookup"><span data-stu-id="9971c-223">csharp_new_line_before_else</span></span> |
| <span data-ttu-id="9971c-224">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-224">**Applicable languages**</span></span> | <span data-ttu-id="9971c-225">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-225">C#</span></span> |
| <span data-ttu-id="9971c-226">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-226">**Introduced version**</span></span> | <span data-ttu-id="9971c-227">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-227">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-228">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-228">**Option values**</span></span> | <span data-ttu-id="9971c-229">`true` - 将 `else` 语句置于新行。</span><span class="sxs-lookup"><span data-stu-id="9971c-229">`true` - Place `else` statements on a new line.</span></span><br /><br /><span data-ttu-id="9971c-230">`false` - 将 `else` 语句置于同一行。</span><span class="sxs-lookup"><span data-stu-id="9971c-230">`false` - Place `else` statements on the same line.</span></span> |

<span data-ttu-id="9971c-231">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-231">Code examples:</span></span>

```csharp
// csharp_new_line_before_else = true
if (...) {
    ...
}
else {
    ...
}

// csharp_new_line_before_else = false
if (...) {
    ...
} else {
    ...
}
```

#### <a name="csharp_new_line_before_catch"></a><span data-ttu-id="9971c-232">csharp\_new\_line\_before_catch</span><span class="sxs-lookup"><span data-stu-id="9971c-232">csharp\_new\_line\_before_catch</span></span>

|<span data-ttu-id="9971c-233">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-233">Property</span></span>|<span data-ttu-id="9971c-234">值</span><span class="sxs-lookup"><span data-stu-id="9971c-234">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-235">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-235">**Option name**</span></span> | <span data-ttu-id="9971c-236">csharp_new_line_before_catch</span><span class="sxs-lookup"><span data-stu-id="9971c-236">csharp_new_line_before_catch</span></span> |
| <span data-ttu-id="9971c-237">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-237">**Applicable languages**</span></span> | <span data-ttu-id="9971c-238">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-238">C#</span></span> |
| <span data-ttu-id="9971c-239">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-239">**Introduced version**</span></span> | <span data-ttu-id="9971c-240">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-240">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-241">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-241">**Option values**</span></span> | <span data-ttu-id="9971c-242">`true` - 将 `catch` 语句置于新行。</span><span class="sxs-lookup"><span data-stu-id="9971c-242">`true` - Place `catch` statements on a new line.</span></span><br /><br /><span data-ttu-id="9971c-243">`false` - 将 `catch` 语句置于同一行。</span><span class="sxs-lookup"><span data-stu-id="9971c-243">`false` - Place `catch` statements on the same line.</span></span> |

<span data-ttu-id="9971c-244">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-244">Code examples:</span></span>

```csharp
// csharp_new_line_before_catch = true
try {
    ...
}
catch (Exception e) {
    ...
}

// csharp_new_line_before_catch = false
try {
    ...
} catch (Exception e) {
    ...
}
```

#### <a name="csharp_new_line_before_finally"></a><span data-ttu-id="9971c-245">csharp\_new\_line\_before_finally</span><span class="sxs-lookup"><span data-stu-id="9971c-245">csharp\_new\_line\_before_finally</span></span>

|<span data-ttu-id="9971c-246">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-246">Property</span></span>|<span data-ttu-id="9971c-247">值</span><span class="sxs-lookup"><span data-stu-id="9971c-247">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-248">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-248">**Option name**</span></span> | <span data-ttu-id="9971c-249">csharp_new_line_before_finally</span><span class="sxs-lookup"><span data-stu-id="9971c-249">csharp_new_line_before_finally</span></span> |
| <span data-ttu-id="9971c-250">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-250">**Applicable languages**</span></span> | <span data-ttu-id="9971c-251">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-251">C#</span></span> |
| <span data-ttu-id="9971c-252">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-252">**Introduced version**</span></span> | <span data-ttu-id="9971c-253">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-253">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-254">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-254">**Option values**</span></span> | <span data-ttu-id="9971c-255">`true` - 需要将 `finally` 语句置于右大括号后的新行。</span><span class="sxs-lookup"><span data-stu-id="9971c-255">`true` - Require `finally` statements to be on a new line after the closing brace.</span></span><br /><br /><span data-ttu-id="9971c-256">`false` - 需要将 `finally` 语句置于右大括号所在的同一行。</span><span class="sxs-lookup"><span data-stu-id="9971c-256">`false` - Require `finally` statements to be on the same line as the closing brace.</span></span> |

<span data-ttu-id="9971c-257">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-257">Code examples:</span></span>

```csharp
// csharp_new_line_before_finally = true
try {
    ...
}
catch (Exception e) {
    ...
}
finally {
    ...
}

// csharp_new_line_before_finally = false
try {
    ...
} catch (Exception e) {
    ...
} finally {
    ...
}
```

#### <a name="csharp_new_line_before_members_in_object_initializers"></a><span data-ttu-id="9971c-258">csharp\_new\_line\_before\_members\_in\_object_initializers</span><span class="sxs-lookup"><span data-stu-id="9971c-258">csharp\_new\_line\_before\_members\_in\_object_initializers</span></span>

|<span data-ttu-id="9971c-259">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-259">Property</span></span>|<span data-ttu-id="9971c-260">值</span><span class="sxs-lookup"><span data-stu-id="9971c-260">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-261">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-261">**Option name**</span></span> | <span data-ttu-id="9971c-262">csharp_new_line_before_members_in_object_initializers</span><span class="sxs-lookup"><span data-stu-id="9971c-262">csharp_new_line_before_members_in_object_initializers</span></span> |
| <span data-ttu-id="9971c-263">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-263">**Applicable languages**</span></span> | <span data-ttu-id="9971c-264">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-264">C#</span></span> |
| <span data-ttu-id="9971c-265">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-265">**Introduced version**</span></span> | <span data-ttu-id="9971c-266">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-266">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-267">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-267">**Option values**</span></span> | <span data-ttu-id="9971c-268">`true` - 需要将对象初始值设定项的成员置于单独的行</span><span class="sxs-lookup"><span data-stu-id="9971c-268">`true` - Require members of object initializers to be on separate lines</span></span><br /><br /><span data-ttu-id="9971c-269">`false` - 需要将对象初始值设定项的成员置于同一行</span><span class="sxs-lookup"><span data-stu-id="9971c-269">`false` - Require members of object initializers to be on the same line</span></span> |

<span data-ttu-id="9971c-270">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-270">Code examples:</span></span>

```csharp
// csharp_new_line_before_members_in_object_initializers = true
var z = new B()
{
    A = 3,
    B = 4
}

// csharp_new_line_before_members_in_object_initializers = false
var z = new B()
{
    A = 3, B = 4
}
```

#### <a name="csharp_new_line_before_members_in_anonymous_types"></a><span data-ttu-id="9971c-271">csharp\_new\_line\_before\_members\_in\_anonymous_types</span><span class="sxs-lookup"><span data-stu-id="9971c-271">csharp\_new\_line\_before\_members\_in\_anonymous_types</span></span>

|<span data-ttu-id="9971c-272">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-272">Property</span></span>|<span data-ttu-id="9971c-273">值</span><span class="sxs-lookup"><span data-stu-id="9971c-273">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-274">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-274">**Option name**</span></span> | <span data-ttu-id="9971c-275">csharp_new_line_before_members_in_anonymous_types</span><span class="sxs-lookup"><span data-stu-id="9971c-275">csharp_new_line_before_members_in_anonymous_types</span></span> |
| <span data-ttu-id="9971c-276">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-276">**Applicable languages**</span></span> | <span data-ttu-id="9971c-277">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-277">C#</span></span> |
| <span data-ttu-id="9971c-278">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-278">**Introduced version**</span></span> | <span data-ttu-id="9971c-279">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-279">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-280">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-280">**Option values**</span></span> | <span data-ttu-id="9971c-281">`true` - 需要将匿名类型的成员置于单独的行</span><span class="sxs-lookup"><span data-stu-id="9971c-281">`true` - Require members of anonymous types to be on separate lines</span></span><br /><br /><span data-ttu-id="9971c-282">`false` - 需要将匿名类型的成员置于同一行</span><span class="sxs-lookup"><span data-stu-id="9971c-282">`false` - Require members of anonymous types to be on the same line</span></span> |

<span data-ttu-id="9971c-283">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-283">Code examples:</span></span>

```csharp
// csharp_new_line_before_members_in_anonymous_types = true
var z = new
{
    A = 3,
    B = 4
}

// csharp_new_line_before_members_in_anonymous_types = false
var z = new
{
    A = 3, B = 4
}
```

#### <a name="csharp_new_line_between_query_expression_clauses"></a><span data-ttu-id="9971c-284">csharp_new_line_between_query_expression_clauses</span><span class="sxs-lookup"><span data-stu-id="9971c-284">csharp_new_line_between_query_expression_clauses</span></span>

|<span data-ttu-id="9971c-285">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-285">Property</span></span>|<span data-ttu-id="9971c-286">值</span><span class="sxs-lookup"><span data-stu-id="9971c-286">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-287">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-287">**Option name**</span></span> | <span data-ttu-id="9971c-288">csharp_new_line_between_query_expression_clauses</span><span class="sxs-lookup"><span data-stu-id="9971c-288">csharp_new_line_between_query_expression_clauses</span></span> |
| <span data-ttu-id="9971c-289">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-289">**Applicable languages**</span></span> | <span data-ttu-id="9971c-290">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-290">C#</span></span> |
| <span data-ttu-id="9971c-291">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-291">**Introduced version**</span></span> | <span data-ttu-id="9971c-292">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-292">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-293">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-293">**Option values**</span></span> | <span data-ttu-id="9971c-294">`true` - 要求将查询表达式子句的元素置于单独的行</span><span class="sxs-lookup"><span data-stu-id="9971c-294">`true` - Require elements of query expression clauses to be on separate lines</span></span><br /><br /><span data-ttu-id="9971c-295">`false` - 要求将查询表达式子句的元素置于同一行</span><span class="sxs-lookup"><span data-stu-id="9971c-295">`false` - Require elements of query expression clauses to be on the same line</span></span> |

<span data-ttu-id="9971c-296">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-296">Code examples:</span></span>

```csharp
// csharp_new_line_between_query_expression_clauses = true
var q = from a in e
        from b in e
        select a * b;

// csharp_new_line_between_query_expression_clauses = false
var q = from a in e from b in e
        select a * b;
```

### <a name="indentation-options"></a><span data-ttu-id="9971c-297">缩进选项</span><span class="sxs-lookup"><span data-stu-id="9971c-297">Indentation options</span></span>

<span data-ttu-id="9971c-298">这些格式设置规则与是否使用缩进设置代码的格式有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-298">These formatting rules concern the use of indentation to format code.</span></span>

<span data-ttu-id="9971c-299">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-299">Example *.editorconfig* file:</span></span>

```ini
# CSharp formatting rules:
[*.cs]
csharp_indent_case_contents = true
csharp_indent_switch_labels = true
csharp_indent_labels = flush_left
csharp_indent_block_contents = true
csharp_indent_braces = false
csharp_indent_case_contents_when_block = true
```

#### <a name="csharp_indent_case_contents"></a><span data-ttu-id="9971c-300">csharp\_indent\_case_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-300">csharp\_indent\_case_contents</span></span>

|<span data-ttu-id="9971c-301">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-301">Property</span></span>|<span data-ttu-id="9971c-302">值</span><span class="sxs-lookup"><span data-stu-id="9971c-302">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-303">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-303">**Option name**</span></span> | <span data-ttu-id="9971c-304">csharp_indent_case_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-304">csharp_indent_case_contents</span></span> |
| <span data-ttu-id="9971c-305">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-305">**Applicable languages**</span></span> | <span data-ttu-id="9971c-306">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-306">C#</span></span> |
| <span data-ttu-id="9971c-307">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-307">**Introduced version**</span></span> | <span data-ttu-id="9971c-308">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-308">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-309">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-309">**Option values**</span></span> | <span data-ttu-id="9971c-310">`true` - 缩进 `switch` case 内容</span><span class="sxs-lookup"><span data-stu-id="9971c-310">`true` - Indent `switch` case contents</span></span><br /><br /><span data-ttu-id="9971c-311">`false` - 不缩进 `switch` case 内容</span><span class="sxs-lookup"><span data-stu-id="9971c-311">`false` - Do not indent `switch` case contents</span></span> |

- <span data-ttu-id="9971c-312">如果此规则设置为“true”，则为 i。</span><span class="sxs-lookup"><span data-stu-id="9971c-312">When this rule is set to **true**, i.</span></span>
- <span data-ttu-id="9971c-313">如果此规则设置为“false”，则为 d。</span><span class="sxs-lookup"><span data-stu-id="9971c-313">When this rule is set to **false**, d.</span></span>

<span data-ttu-id="9971c-314">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-314">Code examples:</span></span>

```csharp
// csharp_indent_case_contents = true
switch(c) {
    case Color.Red:
        Console.WriteLine("The color is red");
        break;
    case Color.Blue:
        Console.WriteLine("The color is blue");
        break;
    default:
        Console.WriteLine("The color is unknown.");
        break;
}

// csharp_indent_case_contents = false
switch(c) {
    case Color.Red:
    Console.WriteLine("The color is red");
    break;
    case Color.Blue:
    Console.WriteLine("The color is blue");
    break;
    default:
    Console.WriteLine("The color is unknown.");
    break;
}
```

#### <a name="csharp_indent_switch_labels"></a><span data-ttu-id="9971c-315">csharp\_indent\_switch_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-315">csharp\_indent\_switch_labels</span></span>

|<span data-ttu-id="9971c-316">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-316">Property</span></span>|<span data-ttu-id="9971c-317">值</span><span class="sxs-lookup"><span data-stu-id="9971c-317">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-318">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-318">**Option name**</span></span> | <span data-ttu-id="9971c-319">csharp_indent_switch_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-319">csharp_indent_switch_labels</span></span> |
| <span data-ttu-id="9971c-320">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-320">**Applicable languages**</span></span> | <span data-ttu-id="9971c-321">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-321">C#</span></span> |
| <span data-ttu-id="9971c-322">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-322">**Introduced version**</span></span> | <span data-ttu-id="9971c-323">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-323">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-324">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-324">**Option values**</span></span> | <span data-ttu-id="9971c-325">`true` - 缩进 `switch` 标签</span><span class="sxs-lookup"><span data-stu-id="9971c-325">`true` - Indent `switch` labels</span></span><br /><br /><span data-ttu-id="9971c-326">`false` - 不缩进 `switch` 标签</span><span class="sxs-lookup"><span data-stu-id="9971c-326">`false` - Do not indent `switch` labels</span></span> |

<span data-ttu-id="9971c-327">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-327">Code examples:</span></span>

```csharp
// csharp_indent_switch_labels = true
switch(c) {
    case Color.Red:
        Console.WriteLine("The color is red");
        break;
    case Color.Blue:
        Console.WriteLine("The color is blue");
        break;
    default:
        Console.WriteLine("The color is unknown.");
        break;
}

// csharp_indent_switch_labels = false
switch(c) {
case Color.Red:
    Console.WriteLine("The color is red");
    break;
case Color.Blue:
    Console.WriteLine("The color is blue");
    break;
default:
    Console.WriteLine("The color is unknown.");
    break;
}
```

#### <a name="csharp_indent_labels"></a><span data-ttu-id="9971c-328">csharp\_indent_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-328">csharp\_indent_labels</span></span>

|<span data-ttu-id="9971c-329">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-329">Property</span></span>|<span data-ttu-id="9971c-330">值</span><span class="sxs-lookup"><span data-stu-id="9971c-330">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-331">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-331">**Option name**</span></span> | <span data-ttu-id="9971c-332">csharp_indent_labels</span><span class="sxs-lookup"><span data-stu-id="9971c-332">csharp_indent_labels</span></span> |
| <span data-ttu-id="9971c-333">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-333">**Applicable languages**</span></span> | <span data-ttu-id="9971c-334">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-334">C#</span></span> |
| <span data-ttu-id="9971c-335">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-335">**Introduced version**</span></span> | <span data-ttu-id="9971c-336">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-336">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-337">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-337">**Option values**</span></span> | <span data-ttu-id="9971c-338">`flush_left` - 标签置于最左侧的列</span><span class="sxs-lookup"><span data-stu-id="9971c-338">`flush_left` - Labels are placed at the leftmost column</span></span><br /><br /><span data-ttu-id="9971c-339">`one_less_than_current` - 将标签置于比当前上下文少一个缩进的位置</span><span class="sxs-lookup"><span data-stu-id="9971c-339">`one_less_than_current` - Labels are placed at one less indent to the current context</span></span><br /><br /><span data-ttu-id="9971c-340">`no_change` - 将标签置于与当前上下文相同的缩进位置</span><span class="sxs-lookup"><span data-stu-id="9971c-340">`no_change` - Labels are placed at the same indent as the current context</span></span> |

<span data-ttu-id="9971c-341">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-341">Code examples:</span></span>

```csharp
// csharp_indent_labels= flush_left
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
error:
        throw new Exception(...);
    }
}

// csharp_indent_labels = one_less_than_current
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
    error:
        throw new Exception(...);
    }
}

// csharp_indent_labels= no_change
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
        error:
        throw new Exception(...);
    }
}
```

#### <a name="csharp_indent_block_contents"></a><span data-ttu-id="9971c-342">csharp_indent_block_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-342">csharp_indent_block_contents</span></span>

|<span data-ttu-id="9971c-343">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-343">Property</span></span>|<span data-ttu-id="9971c-344">值</span><span class="sxs-lookup"><span data-stu-id="9971c-344">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-345">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-345">**Option name**</span></span> | <span data-ttu-id="9971c-346">csharp_indent_block_contents</span><span class="sxs-lookup"><span data-stu-id="9971c-346">csharp_indent_block_contents</span></span> |
| <span data-ttu-id="9971c-347">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-347">**Applicable languages**</span></span> | <span data-ttu-id="9971c-348">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-348">C#</span></span> |
| <span data-ttu-id="9971c-349">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-349">**Option values**</span></span> | `true` - <br /><br />`false` -  |

<span data-ttu-id="9971c-350">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-350">Code examples:</span></span>

```csharp
// csharp_indent_block_contents = true
static void Hello()
{
    Console.WriteLine("Hello");
}

// csharp_indent_block_contents = false
static void Hello()
{
Console.WriteLine("Hello");
}
```

#### <a name="csharp_indent_braces"></a><span data-ttu-id="9971c-351">csharp_indent_braces</span><span class="sxs-lookup"><span data-stu-id="9971c-351">csharp_indent_braces</span></span>

|<span data-ttu-id="9971c-352">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-352">Property</span></span>|<span data-ttu-id="9971c-353">值</span><span class="sxs-lookup"><span data-stu-id="9971c-353">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-354">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-354">**Option name**</span></span> | <span data-ttu-id="9971c-355">csharp_indent_braces</span><span class="sxs-lookup"><span data-stu-id="9971c-355">csharp_indent_braces</span></span> |
| <span data-ttu-id="9971c-356">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-356">**Applicable languages**</span></span> | <span data-ttu-id="9971c-357">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-357">C#</span></span> |
| <span data-ttu-id="9971c-358">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-358">**Option values**</span></span> | `true` - <br /><br />`false` -  |

<span data-ttu-id="9971c-359">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-359">Code examples:</span></span>

```csharp
// csharp_indent_braces = true
static void Hello()
    {
    Console.WriteLine("Hello");
    }

// csharp_indent_braces = false
static void Hello()
{
    Console.WriteLine("Hello");
}
```

#### <a name="csharp_indent_case_contents_when_block"></a><span data-ttu-id="9971c-360">csharp_indent_case_contents_when_block</span><span class="sxs-lookup"><span data-stu-id="9971c-360">csharp_indent_case_contents_when_block</span></span>

|<span data-ttu-id="9971c-361">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-361">Property</span></span>|<span data-ttu-id="9971c-362">值</span><span class="sxs-lookup"><span data-stu-id="9971c-362">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-363">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-363">**Option name**</span></span> | <span data-ttu-id="9971c-364">csharp_indent_case_contents_when_block</span><span class="sxs-lookup"><span data-stu-id="9971c-364">csharp_indent_case_contents_when_block</span></span> |
| <span data-ttu-id="9971c-365">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-365">**Applicable languages**</span></span> | <span data-ttu-id="9971c-366">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-366">C#</span></span> |
| <span data-ttu-id="9971c-367">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-367">**Option values**</span></span> | `true` - <br /><br />`false` -  |

<span data-ttu-id="9971c-368">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-368">Code examples:</span></span>

```csharp
// csharp_indent_case_contents_when_block = true
case 0:
    {
        Console.WriteLine("Hello");
        break;
    }

// csharp_indent_case_contents_when_block = false
case 0:
{
    Console.WriteLine("Hello");
    break;
}
```

### <a name="spacing-options"></a><span data-ttu-id="9971c-369">间距选项</span><span class="sxs-lookup"><span data-stu-id="9971c-369">Spacing options</span></span>

<span data-ttu-id="9971c-370">这些格式设置规则与是否使用空格字符设置代码的格式有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-370">These formatting rules concern the use of space characters to format code.</span></span>

<span data-ttu-id="9971c-371">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-371">Example *.editorconfig* file:</span></span>

```ini
# CSharp formatting rules:
[*.cs]
csharp_space_after_cast = true
csharp_space_after_keywords_in_control_flow_statements = true
csharp_space_between_parentheses = control_flow_statements, type_casts
csharp_space_before_colon_in_inheritance_clause = true
csharp_space_after_colon_in_inheritance_clause = true
csharp_space_around_binary_operators = before_and_after
csharp_space_between_method_declaration_parameter_list_parentheses = true
csharp_space_between_method_declaration_empty_parameter_list_parentheses = false
csharp_space_between_method_declaration_name_and_open_parenthesis = false
csharp_space_between_method_call_parameter_list_parentheses = true
csharp_space_between_method_call_empty_parameter_list_parentheses = false
csharp_space_between_method_call_name_and_opening_parenthesis = false
csharp_space_after_comma = true
csharp_space_before_comma = false
csharp_space_after_dot = false
csharp_space_before_dot = false
csharp_space_after_semicolon_in_for_statement = true
csharp_space_before_semicolon_in_for_statement = false
csharp_space_around_declaration_statements = false
csharp_space_before_open_square_brackets = false
csharp_space_between_empty_square_brackets = false
csharp_space_between_square_brackets = false
```

#### <a name="csharp_space_after_cast"></a><span data-ttu-id="9971c-372">csharp\_space\_after_cast</span><span class="sxs-lookup"><span data-stu-id="9971c-372">csharp\_space\_after_cast</span></span>

|<span data-ttu-id="9971c-373">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-373">Property</span></span>|<span data-ttu-id="9971c-374">值</span><span class="sxs-lookup"><span data-stu-id="9971c-374">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-375">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-375">**Option name**</span></span> | <span data-ttu-id="9971c-376">csharp_space_after_cast</span><span class="sxs-lookup"><span data-stu-id="9971c-376">csharp_space_after_cast</span></span> |
| <span data-ttu-id="9971c-377">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-377">**Applicable languages**</span></span> | <span data-ttu-id="9971c-378">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-378">C#</span></span> |
| <span data-ttu-id="9971c-379">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-379">**Introduced version**</span></span> | <span data-ttu-id="9971c-380">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-380">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-381">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-381">**Option values**</span></span> | <span data-ttu-id="9971c-382">`true` - 在强制转换和值之间放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-382">`true` - Place a space character between a cast and the value</span></span><br /><br /><span data-ttu-id="9971c-383">`false` - 删除转换和值之间的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-383">`false` - Remove space between the cast and the value</span></span> |

<span data-ttu-id="9971c-384">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-384">Code examples:</span></span>

```csharp
// csharp_space_after_cast = true
int y = (int) x;

// csharp_space_after_cast = false
int y = (int)x;
```

#### <a name="csharp_space_after_keywords_in_control_flow_statements"></a><span data-ttu-id="9971c-385">csharp_space_after_keywords_in_control_flow_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-385">csharp_space_after_keywords_in_control_flow_statements</span></span>

|<span data-ttu-id="9971c-386">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-386">Property</span></span>|<span data-ttu-id="9971c-387">值</span><span class="sxs-lookup"><span data-stu-id="9971c-387">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-388">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-388">**Option name**</span></span> | <span data-ttu-id="9971c-389">csharp_space_after_keywords_in_control_flow_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-389">csharp_space_after_keywords_in_control_flow_statements</span></span> |
| <span data-ttu-id="9971c-390">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-390">**Applicable languages**</span></span> | <span data-ttu-id="9971c-391">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-391">C#</span></span> |
| <span data-ttu-id="9971c-392">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-392">**Introduced version**</span></span> | <span data-ttu-id="9971c-393">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-393">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-394">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-394">**Option values**</span></span> | <span data-ttu-id="9971c-395">`true` - 在控制流语句（如 `for` 循环）中的关键字后放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-395">`true` - Place a space character after a keyword in a control flow statement such as a `for` loop</span></span><br /><br /><span data-ttu-id="9971c-396">`false` - 删除控制流语句（如 `for` 循环）中的关键字后的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-396">`false` - Remove space after a keyword in a control flow statement such as a `for` loop</span></span> |

<span data-ttu-id="9971c-397">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-397">Code examples:</span></span>

```csharp
// csharp_space_after_keywords_in_control_flow_statements = true
for (int i;i<x;i++) { ... }

// csharp_space_after_keywords_in_control_flow_statements = false
for(int i;i<x;i++) { ... }
```

#### <a name="csharp_space_between_parentheses"></a><span data-ttu-id="9971c-398">csharp_space_between_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-398">csharp_space_between_parentheses</span></span>

|<span data-ttu-id="9971c-399">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-399">Property</span></span>|<span data-ttu-id="9971c-400">值</span><span class="sxs-lookup"><span data-stu-id="9971c-400">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-401">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-401">**Option name**</span></span> | <span data-ttu-id="9971c-402">csharp_space_between_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-402">csharp_space_between_parentheses</span></span> |
| <span data-ttu-id="9971c-403">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-403">**Applicable languages**</span></span> | <span data-ttu-id="9971c-404">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-404">C#</span></span> |
| <span data-ttu-id="9971c-405">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-405">**Introduced version**</span></span> | <span data-ttu-id="9971c-406">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-406">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-407">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-407">**Option values**</span></span> | <span data-ttu-id="9971c-408">`control_flow_statements` - 在控制流语句的括号之间放置空格</span><span class="sxs-lookup"><span data-stu-id="9971c-408">`control_flow_statements` - Place space between parentheses of control flow statements</span></span><br /><br /><span data-ttu-id="9971c-409">`expressions` - 在表达式的括号之间放置空格</span><span class="sxs-lookup"><span data-stu-id="9971c-409">`expressions` - Place space between parentheses of expressions</span></span><br /><br /><span data-ttu-id="9971c-410">`type_casts` - 在类型转换中的括号之间放置空格</span><span class="sxs-lookup"><span data-stu-id="9971c-410">`type_casts` - Place space between parentheses in type casts</span></span> |

<span data-ttu-id="9971c-411">如果省略此规则或使用 `control_flow_statements`、`expressions` 或 `type_casts` 以外的值，则不会应用该设置。</span><span class="sxs-lookup"><span data-stu-id="9971c-411">If you omit this rule or use a value other than `control_flow_statements`, `expressions`, or `type_casts`, the setting is not applied.</span></span>

<span data-ttu-id="9971c-412">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-412">Code examples:</span></span>

```csharp
// csharp_space_between_parentheses = control_flow_statements
for ( int i = 0; i < 10; i++ ) { }

// csharp_space_between_parentheses = expressions
var z = ( x * y ) - ( ( y - x ) * 3 );

// csharp_space_between_parentheses = type_casts
int y = ( int )x;
```

#### <a name="csharp_space_before_colon_in_inheritance_clause"></a><span data-ttu-id="9971c-413">csharp\_space\_before\_colon\_in\_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-413">csharp\_space\_before\_colon\_in\_inheritance_clause</span></span>

|<span data-ttu-id="9971c-414">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-414">Property</span></span>|<span data-ttu-id="9971c-415">值</span><span class="sxs-lookup"><span data-stu-id="9971c-415">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-416">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-416">**Option name**</span></span> | <span data-ttu-id="9971c-417">csharp_space_before_colon_in_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-417">csharp_space_before_colon_in_inheritance_clause</span></span> |
| <span data-ttu-id="9971c-418">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-418">**Applicable languages**</span></span> | <span data-ttu-id="9971c-419">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-419">C#</span></span> |
| <span data-ttu-id="9971c-420">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-420">**Introduced version**</span></span> | <span data-ttu-id="9971c-421">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-421">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-422">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-422">**Option values**</span></span> | <span data-ttu-id="9971c-423">`true` - 在类型声明中的基或接口冒号前放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-423">`true` - Place a space character before the colon for bases or interfaces in a type declaration</span></span><br /><br /><span data-ttu-id="9971c-424">`false` - 删除类型声明中基或接口冒号前的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-424">`false` - Remove space before the colon for bases or interfaces in a type declaration</span></span> |

<span data-ttu-id="9971c-425">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-425">Code examples:</span></span>

```csharp
// csharp_space_before_colon_in_inheritance_clause = true
interface I
{

}

class C : I
{

}

// csharp_space_before_colon_in_inheritance_clause = false
interface I
{

}

class C: I
{

}
```

#### <a name="csharp_space_after_colon_in_inheritance_clause"></a><span data-ttu-id="9971c-426">csharp\_space\_after\_colon\_in\_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-426">csharp\_space\_after\_colon\_in\_inheritance_clause</span></span>

|<span data-ttu-id="9971c-427">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-427">Property</span></span>|<span data-ttu-id="9971c-428">值</span><span class="sxs-lookup"><span data-stu-id="9971c-428">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-429">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-429">**Option name**</span></span> | <span data-ttu-id="9971c-430">csharp_space_after_colon_in_inheritance_clause</span><span class="sxs-lookup"><span data-stu-id="9971c-430">csharp_space_after_colon_in_inheritance_clause</span></span> |
| <span data-ttu-id="9971c-431">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-431">**Applicable languages**</span></span> | <span data-ttu-id="9971c-432">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-432">C#</span></span> |
| <span data-ttu-id="9971c-433">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-433">**Introduced version**</span></span> | <span data-ttu-id="9971c-434">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-434">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-435">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-435">**Option values**</span></span> | <span data-ttu-id="9971c-436">`true` - 在类型声明中的基或接口冒号后放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-436">`true` - Place a space character after the colon for bases or interfaces in a type declaration</span></span><br /><br /><span data-ttu-id="9971c-437">`false` - 删除类型声明中基或接口冒号后的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-437">`false` - Remove space after the colon for bases or interfaces in a type declaration</span></span> |

<span data-ttu-id="9971c-438">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-438">Code examples:</span></span>

```csharp
// csharp_space_after_colon_in_inheritance_clause = true
interface I
{

}

class C : I
{

}

// csharp_space_after_colon_in_inheritance_clause = false
interface I
{

}

class C :I
{

}
```

#### <a name="csharp_space_around_binary_operators"></a><span data-ttu-id="9971c-439">csharp\_space\_around\_binary_operators</span><span class="sxs-lookup"><span data-stu-id="9971c-439">csharp\_space\_around\_binary_operators</span></span>

|<span data-ttu-id="9971c-440">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-440">Property</span></span>|<span data-ttu-id="9971c-441">值</span><span class="sxs-lookup"><span data-stu-id="9971c-441">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-442">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-442">**Option name**</span></span> | <span data-ttu-id="9971c-443">csharp_space_around_binary_operators</span><span class="sxs-lookup"><span data-stu-id="9971c-443">csharp_space_around_binary_operators</span></span> |
| <span data-ttu-id="9971c-444">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-444">**Applicable languages**</span></span> | <span data-ttu-id="9971c-445">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-445">C#</span></span> |
| <span data-ttu-id="9971c-446">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-446">**Introduced version**</span></span> | <span data-ttu-id="9971c-447">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-447">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-448">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-448">**Option values**</span></span> | <span data-ttu-id="9971c-449">`before_and_after` - 在二元运算符前后插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-449">`before_and_after` - Insert space before and after the binary operator</span></span><br /><br /><span data-ttu-id="9971c-450">`none` - 删除二元运算符前后的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-450">`none` - Remove spaces before and after the binary operator</span></span><br /><br /><span data-ttu-id="9971c-451">`ignore` - 忽略二元运算符前后的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-451">`ignore` - Ignore spaces around binary operators</span></span> |

<span data-ttu-id="9971c-452">如果省略此规则或使用 `before_and_after`、`none` 或 `ignore` 以外的值，则不会应用该设置。</span><span class="sxs-lookup"><span data-stu-id="9971c-452">If you omit this rule, or use a value other than `before_and_after`, `none`, or `ignore`, the setting is not applied.</span></span>

<span data-ttu-id="9971c-453">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-453">Code examples:</span></span>

```csharp
// csharp_space_around_binary_operators = before_and_after
return x * (x - y);

// csharp_space_around_binary_operators = none
return x*(x-y);

// csharp_space_around_binary_operators = ignore
return x  *  (x-y);
```

#### <a name="csharp_space_between_method_declaration_parameter_list_parentheses"></a><span data-ttu-id="9971c-454">csharp_space_between_method_declaration_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-454">csharp_space_between_method_declaration_parameter_list_parentheses</span></span>

|<span data-ttu-id="9971c-455">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-455">Property</span></span>|<span data-ttu-id="9971c-456">值</span><span class="sxs-lookup"><span data-stu-id="9971c-456">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-457">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-457">**Option name**</span></span> | <span data-ttu-id="9971c-458">csharp_space_between_method_declaration_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-458">csharp_space_between_method_declaration_parameter_list_parentheses</span></span> |
| <span data-ttu-id="9971c-459">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-459">**Applicable languages**</span></span> | <span data-ttu-id="9971c-460">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-460">C#</span></span> |
| <span data-ttu-id="9971c-461">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-461">**Introduced version**</span></span> | <span data-ttu-id="9971c-462">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-462">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-463">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-463">**Option values**</span></span> | <span data-ttu-id="9971c-464">`true` - 在方法声明参数列表的左括号之后和右括号之前放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-464">`true` - Place a space character after the opening parenthesis and before the closing parenthesis of a method declaration parameter list</span></span><br /><br /><span data-ttu-id="9971c-465">`false` - 删除方法声明参数列表的左括号之后和右括号之前的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-465">`false` - Remove space characters after the opening parenthesis and before the closing parenthesis of a method declaration parameter list</span></span> |

<span data-ttu-id="9971c-466">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-466">Code examples:</span></span>

```csharp
// csharp_space_between_method_declaration_parameter_list_parentheses = true
void Bark( int x ) { ... }

// csharp_space_between_method_declaration_parameter_list_parentheses = false
void Bark(int x) { ... }
```

#### <a name="csharp_space_between_method_declaration_empty_parameter_list_parentheses"></a><span data-ttu-id="9971c-467">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-467">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span></span>

|<span data-ttu-id="9971c-468">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-468">Property</span></span>|<span data-ttu-id="9971c-469">值</span><span class="sxs-lookup"><span data-stu-id="9971c-469">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-470">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-470">**Option name**</span></span> | <span data-ttu-id="9971c-471">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-471">csharp_space_between_method_declaration_empty_parameter_list_parentheses</span></span> |
| <span data-ttu-id="9971c-472">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-472">**Applicable languages**</span></span> | <span data-ttu-id="9971c-473">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-473">C#</span></span> |
| <span data-ttu-id="9971c-474">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-474">**Introduced version**</span></span> | <span data-ttu-id="9971c-475">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-475">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-476">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-476">**Option values**</span></span> | <span data-ttu-id="9971c-477">`true` - 在方法声明的空参数列表括号内插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-477">`true` - Insert space within empty parameter list parentheses for a method declaration</span></span><br /><br /><span data-ttu-id="9971c-478">`false` - 删除方法声明的空参数列表括号内的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-478">`false` - Remove space within empty parameter list parentheses for a method declaration</span></span> |

<span data-ttu-id="9971c-479">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-479">Code examples:</span></span>

```csharp
// csharp_space_between_method_declaration_empty_parameter_list_parentheses = true
void Goo( )
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}

// csharp_space_between_method_declaration_empty_parameter_list_parentheses = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharp_space_between_method_declaration_name_and_open_parenthesis"></a><span data-ttu-id="9971c-480">csharp_space_between_method_declaration_name_and_open_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-480">csharp_space_between_method_declaration_name_and_open_parenthesis</span></span>

|<span data-ttu-id="9971c-481">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-481">Property</span></span>|<span data-ttu-id="9971c-482">值</span><span class="sxs-lookup"><span data-stu-id="9971c-482">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-483">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-483">**Option name**</span></span> | <span data-ttu-id="9971c-484">csharp_space_between_method_declaration_name_and_open_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-484">csharp_space_between_method_declaration_name_and_open_parenthesis</span></span> |
| <span data-ttu-id="9971c-485">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-485">**Applicable languages**</span></span> | <span data-ttu-id="9971c-486">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-486">C#</span></span> |
| <span data-ttu-id="9971c-487">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-487">**Option values**</span></span> | <span data-ttu-id="9971c-488">`true` - 在方法声明中方法名称和左括号之间放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-488">`true` - Place a space character between the method name and opening parenthesis in the method declaration</span></span><br /><br /><span data-ttu-id="9971c-489">`false` - 删除方法声明中方法名称和左括号之间的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-489">`false` - Remove space characters between the method name and opening parenthesis in the method declaration</span></span> |

<span data-ttu-id="9971c-490">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-490">Code examples:</span></span>

```csharp
// csharp_space_between_method_declaration_name_and_open_parenthesis = true
void M () { }

// csharp_space_between_method_declaration_name_and_open_parenthesis = false
void M() { }
```

#### <a name="csharp_space_between_method_call_parameter_list_parentheses"></a><span data-ttu-id="9971c-491">csharp_space_between_method_call_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-491">csharp_space_between_method_call_parameter_list_parentheses</span></span>

|<span data-ttu-id="9971c-492">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-492">Property</span></span>|<span data-ttu-id="9971c-493">值</span><span class="sxs-lookup"><span data-stu-id="9971c-493">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-494">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-494">**Option name**</span></span> | <span data-ttu-id="9971c-495">csharp_space_between_method_call_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-495">csharp_space_between_method_call_parameter_list_parentheses</span></span> |
| <span data-ttu-id="9971c-496">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-496">**Applicable languages**</span></span> | <span data-ttu-id="9971c-497">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-497">C#</span></span> |
| <span data-ttu-id="9971c-498">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-498">**Introduced version**</span></span> | <span data-ttu-id="9971c-499">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-499">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-500">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-500">**Option values**</span></span> | <span data-ttu-id="9971c-501">`true` - 在方法调用的左括号之后和右括号之前放置空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-501">`true` - Place a space character after the opening parenthesis and before the closing parenthesis of a method call</span></span><br /><br /><span data-ttu-id="9971c-502">`false` - 删除方法调用的左括号之后和右括号之前的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-502">`false` - Remove space characters after the opening parenthesis and before the closing parenthesis of a method call</span></span> |

<span data-ttu-id="9971c-503">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-503">Code examples:</span></span>

```csharp
// csharp_space_between_method_call_parameter_list_parentheses = true
MyMethod( argument );

// csharp_space_between_method_call_parameter_list_parentheses = false
MyMethod(argument);
```

#### <a name="csharp_space_between_method_call_empty_parameter_list_parentheses"></a><span data-ttu-id="9971c-504">csharp_space_between_method_call_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-504">csharp_space_between_method_call_empty_parameter_list_parentheses</span></span>

|<span data-ttu-id="9971c-505">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-505">Property</span></span>|<span data-ttu-id="9971c-506">值</span><span class="sxs-lookup"><span data-stu-id="9971c-506">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-507">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-507">**Option name**</span></span> | <span data-ttu-id="9971c-508">csharp_space_between_method_call_empty_parameter_list_parentheses</span><span class="sxs-lookup"><span data-stu-id="9971c-508">csharp_space_between_method_call_empty_parameter_list_parentheses</span></span> |
| <span data-ttu-id="9971c-509">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-509">**Applicable languages**</span></span> | <span data-ttu-id="9971c-510">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-510">C#</span></span> |
| <span data-ttu-id="9971c-511">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-511">**Introduced version**</span></span> | <span data-ttu-id="9971c-512">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-512">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-513">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-513">**Option values**</span></span> | <span data-ttu-id="9971c-514">`true` - 在空参数列表的括号中插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-514">`true` - Insert space within empty argument list parentheses</span></span><br /><br /><span data-ttu-id="9971c-515">`false` - 删除空参数列表括号内的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-515">`false` - Remove space within empty argument list parentheses</span></span> |

<span data-ttu-id="9971c-516">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-516">Code examples:</span></span>

```csharp
// csharp_space_between_method_call_empty_parameter_list_parentheses = true
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo( );
}

// csharp_space_between_method_call_empty_parameter_list_parentheses = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharp_space_between_method_call_name_and_opening_parenthesis"></a><span data-ttu-id="9971c-517">csharp_space_between_method_call_name_and_opening_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-517">csharp_space_between_method_call_name_and_opening_parenthesis</span></span>

|<span data-ttu-id="9971c-518">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-518">Property</span></span>|<span data-ttu-id="9971c-519">值</span><span class="sxs-lookup"><span data-stu-id="9971c-519">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-520">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-520">**Option name**</span></span> | <span data-ttu-id="9971c-521">csharp_space_between_method_call_name_and_opening_parenthesis</span><span class="sxs-lookup"><span data-stu-id="9971c-521">csharp_space_between_method_call_name_and_opening_parenthesis</span></span> |
| <span data-ttu-id="9971c-522">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-522">**Applicable languages**</span></span> | <span data-ttu-id="9971c-523">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-523">C#</span></span> |
| <span data-ttu-id="9971c-524">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-524">**Introduced version**</span></span> | <span data-ttu-id="9971c-525">Visual Studio 2017 15.7 版</span><span class="sxs-lookup"><span data-stu-id="9971c-525">Visual Studio 2017 version 15.7</span></span> |
| <span data-ttu-id="9971c-526">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-526">**Option values**</span></span> | <span data-ttu-id="9971c-527">`true` - 在方法调用名称和左括号之间插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-527">`true` - Insert space between method call name and opening parenthesis</span></span><br /><br /><span data-ttu-id="9971c-528">`false` - 删除方法调用名称和左括号之间的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-528">`false` - Remove space between method call name and opening parenthesis</span></span> |

<span data-ttu-id="9971c-529">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-529">Code examples:</span></span>

```csharp
// csharp_space_between_method_call_name_and_opening_parenthesis = true
void Goo()
{
    Goo (1);
}

void Goo(int x)
{
    Goo ();
}

// csharp_space_between_method_call_name_and_opening_parenthesis = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharp_space_after_comma"></a><span data-ttu-id="9971c-530">csharp_space_after_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-530">csharp_space_after_comma</span></span>

|<span data-ttu-id="9971c-531">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-531">Property</span></span>|<span data-ttu-id="9971c-532">值</span><span class="sxs-lookup"><span data-stu-id="9971c-532">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-533">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-533">**Option name**</span></span> | <span data-ttu-id="9971c-534">csharp_space_after_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-534">csharp_space_after_comma</span></span> |
| <span data-ttu-id="9971c-535">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-535">**Applicable languages**</span></span> | <span data-ttu-id="9971c-536">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-536">C#</span></span> |
| <span data-ttu-id="9971c-537">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-537">**Option values**</span></span> | <span data-ttu-id="9971c-538">`true` - 在逗号后面插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-538">`true` - Insert space after a comma</span></span><br /><br /><span data-ttu-id="9971c-539">`false` - 删除逗号后面的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-539">`false` - Remove space after a comma</span></span> |

<span data-ttu-id="9971c-540">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-540">Code examples:</span></span>

```csharp
// csharp_space_after_comma = true
int[] x = new int[] { 1, 2, 3, 4, 5 };

// csharp_space_after_comma = false
int[] x = new int[] { 1,2,3,4,5 }
```

#### <a name="csharp_space_before_comma"></a><span data-ttu-id="9971c-541">csharp_space_before_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-541">csharp_space_before_comma</span></span>

|<span data-ttu-id="9971c-542">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-542">Property</span></span>|<span data-ttu-id="9971c-543">值</span><span class="sxs-lookup"><span data-stu-id="9971c-543">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-544">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-544">**Option name**</span></span> | <span data-ttu-id="9971c-545">csharp_space_before_comma</span><span class="sxs-lookup"><span data-stu-id="9971c-545">csharp_space_before_comma</span></span> |
| <span data-ttu-id="9971c-546">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-546">**Applicable languages**</span></span> | <span data-ttu-id="9971c-547">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-547">C#</span></span> |
| <span data-ttu-id="9971c-548">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-548">**Option values**</span></span> | <span data-ttu-id="9971c-549">`true` - 在逗号前插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-549">`true` - Insert space before a comma</span></span><br /><br /><span data-ttu-id="9971c-550">`false` - 删除逗号前的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-550">`false` - Remove space before a comma</span></span> |

<span data-ttu-id="9971c-551">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-551">Code examples:</span></span>

```csharp
// csharp_space_before_comma = true
int[] x = new int[] { 1 , 2 , 3 , 4 , 5 };

// csharp_space_before_comma = false
int[] x = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharp_space_after_dot"></a><span data-ttu-id="9971c-552">csharp_space_after_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-552">csharp_space_after_dot</span></span>

|<span data-ttu-id="9971c-553">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-553">Property</span></span>|<span data-ttu-id="9971c-554">值</span><span class="sxs-lookup"><span data-stu-id="9971c-554">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-555">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-555">**Option name**</span></span> | <span data-ttu-id="9971c-556">csharp_space_after_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-556">csharp_space_after_dot</span></span> |
| <span data-ttu-id="9971c-557">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-557">**Applicable languages**</span></span> | <span data-ttu-id="9971c-558">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-558">C#</span></span> |
| <span data-ttu-id="9971c-559">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-559">**Option values**</span></span> | <span data-ttu-id="9971c-560">`true` - 在点号后面插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-560">`true` - Insert space after a dot</span></span><br /><br /><span data-ttu-id="9971c-561">`false` - 删除点号后面的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-561">`false` - Remove space after a dot</span></span> |

<span data-ttu-id="9971c-562">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-562">Code examples:</span></span>

```csharp
// csharp_space_after_dot = true
this. Goo();

// csharp_space_after_dot = false
this.Goo();
```

#### <a name="csharp_space_before_dot"></a><span data-ttu-id="9971c-563">csharp_space_before_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-563">csharp_space_before_dot</span></span>

|<span data-ttu-id="9971c-564">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-564">Property</span></span>|<span data-ttu-id="9971c-565">值</span><span class="sxs-lookup"><span data-stu-id="9971c-565">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-566">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-566">**Option name**</span></span> | <span data-ttu-id="9971c-567">csharp_space_before_dot</span><span class="sxs-lookup"><span data-stu-id="9971c-567">csharp_space_before_dot</span></span> |
| <span data-ttu-id="9971c-568">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-568">**Applicable languages**</span></span> | <span data-ttu-id="9971c-569">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-569">C#</span></span> |
| <span data-ttu-id="9971c-570">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-570">**Option values**</span></span> | <span data-ttu-id="9971c-571">`true` - 在点前插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-571">`true` - Insert space before a dot</span></span> <br /><br /><span data-ttu-id="9971c-572">`false` - 删除点前的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-572">`false` - Remove space before a dot</span></span> |

<span data-ttu-id="9971c-573">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-573">Code examples:</span></span>

```csharp
// csharp_space_before_dot = true
this .Goo();

// csharp_space_before_dot = false
this.Goo();
```

#### <a name="csharp_space_after_semicolon_in_for_statement"></a><span data-ttu-id="9971c-574">csharp_space_after_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-574">csharp_space_after_semicolon_in_for_statement</span></span>

|<span data-ttu-id="9971c-575">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-575">Property</span></span>|<span data-ttu-id="9971c-576">值</span><span class="sxs-lookup"><span data-stu-id="9971c-576">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-577">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-577">**Option name**</span></span> | <span data-ttu-id="9971c-578">csharp_space_after_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-578">csharp_space_after_semicolon_in_for_statement</span></span> |
| <span data-ttu-id="9971c-579">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-579">**Applicable languages**</span></span> | <span data-ttu-id="9971c-580">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-580">C#</span></span> |
| <span data-ttu-id="9971c-581">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-581">**Option values**</span></span> | <span data-ttu-id="9971c-582">`true` - 在 `for` 语句中的每个分号后面插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-582">`true` - Insert space after each semicolon in a `for` statement</span></span><br /><br /><span data-ttu-id="9971c-583">`false` - 删除 `for` 语句中每个分号后的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-583">`false` - Remove space after each semicolon in a `for` statement</span></span> |

<span data-ttu-id="9971c-584">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-584">Code examples:</span></span>

```csharp
// csharp_space_after_semicolon_in_for_statement = true
for (int i = 0; i < x.Length; i++)

// csharp_space_after_semicolon_in_for_statement = false
for (int i = 0;i < x.Length;i++)
```

##### <a name="csharp_space_before_semicolon_in_for_statement"></a><span data-ttu-id="9971c-585">csharp_space_before_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-585">csharp_space_before_semicolon_in_for_statement</span></span>

|<span data-ttu-id="9971c-586">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-586">Property</span></span>|<span data-ttu-id="9971c-587">值</span><span class="sxs-lookup"><span data-stu-id="9971c-587">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-588">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-588">**Option name**</span></span> | <span data-ttu-id="9971c-589">csharp_space_before_semicolon_in_for_statement</span><span class="sxs-lookup"><span data-stu-id="9971c-589">csharp_space_before_semicolon_in_for_statement</span></span> |
| <span data-ttu-id="9971c-590">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-590">**Applicable languages**</span></span> | <span data-ttu-id="9971c-591">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-591">C#</span></span> |
| <span data-ttu-id="9971c-592">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-592">**Option values**</span></span> | <span data-ttu-id="9971c-593">`true` - 在 `for` 语句中的每个分号前插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-593">`true` - Insert space before each semicolon in a `for` statement</span></span> <br /><br /><span data-ttu-id="9971c-594">`false` - 删除 `for` 语句中每个分号前的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-594">`false` - Remove space before each semicolon in a `for` statement</span></span> |

<span data-ttu-id="9971c-595">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-595">Code examples:</span></span>

```csharp
// csharp_space_before_semicolon_in_for_statement = true
for (int i = 0 ; i < x.Length ; i++)

// csharp_space_before_semicolon_in_for_statement = false
for (int i = 0; i < x.Length; i++)
```

#### <a name="csharp_space_around_declaration_statements"></a><span data-ttu-id="9971c-596">csharp_space_around_declaration_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-596">csharp_space_around_declaration_statements</span></span>

|<span data-ttu-id="9971c-597">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-597">Property</span></span>|<span data-ttu-id="9971c-598">值</span><span class="sxs-lookup"><span data-stu-id="9971c-598">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-599">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-599">**Option name**</span></span> | <span data-ttu-id="9971c-600">csharp_space_around_declaration_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-600">csharp_space_around_declaration_statements</span></span> |
| <span data-ttu-id="9971c-601">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-601">**Applicable languages**</span></span> | <span data-ttu-id="9971c-602">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-602">C#</span></span> |
| <span data-ttu-id="9971c-603">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-603">**Option values**</span></span> | <span data-ttu-id="9971c-604">`ignore` - 不删除声明语句中多余的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-604">`ignore` - Don't remove extra space characters in declaration statements</span></span><br /><br /><span data-ttu-id="9971c-605">`false` - 删除声明语句中多余的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-605">`false` - Remove extra space characters in declaration statements</span></span> |

<span data-ttu-id="9971c-606">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-606">Code examples:</span></span>

```csharp
// csharp_space_around_declaration_statements = ignore
int    x    =    0   ;

// csharp_space_around_declaration_statements = false
int x = 0;
```

#### <a name="csharp_space_before_open_square_brackets"></a><span data-ttu-id="9971c-607">csharp_space_before_open_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-607">csharp_space_before_open_square_brackets</span></span>

|<span data-ttu-id="9971c-608">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-608">Property</span></span>|<span data-ttu-id="9971c-609">值</span><span class="sxs-lookup"><span data-stu-id="9971c-609">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-610">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-610">**Option name**</span></span> | <span data-ttu-id="9971c-611">csharp_space_before_open_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-611">csharp_space_before_open_square_brackets</span></span> |
| <span data-ttu-id="9971c-612">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-612">**Applicable languages**</span></span> | <span data-ttu-id="9971c-613">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-613">C#</span></span> |
| <span data-ttu-id="9971c-614">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-614">**Option values**</span></span> | <span data-ttu-id="9971c-615">`true` - 在左方括号 `[` 前插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-615">`true` - Insert space before opening square brackets `[`</span></span> <br /><br /><span data-ttu-id="9971c-616">`false` - 删除左方括号 `[` 前的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-616">`false` - Remove space before opening square brackets `[`</span></span> |

<span data-ttu-id="9971c-617">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-617">Code examples:</span></span>

```csharp
// csharp_space_before_open_square_brackets = true
int [] numbers = new int [] { 1, 2, 3, 4, 5 };

// csharp_space_before_open_square_brackets = false
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharp_space_between_empty_square_brackets"></a><span data-ttu-id="9971c-618">csharp_space_between_empty_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-618">csharp_space_between_empty_square_brackets</span></span>

|<span data-ttu-id="9971c-619">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-619">Property</span></span>|<span data-ttu-id="9971c-620">值</span><span class="sxs-lookup"><span data-stu-id="9971c-620">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-621">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-621">**Option name**</span></span> | <span data-ttu-id="9971c-622">csharp_space_between_empty_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-622">csharp_space_between_empty_square_brackets</span></span> |
| <span data-ttu-id="9971c-623">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-623">**Applicable languages**</span></span> | <span data-ttu-id="9971c-624">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-624">C#</span></span> |
| <span data-ttu-id="9971c-625">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-625">**Option values**</span></span> | <span data-ttu-id="9971c-626">`true` - 在空方括号 `[ ]` 之间插入空格</span><span class="sxs-lookup"><span data-stu-id="9971c-626">`true` - Insert space between empty square brackets `[ ]`</span></span> <br /><br /><span data-ttu-id="9971c-627">`false` - 删除空方括号 `[]` 之间的空格</span><span class="sxs-lookup"><span data-stu-id="9971c-627">`false` - Remove space between empty square brackets `[]`</span></span> |

<span data-ttu-id="9971c-628">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-628">Code examples:</span></span>

```csharp
// csharp_space_between_empty_square_brackets = true
int[ ] numbers = new int[ ] { 1, 2, 3, 4, 5 };

// csharp_space_between_empty_square_brackets = false
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharp_space_between_square_brackets"></a><span data-ttu-id="9971c-629">csharp_space_between_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-629">csharp_space_between_square_brackets</span></span>

|<span data-ttu-id="9971c-630">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-630">Property</span></span>|<span data-ttu-id="9971c-631">值</span><span class="sxs-lookup"><span data-stu-id="9971c-631">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-632">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-632">**Option name**</span></span> | <span data-ttu-id="9971c-633">csharp_space_between_square_brackets</span><span class="sxs-lookup"><span data-stu-id="9971c-633">csharp_space_between_square_brackets</span></span> |
| <span data-ttu-id="9971c-634">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-634">**Applicable languages**</span></span> | <span data-ttu-id="9971c-635">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-635">C#</span></span> |
| <span data-ttu-id="9971c-636">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-636">**Option values**</span></span> | <span data-ttu-id="9971c-637">`true` - 在非空方括号 `[ 0 ]` 中插入空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-637">`true` - Insert space characters in non-empty square brackets `[ 0 ]`</span></span> <br /><br /><span data-ttu-id="9971c-638">`false` - 删除非空方括号 `[0]` 中的空格字符</span><span class="sxs-lookup"><span data-stu-id="9971c-638">`false` - Remove space characters in non-empty square brackets `[0]`</span></span> |

<span data-ttu-id="9971c-639">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-639">Code examples:</span></span>

```csharp
// csharp_space_between_square_brackets = true
int index = numbers[ 0 ];

// csharp_space_between_square_brackets = false
int index = numbers[0];
```

### <a name="wrap-options"></a><span data-ttu-id="9971c-640">换行选项</span><span class="sxs-lookup"><span data-stu-id="9971c-640">Wrap options</span></span>

<span data-ttu-id="9971c-641">这些格式设置规则与语句和代码块中单一行以及单独的行的使用有关。</span><span class="sxs-lookup"><span data-stu-id="9971c-641">These formatting rules concern the use of single lines versus separate lines for statements and code blocks.</span></span>

<span data-ttu-id="9971c-642">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-642">Example *.editorconfig* file:</span></span>

```ini
# CSharp formatting rules:
[*.cs]
csharp_preserve_single_line_statements = true
csharp_preserve_single_line_blocks = true
```

#### <a name="csharp_preserve_single_line_statements"></a><span data-ttu-id="9971c-643">csharp_preserve_single_line_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-643">csharp_preserve_single_line_statements</span></span>

|<span data-ttu-id="9971c-644">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-644">Property</span></span>|<span data-ttu-id="9971c-645">值</span><span class="sxs-lookup"><span data-stu-id="9971c-645">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-646">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-646">**Option name**</span></span> | <span data-ttu-id="9971c-647">csharp_preserve_single_line_statements</span><span class="sxs-lookup"><span data-stu-id="9971c-647">csharp_preserve_single_line_statements</span></span> |
| <span data-ttu-id="9971c-648">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-648">**Applicable languages**</span></span> | <span data-ttu-id="9971c-649">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-649">C#</span></span> |
| <span data-ttu-id="9971c-650">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-650">**Introduced version**</span></span> | <span data-ttu-id="9971c-651">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-651">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-652">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-652">**Option values**</span></span> | <span data-ttu-id="9971c-653">`true` - 将语句和成员声明保留在同一行上</span><span class="sxs-lookup"><span data-stu-id="9971c-653">`true` - Leave statements and member declarations on the same line</span></span><br /><br /><span data-ttu-id="9971c-654">`false` - 将语句和成员声明保留在不同行上</span><span class="sxs-lookup"><span data-stu-id="9971c-654">`false` - Leave statements and member declarations on different lines</span></span> |

<span data-ttu-id="9971c-655">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-655">Code examples:</span></span>

```csharp
//csharp_preserve_single_line_statements = true
int i = 0; string name = "John";

//csharp_preserve_single_line_statements = false
int i = 0;
string name = "John";
```

#### <a name="csharp_preserve_single_line_blocks"></a><span data-ttu-id="9971c-656">csharp_preserve_single_line_blocks</span><span class="sxs-lookup"><span data-stu-id="9971c-656">csharp_preserve_single_line_blocks</span></span>

|<span data-ttu-id="9971c-657">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-657">Property</span></span>|<span data-ttu-id="9971c-658">值</span><span class="sxs-lookup"><span data-stu-id="9971c-658">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-659">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-659">**Option name**</span></span> | <span data-ttu-id="9971c-660">csharp_preserve_single_line_blocks</span><span class="sxs-lookup"><span data-stu-id="9971c-660">csharp_preserve_single_line_blocks</span></span> |
| <span data-ttu-id="9971c-661">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-661">**Applicable languages**</span></span> | <span data-ttu-id="9971c-662">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-662">C#</span></span> |
| <span data-ttu-id="9971c-663">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-663">**Introduced version**</span></span> | <span data-ttu-id="9971c-664">Visual Studio 2017 版本 15.3</span><span class="sxs-lookup"><span data-stu-id="9971c-664">Visual Studio 2017 version 15.3</span></span> |
| <span data-ttu-id="9971c-665">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-665">**Option values**</span></span> | <span data-ttu-id="9971c-666">`true` - 将代码块保留在单个行上</span><span class="sxs-lookup"><span data-stu-id="9971c-666">`true` - Leave code block on single line</span></span><br /><br /><span data-ttu-id="9971c-667">`false` - 将代码块保留在单独的行上</span><span class="sxs-lookup"><span data-stu-id="9971c-667">`false` - Leave code block on separate lines</span></span> |

<span data-ttu-id="9971c-668">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-668">Code examples:</span></span>

```csharp
//csharp_preserve_single_line_blocks = true
public int Foo { get; set; }

//csharp_preserve_single_line_blocks = false
public int MyProperty
{
    get; set;
}
```

### <a name="using-directive-options"></a><span data-ttu-id="9971c-669">using 指令选项</span><span class="sxs-lookup"><span data-stu-id="9971c-669">Using directive options</span></span>

<span data-ttu-id="9971c-670">此格式设置规则涉及到使用放置在命名空间内和外的 using 指令。</span><span class="sxs-lookup"><span data-stu-id="9971c-670">This formatting rule concerns the use of using directives being placed inside versus outside a namespace.</span></span>

<span data-ttu-id="9971c-671">.editorconfig 文件示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-671">Example *.editorconfig* file:</span></span>

```ini
# 'using' directive preferences
[*.cs]
csharp_using_directive_placement = outside_namespace
csharp_using_directive_placement = inside_namespace
```

#### <a name="csharp_using_directive_placement"></a><span data-ttu-id="9971c-672">csharp_using_directive_placement</span><span class="sxs-lookup"><span data-stu-id="9971c-672">csharp_using_directive_placement</span></span>

|<span data-ttu-id="9971c-673">Property</span><span class="sxs-lookup"><span data-stu-id="9971c-673">Property</span></span>|<span data-ttu-id="9971c-674">值</span><span class="sxs-lookup"><span data-stu-id="9971c-674">Value</span></span>|
|-|-|
| <span data-ttu-id="9971c-675">**选项名称**</span><span class="sxs-lookup"><span data-stu-id="9971c-675">**Option name**</span></span> | <span data-ttu-id="9971c-676">csharp_using_directive_placement</span><span class="sxs-lookup"><span data-stu-id="9971c-676">csharp_using_directive_placement</span></span> |
| <span data-ttu-id="9971c-677">**适用的语言**</span><span class="sxs-lookup"><span data-stu-id="9971c-677">**Applicable languages**</span></span> | <span data-ttu-id="9971c-678">C#</span><span class="sxs-lookup"><span data-stu-id="9971c-678">C#</span></span> |
| <span data-ttu-id="9971c-679">**引入的版本**</span><span class="sxs-lookup"><span data-stu-id="9971c-679">**Introduced version**</span></span> | <span data-ttu-id="9971c-680">Visual Studio 2019 版本 16.1</span><span class="sxs-lookup"><span data-stu-id="9971c-680">Visual Studio 2019 version 16.1</span></span> |
| <span data-ttu-id="9971c-681">**选项值**</span><span class="sxs-lookup"><span data-stu-id="9971c-681">**Option values**</span></span> | <span data-ttu-id="9971c-682">`outside_namespace` - 将 using 指令保留在命名空间之外</span><span class="sxs-lookup"><span data-stu-id="9971c-682">`outside_namespace` - Leave using directives outside namespace</span></span><br /><br /><span data-ttu-id="9971c-683">`inside_namespace` - 将 using 指令保留在命名空间之内</span><span class="sxs-lookup"><span data-stu-id="9971c-683">`inside_namespace` - Leave using directives inside namespace</span></span> |

<span data-ttu-id="9971c-684">代码示例：</span><span class="sxs-lookup"><span data-stu-id="9971c-684">Code examples:</span></span>

```csharp
// csharp_using_directive_placement = outside_namespace
using System;

namespace Conventions
{

}

// csharp_using_directive_placement = inside_namespace
namespace Conventions
{
    using System;
}
```

## <a name="see-also"></a><span data-ttu-id="9971c-685">请参阅</span><span class="sxs-lookup"><span data-stu-id="9971c-685">See also</span></span>

- [<span data-ttu-id="9971c-686">语言规则</span><span class="sxs-lookup"><span data-stu-id="9971c-686">Language rules</span></span>](language-rules.md)
- [<span data-ttu-id="9971c-687">命名规则</span><span class="sxs-lookup"><span data-stu-id="9971c-687">Naming rules</span></span>](naming-rules.md)
- [<span data-ttu-id="9971c-688">.NET 代码样式规则参考</span><span class="sxs-lookup"><span data-stu-id="9971c-688">.NET code style rules reference</span></span>](index.md)
