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
# <a name="how-to-customize-character-encoding-with-no-locsystemtextjson"></a><span data-ttu-id="33f31-103">如何使用 System.Text.Json 自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="33f31-103">How to customize character encoding with System.Text.Json</span></span>

<span data-ttu-id="33f31-104">默认情况下，序列化程序会转义所有非 ASCII 字符。</span><span class="sxs-lookup"><span data-stu-id="33f31-104">By default, the serializer escapes all non-ASCII characters.</span></span> <span data-ttu-id="33f31-105">即，会将它们替换为 `\uxxxx`，其中 `xxxx` 为字符的 Unicode 代码。</span><span class="sxs-lookup"><span data-stu-id="33f31-105">That is, it replaces them with `\uxxxx` where `xxxx` is the Unicode code of the character.</span></span> <span data-ttu-id="33f31-106">例如，如果以下 JSON 中的 `Summary` 属性设置为西里尔文 `жарко`，则 `WeatherForecast` 对象会进行序列化，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="33f31-106">For example, if the `Summary` property in the following JSON is set to Cyrillic `жарко`, the `WeatherForecast` object is serialized as shown in this example:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "\u0436\u0430\u0440\u043A\u043E"
}
```

## <a name="serialize-language-character-sets"></a><span data-ttu-id="33f31-107">序列化语言字符集</span><span class="sxs-lookup"><span data-stu-id="33f31-107">Serialize language character sets</span></span>

<span data-ttu-id="33f31-108">若要序列化一种或多种语言的字符集而不进行转义，请在创建 <xref:System.Text.Encodings.Web.JavaScriptEncoder?displayProperty=fullName> 的实例时指定 [Unicode 范围](xref:System.Text.Unicode.UnicodeRanges)，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="33f31-108">To serialize the character set(s) of one or more languages without escaping, specify [Unicode range(s)](xref:System.Text.Unicode.UnicodeRanges) when creating an instance of <xref:System.Text.Encodings.Web.JavaScriptEncoder?displayProperty=fullName>, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="LanguageSets":::

<span data-ttu-id="33f31-109">此代码不转义西里尔文或希腊语字符。</span><span class="sxs-lookup"><span data-stu-id="33f31-109">This code doesn't escape Cyrillic or Greek characters.</span></span> <span data-ttu-id="33f31-110">如果 `Summary` 属性设置为西里尔文 `жарко`，则 `WeatherForecast` 对象会进行序列化，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="33f31-110">If the `Summary` property is set to Cyrillic `жарко`, the `WeatherForecast` object is serialized as shown in this example:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "жарко"
}
```

<span data-ttu-id="33f31-111">若要序列化所有语言集而不进行转义，请使用 <xref:System.Text.Unicode.UnicodeRanges.All?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="33f31-111">To serialize all language sets without escaping, use <xref:System.Text.Unicode.UnicodeRanges.All?displayProperty=nameWithType>.</span></span>

## <a name="serialize-specific-characters"></a><span data-ttu-id="33f31-112">序列化特定字符</span><span class="sxs-lookup"><span data-stu-id="33f31-112">Serialize specific characters</span></span>

<span data-ttu-id="33f31-113">一种替代方法是指定要允许的单个字符，而不进行转义。</span><span class="sxs-lookup"><span data-stu-id="33f31-113">An alternative is to specify individual characters that you want to allow through without being escaped.</span></span> <span data-ttu-id="33f31-114">下面的示例仅序列化 `жарко` 的前两个字符：</span><span class="sxs-lookup"><span data-stu-id="33f31-114">The following example serializes only the first two characters of `жарко`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="SelectedCharacters":::

<span data-ttu-id="33f31-115">下面是前面代码生成的 JSON 的示例：</span><span class="sxs-lookup"><span data-stu-id="33f31-115">Here's an example of JSON produced by the preceding code:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "жа\u0440\u043A\u043E"
}
```

## <a name="serialize-all-characters"></a><span data-ttu-id="33f31-116">序列化所有字符</span><span class="sxs-lookup"><span data-stu-id="33f31-116">Serialize all characters</span></span>

<span data-ttu-id="33f31-117">若要最大程度地减少转义，可以使用 <xref:System.Text.Encodings.Web.JavaScriptEncoder.UnsafeRelaxedJsonEscaping?displayProperty=nameWithType>，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="33f31-117">To minimize escaping you can use <xref:System.Text.Encodings.Web.JavaScriptEncoder.UnsafeRelaxedJsonEscaping?displayProperty=nameWithType>, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="Usings":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializeCustomEncoding.cs" id="UnsafeRelaxed":::

> [!CAUTION]
> <span data-ttu-id="33f31-118">与默认编码器相比，`UnsafeRelaxedJsonEscaping` 编码器在允许字符通过而不进行转义方面更加宽松：</span><span class="sxs-lookup"><span data-stu-id="33f31-118">Compared to the default encoder, the `UnsafeRelaxedJsonEscaping` encoder is more permissive about allowing characters to pass through unescaped:</span></span>
>
> * <span data-ttu-id="33f31-119">它不转义 HTML 敏感字符，如 `<`、`>`、`&` 和 `'`。</span><span class="sxs-lookup"><span data-stu-id="33f31-119">It doesn't escape HTML-sensitive characters such as `<`, `>`, `&`, and `'`.</span></span>
> * <span data-ttu-id="33f31-120">它不提供任何针对 XSS 或信息泄露攻击（如客户端和服务器在字符集方面不一致所可能导致的攻击）的额外深度防御保护。</span><span class="sxs-lookup"><span data-stu-id="33f31-120">It doesn't offer any additional defense-in-depth protections against XSS or information disclosure attacks, such as those which might result from the client and server disagreeing on the *charset*.</span></span>
>
> <span data-ttu-id="33f31-121">仅当知道客户端将生成的有效负载解释为 UTF-8 编码的 JSON 时，才使用不安全编码器。</span><span class="sxs-lookup"><span data-stu-id="33f31-121">Use the unsafe encoder only when it's known that the client will be interpreting the resulting payload as UTF-8 encoded JSON.</span></span> <span data-ttu-id="33f31-122">例如，如果服务器在发送响应标头 `Content-Type: application/json; charset=utf-8`，则可以使用它。</span><span class="sxs-lookup"><span data-stu-id="33f31-122">For example, you can use it if the server is sending the response header `Content-Type: application/json; charset=utf-8`.</span></span> <span data-ttu-id="33f31-123">永远不允许将原始 `UnsafeRelaxedJsonEscaping` 输出发出到 HTML 页面或 `<script>` 元素。</span><span class="sxs-lookup"><span data-stu-id="33f31-123">Never allow the raw `UnsafeRelaxedJsonEscaping` output to be emitted into an HTML page or a `<script>` element.</span></span>

## <a name="see-also"></a><span data-ttu-id="33f31-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="33f31-124">See also</span></span>

* [<span data-ttu-id="33f31-125">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="33f31-125">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="33f31-126">如何编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="33f31-126">How to write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="33f31-127">如何编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="33f31-127">How to write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* <span data-ttu-id="33f31-128">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="33f31-128">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
