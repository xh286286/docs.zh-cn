---
title: 如何对 .NET 运行时和 SDK 进行版本控制
description: 本文介绍如何对 .NET SDK 和运行时进行版本控制（与语义版本控制类似）。
ms.date: 12/07/2020
ms.openlocfilehash: 2fe0b162b52f1e4500ec87f7d5d92054cd569552
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009301"
---
# <a name="overview-of-how-net-is-versioned"></a><span data-ttu-id="43680-103">.NET 的版本控制方式概述</span><span class="sxs-lookup"><span data-stu-id="43680-103">Overview of how .NET is versioned</span></span>

<span data-ttu-id="43680-104">[.NET 运行时和 .NET SDK](../introduction.md#sdk-and-runtimes) 添加新功能的频率不同。</span><span class="sxs-lookup"><span data-stu-id="43680-104">The [.NET Runtime and the .NET SDK](../introduction.md#sdk-and-runtimes) add new features at different frequencies.</span></span> <span data-ttu-id="43680-105">通常来说，SDK 的更新频率比运行时高。</span><span class="sxs-lookup"><span data-stu-id="43680-105">In general, the SDK is updated more frequently than the Runtime.</span></span> <span data-ttu-id="43680-106">本文介绍运行时和 SDK 版本号。</span><span class="sxs-lookup"><span data-stu-id="43680-106">This article explains the runtime and the SDK version numbers.</span></span>

## <a name="versioning-details"></a><span data-ttu-id="43680-107">版本控制详细信息</span><span class="sxs-lookup"><span data-stu-id="43680-107">Versioning details</span></span>

<span data-ttu-id="43680-108">.NET 运行时具有用于版本控制的主要/次要/补丁方法，且该方法遵循[语义版本控制](#semantic-versioning)。</span><span class="sxs-lookup"><span data-stu-id="43680-108">The .NET Runtime has a major/minor/patch approach to versioning that follows [semantic versioning](#semantic-versioning).</span></span>

<span data-ttu-id="43680-109">.NET SDK 不遵循语义版本控制。</span><span class="sxs-lookup"><span data-stu-id="43680-109">The .NET SDK doesn't follow semantic versioning.</span></span> <span data-ttu-id="43680-110">.NET SDK 发布速度更快，其版本必须显示相应的运行时和 SDK 自己的次要版本及补丁版本。</span><span class="sxs-lookup"><span data-stu-id="43680-110">The .NET SDK releases faster and its version numbers must communicate both the aligned runtime and the SDK's own minor and patch releases.</span></span>

<span data-ttu-id="43680-111">.NET SDK 版本号的前两个位置被锁定，其中显示与之一起发布的 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="43680-111">The first two positions of the .NET SDK version number are locked to the .NET Runtime it released with.</span></span> <span data-ttu-id="43680-112">每个版本的 SDK 都可以为此版本或任何更低版本的运行时创建应用程序。</span><span class="sxs-lookup"><span data-stu-id="43680-112">Each version of the SDK can create applications for this runtime or any lower version.</span></span>

<span data-ttu-id="43680-113">SDK 版本号的第三个位置同时传达次要编号和修补程序编号。</span><span class="sxs-lookup"><span data-stu-id="43680-113">The third position of the SDK version number communicates both the minor and patch number.</span></span> <span data-ttu-id="43680-114">次要版本乘以 100。</span><span class="sxs-lookup"><span data-stu-id="43680-114">The minor version is multiplied by 100.</span></span> <span data-ttu-id="43680-115">次要版本 1，修补程序版本 2 将表示为 102。</span><span class="sxs-lookup"><span data-stu-id="43680-115">Minor version 1, patch version 2 would be represented as 102.</span></span> <span data-ttu-id="43680-116">最后两位数代表修补程序号。</span><span class="sxs-lookup"><span data-stu-id="43680-116">The final two digits represent the patch number.</span></span> <span data-ttu-id="43680-117">例如，下面是运行时和 SDK 版本号可能出现的序列：</span><span class="sxs-lookup"><span data-stu-id="43680-117">For example, here's a possible sequence of runtime and SDK version numbers:</span></span>

| <span data-ttu-id="43680-118">更改</span><span class="sxs-lookup"><span data-stu-id="43680-118">Change</span></span>                | <span data-ttu-id="43680-119">.NET 运行时</span><span class="sxs-lookup"><span data-stu-id="43680-119">.NET Runtime</span></span>      | <span data-ttu-id="43680-120">.NET SDK (\*)</span><span class="sxs-lookup"><span data-stu-id="43680-120">.NET SDK (\*)</span></span>     |
|-----------------------|-------------------|-------------------|
| <span data-ttu-id="43680-121">初始版本</span><span class="sxs-lookup"><span data-stu-id="43680-121">Initial release</span></span>       | <span data-ttu-id="43680-122">2.2.0</span><span class="sxs-lookup"><span data-stu-id="43680-122">2.2.0</span></span>             | <span data-ttu-id="43680-123">2.2.100</span><span class="sxs-lookup"><span data-stu-id="43680-123">2.2.100</span></span>           |
| <span data-ttu-id="43680-124">SDK 修补程序</span><span class="sxs-lookup"><span data-stu-id="43680-124">SDK Patch</span></span>             | <span data-ttu-id="43680-125">2.2.0</span><span class="sxs-lookup"><span data-stu-id="43680-125">2.2.0</span></span>             | <span data-ttu-id="43680-126">2.2.101</span><span class="sxs-lookup"><span data-stu-id="43680-126">2.2.101</span></span>           |
| <span data-ttu-id="43680-127">运行时和 SDK 修补程序</span><span class="sxs-lookup"><span data-stu-id="43680-127">Runtime and SDK Patch</span></span> | <span data-ttu-id="43680-128">2.2.1</span><span class="sxs-lookup"><span data-stu-id="43680-128">2.2.1</span></span>             | <span data-ttu-id="43680-129">2.2.102</span><span class="sxs-lookup"><span data-stu-id="43680-129">2.2.102</span></span>           |
| <span data-ttu-id="43680-130">SDK 功能更改</span><span class="sxs-lookup"><span data-stu-id="43680-130">SDK Feature change</span></span>    | <span data-ttu-id="43680-131">2.2.1</span><span class="sxs-lookup"><span data-stu-id="43680-131">2.2.1</span></span>             | <span data-ttu-id="43680-132">2.2.200</span><span class="sxs-lookup"><span data-stu-id="43680-132">2.2.200</span></span>           |

<span data-ttu-id="43680-133">注意：</span><span class="sxs-lookup"><span data-stu-id="43680-133">NOTES:</span></span>

- <span data-ttu-id="43680-134">如果在运行时功能更新之前，SDK 有 10 个功能更新，则版本号将滚动到 1000 系列，2.2.1000 等编号为 2.2.900 之后的功能版本。</span><span class="sxs-lookup"><span data-stu-id="43680-134">If the SDK has 10 feature updates before a runtime feature update, version numbers roll into the 1000 series with numbers like 2.2.1000 as the feature release following 2.2.900.</span></span> <span data-ttu-id="43680-135">应该不会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="43680-135">This situation isn't expected to occur.</span></span>
- <span data-ttu-id="43680-136">不会出现为发布功能的 99 修补程序版本。</span><span class="sxs-lookup"><span data-stu-id="43680-136">99 patch releases without a feature release won't occur.</span></span> <span data-ttu-id="43680-137">如果某版本接近此数字，则会强制发布功能。</span><span class="sxs-lookup"><span data-stu-id="43680-137">If a release approaches this number, it forces a feature release.</span></span>

<span data-ttu-id="43680-138">可在 [dotnet/设计](https://github.com/dotnet/designs/pull/29) 存储库中查看初始建议的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="43680-138">You can see more details in the initial proposal at the [dotnet/designs](https://github.com/dotnet/designs/pull/29) repository.</span></span>

## <a name="semantic-versioning"></a><span data-ttu-id="43680-139">语义化版本控制</span><span class="sxs-lookup"><span data-stu-id="43680-139">Semantic versioning</span></span>

<span data-ttu-id="43680-140">.NET 运行时大致遵循[语义版本控制 (SemVer)](https://semver.org/)，采用 `MAJOR.MINOR.PATCH` 版本控制，通过版本号的各部分来描述更改程度和类型。</span><span class="sxs-lookup"><span data-stu-id="43680-140">The .NET *Runtime* roughly adheres to [Semantic Versioning (SemVer)](https://semver.org/), adopting the use of `MAJOR.MINOR.PATCH` versioning, using the various parts of the version number to describe the degree and type of change.</span></span>

```
MAJOR.MINOR.PATCH[-PRERELEASE-BUILDNUMBER]
```

<span data-ttu-id="43680-141">可选的 `PRERELEASE` 和 `BUILDNUMBER` 部分永远不会成为受支持版本的一部分，并且将仅存在于夜间版本、来自源目标的本地版本，以及不受支持的预览版本中。</span><span class="sxs-lookup"><span data-stu-id="43680-141">The optional `PRERELEASE` and `BUILDNUMBER` parts are never part of supported releases and only exist on nightly builds, local builds from source targets, and unsupported preview releases.</span></span>

### <a name="understand-runtime-version-number-changes"></a><span data-ttu-id="43680-142">了解运行时版本号更改</span><span class="sxs-lookup"><span data-stu-id="43680-142">Understand runtime version number changes</span></span>

<span data-ttu-id="43680-143">`MAJOR` 在下列情况时递增：</span><span class="sxs-lookup"><span data-stu-id="43680-143">`MAJOR` is incremented when:</span></span>

- <span data-ttu-id="43680-144">产品或新产品方向发生重大更改。</span><span class="sxs-lookup"><span data-stu-id="43680-144">Significant changes occur to the product, or a new product direction.</span></span>
- <span data-ttu-id="43680-145">发生了中断性变更。</span><span class="sxs-lookup"><span data-stu-id="43680-145">Breaking changes were taken.</span></span> <span data-ttu-id="43680-146">接受中断性变更存在较大障碍。</span><span class="sxs-lookup"><span data-stu-id="43680-146">There's a high bar to accepting breaking changes.</span></span>
- <span data-ttu-id="43680-147">旧版本不再受支持。</span><span class="sxs-lookup"><span data-stu-id="43680-147">An old version is no longer supported.</span></span>
- <span data-ttu-id="43680-148">采用了现有依赖项的较新 `MAJOR` 版本。</span><span class="sxs-lookup"><span data-stu-id="43680-148">A newer `MAJOR` version of an existing dependency is adopted.</span></span>

<span data-ttu-id="43680-149">`MINOR` 在下列情况时递增：</span><span class="sxs-lookup"><span data-stu-id="43680-149">`MINOR` is incremented when:</span></span>

- <span data-ttu-id="43680-150">添加了公共 API 外围应用。</span><span class="sxs-lookup"><span data-stu-id="43680-150">Public API surface area is added.</span></span>
- <span data-ttu-id="43680-151">添加了新行为。</span><span class="sxs-lookup"><span data-stu-id="43680-151">A new behavior is added.</span></span>
- <span data-ttu-id="43680-152">采用了现有依赖项的较新 `MINOR` 版本。</span><span class="sxs-lookup"><span data-stu-id="43680-152">A newer `MINOR` version of an existing dependency is adopted.</span></span>
- <span data-ttu-id="43680-153">引入了新依赖项。</span><span class="sxs-lookup"><span data-stu-id="43680-153">A new dependency is introduced.</span></span>

<span data-ttu-id="43680-154">`PATCH` 在下列情况时递增：</span><span class="sxs-lookup"><span data-stu-id="43680-154">`PATCH` is incremented when:</span></span>

- <span data-ttu-id="43680-155">进行了 Bug 修复。</span><span class="sxs-lookup"><span data-stu-id="43680-155">Bug fixes are made.</span></span>
- <span data-ttu-id="43680-156">添加了对较新平台的支持。</span><span class="sxs-lookup"><span data-stu-id="43680-156">Support for a newer platform is added.</span></span>
- <span data-ttu-id="43680-157">采用了现有依赖项的较新 `PATCH` 版本。</span><span class="sxs-lookup"><span data-stu-id="43680-157">A newer `PATCH` version of an existing dependency is adopted.</span></span>
- <span data-ttu-id="43680-158">任何其他不符合上述情况的更改。</span><span class="sxs-lookup"><span data-stu-id="43680-158">Any other change doesn't fit one of the previous cases.</span></span>

<span data-ttu-id="43680-159">存在多处更改时，单个更改影响的最高级别元素会递增，并将随后的元素重置为零。</span><span class="sxs-lookup"><span data-stu-id="43680-159">When there are multiple changes, the highest element affected by individual changes is incremented, and the following ones are reset to zero.</span></span> <span data-ttu-id="43680-160">例如，当 `MAJOR` 递增时，`MINOR` 和 `PATCH` 将重置为零。</span><span class="sxs-lookup"><span data-stu-id="43680-160">For example, when `MAJOR` is incremented, `MINOR` and `PATCH` are reset to zero.</span></span> <span data-ttu-id="43680-161">当 `MINOR` 递增时，`PATCH` 将重置为零，而 `MAJOR` 保持不变。</span><span class="sxs-lookup"><span data-stu-id="43680-161">When `MINOR` is incremented, `PATCH` is reset to zero while `MAJOR` is left untouched.</span></span>

## <a name="version-numbers-in-file-names"></a><span data-ttu-id="43680-162">文件名中的版本号</span><span class="sxs-lookup"><span data-stu-id="43680-162">Version numbers in file names</span></span>

<span data-ttu-id="43680-163">为 .NET 下载的文件带有版本，例如 `dotnet-sdk-2.1.300-win10-x64.exe`。</span><span class="sxs-lookup"><span data-stu-id="43680-163">The files downloaded for .NET carry the version, for example, `dotnet-sdk-2.1.300-win10-x64.exe`.</span></span>

### <a name="preview-versions"></a><span data-ttu-id="43680-164">预览版</span><span class="sxs-lookup"><span data-stu-id="43680-164">Preview versions</span></span>

<span data-ttu-id="43680-165">预览版向版本号追加了 `-preview[number]-([build]|"final")`。</span><span class="sxs-lookup"><span data-stu-id="43680-165">Preview versions have a `-preview[number]-([build]|"final")` appended to the version number.</span></span> <span data-ttu-id="43680-166">例如 `2.0.0-preview1-final`。</span><span class="sxs-lookup"><span data-stu-id="43680-166">For example, `2.0.0-preview1-final`.</span></span>

### <a name="servicing-versions"></a><span data-ttu-id="43680-167">服务版本</span><span class="sxs-lookup"><span data-stu-id="43680-167">Servicing versions</span></span>

<span data-ttu-id="43680-168">在版本发布后，版本分支通常停止生成日常版本，而开始生成服务版本。</span><span class="sxs-lookup"><span data-stu-id="43680-168">After a release goes out, the release branches generally stop producing daily builds and instead start producing servicing builds.</span></span> <span data-ttu-id="43680-169">服务版本向版本追加了 `-servicing-[number]`。</span><span class="sxs-lookup"><span data-stu-id="43680-169">Servicing versions have a `-servicing-[number]` appended to the version.</span></span> <span data-ttu-id="43680-170">例如 `2.0.1-servicing-006924`。</span><span class="sxs-lookup"><span data-stu-id="43680-170">For example, `2.0.1-servicing-006924`.</span></span>

## <a name="relationship-to-net-standard-versions"></a><span data-ttu-id="43680-171">与 .NET Standard 版本的关系</span><span class="sxs-lookup"><span data-stu-id="43680-171">Relationship to .NET Standard versions</span></span>

<span data-ttu-id="43680-172">.NET Standard 由 .NET 引用程序集组成。</span><span class="sxs-lookup"><span data-stu-id="43680-172">.NET Standard consists of a .NET reference assembly.</span></span> <span data-ttu-id="43680-173">每个平台都有多个特定的实现。</span><span class="sxs-lookup"><span data-stu-id="43680-173">There are multiple implementations specific to each platform.</span></span> <span data-ttu-id="43680-174">引用程序集包含 .NET API 的定义，后者是给定 .NET Standard 版本的一部分。</span><span class="sxs-lookup"><span data-stu-id="43680-174">The reference assembly contains the definition of .NET APIs which are part of a given .NET Standard version.</span></span> <span data-ttu-id="43680-175">每个实现均满足特定平台上的 .NET Standard 协定。</span><span class="sxs-lookup"><span data-stu-id="43680-175">Each implementation fulfills the .NET Standard contract on the specific platform.</span></span>

<span data-ttu-id="43680-176">.NET Standard 引用程序集使用 `MAJOR.MINOR` 版本控制方案。</span><span class="sxs-lookup"><span data-stu-id="43680-176">The .NET Standard reference assembly uses a `MAJOR.MINOR` versioning scheme.</span></span> <span data-ttu-id="43680-177">`PATCH` 级别对 .NET Standard 并无用处，因为它只公开 API 规范（没有实现），并且根据定义，对 API 的任何更改都将作为功能集的更改，从进而产生新的 `MINOR` 版本。</span><span class="sxs-lookup"><span data-stu-id="43680-177">`PATCH` level isn't useful for .NET Standard because it exposes only an API specification (no implementation) and by definition any change to the API would represent a change in the feature set, and thus a new `MINOR` version.</span></span>

<span data-ttu-id="43680-178">每个平台上的实现通常可作为平台版本的一部分更新，因此对于在该平台上使用 .NET Standard 的程序员来说并不明显。</span><span class="sxs-lookup"><span data-stu-id="43680-178">The implementations on each platform may be updated, typically as part of the platform release, and thus not evident to the programmers using .NET Standard on that platform.</span></span>

<span data-ttu-id="43680-179">有关详细信息，请参阅 [.NET Standard](../../standard/net-standard.md)。</span><span class="sxs-lookup"><span data-stu-id="43680-179">For more information, see [.NET Standard](../../standard/net-standard.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="43680-180">请参阅</span><span class="sxs-lookup"><span data-stu-id="43680-180">See also</span></span>

- [<span data-ttu-id="43680-181">目标框架</span><span class="sxs-lookup"><span data-stu-id="43680-181">Target frameworks</span></span>](../../standard/frameworks.md)
- [<span data-ttu-id="43680-182">.NET 分发打包</span><span class="sxs-lookup"><span data-stu-id="43680-182">.NET distribution packaging</span></span>](../distribution-packaging.md)
- [<span data-ttu-id="43680-183">.NET 支持生命周期简报</span><span class="sxs-lookup"><span data-stu-id="43680-183">.NET Support Lifecycle Fact Sheet</span></span>](https://dotnet.microsoft.com/platform/support/policy)
- [<span data-ttu-id="43680-184">.NET 的 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="43680-184">Docker images for .NET</span></span>](https://hub.docker.com/_/microsoft-dotnet/)
