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
# <a name="how-to-instantiate-jsonserializeroptions-instances-with-no-locsystemtextjson"></a><span data-ttu-id="2f20c-103">如何使用 System.Text.Json 实例化 JsonSerializerOptions 实例</span><span class="sxs-lookup"><span data-stu-id="2f20c-103">How to instantiate JsonSerializerOptions instances with System.Text.Json</span></span>

<span data-ttu-id="2f20c-104">本文将介绍如何通过复制现有实例或使用 Web 默认值实例化 <xref:System.Text.Json.JsonSerializerOptions> 实例。</span><span class="sxs-lookup"><span data-stu-id="2f20c-104">In this article, you'll learn how to instantiate <xref:System.Text.Json.JsonSerializerOptions> instances by copying existing instances or with web defaults.</span></span>

## <a name="copy-jsonserializeroptions"></a><span data-ttu-id="2f20c-105">复制 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="2f20c-105">Copy JsonSerializerOptions</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="2f20c-106">存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerOptions)) ，可让你使用与现有实例相同的选项来创建新的实例，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="2f20c-106">There is a [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerOptions)) that lets you create a new instance with the same options as an existing instance, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/CopyOptions.cs" highlight="29":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="2f20c-107">使用现有实例的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。</span><span class="sxs-lookup"><span data-stu-id="2f20c-107">A `JsonSerializerOptions` constructor that takes an existing instance is not available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="web-defaults-for-jsonserializeroptions"></a><span data-ttu-id="2f20c-108">JsonSerializerOptions 的 Web 默认值</span><span class="sxs-lookup"><span data-stu-id="2f20c-108">Web defaults for JsonSerializerOptions</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="2f20c-109">下面是具有 Web 应用不同默认值的选项：</span><span class="sxs-lookup"><span data-stu-id="2f20c-109">Here are the options that have different defaults for web apps:</span></span>

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>
* <xref:System.Text.Json.JsonSerializerOptions.NumberHandling%2A> = <xref:System.Text.Json.Serialization.JsonNumberHandling.AllowReadingFromString>

<span data-ttu-id="2f20c-110">存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerDefaults)?view=net-5.0&preserve-view=true)，可让你通过 ASP.NET Core 对 Web 应用使用的默认选项创建新的实例，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="2f20c-110">There's a [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerDefaults)?view=net-5.0&preserve-view=true) that lets you create a new instance with the default options that ASP.NET Core uses for web apps, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/OptionsDefaults.cs" highlight="24":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="2f20c-111">下面是具有 Web 应用不同默认值的选项：</span><span class="sxs-lookup"><span data-stu-id="2f20c-111">Here are the options that have different defaults for web apps:</span></span>

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>

<span data-ttu-id="2f20c-112">指定一组默认值的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。</span><span class="sxs-lookup"><span data-stu-id="2f20c-112">A `JsonSerializerOptions` constructor that specifies a set of defaults is not available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="2f20c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f20c-113">See also</span></span>

* [<span data-ttu-id="2f20c-114">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="2f20c-114">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="2f20c-115">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="2f20c-115">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="2f20c-116">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="2f20c-116">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="2f20c-117">忽略属性</span><span class="sxs-lookup"><span data-stu-id="2f20c-117">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="2f20c-118">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="2f20c-118">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="2f20c-119">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="2f20c-119">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="2f20c-120">保留循环引用</span><span class="sxs-lookup"><span data-stu-id="2f20c-120">Preserve circular references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="2f20c-121">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="2f20c-121">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="2f20c-122">多态序列化</span><span class="sxs-lookup"><span data-stu-id="2f20c-122">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* <span data-ttu-id="2f20c-123">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="2f20c-123">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
