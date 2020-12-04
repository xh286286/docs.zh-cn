---
title: 类型系统运行时事件
description: 请参阅收集特定于 .NET 类型系统的诊断信息的 .NET 运行时事件，如 TypeLoadStart 和 TypeLoadStop。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- type system events (CoreCLR)
- ETW, EventPipe, LTTng type system events (CoreCLR)
ms.openlocfilehash: 8eee89cddb0098da2cb449a4be21945adac725e3
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "96591055"
---
# <a name="net-runtime-type-events"></a><span data-ttu-id="ff19d-103">.NET 运行时类型事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-103">.NET runtime type events</span></span>

<span data-ttu-id="ff19d-104">这些事件收集与加载类型相关的信息。</span><span class="sxs-lookup"><span data-stu-id="ff19d-104">These events collect information relating to loading types.</span></span> <span data-ttu-id="ff19d-105">有关如何将这些事件用于诊断的详细信息，请参阅 [日志记录和跟踪 .net 应用程序](../../core/diagnostics/logging-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="ff19d-105">For more information about how to use these events for diagnostic purposes, see [logging and tracing .NET applications](../../core/diagnostics/logging-tracing.md)</span></span>

## <a name="typeloadstart-event"></a><span data-ttu-id="ff19d-106">TypeLoadStart 事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-106">TypeLoadStart Event</span></span>

|<span data-ttu-id="ff19d-107">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff19d-107">Keyword for raising the event</span></span>|<span data-ttu-id="ff19d-108">事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-108">Event</span></span>|<span data-ttu-id="ff19d-109">Level</span><span class="sxs-lookup"><span data-stu-id="ff19d-109">Level</span></span>|  
|-----------------------------------|-----------|-----------|  
|<span data-ttu-id="ff19d-110">`TypeDiagnosticKeyword` (0x8000000000) </span><span class="sxs-lookup"><span data-stu-id="ff19d-110">`TypeDiagnosticKeyword` (0x8000000000)</span></span>|<span data-ttu-id="ff19d-111">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff19d-111">Informational (4)</span></span>|  

|<span data-ttu-id="ff19d-112">事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-112">Event</span></span>|<span data-ttu-id="ff19d-113">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff19d-113">Event ID</span></span>|<span data-ttu-id="ff19d-114">描述</span><span class="sxs-lookup"><span data-stu-id="ff19d-114">Description</span></span>|  
|-----------|--------------|-----------------|  
|`TypeLoadStart`|<span data-ttu-id="ff19d-115">73</span><span class="sxs-lookup"><span data-stu-id="ff19d-115">73</span></span>|<span data-ttu-id="ff19d-116">类型加载已开始。</span><span class="sxs-lookup"><span data-stu-id="ff19d-116">A type load has started.</span></span>|

|<span data-ttu-id="ff19d-117">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff19d-117">Field name</span></span>|<span data-ttu-id="ff19d-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff19d-118">Data type</span></span>|<span data-ttu-id="ff19d-119">说明</span><span class="sxs-lookup"><span data-stu-id="ff19d-119">Description</span></span>|  
|----------------|---------------|-----------------|  
|`TypeLoadStartID`|`win:UInt32`|<span data-ttu-id="ff19d-120">类型加载操作的 ID。</span><span class="sxs-lookup"><span data-stu-id="ff19d-120">ID for the type load operation.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff19d-121">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff19d-121">Unique ID for the instance of CLR or CoreCLR.</span></span>|  

## <a name="typeloadstop-event"></a><span data-ttu-id="ff19d-122">TypeLoadStop 事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-122">TypeLoadStop Event</span></span>

|<span data-ttu-id="ff19d-123">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff19d-123">Keyword for raising the event</span></span>|<span data-ttu-id="ff19d-124">Level</span><span class="sxs-lookup"><span data-stu-id="ff19d-124">Level</span></span>|  
|-----------------------------------|-----------|-----------|  
|<span data-ttu-id="ff19d-125">`TypeDiagnosticKeyword` (0x8000000000) </span><span class="sxs-lookup"><span data-stu-id="ff19d-125">`TypeDiagnosticKeyword` (0x8000000000)</span></span>|<span data-ttu-id="ff19d-126">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff19d-126">Informational (4)</span></span>|  

|<span data-ttu-id="ff19d-127">事件</span><span class="sxs-lookup"><span data-stu-id="ff19d-127">Event</span></span>|<span data-ttu-id="ff19d-128">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff19d-128">Event ID</span></span>|<span data-ttu-id="ff19d-129">描述</span><span class="sxs-lookup"><span data-stu-id="ff19d-129">Description</span></span>|  
|-----------|--------------|-----------------|  
|`TypeLoadStop`|<span data-ttu-id="ff19d-130">74</span><span class="sxs-lookup"><span data-stu-id="ff19d-130">74</span></span>|<span data-ttu-id="ff19d-131">类型加载已完成。</span><span class="sxs-lookup"><span data-stu-id="ff19d-131">A type load is finished.</span></span>|

|<span data-ttu-id="ff19d-132">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff19d-132">Field name</span></span>|<span data-ttu-id="ff19d-133">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff19d-133">Data type</span></span>|<span data-ttu-id="ff19d-134">说明</span><span class="sxs-lookup"><span data-stu-id="ff19d-134">Description</span></span>|  
|----------------|---------------|-----------------|  
|`TypeLoadStartID`|`win:UInt32`|<span data-ttu-id="ff19d-135">类型加载操作 (的 ID 与相应的 TypeLoadStart 事件的 TypeLoadStartID) 相匹配。</span><span class="sxs-lookup"><span data-stu-id="ff19d-135">ID for the type load operation (matches the corresponding TypeLoadStart event's TypeLoadStartID).</span></span>|
|`LoadLevel`|`win:UInt16`|<span data-ttu-id="ff19d-136">类型负载级别。</span><span class="sxs-lookup"><span data-stu-id="ff19d-136">Type load level.</span></span>|
|`TypeID`|`win:UInt64`|<span data-ttu-id="ff19d-137">指向该类型句柄的指针。</span><span class="sxs-lookup"><span data-stu-id="ff19d-137">Pointer to the type handle.</span></span>|
|`TypeName`|`win:UnicodeString`|<span data-ttu-id="ff19d-138">类型的名称。</span><span class="sxs-lookup"><span data-stu-id="ff19d-138">Name of the type.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff19d-139">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff19d-139">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
