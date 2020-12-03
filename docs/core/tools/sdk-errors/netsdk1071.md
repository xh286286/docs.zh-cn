---
title: NETSDK1071：“{0}”的 PackageReference 指定了版本 `{1}`。
description: 如何解决对某版本的框架包含的元包的 PackageReference 问题。
author: Forgind
ms.topic: error-reference
ms.date: 10/09/2020
f1_keywords:
- NETSDK1071
ms.openlocfilehash: 1381fc63941ec04efb31035d13913620a195c236
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713075"
---
# <a name="netsdk1071-explicitly-versioned-packagereference-to-a-metapackage-that-would-be-included-with-the-framework"></a><span data-ttu-id="73e92-103">NETSDK1071：对框架中将包含的元包的显式版本化 PackageReference。</span><span class="sxs-lookup"><span data-stu-id="73e92-103">NETSDK1071: Explicitly versioned PackageReference to a metapackage that would be included with the framework.</span></span>

<span data-ttu-id="73e92-104">**本文适用于：** ✔️ .NET 5.0.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="73e92-104">**This article applies to:** ✔️ .NET 5.0.100 SDK and later versions</span></span>

<span data-ttu-id="73e92-105">当 .NET SDK 发出警告 NETSDK1071 时，它表明将来在 PackageReference 中指定的元包版本与通过 TargetFramework 属性隐式引用的元包版本之间可能会存在版本冲突：</span><span class="sxs-lookup"><span data-stu-id="73e92-105">When the .NET SDK issues warning NETSDK1071, it suggests there may be a version conflict in the future between the version of a metapackage specified in a PackageReference and the version of that metapackage as implicitly referenced via a TargetFramework property:</span></span>

```xml
<PropertyGroup>
  <TargetFramework>netcoreapp3.1</TargetFramework>
</PropertyGroup>
```

<span data-ttu-id="73e92-106">由于 TargetFramework 会自动引入元包的版本，因此如果版本不同，它们将发生冲突。</span><span class="sxs-lookup"><span data-stu-id="73e92-106">Since the TargetFramework automatically brings in a version of the metapackage, the versions will conflict should they ever differ.</span></span>

<span data-ttu-id="73e92-107">若要解决此问题：</span><span class="sxs-lookup"><span data-stu-id="73e92-107">To resolve this:</span></span>

1. <span data-ttu-id="73e92-108">在面向 .NET Core 或 .NET Standard 时，请考虑避免显式引用项目文件中的 `Microsoft.NETCore.App` 或 `NETStandard.Library`。</span><span class="sxs-lookup"><span data-stu-id="73e92-108">Consider, when targeting .NET Core or .NET Standard, avoiding explicit references to `Microsoft.NETCore.App` or `NETStandard.Library` in your project file.</span></span>
2. <span data-ttu-id="73e92-109">面向 .NET Core 时，如果需要特定版本的运行时，请使用 `<RuntimeFrameworkVersion>` 属性，而不是直接引用元包。</span><span class="sxs-lookup"><span data-stu-id="73e92-109">If you need a specific version of the runtime when targeting .NET Core, use the `<RuntimeFrameworkVersion>`property instead of referencing the metapackage directly.</span></span> <span data-ttu-id="73e92-110">例如，如果使用的是 [self-contained deployments](../../deploying/index.md#publish-self-contained) 并需要 1.0.0 LTS 运行时的特定修补程序，则可能会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="73e92-110">As an example, this could happen if you're using [self-contained deployments](../../deploying/index.md#publish-self-contained) and need a specific patch of the 1.0.0 LTS runtime.</span></span>
3. <span data-ttu-id="73e92-111">面向 .NET Standard 时，如果需要特定版本的 `NetStandard.Library`，可以使用 `<NetStandardImplicitPackageVersion>` 属性并将其设置为所需版本。</span><span class="sxs-lookup"><span data-stu-id="73e92-111">If you need a specific version of `NetStandard.Library` when targeting .NET Standard, you can use the `<NetStandardImplicitPackageVersion>` property and set it to the version you need.</span></span>
4. <span data-ttu-id="73e92-112">请勿在 .NET Framework 项目中显式添加或更新对 `Microsoft.NETCore.App` 或 `NETSTandard.Library` 的引用。</span><span class="sxs-lookup"><span data-stu-id="73e92-112">Don't explicitly add or update references to either `Microsoft.NETCore.App` or `NETSTandard.Library` in .NET Framework projects.</span></span> <span data-ttu-id="73e92-113">使用基于 .NET Standard 的 NuGet 包时，NuGet 会自动安装所需的任何版本的 `NETStandard.Library`。</span><span class="sxs-lookup"><span data-stu-id="73e92-113">NuGet automatically installs any version of `NETStandard.Library` you need when using a .NET Standard-based NuGet package.</span></span>
5. <span data-ttu-id="73e92-114">使用 .NET Core 2.1+ 时，请勿指定 `Microsoft.AspNetCore.App` 或 `Microsoft.AspNetCore.All` 版本，因为 .NET Core SDK 会自动选择相应的版本。</span><span class="sxs-lookup"><span data-stu-id="73e92-114">Do not specify a version for `Microsoft.AspNetCore.App` or `Microsoft.AspNetCore.All` when using .NET Core 2.1+, as the .NET Core SDK automatically selects the appropriate version.</span></span> <span data-ttu-id="73e92-115">（注意：如果该项目还使用 `Microsoft.NET.Sdk.Web`，则此操作仅适用于面向 .NET Core 2.1 的情况。</span><span class="sxs-lookup"><span data-stu-id="73e92-115">(Note: This only works when targeting .NET Core 2.1 if the project also uses `Microsoft.NET.Sdk.Web`.</span></span> <span data-ttu-id="73e92-116">.NET Core 2.2 SDK 中解决了此问题。）</span><span class="sxs-lookup"><span data-stu-id="73e92-116">This problem was resolved in the .NET Core 2.2 SDK.)</span></span>
6. <span data-ttu-id="73e92-117">如果希望警告消失，还可以禁用它：</span><span class="sxs-lookup"><span data-stu-id="73e92-117">If you want the warning to go away, you can also disable it:</span></span>

   ```xml
   <PackageReference Include="Microsoft.NetCore.App" Version="2.2.8" >
     <AllowExplicitVersion>true</AllowExplicitVersion>
   </PackageReference>
   ```
