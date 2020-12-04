---
title: 运行时事件
description: 查看 .NET 运行时发出的诊断事件 (CoreCLR) ，该事件可与 ETW、LTTng 或 EventPipe 一起使用。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- runtime events (CoreCLR)
- ETW, EventPipe runtime events (CoreCLR)
ms.openlocfilehash: 33fa7275ce40934ce043b4d0dba5749c37515755
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "96591059"
---
# <a name="net-runtime-events"></a><span data-ttu-id="a16f7-103">.NET 运行时事件</span><span class="sxs-lookup"><span data-stu-id="a16f7-103">.NET runtime events</span></span>

<span data-ttu-id="a16f7-104">.NET 运行时 (CoreCLR) 发出各种事件，这些事件可用于诊断 .NET 应用程序的问题，这些事件可通过各种机制（例如 `ETW` 、 `LTTng` 和）使用 `EventPipe` 。</span><span class="sxs-lookup"><span data-stu-id="a16f7-104">The .NET runtime (CoreCLR) emits various events that can be used to diagnose issues with your .NET application that can be consumed via various mechanisms such as `ETW`, `LTTng`, and `EventPipe`.</span></span>

<span data-ttu-id="a16f7-105">本文档作为对 .NET Core 运行时激发的事件的引用。</span><span class="sxs-lookup"><span data-stu-id="a16f7-105">This document serves as a reference on the events that are fired by .NET Core runtime.</span></span>

<span data-ttu-id="a16f7-106">有关 .NET Framework 中的运行时事件，请参阅 [CLR ETW 事件](../../framework/performance/clr-etw-events.md)。</span><span class="sxs-lookup"><span data-stu-id="a16f7-106">For runtime events in .NET Framework, see [CLR ETW Events](../../framework/performance/clr-etw-events.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a16f7-107">在本节中</span><span class="sxs-lookup"><span data-stu-id="a16f7-107">In this section</span></span>

<span data-ttu-id="a16f7-108">[争用事件](runtime-contention-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-108">[Contention Events](runtime-contention-events.md)</span></span>\
<span data-ttu-id="a16f7-109">这些事件收集有关监视器锁争用的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-109">These events collect information about monitor lock contentions.</span></span>

<span data-ttu-id="a16f7-110">[垃圾回收事件](runtime-garbage-collection-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-110">[Garbage Collection Events](runtime-garbage-collection-events.md)</span></span>\
<span data-ttu-id="a16f7-111">这些事件可收集有关垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-111">These events collect information pertaining to garbage collection.</span></span> <span data-ttu-id="a16f7-112">它们有助于诊断和调试，包括确定垃圾回收执行的次数、垃圾回收期间释放的内存量等。</span><span class="sxs-lookup"><span data-stu-id="a16f7-112">They help in diagnostics and debugging, including determining how many times garbage collection was performed, how much memory was freed during garbage collection, etc.</span></span>

<span data-ttu-id="a16f7-113">[异常事件](runtime-exception-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-113">[Exception Events](runtime-exception-events.md)</span></span>\
<span data-ttu-id="a16f7-114">这些运行时事件捕获有关引发的异常的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-114">These runtime events capture information about exceptions that are thrown.</span></span>

<span data-ttu-id="a16f7-115">[互操作事件](runtime-interop-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-115">[Interop Events](runtime-interop-events.md)</span></span>\
<span data-ttu-id="a16f7-116">这些运行时事件捕获有关公共中间语言 (CIL) 存根生成的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-116">These runtime events capture information about Common Intermediate Language (CIL) stub generation.</span></span>

<span data-ttu-id="a16f7-117">[加载器和联编程序事件](runtime-loader-binder-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-117">[Loader and Binder Events](runtime-loader-binder-events.md)</span></span>\
<span data-ttu-id="a16f7-118">这些事件将收集与加载和卸载程序集和模块相关的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-118">These events collect information relating to loading and unloading assemblies and modules.</span></span>

<span data-ttu-id="a16f7-119">[方法事件](runtime-method-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-119">[Method Events](runtime-method-events.md)</span></span>\
<span data-ttu-id="a16f7-120">这些事件收集特定于方法的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-120">These events collect information that is specific to methods.</span></span> <span data-ttu-id="a16f7-121">符号解析需要这些事件的负载。</span><span class="sxs-lookup"><span data-stu-id="a16f7-121">The payload of these events is required for symbol resolution.</span></span> <span data-ttu-id="a16f7-122">此外，这些事件还提供如调用方法的次数等有用信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-122">In addition, these events provide helpful information such as the number of times a method was called.</span></span>

<span data-ttu-id="a16f7-123">[线程事件](runtime-thread-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-123">[Thread Events](runtime-thread-events.md)</span></span>\
<span data-ttu-id="a16f7-124">这些事件收集有关工作线程和 I/O 线程的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-124">These events collect information about worker and I/O threads.</span></span>

<span data-ttu-id="a16f7-125">[类型事件](runtime-type-events.md)</span><span class="sxs-lookup"><span data-stu-id="a16f7-125">[Type Events](runtime-type-events.md)</span></span>\
<span data-ttu-id="a16f7-126">这些事件收集有关类型系统的信息。</span><span class="sxs-lookup"><span data-stu-id="a16f7-126">These events collect information about the type system.</span></span>
