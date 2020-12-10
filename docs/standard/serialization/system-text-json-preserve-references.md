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
# <a name="how-to-handle-circular-references-with-no-locsystemtextjson"></a><span data-ttu-id="c788a-103">如何使用 System.Text.Json 处理循环引用</span><span class="sxs-lookup"><span data-stu-id="c788a-103">How to handle circular references with System.Text.Json</span></span>

<span data-ttu-id="c788a-104">本文将介绍如何使用 `System.Text.Json` 命名空间处理循环引用。</span><span class="sxs-lookup"><span data-stu-id="c788a-104">In this article, you will learn how to handle circular references with the `System.Text.Json` namespace.</span></span>

## <a name="preserve-references-and-handle-circular-references"></a><span data-ttu-id="c788a-105">保留引用并处理循环引用</span><span class="sxs-lookup"><span data-stu-id="c788a-105">Preserve references and handle circular references</span></span>

::: zone pivot="dotnet-5-0"

<span data-ttu-id="c788a-106">若要保留引用并处理循环引用，请将 <xref:System.Text.Json.JsonSerializerOptions.ReferenceHandler%2A> 设置为 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A>。</span><span class="sxs-lookup"><span data-stu-id="c788a-106">To preserve references and handle circular references, set <xref:System.Text.Json.JsonSerializerOptions.ReferenceHandler%2A> to <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A>.</span></span> <span data-ttu-id="c788a-107">此设置会导致以下行为：</span><span class="sxs-lookup"><span data-stu-id="c788a-107">This setting causes the following behavior:</span></span>

* <span data-ttu-id="c788a-108">在序列化时：</span><span class="sxs-lookup"><span data-stu-id="c788a-108">On serialize:</span></span>

  <span data-ttu-id="c788a-109">编写复杂类型时，序列化程序还会写入元数据属性（`$id`、`$values` 和 `$ref`）。</span><span class="sxs-lookup"><span data-stu-id="c788a-109">When writing complex types, the serializer also writes metadata properties (`$id`, `$values`, and `$ref`).</span></span>

* <span data-ttu-id="c788a-110">在反序列化时：</span><span class="sxs-lookup"><span data-stu-id="c788a-110">On deserialize:</span></span>

  <span data-ttu-id="c788a-111">需要元数据（虽然不是必需的），并且反序列化程序会尝试理解它。</span><span class="sxs-lookup"><span data-stu-id="c788a-111">Metadata is expected (although not mandatory), and the deserializer tries to understand it.</span></span>

<span data-ttu-id="c788a-112">下面的代码演示 `Preserve` 属性的用法。</span><span class="sxs-lookup"><span data-stu-id="c788a-112">The following code illustrates use of the `Preserve` setting.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/PreserveReferences.cs" highlight="34":::

<span data-ttu-id="c788a-113">此功能不能用于保留值类型或不可变类型。</span><span class="sxs-lookup"><span data-stu-id="c788a-113">This feature can't be used to preserve value types or immutable types.</span></span> <span data-ttu-id="c788a-114">在反序列化时，将在读取整个有效负载后创建不可变类型的实例。</span><span class="sxs-lookup"><span data-stu-id="c788a-114">On deserialization, the instance of an immutable type is created after the entire payload is read.</span></span> <span data-ttu-id="c788a-115">因此，如果对同一实例的引用出现在 JSON 有效负载中，则无法对其进行反序列化。</span><span class="sxs-lookup"><span data-stu-id="c788a-115">So it would be impossible to deserialize the same instance if a reference to it appears within the JSON payload.</span></span>

<span data-ttu-id="c788a-116">对于值类型、不可变类型和数组，不会序列化任何引用元数据。</span><span class="sxs-lookup"><span data-stu-id="c788a-116">For value types, immutable types, and arrays, no reference metadata is serialized.</span></span> <span data-ttu-id="c788a-117">反序列化时，如果发现 `$ref` 或 `$id`，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="c788a-117">On deserialization, an exception is thrown if `$ref` or `$id` is found.</span></span> <span data-ttu-id="c788a-118">但是，值类型忽略 `$id`（对于集合，则为 `$values`），以便可以反序列化使用 Newtonsoft.Json 序列化的有效负载。</span><span class="sxs-lookup"><span data-stu-id="c788a-118">However, value types ignore `$id` (and `$values` in the case of collections) to make it possible to deserialize payloads that were serialized by using Newtonsoft.Json.</span></span>  <span data-ttu-id="c788a-119">Newtonsoft.Json 为此类类型序列化元数据。</span><span class="sxs-lookup"><span data-stu-id="c788a-119">Newtonsoft.Json does serialize metadata for such types.</span></span>

<span data-ttu-id="c788a-120">为了确定对象是否相等，System.Text.Json 在比较两个对象实例时使用引用相等性 (<xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=nameWithType>) 而不是值相等性 (<xref:System.Object.Equals(System.Object)?displayProperty=nameWithType> 的 <xref:System.Collections.Generic.ReferenceEqualityComparer.Instance%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="c788a-120">To determine if objects are equal, System.Text.Json uses <xref:System.Collections.Generic.ReferenceEqualityComparer.Instance%2A?displayProperty=nameWithType>, which uses reference equality (<xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=nameWithType>) instead of value equality (<xref:System.Object.Equals(System.Object)?displayProperty=nameWithType> when comparing two object instances.</span></span>

<span data-ttu-id="c788a-121">有关如何序列化和反序列化引用的详细信息，请参阅 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="c788a-121">For more information about how references are serialized and deserialized, see <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A?displayProperty=nameWithType>.</span></span>

<span data-ttu-id="c788a-122"><xref:System.Text.Json.Serialization.ReferenceResolver> 类定义在序列化和反序列化过程中保留引用的行为。</span><span class="sxs-lookup"><span data-stu-id="c788a-122">The <xref:System.Text.Json.Serialization.ReferenceResolver> class defines the behavior of preserving references on serialization and deserialization.</span></span> <span data-ttu-id="c788a-123">创建派生类以指定自定义行为。</span><span class="sxs-lookup"><span data-stu-id="c788a-123">Create a derived class to specify custom behavior.</span></span> <span data-ttu-id="c788a-124">有关示例，请参阅 [GuidReferenceResolver](https://github.com/dotnet/docs/blob/9d5e88edbd7f12be463775ffebbf07ac8415fe18/docs/standard/serialization/snippets/system-text-json-how-to-5-0/csharp/GuidReferenceResolverExample.cs)。</span><span class="sxs-lookup"><span data-stu-id="c788a-124">For an example, see [GuidReferenceResolver](https://github.com/dotnet/docs/blob/9d5e88edbd7f12be463775ffebbf07ac8415fe18/docs/standard/serialization/snippets/system-text-json-how-to-5-0/csharp/GuidReferenceResolverExample.cs).</span></span>

::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="c788a-125">.NET Core 3.1 中的 System.Text.Json 仅支持按值进行进行序列化，并对循环引用引发异常。</span><span class="sxs-lookup"><span data-stu-id="c788a-125">System.Text.Json in .NET Core 3.1 only supports serialization by value and throws an exception for circular references.</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="c788a-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="c788a-126">See also</span></span>

* [<span data-ttu-id="c788a-127">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="c788a-127">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="c788a-128">实例化 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="c788a-128">Instantiate JsonSerializerOptions</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="c788a-129">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="c788a-129">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="c788a-130">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="c788a-130">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="c788a-131">忽略属性</span><span class="sxs-lookup"><span data-stu-id="c788a-131">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="c788a-132">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="c788a-132">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="c788a-133">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="c788a-133">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="c788a-134">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="c788a-134">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="c788a-135">多态序列化</span><span class="sxs-lookup"><span data-stu-id="c788a-135">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* <span data-ttu-id="c788a-136">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="c788a-136">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
