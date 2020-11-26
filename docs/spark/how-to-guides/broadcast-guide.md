---
title: 在 .NET for Apache Spark 中使用广播变量
description: 了解如何在 .NET for Apache Spark 应用程序中使用广播变量。
ms.author: nidutta
author: Niharikadutta
ms.date: 10/09/2020
ms.topic: conceptual
ms.custom: mvc,how-to
ms.openlocfilehash: ca6dab01cbd639594da0b51f145272a9a150e93c
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94687748"
---
# <a name="use-broadcast-variables-in-net-for-apache-spark"></a><span data-ttu-id="be4cd-103">在 .NET for Apache Spark 中使用广播变量</span><span class="sxs-lookup"><span data-stu-id="be4cd-103">Use broadcast variables in .NET for Apache Spark</span></span>

<span data-ttu-id="be4cd-104">本文介绍如何在 .NET for Apache Spark 中使用广播变量。</span><span class="sxs-lookup"><span data-stu-id="be4cd-104">In this article, you learn how to use broadcast variables in .NET for Apache Spark.</span></span> <span data-ttu-id="be4cd-105">[Apache Spark 中的广播变量](https://spark.apache.org/docs/2.2.0/rdd-programming-guide.html#broadcast-variables)是一种机制，可实现在应为只读的执行程序之间共享变量。</span><span class="sxs-lookup"><span data-stu-id="be4cd-105">[Broadcast variables in Apache Spark](https://spark.apache.org/docs/2.2.0/rdd-programming-guide.html#broadcast-variables) are mechanisms for sharing variables across executors that are meant to be read-only.</span></span> <span data-ttu-id="be4cd-106">借助广播变量即可在每台计算机上缓存只读变量，无需将其副本与任务一起交付。</span><span class="sxs-lookup"><span data-stu-id="be4cd-106">Broadcast variables allow you to keep a read-only variable cached on each machine rather than shipping a copy of it with tasks.</span></span> <span data-ttu-id="be4cd-107">可以使用广播变量高效地为每个节点提供大型输入数据集的副本。</span><span class="sxs-lookup"><span data-stu-id="be4cd-107">You can use broadcast variables to give every node a copy of a large input dataset in an efficient manner.</span></span>

<span data-ttu-id="be4cd-108">由于数据仅发送一次，因此相较于随每个任务一起交付给执行程序的局部变量，广播变量具有性能优势。</span><span class="sxs-lookup"><span data-stu-id="be4cd-108">Because the data is sent only once, broadcast variables have performance benefits when compared to local variables that are shipped to the executors with each task.</span></span> <span data-ttu-id="be4cd-109">请参阅[官方广播变量文档](https://spark.apache.org/docs/2.2.0/rdd-programming-guide.html#broadcast-variables)，更深入地了解广播变量及其使用原因。</span><span class="sxs-lookup"><span data-stu-id="be4cd-109">Refer to the [official broadcast variable documentation](https://spark.apache.org/docs/2.2.0/rdd-programming-guide.html#broadcast-variables) to get a deeper understanding of broadcast variables and why they are used.</span></span>

## <a name="create-broadcast-variables"></a><span data-ttu-id="be4cd-110">创建广播变量</span><span class="sxs-lookup"><span data-stu-id="be4cd-110">Create broadcast variables</span></span>

<span data-ttu-id="be4cd-111">若要创建广播变量，请为任何变量 `v` 调用 `SparkContext.Broadcast(v)`。</span><span class="sxs-lookup"><span data-stu-id="be4cd-111">To create a broadcast variable, call `SparkContext.Broadcast(v)` for any variable `v`.</span></span> <span data-ttu-id="be4cd-112">广播变量是以变量 `v` 为中心的包装器，可以通过调用 `Value()` 方法访问它的值。</span><span class="sxs-lookup"><span data-stu-id="be4cd-112">The broadcast variable is a wrapper around the variable `v`, and its value can be accessed by calling the `Value()` method.</span></span>

<span data-ttu-id="be4cd-113">在以下代码片段中，创建了字符串变量 `v`，并在调用 `SparkContext.Broadcast(v)` 时创建了广播变量 `bv`。</span><span class="sxs-lookup"><span data-stu-id="be4cd-113">In the following code snippet, a string variable `v` is created, and a broadcast variable `bv` is created when `SparkContext.Broadcast(v)`is called.</span></span> <span data-ttu-id="be4cd-114">请注意，`Broadcast` 的类型参数（即字符串）与广播的变量的类型匹配。</span><span class="sxs-lookup"><span data-stu-id="be4cd-114">Notice the type parameter for `Broadcast`, string, matches the type of the variable being broadcasted.</span></span> <span data-ttu-id="be4cd-115">用户定义的函数 (UDF) 返回 `bv` 的值。</span><span class="sxs-lookup"><span data-stu-id="be4cd-115">The user-defined function (UDF) returns the value of `bv`.</span></span>

```csharp
string v = "Variable to be broadcasted";
Broadcast<string> bv = SparkContext.Broadcast(v);

Func<Column, Column> udf = Udf<string, string>(
    str => $"{str}: {bv.Value()}");
```

## <a name="delete-broadcast-variables"></a><span data-ttu-id="be4cd-116">删除广播变量</span><span class="sxs-lookup"><span data-stu-id="be4cd-116">Delete broadcast variables</span></span>

<span data-ttu-id="be4cd-117">可以通过调用 `Destroy()` 方法从所有执行程序中删除广播变量。</span><span class="sxs-lookup"><span data-stu-id="be4cd-117">The broadcast variable can be deleted from all executors by calling the `Destroy()` method.</span></span>

```csharp
bv.Destroy();
```

<span data-ttu-id="be4cd-118">`Destroy()` 可删除与广播变量相关的所有数据和元数据，应谨慎使用。</span><span class="sxs-lookup"><span data-stu-id="be4cd-118">`Destroy()` deletes all data and metadata related to the broadcast variable and should be used with caution.</span></span> <span data-ttu-id="be4cd-119">广播变量一经销毁，即无法再次使用。</span><span class="sxs-lookup"><span data-stu-id="be4cd-119">Once a broadcast variable is destroyed, it can't be used again.</span></span>

## <a name="limit-broadcast-variable-scope-in-udfs"></a><span data-ttu-id="be4cd-120">在 UDF 中限制广播变量范围</span><span class="sxs-lookup"><span data-stu-id="be4cd-120">Limit broadcast variable scope in UDFs</span></span>

<span data-ttu-id="be4cd-121">在 UDF 中使用广播变量时，需要将变量的范围限制为仅引用该变量的 UDF。</span><span class="sxs-lookup"><span data-stu-id="be4cd-121">When you use broadcast variables in UDFs, you need to limit the scope of the variable to only the UDF that is referencing the variable.</span></span> <span data-ttu-id="be4cd-122">[UDF 使用指南](udf-guide.md)详细描述了这一现象。</span><span class="sxs-lookup"><span data-stu-id="be4cd-122">The [guide to using UDFs](udf-guide.md) describes this phenomenon in detail.</span></span> <span data-ttu-id="be4cd-123">对广播变量调用 `Destroy()` 时，范围特别重要。</span><span class="sxs-lookup"><span data-stu-id="be4cd-123">Scope is especially crucial when you call `Destroy()` on the broadcast variable.</span></span>

<span data-ttu-id="be4cd-124">如果已销毁的广播变量对其他 UDF 可见或可通过其他 UDF 访问，则即使所有 UDF 未对其进行引用，也会将其选中进行序列化。</span><span class="sxs-lookup"><span data-stu-id="be4cd-124">If the broadcast variable that has been destroyed is visible to or accessible from other UDFs, it gets picked up for serialization by all of the UDFs, even if it is not being referenced by them.</span></span> <span data-ttu-id="be4cd-125">.NET for Apache Spark 无法序列化已销毁的广播变量，进而导致错误。</span><span class="sxs-lookup"><span data-stu-id="be4cd-125">.NET for Apache Spark is unable to serialize the destroyed broadcast variable, which results in an error.</span></span> <span data-ttu-id="be4cd-126">下面的代码片段演示了这一错误：</span><span class="sxs-lookup"><span data-stu-id="be4cd-126">The following code snippet demonstrates this error:</span></span>

```csharp
string v = "Variable to be broadcasted";
Broadcast<string> bv = SparkContext.Broadcast(v);

// Using the broadcast variable in a UDF:
Func<Column, Column> udf1 = Udf<string, string>(
    str => $"{str}: {bv.Value()}");

// Destroying bv
bv.Destroy();

// Calling udf1 after destroying bv throws the following expected exception:
// org.apache.spark.SparkException: Attempted to use Broadcast(0) after it was destroyed
df.Select(udf1(df["_1"])).Show();

// Different UDF udf2 that is not referencing bv
Func<Column, Column> udf2 = Udf<string, string>(
    str => $"{str}: not referencing broadcast variable");

// Calling udf2 throws the following (unexpected) exception:
// [Error] [JvmBridge] org.apache.spark.SparkException: Task not serializable
df.Select(udf2(df["_1"])).Show();
```

<span data-ttu-id="be4cd-127">下面的代码片段演示了如何确保销毁 `bv` 不会由于意外的序列化行为而影响 `udf2`：</span><span class="sxs-lookup"><span data-stu-id="be4cd-127">The following code snippet demonstrates how to ensure that destroying `bv` doesn't affect `udf2` because of an unexpected serialization behavior:</span></span>

```csharp
string v = "Variable to be broadcasted";
// Restricting the visibility of bv to only the UDF referencing it
{
    Broadcast<string> bv = SparkContext.Broadcast(v);

    // Using the broadcast variable in a UDF:
    Func<Column, Column> udf1 = Udf<string, string>(
        str => $"{str}: {bv.Value()}");

    // Destroying bv
    bv.Destroy();
}

// Different UDF udf2 that is not referencing bv
Func<Column, Column> udf2 = Udf<string, string>(
    str => $"{str}: not referencing broadcast variable");

// Calling udf2 works fine as expected
df.Select(udf2(df["_1"])).Show();
```

## <a name="faqs"></a><span data-ttu-id="be4cd-128">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="be4cd-128">FAQs</span></span>

<span data-ttu-id="be4cd-129">**为什么广播变量无法与 .NET Interactive 一起使用？**</span><span class="sxs-lookup"><span data-stu-id="be4cd-129">**Why don't Broadcast Variables work with .NET Interactive?**</span></span>  
<span data-ttu-id="be4cd-130">广播变量不能与交互式方案一起使用的原因在于，.NET 交互窗口的设计会将单元格中定义的每个对象都追加到其单元格提交类中，这是因为未标记为可序列化，因此失败，并出现如前所示的同一异常。</span><span class="sxs-lookup"><span data-stu-id="be4cd-130">Broadcast variables don't work with interactive scenarios because of .NET interactive's design of appending each object defined in a cell with its cell submission class, which since is not marked serializable, fails with the same exception as shown previously.</span></span> <span data-ttu-id="be4cd-131">有关详细信息，请查看[此文章](dotnet-interactive-udf-issue.md)。</span><span class="sxs-lookup"><span data-stu-id="be4cd-131">For more information, please check out [this article](dotnet-interactive-udf-issue.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="be4cd-132">后续步骤</span><span class="sxs-lookup"><span data-stu-id="be4cd-132">Next steps</span></span>

* [<span data-ttu-id="be4cd-133">.NET for Apache Spark 入门</span><span class="sxs-lookup"><span data-stu-id="be4cd-133">Get started with .NET for Apache Spark</span></span>](../tutorials/get-started.md)
* [<span data-ttu-id="be4cd-134">在 Windows 上调试 .NET for Apache Spark 应用程序</span><span class="sxs-lookup"><span data-stu-id="be4cd-134">Debug a .NET for Apache Spark application on Windows</span></span>](debug.md)
* [<span data-ttu-id="be4cd-135">部署 .NET for Apache Spark 辅助角色和用户定义的函数二进制文件</span><span class="sxs-lookup"><span data-stu-id="be4cd-135">Deploy .NET for Apache Spark worker and user-defined function binaries</span></span>](deploy-worker-udf-binaries.md)
