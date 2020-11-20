---
ms.openlocfilehash: ed269683f5c4569c21ae53e9a3c1ec65eb5ebd43
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506842"
---

### <a name="install-the-sdk"></a><span data-ttu-id="76d7e-101">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="76d7e-101">Install the SDK</span></span>

<span data-ttu-id="76d7e-102">.NET SDK 使你可以通过 .NET 开发应用。</span><span class="sxs-lookup"><span data-stu-id="76d7e-102">The .NET SDK allows you to develop apps with .NET.</span></span> <span data-ttu-id="76d7e-103">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="76d7e-103">If you install the .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="76d7e-104">若要安装 .NET SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="76d7e-104">To install the .NET SDK, run the following commands:</span></span>

```bash
sudo zypper install dotnet-sdk-5.0
```

### <a name="install-the-runtime"></a><span data-ttu-id="76d7e-105">安装运行时</span><span class="sxs-lookup"><span data-stu-id="76d7e-105">Install the runtime</span></span>

<span data-ttu-id="76d7e-106">通过 ASP.NET Core 运行时，可以运行使用 .NET 开发且未提供运行时的应用。</span><span class="sxs-lookup"><span data-stu-id="76d7e-106">The ASP.NET Core Runtime allows you to run apps that were made with .NET that didn't provide the runtime.</span></span> <span data-ttu-id="76d7e-107">以下命令将安装 ASP.NET Core 运行时，这是与 .NET 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="76d7e-107">The following commands install the ASP.NET Core Runtime, which is the most compatible runtime for .NET.</span></span> <span data-ttu-id="76d7e-108">在终端中，运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="76d7e-108">In your terminal, run the following commands:</span></span>

```bash
sudo zypper install aspnetcore-runtime-5.0
```

<span data-ttu-id="76d7e-109">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET 运行时：将上一命令中的 `aspnetcore-runtime-5.0` 替换为 `dotnet-runtime-5.0`：</span><span class="sxs-lookup"><span data-stu-id="76d7e-109">As an alternative to the ASP.NET Core Runtime, you can install the .NET Runtime, which doesn't include ASP.NET Core support: replace `aspnetcore-runtime-5.0` in the previous command with `dotnet-runtime-5.0`:</span></span>

```bash
sudo zypper install dotnet-runtime-5.0
```
