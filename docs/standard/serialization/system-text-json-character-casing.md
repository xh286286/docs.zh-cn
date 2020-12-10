---
title: 如何使用 System.Text.Json 启用不区分大小写的属性名称
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何启用不区分大小写的属性名称匹配。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 2d663ac8c1c15d61959a62c40d9a3b0993484032
ms.sourcegitcommit: 9d525bb8109216ca1dc9e39c149d4902f4b43da5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "96599071"
---
# <a name="how-to-enable-case-insensitive-property-name-matching-with-no-locsystemtextjson"></a>如何使用 System.Text.Json 启用不区分大小写的属性名称

本文将介绍如何使用 `System.Text.Json` 命名空间启用不区分大小写的属性名称匹配。

## <a name="case-insensitive-property-matching"></a>不区分大小写的属性匹配

默认情况下，反序列化会查找 JSON 与目标对象属性之间区分大小写的属性名称匹配。 若要更改该行为，请将 <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive?displayProperty=nameWithType> 设置为 `true`：

> [!NOTE]
> [Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)为不区分大小写。

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/DeserializeCaseInsensitive.cs" id="Deserialize":::

下面是具有 camel 大小写属性名称的示例 JSON。 它可以反序列化为具有帕斯卡拼写法属性名称的以下类型。

```json
{
  "date": "2019-08-01T00:00:00-07:00",
  "temperatureCelsius": 25,
  "summary": "Hot",
}
```

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

## <a name="see-also"></a>请参阅

* [System.Text.Json 概述](system-text-json-overview.md)
* [实例化 JsonSerializerOptions](system-text-json-configure-options.md)
* [自定义属性名称和值](system-text-json-customize-properties.md)
* [忽略属性](system-text-json-ignore-properties.md)
* [允许无效的 JSON](system-text-json-invalid-json.md)
* [处理溢出 JSON](system-text-json-handle-overflow.md)
* [保留循环引用](system-text-json-preserve-references.md)
* [不可变类型和非公共访问器](system-text-json-immutability.md)
* [多态序列化](system-text-json-polymorphism.md)
* [System.Text.Json API 参考](xref:System.Text.Json)
