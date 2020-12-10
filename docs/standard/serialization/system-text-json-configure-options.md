---
title: 如何使用 System.Text.Json 实例化 JsonSerializerOptions
description: 了解如何通过复制现有实例或使用 Web 默认值来实例化 JsonSerializerOptions 实例。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
zone_pivot_groups: dotnet-version
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 0febfe15f36856f10699fd327fb17c146277eb9b
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439778"
---
# <a name="how-to-instantiate-jsonserializeroptions-instances-with-no-locsystemtextjson"></a>如何使用 System.Text.Json 实例化 JsonSerializerOptions 实例

本文将介绍如何通过复制现有实例或使用 Web 默认值实例化 <xref:System.Text.Json.JsonSerializerOptions> 实例。

## <a name="copy-jsonserializeroptions"></a>复制 JsonSerializerOptions

::: zone pivot="dotnet-5-0"
存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerOptions)) ，可让你使用与现有实例相同的选项来创建新的实例，如以下示例中所示：

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/CopyOptions.cs" highlight="29":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
使用现有实例的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。
::: zone-end

## <a name="web-defaults-for-jsonserializeroptions"></a>JsonSerializerOptions 的 Web 默认值

::: zone pivot="dotnet-5-0"
下面是具有 Web 应用不同默认值的选项：

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>
* <xref:System.Text.Json.JsonSerializerOptions.NumberHandling%2A> = <xref:System.Text.Json.Serialization.JsonNumberHandling.AllowReadingFromString>

存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerDefaults)?view=net-5.0&preserve-view=true)，可让你通过 ASP.NET Core 对 Web 应用使用的默认选项创建新的实例，如以下示例中所示：

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/OptionsDefaults.cs" highlight="24":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
下面是具有 Web 应用不同默认值的选项：

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>

指定一组默认值的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。
::: zone-end

## <a name="see-also"></a>请参阅

* [System.Text.Json 概述](system-text-json-overview.md)
* [启用不区分大小写的匹配](system-text-json-character-casing.md)
* [自定义属性名称和值](system-text-json-customize-properties.md)
* [忽略属性](system-text-json-ignore-properties.md)
* [允许无效的 JSON](system-text-json-invalid-json.md)
* [处理溢出 JSON](system-text-json-handle-overflow.md)
* [保留循环引用](system-text-json-preserve-references.md)
* [不可变类型和非公共访问器](system-text-json-immutability.md)
* [多态序列化](system-text-json-polymorphism.md)
* [System.Text.Json API 参考](xref:System.Text.Json)
