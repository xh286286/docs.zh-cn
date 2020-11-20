---
title: NETSDK1013：无法识别 TargetFramework 值。
description: 如何确定和设置有效 TargetFramework 值
author: marcpop
ms.topic: error-reference
ms.date: 10/9/2020
f1_keywords:
- NETSDK1013
ms.openlocfilehash: bcaed878b663f8bc957e8469ffd78caa9babf710
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94445669"
---
# <a name="netsdk1013-the-targetframework-value-was-not-recognized"></a><span data-ttu-id="9e9a4-103">NETSDK1013：无法识别 TargetFramework 值</span><span class="sxs-lookup"><span data-stu-id="9e9a4-103">NETSDK1013: The TargetFramework value was not recognized</span></span>

<span data-ttu-id="9e9a4-104">本文适用于：✔️ .NET 3.1.100 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="9e9a4-104">**This article applies to:** ✔️ .NET 3.1.100 SDK and later versions</span></span>

<span data-ttu-id="9e9a4-105">SDK 尝试将 `<TargetFramework>` 或 `<TargetFrameworks>` 项目文件中提供的值分析为已知值。</span><span class="sxs-lookup"><span data-stu-id="9e9a4-105">The SDK tries to parse the values provided in the project file for `<TargetFramework>` or `<TargetFrameworks>` into a well known value.</span></span>  <span data-ttu-id="9e9a4-106">如果无法识别该值，则 `TargetFrameworkIdentifier` 或 `TargetFrameworkVersion` 值可能会设置为空字符串或 `Unsupported`。</span><span class="sxs-lookup"><span data-stu-id="9e9a4-106">If the value is not recognized, the `TargetFrameworkIdentifier` or `TargetFrameworkVersion` value may be set to an empty string or `Unsupported`.</span></span>

<span data-ttu-id="9e9a4-107">为了解决此问题，请检查[支持的框架](../../../standard/frameworks.md)列表中 `TargetFramework` 值的拼写。</span><span class="sxs-lookup"><span data-stu-id="9e9a4-107">To resolve this, check the spelling of your `TargetFramework` value from the list of [supported frameworks](../../../standard/frameworks.md).</span></span>
<span data-ttu-id="9e9a4-108">也可以直接在项目文件中设置 `TargetFrameworkIdentifier` 和 `TargetFrameworkVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="9e9a4-108">You can also set the `TargetFrameworkIdentifier` and `TargetFrameworkVersion` properties directly in your project file.</span></span>

```xml
<PropertyGroup Condition="'$(TargetFrameworkIdentifier)' == ''">
  <TargetFrameworkIdentifier>.NETCOREAPP</TargetFrameworkIdentifier>
  <TargetFrameworkVersion>3.1</TargetFrameworkVersion>
</PropertyGroup>
```
