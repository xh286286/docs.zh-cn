---
title: 垃圾回收运行时事件
description: 请参阅收集特定于 .NET 垃圾回收器的诊断信息的 .NET 运行时事件。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- GC events
- garbage collection events (CoreCLR)
- ETW, EventPipe, LTTng garbage collection events (CoreCLR)
ms.openlocfilehash: 2799a93f351baf23ec7a359b0b4b2be5c216dc4d
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "96591061"
---
# <a name="net-runtime-garbage-collection-events"></a><span data-ttu-id="c32b7-103">.NET 运行时垃圾回收事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-103">.NET runtime garbage collection events</span></span>

<span data-ttu-id="c32b7-104">这些事件可收集有关垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="c32b7-104">These events collect information pertaining to garbage collection.</span></span> <span data-ttu-id="c32b7-105">它们有助于诊断和调试，包括确定垃圾回收执行的次数、垃圾回收期间释放的内存量等。有关如何将这些事件用于诊断的详细信息，请参阅 [日志记录和跟踪 .net 应用程序](../../core/diagnostics/logging-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="c32b7-105">They help in diagnostics and debugging, including determining how many times garbage collection was performed, how much memory was freed during garbage collection, etc. For more information about how to use these events for diagnostic purposes, see [logging and tracing .NET applications](../../core/diagnostics/logging-tracing.md)</span></span>

## <a name="gcstart_v2-event"></a><span data-ttu-id="c32b7-106">GCStart_V2 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-106">GCStart_V2 Event</span></span>

<span data-ttu-id="c32b7-107">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-107">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-108">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-108">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-109">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-109">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-110">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-110">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-111">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-111">Informational (4)</span></span>|

<span data-ttu-id="c32b7-112">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-112">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-113">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-113">Event</span></span>|<span data-ttu-id="c32b7-114">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-114">Event ID</span></span>|<span data-ttu-id="c32b7-115">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-115">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCStart_V1`|<span data-ttu-id="c32b7-116">1</span><span class="sxs-lookup"><span data-stu-id="c32b7-116">1</span></span>|<span data-ttu-id="c32b7-117">垃圾回收已启动。</span><span class="sxs-lookup"><span data-stu-id="c32b7-117">A garbage collection has started.</span></span>|

<span data-ttu-id="c32b7-118">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-118">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-119">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-119">Field name</span></span>|<span data-ttu-id="c32b7-120">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-120">Data type</span></span>|<span data-ttu-id="c32b7-121">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-121">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt32`|<span data-ttu-id="c32b7-122">第 *n* 代垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-122">The *n* th garbage collection.</span></span>|
|`Depth`|`win:UInt32`|<span data-ttu-id="c32b7-123">正在回收的代。</span><span class="sxs-lookup"><span data-stu-id="c32b7-123">The generation that is being collected.</span></span>|
|`Reason`|`win:UInt32`|<span data-ttu-id="c32b7-124">垃圾回收的触发原因：</span><span class="sxs-lookup"><span data-stu-id="c32b7-124">Why the garbage collection was triggered:</span></span><br /><br /> <span data-ttu-id="c32b7-125">`0x0` -小对象堆分配。</span><span class="sxs-lookup"><span data-stu-id="c32b7-125">`0x0` - Small object heap allocation.</span></span><br /><br /> <span data-ttu-id="c32b7-126">`0x1` 触发.</span><span class="sxs-lookup"><span data-stu-id="c32b7-126">`0x1` - Induced.</span></span><br /><br /> <span data-ttu-id="c32b7-127">`0x2` -内存不足。</span><span class="sxs-lookup"><span data-stu-id="c32b7-127">`0x2` - Low memory.</span></span><br /><br /> <span data-ttu-id="c32b7-128">`0x3` 空白处.</span><span class="sxs-lookup"><span data-stu-id="c32b7-128">`0x3` - Empty.</span></span><br /><br /> <span data-ttu-id="c32b7-129">`0x4` -大型对象堆分配。</span><span class="sxs-lookup"><span data-stu-id="c32b7-129">`0x4` - Large object heap allocation.</span></span><br /><br /> <span data-ttu-id="c32b7-130">`0x5` (小对象堆) 空间不足。</span><span class="sxs-lookup"><span data-stu-id="c32b7-130">`0x5` - Out of space (for small object heap).</span></span><br /><br /> <span data-ttu-id="c32b7-131">`0x6` 对于大型对象堆)  (空间不足。</span><span class="sxs-lookup"><span data-stu-id="c32b7-131">`0x6` - Out of space (for large object heap).</span></span><br /><br /> <span data-ttu-id="c32b7-132">`0x7` -已引发，但未强制为阻止。</span><span class="sxs-lookup"><span data-stu-id="c32b7-132">`0x7` - Induced but not forced as blocking.</span></span>|
|`Type`|`win:UInt32`|<span data-ttu-id="c32b7-133">`0x0` -在后台垃圾回收外部发生了阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-133">`0x0` - Blocking garbage collection occurred outside background garbage collection.</span></span><br /><br /> <span data-ttu-id="c32b7-134">`0x1` -后台垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-134">`0x1` - Background garbage collection.</span></span><br /><br /> <span data-ttu-id="c32b7-135">`0x2` -在后台垃圾回收期间发生了阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-135">`0x2` - Blocking garbage collection occurred during background garbage collection.</span></span>|
|`ClrInstanceID`|<span data-ttu-id="c32b7-136">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-136">win:UInt16</span></span>|<span data-ttu-id="c32b7-137">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-137">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gcend_v1-event"></a><span data-ttu-id="c32b7-138">GCEnd_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-138">GCEnd_V1 Event</span></span>

<span data-ttu-id="c32b7-139">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-139">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-140">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-140">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-141">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-141">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-142">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-142">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-143">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-143">Informational (4)</span></span>|

<span data-ttu-id="c32b7-144">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-144">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-145">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-145">Event</span></span>|<span data-ttu-id="c32b7-146">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-146">Event ID</span></span>|<span data-ttu-id="c32b7-147">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-147">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCEnd_V1`|<span data-ttu-id="c32b7-148">2</span><span class="sxs-lookup"><span data-stu-id="c32b7-148">2</span></span>|<span data-ttu-id="c32b7-149">垃圾回收已结束。</span><span class="sxs-lookup"><span data-stu-id="c32b7-149">The garbage collection has ended.</span></span>|

<span data-ttu-id="c32b7-150">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-150">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-151">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-151">Field name</span></span>|<span data-ttu-id="c32b7-152">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-152">Data type</span></span>|<span data-ttu-id="c32b7-153">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-153">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt32`|<span data-ttu-id="c32b7-154">第 *n* 代垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-154">The *n* th garbage collection.</span></span>|
|`Depth`|`win:UInt32`|<span data-ttu-id="c32b7-155">已回收的代。</span><span class="sxs-lookup"><span data-stu-id="c32b7-155">The generation that was collected.</span></span>|
|`ClrInstanceID`|<span data-ttu-id="c32b7-156">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-156">win:UInt16</span></span>|<span data-ttu-id="c32b7-157">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-157">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gcheapstats_v2-event"></a><span data-ttu-id="c32b7-158">GCHeapStats_V2 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-158">GCHeapStats_V2 Event</span></span>

<span data-ttu-id="c32b7-159">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-159">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-160">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-160">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-161">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-161">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-162">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-162">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-163">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-163">Informational (4)</span></span>|

<span data-ttu-id="c32b7-164">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-164">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-165">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-165">Event</span></span>|<span data-ttu-id="c32b7-166">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-166">Event ID</span></span>|<span data-ttu-id="c32b7-167">描述</span><span class="sxs-lookup"><span data-stu-id="c32b7-167">Description</span></span>|
|-----------|--------------|-----------------|
|`GCHeapStats_V2`|<span data-ttu-id="c32b7-168">4</span><span class="sxs-lookup"><span data-stu-id="c32b7-168">4</span></span>|<span data-ttu-id="c32b7-169">在每次垃圾回收结束时显示堆统计信息。</span><span class="sxs-lookup"><span data-stu-id="c32b7-169">Shows the heap statistics at the end of each garbage collection.</span></span>|

<span data-ttu-id="c32b7-170">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-170">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-171">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-171">Field name</span></span>|<span data-ttu-id="c32b7-172">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-172">Data type</span></span>|<span data-ttu-id="c32b7-173">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-173">Description</span></span>|
|----------------|---------------|-----------------|
|`GenerationSize0`|`win:UInt64`|<span data-ttu-id="c32b7-174">第 0 代内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-174">The size, in bytes, of generation 0 memory.</span></span>|
|`TotalPromotedSize0`|`win:UInt64`|<span data-ttu-id="c32b7-175">从第 0 代提升到第 1 代的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-175">The number of bytes that are promoted from generation 0 to generation 1.</span></span>|
|`GenerationSize1`|`win:UInt64`|<span data-ttu-id="c32b7-176">第 1 代内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-176">The size, in bytes, of generation 1 memory.</span></span>|
|`TotalPromotedSize1`|`win:UInt64`|<span data-ttu-id="c32b7-177">从第 1 代提升到第 2 代的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-177">The number of bytes that are promoted from generation 1 to generation 2.</span></span>|
|`GenerationSize2`|`win:UInt64`|<span data-ttu-id="c32b7-178">第 2 代内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-178">The size, in bytes, of generation 2 memory.</span></span>|
|`TotalPromotedSize2`|`win:UInt64`|<span data-ttu-id="c32b7-179">上次回收后仍存在于第 2 代中的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-179">The number of bytes that survived in generation 2 after the last collection.</span></span>|
|`GenerationSize3`|`win:UInt64`|<span data-ttu-id="c32b7-180">大型对象堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-180">The size, in bytes, of the large object heap.</span></span>|
|`TotalPromotedSize3`|`win:UInt64`|<span data-ttu-id="c32b7-181">上次回收后仍存在于大型对象堆中的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-181">The number of bytes that survived in the large object heap after the last collection.</span></span>|
|`FinalizationPromotedSize`|`win:UInt64`|<span data-ttu-id="c32b7-182">准备终结的对象的总大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-182">The total size, in bytes, of the objects that are ready for finalization.</span></span>|
|`FinalizationPromotedCount`|`win:UInt64`|<span data-ttu-id="c32b7-183">已准备好进行终结的对象的数目。</span><span class="sxs-lookup"><span data-stu-id="c32b7-183">The number of objects that are ready for finalization.</span></span>|
|`PinnedObjectCount`|`win:UInt32`|<span data-ttu-id="c32b7-184">固定（不可移动）对象的数目。</span><span class="sxs-lookup"><span data-stu-id="c32b7-184">The number of pinned (unmovable) objects.</span></span>|
|`SinkBlockCount`|`win:UInt32`|<span data-ttu-id="c32b7-185">正在使用的同步块的数目。</span><span class="sxs-lookup"><span data-stu-id="c32b7-185">The number of synchronization blocks in use.</span></span>|
|`GCHandleCount`|`win:UInt32`|<span data-ttu-id="c32b7-186">使用中的垃圾回收句柄的数目。</span><span class="sxs-lookup"><span data-stu-id="c32b7-186">The number of garbage collection handles in use.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-187">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-187">Unique ID for the instance of CoreCLR.</span></span>|
|`GenerationSize4`|`win:UInt64`|<span data-ttu-id="c32b7-188">固定对象堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-188">The size, in bytes, of the pinned object heap.</span></span>|
|`TotalPromotedSize4`|`win:UInt64`|<span data-ttu-id="c32b7-189">上次回收后保留在固定对象堆中的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-189">The number of bytes that survived in the pinned object heap after the last collection.</span></span>|

## <a name="gccreatesegment_v1-event"></a><span data-ttu-id="c32b7-190">GCCreateSegment_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-190">GCCreateSegment_V1 event</span></span>

<span data-ttu-id="c32b7-191">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-191">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-192">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-192">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-193">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-193">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-194">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-194">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-195">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-195">Informational (4)</span></span>|

<span data-ttu-id="c32b7-196">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-196">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-197">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-197">Event</span></span>|<span data-ttu-id="c32b7-198">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-198">Event ID</span></span>|<span data-ttu-id="c32b7-199">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-199">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCCreateSegment_V1`|<span data-ttu-id="c32b7-200">5</span><span class="sxs-lookup"><span data-stu-id="c32b7-200">5</span></span>|<span data-ttu-id="c32b7-201">已创建的新的垃圾回收段。</span><span class="sxs-lookup"><span data-stu-id="c32b7-201">A new garbage collection segment has been created.</span></span> <span data-ttu-id="c32b7-202">此外，当在已运行的进程中启用跟踪时，将为每个现有段引发此事件。</span><span class="sxs-lookup"><span data-stu-id="c32b7-202">In addition, when tracing is enabled on a process that is already running, this event is raised for each existing segment.</span></span>|

<span data-ttu-id="c32b7-203">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-203">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-204">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-204">Field name</span></span>|<span data-ttu-id="c32b7-205">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-205">Data type</span></span>|<span data-ttu-id="c32b7-206">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-206">Description</span></span>|
|----------------|---------------|-----------------|
|`Address`|`win:UInt64`|<span data-ttu-id="c32b7-207">段的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-207">The address of the segment.</span></span>|
|`Size`|`win:UInt64`|<span data-ttu-id="c32b7-208">段的大小。</span><span class="sxs-lookup"><span data-stu-id="c32b7-208">The size of the segment.</span></span>|
|`Type`|`win:UInt32`|<span data-ttu-id="c32b7-209">0x0 - 小型对象堆。</span><span class="sxs-lookup"><span data-stu-id="c32b7-209">0x0 - Small object heap.</span></span><br /><br /> <span data-ttu-id="c32b7-210">0x0 - 大型对象堆。</span><span class="sxs-lookup"><span data-stu-id="c32b7-210">0x1 - Large object heap.</span></span><br /><br /> <span data-ttu-id="c32b7-211">0x2 - 只读堆。</span><span class="sxs-lookup"><span data-stu-id="c32b7-211">0x2 - Read-only heap.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-212">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-212">Unique ID for the instance of CoreCLR.</span></span>|

<span data-ttu-id="c32b7-213">请注意，由垃圾回收器分配的段的大小特定于实现，且随时可能更改（包括定期更新）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-213">Note that the size of segments allocated by the garbage collector is implementation-specific and is subject to change at any time, including in periodic updates.</span></span> <span data-ttu-id="c32b7-214">应用程序不应假设特定段的大小或依赖于此大小，也不应尝试配置段分配可用的内存量。</span><span class="sxs-lookup"><span data-stu-id="c32b7-214">Your app should never make assumptions about or depend on a particular segment size, nor should it attempt to configure the amount of memory available for segment allocations.</span></span>

## <a name="gcfreesegment_v1-event"></a><span data-ttu-id="c32b7-215">GCFreeSegment_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-215">GCFreeSegment_V1 event</span></span>

<span data-ttu-id="c32b7-216">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-216">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-217">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-217">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-218">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-218">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-219">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-219">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-220">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-220">Informational (4)</span></span>|

<span data-ttu-id="c32b7-221">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-221">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-222">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-222">Event</span></span>|<span data-ttu-id="c32b7-223">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-223">Event ID</span></span>|<span data-ttu-id="c32b7-224">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-224">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCFreeSegment_V1`|<span data-ttu-id="c32b7-225">6</span><span class="sxs-lookup"><span data-stu-id="c32b7-225">6</span></span>|<span data-ttu-id="c32b7-226">已释放垃圾回收段。</span><span class="sxs-lookup"><span data-stu-id="c32b7-226">A garbage collection segment has been released.</span></span>|

<span data-ttu-id="c32b7-227">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-227">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-228">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-228">Field name</span></span>|<span data-ttu-id="c32b7-229">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-229">Data type</span></span>|<span data-ttu-id="c32b7-230">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-230">Description</span></span>|
|----------------|---------------|-----------------|
|`Address`|`win:UInt64`|<span data-ttu-id="c32b7-231">段的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-231">The address of the segment.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-232">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-232">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gcrestarteebegin_v1-event"></a><span data-ttu-id="c32b7-233">GCRestartEEBegin_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-233">GCRestartEEBegin_V1 event</span></span>

<span data-ttu-id="c32b7-234">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-234">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-235">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-235">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-236">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-236">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-237">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-237">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-238">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-238">Informational (4)</span></span>|

<span data-ttu-id="c32b7-239">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-239">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-240">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-240">Event</span></span>|<span data-ttu-id="c32b7-241">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-241">Event ID</span></span>|<span data-ttu-id="c32b7-242">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-242">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCRestartEEBegin_V1`|<span data-ttu-id="c32b7-243">7</span><span class="sxs-lookup"><span data-stu-id="c32b7-243">7</span></span>|<span data-ttu-id="c32b7-244">已开始从公共语言运行时挂起进行恢复。</span><span class="sxs-lookup"><span data-stu-id="c32b7-244">Resumption from common language runtime suspension has begun.</span></span>|

<span data-ttu-id="c32b7-245">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-245">This event does not have any event data.</span></span>

## <a name="gcrestarteeend_v1-event"></a><span data-ttu-id="c32b7-246">GCRestartEEEnd_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-246">GCRestartEEEnd_V1 event</span></span>

<span data-ttu-id="c32b7-247">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-247">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-248">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-248">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-249">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-249">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-250">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-250">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-251">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-251">Informational (4)</span></span>|

<span data-ttu-id="c32b7-252">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-252">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-253">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-253">Event</span></span>|<span data-ttu-id="c32b7-254">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-254">Event Id</span></span>|<span data-ttu-id="c32b7-255">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-255">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCRestartEEEnd_V1`|<span data-ttu-id="c32b7-256">3</span><span class="sxs-lookup"><span data-stu-id="c32b7-256">3</span></span>|<span data-ttu-id="c32b7-257">从公共语言运行时挂起进行的恢复已结束。</span><span class="sxs-lookup"><span data-stu-id="c32b7-257">Resumption from common language runtime suspension has ended.</span></span>|

<span data-ttu-id="c32b7-258">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-258">This event does not have any event data.</span></span>

## <a name="gcsuspendeeend_v1-event"></a><span data-ttu-id="c32b7-259">GCSuspendEEEnd_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-259">GCSuspendEEEnd_V1 event</span></span>

<span data-ttu-id="c32b7-260">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-260">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-261">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-261">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-262">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-262">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-263">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-263">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-264">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-264">Informational (4)</span></span>|

<span data-ttu-id="c32b7-265">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-265">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-266">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-266">Event</span></span>|<span data-ttu-id="c32b7-267">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-267">Event ID</span></span>|<span data-ttu-id="c32b7-268">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-268">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCSuspendEEEnd_V1`|<span data-ttu-id="c32b7-269">8</span><span class="sxs-lookup"><span data-stu-id="c32b7-269">8</span></span>|<span data-ttu-id="c32b7-270">结束垃圾回收执行引擎的挂起。</span><span class="sxs-lookup"><span data-stu-id="c32b7-270">End of suspension of the execution engine for garbage collection.</span></span>|

<span data-ttu-id="c32b7-271">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-271">This event does not have any event data.</span></span>

## <a name="gcsuspendeebegin_v1-event"></a><span data-ttu-id="c32b7-272">GCSuspendEEBegin_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-272">GCSuspendEEBegin_V1 event</span></span>

<span data-ttu-id="c32b7-273">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-273">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-274">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-274">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-275">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-275">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-276">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-276">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-277">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-277">Informational (4)</span></span>|

<span data-ttu-id="c32b7-278">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-278">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-279">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-279">Event</span></span>|<span data-ttu-id="c32b7-280">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-280">Event ID</span></span>|<span data-ttu-id="c32b7-281">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-281">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCSuspendEEBegin_V1`|<span data-ttu-id="c32b7-282">8</span><span class="sxs-lookup"><span data-stu-id="c32b7-282">8</span></span>|<span data-ttu-id="c32b7-283">开始挂起垃圾回收的执行引擎。</span><span class="sxs-lookup"><span data-stu-id="c32b7-283">Start of suspension of the execution engine for garbage collection.</span></span>|

|<span data-ttu-id="c32b7-284">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-284">Field name</span></span>|<span data-ttu-id="c32b7-285">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-285">Data type</span></span>|<span data-ttu-id="c32b7-286">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-286">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt32`|<span data-ttu-id="c32b7-287">第 *n* 代垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c32b7-287">The *n* th garbage collection.</span></span>|
|`Reason`|`win:UInt32`|<span data-ttu-id="c32b7-288">EE 挂起的原因。</span><span class="sxs-lookup"><span data-stu-id="c32b7-288">Reason for EE suspension.</span></span><br/><br/><span data-ttu-id="c32b7-289">`0x0`：挂起其他</span><span class="sxs-lookup"><span data-stu-id="c32b7-289">`0x0`: Suspend for Other</span></span><br/><br/><span data-ttu-id="c32b7-290">`0x1`：挂起 GC。</span><span class="sxs-lookup"><span data-stu-id="c32b7-290">`0x1`: Suspend for GC.</span></span><br/><br/><span data-ttu-id="c32b7-291">`0x2`：挂起 AppDomain 关闭。</span><span class="sxs-lookup"><span data-stu-id="c32b7-291">`0x2`: Suspend for AppDomain shutdown.</span></span><br/><br/><span data-ttu-id="c32b7-292">`0x3`：挂起代码间距调整。</span><span class="sxs-lookup"><span data-stu-id="c32b7-292">`0x3`: Suspend for code pitching.</span></span><br/><br/><span data-ttu-id="c32b7-293">`0x4`：挂起以关闭。</span><span class="sxs-lookup"><span data-stu-id="c32b7-293">`0x4`: Suspend for shutdown.</span></span><br/><br/><span data-ttu-id="c32b7-294">`0x5`：挂起调试器。</span><span class="sxs-lookup"><span data-stu-id="c32b7-294">`0x5`: Suspend for debugger.</span></span><br/><br/><span data-ttu-id="c32b7-295">`0x6`：挂起 GC 准备。</span><span class="sxs-lookup"><span data-stu-id="c32b7-295">`0x6`: Suspend for GC Prep.</span></span><br/><br/><span data-ttu-id="c32b7-296">`0x7`：挂起调试程序扫描</span><span class="sxs-lookup"><span data-stu-id="c32b7-296">`0x7`: Suspend for debugger sweep</span></span>|

## <a name="gcallocationtick_v3-event"></a><span data-ttu-id="c32b7-297">GCAllocationTick_V3 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-297">GCAllocationTick_V3 event</span></span>

<span data-ttu-id="c32b7-298">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-298">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-299">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-299">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-300">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-300">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-301">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-301">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-302">详细 (4) </span><span class="sxs-lookup"><span data-stu-id="c32b7-302">Verbose (4)</span></span>|

<span data-ttu-id="c32b7-303">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-303">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-304">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-304">Event</span></span>|<span data-ttu-id="c32b7-305">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-305">Event ID</span></span>|<span data-ttu-id="c32b7-306">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-306">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCAllocationTick_V3`|<span data-ttu-id="c32b7-307">10</span><span class="sxs-lookup"><span data-stu-id="c32b7-307">10</span></span>|<span data-ttu-id="c32b7-308">每次大约分配 100 KB。</span><span class="sxs-lookup"><span data-stu-id="c32b7-308">Each time approximately 100 KB is allocated.</span></span>|

<span data-ttu-id="c32b7-309">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-309">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-310">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-310">Field name</span></span>|<span data-ttu-id="c32b7-311">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-311">Data type</span></span>|<span data-ttu-id="c32b7-312">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-312">Description</span></span>|
|----------------|---------------|-----------------|
|`AllocationAmount`|`win:UInt32`|<span data-ttu-id="c32b7-313">分配大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-313">The allocation size, in bytes.</span></span> <span data-ttu-id="c32b7-314">对于小于 ULONG（4,294,967,295 字节）长度的分配，此值为精确值。</span><span class="sxs-lookup"><span data-stu-id="c32b7-314">This value is accurate for allocations that are less than the length of a ULONG (4,294,967,295 bytes).</span></span> <span data-ttu-id="c32b7-315">如果分配长度更大，则此字段包含了截断的值。</span><span class="sxs-lookup"><span data-stu-id="c32b7-315">If the allocation is greater, this field contains a truncated value.</span></span> <span data-ttu-id="c32b7-316">对于非常大的分配使用 `AllocationAmount64` 。</span><span class="sxs-lookup"><span data-stu-id="c32b7-316">Use `AllocationAmount64` for very large allocations.</span></span>|
|`AllocationKind`|`win:UInt32`|<span data-ttu-id="c32b7-317">`0x0` -小对象分配 (在小对象堆) 中分配。</span><span class="sxs-lookup"><span data-stu-id="c32b7-317">`0x0` - Small object allocation (allocation is in small object heap).</span></span><br /><br /> <span data-ttu-id="c32b7-318">`0x1` -大型对象分配 (在大型对象堆) 中分配。</span><span class="sxs-lookup"><span data-stu-id="c32b7-318">`0x1` - Large object allocation (allocation is in large object heap).</span></span>|
|`AllocationAmount64`|`win:UInt64`|<span data-ttu-id="c32b7-319">分配大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-319">The allocation size, in bytes.</span></span> <span data-ttu-id="c32b7-320">对于非常大的分配，此值为精确值。</span><span class="sxs-lookup"><span data-stu-id="c32b7-320">This value is accurate for very large allocations.</span></span>|
|`TypeId`|`win:Pointer`|<span data-ttu-id="c32b7-321">MethodTable 的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-321">The address of the MethodTable.</span></span> <span data-ttu-id="c32b7-322">如果在此事件期间分配了几种类型的对象，则此地址为对应于分配的最后一个对象（导致超过 100 KB 阙值的对象）的 MethodTable 地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-322">When there are several types of objects that were allocated during this event, this is the address of the MethodTable that corresponds to the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|
|`TypeName`|`win:UnicodeString`|<span data-ttu-id="c32b7-323">已分配的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="c32b7-323">The name of the type that was allocated.</span></span> <span data-ttu-id="c32b7-324">如果在此事件期间分配了几种类型的对象，则此地址为对应于分配的最后一个类型（导致超过 100 KB 阙值的对象）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-324">When there are several types of objects that were allocated during this event, this is the type of the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|
|`HeapIndex`|`win:UInt32`|<span data-ttu-id="c32b7-325">此对象所分配到的堆。</span><span class="sxs-lookup"><span data-stu-id="c32b7-325">The heap where the object was allocated.</span></span> <span data-ttu-id="c32b7-326">与工作站垃圾回收一起运行时，此值为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="c32b7-326">This value is 0 (zero) when running with workstation garbage collection.</span></span>|
|`Address`|`win:Pointer`|<span data-ttu-id="c32b7-327">上次分配的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-327">The address of the last allocated object.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-328">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-328">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gccreateconcurrentthread_v1-event"></a><span data-ttu-id="c32b7-329">GCCreateConcurrentThread_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-329">GCCreateConcurrentThread_V1 event</span></span>

<span data-ttu-id="c32b7-330">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-330">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-331">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-331">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-332">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-332">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-333">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-333">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-334">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-334">Informational (4)</span></span>|
|<span data-ttu-id="c32b7-335">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="c32b7-335">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="c32b7-336">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-336">Informational (4)</span></span>|

<span data-ttu-id="c32b7-337">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-337">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-338">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-338">Event</span></span>|<span data-ttu-id="c32b7-339">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-339">Event ID</span></span>|<span data-ttu-id="c32b7-340">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-340">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCCreateConcurrentThread_V1`|<span data-ttu-id="c32b7-341">11</span><span class="sxs-lookup"><span data-stu-id="c32b7-341">11</span></span>|<span data-ttu-id="c32b7-342">已创建并发垃圾回收线程。</span><span class="sxs-lookup"><span data-stu-id="c32b7-342">Concurrent garbage collection thread was created.</span></span>|

<span data-ttu-id="c32b7-343">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-343">This event does not have any event data.</span></span>

## <a name="gcterminateconcurrentthread_v1-event"></a><span data-ttu-id="c32b7-344">GCTerminateConcurrentThread_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-344">GCTerminateConcurrentThread_V1 event</span></span>

<span data-ttu-id="c32b7-345">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-345">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-346">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-346">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-347">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-347">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-348">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-348">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-349">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-349">Informational (4)</span></span>|
|<span data-ttu-id="c32b7-350">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="c32b7-350">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="c32b7-351">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-351">Informational (4)</span></span>|

<span data-ttu-id="c32b7-352">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-352">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-353">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-353">Event</span></span>|<span data-ttu-id="c32b7-354">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-354">Event ID</span></span>|<span data-ttu-id="c32b7-355">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-355">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCTerminateConcurrentThread_V1`|<span data-ttu-id="c32b7-356">12</span><span class="sxs-lookup"><span data-stu-id="c32b7-356">12</span></span>|<span data-ttu-id="c32b7-357">已终止并发垃圾回收线程。</span><span class="sxs-lookup"><span data-stu-id="c32b7-357">Concurrent garbage collection thread was terminated.</span></span>|

<span data-ttu-id="c32b7-358">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-358">This event does not have any event data.</span></span>

## <a name="gcfinalizersbegin_v1-event"></a><span data-ttu-id="c32b7-359">GCFinalizersBegin_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-359">GCFinalizersBegin_V1 event</span></span>

<span data-ttu-id="c32b7-360">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-360">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-361">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-361">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-362">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-362">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-363">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-363">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-364">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-364">Informational (4)</span></span>|

<span data-ttu-id="c32b7-365">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-365">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-366">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-366">Event</span></span>|<span data-ttu-id="c32b7-367">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-367">Event ID</span></span>|<span data-ttu-id="c32b7-368">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-368">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCFinalizersBegin_V1`|<span data-ttu-id="c32b7-369">14</span><span class="sxs-lookup"><span data-stu-id="c32b7-369">14</span></span>|<span data-ttu-id="c32b7-370">开始运行终结器。</span><span class="sxs-lookup"><span data-stu-id="c32b7-370">The start of running finalizers.</span></span>|

<span data-ttu-id="c32b7-371">此事件没有任何事件数据。</span><span class="sxs-lookup"><span data-stu-id="c32b7-371">This event does not have any event data.</span></span>

## <a name="gcfinalizersend_v1-event"></a><span data-ttu-id="c32b7-372">GCFinalizersEnd_V1 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-372">GCFinalizersEnd_V1 event</span></span>

<span data-ttu-id="c32b7-373">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-373">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-374">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-374">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-375">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-375">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-376">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-376">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-377">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-377">Informational (4)</span></span>|

<span data-ttu-id="c32b7-378">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-378">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-379">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-379">Event</span></span>|<span data-ttu-id="c32b7-380">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-380">Event ID</span></span>|<span data-ttu-id="c32b7-381">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-381">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCFinalizersEnd_V1`|<span data-ttu-id="c32b7-382">13</span><span class="sxs-lookup"><span data-stu-id="c32b7-382">13</span></span>|<span data-ttu-id="c32b7-383">结束运行终结器。</span><span class="sxs-lookup"><span data-stu-id="c32b7-383">The end of running finalizers.</span></span>|

<span data-ttu-id="c32b7-384">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-384">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-385">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-385">Field name</span></span>|<span data-ttu-id="c32b7-386">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-386">Data type</span></span>|<span data-ttu-id="c32b7-387">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-387">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt32`|<span data-ttu-id="c32b7-388">运行的终结器数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-388">The number of finalizers that were run.</span></span>|
|`ClrInstanceID`|<span data-ttu-id="c32b7-389">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-389">win:UInt16</span></span>|<span data-ttu-id="c32b7-390">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-390">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="setgchandle-event"></a><span data-ttu-id="c32b7-391">SetGCHandle 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-391">SetGCHandle event</span></span>

<span data-ttu-id="c32b7-392">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-392">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-393">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-393">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-394">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-394">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-395">`GCHandleKeyword` (0x2) </span><span class="sxs-lookup"><span data-stu-id="c32b7-395">`GCHandleKeyword` (0x2)</span></span>|<span data-ttu-id="c32b7-396">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-396">Informational (4)</span></span>|

<span data-ttu-id="c32b7-397">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-397">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-398">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-398">Event</span></span>|<span data-ttu-id="c32b7-399">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-399">Event ID</span></span>|<span data-ttu-id="c32b7-400">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-400">Raised when</span></span>|
|-----------|--------------|-----------------|
|`SetGCHandle`|<span data-ttu-id="c32b7-401">30</span><span class="sxs-lookup"><span data-stu-id="c32b7-401">30</span></span>|<span data-ttu-id="c32b7-402">已设置 GC 句柄。</span><span class="sxs-lookup"><span data-stu-id="c32b7-402">A GC Handle has been set.</span></span>|

<span data-ttu-id="c32b7-403">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-403">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-404">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-404">Field name</span></span>|<span data-ttu-id="c32b7-405">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-405">Data type</span></span>|<span data-ttu-id="c32b7-406">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-406">Description</span></span>|
|----------------|---------------|-----------------|
|`HandleID`|`win:Pointer`|<span data-ttu-id="c32b7-407">已分配的句柄的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-407">The address of the allocated handle.</span></span>|
|`ObjectID`|`win:Pointer`|<span data-ttu-id="c32b7-408">创建了其句柄的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-408">The address of the object whose handle was created.</span></span>|
|`Kind`|`win:UInt32`|<span data-ttu-id="c32b7-409">已设置的 GC 句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="c32b7-409">The type of GC handle that was set.</span></span> <br /><br /><span data-ttu-id="c32b7-410">`0x0`: WeakShort</span><span class="sxs-lookup"><span data-stu-id="c32b7-410">`0x0`: WeakShort</span></span> <br/><br/><span data-ttu-id="c32b7-411">`0x1`: WeakLong</span><span class="sxs-lookup"><span data-stu-id="c32b7-411">`0x1`: WeakLong</span></span> <br /><br /><span data-ttu-id="c32b7-412">`0x2`：强</span><span class="sxs-lookup"><span data-stu-id="c32b7-412">`0x2`: Strong</span></span> <br /><br /><span data-ttu-id="c32b7-413">`0x3`：固定</span><span class="sxs-lookup"><span data-stu-id="c32b7-413">`0x3`: Pinned</span></span> <br /><br /><span data-ttu-id="c32b7-414">`0x4`：变量</span><span class="sxs-lookup"><span data-stu-id="c32b7-414">`0x4`: Variable</span></span><br /><br /><span data-ttu-id="c32b7-415">`0x5`: RefCounted</span><span class="sxs-lookup"><span data-stu-id="c32b7-415">`0x5`: RefCounted</span></span> <br /><br /><span data-ttu-id="c32b7-416">`0x6`：依赖</span><span class="sxs-lookup"><span data-stu-id="c32b7-416">`0x6`: Dependent</span></span><br /><br /><span data-ttu-id="c32b7-417">`0x7`: AsyncPinned</span><span class="sxs-lookup"><span data-stu-id="c32b7-417">`0x7`: AsyncPinned</span></span><br /><br /><span data-ttu-id="c32b7-418">`0x8`： SizedRef</span><span class="sxs-lookup"><span data-stu-id="c32b7-418">`0x8`: SizedRef</span></span>|
|`Generation`|`win:UInt32`|<span data-ttu-id="c32b7-419">创建了其句柄的对象的生成。</span><span class="sxs-lookup"><span data-stu-id="c32b7-419">The generation of the object whose handle was created.</span></span>|
|`AppDomainID`|`win:UInt64`|<span data-ttu-id="c32b7-420">AppDomain ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-420">The AppDomain ID.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-421">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-421">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="destroygchandle-event"></a><span data-ttu-id="c32b7-422">DestroyGCHandle 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-422">DestroyGCHandle event</span></span>

<span data-ttu-id="c32b7-423">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-423">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-424">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-424">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-425">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-425">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-426">`GCHandleKeyword` (0x2) </span><span class="sxs-lookup"><span data-stu-id="c32b7-426">`GCHandleKeyword` (0x2)</span></span>|<span data-ttu-id="c32b7-427">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="c32b7-427">Informational (4)</span></span>|

<span data-ttu-id="c32b7-428">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-428">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-429">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-429">Event</span></span>|<span data-ttu-id="c32b7-430">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-430">Event ID</span></span>|<span data-ttu-id="c32b7-431">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-431">Raised when</span></span>|
|-----------|--------------|-----------------|
|`DestroyGCHandle`|<span data-ttu-id="c32b7-432">31</span><span class="sxs-lookup"><span data-stu-id="c32b7-432">31</span></span>|<span data-ttu-id="c32b7-433">GC 句柄已销毁。</span><span class="sxs-lookup"><span data-stu-id="c32b7-433">A GC Handle is destroyed.</span></span>|

<span data-ttu-id="c32b7-434">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-434">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-435">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-435">Field name</span></span>|<span data-ttu-id="c32b7-436">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-436">Data type</span></span>|<span data-ttu-id="c32b7-437">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-437">Description</span></span>|
|----------------|---------------|-----------------|
|`HandleID`|`win:Pointer`|<span data-ttu-id="c32b7-438">已销毁句柄的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-438">The address of the destroyed handle.</span></span>|
|`ClrInstanceID`|<span data-ttu-id="c32b7-439">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-439">win:UInt16</span></span>|<span data-ttu-id="c32b7-440">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-440">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="pinobjectatgctime-event"></a><span data-ttu-id="c32b7-441">PinObjectAtGCTime 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-441">PinObjectAtGCTime event</span></span>

<span data-ttu-id="c32b7-442">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-442">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-443">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-443">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-444">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-444">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-445">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-445">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-446">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="c32b7-446">Verbose (5)</span></span>|

<span data-ttu-id="c32b7-447">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-447">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-448">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-448">Event</span></span>|<span data-ttu-id="c32b7-449">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-449">Event ID</span></span>|<span data-ttu-id="c32b7-450">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-450">Raised when</span></span>|
|-----------|--------------|-----------------|
|`PinObjectAtGCTime`|<span data-ttu-id="c32b7-451">33</span><span class="sxs-lookup"><span data-stu-id="c32b7-451">33</span></span>|<span data-ttu-id="c32b7-452">对象在 GC 期间被固定。</span><span class="sxs-lookup"><span data-stu-id="c32b7-452">An object was pinned during a GC.</span></span>|

<span data-ttu-id="c32b7-453">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-453">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-454">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-454">Field name</span></span>|<span data-ttu-id="c32b7-455">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-455">Data type</span></span>|<span data-ttu-id="c32b7-456">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-456">Description</span></span>|
|----------------|---------------|-----------------|
|`HandleID`|`win:Pointer`|<span data-ttu-id="c32b7-457">句柄的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-457">The address of the handle.</span></span>|
|`ObjectID`|`win:Pointer`|<span data-ttu-id="c32b7-458">固定对象的地址。</span><span class="sxs-lookup"><span data-stu-id="c32b7-458">The address of the pinned object.</span></span>|
|`ObjectSize`|`win:UInt64`|<span data-ttu-id="c32b7-459">固定对象的大小。</span><span class="sxs-lookup"><span data-stu-id="c32b7-459">The size of the pinned object.</span></span>|
|`TypeName`|`win:UnicodeString`|<span data-ttu-id="c32b7-460">固定对象的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="c32b7-460">The name of the type of the pinned object.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-461">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-461">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gctriggered-event"></a><span data-ttu-id="c32b7-462">GCTriggered 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-462">GCTriggered event</span></span>

<span data-ttu-id="c32b7-463">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-463">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-464">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-464">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-465">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-465">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-466">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-466">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-467">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="c32b7-467">Verbose (5)</span></span>|

<span data-ttu-id="c32b7-468">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-468">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-469">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-469">Event</span></span>|<span data-ttu-id="c32b7-470">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-470">Event ID</span></span>|<span data-ttu-id="c32b7-471">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-471">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCTriggered`|<span data-ttu-id="c32b7-472">33</span><span class="sxs-lookup"><span data-stu-id="c32b7-472">33</span></span>|<span data-ttu-id="c32b7-473">已触发 GC。</span><span class="sxs-lookup"><span data-stu-id="c32b7-473">A GC has been triggered.</span></span>|

<span data-ttu-id="c32b7-474">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-474">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-475">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-475">Field name</span></span>|<span data-ttu-id="c32b7-476">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-476">Data type</span></span>|<span data-ttu-id="c32b7-477">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-477">Description</span></span>|
|----------------|---------------|-----------------|
|`Reason`|`win:UInt32`|<span data-ttu-id="c32b7-478">触发 GC 的原因。</span><span class="sxs-lookup"><span data-stu-id="c32b7-478">The reason a GC was triggered.</span></span><br/><br/><span data-ttu-id="c32b7-479">`0x0`: AllocSmall</span><span class="sxs-lookup"><span data-stu-id="c32b7-479">`0x0`: AllocSmall</span></span><br/><br/><span data-ttu-id="c32b7-480">`0x1`：已引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-480">`0x1`: Induced</span></span> <br/><br/><span data-ttu-id="c32b7-481">`0x2`: LowMemory</span><span class="sxs-lookup"><span data-stu-id="c32b7-481">`0x2`: LowMemory</span></span> <br/><br/><span data-ttu-id="c32b7-482">`0x3`： Empty</span><span class="sxs-lookup"><span data-stu-id="c32b7-482">`0x3`: Empty</span></span> <br/><br/><span data-ttu-id="c32b7-483">`0x4`: AllocLarge</span><span class="sxs-lookup"><span data-stu-id="c32b7-483">`0x4`: AllocLarge</span></span> <br/><br/><span data-ttu-id="c32b7-484">`0x5`: OutOfSpaceSmallObjectHeap</span><span class="sxs-lookup"><span data-stu-id="c32b7-484">`0x5`: OutOfSpaceSmallObjectHeap</span></span> <br/><br/><span data-ttu-id="c32b7-485">`0x6`: OutOfSpaceLargeObjectHeap</span><span class="sxs-lookup"><span data-stu-id="c32b7-485">`0x6`: OutOfSpaceLargeObjectHeap</span></span> <br/><br/><span data-ttu-id="c32b7-486">`0x7`:InducedNoForce</span><span class="sxs-lookup"><span data-stu-id="c32b7-486">`0x7`:InducedNoForce</span></span> <br/><br/><span data-ttu-id="c32b7-487">`0x8`：压力</span><span class="sxs-lookup"><span data-stu-id="c32b7-487">`0x8`: Stress</span></span> <br/><br/><span data-ttu-id="c32b7-488">`0x9`: InducedLowMemory</span><span class="sxs-lookup"><span data-stu-id="c32b7-488">`0x9`: InducedLowMemory</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-489">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-489">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="increasememorypressure-event"></a><span data-ttu-id="c32b7-490">IncreaseMemoryPressure 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-490">IncreaseMemoryPressure event</span></span>

<span data-ttu-id="c32b7-491">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-491">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-492">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-492">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-493">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-493">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-494">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-494">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-495"> (4) 的信息</span><span class="sxs-lookup"><span data-stu-id="c32b7-495">Information (4)</span></span>|

<span data-ttu-id="c32b7-496">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-496">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-497">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-497">Event</span></span>|<span data-ttu-id="c32b7-498">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-498">Event ID</span></span>|<span data-ttu-id="c32b7-499">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-499">Raised when</span></span>|
|----------------|---------------|-----------------|
|`IncreaseMemoryPressure`|<span data-ttu-id="c32b7-500">200</span><span class="sxs-lookup"><span data-stu-id="c32b7-500">200</span></span>|<span data-ttu-id="c32b7-501">增加了内存压力。</span><span class="sxs-lookup"><span data-stu-id="c32b7-501">Memory pressure was increased.</span></span>|

<span data-ttu-id="c32b7-502">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-502">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-503">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-503">Field Name</span></span>|<span data-ttu-id="c32b7-504">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-504">Data type</span></span>|<span data-ttu-id="c32b7-505">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-505">Description</span></span>|
|----------------|---------------|-----------------|
|`ClrInstanceID`|<span data-ttu-id="c32b7-506">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-506">win:UInt16</span></span>|<span data-ttu-id="c32b7-507">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-507">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="decreasememorypressure-event"></a><span data-ttu-id="c32b7-508">DecreaseMemoryPressure 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-508">DecreaseMemoryPressure event</span></span>

<span data-ttu-id="c32b7-509">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-509">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-510">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-510">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-511">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-511">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-512">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-512">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-513"> (4) 的信息</span><span class="sxs-lookup"><span data-stu-id="c32b7-513">Information (4)</span></span>|

<span data-ttu-id="c32b7-514">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-514">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-515">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-515">Event</span></span>|<span data-ttu-id="c32b7-516">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-516">Event ID</span></span>|<span data-ttu-id="c32b7-517">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-517">Raised when</span></span>|
|----------------|---------------|-----------------|
|`DecreaseMemoryPressure`|<span data-ttu-id="c32b7-518">201</span><span class="sxs-lookup"><span data-stu-id="c32b7-518">201</span></span>|<span data-ttu-id="c32b7-519">内存压力下降。</span><span class="sxs-lookup"><span data-stu-id="c32b7-519">Memory pressure was decreased.</span></span>|

<span data-ttu-id="c32b7-520">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-520">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-521">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-521">Field Name</span></span>|<span data-ttu-id="c32b7-522">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-522">Data type</span></span>|<span data-ttu-id="c32b7-523">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-523">Description</span></span>|
|----------------|---------------|-----------------|
|`BytesFreed`|`win:UInt32`|<span data-ttu-id="c32b7-524">已释放字节。</span><span class="sxs-lookup"><span data-stu-id="c32b7-524">Bytes freed.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-525">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-525">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="gcmarkwithtype-event"></a><span data-ttu-id="c32b7-526">GCMarkWithType 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-526">GCMarkWithType event</span></span>

<span data-ttu-id="c32b7-527">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-527">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-528">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-528">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-529">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-529">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-530">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-530">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-531"> (4) 的信息</span><span class="sxs-lookup"><span data-stu-id="c32b7-531">Information (4)</span></span>|

<span data-ttu-id="c32b7-532">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-532">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-533">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-533">Event</span></span>|<span data-ttu-id="c32b7-534">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-534">Event ID</span></span>|<span data-ttu-id="c32b7-535">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-535">Raised when</span></span>|
|----------------|---------------|-----------------|
|`GCMarkWithType`|<span data-ttu-id="c32b7-536">202</span><span class="sxs-lookup"><span data-stu-id="c32b7-536">202</span></span>|<span data-ttu-id="c32b7-537">Gc 标记阶段中已标记了一个 GC 根。</span><span class="sxs-lookup"><span data-stu-id="c32b7-537">A GC root has been marked during GC mark phase.</span></span>|

<span data-ttu-id="c32b7-538">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-538">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-539">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-539">Field Name</span></span>|<span data-ttu-id="c32b7-540">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-540">Data type</span></span>|<span data-ttu-id="c32b7-541">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-541">Description</span></span>|
|----------------|---------------|-----------------|
|`HeapNum`|`win:UInt32`|<span data-ttu-id="c32b7-542">堆号。</span><span class="sxs-lookup"><span data-stu-id="c32b7-542">The heap number.</span></span>|
|`ClrInstanceID`|<span data-ttu-id="c32b7-543">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="c32b7-543">win:UInt16</span></span>|<span data-ttu-id="c32b7-544">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-544">Unique ID for the instance of CoreCLR.</span></span>|
|`Type`|`win:UInt32`|<span data-ttu-id="c32b7-545">GC 根类型。</span><span class="sxs-lookup"><span data-stu-id="c32b7-545">The GC root type.</span></span><br/><br/><span data-ttu-id="c32b7-546">`0x0`： Stack</span><span class="sxs-lookup"><span data-stu-id="c32b7-546">`0x0`: Stack</span></span><br/><br/><span data-ttu-id="c32b7-547">`0x1`：终结器</span><span class="sxs-lookup"><span data-stu-id="c32b7-547">`0x1`: Finalizer</span></span><br/><br/><span data-ttu-id="c32b7-548">`0x2`：句柄</span><span class="sxs-lookup"><span data-stu-id="c32b7-548">`0x2`: Handle</span></span><br/><br/><span data-ttu-id="c32b7-549">`0x3`：较早</span><span class="sxs-lookup"><span data-stu-id="c32b7-549">`0x3`: Older</span></span><br/><br/><span data-ttu-id="c32b7-550">`0x4`： SizedRef</span><span class="sxs-lookup"><span data-stu-id="c32b7-550">`0x4`: SizedRef</span></span><br/><br/><span data-ttu-id="c32b7-551">`0x5`：溢出</span><span class="sxs-lookup"><span data-stu-id="c32b7-551">`0x5`: Overflow</span></span><br/><br/>|
|`Bytes`|`win:UInt64`|<span data-ttu-id="c32b7-552">标记的字节数。</span><span class="sxs-lookup"><span data-stu-id="c32b7-552">The number of bytes marked.</span></span>|

## <a name="gcjoin_v2-event"></a><span data-ttu-id="c32b7-553">GCJoin_V2 事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-553">GCJoin_V2 event</span></span>

<span data-ttu-id="c32b7-554">下表显示了关键字和级别：</span><span class="sxs-lookup"><span data-stu-id="c32b7-554">The following table shows the keyword and level:</span></span>

|<span data-ttu-id="c32b7-555">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="c32b7-555">Keyword for raising the event</span></span>|<span data-ttu-id="c32b7-556">Level</span><span class="sxs-lookup"><span data-stu-id="c32b7-556">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="c32b7-557">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="c32b7-557">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="c32b7-558">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="c32b7-558">Verbose (5)</span></span>|

<span data-ttu-id="c32b7-559">下表显示了事件信息：</span><span class="sxs-lookup"><span data-stu-id="c32b7-559">The following table shows the event information:</span></span>

|<span data-ttu-id="c32b7-560">事件</span><span class="sxs-lookup"><span data-stu-id="c32b7-560">Event</span></span>|<span data-ttu-id="c32b7-561">事件 ID</span><span class="sxs-lookup"><span data-stu-id="c32b7-561">Event ID</span></span>|<span data-ttu-id="c32b7-562">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="c32b7-562">Raised when</span></span>|
|-----------|--------------|-----------------|
|`GCJoin_V2`|<span data-ttu-id="c32b7-563">203</span><span class="sxs-lookup"><span data-stu-id="c32b7-563">203</span></span>|<span data-ttu-id="c32b7-564">已加入 GC 线程。</span><span class="sxs-lookup"><span data-stu-id="c32b7-564">A GC thread joined.</span></span>|

<span data-ttu-id="c32b7-565">下表显示了事件数据：</span><span class="sxs-lookup"><span data-stu-id="c32b7-565">The following table shows the event data:</span></span>

|<span data-ttu-id="c32b7-566">字段名称</span><span class="sxs-lookup"><span data-stu-id="c32b7-566">Field name</span></span>|<span data-ttu-id="c32b7-567">数据类型</span><span class="sxs-lookup"><span data-stu-id="c32b7-567">Data type</span></span>|<span data-ttu-id="c32b7-568">说明</span><span class="sxs-lookup"><span data-stu-id="c32b7-568">Description</span></span>|
|----------------|---------------|-----------------|
|`Heap`|`win:UInt32`|<span data-ttu-id="c32b7-569">堆号</span><span class="sxs-lookup"><span data-stu-id="c32b7-569">The heap number</span></span>|
|`JoinTime`|`win:UInt32`|<span data-ttu-id="c32b7-570">指示在联接 (联接结束时是否激发此事件 `0x0` ， `0x1` 对于联接端) 为。</span><span class="sxs-lookup"><span data-stu-id="c32b7-570">Indicates whether this event is fired at the start of a join or end of a join (`0x0` for join start, `0x1` for join end)</span></span>|
|`JoinType`|`win:UInt32`|<span data-ttu-id="c32b7-571">联接类型。</span><span class="sxs-lookup"><span data-stu-id="c32b7-571">The join type.</span></span> <br/><br/><span data-ttu-id="c32b7-572">`0x0`：上次联接</span><span class="sxs-lookup"><span data-stu-id="c32b7-572">`0x0`: Last Join</span></span><br/><br/><span data-ttu-id="c32b7-573">`0x1`：联接</span><span class="sxs-lookup"><span data-stu-id="c32b7-573">`0x1`: Join</span></span> <br/><br/><span data-ttu-id="c32b7-574">`0x2`：重新启动</span><span class="sxs-lookup"><span data-stu-id="c32b7-574">`0x2`: Restart</span></span> <br/><br/><span data-ttu-id="c32b7-575">`0x3`：第一个反向联接</span><span class="sxs-lookup"><span data-stu-id="c32b7-575">`0x3`: First Reverse Join</span></span><br/><br/><span data-ttu-id="c32b7-576">`0x4`：反向联接</span><span class="sxs-lookup"><span data-stu-id="c32b7-576">`0x4`: Reverse Join</span></span><br/><br/>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="c32b7-577">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="c32b7-577">Unique ID for the instance of CoreCLR.</span></span>|
