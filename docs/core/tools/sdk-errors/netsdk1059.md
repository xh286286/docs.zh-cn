---
title: NETSDK1059：项目包含已过时的 .NET CLI 工具
description: 如何解决项目包含已过时的 .NET CLI 工具的问题。
author: sfoslund
ms.topic: error-reference
ms.date: 10/09/2020
f1_keywords:
- NETSDK1059
ms.openlocfilehash: b80f42495e1aff8d37008946f10f68c195d5a9ec
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713114"
---
# <a name="netsdk1059-project-contains-obsolete-net-cli-tool"></a><span data-ttu-id="740ef-103">NETSDK1059：项目包含已过时的 .NET CLI 工具</span><span class="sxs-lookup"><span data-stu-id="740ef-103">NETSDK1059: Project contains obsolete .NET CLI tool</span></span>

<span data-ttu-id="740ef-104">本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="740ef-104">**This article applies to:** ✔️ .NET Core 2.1.100 SDK and later versions</span></span>

<span data-ttu-id="740ef-105">当 .NET SDK 发出警告 NETSDK1059 时，表示项目包含已过时的 .NET CLI 工具。</span><span class="sxs-lookup"><span data-stu-id="740ef-105">When the .NET SDK issues warning NETSDK1059, your project contains an obsolete .NET CLI tool.</span></span> <span data-ttu-id="740ef-106">自 .NET Core 2.1 起，这些工具包含在 .NET SDK 中，无需由项目显式引用。</span><span class="sxs-lookup"><span data-stu-id="740ef-106">As of .NET Core 2.1, these tools are included in the .NET SDK and do not need to be explicitly referenced by the project.</span></span> <span data-ttu-id="740ef-107">要详细了解如何迁移到 .NET Core 2.1，请参阅[此处](https://aka.ms/dotnetclitools-in-box)。</span><span class="sxs-lookup"><span data-stu-id="740ef-107">More information for migrating to .NET Core 2.1 can be found [here](https://aka.ms/dotnetclitools-in-box).</span></span>
