---
title: 网络中断性变更
description: 列出 .NET Core 2.0 和 3.0 中网络的中断性变更。
ms.date: 05/05/2020
ms.openlocfilehash: 761c6481888bcb8e91f7b4212355aca067632495
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689207"
---
# <a name="networking-breaking-changes-in-net-core-20-and-30"></a><span data-ttu-id="77030-103">.NET Core 2.0 和 3.0 中的网络中断性变更</span><span class="sxs-lookup"><span data-stu-id="77030-103">Networking breaking changes in .NET Core 2.0 and 3.0</span></span>

<span data-ttu-id="77030-104">本页记录了以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="77030-104">The following breaking changes are documented on this page:</span></span>

| <span data-ttu-id="77030-105">重大更改</span><span class="sxs-lookup"><span data-stu-id="77030-105">Breaking change</span></span> | <span data-ttu-id="77030-106">引入的版本</span><span class="sxs-lookup"><span data-stu-id="77030-106">Introduced version</span></span> |
| - | - |
| [<span data-ttu-id="77030-107">HttpRequestMessage.Version 的默认值已更改为 1.1</span><span class="sxs-lookup"><span data-stu-id="77030-107">Default value of HttpRequestMessage.Version changed to 1.1</span></span>](#default-value-of-httprequestmessageversion-changed-to-11) | <span data-ttu-id="77030-108">3.0</span><span class="sxs-lookup"><span data-stu-id="77030-108">3.0</span></span> |
| [<span data-ttu-id="77030-109">WebClient.CancelAsync 并不总是立即取消</span><span class="sxs-lookup"><span data-stu-id="77030-109">WebClient.CancelAsync doesn't always cancel immediately</span></span>](#webclientcancelasync-doesnt-always-cancel-immediately) | <span data-ttu-id="77030-110">2.0</span><span class="sxs-lookup"><span data-stu-id="77030-110">2.0</span></span> |

## <a name="net-core-30"></a><span data-ttu-id="77030-111">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="77030-111">.NET Core 3.0</span></span>

[!INCLUDE[Default value of HttpRequestMessage.Version changed to 1.1](~/includes/core-changes/networking/3.0/httprequestmessage-version-change.md)]

***

## <a name="net-core-20"></a><span data-ttu-id="77030-112">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="77030-112">.NET Core 2.0</span></span>

[!INCLUDE [behavior-change-webclient-cancelasync](../../../includes/core-changes/networking/2.0/behavior-change-webclient-cancelasync.md)]

***
