---
ms.openlocfilehash: f6e4c3d5c5fd020562e48515554136e0f8b6785c
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96032266"
---
### <a name="data-protection-dataprotectionblobs-uses-new-azure-storage-apis"></a><span data-ttu-id="58f22-101">数据保护：DataProtection.Blobs 使用新的 Azure 存储 API</span><span class="sxs-lookup"><span data-stu-id="58f22-101">Data Protection: DataProtection.Blobs uses new Azure Storage APIs</span></span>

<span data-ttu-id="58f22-102">`Azure.Extensions.AspNetCore.DataProtection.Blobs` 取决于 [Azure 存储库](https://github.com/Azure/azure-storage-net)。</span><span class="sxs-lookup"><span data-stu-id="58f22-102">`Azure.Extensions.AspNetCore.DataProtection.Blobs` depends on the [Azure Storage libraries](https://github.com/Azure/azure-storage-net).</span></span> <span data-ttu-id="58f22-103">这些库已重命名其程序集、包和命名空间。</span><span class="sxs-lookup"><span data-stu-id="58f22-103">These libraries renamed their assemblies, packages, and namespaces.</span></span> <span data-ttu-id="58f22-104">从 ASP.NET Core 3.0 开始，`Azure.Extensions.AspNetCore.DataProtection.Blobs` 使用新的带有 `Azure.Storage.` 前缀的 API 和包。</span><span class="sxs-lookup"><span data-stu-id="58f22-104">Starting in ASP.NET Core 3.0, `Azure.Extensions.AspNetCore.DataProtection.Blobs` uses the new `Azure.Storage.`-prefixed APIs and packages.</span></span>

<span data-ttu-id="58f22-105">有关 Azure 存储 API 的问题，请使用 <https://github.com/Azure/azure-storage-net>。</span><span class="sxs-lookup"><span data-stu-id="58f22-105">For questions about the Azure Storage APIs, use <https://github.com/Azure/azure-storage-net>.</span></span> <span data-ttu-id="58f22-106">有关此问题的讨论，请参阅 [dotnet/aspnetcore#19570](https://github.com/dotnet/aspnetcore/issues/19570)。</span><span class="sxs-lookup"><span data-stu-id="58f22-106">For discussion on this issue, see [dotnet/aspnetcore#19570](https://github.com/dotnet/aspnetcore/issues/19570).</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="58f22-107">引入的版本</span><span class="sxs-lookup"><span data-stu-id="58f22-107">Version introduced</span></span>

<span data-ttu-id="58f22-108">3.0</span><span class="sxs-lookup"><span data-stu-id="58f22-108">3.0</span></span>

#### <a name="old-behavior"></a><span data-ttu-id="58f22-109">旧行为</span><span class="sxs-lookup"><span data-stu-id="58f22-109">Old behavior</span></span>

<span data-ttu-id="58f22-110">该包引用了 `WindowsAzure.Storage` NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="58f22-110">The package referenced the `WindowsAzure.Storage` NuGet package.</span></span>
<span data-ttu-id="58f22-111">该包引用 `Microsoft.Azure.Storage.Blob` NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="58f22-111">The package references the `Microsoft.Azure.Storage.Blob` NuGet package.</span></span>

#### <a name="new-behavior"></a><span data-ttu-id="58f22-112">新行为</span><span class="sxs-lookup"><span data-stu-id="58f22-112">New behavior</span></span>

<span data-ttu-id="58f22-113">该包引用 `Azure.Storage.Blob` NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="58f22-113">The package references the `Azure.Storage.Blob` NuGet package.</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="58f22-114">更改原因</span><span class="sxs-lookup"><span data-stu-id="58f22-114">Reason for change</span></span>

<span data-ttu-id="58f22-115">此更改允许 `Azure.Extensions.AspNetCore.DataProtection.Blobs` 迁移到建议的 Azure 存储包。</span><span class="sxs-lookup"><span data-stu-id="58f22-115">This change allows `Azure.Extensions.AspNetCore.DataProtection.Blobs` to migrate to the recommended Azure Storage packages.</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="58f22-116">建议操作</span><span class="sxs-lookup"><span data-stu-id="58f22-116">Recommended action</span></span>

<span data-ttu-id="58f22-117">如果仍需要将较旧的 Azure 存储 API 与 ASP.NET Core 3.0 一起使用，请将直接依赖项添加到包 [WindowsAzure.Storage](https://www.nuget.org/packages/WindowsAzure.Storage/) 或 [Microsoft.Azure.Storage](https://www.nuget.org/packages/Microsoft.Azure.Storage.Blob/)。</span><span class="sxs-lookup"><span data-stu-id="58f22-117">If you still need to use the older Azure Storage APIs with ASP.NET Core 3.0, add a direct dependency to the package [WindowsAzure.Storage](https://www.nuget.org/packages/WindowsAzure.Storage/) or [Microsoft.Azure.Storage](https://www.nuget.org/packages/Microsoft.Azure.Storage.Blob/).</span></span> <span data-ttu-id="58f22-118">此包可以与新的 `Azure.Storage` API 一起安装。</span><span class="sxs-lookup"><span data-stu-id="58f22-118">This package can be installed alongside the new `Azure.Storage` APIs.</span></span>

<span data-ttu-id="58f22-119">在许多情况下，升级仅涉及更改 `using` 语句以使用新的命名空间：</span><span class="sxs-lookup"><span data-stu-id="58f22-119">In many cases, the upgrade only involves changing the `using` statements to use the new namespaces:</span></span>

```diff
- using Microsoft.WindowsAzure.Storage;
- using Microsoft.WindowsAzure.Storage.Blob;
- using Microsoft.Azure.Storage;
- using Microsoft.Azure.Storage.Blob;
+ using Azure.Storage;
+ using Azure.Storage.Blobs;
```

#### <a name="category"></a><span data-ttu-id="58f22-120">类别</span><span class="sxs-lookup"><span data-stu-id="58f22-120">Category</span></span>

<span data-ttu-id="58f22-121">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="58f22-121">ASP.NET Core</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="58f22-122">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="58f22-122">Affected APIs</span></span>

<span data-ttu-id="58f22-123">无</span><span class="sxs-lookup"><span data-stu-id="58f22-123">None</span></span>

<!-- 

#### Affected APIs

Not detectable via API analysis

-->
