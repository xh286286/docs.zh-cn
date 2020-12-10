---
title: 如何使用 System.Text.Json 保留引用
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何保留引用并处理循环引用。
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
ms.openlocfilehash: 9254ca261c7d748c04c311fa56359014f752ff31
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439758"
---
# <a name="how-to-handle-circular-references-with-no-locsystemtextjson"></a>如何使用 System.Text.Json 处理循环引用

本文将介绍如何使用 `System.Text.Json` 命名空间处理循环引用。

## <a name="preserve-references-and-handle-circular-references"></a>保留引用并处理循环引用

::: zone pivot="dotnet-5-0"

若要保留引用并处理循环引用，请将 <xref:System.Text.Json.JsonSerializerOptions.ReferenceHandler%2A> 设置为 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A>。 此设置会导致以下行为：

* 在序列化时：

  编写复杂类型时，序列化程序还会写入元数据属性（`$id`、`$values` 和 `$ref`）。

* 在反序列化时：

  需要元数据（虽然不是必需的），并且反序列化程序会尝试理解它。

下面的代码演示 `Preserve` 属性的用法。

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/PreserveReferences.cs" highlight="34":::

此功能不能用于保留值类型或不可变类型。 在反序列化时，将在读取整个有效负载后创建不可变类型的实例。 因此，如果对同一实例的引用出现在 JSON 有效负载中，则无法对其进行反序列化。

对于值类型、不可变类型和数组，不会序列化任何引用元数据。 反序列化时，如果发现 `$ref` 或 `$id`，则会引发异常。 但是，值类型忽略 `$id`（对于集合，则为 `$values`），以便可以反序列化使用 Newtonsoft.Json 序列化的有效负载。  Newtonsoft.Json 为此类类型序列化元数据。

为了确定对象是否相等，System.Text.Json 在比较两个对象实例时使用引用相等性 (<xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=nameWithType>) 而不是值相等性 (<xref:System.Object.Equals(System.Object)?displayProperty=nameWithType> 的 <xref:System.Collections.Generic.ReferenceEqualityComparer.Instance%2A?displayProperty=nameWithType>。

有关如何序列化和反序列化引用的详细信息，请参阅 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A?displayProperty=nameWithType>。

<xref:System.Text.Json.Serialization.ReferenceResolver> 类定义在序列化和反序列化过程中保留引用的行为。 创建派生类以指定自定义行为。 有关示例，请参阅 [GuidReferenceResolver](https://github.com/dotnet/docs/blob/9d5e88edbd7f12be463775ffebbf07ac8415fe18/docs/standard/serialization/snippets/system-text-json-how-to-5-0/csharp/GuidReferenceResolverExample.cs)。

::: zone-end

::: zone pivot="dotnet-core-3-1"
.NET Core 3.1 中的 System.Text.Json 仅支持按值进行进行序列化，并对循环引用引发异常。
::: zone-end

## <a name="see-also"></a>请参阅

* [System.Text.Json 概述](system-text-json-overview.md)
* [实例化 JsonSerializerOptions](system-text-json-configure-options.md)
* [启用不区分大小写的匹配](system-text-json-character-casing.md)
* [自定义属性名称和值](system-text-json-customize-properties.md)
* [忽略属性](system-text-json-ignore-properties.md)
* [允许无效的 JSON](system-text-json-invalid-json.md)
* [处理溢出 JSON](system-text-json-handle-overflow.md)
* [不可变类型和非公共访问器](system-text-json-immutability.md)
* [多态序列化](system-text-json-polymorphism.md)
* [System.Text.Json API 参考](xref:System.Text.Json)
