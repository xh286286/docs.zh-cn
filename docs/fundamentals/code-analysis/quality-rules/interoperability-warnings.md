---
title: '可移植性和互操作性规则 (代码分析) '
description: 了解代码分析规则可移植性和互操作性规则
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.Portablityrules
- vs.codeanalysis.Interoperabilityrules
helpviewer_keywords:
- managed code analysis rules, interoperability rules, portability rules
- portability rules
- warnings, portability
- interoperability rules
- warnings, interoperability
author: gewarren
ms.author: gewarren
ms.openlocfilehash: a20cd77e13c4a8b95633d129990667f0a8de3ee8
ms.sourcegitcommit: 2e4adc490c1d2a705a0592b295d606b10b9f51f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "96590173"
---
# <a name="portability-and-interoperability-rules"></a><span data-ttu-id="60618-103">可移植性和互操作性规则</span><span class="sxs-lookup"><span data-stu-id="60618-103">Portability and interoperability rules</span></span>

<span data-ttu-id="60618-104">可移植性规则支持跨不同平台的可移植性。</span><span class="sxs-lookup"><span data-stu-id="60618-104">Portability rules support portability across different platforms.</span></span> <span data-ttu-id="60618-105">互操作性规则支持与 COM 客户端的交互。</span><span class="sxs-lookup"><span data-stu-id="60618-105">Interoperability rules support interaction with COM clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="60618-106">在本节中</span><span class="sxs-lookup"><span data-stu-id="60618-106">In this section</span></span>

| <span data-ttu-id="60618-107">规则</span><span class="sxs-lookup"><span data-stu-id="60618-107">Rule</span></span> | <span data-ttu-id="60618-108">描述</span><span class="sxs-lookup"><span data-stu-id="60618-108">Description</span></span> |
| - | - |
| [<span data-ttu-id="60618-109">CA1401： P/Invoke 应不可见</span><span class="sxs-lookup"><span data-stu-id="60618-109">CA1401: P/Invokes should not be visible</span></span>](ca1401.md) | <span data-ttu-id="60618-110">公共类型中的公共或受保护方法具有 System.Runtime.InteropServices.DllImportAttribute 特性 (也由 Visual Basic) 中的 Declare 关键字实现。</span><span class="sxs-lookup"><span data-stu-id="60618-110">A public or protected method in a public type has the System.Runtime.InteropServices.DllImportAttribute attribute (also implemented by the Declare keyword in Visual Basic).</span></span> <span data-ttu-id="60618-111">这些方法不能公开。</span><span class="sxs-lookup"><span data-stu-id="60618-111">Such methods should not be exposed.</span></span> |
| [<span data-ttu-id="60618-112">CA1416：验证平台兼容性</span><span class="sxs-lookup"><span data-stu-id="60618-112">CA1416: Validate platform compatibility</span></span>](ca1416.md) | <span data-ttu-id="60618-113">在组件上使用平台相关的 Api 使代码在所有平台上都不再工作。</span><span class="sxs-lookup"><span data-stu-id="60618-113">Using platform-dependent APIs on a component makes the code no longer work across all platforms.</span></span> |
| [<span data-ttu-id="60618-114">CA1417：不 `OutAttribute` 在 P/invoke 的字符串参数上使用</span><span class="sxs-lookup"><span data-stu-id="60618-114">CA1417: Do not use `OutAttribute` on string parameters for P/Invokes</span></span>](ca1417.md) | <span data-ttu-id="60618-115">如果字符串是暂存的字符串，则通过值传递的字符串参数与 `OutAttribute` 运行时的不稳定性。</span><span class="sxs-lookup"><span data-stu-id="60618-115">String parameters passed by value with the `OutAttribute` can destabilize the runtime if the string is an interned string.</span></span> |
