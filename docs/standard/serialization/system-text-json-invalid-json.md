---
title: 如何使用 System.Text.Json 支持某种无效的 JSON
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何支持注释、尾随逗号和带引号的数字。
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
ms.openlocfilehash: 60cbb98bb65ee5c1ffdd3043e42a04004530a115
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439752"
---
# <a name="how-to-allow-some-kinds-of-invalid-json-with-no-locsystemtextjson"></a><span data-ttu-id="71b65-103">如何使用 System.Text.Json 支持某种无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="71b65-103">How to allow some kinds of invalid JSON with System.Text.Json</span></span>

<span data-ttu-id="71b65-104">本文将介绍如何能够在 JSON 中使用注释、尾随逗号和带引号的数字，以及如何将数字编写为字符串。</span><span class="sxs-lookup"><span data-stu-id="71b65-104">In this article, you will learn how to allow comments, trailing commas, and quoted numbers in JSON, and how to write numbers as strings.</span></span>

## <a name="allow-comments-and-trailing-commas"></a><span data-ttu-id="71b65-105">允许注释和尾随逗号</span><span class="sxs-lookup"><span data-stu-id="71b65-105">Allow comments and trailing commas</span></span>

<span data-ttu-id="71b65-106">默认情况下，JSON 中不允许使用注释和尾随逗号。</span><span class="sxs-lookup"><span data-stu-id="71b65-106">By default, comments and trailing commas are not allowed in JSON.</span></span> <span data-ttu-id="71b65-107">若要在 JSON 中允许注释，请将 <xref:System.Text.Json.JsonSerializerOptions.ReadCommentHandling?displayProperty=nameWithType> 属性设置为 `JsonCommentHandling.Skip`。</span><span class="sxs-lookup"><span data-stu-id="71b65-107">To allow comments in the JSON, set the <xref:System.Text.Json.JsonSerializerOptions.ReadCommentHandling?displayProperty=nameWithType> property to `JsonCommentHandling.Skip`.</span></span>
<span data-ttu-id="71b65-108">若要允许尾随逗号，请将 <xref:System.Text.Json.JsonSerializerOptions.AllowTrailingCommas?displayProperty=nameWithType> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="71b65-108">And to allow trailing commas, set the <xref:System.Text.Json.JsonSerializerOptions.AllowTrailingCommas?displayProperty=nameWithType> property to `true`.</span></span> <span data-ttu-id="71b65-109">下面的示例演示如何允许这两者：</span><span class="sxs-lookup"><span data-stu-id="71b65-109">The following example shows how to allow both:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/DeserializeCommasComments.cs" id="Deserialize":::

<span data-ttu-id="71b65-110">下面是包含注释和尾随逗号的示例 JSON：</span><span class="sxs-lookup"><span data-stu-id="71b65-110">Here's example JSON with comments and a trailing comma:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25, // Fahrenheit 77
  "Summary": "Hot", /* Zharko */
}
```

## <a name="allow-or-write-numbers-in-quotes"></a><span data-ttu-id="71b65-111">允许或写入带引号的数字</span><span class="sxs-lookup"><span data-stu-id="71b65-111">Allow or write numbers in quotes</span></span>

::: zone pivot="dotnet-5-0"

<span data-ttu-id="71b65-112">某些序列化程序将数字编码为 JSON 字符串（括在引号中）。</span><span class="sxs-lookup"><span data-stu-id="71b65-112">Some serializers encode numbers as JSON strings (surrounded by quotes).</span></span>

<span data-ttu-id="71b65-113">例如：</span><span class="sxs-lookup"><span data-stu-id="71b65-113">For example:</span></span>

```json
{
    "DegreesCelsius": "23"
}
```

<span data-ttu-id="71b65-114">不是：</span><span class="sxs-lookup"><span data-stu-id="71b65-114">Instead of:</span></span>

```json
{
    "DegreesCelsius": 23
}
```

<span data-ttu-id="71b65-115">若要在整个输入对象图中序列化带引号的数字或接受带引号的数字，请设置 <xref:System.Text.Json.JsonSerializerOptions.NumberHandling%2A?displayProperty=nameWithType>，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="71b65-115">To serialize numbers in quotes or accept numbers in quotes across the entire input object graph, set <xref:System.Text.Json.JsonSerializerOptions.NumberHandling%2A?displayProperty=nameWithType> as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/QuotedNumbers.cs" highlight="27-29":::

<span data-ttu-id="71b65-116">在通过 ASP.NET Core 间接使用 `System.Text.Json` 时，反序列化时允许使用带引号的数字，因为 ASP.NET Core 指定 [Web 默认选项](xref:System.Text.Json.JsonSerializerDefaults.Web)。</span><span class="sxs-lookup"><span data-stu-id="71b65-116">When you use `System.Text.Json` indirectly through ASP.NET Core, quoted numbers are allowed when deserializing because ASP.NET Core specifies [web default options](xref:System.Text.Json.JsonSerializerDefaults.Web).</span></span>

<span data-ttu-id="71b65-117">若要允许或写入特定属性、字段或类型的带引号的数字，请使用 [[JsonNumberHandling]](xref:System.Text.Json.Serialization.JsonNumberHandlingAttribute) 特性。</span><span class="sxs-lookup"><span data-stu-id="71b65-117">To allow or write quoted numbers for specific properties, fields, or types, use the [[JsonNumberHandling]](xref:System.Text.Json.Serialization.JsonNumberHandlingAttribute) attribute.</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="71b65-118">.NET Core 3.1 中的 `System.Text.Json` 不支持序列化或反序列化用引号引起来的数字。</span><span class="sxs-lookup"><span data-stu-id="71b65-118">`System.Text.Json` in .NET Core 3.1 doesn't support serializing or deserializing numbers surrounded by quotation marks.</span></span> <span data-ttu-id="71b65-119">有关详细信息，请参阅[允许或写入带引号的数字](system-text-json-migrate-from-newtonsoft-how-to.md#allow-or-write-numbers-in-quotes)。</span><span class="sxs-lookup"><span data-stu-id="71b65-119">For more information, see [Allow or write numbers in quotes](system-text-json-migrate-from-newtonsoft-how-to.md#allow-or-write-numbers-in-quotes).</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="71b65-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="71b65-120">See also</span></span>

* [<span data-ttu-id="71b65-121">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="71b65-121">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="71b65-122">实例化 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="71b65-122">Instantiate JsonSerializerOptions</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="71b65-123">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="71b65-123">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="71b65-124">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="71b65-124">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="71b65-125">忽略属性</span><span class="sxs-lookup"><span data-stu-id="71b65-125">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="71b65-126">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="71b65-126">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="71b65-127">保留循环引用</span><span class="sxs-lookup"><span data-stu-id="71b65-127">Preserve circular references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="71b65-128">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="71b65-128">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="71b65-129">多态序列化</span><span class="sxs-lookup"><span data-stu-id="71b65-129">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* <span data-ttu-id="71b65-130">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="71b65-130">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
