---
title: .NET 中的代码分析
titleSuffix: ''
description: 了解 .NET SDK 中的源代码分析。
ms.date: 08/22/2020
ms.topic: overview
ms.custom: updateeachrelease
helpviewer_keywords:
- code analysis
- code analyzers
ms.openlocfilehash: 8efac4d5e3fddcb9fdc6e08bcc933f2776420ced
ms.sourcegitcommit: ecd9e9bb2225eb76f819722ea8b24988fe46f34c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "96739969"
---
# <a name="overview-of-net-source-code-analysis"></a><span data-ttu-id="5d363-103">.NET 源代码分析概述</span><span class="sxs-lookup"><span data-stu-id="5d363-103">Overview of .NET source code analysis</span></span>

<span data-ttu-id="5d363-104">.NET Compiler Platform (Roslyn) 分析器会检查 C# 或 Visual Basic 代码的代码质量和代码样式问题。</span><span class="sxs-lookup"><span data-stu-id="5d363-104">.NET compiler platform (Roslyn) analyzers inspect your C# or Visual Basic code for code quality and code style issues.</span></span> <span data-ttu-id="5d363-105">从 .NET 5.0 开始，这些分析器包含在 .NET SDK 中。</span><span class="sxs-lookup"><span data-stu-id="5d363-105">Starting in .NET 5.0, these analyzers are included with the .NET SDK.</span></span> <span data-ttu-id="5d363-106">如果不想移到 .NET 5 + SDK，或者想要使用基于 NuGet 包的模型，则可以在 `Microsoft.CodeAnalysis.NetAnalyzers` [nuget 包](https://www.nuget.org/packages/Microsoft.CodeAnalysis.NetAnalyzers)中使用该分析器。</span><span class="sxs-lookup"><span data-stu-id="5d363-106">If you don't want to move to the .NET 5+ SDK or if you prefer a NuGet package-based model, the analyzers are also available in the `Microsoft.CodeAnalysis.NetAnalyzers` [NuGet package](https://www.nuget.org/packages/Microsoft.CodeAnalysis.NetAnalyzers).</span></span> <span data-ttu-id="5d363-107">对于按需版本更新，你可能更倾向于使用基于包的模型。</span><span class="sxs-lookup"><span data-stu-id="5d363-107">You might prefer a package-based model for on-demand version updates.</span></span>

> [!NOTE]
> <span data-ttu-id="5d363-108">.NET 分析器与目标平台无关。</span><span class="sxs-lookup"><span data-stu-id="5d363-108">.NET analyzers are target-platform agnostic.</span></span> <span data-ttu-id="5d363-109">也就是说，你的项目不需要面向特定的 .NET 平台。</span><span class="sxs-lookup"><span data-stu-id="5d363-109">That is, your project does not need to target a specific .NET platform.</span></span> <span data-ttu-id="5d363-110">分析器适用于目标为的项目以及 `net5.0` 更早的 .net 版本，如 `netcoreapp` 、 `netstandard` 和 `net472` 。</span><span class="sxs-lookup"><span data-stu-id="5d363-110">The analyzers work for projects that target `net5.0` as well as earlier .NET versions, such as `netcoreapp`, `netstandard`, and `net472`.</span></span>

- [<span data-ttu-id="5d363-111"> ( "CAxxxx" 规则的代码质量分析) </span><span class="sxs-lookup"><span data-stu-id="5d363-111">Code quality analysis ("CAxxxx" rules)</span></span>](#code-quality-analysis)
- [<span data-ttu-id="5d363-112"> ( "IDExxxx" 规则的代码样式分析) </span><span class="sxs-lookup"><span data-stu-id="5d363-112">Code style analysis ("IDExxxx" rules)</span></span>](#code-style-analysis)

<span data-ttu-id="5d363-113">如果分析器发现规则冲突，则会将其报告为建议、警告或错误，具体情况视每个规则的 [配置](configuration-options.md)方式而定。</span><span class="sxs-lookup"><span data-stu-id="5d363-113">If rule violations are found by an analyzer, they're reported as a suggestion, warning, or error, depending on how each rule is [configured](configuration-options.md).</span></span> <span data-ttu-id="5d363-114">代码分析冲突以前缀 "CA" 或 "IDE" 显示，以便将它们与编译器错误区分开来。</span><span class="sxs-lookup"><span data-stu-id="5d363-114">Code analysis violations appear with the prefix "CA" or "IDE" to differentiate them from compiler errors.</span></span>

> [!TIP]
>
> - <span data-ttu-id="5d363-115">你还可以安装第三方分析器，如 [StyleCop](https://www.nuget.org/packages/StyleCop.Analyzers/)、 [Roslynator](https://www.nuget.org/packages/Roslynator.Analyzers/)、 [XUnit 分析器](https://www.nuget.org/packages/xunit.analyzers/)和 [sonar.projectname Analyzer](https://www.nuget.org/packages/SonarAnalyzer.CSharp/)。</span><span class="sxs-lookup"><span data-stu-id="5d363-115">You can also install third party analyzers, such as [StyleCop](https://www.nuget.org/packages/StyleCop.Analyzers/), [Roslynator](https://www.nuget.org/packages/Roslynator.Analyzers/), [XUnit Analyzers](https://www.nuget.org/packages/xunit.analyzers/), and [Sonar Analyzer](https://www.nuget.org/packages/SonarAnalyzer.CSharp/).</span></span>
> - <span data-ttu-id="5d363-116">如果你使用的是 Visual Studio，许多分析器规则都有关联的代码修复程序，你可以应用这些 *修补程序* 来纠正此问题。</span><span class="sxs-lookup"><span data-stu-id="5d363-116">If you're using Visual Studio, many analyzer rules have associated *code fixes* that you can apply to correct the problem.</span></span> <span data-ttu-id="5d363-117">代码修复显示在灯泡图标菜单中。</span><span class="sxs-lookup"><span data-stu-id="5d363-117">Code fixes are shown in the light bulb icon menu.</span></span>

## <a name="code-quality-analysis"></a><span data-ttu-id="5d363-118">代码质量分析</span><span class="sxs-lookup"><span data-stu-id="5d363-118">Code quality analysis</span></span>

<span data-ttu-id="5d363-119">_代码质量分析 ( "CA" ) 规则_ 检查您的 c # 或 Visual Basic 代码以获得安全性、性能、设计和其他问题。</span><span class="sxs-lookup"><span data-stu-id="5d363-119">_Code quality analysis ("CA") rules_ inspect your C# or Visual Basic code for security, performance, design and other issues.</span></span> <span data-ttu-id="5d363-120">默认情况下，对于面向 .NET 5.0 或更高版本的项目，分析处于启用状态。</span><span class="sxs-lookup"><span data-stu-id="5d363-120">Analysis is enabled, by default, for projects that target .NET 5.0 or later.</span></span> <span data-ttu-id="5d363-121">通过将 [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) 属性设置为，可以对面向早期 .net 版本的项目启用代码分析 `true` 。</span><span class="sxs-lookup"><span data-stu-id="5d363-121">You can enable code analysis on projects that target earlier .NET versions by setting the [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) property to `true`.</span></span> <span data-ttu-id="5d363-122">你还可以通过将设置为来对你的项目禁用代码分析 `EnableNETAnalyzers` `false` 。</span><span class="sxs-lookup"><span data-stu-id="5d363-122">You can also disable code analysis for your project by setting `EnableNETAnalyzers` to `false`.</span></span>

> [!TIP]
> <span data-ttu-id="5d363-123">在 Visual Studio 中，你可以使用项目属性窗口来启用或禁用代码分析。</span><span class="sxs-lookup"><span data-stu-id="5d363-123">In Visual Studio, you can enable or disable code analysis using the Project Properties window.</span></span> <span data-ttu-id="5d363-124">若要属性窗口访问项目，请在解决方案资源管理器中右键单击项目，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="5d363-124">To access the Project Properties window, right-click on a project within Solution Explorer and select **Properties**.</span></span> <span data-ttu-id="5d363-125">接下来，选择 " **代码分析** " 选项卡，然后选中或清除相应的复选框以 **启用 .net 分析器**。</span><span class="sxs-lookup"><span data-stu-id="5d363-125">Next, select the **Code Analysis** tab, and then either select or clear the checkbox to **Enable .NET analyzers**.</span></span>

### <a name="enabled-rules"></a><span data-ttu-id="5d363-126">启用规则</span><span class="sxs-lookup"><span data-stu-id="5d363-126">Enabled rules</span></span>

<span data-ttu-id="5d363-127">默认情况下，在 .NET 5.0 Preview 8 中启用以下规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-127">The following rules are enabled, by default, in .NET 5.0 Preview 8.</span></span>

| <span data-ttu-id="5d363-128">诊断 ID</span><span class="sxs-lookup"><span data-stu-id="5d363-128">Diagnostic ID</span></span> | <span data-ttu-id="5d363-129">类别</span><span class="sxs-lookup"><span data-stu-id="5d363-129">Category</span></span> | <span data-ttu-id="5d363-130">严重性</span><span class="sxs-lookup"><span data-stu-id="5d363-130">Severity</span></span> | <span data-ttu-id="5d363-131">说明</span><span class="sxs-lookup"><span data-stu-id="5d363-131">Description</span></span> |
| - | - | - | - |
| [<span data-ttu-id="5d363-132">CA1416</span><span class="sxs-lookup"><span data-stu-id="5d363-132">CA1416</span></span>](/visualstudio/code-quality/ca1416) | <span data-ttu-id="5d363-133">互操作性</span><span class="sxs-lookup"><span data-stu-id="5d363-133">Interoperability</span></span> | <span data-ttu-id="5d363-134">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-134">Warning</span></span> | <span data-ttu-id="5d363-135">平台兼容性分析器</span><span class="sxs-lookup"><span data-stu-id="5d363-135">Platform compatibility analyzer</span></span> |
| [<span data-ttu-id="5d363-136">CA1417</span><span class="sxs-lookup"><span data-stu-id="5d363-136">CA1417</span></span>](/visualstudio/code-quality/ca1417) | <span data-ttu-id="5d363-137">互操作性</span><span class="sxs-lookup"><span data-stu-id="5d363-137">Interoperability</span></span> | <span data-ttu-id="5d363-138">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-138">Warning</span></span> | <span data-ttu-id="5d363-139">不要 `OutAttribute` 在 P/invoke 的字符串参数上使用</span><span class="sxs-lookup"><span data-stu-id="5d363-139">Do not use `OutAttribute` on string parameters for P/Invokes</span></span> |
| [<span data-ttu-id="5d363-140">CA1831</span><span class="sxs-lookup"><span data-stu-id="5d363-140">CA1831</span></span>](/visualstudio/code-quality/ca1831) | <span data-ttu-id="5d363-141">性能</span><span class="sxs-lookup"><span data-stu-id="5d363-141">Performance</span></span> | <span data-ttu-id="5d363-142">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-142">Warning</span></span> | <span data-ttu-id="5d363-143">`AsSpan`适当时使用字符串而不是基于范围的索引器</span><span class="sxs-lookup"><span data-stu-id="5d363-143">Use `AsSpan` instead of range-based indexers for string when appropriate</span></span> |
| [<span data-ttu-id="5d363-144">CA2013</span><span class="sxs-lookup"><span data-stu-id="5d363-144">CA2013</span></span>](/visualstudio/code-quality/ca2013) | <span data-ttu-id="5d363-145">可靠性</span><span class="sxs-lookup"><span data-stu-id="5d363-145">Reliability</span></span> | <span data-ttu-id="5d363-146">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-146">Warning</span></span> | <span data-ttu-id="5d363-147">不要将 `ReferenceEquals` 与值类型一起使用</span><span class="sxs-lookup"><span data-stu-id="5d363-147">Do not use `ReferenceEquals` with value types</span></span> |
| [<span data-ttu-id="5d363-148">CA2014</span><span class="sxs-lookup"><span data-stu-id="5d363-148">CA2014</span></span>](/visualstudio/code-quality/ca2014) | <span data-ttu-id="5d363-149">可靠性</span><span class="sxs-lookup"><span data-stu-id="5d363-149">Reliability</span></span> | <span data-ttu-id="5d363-150">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-150">Warning</span></span> | <span data-ttu-id="5d363-151">不要 `stackalloc` 在循环中使用</span><span class="sxs-lookup"><span data-stu-id="5d363-151">Do not use `stackalloc` in loops</span></span> |
| [<span data-ttu-id="5d363-152">CA2015</span><span class="sxs-lookup"><span data-stu-id="5d363-152">CA2015</span></span>](/visualstudio/code-quality/ca2015) | <span data-ttu-id="5d363-153">可靠性</span><span class="sxs-lookup"><span data-stu-id="5d363-153">Reliability</span></span> | <span data-ttu-id="5d363-154">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-154">Warning</span></span> | <span data-ttu-id="5d363-155">不要定义派生自的类型的终结器 <xref:System.Buffers.MemoryManager%601></span><span class="sxs-lookup"><span data-stu-id="5d363-155">Do not define finalizers for types derived from <xref:System.Buffers.MemoryManager%601></span></span> |
| [<span data-ttu-id="5d363-156">CA2200</span><span class="sxs-lookup"><span data-stu-id="5d363-156">CA2200</span></span>](/visualstudio/code-quality/ca2200) | <span data-ttu-id="5d363-157">使用情况</span><span class="sxs-lookup"><span data-stu-id="5d363-157">Usage</span></span> | <span data-ttu-id="5d363-158">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-158">Warning</span></span> | <span data-ttu-id="5d363-159">再次引发以保留堆栈详细信息</span><span class="sxs-lookup"><span data-stu-id="5d363-159">Rethrow to preserve stack details</span></span>
| [<span data-ttu-id="5d363-160">CA2247</span><span class="sxs-lookup"><span data-stu-id="5d363-160">CA2247</span></span>](/visualstudio/code-quality/ca2247) | <span data-ttu-id="5d363-161">使用情况</span><span class="sxs-lookup"><span data-stu-id="5d363-161">Usage</span></span> | <span data-ttu-id="5d363-162">警告</span><span class="sxs-lookup"><span data-stu-id="5d363-162">Warning</span></span> | <span data-ttu-id="5d363-163">传递给 TaskCompletionSource 构造函数的参数应为 <xref:System.Threading.Tasks.TaskCreationOptions> 枚举，而不是 <xref:System.Threading.Tasks.TaskContinuationOptions></span><span class="sxs-lookup"><span data-stu-id="5d363-163">Argument passed to TaskCompletionSource constructor should be <xref:System.Threading.Tasks.TaskCreationOptions> enum instead of <xref:System.Threading.Tasks.TaskContinuationOptions></span></span> |

<span data-ttu-id="5d363-164">你可以更改这些规则的严重性，以禁用这些规则或将它们提升为错误。</span><span class="sxs-lookup"><span data-stu-id="5d363-164">You can change the severity of these rules to disable them or elevate them to errors.</span></span>

<span data-ttu-id="5d363-165">有关可用代码质量规则的完整列表，请参阅 [代码质量规则](quality-rules/index.md)。</span><span class="sxs-lookup"><span data-stu-id="5d363-165">For a full list of available code quality rules, see [Code quality rules](quality-rules/index.md).</span></span>

### <a name="enable-additional-rules"></a><span data-ttu-id="5d363-166">启用其他规则</span><span class="sxs-lookup"><span data-stu-id="5d363-166">Enable additional rules</span></span>

<span data-ttu-id="5d363-167">从 .NET 5.0 RC2 开始，.NET SDK 附带了所有[“CA”代码质量规则](/visualstudio/code-quality/code-analysis-for-managed-code-warnings)。</span><span class="sxs-lookup"><span data-stu-id="5d363-167">Starting with .NET 5.0 RC2, the .NET SDK ships with all of the ["CA" code quality rules](/visualstudio/code-quality/code-analysis-for-managed-code-warnings).</span></span> <span data-ttu-id="5d363-168">有关每个 .NET SDK 版本附带的规则的完整列表，请参阅 [分析器版本](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md)。</span><span class="sxs-lookup"><span data-stu-id="5d363-168">For a full list of rules that are included with each .NET SDK version, see [analyzer releases](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md).</span></span>

#### <a name="default-analysis-mode"></a><span data-ttu-id="5d363-169">默认分析模式</span><span class="sxs-lookup"><span data-stu-id="5d363-169">Default analysis mode</span></span>

<span data-ttu-id="5d363-170">在默认的分析模式下，某些规则 [默认启用](#enabled-rules) 为生成警告。</span><span class="sxs-lookup"><span data-stu-id="5d363-170">In the default analysis mode, some rules are [enabled by default](#enabled-rules) as build warnings.</span></span> <span data-ttu-id="5d363-171">某些其他规则默认情况下启用为 Visual Studio IDE 建议和相应的代码修复。</span><span class="sxs-lookup"><span data-stu-id="5d363-171">Some other rules are enabled by default only as Visual Studio IDE suggestions with corresponding code fixes.</span></span> <span data-ttu-id="5d363-172">默认情况下，将禁用其余规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-172">The remaining rules are disabled by default.</span></span> <span data-ttu-id="5d363-173">[规则的完整列表](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md)包括每个规则的默认严重性，以及默认情况下是否在默认分析模式下启用规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-173">The [full list of rules](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md) includes each rule's default severity and whether or not the rule is enabled by default in the default analysis mode.</span></span>

#### <a name="custom-analysis-mode"></a><span data-ttu-id="5d363-174">自定义分析模式</span><span class="sxs-lookup"><span data-stu-id="5d363-174">Custom analysis mode</span></span>

<span data-ttu-id="5d363-175">您可以 [配置代码分析规则](configuration-options.md) ，以启用或禁用单个规则或规则类别。</span><span class="sxs-lookup"><span data-stu-id="5d363-175">You can [configure code analysis rules](configuration-options.md) to enable or disable an individual rule or a category of rules.</span></span> <span data-ttu-id="5d363-176">此外，还可以使用 [AnalysisMode](../../core/project-sdk/msbuild-props.md#analysismode) 属性切换到以下自定义分析模式之一：</span><span class="sxs-lookup"><span data-stu-id="5d363-176">Additionally, you can use the [AnalysisMode](../../core/project-sdk/msbuild-props.md#analysismode) property to switch to one of the following custom analysis modes:</span></span>

- <span data-ttu-id="5d363-177">_积极_ 或 _退出_ 模式：默认情况下，所有规则都作为生成警告启用。</span><span class="sxs-lookup"><span data-stu-id="5d363-177">_Aggressive_ or _Opt-out_ mode: All rules are enabled by default as build warnings.</span></span> <span data-ttu-id="5d363-178">可以选择[选择退出](configuration-options.md)各条规则，以禁用它们。</span><span class="sxs-lookup"><span data-stu-id="5d363-178">You can selectively [opt out](configuration-options.md) of individual rules to disable them.</span></span>
- <span data-ttu-id="5d363-179">_保守_ 或 _选择加入_ 模式：默认情况下禁用所有规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-179">_Conservative_ or _Opt-in_ mode: All rules are disabled by default.</span></span> <span data-ttu-id="5d363-180">可以选择[选择加入](configuration-options.md)各条规则，以启用它们。</span><span class="sxs-lookup"><span data-stu-id="5d363-180">You can selectively [opt into](configuration-options.md) individual rules to enable them.</span></span>

### <a name="treat-warnings-as-errors"></a><span data-ttu-id="5d363-181">视警告为错误</span><span class="sxs-lookup"><span data-stu-id="5d363-181">Treat warnings as errors</span></span>

<span data-ttu-id="5d363-182">如果在 `-warnaserror` 生成项目时使用标志，则所有代码分析警告也被视为错误。</span><span class="sxs-lookup"><span data-stu-id="5d363-182">If you use the `-warnaserror` flag when you build your projects, all code analysis warnings are also treated as errors.</span></span> <span data-ttu-id="5d363-183">如果你不希望将代码质量警告 (CAxxxx) 在存在时被视为错误 `-warnaserror` ，可以 `CodeAnalysisTreatWarningsAsErrors` `false` 在项目文件中将 MSBuild 属性设置为。</span><span class="sxs-lookup"><span data-stu-id="5d363-183">If you do not want code quality warnings (CAxxxx) to be treated as errors in presence of `-warnaserror`, you can set the `CodeAnalysisTreatWarningsAsErrors` MSBuild property to `false` in your project file.</span></span>

```xml
<PropertyGroup>
  <CodeAnalysisTreatWarningsAsErrors>false</CodeAnalysisTreatWarningsAsErrors>
</PropertyGroup>
```

<span data-ttu-id="5d363-184">你仍会看到任何代码分析警告，但不会中断你的生成。</span><span class="sxs-lookup"><span data-stu-id="5d363-184">You'll still see any code analysis warnings, but they won't break your build.</span></span>

### <a name="latest-updates"></a><span data-ttu-id="5d363-185">最新更新</span><span class="sxs-lookup"><span data-stu-id="5d363-185">Latest updates</span></span>

<span data-ttu-id="5d363-186">默认情况下，升级到较新版本的 .NET SDK 时，你将获得最新的代码分析规则和默认规则严重性。</span><span class="sxs-lookup"><span data-stu-id="5d363-186">By default, you'll get the latest code analysis rules and default rule severities as you upgrade to newer versions of the .NET SDK.</span></span> <span data-ttu-id="5d363-187">如果不想要此行为，例如，如果想要确保没有启用或禁用任何新规则，可以通过以下方式之一来替代它：</span><span class="sxs-lookup"><span data-stu-id="5d363-187">If you don't want this behavior, for example, if you want to ensure that no new rules are enabled or disabled, you can override it in one of the following ways:</span></span>

- <span data-ttu-id="5d363-188">将 `AnalysisLevel` MSBuild 属性设置为一个特定值，以将警告锁定到该设置。</span><span class="sxs-lookup"><span data-stu-id="5d363-188">Set the `AnalysisLevel` MSBuild property to a specific value to lock the warnings to that set.</span></span> <span data-ttu-id="5d363-189">升级到较新的 SDK 时，仍然会获得这些警告的 bug 修复，但不会启用新的警告，并且不会禁用现有的警告。</span><span class="sxs-lookup"><span data-stu-id="5d363-189">When you upgrade to a newer SDK, you'll still get bug fixes for those warnings, but no new warnings will be enabled and no existing warnings will be disabled.</span></span> <span data-ttu-id="5d363-190">例如，若要将规则集锁定为版本5.0 的 .NET SDK 随附的规则集，请将以下条目添加到项目文件。</span><span class="sxs-lookup"><span data-stu-id="5d363-190">For example, to lock the set of rules to those that ship with version 5.0 of the .NET SDK, add the following entry to your project file.</span></span>

  ```xml
  <PropertyGroup>
    <AnalysisLevel>5.0</AnalysisLevel>
  </PropertyGroup>
  ```

  > [!TIP]
  > <span data-ttu-id="5d363-191">属性的默认值 `AnalysisLevel` 为 `latest` ，这意味着，当你移动到较新版本的 .net SDK 时，始终会获得最新的代码分析规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-191">The default value for the `AnalysisLevel` property is `latest`, which means you always get the latest code analysis rules as you move to newer versions of the .NET SDK.</span></span>

  <span data-ttu-id="5d363-192">有关详细信息，以及要查看可能值的列表，请参阅 [AnalysisLevel](../../core/project-sdk/msbuild-props.md#analysislevel)。</span><span class="sxs-lookup"><span data-stu-id="5d363-192">For more information, and to see a list of possible values, see [AnalysisLevel](../../core/project-sdk/msbuild-props.md#analysislevel).</span></span>

- <span data-ttu-id="5d363-193">安装 [CodeAnalysis NetAnalyzers NuGet 包](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) 以将规则更新与 .net SDK 更新分离。</span><span class="sxs-lookup"><span data-stu-id="5d363-193">Install the [Microsoft.CodeAnalysis.NetAnalyzers NuGet package](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) to decouple rule updates from .NET SDK updates.</span></span> <span data-ttu-id="5d363-194">如果 SDK 包含的分析器程序集版本比 NuGet 包的版本新，则安装包将关闭内置 SDK 分析器并生成生成警告。</span><span class="sxs-lookup"><span data-stu-id="5d363-194">Installing the package turns off the built-in SDK analyzers and generates a build warning if the SDK contains a newer analyzer assembly version than that of the NuGet package.</span></span>

## <a name="code-style-analysis"></a><span data-ttu-id="5d363-195">代码样式分析</span><span class="sxs-lookup"><span data-stu-id="5d363-195">Code style analysis</span></span>

<span data-ttu-id="5d363-196">[代码样式分析](/visualstudio/ide/editorconfig-code-style-settings-reference) ( "IDExxxx" 规则) 使你可以在基本代码中定义和维护一致的代码样式。</span><span class="sxs-lookup"><span data-stu-id="5d363-196">[Code style analysis](/visualstudio/ide/editorconfig-code-style-settings-reference) ("IDExxxx" rules) enables you to define and maintain consistent code style in your codebase.</span></span> <span data-ttu-id="5d363-197">下面是默认设置：</span><span class="sxs-lookup"><span data-stu-id="5d363-197">Following are the default settings:</span></span>

- <span data-ttu-id="5d363-198">命令行生成：默认情况下，对于命令行生成上的所有 .NET 项目，代码样式分析均处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="5d363-198">Command line build: Code style analysis is disabled, by default, for all .NET projects on command-line builds.</span></span>
- <span data-ttu-id="5d363-199">Visual studio：默认情况下，对于 Visual Studio 中的所有 .NET 项目，代码样式分析均为 [代码重构快速操作](/visualstudio/ide/code-generation-in-visual-studio)启用。</span><span class="sxs-lookup"><span data-stu-id="5d363-199">Visual Studio: Code style analysis is enabled, by default, for all .NET projects inside Visual Studio as [code refactoring quick actions](/visualstudio/ide/code-generation-in-visual-studio).</span></span>

<span data-ttu-id="5d363-200">启动 .NET 5.0 RC2 后，可以在命令行和 Visual Studio 内部启用生成代码样式分析。</span><span class="sxs-lookup"><span data-stu-id="5d363-200">Starting .NET 5.0 RC2, you can enable code style analysis on build, both at the command line and inside Visual Studio.</span></span> <span data-ttu-id="5d363-201">代码样式冲突显示为带有 "IDE" 前缀的警告或错误。</span><span class="sxs-lookup"><span data-stu-id="5d363-201">Code style violations appear as warnings or errors with an "IDE" prefix.</span></span> <span data-ttu-id="5d363-202">这使您能够在生成时强制执行一致的代码样式。</span><span class="sxs-lookup"><span data-stu-id="5d363-202">This enables you to enforce consistent code styles at build time.</span></span>

> [!NOTE]
> <span data-ttu-id="5d363-203">代码样式分析功能是实验性的，可能会在 .NET 5 和 .NET 6 版本之间发生更改。</span><span class="sxs-lookup"><span data-stu-id="5d363-203">The code style analysis feature is experimental and may change between the .NET 5 and .NET 6 releases.</span></span>

<span data-ttu-id="5d363-204">对生成启用代码样式分析的步骤：</span><span class="sxs-lookup"><span data-stu-id="5d363-204">Steps to enable code style analysis on build:</span></span>

1. <span data-ttu-id="5d363-205">将 MSBuild 属性 [EnforceCodeStyleInBuild](../../core/project-sdk/msbuild-props.md#enforcecodestyleinbuild) 设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="5d363-205">Set the MSBuild property [EnforceCodeStyleInBuild](../../core/project-sdk/msbuild-props.md#enforcecodestyleinbuild) to `true`.</span></span>

1. <span data-ttu-id="5d363-206">在 *editorconfig* 文件中， [配置](configuration-options.md) 希望在生成时运行的每个 "IDE" 代码样式规则（警告或错误）。</span><span class="sxs-lookup"><span data-stu-id="5d363-206">In an *.editorconfig* file, [configure](configuration-options.md) each "IDE" code style rule that you wish to run on build as a warning or an error.</span></span> <span data-ttu-id="5d363-207">例如：</span><span class="sxs-lookup"><span data-stu-id="5d363-207">For example:</span></span>

   ```ini
   [*.{cs,vb}]
   # IDE0040: Accessibility modifiers required (escalated to a build warning)
   dotnet_diagnostic.IDE0040.severity = warning
   ```

   <span data-ttu-id="5d363-208">或者，您也可以将整个 "样式" 类别配置为警告或错误，默认情况下，您可以选择关闭您不想在生成时运行的规则。</span><span class="sxs-lookup"><span data-stu-id="5d363-208">Alternatively, you can configure the entire "Style" category to be a warning or error, by default, and then selectively turn off rules that you don't want to run on build.</span></span> <span data-ttu-id="5d363-209">例如：</span><span class="sxs-lookup"><span data-stu-id="5d363-209">For example:</span></span>

   ```ini
   [*.{cs,vb}]

   # Default severity for analyzer diagnostics with category 'Style' (escalated to build warnings)
   dotnet_analyzer_diagnostic.category-Style.severity = warning

   # IDE0040: Accessibility modifiers required (disabled on build)
   dotnet_diagnostic.IDE0040.severity = silent
   ```

## <a name="suppress-a-warning"></a><span data-ttu-id="5d363-210">禁止显示警告</span><span class="sxs-lookup"><span data-stu-id="5d363-210">Suppress a warning</span></span>

<span data-ttu-id="5d363-211">若要取消规则冲突，请 `none` 在 EditorConfig 文件中将该规则 ID 的严重性选项设置为。</span><span class="sxs-lookup"><span data-stu-id="5d363-211">To suppress a rule violation, set the severity option for that rule ID to `none` in an EditorConfig file.</span></span> <span data-ttu-id="5d363-212">例如：</span><span class="sxs-lookup"><span data-stu-id="5d363-212">For example:</span></span>

```ini
dotnet_diagnostic.CA1822.severity = none
```

<span data-ttu-id="5d363-213">Visual Studio 提供了其他方式来禁止显示代码分析规则中的警告。</span><span class="sxs-lookup"><span data-stu-id="5d363-213">Visual Studio provides additional ways to suppress warnings from code analysis rules.</span></span> <span data-ttu-id="5d363-214">有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations)。</span><span class="sxs-lookup"><span data-stu-id="5d363-214">For more information, see [Suppress violations](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations).</span></span>

<span data-ttu-id="5d363-215">有关规则严重性的详细信息，请参阅 [配置规则严重性](configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="5d363-215">For more information about rule severities, see [Configure rule severity](configuration-options.md#severity-level).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d363-216">请参阅</span><span class="sxs-lookup"><span data-stu-id="5d363-216">See also</span></span>

- [<span data-ttu-id="5d363-217">代码质量分析规则参考</span><span class="sxs-lookup"><span data-stu-id="5d363-217">Code quality analysis rule reference</span></span>](quality-rules/index.md)
- [<span data-ttu-id="5d363-218">代码样式分析规则引用</span><span class="sxs-lookup"><span data-stu-id="5d363-218">Code style analysis rule reference</span></span>](style-rules/index.md)
- [<span data-ttu-id="5d363-219">Visual Studio 中的代码分析</span><span class="sxs-lookup"><span data-stu-id="5d363-219">Code analysis in Visual Studio</span></span>](/visualstudio/code-quality/roslyn-analyzers-overview)
- [<span data-ttu-id="5d363-220">.NET 编译器平台 SDK</span><span class="sxs-lookup"><span data-stu-id="5d363-220">.NET Compiler Platform SDK</span></span>](../../csharp/roslyn-sdk/index.md)
- [<span data-ttu-id="5d363-221">教程：编写第一个分析器和代码修补程序</span><span class="sxs-lookup"><span data-stu-id="5d363-221">Tutorial: Write your first analyzer and code fix</span></span>](../../csharp/roslyn-sdk/tutorials/how-to-write-csharp-analyzer-code-fix.md)
