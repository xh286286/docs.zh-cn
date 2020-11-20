---
title: NETSDK1022：包含重复的项。
description: 如何根据默认包含项解决重复项消息。
author: marcpopMSFT
ms.topic: error-reference
ms.date: 10/9/2020
f1_keywords:
- NETSDK1022
ms.openlocfilehash: bc803f5316bf09c12c563f1a63b8385d1be4e9ce
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506631"
---
# <a name="netsdk1022-duplicate-items-were-included"></a><span data-ttu-id="e3948-103">NETSDK1022：包含重复的项。</span><span class="sxs-lookup"><span data-stu-id="e3948-103">NETSDK1022: Duplicate items were included.</span></span>

<span data-ttu-id="e3948-104">**本文适用于：** ✔️ .NET 2.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="e3948-104">**This article applies to:** ✔️ .NET 2.1.100 SDK and later versions</span></span>

<span data-ttu-id="e3948-105">从 Visual Studio 2017 / MSBuild 版本 15.3 开始，默认情况下 .NET SDK 会自动包括项目目录中的项。</span><span class="sxs-lookup"><span data-stu-id="e3948-105">Starting in Visual Studio 2017 / MSBuild version 15.3, the .NET SDK automatically includes items from the project directory by default.</span></span>  <span data-ttu-id="e3948-106">这包括 `Compile` 和 `Content` 目标。</span><span class="sxs-lookup"><span data-stu-id="e3948-106">This includes `Compile` and `Content` targets.</span></span>  <span data-ttu-id="e3948-107">这应该能够很好地清理你的项目文件，并降低其中的复杂性。</span><span class="sxs-lookup"><span data-stu-id="e3948-107">This should greatly clean up your project file and reduce the complexity you have there.</span></span>

<span data-ttu-id="e3948-108">通过将正确的属性设置为 false，可以还原到以前的行为。</span><span class="sxs-lookup"><span data-stu-id="e3948-108">You can revert to the earlier behavior by setting the correct property to false.</span></span>

<span data-ttu-id="e3948-109">`Compile` 项的示例：</span><span class="sxs-lookup"><span data-stu-id="e3948-109">Example for `Compile` items:</span></span>

```xml
<PropertyGroup>
    <EnableDefaultCompileItems>false</EnableDefaultCompileItems>
</PropertyGroup>
```
