---
ms.openlocfilehash: 8315b4f86dddfbb68534bc9ad3ad74907daa03d0
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94507037"
---

### <a name="install-the-sdk"></a><span data-ttu-id="0dfb1-101">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="0dfb1-101">Install the SDK</span></span>

<span data-ttu-id="0dfb1-102">.NET Core SDK 使你可以通过 .NET Core 开发应用。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-102">The .NET Core SDK allows you to develop apps with .NET Core.</span></span> <span data-ttu-id="0dfb1-103">如果安装 .NET Core SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-103">If you install the .NET Core SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="0dfb1-104">若要安装 .NET Core SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="0dfb1-104">To install the .NET Core SDK, run the following commands:</span></span>

```bash
sudo dnf install dotnet-sdk-3.0
```

### <a name="install-the-runtime"></a><span data-ttu-id="0dfb1-105">安装运行时</span><span class="sxs-lookup"><span data-stu-id="0dfb1-105">Install the runtime</span></span>

<span data-ttu-id="0dfb1-106">.NET Core 运行时允许运行使用不随附运行时的 .NET Core 所开发的应用。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-106">The .NET Core Runtime allows you to run apps that were made with .NET Core that didn't include the runtime.</span></span> <span data-ttu-id="0dfb1-107">以下命令安装 ASP.NET Core 运行时，这是与 .NET Core 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-107">The following commands install the ASP.NET Core Runtime, which is the most compatible runtime for .NET Core.</span></span> <span data-ttu-id="0dfb1-108">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-108">In your terminal, run the following commands.</span></span>

```bash
sudo dnf install aspnetcore-runtime-3.0
```

<span data-ttu-id="0dfb1-109">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET Core 运行时：将上一命令中的 `aspnetcore-runtime-3.0` 替换为 `dotnet-runtime-3.0`。</span><span class="sxs-lookup"><span data-stu-id="0dfb1-109">As an alternative to the ASP.NET Core Runtime, you can install the .NET Core Runtime, which doesn't include ASP.NET Core support: replace `aspnetcore-runtime-3.0` in the previous command with `dotnet-runtime-3.0`.</span></span>

```bash
sudo dnf install dotnet-runtime-3.0
```
