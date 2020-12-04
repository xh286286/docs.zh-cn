---
title: '预定义的配置文件 (代码分析) '
description: 了解如何使用预定义的 editorconfig 和规则集文件来面向特定类型的代码分析。
ms.date: 09/24/2020
ms.topic: conceptual
ms.openlocfilehash: 4937dcab1183fa3f63be4afc71627a7c7c08c6bd
ms.sourcegitcommit: 665f8fc55258356f4d2f4a6585b750c974b26675
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2020
ms.locfileid: "96590482"
---
# <a name="predefined-configuration-files"></a><span data-ttu-id="5c294-103">预定义配置文件</span><span class="sxs-lookup"><span data-stu-id="5c294-103">Predefined configuration files</span></span>

<span data-ttu-id="5c294-104">预定义的 EditorConfig 和 [规则集](/visualstudio/code-quality/using-rule-sets-to-group-code-analysis-rules) 文件可用，使你能够快速轻松地启用一类代码质量规则，如安全性或设计规则。</span><span class="sxs-lookup"><span data-stu-id="5c294-104">Predefined EditorConfig and [rule set](/visualstudio/code-quality/using-rule-sets-to-group-code-analysis-rules) files are available that make it quick and easy to enable a category of code quality rules, such as security or design rules.</span></span> <span data-ttu-id="5c294-105">通过启用特定类别的规则，可以确定目标问题和特定条件。</span><span class="sxs-lookup"><span data-stu-id="5c294-105">By enabling a specific category of rules, you can identify targeted issues and specific conditions.</span></span> <span data-ttu-id="5c294-106">若要访问这些预定义的文件，请安装 [CodeAnalysis. NetAnalyzers](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) NuGet 分析器包。</span><span class="sxs-lookup"><span data-stu-id="5c294-106">To access these predefined files, install the [Microsoft.CodeAnalysis.NetAnalyzers](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) NuGet analyzer package.</span></span>

<span data-ttu-id="5c294-107">[CodeAnalysis NetAnalyzers](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) 为以下规则类别包括预定义的 EditorConfig 文件和规则集：</span><span class="sxs-lookup"><span data-stu-id="5c294-107">[Microsoft.CodeAnalysis.NetAnalyzers](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) includes predefined EditorConfig files and rule sets for the following rule categories:</span></span>

- <span data-ttu-id="5c294-108">┮Τ砏玥</span><span class="sxs-lookup"><span data-stu-id="5c294-108">All rules</span></span>
- <span data-ttu-id="5c294-109">数据流</span><span class="sxs-lookup"><span data-stu-id="5c294-109">Dataflow</span></span>
- <span data-ttu-id="5c294-110">设计</span><span class="sxs-lookup"><span data-stu-id="5c294-110">Design</span></span>
- <span data-ttu-id="5c294-111">文档</span><span class="sxs-lookup"><span data-stu-id="5c294-111">Documentation</span></span>
- <span data-ttu-id="5c294-112">全球化</span><span class="sxs-lookup"><span data-stu-id="5c294-112">Globalization</span></span>
- <span data-ttu-id="5c294-113">互操作性</span><span class="sxs-lookup"><span data-stu-id="5c294-113">Interoperability</span></span>
- <span data-ttu-id="5c294-114">可维护性</span><span class="sxs-lookup"><span data-stu-id="5c294-114">Maintainability</span></span>
- <span data-ttu-id="5c294-115">命名</span><span class="sxs-lookup"><span data-stu-id="5c294-115">Naming</span></span>
- <span data-ttu-id="5c294-116">性能</span><span class="sxs-lookup"><span data-stu-id="5c294-116">Performance</span></span>
- <span data-ttu-id="5c294-117">从 FxCop 移植</span><span class="sxs-lookup"><span data-stu-id="5c294-117">Ported from FxCop</span></span>
- <span data-ttu-id="5c294-118">可靠性</span><span class="sxs-lookup"><span data-stu-id="5c294-118">Reliability</span></span>
- <span data-ttu-id="5c294-119">安全性</span><span class="sxs-lookup"><span data-stu-id="5c294-119">Security</span></span>
- <span data-ttu-id="5c294-120">使用情况</span><span class="sxs-lookup"><span data-stu-id="5c294-120">Usage</span></span>

<span data-ttu-id="5c294-121">每类规则都有一个 EditorConfig 或规则集文件，用于：</span><span class="sxs-lookup"><span data-stu-id="5c294-121">Each of those categories of rules has an EditorConfig or rule set file to:</span></span>

- <span data-ttu-id="5c294-122">启用类别 (中的所有规则，并禁用所有其他规则) </span><span class="sxs-lookup"><span data-stu-id="5c294-122">Enable all the rules in the category (and disable all other rules)</span></span>
- <span data-ttu-id="5c294-123">使用每个规则的默认严重性并默认启用 (设置并禁用所有其他规则) </span><span class="sxs-lookup"><span data-stu-id="5c294-123">Use each rule's default severity and enabled by default setting (and disable all other rules)</span></span>

> [!TIP]
> <span data-ttu-id="5c294-124">"所有规则" 类别具有一个附加的 EditorConfig 或规则集文件，用于禁用所有规则。</span><span class="sxs-lookup"><span data-stu-id="5c294-124">The "all rules" category has an additional EditorConfig or rule set file to disable all rules.</span></span> <span data-ttu-id="5c294-125">使用此文件可快速删除项目中的任何分析器警告或错误。</span><span class="sxs-lookup"><span data-stu-id="5c294-125">Use this file to quickly get rid of any analyzer warnings or errors in a project.</span></span>

## <a name="predefined-editorconfig-files"></a><span data-ttu-id="5c294-126">预定义的 EditorConfig 文件</span><span class="sxs-lookup"><span data-stu-id="5c294-126">Predefined EditorConfig files</span></span>

<span data-ttu-id="5c294-127">NetAnalyzers 分析器包的预定义 EditorConfig 文件位于安装了 NuGet 包的 *EditorConfig* 子目录中。</span><span class="sxs-lookup"><span data-stu-id="5c294-127">The predefined EditorConfig files for the Microsoft.CodeAnalysis.NetAnalyzers analyzer package are located in the *editorconfig* subdirectory of where the NuGet package was installed.</span></span> <span data-ttu-id="5c294-128">例如，启用所有安全规则的 EditorConfig 文件位于 *EditorConfig/SecurityRulesEnabled/EditorConfig*。</span><span class="sxs-lookup"><span data-stu-id="5c294-128">For example, the EditorConfig file to enable all security rules is located at *editorconfig/SecurityRulesEnabled/.editorconfig*.</span></span>

<span data-ttu-id="5c294-129">将所选的 *editorconfig* 文件复制到项目的根目录。</span><span class="sxs-lookup"><span data-stu-id="5c294-129">Copy the chosen *.editorconfig* file to your project's root directory.</span></span>

## <a name="predefined-rule-sets"></a><span data-ttu-id="5c294-130">预定义规则集</span><span class="sxs-lookup"><span data-stu-id="5c294-130">Predefined rule sets</span></span>

<span data-ttu-id="5c294-131">CodeAnalysis. NetAnalyzers 分析器包的预定义规则集文件位于安装 NuGet 包 *的规则集子目录中* 。</span><span class="sxs-lookup"><span data-stu-id="5c294-131">The predefined rule set files for the Microsoft.CodeAnalysis.NetAnalyzers analyzer package are located in the *rulesets* subdirectory of where the NuGet package was installed.</span></span> <span data-ttu-id="5c294-132">例如，启用所有安全规则的规则集文件位于规则集 */SecurityRulesEnabled*。</span><span class="sxs-lookup"><span data-stu-id="5c294-132">For example, the rule set file to enable all security rules is located at *rulesets/SecurityRulesEnabled.ruleset*.</span></span> <span data-ttu-id="5c294-133">复制一个或多个规则集，并将其粘贴到包含项目的目录中。</span><span class="sxs-lookup"><span data-stu-id="5c294-133">Copy one or more of the rule sets and paste them in the directory that contains your project.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c294-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c294-134">See also</span></span>

- [<span data-ttu-id="5c294-135">分析器配置</span><span class="sxs-lookup"><span data-stu-id="5c294-135">Analyzer configuration</span></span>](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md)
- [<span data-ttu-id="5c294-136">EditorConfig 的 .NET 代码样式规则选项</span><span class="sxs-lookup"><span data-stu-id="5c294-136">.NET code style rule options for EditorConfig</span></span>](code-style-rule-options.md)
