---
ms.openlocfilehash: 8c05af045d2d9666b20f36e36c68cc853f906eae
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506843"
---

<span data-ttu-id="70caf-101">安装 .NET 包时，可能会看到类似于 `signature verification failed for file 'repomd.xml' from repository 'packages-microsoft-com-prod'` 的错误。</span><span class="sxs-lookup"><span data-stu-id="70caf-101">While installing the .NET package, you may see an error similar to `signature verification failed for file 'repomd.xml' from repository 'packages-microsoft-com-prod'`.</span></span> <span data-ttu-id="70caf-102">一般而言，此错误表示 .NET 的包源正在通过更新的包版本进行更新，应稍后重试。</span><span class="sxs-lookup"><span data-stu-id="70caf-102">Generally speaking, this error means that the package feed for .NET is being upgraded with newer package versions, and that you should try again later.</span></span> <span data-ttu-id="70caf-103">升级期间，包源的不可用时间不应超过 2 小时。</span><span class="sxs-lookup"><span data-stu-id="70caf-103">During an upgrade, the package feed should not be unavailable for more than 2 hours.</span></span> <span data-ttu-id="70caf-104">如果持续收到此错误超过 2 小时，请在 <https://github.com/dotnet/core/issues> 中提交问题。</span><span class="sxs-lookup"><span data-stu-id="70caf-104">If you continually receive this error for more than 2 hours, please file an issue at <https://github.com/dotnet/core/issues>.</span></span>
