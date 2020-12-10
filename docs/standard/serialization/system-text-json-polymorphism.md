---
title: 如何使用 System.Text.Json 序列化派生类的属性
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何序列化多态对象。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 4b99a402ea4f4c664d3bfd75627ffaf94948d493
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439759"
---
# <a name="how-to-serialize-properties-of-derived-classes-with-no-locsystemtextjson"></a><span data-ttu-id="04ca2-103">如何使用 System.Text.Json 序列化派生类的属性</span><span class="sxs-lookup"><span data-stu-id="04ca2-103">How to serialize properties of derived classes with System.Text.Json</span></span>

<span data-ttu-id="04ca2-104">本文将介绍如何使用 `System.Text.Json` 命名空间序列化派生类的属性。</span><span class="sxs-lookup"><span data-stu-id="04ca2-104">In this article, you will learn how to serialize properties of derived classes with the `System.Text.Json` namespace.</span></span>

## <a name="serialize-properties-of-derived-classes"></a><span data-ttu-id="04ca2-105">序列化派生类的属性</span><span class="sxs-lookup"><span data-stu-id="04ca2-105">Serialize properties of derived classes</span></span>

<span data-ttu-id="04ca2-106">不支持多态类型层次结构的序列化。</span><span class="sxs-lookup"><span data-stu-id="04ca2-106">Serialization of a polymorphic type hierarchy is _not_ supported.</span></span> <span data-ttu-id="04ca2-107">例如，如果属性定义为接口或抽象类，则即使运行时类型具有其他属性，也只会序列化对接口或抽象类定义的属性。</span><span class="sxs-lookup"><span data-stu-id="04ca2-107">For example, if a property is defined as an interface or an abstract class, only the properties defined on the interface or abstract class are serialized, even if the runtime type has additional properties.</span></span> <span data-ttu-id="04ca2-108">此部分中介绍了此行为的例外情况。</span><span class="sxs-lookup"><span data-stu-id="04ca2-108">The exceptions to this behavior are explained in this section.</span></span>

<span data-ttu-id="04ca2-109">例如，假设有一个 `WeatherForecast` 类和一个派生类 `WeatherForecastDerived`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-109">For example, suppose you have a `WeatherForecast` class and a derived class `WeatherForecastDerived`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WFDerived":::

<span data-ttu-id="04ca2-110">并且假设 `Serialize` 方法的类型参数在编译时为 `WeatherForecast`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-110">And suppose the type argument of the `Serialize` method at compile time is `WeatherForecast`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializePolymorphic.cs" id="SerializeDefault":::

<span data-ttu-id="04ca2-111">在这种情况下，即使 `weatherForecast` 对象实际上是 `WeatherForecastDerived` 对象，也不会序列化 `WindSpeed` 属性。</span><span class="sxs-lookup"><span data-stu-id="04ca2-111">In this scenario, the `WindSpeed` property is not serialized even if the `weatherForecast` object is actually a `WeatherForecastDerived` object.</span></span> <span data-ttu-id="04ca2-112">仅序列化基类属性：</span><span class="sxs-lookup"><span data-stu-id="04ca2-112">Only the base class properties are serialized:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "Hot"
}
```

<span data-ttu-id="04ca2-113">此行为旨在帮助防止在运行时创建的派生类型中发生意外数据泄露。</span><span class="sxs-lookup"><span data-stu-id="04ca2-113">This behavior is intended to help prevent accidental exposure of data in a derived runtime-created type.</span></span>

<span data-ttu-id="04ca2-114">若要序列化前面示例中派生类型的属性，请使用以下方法之一：</span><span class="sxs-lookup"><span data-stu-id="04ca2-114">To serialize the properties of the derived type in the preceding example, use one of the following approaches:</span></span>

* <span data-ttu-id="04ca2-115">调用 <xref:System.Text.Json.JsonSerializer.Serialize%2A> 的重载，以便在运行时指定类型：</span><span class="sxs-lookup"><span data-stu-id="04ca2-115">Call an overload of <xref:System.Text.Json.JsonSerializer.Serialize%2A> that lets you specify the type at run time:</span></span>

  :::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializePolymorphic.cs" id="SerializeGetType":::

* <span data-ttu-id="04ca2-116">将要序列化的对象声明为 `object`。</span><span class="sxs-lookup"><span data-stu-id="04ca2-116">Declare the object to be serialized as `object`.</span></span>

  :::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializePolymorphic.cs" id="SerializeObject":::

<span data-ttu-id="04ca2-117">在前面的示例方案中，这两种方法都会使 `WindSpeed` 属性包含在 JSON 输出中：</span><span class="sxs-lookup"><span data-stu-id="04ca2-117">In the preceding example scenario, both approaches cause the `WindSpeed` property to be included in the JSON output:</span></span>

```json
{
  "WindSpeed": 35,
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "Hot"
}
```

> [!IMPORTANT]
> <span data-ttu-id="04ca2-118">这些方法只为要序列化的根对象提供多态序列化，而不为该根对象的属性提供。</span><span class="sxs-lookup"><span data-stu-id="04ca2-118">These approaches provide polymorphic serialization only for the root object to be serialized, not for properties of that root object.</span></span>

<span data-ttu-id="04ca2-119">如果将较低级别的对象定义为类型 `object`，则可以对它们进行多态序列化。</span><span class="sxs-lookup"><span data-stu-id="04ca2-119">You can get polymorphic serialization for lower-level objects if you define them as type `object`.</span></span> <span data-ttu-id="04ca2-120">例如，假设 `WeatherForecast` 类具有一个名为 `PreviousForecast` 的属性，该属性可以定义为类型 `WeatherForecast` 或 `object`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-120">For example, suppose your `WeatherForecast` class has a property named `PreviousForecast` that can be defined as type `WeatherForecast` or `object`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WFWithPrevious":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WFWithPreviousAsObject":::

<span data-ttu-id="04ca2-121">如果 `PreviousForecast` 属性包含 `WeatherForecastDerived` 的实例：</span><span class="sxs-lookup"><span data-stu-id="04ca2-121">If the `PreviousForecast` property contains an instance of `WeatherForecastDerived`:</span></span>

* <span data-ttu-id="04ca2-122">序列化 `WeatherForecastWithPrevious` 的 JSON 输出不包含 `WindSpeed`。</span><span class="sxs-lookup"><span data-stu-id="04ca2-122">The JSON output from serializing `WeatherForecastWithPrevious` **doesn't include** `WindSpeed`.</span></span>
* <span data-ttu-id="04ca2-123">序列化 `WeatherForecastWithPreviousAsObject` 的 JSON 输出包含 `WindSpeed`。</span><span class="sxs-lookup"><span data-stu-id="04ca2-123">The JSON output from serializing `WeatherForecastWithPreviousAsObject` **includes** `WindSpeed`.</span></span>

<span data-ttu-id="04ca2-124">若要序列化 `WeatherForecastWithPreviousAsObject`，无需调用 `Serialize<object>` 或 `GetType`，因为根对象不是可能属于派生类型的对象。</span><span class="sxs-lookup"><span data-stu-id="04ca2-124">To serialize `WeatherForecastWithPreviousAsObject`, it isn't necessary to call `Serialize<object>` or `GetType` because the root object isn't the one that may be of a derived type.</span></span> <span data-ttu-id="04ca2-125">下面的代码示例不调用 `Serialize<object>` 或 `GetType`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-125">The following code example doesn't call `Serialize<object>` or `GetType`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializePolymorphic.cs" id="SerializeSecondLevel":::

<span data-ttu-id="04ca2-126">前面的代码会正确地序列化 `WeatherForecastWithPreviousAsObject`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-126">The preceding code correctly serializes `WeatherForecastWithPreviousAsObject`:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "Hot",
  "PreviousForecast": {
    "WindSpeed": 35,
    "Date": "2019-08-01T00:00:00-07:00",
    "TemperatureCelsius": 25,
    "Summary": "Hot"
  }
}
```

<span data-ttu-id="04ca2-127">将属性定义为 `object` 的相同方法适用于接口。</span><span class="sxs-lookup"><span data-stu-id="04ca2-127">The same approach of defining properties as `object` works with interfaces.</span></span> <span data-ttu-id="04ca2-128">假设具有以下接口和实现，并且要使用包含实现实例的属性序列化类：</span><span class="sxs-lookup"><span data-stu-id="04ca2-128">Suppose you have the following interface and implementation, and you want to serialize a class with properties that contain implementation instances:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/IForecast.cs":::

<span data-ttu-id="04ca2-129">序列化 `Forecasts` 的实例时，只有 `Tuesday` 显示 `WindSpeed` 属性，因为 `Tuesday` 定义为 `object`：</span><span class="sxs-lookup"><span data-stu-id="04ca2-129">When you serialize an instance of `Forecasts`, only `Tuesday` shows the `WindSpeed` property, because `Tuesday` is defined as `object`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/SerializePolymorphic.cs" id="SerializeInterface":::

<span data-ttu-id="04ca2-130">下面的示例显示前面代码生成的 JSON：</span><span class="sxs-lookup"><span data-stu-id="04ca2-130">The following example shows the JSON that results from the preceding code:</span></span>

```json
{
  "Monday": {
    "Date": "2020-01-06T00:00:00-08:00",
    "TemperatureCelsius": 10,
    "Summary": "Cool"
  },
  "Tuesday": {
    "Date": "2020-01-07T00:00:00-08:00",
    "TemperatureCelsius": 11,
    "Summary": "Rainy",
    "WindSpeed": 10
  }
}
```

<span data-ttu-id="04ca2-131">有关多态序列化的详细信息，以及有关反序列化的信息，请参阅[如何从 Newtonsoft.Json 迁移到 System.Text.Json](system-text-json-migrate-from-newtonsoft-how-to.md#polymorphic-serialization)。</span><span class="sxs-lookup"><span data-stu-id="04ca2-131">For more information about polymorphic **serialization**, and for information about **deserialization**, see [How to migrate from Newtonsoft.Json to System.Text.Json](system-text-json-migrate-from-newtonsoft-how-to.md#polymorphic-serialization).</span></span>

## <a name="see-also"></a><span data-ttu-id="04ca2-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="04ca2-132">See also</span></span>

* [<span data-ttu-id="04ca2-133">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="04ca2-133">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="04ca2-134">实例化 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="04ca2-134">Instantiate JsonSerializerOptions</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="04ca2-135">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="04ca2-135">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="04ca2-136">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="04ca2-136">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="04ca2-137">忽略属性</span><span class="sxs-lookup"><span data-stu-id="04ca2-137">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="04ca2-138">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="04ca2-138">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="04ca2-139">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="04ca2-139">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="04ca2-140">保留循环引用</span><span class="sxs-lookup"><span data-stu-id="04ca2-140">Preserve circular references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="04ca2-141">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="04ca2-141">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* <span data-ttu-id="04ca2-142">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="04ca2-142">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
