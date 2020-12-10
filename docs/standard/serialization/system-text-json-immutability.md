---
title: 如何通过 System.Text.Json 使用不可变类型和非公共访问器
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何使用不可变类型和非公共访问器。
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
ms.openlocfilehash: d3e61d44ce22b7f50838b6d3ba9cf64004bd3725
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439756"
---
# <a name="how-to-use-immutable-types-and-non-public-accessors-with-no-locsystemtextjson"></a><span data-ttu-id="55710-103">如何通过 System.Text.Json 使用不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="55710-103">How to use immutable types and non-public accessors with System.Text.Json</span></span>

<span data-ttu-id="55710-104">本文将介绍如何通过 `System.Text.Json` 命名空间使用不可变类型（如“记录”）。</span><span class="sxs-lookup"><span data-stu-id="55710-104">In this article, you will learn how to use immutable types, such as Records, with the `System.Text.Json` namespace.</span></span>

## <a name="immutable-types-and-records"></a><span data-ttu-id="55710-105">不可变类型和记录</span><span class="sxs-lookup"><span data-stu-id="55710-105">Immutable types and Records</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="55710-106">`System.Text.Json` 可以使用参数化构造函数，这可以反序列化不可变的类或结构。</span><span class="sxs-lookup"><span data-stu-id="55710-106">`System.Text.Json` can use a parameterized constructor, which makes it possible to deserialize an immutable class or struct.</span></span> <span data-ttu-id="55710-107">对于类，如果唯一构造函数是参数化的构造函数，则将使用该构造函数。</span><span class="sxs-lookup"><span data-stu-id="55710-107">For a class, if the only constructor is a parameterized one, that constructor will be used.</span></span> <span data-ttu-id="55710-108">对于结构或包含多个构造函数的类，通过应用 [[JsonConstructor]](xref:System.Text.Json.Serialization.JsonConstructorAttribute.%23ctor%2A) 特性来指定要使用的构造函数。</span><span class="sxs-lookup"><span data-stu-id="55710-108">For a struct, or a class with multiple constructors, specify the one to use by applying the [[JsonConstructor]](xref:System.Text.Json.Serialization.JsonConstructorAttribute.%23ctor%2A) attribute.</span></span> <span data-ttu-id="55710-109">如果未使用该特性，则始终使用公共无参数构造函数（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="55710-109">When the attribute is not used, a public parameterless constructor is always used if present.</span></span> <span data-ttu-id="55710-110">该特性只能与公共构造函数一起使用。</span><span class="sxs-lookup"><span data-stu-id="55710-110">The attribute can only be used with public constructors.</span></span> <span data-ttu-id="55710-111">以下示例使用 `[JsonConstructor]` 特性：</span><span class="sxs-lookup"><span data-stu-id="55710-111">The following example uses the `[JsonConstructor]` attribute:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/ImmutableTypes.cs" highlight="13":::

<span data-ttu-id="55710-112">还支持 C# 9 记录，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="55710-112">Records in C# 9 are also supported, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/Records.cs":::

<span data-ttu-id="55710-113">对于因其所有属性资源库都是非公共的而不可变的类型，请参阅以下部分，了解[非公共属性访问器](#non-public-property-accessors)。</span><span class="sxs-lookup"><span data-stu-id="55710-113">For types that are immutable because all their property setters are non-public, see the following section about [non-public property accessors](#non-public-property-accessors).</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="55710-114">.NET Core 3.1 不支持 `JsonConstructorAttribute` 和 C# 9 记录。</span><span class="sxs-lookup"><span data-stu-id="55710-114">`JsonConstructorAttribute` and C# 9 Record support aren't available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="non-public-property-accessors"></a><span data-ttu-id="55710-115">非公共属性访问器</span><span class="sxs-lookup"><span data-stu-id="55710-115">Non-public property accessors</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="55710-116">若要允许使用非公共属性访问器，请使用 [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) 特性，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="55710-116">To enable use of a non-public property accessor, use the [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) attribute, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/NonPublicAccessors.cs" highlight="12,15":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="55710-117">.NET Core 3.1 不支持非公共属性访问器。</span><span class="sxs-lookup"><span data-stu-id="55710-117">Non-public property accessors are not supported in .NET Core 3.1.</span></span> <span data-ttu-id="55710-118">有关详细信息，请参阅[从 Newtonsoft.Json 迁移一文](system-text-json-migrate-from-newtonsoft-how-to.md#non-public-property-setters-and-getters)。</span><span class="sxs-lookup"><span data-stu-id="55710-118">For more information, see [the Migrate from Newtonsoft.Json article](system-text-json-migrate-from-newtonsoft-how-to.md#non-public-property-setters-and-getters).</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="55710-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="55710-119">See also</span></span>

* [<span data-ttu-id="55710-120">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="55710-120">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="55710-121">实例化 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="55710-121">Instantiate JsonSerializerOptions</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="55710-122">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="55710-122">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="55710-123">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="55710-123">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="55710-124">忽略属性</span><span class="sxs-lookup"><span data-stu-id="55710-124">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="55710-125">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="55710-125">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="55710-126">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="55710-126">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="55710-127">保留循环引用</span><span class="sxs-lookup"><span data-stu-id="55710-127">Preserve circular references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="55710-128">多态序列化</span><span class="sxs-lookup"><span data-stu-id="55710-128">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* <span data-ttu-id="55710-129">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="55710-129">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
