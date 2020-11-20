---
ms.openlocfilehash: 3bb59ba23214f67100d3a78bb689c941b2d187e6
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506949"
---

<span data-ttu-id="372ec-101">安装 .NET 包时，可能会看到类似于 `Failed to fetch ... File has unexpected size ... Mirror sync in progress?` 的错误。</span><span class="sxs-lookup"><span data-stu-id="372ec-101">While installing the .NET package, you may see an error similar to `Failed to fetch ... File has unexpected size ... Mirror sync in progress?`.</span></span> <span data-ttu-id="372ec-102">此错误表示 .NET 的包源正在通过更新的包版本进行更新，应稍后重试。</span><span class="sxs-lookup"><span data-stu-id="372ec-102">This error could mean that the package feed for .NET is being upgraded with newer package versions, and that you should try again later.</span></span> <span data-ttu-id="372ec-103">升级期间，包源的不可用时间不应超过 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="372ec-103">During an upgrade, the package feed shouldn't be unavailable for more than 30 minutes.</span></span> <span data-ttu-id="372ec-104">如果持续收到此错误超过 30 分钟，请在 <https://github.com/dotnet/core/issues> 中提交问题。</span><span class="sxs-lookup"><span data-stu-id="372ec-104">If you continually receive this error for more than 30 minutes, please file an issue at <https://github.com/dotnet/core/issues>.</span></span>
