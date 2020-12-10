---
title: BinaryFormatter 事件源
description: 了解如何使用 BinaryFormatter 事件源记录进行序列化或反序列化的时间。
ms.date: 12/03/2020
ms.author: levib
author: GrabYourPitchforks
ms.openlocfilehash: 9ae2af77b6cfc270207fb0f2969ada8c2eca1153
ms.sourcegitcommit: ecd9e9bb2225eb76f819722ea8b24988fe46f34c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "96740387"
---
# <a name="binaryformatter-event-source"></a><span data-ttu-id="971b8-103">BinaryFormatter 事件源</span><span class="sxs-lookup"><span data-stu-id="971b8-103">BinaryFormatter event source</span></span>

<span data-ttu-id="971b8-104">从 .NET 5.0 开始，<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> 包含内置的 <xref:System.Diagnostics.Tracing.EventSource>，你可通过此功能了解进行对象序列化或反序列化的时间。</span><span class="sxs-lookup"><span data-stu-id="971b8-104">Starting with .NET 5.0, <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> includes a built-in <xref:System.Diagnostics.Tracing.EventSource> that gives you visibility into when an object serialization or deserialization is occurring.</span></span> <span data-ttu-id="971b8-105">应用可以使用 <xref:System.Diagnostics.Tracing.EventListener> 派生的类型侦听这些通知，并进行记录。</span><span class="sxs-lookup"><span data-stu-id="971b8-105">Apps can use <xref:System.Diagnostics.Tracing.EventListener>-derived types to listen for these notifications and log them.</span></span>

<span data-ttu-id="971b8-106">此功能不能代替 <xref:System.Runtime.Serialization.SerializationBinder> 或 <xref:System.Runtime.Serialization.ISerializationSurrogate>，不能用于修改要序列化或反序列化的数据。</span><span class="sxs-lookup"><span data-stu-id="971b8-106">This functionality is not a substitute for a <xref:System.Runtime.Serialization.SerializationBinder> or an <xref:System.Runtime.Serialization.ISerializationSurrogate> and can't be used to modify the data being serialized or deserialized.</span></span> <span data-ttu-id="971b8-107">此事件系统用于深入了解要序列化或反序列化的类型。</span><span class="sxs-lookup"><span data-stu-id="971b8-107">Rather, this eventing system is intended to provide insight into the types being serialized or deserialized.</span></span> <span data-ttu-id="971b8-108">它还可用于检测对 `BinaryFormatter` 基础结构的意外调用，如来自第三方库代码的调用。</span><span class="sxs-lookup"><span data-stu-id="971b8-108">It can also be used to detect unintended calls into the `BinaryFormatter` infrastructure, such as calls originating from third-party library code.</span></span>

## <a name="description-of-events"></a><span data-ttu-id="971b8-109">事件说明</span><span class="sxs-lookup"><span data-stu-id="971b8-109">Description of events</span></span>

<span data-ttu-id="971b8-110">`BinaryFormatter` 事件源的已知名称为 `System.Runtime.Serialization.Formatters.Binary.BinaryFormatterEventSource`。</span><span class="sxs-lookup"><span data-stu-id="971b8-110">The `BinaryFormatter` event source has the well-known name `System.Runtime.Serialization.Formatters.Binary.BinaryFormatterEventSource`.</span></span> <span data-ttu-id="971b8-111">侦听器可以订阅 6 个事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-111">Listeners may subscribe to 6 events.</span></span>

### <a name="serializationstart-event-id--10"></a><span data-ttu-id="971b8-112">SerializationStart 事件（ID 为 `10`）</span><span class="sxs-lookup"><span data-stu-id="971b8-112">SerializationStart event (id = `10`)</span></span>

<span data-ttu-id="971b8-113">在 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Serialize%2A?displayProperty=nameWithType> 已调用并且序列化进程已启动时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-113">Raised when <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Serialize%2A?displayProperty=nameWithType> has been called and has started the serialization process.</span></span> <span data-ttu-id="971b8-114">此事件与 `SerializationEnd` 事件成对出现。</span><span class="sxs-lookup"><span data-stu-id="971b8-114">This event is paired with the `SerializationEnd` event.</span></span> <span data-ttu-id="971b8-115">对象在其自己的序列化例程中调用 `SerializationStart` 时，`BinaryFormatter.Serialize` 事件可以递归方式调用。</span><span class="sxs-lookup"><span data-stu-id="971b8-115">The `SerializationStart` event can be called recursively if an object calls `BinaryFormatter.Serialize` within its own serialization routine.</span></span>

<span data-ttu-id="971b8-116">此事件不包含有效负载。</span><span class="sxs-lookup"><span data-stu-id="971b8-116">This event doesn't contain a payload.</span></span>

### <a name="serializationend-event-id--11"></a><span data-ttu-id="971b8-117">SerializationEnd 事件（ID 为 `11`）</span><span class="sxs-lookup"><span data-stu-id="971b8-117">SerializationEnd event (id = `11`)</span></span>

<span data-ttu-id="971b8-118">在 `BinaryFormatter.Serialize` 已完成其工作时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-118">Raised when `BinaryFormatter.Serialize` has completed its work.</span></span> <span data-ttu-id="971b8-119">`SerializationEnd` 每次出现时，都表示最后一个未成对的 `SerializationStart` 事件完成。</span><span class="sxs-lookup"><span data-stu-id="971b8-119">Each occurrence of `SerializationEnd` denotes the completion of the last unpaired `SerializationStart` event.</span></span>

<span data-ttu-id="971b8-120">此事件不包含有效负载。</span><span class="sxs-lookup"><span data-stu-id="971b8-120">This event doesn't contain a payload.</span></span>

### <a name="serializingobject-event-id--12"></a><span data-ttu-id="971b8-121">SerializingObject 事件（ID 为 `12`）</span><span class="sxs-lookup"><span data-stu-id="971b8-121">SerializingObject event (id = `12`)</span></span>

<span data-ttu-id="971b8-122">在 `BinaryFormatter.Serialize` 正在序列化非基元类型时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-122">Raised when `BinaryFormatter.Serialize` is in the process of serializing a non-primitive type.</span></span> <span data-ttu-id="971b8-123">`BinaryFormatter` 基础结构会对某些类型（如 `string` 和 `int`）进行特殊处理，当它遇到这些类型时不会引发此事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-123">The `BinaryFormatter` infrastructure special-cases certain types (such as `string` and `int`) and doesn't raise this event when these types are encountered.</span></span> <span data-ttu-id="971b8-124">此事件将针对用户定义的类型和 `BinaryFormatter` 本机无法理解的其他类型引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-124">This event is raised for user-defined types and other types that `BinaryFormatter` doesn't natively understand.</span></span>

<span data-ttu-id="971b8-125">此事件可在 `SerializationStart` 和 `SerializationEnd` 事件之间引发零次或多次。</span><span class="sxs-lookup"><span data-stu-id="971b8-125">This event may be raised zero or more times between `SerializationStart` and `SerializationEnd` events.</span></span>

<span data-ttu-id="971b8-126">此事件包含有效负载，其中包括一个参数：</span><span class="sxs-lookup"><span data-stu-id="971b8-126">This event contains a payload with one argument:</span></span>

* <span data-ttu-id="971b8-127">`typeName` (`string`)：要序列化的类型的程序集限定名称（请参阅 <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType>）。</span><span class="sxs-lookup"><span data-stu-id="971b8-127">`typeName` (`string`): The assembly-qualified name (see <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType>) of the type being serialized.</span></span>

### <a name="deserializationstart-event-id--20"></a><span data-ttu-id="971b8-128">DeserializationStart 事件（ID 为 `20`）</span><span class="sxs-lookup"><span data-stu-id="971b8-128">DeserializationStart event (id = `20`)</span></span>

<span data-ttu-id="971b8-129">在 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize%2A?displayProperty=nameWithType> 已调用并且反序列化进程已启动时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-129">Raised when <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize%2A?displayProperty=nameWithType> has been called and has started the deserialization process.</span></span> <span data-ttu-id="971b8-130">此事件与 `DeserializationEnd` 事件成对出现。</span><span class="sxs-lookup"><span data-stu-id="971b8-130">This event is paired with the `DeserializationEnd` event.</span></span> <span data-ttu-id="971b8-131">对象在其自己的反序列化例程中调用 `DeserializationStart` 时，`BinaryFormatter.Deserialize` 事件可以递归方式调用。</span><span class="sxs-lookup"><span data-stu-id="971b8-131">The `DeserializationStart` event can be called recursively if an object calls `BinaryFormatter.Deserialize` within its own deserialization routine.</span></span>

<span data-ttu-id="971b8-132">此事件不包含有效负载。</span><span class="sxs-lookup"><span data-stu-id="971b8-132">This event doesn't contain a payload.</span></span>

### <a name="deserializationend-event-id--21"></a><span data-ttu-id="971b8-133">DeserializationEnd 事件（ID 为 `21`）</span><span class="sxs-lookup"><span data-stu-id="971b8-133">DeserializationEnd event (id = `21`)</span></span>

<span data-ttu-id="971b8-134">在 `BinaryFormatter.Deserialize` 已完成其工作时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-134">Raised when `BinaryFormatter.Deserialize` has completed its work.</span></span> <span data-ttu-id="971b8-135">`DeserializationEnd` 每次出现时，都表示最后一个未成对的 `DeserializationStart` 事件完成。</span><span class="sxs-lookup"><span data-stu-id="971b8-135">Each occurrence of `DeserializationEnd` denotes the completion of the last unpaired `DeserializationStart` event.</span></span>

<span data-ttu-id="971b8-136">此事件不包含有效负载。</span><span class="sxs-lookup"><span data-stu-id="971b8-136">This event doesn't contain a payload.</span></span>

### <a name="deserializingobject-event-id--22"></a><span data-ttu-id="971b8-137">DeserializingObject 事件（ID 为 `22`）</span><span class="sxs-lookup"><span data-stu-id="971b8-137">DeserializingObject event (id = `22`)</span></span>

<span data-ttu-id="971b8-138">在 `BinaryFormatter.Deserialize` 正在反序列化非基元类型时引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-138">Raised when `BinaryFormatter.Deserialize` is in the process of deserializing a non-primitive type.</span></span> <span data-ttu-id="971b8-139">`BinaryFormatter` 基础结构会对某些类型（如 `string` 和 `int`）进行特殊处理，当它遇到这些类型时不会引发此事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-139">The `BinaryFormatter` infrastructure special-cases certain types (such as `string` and `int`) and doesn't raise this event when these types are encountered.</span></span> <span data-ttu-id="971b8-140">此事件将针对用户定义的类型和 `BinaryFormatter` 本机无法理解的其他类型引发。</span><span class="sxs-lookup"><span data-stu-id="971b8-140">This event is raised for user-defined types and other types that `BinaryFormatter` doesn't natively understand.</span></span>

<span data-ttu-id="971b8-141">此事件可在 `DeserializationStart` 和 `DeserializationEnd` 事件之间引发零次或多次。</span><span class="sxs-lookup"><span data-stu-id="971b8-141">This event may be raised zero or more times between `DeserializationStart` and `DeserializationEnd` events.</span></span>

<span data-ttu-id="971b8-142">此事件包含有效负载，其中包括一个参数。</span><span class="sxs-lookup"><span data-stu-id="971b8-142">This event contains a payload with one argument.</span></span>

* <span data-ttu-id="971b8-143">`typeName` (`string`)：要反序列化的类型的程序集限定名称（请参阅 <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType>）。</span><span class="sxs-lookup"><span data-stu-id="971b8-143">`typeName` (`string`): The assembly-qualified name (see <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType>) of the type being deserialized.</span></span>

### <a name="advanced-subscribing-to-a-subset-of-notifications"></a><span data-ttu-id="971b8-144">\[高级\] 订阅部分通知</span><span class="sxs-lookup"><span data-stu-id="971b8-144">\[Advanced\] Subscribing to a subset of notifications</span></span>

<span data-ttu-id="971b8-145">仅需要订阅部分通知的侦听器可以选择要启用的关键字。</span><span class="sxs-lookup"><span data-stu-id="971b8-145">Listeners who wish to subscribe to only a subset of notifications can choose which keywords to enable.</span></span>

* <span data-ttu-id="971b8-146">`Serialization` = `(EventKeywords)1`：引发 `SerializationStart`、`SerializationEnd` 和 `SerializingObject` 事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-146">`Serialization` = `(EventKeywords)1`: Raises the `SerializationStart`, `SerializationEnd`, and `SerializingObject` events.</span></span>
* <span data-ttu-id="971b8-147">`Deserialization` = `(EventKeywords)2`：引发 `DeserializationStart`、`DeserializationEnd` 和 `DeserializingObject` 事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-147">`Deserialization` = `(EventKeywords)2`: Raises the `DeserializationStart`, `DeserializationEnd`, and `DeserializingObject` events.</span></span>

<span data-ttu-id="971b8-148">如果在 `EventListener` 注册过程中未提供关键字筛选器，则系统将引发所有事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-148">If no keyword filters are provided during `EventListener` registration, all events are raised.</span></span>

<span data-ttu-id="971b8-149">有关详细信息，请参阅 <xref:System.Diagnostics.Tracing.EventKeywords?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="971b8-149">For more information, see <xref:System.Diagnostics.Tracing.EventKeywords?displayProperty=nameWithType>.</span></span>

## <a name="sample-code"></a><span data-ttu-id="971b8-150">示例代码</span><span class="sxs-lookup"><span data-stu-id="971b8-150">Sample code</span></span>

<span data-ttu-id="971b8-151">下面的代码：</span><span class="sxs-lookup"><span data-stu-id="971b8-151">The following code:</span></span>

- <span data-ttu-id="971b8-152">创建将写入 `System.Console` 的 `EventListener` 派生的类型，</span><span class="sxs-lookup"><span data-stu-id="971b8-152">creates an `EventListener`-derived type that writes to `System.Console`,</span></span>
- <span data-ttu-id="971b8-153">为该侦听器订阅 `BinaryFormatter` 生成的通知，</span><span class="sxs-lookup"><span data-stu-id="971b8-153">subscribes that listener to `BinaryFormatter`-produced notifications,</span></span>
- <span data-ttu-id="971b8-154">使用 `BinaryFormatter` 序列化和反序列化简单的对象图，并</span><span class="sxs-lookup"><span data-stu-id="971b8-154">serializes and deserializes a simple object graph using `BinaryFormatter`, and</span></span>
- <span data-ttu-id="971b8-155">分析已引发的事件。</span><span class="sxs-lookup"><span data-stu-id="971b8-155">analyzes the events that have been raised.</span></span>

:::code language="csharp" source="snippets/binaryformatter-event-source/csharp/Program.cs":::

<span data-ttu-id="971b8-156">上面的代码生成的输出与下面的示例相似：</span><span class="sxs-lookup"><span data-stu-id="971b8-156">The preceding code produces output similar to the following example:</span></span>

```output
Event SerializationStart (id=10) received.
Event SerializingObject (id=12) received.
typeName = BinaryFormatterEventSample.Person, BinaryFormatterEventSample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null
Event SerializingObject (id=12) received.
typeName = BinaryFormatterEventSample.Book, BinaryFormatterEventSample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null
Event SerializationStop (id=11) received.
Event DeserializationStart (id=20) received.
Event DeserializingObject (id=22) received.
typeName = BinaryFormatterEventSample.Person, BinaryFormatterEventSample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null
Event DeserializingObject (id=22) received.
typeName = BinaryFormatterEventSample.Book, BinaryFormatterEventSample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null
Event DeserializationStop (id=21) received.
Rehydrated person Logan Edwards
Favorite book: A Tale of Two Cities by Charles Dickens, list price 10.25
```

<span data-ttu-id="971b8-157">在此示例中，基于控制台的 `EventListener` 将对序列化启动、`Person` 和 `Book` 的实例序列化以及序列化完成进行记录。</span><span class="sxs-lookup"><span data-stu-id="971b8-157">In this sample, the console-based `EventListener` logs that serialization starts, instances of `Person` and `Book` are serialized, and then serialization completes.</span></span> <span data-ttu-id="971b8-158">同样，反序列化启动后，`Person` 和 `Book` 的实例将进行反序列化，然后反序列化完成。</span><span class="sxs-lookup"><span data-stu-id="971b8-158">Similarly, once deserialization has started, instances of `Person` and `Book` are deserialized, and then deserialization completes.</span></span>

<span data-ttu-id="971b8-159">然后，应用将打印已反序列化的 `Person` 中包含的值，以证明对象确实已正确地进行序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="971b8-159">The app then prints the values contained in the deserialized `Person` to demonstrate that the object did in fact serialize and deserialize properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="971b8-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="971b8-160">See also</span></span>

<span data-ttu-id="971b8-161">有关使用 `EventListener` 接收基于 `EventSource` 的通知的详细信息，请参阅 [`EventListener` 类](xref:System.Diagnostics.Tracing.EventListener)。</span><span class="sxs-lookup"><span data-stu-id="971b8-161">For more information on using `EventListener` to receive `EventSource`-based notifications, see [the `EventListener` class](xref:System.Diagnostics.Tracing.EventListener).</span></span>
