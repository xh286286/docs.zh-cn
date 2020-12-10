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
# <a name="how-to-enable-case-insensitive-property-name-matching-with-no-locsystemtextjson"></a><span data-ttu-id="caa75-103">如何使用 System.Text.Json 启用不区分大小写的属性名称</span><span class="sxs-lookup"><span data-stu-id="caa75-103">How to enable case-insensitive property name matching with System.Text.Json</span></span>

<span data-ttu-id="caa75-104">本文将介绍如何使用 `System.Text.Json` 命名空间启用不区分大小写的属性名称匹配。</span><span class="sxs-lookup"><span data-stu-id="caa75-104">In this article, you will learn how to enable case-insensitive property name matching with the `System.Text.Json` namespace.</span></span>

## <a name="case-insensitive-property-matching"></a><span data-ttu-id="caa75-105">不区分大小写的属性匹配</span><span class="sxs-lookup"><span data-stu-id="caa75-105">Case-insensitive property matching</span></span>

<span data-ttu-id="caa75-106">默认情况下，反序列化会查找 JSON 与目标对象属性之间区分大小写的属性名称匹配。</span><span class="sxs-lookup"><span data-stu-id="caa75-106">By default, deserialization looks for case-sensitive property name matches between JSON and the target object properties.</span></span> <span data-ttu-id="caa75-107">若要更改该行为，请将 <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive?displayProperty=nameWithType> 设置为 `true`：</span><span class="sxs-lookup"><span data-stu-id="caa75-107">To change that behavior, set <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive?displayProperty=nameWithType> to `true`:</span></span>

> [!NOTE]
> <span data-ttu-id="caa75-108">[Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="caa75-108">The [web default](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions) is case-insensitive.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/DeserializeCaseInsensitive.cs" id="Deserialize":::

<span data-ttu-id="caa75-109">下面是具有 camel 大小写属性名称的示例 JSON。</span><span class="sxs-lookup"><span data-stu-id="caa75-109">Here's example JSON with camel case property names.</span></span> <span data-ttu-id="caa75-110">它可以反序列化为具有帕斯卡拼写法属性名称的以下类型。</span><span class="sxs-lookup"><span data-stu-id="caa75-110">It can be deserialized into the following type that has Pascal case property names.</span></span>

```json
{
  "date": "2019-08-01T00:00:00-07:00",
  "temperatureCelsius": 25,
  "summary": "Hot",
}
```

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

## <a name="see-also"></a><span data-ttu-id="caa75-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="caa75-111">See also</span></span>

* [<span data-ttu-id="caa75-112">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="caa75-112">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="caa75-113">实例化 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="caa75-113">Instantiate JsonSerializerOptions</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="caa75-114">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="caa75-114">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="caa75-115">忽略属性</span><span class="sxs-lookup"><span data-stu-id="caa75-115">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="caa75-116">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="caa75-116">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="caa75-117">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="caa75-117">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="caa75-118">保留循环引用</span><span class="sxs-lookup"><span data-stu-id="caa75-118">Preserve circular references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="caa75-119">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="caa75-119">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="caa75-120">多态序列化</span><span class="sxs-lookup"><span data-stu-id="caa75-120">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* <span data-ttu-id="caa75-121">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="caa75-121">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
