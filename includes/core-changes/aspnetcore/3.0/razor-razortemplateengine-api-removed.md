---
ms.openlocfilehash: 35dd8db243b03e1dfd6311195ec97673cf114877
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96032301"
---
### <a name="razor-razortemplateengine-api-removed"></a><span data-ttu-id="b5f74-101">Razor：已删除 RazorTemplateEngine API</span><span class="sxs-lookup"><span data-stu-id="b5f74-101">Razor: RazorTemplateEngine API removed</span></span>

<span data-ttu-id="b5f74-102">已删除 [RazorTemplateEngine](/dotnet/api/microsoft.aspnetcore.razor.language.razortemplateengine?view=aspnetcore-2.2) API，该内容已替换为 <xref:Microsoft.AspNetCore.Razor.Language.RazorProjectEngine>。</span><span class="sxs-lookup"><span data-stu-id="b5f74-102">The [RazorTemplateEngine](/dotnet/api/microsoft.aspnetcore.razor.language.razortemplateengine?view=aspnetcore-2.2) API was removed and replaced with <xref:Microsoft.AspNetCore.Razor.Language.RazorProjectEngine>.</span></span>

<span data-ttu-id="b5f74-103">有关讨论，请参阅 GitHub 问题 [dotnet/aspnetcore#25215](https://github.com/dotnet/aspnetcore/issues/25215)。</span><span class="sxs-lookup"><span data-stu-id="b5f74-103">For discussion, see GitHub issue [dotnet/aspnetcore#25215](https://github.com/dotnet/aspnetcore/issues/25215).</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="b5f74-104">引入的版本</span><span class="sxs-lookup"><span data-stu-id="b5f74-104">Version introduced</span></span>

<span data-ttu-id="b5f74-105">3.0</span><span class="sxs-lookup"><span data-stu-id="b5f74-105">3.0</span></span>

#### <a name="old-behavior"></a><span data-ttu-id="b5f74-106">旧行为</span><span class="sxs-lookup"><span data-stu-id="b5f74-106">Old behavior</span></span>

<span data-ttu-id="b5f74-107">可创建模板引擎并将其用于分析和生成 Razor 文件的代码。</span><span class="sxs-lookup"><span data-stu-id="b5f74-107">A template engine can be created and used to parse and generate code for Razor files.</span></span>

#### <a name="new-behavior"></a><span data-ttu-id="b5f74-108">新行为</span><span class="sxs-lookup"><span data-stu-id="b5f74-108">New behavior</span></span>

<span data-ttu-id="b5f74-109">可创建 `RazorProjectEngine`，使其提供与 `RazorTemplateEngine` 相同类型的信息，以分析和生成 Razor 文件的代码。</span><span class="sxs-lookup"><span data-stu-id="b5f74-109">`RazorProjectEngine` can be created and provided the same type of information as `RazorTemplateEngine` to parse and generate code for Razor files.</span></span> <span data-ttu-id="b5f74-110">`RazorProjectEngine` 也可提供额外的配置级别。</span><span class="sxs-lookup"><span data-stu-id="b5f74-110">`RazorProjectEngine` also provides extra levels of configuration.</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="b5f74-111">更改原因</span><span class="sxs-lookup"><span data-stu-id="b5f74-111">Reason for change</span></span>

<span data-ttu-id="b5f74-112">`RazorTemplateEngine` 与现有实现过于紧密耦合。</span><span class="sxs-lookup"><span data-stu-id="b5f74-112">`RazorTemplateEngine` was too tightly coupled to the existing implementations.</span></span> <span data-ttu-id="b5f74-113">在尝试正确配置 Razor 分析/生成管道时，这种紧密耦合会导致更多问题。</span><span class="sxs-lookup"><span data-stu-id="b5f74-113">This tight coupling led to more questions when trying to properly configure a Razor parsing/generation pipeline.</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="b5f74-114">建议操作</span><span class="sxs-lookup"><span data-stu-id="b5f74-114">Recommended action</span></span>

<span data-ttu-id="b5f74-115">请使用 `RazorProjectEngine`，而不是 `RazorTemplateEngine`。</span><span class="sxs-lookup"><span data-stu-id="b5f74-115">Use `RazorProjectEngine` instead of `RazorTemplateEngine`.</span></span> <span data-ttu-id="b5f74-116">请考虑以下示例。</span><span class="sxs-lookup"><span data-stu-id="b5f74-116">Consider the following examples.</span></span>

##### <a name="create-and-configure-the-razorprojectengine"></a><span data-ttu-id="b5f74-117">创建和配置 RazorProjectEngine</span><span class="sxs-lookup"><span data-stu-id="b5f74-117">Create and configure the RazorProjectEngine</span></span>

```csharp
RazorProjectEngine projectEngine =
    RazorProjectEngine.Create(RazorConfiguration.Default,
        RazorProjectFileSystem.Create(@"C:\source\repos\ConsoleApp4\ConsoleApp4"),
        builder =>
        {
            builder.ConfigureClass((document, classNode) =>
            {
                classNode.ClassName = "MyClassName";

                // Can also configure other aspects of the class here.
            });

            // More configuration can go here
        });
```

##### <a name="generate-code-for-a-razor-file"></a><span data-ttu-id="b5f74-118">生成 Razor 文件的代码</span><span class="sxs-lookup"><span data-stu-id="b5f74-118">Generate code for a Razor file</span></span>

```csharp
RazorProjectItem item = projectEngine.FileSystem.GetItem(
    @"C:\source\repos\ConsoleApp4\ConsoleApp4\Example.cshtml",
    FileKinds.Legacy);
RazorCodeDocument output = projectEngine.Process(item);

// Things available
RazorSyntaxTree syntaxTree = output.GetSyntaxTree();
DocumentIntermediateNode intermediateDocument =
    output.GetDocumentIntermediateNode();
RazorCSharpDocument csharpDocument = output.GetCSharpDocument();
```

#### <a name="category"></a><span data-ttu-id="b5f74-119">类别</span><span class="sxs-lookup"><span data-stu-id="b5f74-119">Category</span></span>

<span data-ttu-id="b5f74-120">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="b5f74-120">ASP.NET Core</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="b5f74-121">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="b5f74-121">Affected APIs</span></span>

- [<span data-ttu-id="b5f74-122">RazorTemplateEngine</span><span class="sxs-lookup"><span data-stu-id="b5f74-122">RazorTemplateEngine</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.razortemplateengine?view=aspnetcore-2.2)
- [<span data-ttu-id="b5f74-123">RazorTemplateEngineOptions</span><span class="sxs-lookup"><span data-stu-id="b5f74-123">RazorTemplateEngineOptions</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.razortemplateengineoptions?view=aspnetcore-2.2)

<!--

#### Affected APIs

- `T:Microsoft.AspNetCore.Razor.Language.RazorTemplateEngine`
- `T:Microsoft.AspNetCore.Razor.Language.RazorTemplateEngineOptions`

-->
