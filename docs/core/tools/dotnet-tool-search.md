---
title: dotnet tool search 命令
description: Dotnet tool search 命令搜索已发布到 NuGet.org 的 .NET 工具。
ms.date: 11/11/2020
ms.openlocfilehash: e0289e651ec4a439c791c8c948bef2d85d9c3794
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "94634137"
---
# <a name="dotnet-tool-search"></a><span data-ttu-id="d5ea1-103">dotnet tool search</span><span class="sxs-lookup"><span data-stu-id="d5ea1-103">dotnet tool search</span></span>

<span data-ttu-id="d5ea1-104">**本文适用于：** ✔️ .NET 5.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="d5ea1-104">**This article applies to:** ✔️ .NET 5.0 SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="d5ea1-105">名称</span><span class="sxs-lookup"><span data-stu-id="d5ea1-105">Name</span></span>

<span data-ttu-id="d5ea1-106">`dotnet tool search` - 搜索已发布到 NuGet 的 [.NET 工具](global-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-106">`dotnet tool search` - Searches all [.NET tools](global-tools.md) that are published to NuGet.</span></span>

## <a name="synopsis"></a><span data-ttu-id="d5ea1-107">摘要</span><span class="sxs-lookup"><span data-stu-id="d5ea1-107">Synopsis</span></span>

```dotnetcli
dotnet tool search [--detail]  [--prerelease]
    [--skip <NUMBER>] [--take <NUMBER>] <SEARCH TERM>

dotnet tool search -h|--help
```

## <a name="description"></a><span data-ttu-id="d5ea1-108">描述</span><span class="sxs-lookup"><span data-stu-id="d5ea1-108">Description</span></span>

<span data-ttu-id="d5ea1-109">`dotnet tool search` 命令提供了一种方法，使你可以在 NuGet 中搜索可用作 .NET 全局、工具路径或本地工具的工具。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-109">The `dotnet tool search` command provides a way for you to search NuGet for tools that can be used as .NET global, tool-path, or local tools.</span></span> <span data-ttu-id="d5ea1-110">该命令搜索工具名称和元数据（如标题、说明和标记）。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-110">The command searches the tool names and metadata such as titles, descriptions, and tags.</span></span>

<span data-ttu-id="d5ea1-111">该命令使用 [NuGet 搜索 API](/nuget/api/search-query-service-resource#search-for-packages)。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-111">The command uses the [NuGet Search API](/nuget/api/search-query-service-resource#search-for-packages).</span></span> <span data-ttu-id="d5ea1-112">它筛选 `packageType=dotnettool` 以仅选择 .NET 工具包。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-112">It filters on `packageType=dotnettool` to select only .NET tool packages.</span></span>

## <a name="options"></a><span data-ttu-id="d5ea1-113">选项</span><span class="sxs-lookup"><span data-stu-id="d5ea1-113">Options</span></span>

- **`--detail`**

  <span data-ttu-id="d5ea1-114">显示查询的详细结果。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-114">Shows detailed results from the query.</span></span>

- **`--prerelease`**

  <span data-ttu-id="d5ea1-115">包含预发行包。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-115">Includes pre-release packages.</span></span>

- **`--skip <NUMBER>`**

  <span data-ttu-id="d5ea1-116">指定要跳过的查询结果数。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-116">Specifies the number of query results to skip.</span></span> <span data-ttu-id="d5ea1-117">用于分页。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-117">Used for pagination.</span></span>

- **`--take <NUMBER>`**

  <span data-ttu-id="d5ea1-118">指定要显示的查询结果数。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-118">Specifies the number of query results to show.</span></span> <span data-ttu-id="d5ea1-119">用于分页。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-119">Used for pagination.</span></span>

- **`-h|--help`**

  <span data-ttu-id="d5ea1-120">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-120">Shows command-line help.</span></span>

## <a name="examples"></a><span data-ttu-id="d5ea1-121">示例</span><span class="sxs-lookup"><span data-stu-id="d5ea1-121">Examples</span></span>

- <span data-ttu-id="d5ea1-122">在 NuGet.org 中搜索其包名称或描述中具有“格式”的 .NET 工具：</span><span class="sxs-lookup"><span data-stu-id="d5ea1-122">Search NuGet.org for .NET tools that have "format" in their package name or description:</span></span>

  ```dotnetcli
  dotnet tool search format
  ```

  <span data-ttu-id="d5ea1-123">输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="d5ea1-123">The output looks like the following example:</span></span>

  ```output
  Package ID                              Latest Version      Authors                                                                     Downloads      Verified
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------
  dotnet-format                           4.1.131201          Microsoft                                                                   496746
  bsoa.generator                          1.0.0               Microsoft                                                                   533
  ```

- <span data-ttu-id="d5ea1-124">在 NuGet.org 中搜索其包名称或元数据中具有“格式”的 .NET 工具，仅显示第一条结果并显示详细视图。</span><span class="sxs-lookup"><span data-stu-id="d5ea1-124">Search NuGet.org for .NET tools that have "format" in their package name or metadata, show only the first result, and show a detailed view.</span></span>

  ```dotnetcli
  dotnet tool search format --take 1 --detail
  ```

  <span data-ttu-id="d5ea1-125">输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="d5ea1-125">The output looks like the following example:</span></span>

  ```output
  ----------------
  dotnet-format
  Latest Version: 4.1.131201
  Authors: Microsoft
  Tags:
  Downloads: 496746
  Verified: False
  Description: Command line tool for formatting C# and Visual Basic code files based on .editorconfig settings.
  Versions:
          3.0.2 Downloads: 1973
          3.0.4 Downloads: 9064
          3.1.37601 Downloads: 114730
          3.2.107702 Downloads: 13423
          3.3.111304 Downloads: 131195
          4.0.130203 Downloads: 78610
          4.1.131201 Downloads: 145927
  ```

## <a name="see-also"></a><span data-ttu-id="d5ea1-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5ea1-126">See also</span></span>

- [<span data-ttu-id="d5ea1-127">.NET 工具</span><span class="sxs-lookup"><span data-stu-id="d5ea1-127">.NET tools</span></span>](global-tools.md)
- [<span data-ttu-id="d5ea1-128">教程：使用 .NET CLI 安装和使用 .NET 全局工具</span><span class="sxs-lookup"><span data-stu-id="d5ea1-128">Tutorial: Install and use a .NET global tool using the .NET CLI</span></span>](global-tools-how-to-use.md)
- [<span data-ttu-id="d5ea1-129">教程：使用 .NET CLI 安装和使用 .NET 本地工具</span><span class="sxs-lookup"><span data-stu-id="d5ea1-129">Tutorial: Install and use a .NET local tool using the .NET CLI</span></span>](local-tools-how-to-use.md)
