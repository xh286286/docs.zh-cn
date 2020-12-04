---
title: ThreadPool 运行时事件
description: 请参阅在 .NET Core 中收集有关线程池的诊断信息的 .NET 运行时线程池事件。 线程池事件为工作线程池事件或 i/o 线程池事件。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- ThreadPool events (CoreCLR)
- ETW, thread pool events (CoreCLR)
ms.openlocfilehash: cdd6041c5842d4922c60e33daf6db366f7d35327
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96591083"
---
# <a name="net-runtime-thread-pool-events"></a><span data-ttu-id="471a6-104">.NET 运行时线程池事件</span><span class="sxs-lookup"><span data-stu-id="471a6-104">.NET runtime thread pool events</span></span>

<span data-ttu-id="471a6-105">这些事件收集有关线程池内的工作线程和 i/o 线程的信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-105">These events collect information about worker and I/O threads in the threadpool.</span></span> <span data-ttu-id="471a6-106">有关如何将这些事件用于诊断的详细信息，请参阅 [日志记录和跟踪 .net 应用程序](../../core/diagnostics/logging-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="471a6-106">For more information about how to use these events for diagnostic purposes, see [logging and tracing .NET applications](../../core/diagnostics/logging-tracing.md)</span></span>

## <a name="iothreadcreate_v1-event"></a><span data-ttu-id="471a6-107">IOThreadCreate_V1 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-107">IOThreadCreate_V1 event</span></span>

 <span data-ttu-id="471a6-108">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-108">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-109">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-109">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-110">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-110">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-111">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-111">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-112">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-112">Informational (4)</span></span>|

 <span data-ttu-id="471a6-113">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-113">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-114">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-114">Event</span></span>|<span data-ttu-id="471a6-115">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-115">Event ID</span></span>|<span data-ttu-id="471a6-116">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="471a6-116">Raised when</span></span>|
|-----------------------------------|-----------|
|`IOThreadCreate_V1`|<span data-ttu-id="471a6-117">44</span><span class="sxs-lookup"><span data-stu-id="471a6-117">44</span></span>|<span data-ttu-id="471a6-118">在线程池中创建 I/O 线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-118">An I/O thread is created in the thread pool.</span></span>|

 <span data-ttu-id="471a6-119">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-119">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-120">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-120">Field name</span></span>|<span data-ttu-id="471a6-121">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-121">Data type</span></span>|<span data-ttu-id="471a6-122">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-122">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt64`|<span data-ttu-id="471a6-123">I/O 线程数，包括新创建的线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-123">Number of I/O threads, including the newly created thread.</span></span>|
|`NumRetired`|`win:UInt64`|<span data-ttu-id="471a6-124">已停用的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-124">Number of retired worker threads.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-125">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-125">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="iothreadterminate_v1-event"></a><span data-ttu-id="471a6-126">IOThreadTerminate_V1 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-126">IOThreadTerminate_V1 event</span></span>

 <span data-ttu-id="471a6-127">下表显示关键字和级别</span><span class="sxs-lookup"><span data-stu-id="471a6-127">The following table shows the keyword and level</span></span>

|<span data-ttu-id="471a6-128">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-128">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-129">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-129">Level</span></span>
|-----------------------------------|-----------
|<span data-ttu-id="471a6-130">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-130">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-131">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-131">Informational (4)</span></span>

 <span data-ttu-id="471a6-132">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-132">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-133">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-133">Event</span></span>|<span data-ttu-id="471a6-134">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-134">Event ID</span></span>|<span data-ttu-id="471a6-135">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="471a6-135">Raised when</span></span>|
|-----------|--------------|-----------------|
|`IOThreadTerminate`|<span data-ttu-id="471a6-136">45</span><span class="sxs-lookup"><span data-stu-id="471a6-136">45</span></span>|<span data-ttu-id="471a6-137">线程池中的 i/o 线程终止。</span><span class="sxs-lookup"><span data-stu-id="471a6-137">An I/O thread is terminated in the thread pool.</span></span>|

 <span data-ttu-id="471a6-138">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-138">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-139">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-139">Field name</span></span>|<span data-ttu-id="471a6-140">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-140">Data type</span></span>|<span data-ttu-id="471a6-141">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-141">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt64`|<span data-ttu-id="471a6-142">线程池中剩余的 I/O 线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-142">Number of I/O threads remaining in the thread pool.</span></span>|
|`NumRetired`|`win:UInt64`|<span data-ttu-id="471a6-143">已停用的 I/O 线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-143">Number of retired I/O threads.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-144">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-144">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="iothreadretire_v1-event"></a><span data-ttu-id="471a6-145">IOThreadRetire_V1 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-145">IOThreadRetire_V1 event</span></span>

 <span data-ttu-id="471a6-146">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-146">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-147">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-147">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-148">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-148">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-149">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-149">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-150">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-150">Informational (4)</span></span>|

 <span data-ttu-id="471a6-151">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-151">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-152">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-152">Event</span></span>|<span data-ttu-id="471a6-153">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-153">Event ID</span></span>|<span data-ttu-id="471a6-154">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="471a6-154">Raised when</span></span>|
|-----------|--------------|-----------------|
|`IOThreadRetire_V1`|<span data-ttu-id="471a6-155">46</span><span class="sxs-lookup"><span data-stu-id="471a6-155">46</span></span>|<span data-ttu-id="471a6-156">I/O 线程变为停用候选项。</span><span class="sxs-lookup"><span data-stu-id="471a6-156">An I/O thread becomes a retirement candidate.</span></span>|

 <span data-ttu-id="471a6-157">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-157">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-158">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-158">Field name</span></span>|<span data-ttu-id="471a6-159">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-159">Data type</span></span>|<span data-ttu-id="471a6-160">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-160">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt64`|<span data-ttu-id="471a6-161">线程池中剩余的 I/O 线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-161">Number of I/O threads remaining in the thread pool.</span></span>|
|`NumRetired`|`win:UInt64`|<span data-ttu-id="471a6-162">已停用的 I/O 线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-162">Number of retired I/O threads.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-163">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-163">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="iothreadunretire_v1-event"></a><span data-ttu-id="471a6-164">IOThreadUnretire_V1 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-164">IOThreadUnretire_V1 event</span></span>

 <span data-ttu-id="471a6-165">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-165">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-166">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-166">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-167">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-167">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-168">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-168">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-169">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-169">Informational (4)</span></span>|

 <span data-ttu-id="471a6-170">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-170">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-171">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-171">Event</span></span>|<span data-ttu-id="471a6-172">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-172">Event ID</span></span>|<span data-ttu-id="471a6-173">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="471a6-173">Raised when</span></span>|
|-----------|--------------|-----------------|
|`IOThreadUnretire_V1`|<span data-ttu-id="471a6-174">47</span><span class="sxs-lookup"><span data-stu-id="471a6-174">47</span></span>|<span data-ttu-id="471a6-175">I/O 线程因在该线程变为停用候选项后的等待期间内达到 I/O 而恢复使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-175">An I/O thread is unretired because of I/O that arrives within a waiting period after the thread becomes a retirement candidate.</span></span>|

 <span data-ttu-id="471a6-176">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-176">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-177">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-177">Field name</span></span>|<span data-ttu-id="471a6-178">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-178">Data type</span></span>|<span data-ttu-id="471a6-179">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-179">Description</span></span>|
|----------------|---------------|-----------------|
|`Count`|`win:UInt64`|<span data-ttu-id="471a6-180">线程池中的 I/O 线程数，包括这一个。</span><span class="sxs-lookup"><span data-stu-id="471a6-180">Number of I/O threads in the thread pool, including this one.</span></span>|
|`NumRetired`|`win:UInt64`|<span data-ttu-id="471a6-181">已停用的 I/O 线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-181">Number of retired I/O threads.</span></span>|
|`ClrInstanceID`|`Win:UInt16`|<span data-ttu-id="471a6-182">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-182">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadstart-event"></a><span data-ttu-id="471a6-183">ThreadPoolWorkerThreadStart 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-183">ThreadPoolWorkerThreadStart event</span></span>

|<span data-ttu-id="471a6-184">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-184">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-185">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-185">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="471a6-186">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-186">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-187">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-187">Informational (4)</span></span>|

|<span data-ttu-id="471a6-188">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-188">Event</span></span>|<span data-ttu-id="471a6-189">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-189">Event ID</span></span>|<span data-ttu-id="471a6-190">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-190">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadStart`|<span data-ttu-id="471a6-191">50</span><span class="sxs-lookup"><span data-stu-id="471a6-191">50</span></span>|<span data-ttu-id="471a6-192">创建工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-192">A worker thread is created.</span></span>|

|<span data-ttu-id="471a6-193">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-193">Field name</span></span>|<span data-ttu-id="471a6-194">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-194">Data type</span></span>|<span data-ttu-id="471a6-195">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-195">Description</span></span>|
|----------------|---------------|-----------------|
|`ActiveWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-196">可用于处理工作的工作线程数，包括已在处理工作的工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-196">Number of worker threads available to process work, including those that are already processing work.</span></span>|
|`RetiredWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-197">不能用于处理工作但被保留以防之后需要更多线程的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-197">Number of worker threads that are not available to process work, but that are being held in reserve in case more threads are needed later.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-198">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-198">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadstop-event"></a><span data-ttu-id="471a6-199">ThreadPoolWorkerThreadStop 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-199">ThreadPoolWorkerThreadStop event</span></span>

|<span data-ttu-id="471a6-200">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-200">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-201">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-201">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="471a6-202">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-202">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-203">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-203">Informational (4)</span></span>|

|<span data-ttu-id="471a6-204">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-204">Event</span></span>|<span data-ttu-id="471a6-205">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-205">Event ID</span></span>|<span data-ttu-id="471a6-206">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-206">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadStop`|<span data-ttu-id="471a6-207">51</span><span class="sxs-lookup"><span data-stu-id="471a6-207">51</span></span>|<span data-ttu-id="471a6-208">停止工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-208">A worker thread is stopped.</span></span>|

|<span data-ttu-id="471a6-209">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-209">Field name</span></span>|<span data-ttu-id="471a6-210">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-210">Data type</span></span>|<span data-ttu-id="471a6-211">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-211">Description</span></span>|
|----------------|---------------|-----------------|
|`ActiveWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-212">可用于处理工作的工作线程数，包括已在处理工作的工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-212">Number of worker threads available to process work, including those that are already processing work.</span></span>|
|`RetiredWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-213">不能用于处理工作但被保留以防之后需要更多线程的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-213">Number of worker threads that are not available to process work, but that are being held in reserve in case more threads are needed later.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-214">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-214">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadwait-event"></a><span data-ttu-id="471a6-215">ThreadPoolWorkerThreadWait 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-215">ThreadPoolWorkerThreadWait event</span></span>

|<span data-ttu-id="471a6-216">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-216">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-217">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-217">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="471a6-218">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-218">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-219">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-219">Informational (4)</span></span>|

|<span data-ttu-id="471a6-220">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-220">Event</span></span>|<span data-ttu-id="471a6-221">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-221">Event ID</span></span>|<span data-ttu-id="471a6-222">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-222">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadWait`|<span data-ttu-id="471a6-223">57</span><span class="sxs-lookup"><span data-stu-id="471a6-223">57</span></span>|<span data-ttu-id="471a6-224">工作线程开始等待工作。</span><span class="sxs-lookup"><span data-stu-id="471a6-224">A worker thread starts waiting for work.</span></span>|

|<span data-ttu-id="471a6-225">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-225">Field name</span></span>|<span data-ttu-id="471a6-226">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-226">Data type</span></span>|<span data-ttu-id="471a6-227">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-227">Description</span></span>|
|----------------|---------------|-----------------|
|`ActiveWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-228">可用于处理工作的工作线程数，包括已在处理工作的工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-228">Number of worker threads available to process work, including those that are already processing work.</span></span>|
|`RetiredWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-229">不能用于处理工作但被保留以防之后需要更多线程的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-229">Number of worker threads that are not available to process work, but that are being held in reserve in case more threads are needed later.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-230">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-230">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadretirementstart-event"></a><span data-ttu-id="471a6-231">ThreadPoolWorkerThreadRetirementStart 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-231">ThreadPoolWorkerThreadRetirementStart event</span></span>

|<span data-ttu-id="471a6-232">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-232">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-233">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-233">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="471a6-234">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-234">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-235">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-235">Informational (4)</span></span>|

|<span data-ttu-id="471a6-236">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-236">Event</span></span>|<span data-ttu-id="471a6-237">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-237">Event ID</span></span>|<span data-ttu-id="471a6-238">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-238">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadRetirementStart`|<span data-ttu-id="471a6-239">52</span><span class="sxs-lookup"><span data-stu-id="471a6-239">52</span></span>|<span data-ttu-id="471a6-240">停用工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-240">A worker thread retires.</span></span>|

|<span data-ttu-id="471a6-241">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-241">Field name</span></span>|<span data-ttu-id="471a6-242">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-242">Data type</span></span>|<span data-ttu-id="471a6-243">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-243">Description</span></span>|
|----------------|---------------|-----------------|
|`ActiveWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-244">可用于处理工作的工作线程数，包括已在处理工作的工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-244">Number of worker threads available to process work, including those that are already processing work.</span></span>|
|`RetiredWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-245">不能用于处理工作但被保留以防之后需要更多线程的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-245">Number of worker threads that are not available to process work, but that are being held in reserve in case more threads are needed later.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-246">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-246">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadretirementstop-event"></a><span data-ttu-id="471a6-247">ThreadPoolWorkerThreadRetirementStop 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-247">ThreadPoolWorkerThreadRetirementStop event</span></span>

|<span data-ttu-id="471a6-248">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-248">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-249">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-249">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="471a6-250">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-250">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-251">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-251">Informational (4)</span></span>|

|<span data-ttu-id="471a6-252">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-252">Event</span></span>|<span data-ttu-id="471a6-253">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-253">Event ID</span></span>|<span data-ttu-id="471a6-254">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-254">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadRetirementStop`|<span data-ttu-id="471a6-255">53</span><span class="sxs-lookup"><span data-stu-id="471a6-255">53</span></span>|<span data-ttu-id="471a6-256">停用的工作线程再次变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="471a6-256">A retired worker thread becomes active again.</span></span>|

|<span data-ttu-id="471a6-257">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-257">Field name</span></span>|<span data-ttu-id="471a6-258">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-258">Data type</span></span>|<span data-ttu-id="471a6-259">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-259">Description</span></span>|
|----------------|---------------|-----------------|
|`ActiveWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-260">可用于处理工作的工作线程数，包括已在处理工作的工作线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-260">Number of worker threads available to process work, including those that are already processing work.</span></span>|
|`RetiredWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-261">不能用于处理工作但被保留以防之后需要更多线程的工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-261">Number of worker threads that are not available to process work, but that are being held in reserve in case more threads are needed later.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-262">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-262">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadadjustmentsample-event"></a><span data-ttu-id="471a6-263">ThreadPoolWorkerThreadAdjustmentSample 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-263">ThreadPoolWorkerThreadAdjustmentSample event</span></span>

 <span data-ttu-id="471a6-264">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-264">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-265">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-265">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-266">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-266">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-267">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-267">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-268">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-268">Informational (4)</span></span>|

 <span data-ttu-id="471a6-269">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-269">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-270">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-270">Event</span></span>|<span data-ttu-id="471a6-271">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-271">Event ID</span></span>|<span data-ttu-id="471a6-272">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-272">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadAdjustmentSample`|<span data-ttu-id="471a6-273">54</span><span class="sxs-lookup"><span data-stu-id="471a6-273">54</span></span>|<span data-ttu-id="471a6-274">指一个示例的信息收集，即具有一定并发级别的即时吞吐量测量。</span><span class="sxs-lookup"><span data-stu-id="471a6-274">Refers to the collection of information for one sample; that is, a measurement of throughput with a certain concurrency level, in an instant of time.</span></span>|

 <span data-ttu-id="471a6-275">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-275">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-276">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-276">Field name</span></span>|<span data-ttu-id="471a6-277">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-277">Data type</span></span>|<span data-ttu-id="471a6-278">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-278">Description</span></span>|
|----------------|---------------|-----------------|
|`Throughput`|`win:Double`|<span data-ttu-id="471a6-279">每个时间单位的完成数。</span><span class="sxs-lookup"><span data-stu-id="471a6-279">Number of completions per unit of time.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-280">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-280">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadadjustmentadjustment-event"></a><span data-ttu-id="471a6-281">ThreadPoolWorkerThreadAdjustmentAdjustment 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-281">ThreadPoolWorkerThreadAdjustmentAdjustment event</span></span>

 <span data-ttu-id="471a6-282">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-282">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-283">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-283">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-284">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-284">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-285">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-285">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-286">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-286">Informational (4)</span></span>|

 <span data-ttu-id="471a6-287">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-287">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-288">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-288">Event</span></span>|<span data-ttu-id="471a6-289">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-289">Event ID</span></span>|<span data-ttu-id="471a6-290">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-290">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadAdjustmentAdjustment`|<span data-ttu-id="471a6-291">55</span><span class="sxs-lookup"><span data-stu-id="471a6-291">55</span></span>|<span data-ttu-id="471a6-292">当线程注入（爬山）算法确定并发级别发生更改时，在控件中记录更改。</span><span class="sxs-lookup"><span data-stu-id="471a6-292">Records a change in control, when the thread injection (hill-climbing) algorithm determines that a change in concurrency level is in place.</span></span>|

 <span data-ttu-id="471a6-293">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-293">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-294">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-294">Field name</span></span>|<span data-ttu-id="471a6-295">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-295">Data type</span></span>|<span data-ttu-id="471a6-296">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-296">Description</span></span>|
|----------------|---------------|-----------------|
|`AverageThroughput`|`win:Double`|<span data-ttu-id="471a6-297">测量示例的平均吞吐量。</span><span class="sxs-lookup"><span data-stu-id="471a6-297">Average throughput of a sample of measurements.</span></span>|
|`NewWorkerThreadCount`|`win:UInt32`|<span data-ttu-id="471a6-298">新的活动工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-298">New number of active worker threads.</span></span>|
|`Reason`|`win:UInt32`|<span data-ttu-id="471a6-299">调整的原因。</span><span class="sxs-lookup"><span data-stu-id="471a6-299">Reason for the adjustment.</span></span><br /><br /> <span data-ttu-id="471a6-300">`0x0` 预热.</span><span class="sxs-lookup"><span data-stu-id="471a6-300">`0x0` - Warmup.</span></span><br /><br /> <span data-ttu-id="471a6-301">`0x1` 出错.</span><span class="sxs-lookup"><span data-stu-id="471a6-301">`0x1` - Initializing.</span></span><br /><br /> <span data-ttu-id="471a6-302">`0x2` -随机移动。</span><span class="sxs-lookup"><span data-stu-id="471a6-302">`0x2` - Random move.</span></span><br /><br /> <span data-ttu-id="471a6-303">`0x3` -上升的移动。</span><span class="sxs-lookup"><span data-stu-id="471a6-303">`0x3` - Climbing move.</span></span><br /><br /> <span data-ttu-id="471a6-304">`0x4` -更改点。</span><span class="sxs-lookup"><span data-stu-id="471a6-304">`0x4` - Change point.</span></span><br /><br /> <span data-ttu-id="471a6-305">`0x5` 稳定.</span><span class="sxs-lookup"><span data-stu-id="471a6-305">`0x5` - Stabilizing.</span></span><br /><br /> <span data-ttu-id="471a6-306">`0x6` 资源不足.</span><span class="sxs-lookup"><span data-stu-id="471a6-306">`0x6` - Starvation.</span></span><br /><br /> <span data-ttu-id="471a6-307">`0x7` -线程已超时。</span><span class="sxs-lookup"><span data-stu-id="471a6-307">`0x7` - Thread timed out.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-308">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-308">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolworkerthreadadjustmentstats-event"></a><span data-ttu-id="471a6-309">ThreadPoolWorkerThreadAdjustmentStats 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-309">ThreadPoolWorkerThreadAdjustmentStats event</span></span>

 <span data-ttu-id="471a6-310">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-310">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-311">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-311">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-312">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-312">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-313">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-313">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-314">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-314">Verbose (5)</span></span>

 <span data-ttu-id="471a6-315">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-315">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-316">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-316">Event</span></span>|<span data-ttu-id="471a6-317">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-317">Event ID</span></span>|<span data-ttu-id="471a6-318">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-318">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolWorkerThreadAdjustmentStats`|<span data-ttu-id="471a6-319">56</span><span class="sxs-lookup"><span data-stu-id="471a6-319">56</span></span>|<span data-ttu-id="471a6-320">在线程池上收集数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-320">Gathers data on the thread pool.</span></span>|

 <span data-ttu-id="471a6-321">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-321">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-322">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-322">Field name</span></span>|<span data-ttu-id="471a6-323">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-323">Data type</span></span>|<span data-ttu-id="471a6-324">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-324">Description</span></span>|
|----------------|---------------|-----------------|
|`Duration`|`win:Double`|<span data-ttu-id="471a6-325">收集这些统计信息的时间量（以秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="471a6-325">Amount of time, in seconds, during which these statistics were collected.</span></span>|
|`Throughput`|`win:Double`|<span data-ttu-id="471a6-326">在此间隔期间每秒完成的平均数量。</span><span class="sxs-lookup"><span data-stu-id="471a6-326">Average number of completions per second during this interval.</span></span>|
|`ThreadWave`|`win:Double`|<span data-ttu-id="471a6-327">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-327">Reserved for internal use.</span></span>|
|`ThroughputWave`|`win:Double`|<span data-ttu-id="471a6-328">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-328">Reserved for internal use.</span></span>|
|`ThroughputErrorEstimate`|`win:Double`|<span data-ttu-id="471a6-329">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-329">Reserved for internal use.</span></span>|
|`AverageThroughputErrorEstimate`|`win:Double`|<span data-ttu-id="471a6-330">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-330">Reserved for internal use.</span></span>|
|`ThroughputRatio`|`win:Double`|<span data-ttu-id="471a6-331">在此间隔期间因活动工作线程计数变化导致的相对吞吐量变化。</span><span class="sxs-lookup"><span data-stu-id="471a6-331">The relative improvement in throughput caused by variations in active worker thread count during this interval.</span></span>|
|`Confidence`|`win:Double`|<span data-ttu-id="471a6-332">ThroughputRatio 字段的有效性测量。</span><span class="sxs-lookup"><span data-stu-id="471a6-332">A measure of the validity of the ThroughputRatio field.</span></span>|
|`NewcontrolSetting`|`win:Double`|<span data-ttu-id="471a6-333">将作为活动线程计数未来变化基线的活动工作线程数。</span><span class="sxs-lookup"><span data-stu-id="471a6-333">The number of active worker threads that will serve as the baseline for future variations in active thread count.</span></span>|
|`NewThreadWaveMagnitude`|`win:UInt16`|<span data-ttu-id="471a6-334">活动线程计数的未来变化量值。</span><span class="sxs-lookup"><span data-stu-id="471a6-334">The magnitude of future variations in active thread count.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-335">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-335">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="threadpoolenqueue-event"></a><span data-ttu-id="471a6-336">ThreadPoolEnqueue 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-336">ThreadPoolEnqueue event</span></span>

 <span data-ttu-id="471a6-337">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-337">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-338">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-338">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-339">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-339">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-340">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-340">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-341">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-341">Verbose (5)</span></span>

 <span data-ttu-id="471a6-342">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-342">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-343">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-343">Event</span></span>|<span data-ttu-id="471a6-344">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-344">Event ID</span></span>|<span data-ttu-id="471a6-345">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-345">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolEnqueue`|<span data-ttu-id="471a6-346">61</span><span class="sxs-lookup"><span data-stu-id="471a6-346">61</span></span>|<span data-ttu-id="471a6-347">工作项已在线程池队列中排队。</span><span class="sxs-lookup"><span data-stu-id="471a6-347">A work item was enqueued in the thread pool queue.</span></span>|

 <span data-ttu-id="471a6-348">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-348">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-349">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-349">Field name</span></span>|<span data-ttu-id="471a6-350">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-350">Data type</span></span>|<span data-ttu-id="471a6-351">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-351">Description</span></span>|
|----------------|---------------|-----------------|
|`WorkID`|`win:Pointer`|<span data-ttu-id="471a6-352">指向工作请求的指针。</span><span class="sxs-lookup"><span data-stu-id="471a6-352">Pointer to the work request.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-353">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-353">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadpooldequeue-event"></a><span data-ttu-id="471a6-354">ThreadPoolDequeue 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-354">ThreadPoolDequeue event</span></span>

 <span data-ttu-id="471a6-355">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-355">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-356">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-356">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-357">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-357">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-358">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-358">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-359">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-359">Verbose (5)</span></span>

 <span data-ttu-id="471a6-360">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-360">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-361">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-361">Event</span></span>|<span data-ttu-id="471a6-362">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-362">Event ID</span></span>|<span data-ttu-id="471a6-363">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-363">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolDequeue`|<span data-ttu-id="471a6-364">62</span><span class="sxs-lookup"><span data-stu-id="471a6-364">62</span></span>|<span data-ttu-id="471a6-365">工作项已从线程池队列中取消排队。</span><span class="sxs-lookup"><span data-stu-id="471a6-365">A work item was dequeued from the thread pool queue.</span></span>|

 <span data-ttu-id="471a6-366">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-366">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-367">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-367">Field name</span></span>|<span data-ttu-id="471a6-368">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-368">Data type</span></span>|<span data-ttu-id="471a6-369">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-369">Description</span></span>|
|----------------|---------------|-----------------|
|`WorkID`|`win:Pointer`|<span data-ttu-id="471a6-370">指向工作请求的指针。</span><span class="sxs-lookup"><span data-stu-id="471a6-370">Pointer to the work request.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-371">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-371">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadpoolioenqueue-event"></a><span data-ttu-id="471a6-372">ThreadPoolIOEnqueue 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-372">ThreadPoolIOEnqueue event</span></span>

 <span data-ttu-id="471a6-373">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-373">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-374">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-374">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-375">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-375">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-376">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-376">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-377">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-377">Verbose (5)</span></span>

 <span data-ttu-id="471a6-378">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-378">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-379">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-379">Event</span></span>|<span data-ttu-id="471a6-380">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-380">Event ID</span></span>|<span data-ttu-id="471a6-381">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-381">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolIOEnqueue`|<span data-ttu-id="471a6-382">63</span><span class="sxs-lookup"><span data-stu-id="471a6-382">63</span></span>|<span data-ttu-id="471a6-383">发生异步 IO 完成后，线程排队 IO 完成通知。</span><span class="sxs-lookup"><span data-stu-id="471a6-383">A thread enqueues an IO completion notification after an async IO completion occurs.</span></span>|

 <span data-ttu-id="471a6-384">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-384">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-385">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-385">Field name</span></span>|<span data-ttu-id="471a6-386">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-386">Data type</span></span>|<span data-ttu-id="471a6-387">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-387">Description</span></span>|
|----------------|---------------|-----------------|
|`NativeOverlapped`|`win:Pointer`|<span data-ttu-id="471a6-388">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-388">Reserved for internal use.</span></span>|
|`Overlapped`|`win:Pointer`|<span data-ttu-id="471a6-389">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-389">Reserved for internal use.</span></span>|
|`MultiDequeues`|`win:Boolean`|<span data-ttu-id="471a6-390">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-390">Reserved for internal use.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-391">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-391">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadpooliodequeue-event"></a><span data-ttu-id="471a6-392">ThreadPoolIODequeue 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-392">ThreadPoolIODequeue event</span></span>

 <span data-ttu-id="471a6-393">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-393">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-394">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-394">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-395">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-395">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-396">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-396">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-397">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-397">Verbose (5)</span></span>

 <span data-ttu-id="471a6-398">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-398">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-399">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-399">Event</span></span>|<span data-ttu-id="471a6-400">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-400">Event ID</span></span>|<span data-ttu-id="471a6-401">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-401">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolIODequeue`|<span data-ttu-id="471a6-402">64</span><span class="sxs-lookup"><span data-stu-id="471a6-402">64</span></span>|<span data-ttu-id="471a6-403">线程取消排队了 IO 完成通知。</span><span class="sxs-lookup"><span data-stu-id="471a6-403">A thread dequeues the IO completion notification.</span></span>|

 <span data-ttu-id="471a6-404">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-404">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-405">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-405">Field name</span></span>|<span data-ttu-id="471a6-406">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-406">Data type</span></span>|<span data-ttu-id="471a6-407">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-407">Description</span></span>|
|----------------|---------------|-----------------|
|`NativeOverlapped`|`win:Pointer`|<span data-ttu-id="471a6-408">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-408">Reserved for internal use.</span></span>|
|`Overlapped`|`win:Pointer`|<span data-ttu-id="471a6-409">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-409">Reserved for internal use.</span></span>|
|`MultiDequeues`|`win:Boolean`|<span data-ttu-id="471a6-410">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-410">Reserved for internal use.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-411">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-411">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadpooliopack-event"></a><span data-ttu-id="471a6-412">ThreadPoolIOPack 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-412">ThreadPoolIOPack event</span></span>

 <span data-ttu-id="471a6-413">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-413">The following table shows the keyword and level.</span></span>

|<span data-ttu-id="471a6-414">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-414">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-415">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-415">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-416">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-416">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-417">详细级别 (5)</span><span class="sxs-lookup"><span data-stu-id="471a6-417">Verbose (5)</span></span>|

 <span data-ttu-id="471a6-418">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-418">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-419">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-419">Event</span></span>|<span data-ttu-id="471a6-420">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-420">Event ID</span></span>|<span data-ttu-id="471a6-421">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-421">Description</span></span>|
|-----------|--------------|-----------------|
|`ThreadPoolIOPack`|<span data-ttu-id="471a6-422">65</span><span class="sxs-lookup"><span data-stu-id="471a6-422">65</span></span>|<span data-ttu-id="471a6-423">调用了 ThreadPool 重叠 IO pack。</span><span class="sxs-lookup"><span data-stu-id="471a6-423">ThreadPool overlapped IO pack is called.</span></span>|

 <span data-ttu-id="471a6-424">下表显示了事件数据</span><span class="sxs-lookup"><span data-stu-id="471a6-424">The following table shows the event data</span></span>

|<span data-ttu-id="471a6-425">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-425">Field name</span></span>|<span data-ttu-id="471a6-426">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-426">Data type</span></span>|<span data-ttu-id="471a6-427">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-427">Description</span></span>|
|----------------|---------------|-----------------|
|`NativeOverlapped`|`win:Pointer`|<span data-ttu-id="471a6-428">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-428">Reserved for internal use.</span></span>|
|`Overlapped`|`win:Pointer`|<span data-ttu-id="471a6-429">保留以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="471a6-429">Reserved for internal use.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-430">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-430">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadcreating-event"></a><span data-ttu-id="471a6-431">ThreadCreating 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-431">ThreadCreating event</span></span>

 <span data-ttu-id="471a6-432">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-432">The following table shows the keywords and level.</span></span>

|<span data-ttu-id="471a6-433">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-433">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-434">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-434">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-435">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-435">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-436">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-436">Informational (4)</span></span>|

 <span data-ttu-id="471a6-437">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-437">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-438">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-438">Event</span></span>|<span data-ttu-id="471a6-439">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-439">Event ID</span></span>|<span data-ttu-id="471a6-440">描述</span><span class="sxs-lookup"><span data-stu-id="471a6-440">Description</span></span>|
|----------------|---------------|-----------------|
|`ThreadCreating`|<span data-ttu-id="471a6-441">70</span><span class="sxs-lookup"><span data-stu-id="471a6-441">70</span></span>|<span data-ttu-id="471a6-442">已创建线程。</span><span class="sxs-lookup"><span data-stu-id="471a6-442">Thread has been created.</span></span>|

 <span data-ttu-id="471a6-443">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-443">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-444">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-444">Field name</span></span>|<span data-ttu-id="471a6-445">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-445">Data type</span></span>|<span data-ttu-id="471a6-446">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-446">Description</span></span>|
|----------------|---------------|-----------------|
|`ID`|`win:Pointer`|<span data-ttu-id="471a6-447">线程 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-447">Thread ID</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-448">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-448">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="threadrunning-event"></a><span data-ttu-id="471a6-449">ThreadRunning 事件</span><span class="sxs-lookup"><span data-stu-id="471a6-449">ThreadRunning event</span></span>

 <span data-ttu-id="471a6-450">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="471a6-450">The following table shows the keywords and level.</span></span>

|<span data-ttu-id="471a6-451">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="471a6-451">Keyword for raising the event</span></span>|<span data-ttu-id="471a6-452">Level</span><span class="sxs-lookup"><span data-stu-id="471a6-452">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="471a6-453">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="471a6-453">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="471a6-454">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="471a6-454">Informational (4)</span></span>|

 <span data-ttu-id="471a6-455">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="471a6-455">The following table shows the event information.</span></span>

|<span data-ttu-id="471a6-456">事件</span><span class="sxs-lookup"><span data-stu-id="471a6-456">Event</span></span>|<span data-ttu-id="471a6-457">事件 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-457">Event ID</span></span>|<span data-ttu-id="471a6-458">描述</span><span class="sxs-lookup"><span data-stu-id="471a6-458">Description</span></span>|
|----------------|---------------|-----------------|
|`ThreadRunning`|<span data-ttu-id="471a6-459">71</span><span class="sxs-lookup"><span data-stu-id="471a6-459">71</span></span>|<span data-ttu-id="471a6-460">线程已开始运行。</span><span class="sxs-lookup"><span data-stu-id="471a6-460">Thread has started running.</span></span>|

 <span data-ttu-id="471a6-461">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="471a6-461">The following table shows the event data.</span></span>

|<span data-ttu-id="471a6-462">字段名称</span><span class="sxs-lookup"><span data-stu-id="471a6-462">Field name</span></span>|<span data-ttu-id="471a6-463">数据类型</span><span class="sxs-lookup"><span data-stu-id="471a6-463">Data type</span></span>|<span data-ttu-id="471a6-464">说明</span><span class="sxs-lookup"><span data-stu-id="471a6-464">Description</span></span>|
|----------------|---------------|-----------------|
|`ID`|`win:Pointer`|<span data-ttu-id="471a6-465">线程 ID</span><span class="sxs-lookup"><span data-stu-id="471a6-465">Thread ID</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="471a6-466">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="471a6-466">Unique ID for the instance of CoreCLR.</span></span>|
