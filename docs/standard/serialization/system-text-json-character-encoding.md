---
title: 如何使用 System.Text.Json 自定义字符编码
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何自定义字符编码。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: f6a50a3ca2a5e871294cf7c056cbf197a61cd668
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439775"
---
# <a name="how-to-customize-character-encoding-with-no-locsystemtextjson"></a>如何使用 System.Text.Json 自定义字符编码

默认情况下，序列化程序会转义所有非 ASCII 字符。 即，会将它们替换为 `\uxxxx`，其中 `xxxx` 为字符的 Unicode 代码。 例如，如果以下 JSON 中的 `Summary` 属性设置为西里尔文 `жарко`，则 `WeatherForecast` 对象会进行序列化，如以下示例中所示：

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "\u0436\u0430\u0440\u043A\u043E"
}
```

## <a name="serialize-language-character-sets"></a>序列化语言字符集

若要序列化一种或多种语言的字符集而不进行转义，请在创建 <xref:System.Text.Encodings.Web.JavaScriptEncoder?displayProperty=fullName> 的实例时指定 [Unicode 范围](xref:System.Text.Unicode.UnicodeRanges)，如以下示例中所示：

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="LanguageSets":::

此代码不转义西里尔文或希腊语字符。 如果 `Summary` 属性设置为西里尔文 `жарко`，则 `WeatherForecast` 对象会进行序列化，如以下示例中所示：

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "жарко"
}
```

若要序列化所有语言集而不进行转义，请使用 <xref:System.Text.Unicode.UnicodeRanges.All?displayProperty=nameWithType>。

## <a name="serialize-specific-characters"></a>序列化特定字符

一种替代方法是指定要允许的单个字符，而不进行转义。 下面的示例仅序列化 `жарко` 的前两个字符：

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="SelectedCharacters":::

下面是前面代码生成的 JSON 的示例：

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "жа\u0440\u043A\u043E"
}
```

## <a name="serialize-all-characters"></a>序列化所有字符

若要最大程度地减少转义，可以使用 <xref:System.Text.Encodings.Web.JavaScriptEncoder.UnsafeRelaxedJsonEscaping?displayProperty=nameWithType>，如以下示例中所示：

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="UnsafeRelaxed":::

> [!CAUTION]
> 与默认编码器相比，`UnsafeRelaxedJsonEscaping` 编码器在允许字符通过而不进行转义方面更加宽松：
>
> * 它不转义 HTML 敏感字符，如 `<`、`>`、`&` 和 `'`。
> * 它不提供任何针对 XSS 或信息泄露攻击（如客户端和服务器在字符集方面不一致所可能导致的攻击）的额外深度防御保护。
>
> 仅当知道客户端将生成的有效负载解释为 UTF-8 编码的 JSON 时，才使用不安全编码器。 例如，如果服务器在发送响应标头 `Content-Type: application/json; charset=utf-8`，则可以使用它。 永远不允许将原始 `UnsafeRelaxedJsonEscaping` 输出发出到 HTML 页面或 `<script>` 元素。

## <a name="see-also"></a>请参阅

* [System.Text.Json 概述](system-text-json-overview.md)
* [如何编写自定义序列化程序和反序列化程序](write-custom-serializer-deserializer.md)
* [如何编写用于 JSON 序列化的自定义转换器](system-text-json-converters-how-to.md)
* [System.Text.Json API 参考](xref:System.Text.Json)
