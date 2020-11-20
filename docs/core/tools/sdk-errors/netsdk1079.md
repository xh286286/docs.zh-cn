---
title: NETSDK1079：面向 .NET Core 3.0 或更高版本时，不支持 Microsoft.AspNetCore.All 包。
description: 如何解决从 Microsoft.AspNetCore.App 迁移的问题
author: dsplaisted
ms.topic: error-reference
ms.date: 10/09/2020
f1_keywords:
- NETSDK1079
ms.openlocfilehash: e0b7aba909dbd2931f755238a2de2418d294751d
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94445671"
---
# <a name="netsdk1079-the-microsoftaspnetcoreall-package-is-not-supported-when-targeting-net-core-30-or-higher"></a><span data-ttu-id="7a04d-103">NETSDK1079：面向 .NET Core 3.0 或更高版本时，不支持 Microsoft.AspNetCore.All 包。</span><span class="sxs-lookup"><span data-stu-id="7a04d-103">NETSDK1079: The Microsoft.AspNetCore.All package is not supported when targeting .NET Core 3.0 or higher.</span></span>

<span data-ttu-id="7a04d-104">本文适用于：✔️ .NET Core SDK 3.1.100 及更高版本</span><span class="sxs-lookup"><span data-stu-id="7a04d-104">**This article applies to:** ✔️ .NET Core SDK 3.1.100 and later versions</span></span>

<span data-ttu-id="7a04d-105">在以下情况下，你可能会收到此错误消息：</span><span class="sxs-lookup"><span data-stu-id="7a04d-105">You may receive this error message when:</span></span>

- <span data-ttu-id="7a04d-106">将 ASP.NET Core 项目从 .NET Core 2.2 或更早版本重定向到 .NET Core 3.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="7a04d-106">You retarget an ASP.NET Core project from .NET Core 2.2 or earlier to .NET Core 3.0 or later.</span></span>
- <span data-ttu-id="7a04d-107">该项目使用 Microsoft.AspNetCore.All 包。</span><span class="sxs-lookup"><span data-stu-id="7a04d-107">The project uses the Microsoft.AspNetCore.All package.</span></span>

<span data-ttu-id="7a04d-108">已删除 Microsoft.AspNetCore.All 的 `PackageReference`。</span><span class="sxs-lookup"><span data-stu-id="7a04d-108">Remove the `PackageReference` for Microsoft.AspNetCore.All.</span></span>  <span data-ttu-id="7a04d-109">你可能还需要为从 Microsoft.AspNetCore.All 引用但不包含在 ASP.NET Core 共享框架中的包添加包引用。</span><span class="sxs-lookup"><span data-stu-id="7a04d-109">You may also need to add package references for packages that were referenced from Microsoft.AspNetCore.All but are not included in the ASP.NET Core shared framework.</span></span>  <span data-ttu-id="7a04d-110">此处列出了这些包：[从 Microsoft.AspNetCore.All 迁移到 Microsoft.AspNetCore.App](/aspnet/core/fundamentals/metapackage#migrating-from-microsoftaspnetcoreall-to-microsoftaspnetcoreapp)。</span><span class="sxs-lookup"><span data-stu-id="7a04d-110">These packages are listed here: [Migrating from Microsoft.AspNetCore.All to Microsoft.AspNetCore.App](/aspnet/core/fundamentals/metapackage#migrating-from-microsoftaspnetcoreall-to-microsoftaspnetcoreapp).</span></span>

<span data-ttu-id="7a04d-111">另请参阅[从 ASP.NET Core 2.2 迁移到 3.0](/aspnet/core/migration/22-to-30)</span><span class="sxs-lookup"><span data-stu-id="7a04d-111">See also [Migrate from ASP.NET Core 2.2 to 3.0](/aspnet/core/migration/22-to-30)</span></span>
