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
# <a name="netsdk1013-the-targetframework-value-was-not-recognized"></a>NETSDK1013：无法识别 TargetFramework 值

本文适用于：✔️ .NET 3.1.100 SDK 及更高版本

SDK 尝试将 `<TargetFramework>` 或 `<TargetFrameworks>` 项目文件中提供的值分析为已知值。  如果无法识别该值，则 `TargetFrameworkIdentifier` 或 `TargetFrameworkVersion` 值可能会设置为空字符串或 `Unsupported`。

为了解决此问题，请检查[支持的框架](../../../standard/frameworks.md)列表中 `TargetFramework` 值的拼写。
也可以直接在项目文件中设置 `TargetFrameworkIdentifier` 和 `TargetFrameworkVersion` 属性。

```xml
<PropertyGroup Condition="'$(TargetFrameworkIdentifier)' == ''">
  <TargetFrameworkIdentifier>.NETCOREAPP</TargetFrameworkIdentifier>
  <TargetFrameworkVersion>3.1</TargetFrameworkVersion>
</PropertyGroup>
```
