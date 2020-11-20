---
title: dotnet new 命令
description: dotnet new 命令可根据指定模板新建 .NET 项目。
no-loc:
- Blazor
- WebAssembly
ms.date: 09/04/2020
ms.openlocfilehash: 3ee644f05ea5929ffc7b11054ef1d974b811f418
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "94634450"
---
# <a name="dotnet-new"></a><span data-ttu-id="46126-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="46126-103">dotnet new</span></span>

<span data-ttu-id="46126-104">本文适用于： ✔️ .NET Core 2.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="46126-104">**This article applies to:** ✔️ .NET Core 2.0 SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="46126-105">“属性”</span><span class="sxs-lookup"><span data-stu-id="46126-105">Name</span></span>

<span data-ttu-id="46126-106">`dotnet new` - 根据指定的模板，创建新的项目、配置文件或解决方案。</span><span class="sxs-lookup"><span data-stu-id="46126-106">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="46126-107">摘要</span><span class="sxs-lookup"><span data-stu-id="46126-107">Synopsis</span></span>

```dotnetcli
dotnet new <TEMPLATE> [--dry-run] [--force] [-i|--install {PATH|NUGET_ID}]
    [-lang|--language {"C#"|"F#"|VB}] [-n|--name <OUTPUT_NAME>]
    [--nuget-source <SOURCE>] [-o|--output <OUTPUT_DIRECTORY>]
    [-u|--uninstall] [--update-apply] [--update-check] [Template options]

dotnet new <TEMPLATE> [-l|--list] [--type <TYPE>]

dotnet new -h|--help
```

## <a name="description"></a><span data-ttu-id="46126-108">描述</span><span class="sxs-lookup"><span data-stu-id="46126-108">Description</span></span>

<span data-ttu-id="46126-109">`dotnet new` 命令基于模板创建 .NET 项目或其他项目。</span><span class="sxs-lookup"><span data-stu-id="46126-109">The `dotnet new` command creates a .NET project or other artifacts based on a template.</span></span>

<span data-ttu-id="46126-110">命令调用[模板引擎](https://github.com/dotnet/templating)，以根据指定的模板和选项在磁盘上创建项目。</span><span class="sxs-lookup"><span data-stu-id="46126-110">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

### <a name="implicit-restore"></a><span data-ttu-id="46126-111">隐式还原</span><span class="sxs-lookup"><span data-stu-id="46126-111">Implicit restore</span></span>

[!INCLUDE[dotnet restore note](~/includes/dotnet-restore-note.md)]

## <a name="arguments"></a><span data-ttu-id="46126-112">自变量</span><span class="sxs-lookup"><span data-stu-id="46126-112">Arguments</span></span>

- **`TEMPLATE`**

  <span data-ttu-id="46126-113">调用命令时要实例化的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-113">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="46126-114">每个模板可能具有可传递的特定选项。</span><span class="sxs-lookup"><span data-stu-id="46126-114">Each template might have specific options you can pass.</span></span> <span data-ttu-id="46126-115">有关详细信息，请参阅[模板选项](#template-options)。</span><span class="sxs-lookup"><span data-stu-id="46126-115">For more information, see [Template options](#template-options).</span></span>

  <span data-ttu-id="46126-116">可以运行 `dotnet new --list` 或 `dotnet new -l` 以查看所有已安装模板的列表。</span><span class="sxs-lookup"><span data-stu-id="46126-116">You can run `dotnet new --list` or `dotnet new -l` to see a list of all installed templates.</span></span> <span data-ttu-id="46126-117">如果 `TEMPLATE` 值与返回表中的“模板”或“短名称”列中的文本不完全匹配，则会对这两列执行 substring 匹配。</span><span class="sxs-lookup"><span data-stu-id="46126-117">If the `TEMPLATE` value isn't an exact match on text in the **Templates** or **Short Name** column from the returned table, a substring match is performed on those two columns.</span></span>

  <span data-ttu-id="46126-118">从 .NET Core 3.0 SDK 开始，当你在以下情况下调用 `dotnet new` 命令时，CLI 将在 NuGet.org 中搜索模板：</span><span class="sxs-lookup"><span data-stu-id="46126-118">Starting with .NET Core 3.0 SDK, the CLI searches for templates in NuGet.org when you invoke the `dotnet new` command in the following conditions:</span></span>

  - <span data-ttu-id="46126-119">如果在调用 `dotnet new` 时 CLI 找不到模板匹配项，即使是部分匹配也不行。</span><span class="sxs-lookup"><span data-stu-id="46126-119">If the CLI can't find a template match when invoking `dotnet new`, not even partial.</span></span>
  - <span data-ttu-id="46126-120">如果有较新版本的模板可用。</span><span class="sxs-lookup"><span data-stu-id="46126-120">If there's a newer version of the template available.</span></span> <span data-ttu-id="46126-121">在这种情况下，将创建项目或工件，但 CLI 会就模板的更新版本发出警告。</span><span class="sxs-lookup"><span data-stu-id="46126-121">In this case, the project or artifact is created but the CLI warns you about an updated version of the template.</span></span>

  <span data-ttu-id="46126-122">下表显示随 .NET SDK 一起预安装的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-122">The following table shows the templates that come pre-installed with the .NET SDK.</span></span> <span data-ttu-id="46126-123">模板的默认语言显示在括号内。</span><span class="sxs-lookup"><span data-stu-id="46126-123">The default language for the template is shown inside the brackets.</span></span> <span data-ttu-id="46126-124">单击短名称链接可查看特定的模板选项。</span><span class="sxs-lookup"><span data-stu-id="46126-124">Click on the short name link to see the specific template options.</span></span>

| <span data-ttu-id="46126-125">模板</span><span class="sxs-lookup"><span data-stu-id="46126-125">Templates</span></span>                                    | <span data-ttu-id="46126-126">短名称</span><span class="sxs-lookup"><span data-stu-id="46126-126">Short name</span></span>                      | <span data-ttu-id="46126-127">语言</span><span class="sxs-lookup"><span data-stu-id="46126-127">Language</span></span>     | <span data-ttu-id="46126-128">Tags</span><span class="sxs-lookup"><span data-stu-id="46126-128">Tags</span></span>                                  | <span data-ttu-id="46126-129">已引入</span><span class="sxs-lookup"><span data-stu-id="46126-129">Introduced</span></span> |
|----------------------------------------------|---------------------------------|--------------|---------------------------------------|------------|
| <span data-ttu-id="46126-130">控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="46126-130">Console Application</span></span>                          | [<span data-ttu-id="46126-131">控制台</span><span class="sxs-lookup"><span data-stu-id="46126-131">console</span></span>](#console)             | <span data-ttu-id="46126-132">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-132">[C#], F#, VB</span></span> | <span data-ttu-id="46126-133">常用/控制台</span><span class="sxs-lookup"><span data-stu-id="46126-133">Common/Console</span></span>                        | <span data-ttu-id="46126-134">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-134">1.0</span></span>        |
| <span data-ttu-id="46126-135">类库</span><span class="sxs-lookup"><span data-stu-id="46126-135">Class library</span></span>                                | [<span data-ttu-id="46126-136">classlib</span><span class="sxs-lookup"><span data-stu-id="46126-136">classlib</span></span>](#classlib)           | <span data-ttu-id="46126-137">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-137">[C#], F#, VB</span></span> | <span data-ttu-id="46126-138">常用/库</span><span class="sxs-lookup"><span data-stu-id="46126-138">Common/Library</span></span>                        | <span data-ttu-id="46126-139">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-139">1.0</span></span>        |
| <span data-ttu-id="46126-140">WPF 应用程序</span><span class="sxs-lookup"><span data-stu-id="46126-140">WPF Application</span></span>                              | [<span data-ttu-id="46126-141">wpf</span><span class="sxs-lookup"><span data-stu-id="46126-141">wpf</span></span>](#wpf)                     | <span data-ttu-id="46126-142">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-142">[C#], VB</span></span>     | <span data-ttu-id="46126-143">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="46126-143">Common/WPF</span></span>                            | <span data-ttu-id="46126-144">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-144">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-145">WPF 类库</span><span class="sxs-lookup"><span data-stu-id="46126-145">WPF Class library</span></span>                            | [<span data-ttu-id="46126-146">wpflib</span><span class="sxs-lookup"><span data-stu-id="46126-146">wpflib</span></span>](#wpf)                  | <span data-ttu-id="46126-147">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-147">[C#], VB</span></span>     | <span data-ttu-id="46126-148">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="46126-148">Common/WPF</span></span>                            | <span data-ttu-id="46126-149">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-149">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-150">WPF 自定义控件库</span><span class="sxs-lookup"><span data-stu-id="46126-150">WPF Custom Control Library</span></span>                   | [<span data-ttu-id="46126-151">wpfcustomcontrollib</span><span class="sxs-lookup"><span data-stu-id="46126-151">wpfcustomcontrollib</span></span>](#wpf)     | <span data-ttu-id="46126-152">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-152">[C#], VB</span></span>     | <span data-ttu-id="46126-153">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="46126-153">Common/WPF</span></span>                            | <span data-ttu-id="46126-154">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-154">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-155">WPF 用户控件库</span><span class="sxs-lookup"><span data-stu-id="46126-155">WPF User Control Library</span></span>                     | [<span data-ttu-id="46126-156">wpfusercontrollib</span><span class="sxs-lookup"><span data-stu-id="46126-156">wpfusercontrollib</span></span>](#wpf)       | <span data-ttu-id="46126-157">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-157">[C#], VB</span></span>     | <span data-ttu-id="46126-158">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="46126-158">Common/WPF</span></span>                            | <span data-ttu-id="46126-159">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-159">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-160">Windows 窗体 (WinForms) 应用程序</span><span class="sxs-lookup"><span data-stu-id="46126-160">Windows Forms (WinForms) Application</span></span>         | [<span data-ttu-id="46126-161">winforms</span><span class="sxs-lookup"><span data-stu-id="46126-161">winforms</span></span>](#winforms)           | <span data-ttu-id="46126-162">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-162">[C#], VB</span></span>     | <span data-ttu-id="46126-163">常用/WinForms</span><span class="sxs-lookup"><span data-stu-id="46126-163">Common/WinForms</span></span>                       | <span data-ttu-id="46126-164">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-164">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-165">Windows 窗体 (WinForms) 类库</span><span class="sxs-lookup"><span data-stu-id="46126-165">Windows Forms (WinForms) Class library</span></span>       | [<span data-ttu-id="46126-166">winformslib</span><span class="sxs-lookup"><span data-stu-id="46126-166">winformslib</span></span>](#winforms)        | <span data-ttu-id="46126-167">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="46126-167">[C#], VB</span></span>     | <span data-ttu-id="46126-168">常用/WinForms</span><span class="sxs-lookup"><span data-stu-id="46126-168">Common/WinForms</span></span>                       | <span data-ttu-id="46126-169">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="46126-169">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="46126-170">Worker Service</span><span class="sxs-lookup"><span data-stu-id="46126-170">Worker Service</span></span>                               | [<span data-ttu-id="46126-171">worker</span><span class="sxs-lookup"><span data-stu-id="46126-171">worker</span></span>](#web-others)           | <span data-ttu-id="46126-172">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-172">[C#]</span></span>         | <span data-ttu-id="46126-173">常用/Worker/Web</span><span class="sxs-lookup"><span data-stu-id="46126-173">Common/Worker/Web</span></span>                     | <span data-ttu-id="46126-174">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-174">3.0</span></span>        |
| <span data-ttu-id="46126-175">单元测试项目</span><span class="sxs-lookup"><span data-stu-id="46126-175">Unit Test Project</span></span>                            | [<span data-ttu-id="46126-176">mstest</span><span class="sxs-lookup"><span data-stu-id="46126-176">mstest</span></span>](#test)                 | <span data-ttu-id="46126-177">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-177">[C#], F#, VB</span></span> | <span data-ttu-id="46126-178">测试/MSTest</span><span class="sxs-lookup"><span data-stu-id="46126-178">Test/MSTest</span></span>                           | <span data-ttu-id="46126-179">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-179">1.0</span></span>        |
| <span data-ttu-id="46126-180">NUnit 3 测试项目</span><span class="sxs-lookup"><span data-stu-id="46126-180">NUnit 3 Test Project</span></span>                         | [<span data-ttu-id="46126-181">nunit</span><span class="sxs-lookup"><span data-stu-id="46126-181">nunit</span></span>](#nunit)                 | <span data-ttu-id="46126-182">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-182">[C#], F#, VB</span></span> | <span data-ttu-id="46126-183">测试/NUnit</span><span class="sxs-lookup"><span data-stu-id="46126-183">Test/NUnit</span></span>                            | <span data-ttu-id="46126-184">2.1.400</span><span class="sxs-lookup"><span data-stu-id="46126-184">2.1.400</span></span>    |
| <span data-ttu-id="46126-185">NUnit 3 测试项</span><span class="sxs-lookup"><span data-stu-id="46126-185">NUnit 3 Test Item</span></span>                            | `nunit-test`                    | <span data-ttu-id="46126-186">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-186">[C#], F#, VB</span></span> | <span data-ttu-id="46126-187">测试/NUnit</span><span class="sxs-lookup"><span data-stu-id="46126-187">Test/NUnit</span></span>                            | <span data-ttu-id="46126-188">2.2</span><span class="sxs-lookup"><span data-stu-id="46126-188">2.2</span></span>        |
| <span data-ttu-id="46126-189">xUnit 测试项目</span><span class="sxs-lookup"><span data-stu-id="46126-189">xUnit Test Project</span></span>                           | [<span data-ttu-id="46126-190">xunit</span><span class="sxs-lookup"><span data-stu-id="46126-190">xunit</span></span>](#test)                  | <span data-ttu-id="46126-191">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="46126-191">[C#], F#, VB</span></span> | <span data-ttu-id="46126-192">测试/xUnit</span><span class="sxs-lookup"><span data-stu-id="46126-192">Test/xUnit</span></span>                            | <span data-ttu-id="46126-193">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-193">1.0</span></span>        |
| <span data-ttu-id="46126-194">Razor 组件</span><span class="sxs-lookup"><span data-stu-id="46126-194">Razor Component</span></span>                              | `razorcomponent`                | <span data-ttu-id="46126-195">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-195">[C#]</span></span>         | <span data-ttu-id="46126-196">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="46126-196">Web/ASP.NET</span></span>                           | <span data-ttu-id="46126-197">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-197">3.0</span></span>        |
| <span data-ttu-id="46126-198">Razor 页</span><span class="sxs-lookup"><span data-stu-id="46126-198">Razor Page</span></span>                                   | [<span data-ttu-id="46126-199">page</span><span class="sxs-lookup"><span data-stu-id="46126-199">page</span></span>](#page)                   | <span data-ttu-id="46126-200">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-200">[C#]</span></span>         | <span data-ttu-id="46126-201">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="46126-201">Web/ASP.NET</span></span>                           | <span data-ttu-id="46126-202">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-202">2.0</span></span>        |
| <span data-ttu-id="46126-203">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="46126-203">MVC ViewImports</span></span>                              | [<span data-ttu-id="46126-204">viewimports</span><span class="sxs-lookup"><span data-stu-id="46126-204">viewimports</span></span>](#namespace)       | <span data-ttu-id="46126-205">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-205">[C#]</span></span>         | <span data-ttu-id="46126-206">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="46126-206">Web/ASP.NET</span></span>                           | <span data-ttu-id="46126-207">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-207">2.0</span></span>        |
| <span data-ttu-id="46126-208">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="46126-208">MVC ViewStart</span></span>                                | `viewstart`                     | <span data-ttu-id="46126-209">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-209">[C#]</span></span>         | <span data-ttu-id="46126-210">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="46126-210">Web/ASP.NET</span></span>                           | <span data-ttu-id="46126-211">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-211">2.0</span></span>        |
| <span data-ttu-id="46126-212">Blazor 服务器应用</span><span class="sxs-lookup"><span data-stu-id="46126-212">Blazor Server App</span></span>                            | [<span data-ttu-id="46126-213">blazorserver</span><span class="sxs-lookup"><span data-stu-id="46126-213">blazorserver</span></span>](#blazorserver)   | <span data-ttu-id="46126-214">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-214">[C#]</span></span>         | <span data-ttu-id="46126-215">Web/Blazor</span><span class="sxs-lookup"><span data-stu-id="46126-215">Web/Blazor</span></span>                            | <span data-ttu-id="46126-216">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-216">3.0</span></span>        |
| <span data-ttu-id="46126-217">Blazor WebAssembly 应用</span><span class="sxs-lookup"><span data-stu-id="46126-217">Blazor WebAssembly App</span></span>                       | [<span data-ttu-id="46126-218">blazorwasm</span><span class="sxs-lookup"><span data-stu-id="46126-218">blazorwasm</span></span>](#blazorwasm)       | <span data-ttu-id="46126-219">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-219">[C#]</span></span>         | <span data-ttu-id="46126-220">Web/Blazor/WebAssembly</span><span class="sxs-lookup"><span data-stu-id="46126-220">Web/Blazor/WebAssembly</span></span>                | <span data-ttu-id="46126-221">3.1.300</span><span class="sxs-lookup"><span data-stu-id="46126-221">3.1.300</span></span>    |
| <span data-ttu-id="46126-222">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="46126-222">ASP.NET Core Empty</span></span>                           | [<span data-ttu-id="46126-223">web</span><span class="sxs-lookup"><span data-stu-id="46126-223">web</span></span>](#web)                     | <span data-ttu-id="46126-224">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="46126-224">[C#], F#</span></span>     | <span data-ttu-id="46126-225">Web/空</span><span class="sxs-lookup"><span data-stu-id="46126-225">Web/Empty</span></span>                             | <span data-ttu-id="46126-226">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-226">1.0</span></span>        |
| <span data-ttu-id="46126-227">ASP.NET Core Web 应用程序 (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="46126-227">ASP.NET Core Web App (Model-View-Controller)</span></span> | [<span data-ttu-id="46126-228">mvc</span><span class="sxs-lookup"><span data-stu-id="46126-228">mvc</span></span>](#web-options)             | <span data-ttu-id="46126-229">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="46126-229">[C#], F#</span></span>     | <span data-ttu-id="46126-230">Web/MVC</span><span class="sxs-lookup"><span data-stu-id="46126-230">Web/MVC</span></span>                               | <span data-ttu-id="46126-231">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-231">1.0</span></span>        |
| <span data-ttu-id="46126-232">ASP.NET Core Web 应用程序</span><span class="sxs-lookup"><span data-stu-id="46126-232">ASP.NET Core Web App</span></span>                         | [<span data-ttu-id="46126-233">webapp、razor</span><span class="sxs-lookup"><span data-stu-id="46126-233">webapp, razor</span></span>](#web-options)   | <span data-ttu-id="46126-234">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-234">[C#]</span></span>         | <span data-ttu-id="46126-235">Web/MVC/Razor Pages</span><span class="sxs-lookup"><span data-stu-id="46126-235">Web/MVC/Razor Pages</span></span>                   | <span data-ttu-id="46126-236">2.2、2.0</span><span class="sxs-lookup"><span data-stu-id="46126-236">2.2, 2.0</span></span>   |
| <span data-ttu-id="46126-237">含 Angular 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="46126-237">ASP.NET Core with Angular</span></span>                    | [<span data-ttu-id="46126-238">angular</span><span class="sxs-lookup"><span data-stu-id="46126-238">angular</span></span>](#spa)                 | <span data-ttu-id="46126-239">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-239">[C#]</span></span>         | <span data-ttu-id="46126-240">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="46126-240">Web/MVC/SPA</span></span>                           | <span data-ttu-id="46126-241">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-241">2.0</span></span>        |
| <span data-ttu-id="46126-242">含 React.js 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="46126-242">ASP.NET Core with React.js</span></span>                   | [<span data-ttu-id="46126-243">react</span><span class="sxs-lookup"><span data-stu-id="46126-243">react</span></span>](#spa)                   | <span data-ttu-id="46126-244">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-244">[C#]</span></span>         | <span data-ttu-id="46126-245">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="46126-245">Web/MVC/SPA</span></span>                           | <span data-ttu-id="46126-246">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-246">2.0</span></span>        |
| <span data-ttu-id="46126-247">含 React.js 和 Redux 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="46126-247">ASP.NET Core with React.js and Redux</span></span>         | [<span data-ttu-id="46126-248">reactredux</span><span class="sxs-lookup"><span data-stu-id="46126-248">reactredux</span></span>](#reactredux)       | <span data-ttu-id="46126-249">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-249">[C#]</span></span>         | <span data-ttu-id="46126-250">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="46126-250">Web/MVC/SPA</span></span>                           | <span data-ttu-id="46126-251">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-251">2.0</span></span>        |
| <span data-ttu-id="46126-252">Razor 类库</span><span class="sxs-lookup"><span data-stu-id="46126-252">Razor Class Library</span></span>                          | [<span data-ttu-id="46126-253">razorclasslib</span><span class="sxs-lookup"><span data-stu-id="46126-253">razorclasslib</span></span>](#razorclasslib) | <span data-ttu-id="46126-254">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-254">[C#]</span></span>         | <span data-ttu-id="46126-255">Web/Razor/库/Razor 类库</span><span class="sxs-lookup"><span data-stu-id="46126-255">Web/Razor/Library/Razor Class Library</span></span> | <span data-ttu-id="46126-256">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-256">2.1</span></span>        |
| <span data-ttu-id="46126-257">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="46126-257">ASP.NET Core Web API</span></span>                         | [<span data-ttu-id="46126-258">webapi</span><span class="sxs-lookup"><span data-stu-id="46126-258">webapi</span></span>](#webapi)               | <span data-ttu-id="46126-259">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="46126-259">[C#], F#</span></span>     | <span data-ttu-id="46126-260">Web/WebAPI</span><span class="sxs-lookup"><span data-stu-id="46126-260">Web/WebAPI</span></span>                            | <span data-ttu-id="46126-261">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-261">1.0</span></span>        |
| <span data-ttu-id="46126-262">ASP.NET Core gRPC 服务</span><span class="sxs-lookup"><span data-stu-id="46126-262">ASP.NET Core gRPC Service</span></span>                    | [<span data-ttu-id="46126-263">grpc</span><span class="sxs-lookup"><span data-stu-id="46126-263">grpc</span></span>](#web-others)             | <span data-ttu-id="46126-264">[C#]</span><span class="sxs-lookup"><span data-stu-id="46126-264">[C#]</span></span>         | <span data-ttu-id="46126-265">Web/gRPC</span><span class="sxs-lookup"><span data-stu-id="46126-265">Web/gRPC</span></span>                              | <span data-ttu-id="46126-266">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-266">3.0</span></span>        |
| <span data-ttu-id="46126-267">dotnet gitignore 文件</span><span class="sxs-lookup"><span data-stu-id="46126-267">dotnet gitignore file</span></span>                        | `gitignore`                     |              | <span data-ttu-id="46126-268">配置</span><span class="sxs-lookup"><span data-stu-id="46126-268">Config</span></span>                                | <span data-ttu-id="46126-269">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-269">3.0</span></span>        |
| <span data-ttu-id="46126-270">global.json 文件</span><span class="sxs-lookup"><span data-stu-id="46126-270">global.json file</span></span>                             | [<span data-ttu-id="46126-271">globaljson</span><span class="sxs-lookup"><span data-stu-id="46126-271">globaljson</span></span>](#globaljson)       |              | <span data-ttu-id="46126-272">配置</span><span class="sxs-lookup"><span data-stu-id="46126-272">Config</span></span>                                | <span data-ttu-id="46126-273">2.0</span><span class="sxs-lookup"><span data-stu-id="46126-273">2.0</span></span>        |
| <span data-ttu-id="46126-274">NuGet 配置</span><span class="sxs-lookup"><span data-stu-id="46126-274">NuGet Config</span></span>                                 | `nugetconfig`                   |              | <span data-ttu-id="46126-275">配置</span><span class="sxs-lookup"><span data-stu-id="46126-275">Config</span></span>                                | <span data-ttu-id="46126-276">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-276">1.0</span></span>        |
| <span data-ttu-id="46126-277">Dotnet 本地工具清单文件</span><span class="sxs-lookup"><span data-stu-id="46126-277">Dotnet local tool manifest file</span></span>              | `tool-manifest`                 |              | <span data-ttu-id="46126-278">配置</span><span class="sxs-lookup"><span data-stu-id="46126-278">Config</span></span>                                | <span data-ttu-id="46126-279">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-279">3.0</span></span>        |
| <span data-ttu-id="46126-280">Web 配置</span><span class="sxs-lookup"><span data-stu-id="46126-280">Web Config</span></span>                                   | `webconfig`                     |              | <span data-ttu-id="46126-281">配置</span><span class="sxs-lookup"><span data-stu-id="46126-281">Config</span></span>                                | <span data-ttu-id="46126-282">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-282">1.0</span></span>        |
| <span data-ttu-id="46126-283">解决方案文件</span><span class="sxs-lookup"><span data-stu-id="46126-283">Solution File</span></span>                                | `sln`                           |              | <span data-ttu-id="46126-284">解决方案</span><span class="sxs-lookup"><span data-stu-id="46126-284">Solution</span></span>                              | <span data-ttu-id="46126-285">1.0</span><span class="sxs-lookup"><span data-stu-id="46126-285">1.0</span></span>        |
| <span data-ttu-id="46126-286">协议缓冲区文件</span><span class="sxs-lookup"><span data-stu-id="46126-286">Protocol Buffer File</span></span>                         | [<span data-ttu-id="46126-287">proto</span><span class="sxs-lookup"><span data-stu-id="46126-287">proto</span></span>](#namespace)             |              | <span data-ttu-id="46126-288">Web/gRPC</span><span class="sxs-lookup"><span data-stu-id="46126-288">Web/gRPC</span></span>                              | <span data-ttu-id="46126-289">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-289">3.0</span></span>        |

## <a name="options"></a><span data-ttu-id="46126-290">选项</span><span class="sxs-lookup"><span data-stu-id="46126-290">Options</span></span>

- **`--dry-run`**

  <span data-ttu-id="46126-291">显示有关以下内容的摘要：给定命令运行导致模板创建时发生的情况。</span><span class="sxs-lookup"><span data-stu-id="46126-291">Displays a summary of what would happen if the given command were run if it would result in a template creation.</span></span> <span data-ttu-id="46126-292">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-292">Available since .NET Core 2.2 SDK.</span></span>

- **`--force`**

  <span data-ttu-id="46126-293">强制生成内容，即使会更改现有文件，也不例外。</span><span class="sxs-lookup"><span data-stu-id="46126-293">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="46126-294">当选择的模板将覆盖输出目录中的现有文件时，需要执行此操作。</span><span class="sxs-lookup"><span data-stu-id="46126-294">This is required when the template chosen would override existing files in the output directory.</span></span>

- **`-h|--help`**

  <span data-ttu-id="46126-295">打印命令帮助。</span><span class="sxs-lookup"><span data-stu-id="46126-295">Prints out help for the command.</span></span> <span data-ttu-id="46126-296">可针对 `dotnet new` 命令本身或任何模板调用它。</span><span class="sxs-lookup"><span data-stu-id="46126-296">It can be invoked for the `dotnet new` command itself or for any template.</span></span> <span data-ttu-id="46126-297">例如 `dotnet new mvc --help`。</span><span class="sxs-lookup"><span data-stu-id="46126-297">For example, `dotnet new mvc --help`.</span></span>

- **`-i|--install <PATH|NUGET_ID>`**

  <span data-ttu-id="46126-298">从提供的 `PATH` 或 `NUGET_ID` 安装模板包。</span><span class="sxs-lookup"><span data-stu-id="46126-298">Installs a template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="46126-299">若要安装模板包的预发布版本，需要以 `<package-name>::<package-version>` 格式指定该版本。</span><span class="sxs-lookup"><span data-stu-id="46126-299">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="46126-300">默认情况下，`dotnet new` 为该版本传递 \*，它表示最新的稳定包版本。</span><span class="sxs-lookup"><span data-stu-id="46126-300">By default, `dotnet new` passes \* for the version, which represents the latest stable package version.</span></span> <span data-ttu-id="46126-301">请在[示例](#examples)部分查看示例。</span><span class="sxs-lookup"><span data-stu-id="46126-301">See an example in the [Examples](#examples) section.</span></span>
  
  <span data-ttu-id="46126-302">如果在运行此命令时已经安装了模板的某个版本，则该模板将更新到指定版本，如果没有指定版本，则将更新到最新的稳定版本。</span><span class="sxs-lookup"><span data-stu-id="46126-302">If a version of the template was already installed when you run this command, the template will be updated to the specified version, or to the latest stable version if no version was specified.</span></span>

  <span data-ttu-id="46126-303">若要了解如何创建自定义模板，请参阅 [dotnet new 自定义模板](custom-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-303">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

- **`-l|--list`**

  <span data-ttu-id="46126-304">列出包含指定名称的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-304">Lists templates containing the specified name.</span></span> <span data-ttu-id="46126-305">如果未指定名称，则列出所有模板。</span><span class="sxs-lookup"><span data-stu-id="46126-305">If no name is specified, lists all templates.</span></span>

- **`-lang|--language {C#|F#|VB}`**

  <span data-ttu-id="46126-306">要创建的模板的语言。</span><span class="sxs-lookup"><span data-stu-id="46126-306">The language of the template to create.</span></span> <span data-ttu-id="46126-307">接受的语言因模板而异（请参阅[参数](#arguments)部分中的默认值）。</span><span class="sxs-lookup"><span data-stu-id="46126-307">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="46126-308">对于某些模板无效。</span><span class="sxs-lookup"><span data-stu-id="46126-308">Not valid for some templates.</span></span>

  > [!NOTE]
  > <span data-ttu-id="46126-309">某些 shell 将 `#` 解释为特殊字符。</span><span class="sxs-lookup"><span data-stu-id="46126-309">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="46126-310">在这些情况下，请将语言参数值括在引号中。</span><span class="sxs-lookup"><span data-stu-id="46126-310">In those cases, enclose the language parameter value in quotes.</span></span> <span data-ttu-id="46126-311">例如 `dotnet new console -lang "F#"`。</span><span class="sxs-lookup"><span data-stu-id="46126-311">For example, `dotnet new console -lang "F#"`.</span></span>

- **`-n|--name <OUTPUT_NAME>`**

  <span data-ttu-id="46126-312">所创建的输出的名称。</span><span class="sxs-lookup"><span data-stu-id="46126-312">The name for the created output.</span></span> <span data-ttu-id="46126-313">如果未指定名称，使用的是当前目录的名称。</span><span class="sxs-lookup"><span data-stu-id="46126-313">If no name is specified, the name of the current directory is used.</span></span>

- **`--nuget-source <SOURCE>`**

  <span data-ttu-id="46126-314">指定在安装期间要使用的 NuGet 源。</span><span class="sxs-lookup"><span data-stu-id="46126-314">Specifies a NuGet source to use during install.</span></span>

- **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="46126-315">用于放置生成的输出的位置。</span><span class="sxs-lookup"><span data-stu-id="46126-315">Location to place the generated output.</span></span> <span data-ttu-id="46126-316">默认为当前目录。</span><span class="sxs-lookup"><span data-stu-id="46126-316">The default is the current directory.</span></span>

- **`--type <TYPE>`**

  <span data-ttu-id="46126-317">根据可用类型筛选模板。</span><span class="sxs-lookup"><span data-stu-id="46126-317">Filters templates based on available types.</span></span> <span data-ttu-id="46126-318">预定义的值为 `project` 和 `item`。</span><span class="sxs-lookup"><span data-stu-id="46126-318">Predefined values are `project` and `item`.</span></span>

- **`-u|--uninstall [PATH|NUGET_ID]`**

  <span data-ttu-id="46126-319">在提供的 `PATH` 或 `NUGET_ID` 中卸载模板包。</span><span class="sxs-lookup"><span data-stu-id="46126-319">Uninstalls a template pack at the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="46126-320">如果未指定 `<PATH|NUGET_ID>` 值，将显示所有当前安装的模板包及其关联的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-320">When the `<PATH|NUGET_ID>` value isn't specified, all currently installed template packs and their associated templates are displayed.</span></span> <span data-ttu-id="46126-321">指定 `NUGET_ID` 时，请勿包含版本号。</span><span class="sxs-lookup"><span data-stu-id="46126-321">When specifying `NUGET_ID`, don't include the version number.</span></span>

  <span data-ttu-id="46126-322">如果未指定此选项的参数，该命令将列出已安装的模板及其详细信息。</span><span class="sxs-lookup"><span data-stu-id="46126-322">If you don't specify a parameter to this option, the command lists the installed templates and details about them.</span></span>

  > [!NOTE]
  > <span data-ttu-id="46126-323">若要使用 `PATH` 卸载模板，需要完全限定路径。</span><span class="sxs-lookup"><span data-stu-id="46126-323">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="46126-324">例如，C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp 有效，但是包含文件夹中的 ./GarciaSoftware.ConsoleTemplate.CSharp 无效 。</span><span class="sxs-lookup"><span data-stu-id="46126-324">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
  > <span data-ttu-id="46126-325">模板路径中不要包含最后的终止目录斜杠。</span><span class="sxs-lookup"><span data-stu-id="46126-325">Don't include a final terminating directory slash on your template path.</span></span>

- **`--update-apply`**

  <span data-ttu-id="46126-326">检查是否有可用于当前安装的模板包的更新并安装这些更新。</span><span class="sxs-lookup"><span data-stu-id="46126-326">Checks if there are updates available for the template packs that are currently installed and installs them.</span></span> <span data-ttu-id="46126-327">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-327">Available since .NET Core 3.0 SDK.</span></span>

- **`--update-check`**

  <span data-ttu-id="46126-328">检查是否有可用于当前安装的模板包的更新。</span><span class="sxs-lookup"><span data-stu-id="46126-328">Checks if there are updates available for the template packs that are currently installed.</span></span> <span data-ttu-id="46126-329">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-329">Available since .NET Core 3.0 SDK.</span></span>

## <a name="template-options"></a><span data-ttu-id="46126-330">模板选项</span><span class="sxs-lookup"><span data-stu-id="46126-330">Template options</span></span>

<span data-ttu-id="46126-331">每个项目模板都可能有附加选项。</span><span class="sxs-lookup"><span data-stu-id="46126-331">Each project template may have additional options available.</span></span> <span data-ttu-id="46126-332">核心模板有以下附加选项：</span><span class="sxs-lookup"><span data-stu-id="46126-332">The core templates have the following additional options:</span></span>

### <a name="console"></a><span data-ttu-id="46126-333">控制台</span><span class="sxs-lookup"><span data-stu-id="46126-333">console</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-334">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-334">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-335">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-335">Available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="46126-336">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-336">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-337">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-337">SDK version</span></span> | <span data-ttu-id="46126-338">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-338">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-339">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-339">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-340">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-340">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-341">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-341">3.0</span></span>         | `netcoreapp3.0` |

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="46126-342">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="46126-342">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="46126-343">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="46126-343">For example, use `--langVersion 7.3` to use C# 7.3.</span></span> <span data-ttu-id="46126-344">不支持 F#。</span><span class="sxs-lookup"><span data-stu-id="46126-344">Not supported for F#.</span></span> <span data-ttu-id="46126-345">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-345">Available since .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-346">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="46126-346">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-347">如已指定，则在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-347">If specified, doesn't execute an implicit restore during project creation.</span></span> <span data-ttu-id="46126-348">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-348">Available since .NET Core 2.2 SDK.</span></span>

<span data-ttu-id="46126-349">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-349">\*\*_</span></span>

### <a name="classlib"></a><span data-ttu-id="46126-350">classlib</span><span class="sxs-lookup"><span data-stu-id="46126-350">classlib</span></span>

- <span data-ttu-id="46126-351">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-351">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-352">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-352">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-353">值：`net5.0` 或 `netcoreapp<version>`（若要创建 .NET 类库），或`netstandard<version>`（若要创建 .NET Standard 类库）。</span><span class="sxs-lookup"><span data-stu-id="46126-353">Values: `net5.0` or `netcoreapp<version>` to create a .NET Class Library or `netstandard<version>` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="46126-354">.NET 5.0 SDK 的默认值是 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="46126-354">The default value for .NET 5.0 SDK is `net5.0`.</span></span>

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="46126-355">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="46126-355">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="46126-356">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="46126-356">For example, use `--langVersion 7.3` to use C# 7.3.</span></span> <span data-ttu-id="46126-357">不支持 F#。</span><span class="sxs-lookup"><span data-stu-id="46126-357">Not supported for F#.</span></span> <span data-ttu-id="46126-358">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-358">Available since .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-359">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="46126-359">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-360">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-360">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-361">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-361">\*\*_</span></span>

### <a name="wpf-wpflib-wpfcustomcontrollib-wpfusercontrollib"></a><a name="wpf"></a> <span data-ttu-id="46126-362">wpf、wpflib、wpfcustomcontrollib、wpfusercontrollib</span><span class="sxs-lookup"><span data-stu-id="46126-362">wpf, wpflib, wpfcustomcontrollib, wpfusercontrollib</span></span>

- <span data-ttu-id="46126-363">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-363">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-364">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-364">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-365">默认值为 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="46126-365">The default value is `net5.0`.</span></span> <span data-ttu-id="46126-366">自 .NET Core 3.1 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-366">Available since .NET Core 3.1 SDK.</span></span>

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="46126-367">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="46126-367">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="46126-368">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="46126-368">For example, use `--langVersion 7.3` to use C# 7.3.</span></span>

  <span data-ttu-id="46126-369">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="46126-369">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-370">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-370">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-371">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-371">\*\*_</span></span>

### <a name="winforms-winformslib"></a><a name="winforms"></a> <span data-ttu-id="46126-372">winforms、winformslib</span><span class="sxs-lookup"><span data-stu-id="46126-372">winforms, winformslib</span></span>

- <span data-ttu-id="46126-373">_ *`--langVersion <VERSION_NUMBER>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-373">_ *`--langVersion <VERSION_NUMBER>`*\*</span></span>

  <span data-ttu-id="46126-374">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="46126-374">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="46126-375">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="46126-375">For example, use `--langVersion 7.3` to use C# 7.3.</span></span>

  <span data-ttu-id="46126-376">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="46126-376">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-377">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-377">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-378">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-378">\*\*_</span></span>

### <a name="worker-grpc"></a><a name="web-others"></a> <span data-ttu-id="46126-379">worker、grpc</span><span class="sxs-lookup"><span data-stu-id="46126-379">worker, grpc</span></span>

- <span data-ttu-id="46126-380">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-380">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-381">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-381">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-382">默认值为 `netcoreapp3.1`。</span><span class="sxs-lookup"><span data-stu-id="46126-382">The default value is `netcoreapp3.1`.</span></span> <span data-ttu-id="46126-383">自 .NET Core 3.1 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-383">Available since .NET Core 3.1 SDK.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-384">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-384">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-385">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-385">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-386">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-386">\*\*_</span></span>

### <a name="mstest-xunit"></a><a name="test"></a> <span data-ttu-id="46126-387">mstest、xunit</span><span class="sxs-lookup"><span data-stu-id="46126-387">mstest, xunit</span></span>

- <span data-ttu-id="46126-388">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-388">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-389">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-389">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-390">自 .NET Core 3.0 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="46126-390">Option available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="46126-391">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-391">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-392">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-392">SDK version</span></span> | <span data-ttu-id="46126-393">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-393">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-394">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-394">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-395">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-395">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-396">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-396">3.0</span></span>         | `netcoreapp3.0` |

- **`-p|--enable-pack`**

  <span data-ttu-id="46126-397">允许使用 [dotnet pack](dotnet-pack.md) 为项目打包。</span><span class="sxs-lookup"><span data-stu-id="46126-397">Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-398">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-398">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-399">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-399">\*\*_</span></span>

### <a name="nunit"></a><span data-ttu-id="46126-400">nunit</span><span class="sxs-lookup"><span data-stu-id="46126-400">nunit</span></span>

- <span data-ttu-id="46126-401">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-401">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-402">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-402">Specifies the [framework](../../standard/frameworks.md) to target.</span></span>

  <span data-ttu-id="46126-403">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-403">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-404">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-404">SDK version</span></span> | <span data-ttu-id="46126-405">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-405">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-406">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-406">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-407">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-407">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-408">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-408">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="46126-409">2.2</span><span class="sxs-lookup"><span data-stu-id="46126-409">2.2</span></span>         | `netcoreapp2.2` |
  | <span data-ttu-id="46126-410">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-410">2.1</span></span>         | `netcoreapp2.1` |

- **`-p|--enable-pack`**

  <span data-ttu-id="46126-411">允许使用 [dotnet pack](dotnet-pack.md) 为项目打包。</span><span class="sxs-lookup"><span data-stu-id="46126-411">Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-412">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-412">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-413">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-413">\*\*_</span></span>

### <a name="page"></a><span data-ttu-id="46126-414">页</span><span class="sxs-lookup"><span data-stu-id="46126-414">page</span></span>

- <span data-ttu-id="46126-415">_ *`-na|--namespace <NAMESPACE_NAME>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-415">_ *`-na|--namespace <NAMESPACE_NAME>`*\*</span></span>

  <span data-ttu-id="46126-416">已生成代码的命名空间。</span><span class="sxs-lookup"><span data-stu-id="46126-416">Namespace for the generated code.</span></span> <span data-ttu-id="46126-417">默认值为 `MyApp.Namespace`。</span><span class="sxs-lookup"><span data-stu-id="46126-417">The default value is `MyApp.Namespace`.</span></span>

- **`-np|--no-pagemodel`**

  <span data-ttu-id="46126-418">创建不含 PageModel 的页。</span><span class="sxs-lookup"><span data-stu-id="46126-418">Creates the page without a PageModel.</span></span>

<span data-ttu-id="46126-419">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-419">\*\*_</span></span>

### <a name="viewimports-proto"></a><a name="namespace"></a> <span data-ttu-id="46126-420">viewimports、proto</span><span class="sxs-lookup"><span data-stu-id="46126-420">viewimports, proto</span></span>

- <span data-ttu-id="46126-421">_ *`-na|--namespace <NAMESPACE_NAME>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-421">_ *`-na|--namespace <NAMESPACE_NAME>`*\*</span></span>

  <span data-ttu-id="46126-422">已生成代码的命名空间。</span><span class="sxs-lookup"><span data-stu-id="46126-422">Namespace for the generated code.</span></span> <span data-ttu-id="46126-423">默认值为 `MyApp.Namespace`。</span><span class="sxs-lookup"><span data-stu-id="46126-423">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="46126-424">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-424">\*\*_</span></span>

### <a name="blazorserver"></a><span data-ttu-id="46126-425">blazorserver</span><span class="sxs-lookup"><span data-stu-id="46126-425">blazorserver</span></span>

- <span data-ttu-id="46126-426">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-426">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span></span>

  <span data-ttu-id="46126-427">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="46126-427">The type of authentication to use.</span></span> <span data-ttu-id="46126-428">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="46126-428">The possible values are:</span></span>

  - <span data-ttu-id="46126-429">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="46126-429">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="46126-430">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-430">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="46126-431">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-431">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="46126-432">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-432">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="46126-433">`MultiOrg` - 对多个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-433">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
  - <span data-ttu-id="46126-434">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-434">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="46126-435">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-435">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="46126-436">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-436">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-437">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="46126-437">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="46126-438">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-438">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="46126-439">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-439">Use with `IndividualB2C` authentication.</span></span>

- **`-rp|--reset-password-policy-id <ID>`**

  <span data-ttu-id="46126-440">此项目的重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-440">The reset password policy ID for this project.</span></span> <span data-ttu-id="46126-441">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-441">Use with `IndividualB2C` authentication.</span></span>

- **`-ep|--edit-profile-policy-id <ID>`**

  <span data-ttu-id="46126-442">此项目的编辑配置文件策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-442">The edit profile policy ID for this project.</span></span> <span data-ttu-id="46126-443">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-443">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="46126-444">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-444">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="46126-445">与 `SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-445">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="46126-446">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-446">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="46126-447">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-447">The Client ID for this project.</span></span> <span data-ttu-id="46126-448">与 `IndividualB2C`、`SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-448">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="46126-449">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="46126-449">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="46126-450">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="46126-450">The domain for the directory tenant.</span></span> <span data-ttu-id="46126-451">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-451">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-452">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="46126-452">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="46126-453">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="46126-453">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="46126-454">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-454">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-455">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="46126-455">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`--callback-path <PATH>`**

  <span data-ttu-id="46126-456">重定向 URI 的应用程序基路径中的请求路径。</span><span class="sxs-lookup"><span data-stu-id="46126-456">The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="46126-457">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-457">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-458">默认值为 `/signin-oidc`。</span><span class="sxs-lookup"><span data-stu-id="46126-458">The default value is `/signin-oidc`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="46126-459">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="46126-459">Allows this application read-access to the directory.</span></span> <span data-ttu-id="46126-460">仅适用于 `SingleOrg` 或 `MultiOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-460">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-461">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-461">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-462">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-462">Turns off HTTPS.</span></span> <span data-ttu-id="46126-463">此选项仅适用于 `Individual`、`IndividualB2C`、`SingleOrg` 和 `MultiOrg` 未用于 `--auth` 的情况。</span><span class="sxs-lookup"><span data-stu-id="46126-463">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used for `--auth`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="46126-464">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="46126-464">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="46126-465">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-465">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-466">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-466">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-467">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-467">\*\*_</span></span>

### <a name="blazorwasm"></a><span data-ttu-id="46126-468">blazorwasm</span><span class="sxs-lookup"><span data-stu-id="46126-468">blazorwasm</span></span>

- <span data-ttu-id="46126-469">_ *`-f|--framework <FRAMEWORK>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-469">_ *`-f|--framework <FRAMEWORK>`*\*</span></span>

  <span data-ttu-id="46126-470">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-470">Specifies the [framework](../../standard/frameworks.md) to target.</span></span>

  <span data-ttu-id="46126-471">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-471">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-472">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-472">SDK version</span></span> | <span data-ttu-id="46126-473">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-473">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-474">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-474">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-475">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-475">3.1</span></span>         | `netcoreapp3.1` |

- **`--no-restore`**

  <span data-ttu-id="46126-476">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-476">Doesn't execute an implicit restore during project creation.</span></span>

- **`-ho|--hosted`**

  <span data-ttu-id="46126-477">包括 Blazor WebAssembly 应用的 ASP.NET Core 主机。</span><span class="sxs-lookup"><span data-stu-id="46126-477">Includes an ASP.NET Core host for the Blazor WebAssembly app.</span></span>

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="46126-478">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="46126-478">The type of authentication to use.</span></span> <span data-ttu-id="46126-479">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="46126-479">The possible values are:</span></span>

  - <span data-ttu-id="46126-480">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="46126-480">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="46126-481">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-481">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="46126-482">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-482">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="46126-483">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-483">`SingleOrg` - Organizational authentication for a single tenant.</span></span>

- **`--authority <AUTHORITY>`**

  <span data-ttu-id="46126-484">OIDC 提供程序所属的机构。</span><span class="sxs-lookup"><span data-stu-id="46126-484">The authority of the OIDC provider.</span></span> <span data-ttu-id="46126-485">与 `Individual` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-485">Use with `Individual` authentication.</span></span> <span data-ttu-id="46126-486">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-486">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="46126-487">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-487">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="46126-488">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-488">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-489">默认值为 `https://aadB2CInstance.b2clogin.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-489">The default value is `https://aadB2CInstance.b2clogin.com/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="46126-490">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-490">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="46126-491">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-491">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="46126-492">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-492">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="46126-493">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-493">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-494">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-494">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="46126-495">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-495">The Client ID for this project.</span></span> <span data-ttu-id="46126-496">在独立方案中与 `IndividualB2C`、`SingleOrg` 或 `Individual` 身份验证一起使用。</span><span class="sxs-lookup"><span data-stu-id="46126-496">Use with `IndividualB2C`, `SingleOrg`, or `Individual` authentication in standalone scenarios.</span></span> <span data-ttu-id="46126-497">默认值为 `33333333-3333-3333-33333333333333333`。</span><span class="sxs-lookup"><span data-stu-id="46126-497">The default value is `33333333-3333-3333-33333333333333333`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="46126-498">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="46126-498">The domain for the directory tenant.</span></span> <span data-ttu-id="46126-499">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-499">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-500">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="46126-500">The default value is `qualified.domain.name`.</span></span>

- **`--app-id-uri <URI>`**

  <span data-ttu-id="46126-501">要调用的服务器 API 的应用 ID URI。</span><span class="sxs-lookup"><span data-stu-id="46126-501">The App ID Uri for the server API you want to call.</span></span> <span data-ttu-id="46126-502">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-502">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-503">默认值为 `api.id.uri`。</span><span class="sxs-lookup"><span data-stu-id="46126-503">The default value is `api.id.uri`.</span></span>

- **`--api-client-id <ID>`**

  <span data-ttu-id="46126-504">服务器承载的 API 的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-504">The Client ID for the API that the server hosts.</span></span> <span data-ttu-id="46126-505">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-505">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-506">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="46126-506">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`-s|--default-scope <SCOPE>`**

  <span data-ttu-id="46126-507">客户端为预配访问令牌所需请求的 API 作用域。</span><span class="sxs-lookup"><span data-stu-id="46126-507">The API scope the client needs to request to provision an access token.</span></span> <span data-ttu-id="46126-508">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-508">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-509">默认值为 `user_impersonation`。</span><span class="sxs-lookup"><span data-stu-id="46126-509">The default value is `user_impersonation`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="46126-510">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="46126-510">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="46126-511">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-511">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-512">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="46126-512">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="46126-513">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="46126-513">Allows this application read-access to the directory.</span></span> <span data-ttu-id="46126-514">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-514">Only applies to `SingleOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-515">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-515">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-p|--pwa`**

  <span data-ttu-id="46126-516">生成支持安装和脱机使用的渐进式 Web 应用程序 (PWA)。</span><span class="sxs-lookup"><span data-stu-id="46126-516">produces a Progressive Web Application (PWA) supporting installation and offline use.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-517">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-517">Turns off HTTPS.</span></span> <span data-ttu-id="46126-518">此选项仅适用于 `Individual`、`IndividualB2C` 和 `SingleOrg` 未用于 `--auth` 的情况。</span><span class="sxs-lookup"><span data-stu-id="46126-518">This option only applies if `Individual`, `IndividualB2C`, or `SingleOrg` aren't being used for `--auth`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="46126-519">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="46126-519">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="46126-520">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-520">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`--called-api-url <URL>`**

  <span data-ttu-id="46126-521">要从 Web 应用调用的 API 的 URL。</span><span class="sxs-lookup"><span data-stu-id="46126-521">URL of the API to call from the web app.</span></span> <span data-ttu-id="46126-522">仅适用于未指定 ASP.NET Core 主机的 `SingleOrg` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-522">Only applies to `SingleOrg` or `IndividualB2C` authentication without an ASP.NET Core host specified.</span></span> <span data-ttu-id="46126-523">默认值为 `https://graph.microsoft.com/v1.0/me`。</span><span class="sxs-lookup"><span data-stu-id="46126-523">The default value is `https://graph.microsoft.com/v1.0/me`.</span></span>

- **`--calls-graph`**

  <span data-ttu-id="46126-524">指定 Web 应用是否调用 Microsoft Graph。</span><span class="sxs-lookup"><span data-stu-id="46126-524">Specifies if the web app calls Microsoft Graph.</span></span> <span data-ttu-id="46126-525">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-525">Only applies to `SingleOrg` authentication.</span></span>

- **`--called-api-scopes <SCOPES>`**

  <span data-ttu-id="46126-526">为从 Web 应用调用 API 而请求的作用域。</span><span class="sxs-lookup"><span data-stu-id="46126-526">Scopes to request to call the API from the web app.</span></span> <span data-ttu-id="46126-527">仅适用于未指定 ASP.NET Core 主机的 `SingleOrg` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-527">Only applies to `SingleOrg` or `IndividualB2C` authentication without an ASP.NET Core host specified.</span></span> <span data-ttu-id="46126-528">默认值为 `user.read`。</span><span class="sxs-lookup"><span data-stu-id="46126-528">The default is `user.read`.</span></span>

<span data-ttu-id="46126-529">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-529">\*\*_</span></span>

### <a name="web"></a><span data-ttu-id="46126-530">Web</span><span class="sxs-lookup"><span data-stu-id="46126-530">web</span></span>

- <span data-ttu-id="46126-531">_ *`--exclude-launch-settings`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-531">_ *`--exclude-launch-settings`*\*</span></span>

  <span data-ttu-id="46126-532">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-532">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-533">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-533">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-534">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="46126-534">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-535">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-535">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-536">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-536">SDK version</span></span> | <span data-ttu-id="46126-537">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-537">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-538">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-538">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-539">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-539">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-540">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-540">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="46126-541">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-541">2.1</span></span>         | `netcoreapp2.1` |

- **`--no-restore`**

  <span data-ttu-id="46126-542">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-542">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-543">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-543">Turns off HTTPS.</span></span>

<span data-ttu-id="46126-544">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-544">\*\*_</span></span>

### <a name="mvc-webapp"></a><a name="web-options"></a> <span data-ttu-id="46126-545">mvc、webapp</span><span class="sxs-lookup"><span data-stu-id="46126-545">mvc, webapp</span></span>

- <span data-ttu-id="46126-546">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-546">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span></span>

  <span data-ttu-id="46126-547">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="46126-547">The type of authentication to use.</span></span> <span data-ttu-id="46126-548">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="46126-548">The possible values are:</span></span>

  - <span data-ttu-id="46126-549">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="46126-549">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="46126-550">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-550">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="46126-551">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-551">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="46126-552">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-552">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="46126-553">`MultiOrg` - 对多个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-553">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
  - <span data-ttu-id="46126-554">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-554">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="46126-555">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-555">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="46126-556">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-556">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-557">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="46126-557">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="46126-558">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-558">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="46126-559">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-559">Use with `IndividualB2C` authentication.</span></span>

- **`-rp|--reset-password-policy-id <ID>`**

  <span data-ttu-id="46126-560">此项目的重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-560">The reset password policy ID for this project.</span></span> <span data-ttu-id="46126-561">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-561">Use with `IndividualB2C` authentication.</span></span>

- **`-ep|--edit-profile-policy-id <ID>`**

  <span data-ttu-id="46126-562">此项目的编辑配置文件策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-562">The edit profile policy ID for this project.</span></span> <span data-ttu-id="46126-563">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-563">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="46126-564">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-564">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="46126-565">与 `SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-565">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="46126-566">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-566">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="46126-567">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-567">The Client ID for this project.</span></span> <span data-ttu-id="46126-568">与 `IndividualB2C`、`SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-568">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="46126-569">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="46126-569">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="46126-570">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="46126-570">The domain for the directory tenant.</span></span> <span data-ttu-id="46126-571">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-571">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-572">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="46126-572">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="46126-573">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="46126-573">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="46126-574">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-574">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-575">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="46126-575">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`--callback-path <PATH>`**

  <span data-ttu-id="46126-576">重定向 URI 的应用程序基路径中的请求路径。</span><span class="sxs-lookup"><span data-stu-id="46126-576">The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="46126-577">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-577">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-578">默认值为 `/signin-oidc`。</span><span class="sxs-lookup"><span data-stu-id="46126-578">The default value is `/signin-oidc`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="46126-579">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="46126-579">Allows this application read-access to the directory.</span></span> <span data-ttu-id="46126-580">仅适用于 `SingleOrg` 或 `MultiOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-580">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-581">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-581">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-582">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-582">Turns off HTTPS.</span></span> <span data-ttu-id="46126-583">此选项仅适用于未使用 `Individual`、`IndividualB2C`、`SingleOrg` 和 `MultiOrg` 的情况。</span><span class="sxs-lookup"><span data-stu-id="46126-583">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="46126-584">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="46126-584">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="46126-585">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-585">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-586">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-586">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-587">自 .NET Core 3.0 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="46126-587">Option available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="46126-588">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-588">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-589">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-589">SDK version</span></span> | <span data-ttu-id="46126-590">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-590">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-591">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-591">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-592">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-592">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-593">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-593">3.0</span></span>         | `netcoreapp3.0` |

- **`--no-restore`**

  <span data-ttu-id="46126-594">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-594">Doesn't execute an implicit restore during project creation.</span></span>

- **`--use-browserlink`**

  <span data-ttu-id="46126-595">在项目中添加 BrowserLink。</span><span class="sxs-lookup"><span data-stu-id="46126-595">Includes BrowserLink in the project.</span></span> <span data-ttu-id="46126-596">选项在 .NET Core 2.2 和 3.1 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="46126-596">Option not available in .NET Core 2.2 and 3.1 SDK.</span></span>

- **`-rrc|--razor-runtime-compilation`**

  <span data-ttu-id="46126-597">确定项目是否配置为在调试生成中使用 [Razor 运行时编译](/aspnet/core/mvc/views/view-compilation#runtime-compilation)。</span><span class="sxs-lookup"><span data-stu-id="46126-597">Determines if the project is configured to use [Razor runtime compilation](/aspnet/core/mvc/views/view-compilation#runtime-compilation) in Debug builds.</span></span> <span data-ttu-id="46126-598">自 .NET Core 3.1.201 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="46126-598">Option available since .NET Core 3.1.201 SDK.</span></span>

<span data-ttu-id="46126-599">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-599">\*\*_</span></span>

### <a name="angular-react"></a><a name="spa"></a> <span data-ttu-id="46126-600">angular、react</span><span class="sxs-lookup"><span data-stu-id="46126-600">angular, react</span></span>

- <span data-ttu-id="46126-601">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-601">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span></span>

  <span data-ttu-id="46126-602">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="46126-602">The type of authentication to use.</span></span> <span data-ttu-id="46126-603">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-603">Available since .NET Core 3.0 SDK.</span></span>
  
  <span data-ttu-id="46126-604">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="46126-604">The possible values are:</span></span>

  - <span data-ttu-id="46126-605">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="46126-605">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="46126-606">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-606">`Individual` - Individual authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-607">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-607">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-restore`**

  <span data-ttu-id="46126-608">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-608">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-609">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-609">Turns off HTTPS.</span></span> <span data-ttu-id="46126-610">仅当身份验证为 `None` 时，此选项才适用。</span><span class="sxs-lookup"><span data-stu-id="46126-610">This option only applies if authentication is `None`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="46126-611">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="46126-611">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="46126-612">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-612">Only applies to `Individual` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-613">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-613">Available since .NET Core 3.0 SDK.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-614">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-614">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-615">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="46126-615">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-616">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-616">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-617">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-617">SDK version</span></span> | <span data-ttu-id="46126-618">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-618">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-619">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-619">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-620">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-620">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-621">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-621">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="46126-622">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-622">2.1</span></span>         | `netcoreapp2.0` |

<span data-ttu-id="46126-623">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-623">\*\*_</span></span>

### <a name="reactredux"></a><span data-ttu-id="46126-624">reactredux</span><span class="sxs-lookup"><span data-stu-id="46126-624">reactredux</span></span>

- <span data-ttu-id="46126-625">_ *`--exclude-launch-settings`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-625">_ *`--exclude-launch-settings`*\*</span></span>

  <span data-ttu-id="46126-626">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-626">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-627">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-627">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-628">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="46126-628">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-629">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-629">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-630">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-630">SDK version</span></span> | <span data-ttu-id="46126-631">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-631">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-632">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-632">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-633">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-633">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-634">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-634">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="46126-635">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-635">2.1</span></span>         | `netcoreapp2.0` |

- **`--no-restore`**

  <span data-ttu-id="46126-636">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-636">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-637">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-637">Turns off HTTPS.</span></span>

<span data-ttu-id="46126-638">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-638">\*\*_</span></span>

### <a name="razorclasslib"></a><span data-ttu-id="46126-639">razorclasslib</span><span class="sxs-lookup"><span data-stu-id="46126-639">razorclasslib</span></span>

- <span data-ttu-id="46126-640">_ *`--no-restore`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-640">_ *`--no-restore`*\*</span></span>

  <span data-ttu-id="46126-641">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-641">Doesn't execute an implicit restore during project creation.</span></span>

- **`-s|--support-pages-and-views`**

  <span data-ttu-id="46126-642">除了将组件添加到此库以外，还支持添加传统的 Razor 页面和视图。</span><span class="sxs-lookup"><span data-stu-id="46126-642">Supports adding traditional Razor pages and Views in addition to components to this library.</span></span> <span data-ttu-id="46126-643">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="46126-643">Available since .NET Core 3.0 SDK.</span></span>

<span data-ttu-id="46126-644">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-644">\*\*_</span></span>
  
### <a name="webapi"></a><span data-ttu-id="46126-645">webapi</span><span class="sxs-lookup"><span data-stu-id="46126-645">webapi</span></span>

- <span data-ttu-id="46126-646">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-646">_ *`-au|--auth <AUTHENTICATION_TYPE>`*\*</span></span>

  <span data-ttu-id="46126-647">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="46126-647">The type of authentication to use.</span></span> <span data-ttu-id="46126-648">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="46126-648">The possible values are:</span></span>

  - <span data-ttu-id="46126-649">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="46126-649">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="46126-650">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-650">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="46126-651">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-651">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="46126-652">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-652">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="46126-653">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-653">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="46126-654">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-654">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="46126-655">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="46126-655">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="46126-656">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-656">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="46126-657">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-657">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="46126-658">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="46126-658">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="46126-659">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-659">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-660">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="46126-660">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="46126-661">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="46126-661">The Client ID for this project.</span></span> <span data-ttu-id="46126-662">与 `IndividualB2C` 或 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-662">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-663">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="46126-663">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="46126-664">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="46126-664">The domain for the directory tenant.</span></span> <span data-ttu-id="46126-665">与 `IndividualB2C` 或 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-665">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-666">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="46126-666">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="46126-667">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="46126-667">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="46126-668">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="46126-668">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="46126-669">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="46126-669">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="46126-670">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="46126-670">Allows this application read-access to the directory.</span></span> <span data-ttu-id="46126-671">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-671">Only applies to `SingleOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="46126-672">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="46126-672">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="46126-673">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="46126-673">Turns off HTTPS.</span></span> <span data-ttu-id="46126-674">`app.UseHsts` 和 `app.UseHttpsRedirection` 未添加到 `Startup.Configure` 中。</span><span class="sxs-lookup"><span data-stu-id="46126-674">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="46126-675">此选项仅适用于 `IndividualB2C` 或 `SingleOrg` 未用于身份验证的情况。</span><span class="sxs-lookup"><span data-stu-id="46126-675">This option only applies if `IndividualB2C` or `SingleOrg` aren't being used for authentication.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="46126-676">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="46126-676">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="46126-677">仅适用于 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="46126-677">Only applies to `IndividualB2C` authentication.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="46126-678">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="46126-678">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="46126-679">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="46126-679">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="46126-680">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="46126-680">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="46126-681">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46126-681">SDK version</span></span> | <span data-ttu-id="46126-682">默认值</span><span class="sxs-lookup"><span data-stu-id="46126-682">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="46126-683">5.0</span><span class="sxs-lookup"><span data-stu-id="46126-683">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="46126-684">3.1</span><span class="sxs-lookup"><span data-stu-id="46126-684">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="46126-685">3.0</span><span class="sxs-lookup"><span data-stu-id="46126-685">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="46126-686">2.1</span><span class="sxs-lookup"><span data-stu-id="46126-686">2.1</span></span>         | `netcoreapp2.1` |

- **`--no-restore`**

  <span data-ttu-id="46126-687">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="46126-687">Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="46126-688">\*\*_</span><span class="sxs-lookup"><span data-stu-id="46126-688">\*\*_</span></span>

### <a name="globaljson"></a><span data-ttu-id="46126-689">globaljson</span><span class="sxs-lookup"><span data-stu-id="46126-689">globaljson</span></span>

- <span data-ttu-id="46126-690">_ *`--sdk-version <VERSION_NUMBER>`*\*</span><span class="sxs-lookup"><span data-stu-id="46126-690">_ *`--sdk-version <VERSION_NUMBER>`*\*</span></span>

  <span data-ttu-id="46126-691">指定要在 global.json 文件中使用的 .NET SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="46126-691">Specifies the version of the .NET SDK to use in the *global.json* file.</span></span>

***

## <a name="examples"></a><span data-ttu-id="46126-692">示例</span><span class="sxs-lookup"><span data-stu-id="46126-692">Examples</span></span>

- <span data-ttu-id="46126-693">通过指定模板名称，创建 C# 控制台应用程序项目：</span><span class="sxs-lookup"><span data-stu-id="46126-693">Create a C# console application project by specifying the template name:</span></span>

  ```dotnetcli
  dotnet new "Console Application"
  ```

- <span data-ttu-id="46126-694">在当前目录中创建 F# 控制台应用程序项目：</span><span class="sxs-lookup"><span data-stu-id="46126-694">Create an F# console application project in the current directory:</span></span>

  ```dotnetcli
  dotnet new console -lang "F#"
  ```

- <span data-ttu-id="46126-695">在指定的目录中创建 .NET Standard 类库项目：</span><span class="sxs-lookup"><span data-stu-id="46126-695">Create a .NET Standard class library project in the specified directory:</span></span>

  ```dotnetcli
  dotnet new classlib -lang VB -o MyLibrary
  ```

- <span data-ttu-id="46126-696">在当前目录中新建没有设置身份验证的 ASP.NET Core C# MVC 项目：</span><span class="sxs-lookup"><span data-stu-id="46126-696">Create a new ASP.NET Core C# MVC project in the current directory with no authentication:</span></span>

  ```dotnetcli
  dotnet new mvc -au None
  ```

- <span data-ttu-id="46126-697">创建新的 xUnit 项目：</span><span class="sxs-lookup"><span data-stu-id="46126-697">Create a new xUnit project:</span></span>

  ```dotnetcli
  dotnet new xunit
  ```

- <span data-ttu-id="46126-698">列出可用于单页应用程序 (SPA) 模板的所有模板：</span><span class="sxs-lookup"><span data-stu-id="46126-698">List all templates available for Single Page Application (SPA) templates:</span></span>

  ```dotnetcli
  dotnet new spa -l
  ```

- <span data-ttu-id="46126-699">列出与“we”子字符串匹配的所有模板。</span><span class="sxs-lookup"><span data-stu-id="46126-699">List all templates matching the *we* substring.</span></span> <span data-ttu-id="46126-700">找不到完全匹配，因此子字符串匹配针对短名称和名称列运行。</span><span class="sxs-lookup"><span data-stu-id="46126-700">No exact match is found, so substring matching runs against both the short name and name columns.</span></span>

  ```dotnetcli
  dotnet new we -l
  ```

- <span data-ttu-id="46126-701">尝试调用与 ng 匹配的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-701">Attempt to invoke the template matching *ng*.</span></span> <span data-ttu-id="46126-702">如果无法确定单个匹配项，请列出部分匹配项的模板。</span><span class="sxs-lookup"><span data-stu-id="46126-702">If a single match can't be determined, list the templates that are partial matches.</span></span>

  ```dotnetcli
  dotnet new ng
  ```

- <span data-ttu-id="46126-703">安装 ASP.NET Core 的 SPA 模板 2.0 版：</span><span class="sxs-lookup"><span data-stu-id="46126-703">Install version 2.0 of the SPA templates for ASP.NET Core:</span></span>

  ```dotnetcli
  dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0
  ```

- <span data-ttu-id="46126-704">列出已安装的模板及其详细信息，包括如何卸载它们：</span><span class="sxs-lookup"><span data-stu-id="46126-704">List the installed templates and details about them, including how to uninstall them:</span></span>

  ```dotnetcli
  dotnet new -u
  ```

- <span data-ttu-id="46126-705">在当前目录中创建 global.json，将 SDK 版本设置为 3.1.101：</span><span class="sxs-lookup"><span data-stu-id="46126-705">Create a *global.json* in the current directory setting the SDK version to 3.1.101:</span></span>

  ```dotnetcli
  dotnet new globaljson --sdk-version 3.1.101
  ```

## <a name="see-also"></a><span data-ttu-id="46126-706">请参阅</span><span class="sxs-lookup"><span data-stu-id="46126-706">See also</span></span>

- [<span data-ttu-id="46126-707">dotnet new 自定义模板</span><span class="sxs-lookup"><span data-stu-id="46126-707">Custom templates for dotnet new</span></span>](custom-templates.md)
- [<span data-ttu-id="46126-708">创建 dotnet new 自定义模板</span><span class="sxs-lookup"><span data-stu-id="46126-708">Create a custom template for dotnet new</span></span>](../tutorials/cli-templates-create-item-template.md)
- [<span data-ttu-id="46126-709">dotnet/dotnet-template-samples GitHub 存储库</span><span class="sxs-lookup"><span data-stu-id="46126-709">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)
- [<span data-ttu-id="46126-710">dotnet new 可用模板</span><span class="sxs-lookup"><span data-stu-id="46126-710">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
