---
title: 代码样式语言规则
description: '了解使用 c # 和 Visual Basic 语言构造的不同代码样式规则。'
ms.date: 09/25/2020
ms.topic: reference
author: gewarren
ms.author: gewarren
dev_langs:
- CSharp
- VB
helpviewer_keywords:
- language code style rules [EditorConfig]
- language rules
- EditorConfig language conventions
ms.openlocfilehash: b77d9aa2a528a6cf540babd5e5acc148e48c489c
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96591097"
---
# <a name="language-rules"></a><span data-ttu-id="e544e-103">语言规则</span><span class="sxs-lookup"><span data-stu-id="e544e-103">Language rules</span></span>

<span data-ttu-id="e544e-104">代码样式语言规则会影响 .NET 编程语言的各种构造，例如，如何使用修饰符和括号。</span><span class="sxs-lookup"><span data-stu-id="e544e-104">Code style language rules affect how various constructs of .NET programming languages, for example, modifiers and parentheses, are used.</span></span> <span data-ttu-id="e544e-105">这些规则分为以下几类：</span><span class="sxs-lookup"><span data-stu-id="e544e-105">The rules fall into the following categories:</span></span>

- <span data-ttu-id="e544e-106">[.Net 样式规则](#net-style-rules)：适用于 c # 和 Visual Basic 的规则。</span><span class="sxs-lookup"><span data-stu-id="e544e-106">[.NET style rules](#net-style-rules): Rules that apply to both C# and Visual Basic.</span></span> <span data-ttu-id="e544e-107">这些规则的 EditorConfig 选项名称以前缀开头 `dotnet_style_` 。</span><span class="sxs-lookup"><span data-stu-id="e544e-107">The EditorConfig option names for these rules start with `dotnet_style_` prefix.</span></span>
- <span data-ttu-id="e544e-108">[C # 样式规则](#c-style-rules)：仅特定于 c # 语言的规则。</span><span class="sxs-lookup"><span data-stu-id="e544e-108">[C# style rules](#c-style-rules): Rules that are specific to C# language only.</span></span> <span data-ttu-id="e544e-109">这些规则的 EditorConfig 选项名称以前缀开头 `csharp_style_` 。</span><span class="sxs-lookup"><span data-stu-id="e544e-109">The EditorConfig option names for these rules start with `csharp_style_` prefix.</span></span>
- <span data-ttu-id="e544e-110">[Visual Basic 样式规则](#visual-basic-style-rules)：仅特定于 Visual Bsic 语言的规则。</span><span class="sxs-lookup"><span data-stu-id="e544e-110">[Visual Basic style rules](#visual-basic-style-rules): Rules that are specific to Visual Bsic language only.</span></span> <span data-ttu-id="e544e-111">这些规则的 EditorConfig 选项名称以前缀开头 `visual_basic_style_` 。</span><span class="sxs-lookup"><span data-stu-id="e544e-111">The EditorConfig option names for these rules start with `visual_basic_style_` prefix.</span></span>

## <a name="option-format"></a><span data-ttu-id="e544e-112">选项格式</span><span class="sxs-lookup"><span data-stu-id="e544e-112">Option format</span></span>

<span data-ttu-id="e544e-113">可在 EditorConfig 文件中指定语言规则的选项，格式如下：</span><span class="sxs-lookup"><span data-stu-id="e544e-113">Options for language rules can be specified in an EditorConfig file with the following format:</span></span>

`option_name = value:severity`

- <span data-ttu-id="e544e-114">**值**：对于每个语言规则，指定一个值，用于定义是否喜欢样式。</span><span class="sxs-lookup"><span data-stu-id="e544e-114">**Value**: For each language rule, you specify a value that defines if or when to prefer the style.</span></span> <span data-ttu-id="e544e-115">许多规则都接受 `true` 值（以此样式为首选项）或 `false` 值（不以此样式为首选项）。</span><span class="sxs-lookup"><span data-stu-id="e544e-115">Many rules accept a value of `true` (prefer this style) or `false` (do not prefer this style).</span></span> <span data-ttu-id="e544e-116">其他规则接受 `when_on_single_line` 或 `never` 等值。</span><span class="sxs-lookup"><span data-stu-id="e544e-116">Other rules accept values such as `when_on_single_line` or `never`.</span></span>
- <span data-ttu-id="e544e-117">**严重性**：规则的第二部分指定规则的 [严重性级别](../configuration-options.md#severity-level) 。</span><span class="sxs-lookup"><span data-stu-id="e544e-117">**Severity**: The second part of the rule specifies the [severity level](../configuration-options.md#severity-level) for the rule.</span></span> <span data-ttu-id="e544e-118">作为上述选项语法的一部分的严重性规范仅适用于开发 Ide （如 Visual Studio）。</span><span class="sxs-lookup"><span data-stu-id="e544e-118">Severity specification as part of the above option syntax is only respected inside development IDEs, such as Visual Studio.</span></span> <span data-ttu-id="e544e-119">C # 或 VB 编译器不理解此设置，因此在生成过程中不会考虑此设置。</span><span class="sxs-lookup"><span data-stu-id="e544e-119">This setting is not understood by the C# or VB compilers, hence not respected during build.</span></span> <span data-ttu-id="e544e-120">相反，若要强制生成代码样式规则，应使用分析器的基于规则 ID 的严重性配置语法来设置严重性。</span><span class="sxs-lookup"><span data-stu-id="e544e-120">Instead, to enforce code style rules on build, you should set the severity by using the rule ID-based severity configuration syntax for analyzers.</span></span> <span data-ttu-id="e544e-121">语法采用形式 `dotnet_diagnostic.<rule ID>.severity = <severity>`（例如，`dotnet_diagnostic.IDE0040.severity = silent`）。</span><span class="sxs-lookup"><span data-stu-id="e544e-121">The syntax takes the form `dotnet_diagnostic.<rule ID>.severity = <severity>`, for example, `dotnet_diagnostic.IDE0040.severity = silent`.</span></span> <span data-ttu-id="e544e-122">有关详细信息，请参阅此 [GitHub 问题](https://github.com/dotnet/roslyn/issues/44201)。</span><span class="sxs-lookup"><span data-stu-id="e544e-122">For more information, see this [GitHub issue](https://github.com/dotnet/roslyn/issues/44201).</span></span>

> [!TIP]
>
> <span data-ttu-id="e544e-123">自 Visual Studio 2019 版本 16.3 起，在样式冲突发生之后，可以在[快速操作](/visualstudio/ide/quick-actions)灯泡菜单中配置代码样式规则。</span><span class="sxs-lookup"><span data-stu-id="e544e-123">Starting in Visual Studio 2019 version 16.3, you can configure code style rules from the [Quick Actions](/visualstudio/ide/quick-actions) light bulb menu after a style violation occurs.</span></span> <span data-ttu-id="e544e-124">有关详细信息，请参阅 [在 Visual Studio 中自动配置代码样式](/visualstudio/ide/editorconfig-language-conventions#automatically-configure-code-styles-in-visual-studio)。</span><span class="sxs-lookup"><span data-stu-id="e544e-124">For more information, see [Automatically configure code styles in Visual Studio](/visualstudio/ide/editorconfig-language-conventions#automatically-configure-code-styles-in-visual-studio).</span></span>

## <a name="net-style-rules"></a><span data-ttu-id="e544e-125">.NET 样式规则</span><span class="sxs-lookup"><span data-stu-id="e544e-125">.NET style rules</span></span>

<span data-ttu-id="e544e-126">本节中的样式规则均适用于 C# 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="e544e-126">The style rules in this section are applicable to both C# and Visual Basic.</span></span>

- [<span data-ttu-id="e544e-127">"this." 和 "Me." 限定符</span><span class="sxs-lookup"><span data-stu-id="e544e-127">'this.' and 'Me.' qualifiers</span></span>](ide0003-ide0009.md)
  - [<span data-ttu-id="e544e-128">dotnet_style_qualification_for_field</span><span class="sxs-lookup"><span data-stu-id="e544e-128">dotnet_style_qualification_for_field</span></span>](ide0003-ide0009.md#dotnet_style_qualification_for_field)
  - [<span data-ttu-id="e544e-129">dotnet_style_qualification_for_property</span><span class="sxs-lookup"><span data-stu-id="e544e-129">dotnet_style_qualification_for_property</span></span>](ide0003-ide0009.md#dotnet_style_qualification_for_property)
  - [<span data-ttu-id="e544e-130">dotnet_style_qualification_for_method</span><span class="sxs-lookup"><span data-stu-id="e544e-130">dotnet_style_qualification_for_method</span></span>](ide0003-ide0009.md#dotnet_style_qualification_for_method)
  - [<span data-ttu-id="e544e-131">dotnet_style_qualification_for_event</span><span class="sxs-lookup"><span data-stu-id="e544e-131">dotnet_style_qualification_for_event</span></span>](ide0003-ide0009.md#dotnet_style_qualification_for_event)
- [<span data-ttu-id="e544e-132">语言关键字，而非类型引用的框架类型名称</span><span class="sxs-lookup"><span data-stu-id="e544e-132">Language keywords instead of framework type names for type references</span></span>](ide0049.md)
  - [<span data-ttu-id="e544e-133">dotnet_style_predefined_type_for_locals_parameters_members</span><span class="sxs-lookup"><span data-stu-id="e544e-133">dotnet_style_predefined_type_for_locals_parameters_members</span></span>](ide0049.md#dotnet_style_predefined_type_for_locals_parameters_members)
  - [<span data-ttu-id="e544e-134">dotnet_style_predefined_type_for_member_access</span><span class="sxs-lookup"><span data-stu-id="e544e-134">dotnet_style_predefined_type_for_member_access</span></span>](ide0049.md#dotnet_style_predefined_type_for_member_access)
- [<span data-ttu-id="e544e-135">修饰符首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-135">Modifier preferences</span></span>](modifier-preferences.md#net-modifier-preferences)
  - [<span data-ttu-id="e544e-136">dotnet_style_require_accessibility_modifiers</span><span class="sxs-lookup"><span data-stu-id="e544e-136">dotnet_style_require_accessibility_modifiers</span></span>](ide0040.md#dotnet_style_require_accessibility_modifiers)
  - [<span data-ttu-id="e544e-137">csharp_preferred_modifier_order</span><span class="sxs-lookup"><span data-stu-id="e544e-137">csharp_preferred_modifier_order</span></span>](ide0036.md#csharp_preferred_modifier_order)
  - [<span data-ttu-id="e544e-138">visual_basic_preferred_modifier_order</span><span class="sxs-lookup"><span data-stu-id="e544e-138">visual_basic_preferred_modifier_order</span></span>](ide0036.md#visual_basic_preferred_modifier_order)
  - [<span data-ttu-id="e544e-139">dotnet_style_readonly_field</span><span class="sxs-lookup"><span data-stu-id="e544e-139">dotnet_style_readonly_field</span></span>](ide0044.md#dotnet_style_readonly_field)
- [<span data-ttu-id="e544e-140">括号首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-140">Parentheses preferences</span></span>](ide0047-ide0048.md)
  - [<span data-ttu-id="e544e-141">dotnet_style_parentheses_in_arithmetic_binary_operators</span><span class="sxs-lookup"><span data-stu-id="e544e-141">dotnet_style_parentheses_in_arithmetic_binary_operators</span></span>](ide0047-ide0048.md#dotnet_style_parentheses_in_arithmetic_binary_operators)
  - [<span data-ttu-id="e544e-142">dotnet_style_parentheses_in_relational_binary_operators</span><span class="sxs-lookup"><span data-stu-id="e544e-142">dotnet_style_parentheses_in_relational_binary_operators</span></span>](ide0047-ide0048.md#dotnet_style_parentheses_in_relational_binary_operators)
  - [<span data-ttu-id="e544e-143">dotnet_style_parentheses_in_other_binary_operators</span><span class="sxs-lookup"><span data-stu-id="e544e-143">dotnet_style_parentheses_in_other_binary_operators</span></span>](ide0047-ide0048.md#dotnet_style_parentheses_in_other_binary_operators)
  - [<span data-ttu-id="e544e-144">dotnet_style_parentheses_in_other_operators</span><span class="sxs-lookup"><span data-stu-id="e544e-144">dotnet_style_parentheses_in_other_operators</span></span>](ide0047-ide0048.md#dotnet_style_parentheses_in_other_operators)
- [<span data-ttu-id="e544e-145">表达式级首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-145">Expression-level preferences</span></span>](expression-level-preferences.md#net-expression-level-preferences)
  - [<span data-ttu-id="e544e-146">dotnet_style_object_initializer</span><span class="sxs-lookup"><span data-stu-id="e544e-146">dotnet_style_object_initializer</span></span>](ide0017.md#dotnet_style_object_initializer)
  - [<span data-ttu-id="e544e-147">dotnet_style_collection_initializer</span><span class="sxs-lookup"><span data-stu-id="e544e-147">dotnet_style_collection_initializer</span></span>](ide0028.md#dotnet_style_collection_initializer)
  - [<span data-ttu-id="e544e-148">dotnet_style_explicit_tuple_names</span><span class="sxs-lookup"><span data-stu-id="e544e-148">dotnet_style_explicit_tuple_names</span></span>](ide0033.md#dotnet_style_explicit_tuple_names)
  - [<span data-ttu-id="e544e-149">dotnet_style_prefer_inferred_tuple_names</span><span class="sxs-lookup"><span data-stu-id="e544e-149">dotnet_style_prefer_inferred_tuple_names</span></span>](ide0037.md#dotnet_style_prefer_inferred_tuple_names)
  - [<span data-ttu-id="e544e-150">dotnet_style_prefer_inferred_anonymous_type_member_names</span><span class="sxs-lookup"><span data-stu-id="e544e-150">dotnet_style_prefer_inferred_anonymous_type_member_names</span></span>](ide0037.md#dotnet_style_prefer_inferred_anonymous_type_member_names)
  - [<span data-ttu-id="e544e-151">dotnet_style_prefer_auto_properties</span><span class="sxs-lookup"><span data-stu-id="e544e-151">dotnet_style_prefer_auto_properties</span></span>](ide0032.md#dotnet_style_prefer_auto_properties)
  - [<span data-ttu-id="e544e-152">dotnet_style_prefer_conditional_expression_over_assignment</span><span class="sxs-lookup"><span data-stu-id="e544e-152">dotnet_style_prefer_conditional_expression_over_assignment</span></span>](ide0045.md#dotnet_style_prefer_conditional_expression_over_assignment)
  - [<span data-ttu-id="e544e-153">dotnet_style_prefer_conditional_expression_over_return</span><span class="sxs-lookup"><span data-stu-id="e544e-153">dotnet_style_prefer_conditional_expression_over_return</span></span>](ide0046.md#dotnet_style_prefer_conditional_expression_over_return)
  - [<span data-ttu-id="e544e-154">dotnet_style_prefer_compound_assignment</span><span class="sxs-lookup"><span data-stu-id="e544e-154">dotnet_style_prefer_compound_assignment</span></span>](ide0054-ide0074.md#dotnet_style_prefer_compound_assignment)
  - [<span data-ttu-id="e544e-155">dotnet_style_prefer_simplified_interpolation</span><span class="sxs-lookup"><span data-stu-id="e544e-155">dotnet_style_prefer_simplified_interpolation</span></span>](ide0071.md#dotnet_style_prefer_simplified_interpolation)
  - [<span data-ttu-id="e544e-156">dotnet_style_prefer_simplified_boolean_expressions</span><span class="sxs-lookup"><span data-stu-id="e544e-156">dotnet_style_prefer_simplified_boolean_expressions</span></span>](ide0075.md#dotnet_style_prefer_simplified_boolean_expressions)
  - <span data-ttu-id="e544e-157">[向 switch 语句添加缺少的事例](ide0010.md) -此规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-157">[Add missing cases to switch statement](ide0010.md) - This rule has no code style option.</span></span>
  - <span data-ttu-id="e544e-158">[将匿名类型转换为元组](ide0050.md) -此规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-158">[Convert anonymous type to tuple](ide0050.md) - This rule has no code style option.</span></span>
  - <span data-ttu-id="e544e-159">[使用 "system.string"](ide0070.md) -此规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-159">[Use 'System.HashCode.Combine'](ide0070.md) - This rule has no code style option.</span></span>
  - <span data-ttu-id="e544e-160">[将 "typeof" 转换为 "nameof"](ide0082.md) -该规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-160">[Convert 'typeof' to 'nameof'](ide0082.md) - This rule has no code style option.</span></span>
- [<span data-ttu-id="e544e-161">Null 检查首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-161">Null-checking preferences</span></span>](null-checking-preferences.md#net-null-checking-preferences)
  - [<span data-ttu-id="e544e-162">dotnet_style_coalesce_expression</span><span class="sxs-lookup"><span data-stu-id="e544e-162">dotnet_style_coalesce_expression</span></span>](ide0029-ide0030.md#dotnet_style_coalesce_expression)
  - [<span data-ttu-id="e544e-163">dotnet_style_null_propagation</span><span class="sxs-lookup"><span data-stu-id="e544e-163">dotnet_style_null_propagation</span></span>](ide0031.md#dotnet_style_null_propagation)
  - [<span data-ttu-id="e544e-164">dotnet_style_prefer_is_null_check_over_reference_equality_method</span><span class="sxs-lookup"><span data-stu-id="e544e-164">dotnet_style_prefer_is_null_check_over_reference_equality_method</span></span>](ide0041.md#dotnet_style_prefer_is_null_check_over_reference_equality_method)
- [<span data-ttu-id="e544e-165">文件头首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-165">File header preferences</span></span>](ide0073.md)
  - [<span data-ttu-id="e544e-166">file_header_template</span><span class="sxs-lookup"><span data-stu-id="e544e-166">file_header_template</span></span>](ide0073.md#file_header_template)

## <a name="c-style-rules"></a><span data-ttu-id="e544e-167">C # 样式规则</span><span class="sxs-lookup"><span data-stu-id="e544e-167">C# style rules</span></span>

<span data-ttu-id="e544e-168">本节中的样式规则仅适用于 c # 语言。</span><span class="sxs-lookup"><span data-stu-id="e544e-168">The style rules in this section are applicable to C# language only.</span></span>

- [<span data-ttu-id="e544e-169">"var" 首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-169">'var' preferences</span></span>](ide0007-ide0008.md)
  - [<span data-ttu-id="e544e-170">csharp_style_var_for_built_in_types</span><span class="sxs-lookup"><span data-stu-id="e544e-170">csharp_style_var_for_built_in_types</span></span>](ide0007-ide0008.md#csharp_style_var_for_built_in_types)
  - [<span data-ttu-id="e544e-171">csharp_style_var_when_type_is_apparent</span><span class="sxs-lookup"><span data-stu-id="e544e-171">csharp_style_var_when_type_is_apparent</span></span>](ide0007-ide0008.md#csharp_style_var_when_type_is_apparent)
  - [<span data-ttu-id="e544e-172">csharp_style_var_elsewhere</span><span class="sxs-lookup"><span data-stu-id="e544e-172">csharp_style_var_elsewhere</span></span>](ide0007-ide0008.md#csharp_style_var_elsewhere)
- [<span data-ttu-id="e544e-173">Expression-Bodied 成员</span><span class="sxs-lookup"><span data-stu-id="e544e-173">Expression-bodied members</span></span>](expression-bodied-members.md)
  - [<span data-ttu-id="e544e-174">csharp_style_expression_bodied_methods</span><span class="sxs-lookup"><span data-stu-id="e544e-174">csharp_style_expression_bodied_methods</span></span>](ide0022.md#csharp_style_expression_bodied_methods)
  - [<span data-ttu-id="e544e-175">csharp_style_expression_bodied_constructors</span><span class="sxs-lookup"><span data-stu-id="e544e-175">csharp_style_expression_bodied_constructors</span></span>](ide0021.md#csharp_style_expression_bodied_constructors)
  - [<span data-ttu-id="e544e-176">csharp_style_expression_bodied_operators</span><span class="sxs-lookup"><span data-stu-id="e544e-176">csharp_style_expression_bodied_operators</span></span>](ide0023-ide0024.md#csharp_style_expression_bodied_operators)
  - [<span data-ttu-id="e544e-177">csharp_style_expression_bodied_properties</span><span class="sxs-lookup"><span data-stu-id="e544e-177">csharp_style_expression_bodied_properties</span></span>](ide0025.md#csharp_style_expression_bodied_properties)
  - [<span data-ttu-id="e544e-178">csharp_style_expression_bodied_indexers</span><span class="sxs-lookup"><span data-stu-id="e544e-178">csharp_style_expression_bodied_indexers</span></span>](ide0026.md#csharp_style_expression_bodied_indexers)
  - [<span data-ttu-id="e544e-179">csharp_style_expression_bodied_accessors</span><span class="sxs-lookup"><span data-stu-id="e544e-179">csharp_style_expression_bodied_accessors</span></span>](ide0027.md#csharp_style_expression_bodied_accessors)
  - [<span data-ttu-id="e544e-180">csharp_style_expression_bodied_lambdas</span><span class="sxs-lookup"><span data-stu-id="e544e-180">csharp_style_expression_bodied_lambdas</span></span>](ide0053.md#csharp_style_expression_bodied_lambdas)
  - [<span data-ttu-id="e544e-181">csharp_style_expression_bodied_local_functions</span><span class="sxs-lookup"><span data-stu-id="e544e-181">csharp_style_expression_bodied_local_functions</span></span>](ide0061.md#csharp_style_expression_bodied_local_functions)
- [<span data-ttu-id="e544e-182">模式匹配首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-182">Pattern matching preferences</span></span>](pattern-matching-preferences.md)
  - [<span data-ttu-id="e544e-183">csharp_style_pattern_matching_over_is_with_cast_check</span><span class="sxs-lookup"><span data-stu-id="e544e-183">csharp_style_pattern_matching_over_is_with_cast_check</span></span>](ide0020-ide0038.md#csharp_style_pattern_matching_over_is_with_cast_check)
  - [<span data-ttu-id="e544e-184">csharp_style_pattern_matching_over_as_with_null_check</span><span class="sxs-lookup"><span data-stu-id="e544e-184">csharp_style_pattern_matching_over_as_with_null_check</span></span>](ide0019.md#csharp_style_pattern_matching_over_as_with_null_check)
  - [<span data-ttu-id="e544e-185">csharp_style_prefer_switch_expression</span><span class="sxs-lookup"><span data-stu-id="e544e-185">csharp_style_prefer_switch_expression</span></span>](ide0066.md#csharp_style_prefer_switch_expression)
  - [<span data-ttu-id="e544e-186">csharp_style_prefer_pattern_matching</span><span class="sxs-lookup"><span data-stu-id="e544e-186">csharp_style_prefer_pattern_matching</span></span>](ide0078.md#csharp_style_prefer_pattern_matching)
  - [<span data-ttu-id="e544e-187">csharp_style_prefer_not_pattern</span><span class="sxs-lookup"><span data-stu-id="e544e-187">csharp_style_prefer_not_pattern</span></span>](ide0083.md#csharp_style_prefer_not_pattern)
- [<span data-ttu-id="e544e-188">表达式级首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-188">Expression-level preferences</span></span>](expression-level-preferences.md#c-expression-level-preferences)
  - [<span data-ttu-id="e544e-189">csharp_style_inlined_variable_declaration</span><span class="sxs-lookup"><span data-stu-id="e544e-189">csharp_style_inlined_variable_declaration</span></span>](ide0018.md#csharp_style_inlined_variable_declaration)
  - [<span data-ttu-id="e544e-190">csharp_prefer_simple_default_expression</span><span class="sxs-lookup"><span data-stu-id="e544e-190">csharp_prefer_simple_default_expression</span></span>](ide0034.md#csharp_prefer_simple_default_expression)
  - [<span data-ttu-id="e544e-191">csharp_style_pattern_local_over_anonymous_function</span><span class="sxs-lookup"><span data-stu-id="e544e-191">csharp_style_pattern_local_over_anonymous_function</span></span>](ide0039.md#csharp_style_pattern_local_over_anonymous_function)
  - [<span data-ttu-id="e544e-192">csharp_style_deconstructed_variable_declaration</span><span class="sxs-lookup"><span data-stu-id="e544e-192">csharp_style_deconstructed_variable_declaration</span></span>](ide0042.md#csharp_style_deconstructed_variable_declaration)
  - [<span data-ttu-id="e544e-193">csharp_style_prefer_index_operator</span><span class="sxs-lookup"><span data-stu-id="e544e-193">csharp_style_prefer_index_operator</span></span>](ide0056.md#csharp_style_prefer_index_operator)
  - [<span data-ttu-id="e544e-194">csharp_style_prefer_range_operator</span><span class="sxs-lookup"><span data-stu-id="e544e-194">csharp_style_prefer_range_operator</span></span>](ide0057.md#csharp_style_prefer_range_operator)
  - [<span data-ttu-id="e544e-195">csharp_style_implicit_object_creation_when_type_is_apparent</span><span class="sxs-lookup"><span data-stu-id="e544e-195">csharp_style_implicit_object_creation_when_type_is_apparent</span></span>](ide0090.md#csharp_style_implicit_object_creation_when_type_is_apparent)
  - <span data-ttu-id="e544e-196">[向 switch 表达式添加缺少的事例](ide0072.md) -此规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-196">[Add missing cases to switch expression](ide0072.md) - This rule has no code style option.</span></span>
- [<span data-ttu-id="e544e-197">“NULL”检查首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-197">"Null" checking preferences</span></span>](null-checking-preferences.md#c-null-checking-preferences)
  - [<span data-ttu-id="e544e-198">csharp_style_throw_expression</span><span class="sxs-lookup"><span data-stu-id="e544e-198">csharp_style_throw_expression</span></span>](ide0016.md#csharp_style_throw_expression)
  - [<span data-ttu-id="e544e-199">csharp_style_conditional_delegate_call</span><span class="sxs-lookup"><span data-stu-id="e544e-199">csharp_style_conditional_delegate_call</span></span>](ide1005.md#csharp_style_conditional_delegate_call)
- [<span data-ttu-id="e544e-200">代码块首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-200">Code block preferences</span></span>](code-block-preferences.md)
  - [<span data-ttu-id="e544e-201">csharp_prefer_braces</span><span class="sxs-lookup"><span data-stu-id="e544e-201">csharp_prefer_braces</span></span>](ide0011.md#csharp_prefer_braces)
  - [<span data-ttu-id="e544e-202">csharp_prefer_simple_using_statement</span><span class="sxs-lookup"><span data-stu-id="e544e-202">csharp_prefer_simple_using_statement</span></span>](ide0063.md#csharp_prefer_simple_using_statement)
- [<span data-ttu-id="e544e-203">"using" 指令首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-203">'using' directive preferences</span></span>](ide0065.md)
  - [<span data-ttu-id="e544e-204">csharp_using_directive_placement</span><span class="sxs-lookup"><span data-stu-id="e544e-204">csharp_using_directive_placement</span></span>](ide0065.md#csharp_using_directive_placement)
- [<span data-ttu-id="e544e-205">修饰符首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-205">Modifier preferences</span></span>](modifier-preferences.md#c-modifier-preferences)
  - [<span data-ttu-id="e544e-206">csharp_prefer_static_local_function</span><span class="sxs-lookup"><span data-stu-id="e544e-206">csharp_prefer_static_local_function</span></span>](ide0062.md#csharp_prefer_static_local_function)
  - <span data-ttu-id="e544e-207">[使结构字段可写](ide0064.md) -此规则没有代码样式选项。</span><span class="sxs-lookup"><span data-stu-id="e544e-207">[Make struct fields writable](ide0064.md) - This rule has no code style option.</span></span>

## <a name="visual-basic-style-rules"></a><span data-ttu-id="e544e-208">Visual Basic 样式规则</span><span class="sxs-lookup"><span data-stu-id="e544e-208">Visual Basic style rules</span></span>

<span data-ttu-id="e544e-209">本节中的样式规则仅适用于 Visual Basic 语言。</span><span class="sxs-lookup"><span data-stu-id="e544e-209">The style rules in this section are applicable to Visual Basic language only.</span></span>

- [<span data-ttu-id="e544e-210">模式匹配首选项</span><span class="sxs-lookup"><span data-stu-id="e544e-210">Pattern matching preferences</span></span>](pattern-matching-preferences.md)
  - [<span data-ttu-id="e544e-211">visual_basic_style_prefer_isnot_expression</span><span class="sxs-lookup"><span data-stu-id="e544e-211">visual_basic_style_prefer_isnot_expression</span></span>](ide0084.md#visual_basic_style_prefer_isnot_expression)

## <a name="see-also"></a><span data-ttu-id="e544e-212">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e544e-212">See also</span></span>

- [<span data-ttu-id="e544e-213">不必要的代码规则</span><span class="sxs-lookup"><span data-stu-id="e544e-213">Unnecessary code rules</span></span>](unnecessary-code-rules.md)
- [<span data-ttu-id="e544e-214">格式设置规则</span><span class="sxs-lookup"><span data-stu-id="e544e-214">Formatting rules</span></span>](formatting-rules.md)
- [<span data-ttu-id="e544e-215">命名规则</span><span class="sxs-lookup"><span data-stu-id="e544e-215">Naming rules</span></span>](naming-rules.md)
- [<span data-ttu-id="e544e-216">.NET 代码样式规则参考</span><span class="sxs-lookup"><span data-stu-id="e544e-216">.NET code style rules reference</span></span>](index.md)
