---
title: 异常运行时事件
description: 请参阅收集特定于异常和异常处理的诊断信息的 .NET 运行时事件。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- exception events (CoreCLR)
- exception handling events (CoreCLR)
- ETW, EventPipe, LTTng exception events (CoreCLR)
ms.openlocfilehash: f4f63c8469f9c734b872ddaec8d1d7f7f0427576
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96591077"
---
# <a name="net-runtime-exception-events"></a><span data-ttu-id="ff4b4-103">.NET 运行时异常事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-103">.NET runtime exception events</span></span>

<span data-ttu-id="ff4b4-104">这些运行时事件捕获有关引发的异常的信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-104">These runtime events capture information about exceptions that are thrown.</span></span> <span data-ttu-id="ff4b4-105">有关如何将这些事件用于诊断的详细信息，请参阅 [日志记录和跟踪 .net 应用程序](../../core/diagnostics/logging-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-105">For more information about how to use these events for diagnostic purposes, see [logging and tracing .NET applications](../../core/diagnostics/logging-tracing.md)</span></span>

## <a name="exceptionthrown_v1-event"></a><span data-ttu-id="ff4b4-106">ExceptionThrown_V1 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-106">ExceptionThrown_V1 event</span></span>

|<span data-ttu-id="ff4b4-107">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-107">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-108">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-108">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-109">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-109">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-110">错误 (1)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-110">Error (1)</span></span>|

 <span data-ttu-id="ff4b4-111">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-111">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-112">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-112">Event</span></span>|<span data-ttu-id="ff4b4-113">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-113">Event ID</span></span>|<span data-ttu-id="ff4b4-114">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-114">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionThrown_V1`|<span data-ttu-id="ff4b4-115">80</span><span class="sxs-lookup"><span data-stu-id="ff4b4-115">80</span></span>|<span data-ttu-id="ff4b4-116">引发托管异常。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-116">A managed exception is thrown.</span></span>|

|<span data-ttu-id="ff4b4-117">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff4b4-117">Field name</span></span>|<span data-ttu-id="ff4b4-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff4b4-118">Data type</span></span>|<span data-ttu-id="ff4b4-119">说明</span><span class="sxs-lookup"><span data-stu-id="ff4b4-119">Description</span></span>|
|----------------|---------------|-----------------|
|`ExceptionType`|`win:UnicodeString`|<span data-ttu-id="ff4b4-120">异常的类型，例如，`System.NullReferenceException`。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-120">Type of the exception; for example, `System.NullReferenceException`.</span></span>|
|`ExceptionMessage`|`win:UnicodeString`|<span data-ttu-id="ff4b4-121">实际的异常消息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-121">Actual exception message.</span></span>|
|`EIPCodeThrow`|`win:Pointer`|<span data-ttu-id="ff4b4-122">指向异常发生位置的指令指针。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-122">Instruction pointer where exception occurred.</span></span>|
|`ExceptionHR`|`win:UInt32`|<span data-ttu-id="ff4b4-123">异常 [HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-123">Exception [HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a).</span></span>|
|`ExceptionFlags`|`win:UInt16`|<span data-ttu-id="ff4b4-124">`0x01`: HasInnerException.</span><span class="sxs-lookup"><span data-stu-id="ff4b4-124">`0x01`: HasInnerException.</span></span><br /><br /> <span data-ttu-id="ff4b4-125">`0x02`: IsNestedException.</span><span class="sxs-lookup"><span data-stu-id="ff4b4-125">`0x02`: IsNestedException.</span></span><br /><br /> <span data-ttu-id="ff4b4-126">`0x04`: IsRethrownException.</span><span class="sxs-lookup"><span data-stu-id="ff4b4-126">`0x04`: IsRethrownException.</span></span><br /><br /> <span data-ttu-id="ff4b4-127">`0x08`： IsCorruptedStateException (指示进程状态已损坏;请参阅 [处理损坏状态异常](/archive/msdn-magazine/2009/february/clr-inside-out-handling-corrupted-state-exceptions)) 。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-127">`0x08`: IsCorruptedStateException (indicates that the process state is corrupt; see [Handling Corrupted State Exceptions](/archive/msdn-magazine/2009/february/clr-inside-out-handling-corrupted-state-exceptions)).</span></span><br /><br /> <span data-ttu-id="ff4b4-128">`0x10`： IsCLSCompliant (派生自的异常符合 <xref:System.Exception> cls; 否则，它不符合 cls) 。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-128">`0x10`: IsCLSCompliant (an exception that derives from <xref:System.Exception> is CLS-compliant; otherwise, it is not CLS-compliant).</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff4b4-129">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-129">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="exceptioncatchstart-event"></a><span data-ttu-id="ff4b4-130">ExceptionCatchStart 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-130">ExceptionCatchStart event</span></span>

<span data-ttu-id="ff4b4-131">当托管异常 catch 处理程序开始时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-131">This event is emitted when a managed exception catch handler begins.</span></span>

|<span data-ttu-id="ff4b4-132">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-132">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-133">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-133">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-134">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-134">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-135">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-135">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-136">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-136">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-137">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-137">Event</span></span>|<span data-ttu-id="ff4b4-138">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-138">Event ID</span></span>|<span data-ttu-id="ff4b4-139">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-139">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionCatchStart`|<span data-ttu-id="ff4b4-140">250</span><span class="sxs-lookup"><span data-stu-id="ff4b4-140">250</span></span>|<span data-ttu-id="ff4b4-141">托管异常由运行时处理。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-141">A managed exception is handled by the runtime.</span></span>|

|<span data-ttu-id="ff4b4-142">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff4b4-142">Field name</span></span>|<span data-ttu-id="ff4b4-143">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff4b4-143">Data type</span></span>|<span data-ttu-id="ff4b4-144">说明</span><span class="sxs-lookup"><span data-stu-id="ff4b4-144">Description</span></span>|
|----------------|---------------|-----------------|
|`EIPCodeThrow`|`win:Pointer`|<span data-ttu-id="ff4b4-145">指向异常发生位置的指令指针。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-145">Instruction pointer where exception occurred.</span></span>|
|`MethodID`|`win:Pointer`|<span data-ttu-id="ff4b4-146">一个指针，指向发生了异常的方法上的方法说明符。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-146">Pointer to the method descriptor on the method where exception occurred.</span></span>|
|`MethodName`|`win:UnicodeString`|<span data-ttu-id="ff4b4-147">发生异常的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-147">Name of the method where exception occurred.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff4b4-148">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-148">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="exceptioncatchstop-event"></a><span data-ttu-id="ff4b4-149">ExceptionCatchStop 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-149">ExceptionCatchStop event</span></span>

<span data-ttu-id="ff4b4-150">当托管异常 catch 处理程序结束时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-150">This event is emitted when a managed exception catch handler ends.</span></span>

|<span data-ttu-id="ff4b4-151">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-151">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-152">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-152">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-153">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-153">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-154">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-154">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-155">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-155">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-156">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-156">Event</span></span>|<span data-ttu-id="ff4b4-157">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-157">Event ID</span></span>|<span data-ttu-id="ff4b4-158">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-158">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionCatchStop`|<span data-ttu-id="ff4b4-159">251</span><span class="sxs-lookup"><span data-stu-id="ff4b4-159">251</span></span>|<span data-ttu-id="ff4b4-160">已完成托管异常 catch 处理程序。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-160">A managed exception catch handler is done.</span></span>|

## <a name="exceptionfinallystart-event"></a><span data-ttu-id="ff4b4-161">ExceptionFinallyStart 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-161">ExceptionFinallyStart event</span></span>

<span data-ttu-id="ff4b4-162">当托管异常 finally 处理程序开始时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-162">This event is emitted when a managed exception finally handler begins.</span></span>

|<span data-ttu-id="ff4b4-163">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-163">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-164">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-164">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-165">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-165">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-166">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-166">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-167">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-167">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-168">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-168">Event</span></span>|<span data-ttu-id="ff4b4-169">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-169">Event ID</span></span>|<span data-ttu-id="ff4b4-170">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-170">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionFinallyStart`|<span data-ttu-id="ff4b4-171">252</span><span class="sxs-lookup"><span data-stu-id="ff4b4-171">252</span></span>|<span data-ttu-id="ff4b4-172">托管异常由运行时处理。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-172">A managed exception is handled by the runtime.</span></span>|

|<span data-ttu-id="ff4b4-173">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff4b4-173">Field name</span></span>|<span data-ttu-id="ff4b4-174">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff4b4-174">Data type</span></span>|<span data-ttu-id="ff4b4-175">说明</span><span class="sxs-lookup"><span data-stu-id="ff4b4-175">Description</span></span>|
|----------------|---------------|-----------------|
|`EIPCodeThrow`|`win:Pointer`|<span data-ttu-id="ff4b4-176">指向异常发生位置的指令指针。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-176">Instruction pointer where exception occurred.</span></span>|
|`MethodID`|`win:Pointer`|<span data-ttu-id="ff4b4-177">一个指针，指向发生了异常的方法上的方法说明符。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-177">Pointer to the method descriptor on the method where exception occurred.</span></span>|
|`MethodName`|`win:UnicodeString`|<span data-ttu-id="ff4b4-178">发生异常的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-178">Name of the method where exception occurred.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff4b4-179">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-179">Unique ID for the instance of CLR or CoreCLR.</span></span>|

## <a name="exceptionfinallystop-event"></a><span data-ttu-id="ff4b4-180">ExceptionFinallyStop 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-180">ExceptionFinallyStop event</span></span>

<span data-ttu-id="ff4b4-181">当托管异常 catch 处理程序结束时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-181">This event is emitted when a managed exception catch handler ends.</span></span>

|<span data-ttu-id="ff4b4-182">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-182">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-183">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-183">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-184">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-184">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-185">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-185">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-186">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-186">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-187">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-187">Event</span></span>|<span data-ttu-id="ff4b4-188">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-188">Event ID</span></span>|<span data-ttu-id="ff4b4-189">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-189">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionFinallyStop`|<span data-ttu-id="ff4b4-190">253</span><span class="sxs-lookup"><span data-stu-id="ff4b4-190">253</span></span>|<span data-ttu-id="ff4b4-191">托管异常 finally 处理程序已完成。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-191">A managed exception finally handler is done.</span></span>|

## <a name="exceptionfilterstart-event"></a><span data-ttu-id="ff4b4-192">ExceptionFilterStart 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-192">ExceptionFilterStart event</span></span>

<span data-ttu-id="ff4b4-193">当托管异常筛选开始时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-193">This event is emitted when a managed exception filtering begins.</span></span>

|<span data-ttu-id="ff4b4-194">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-194">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-195">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-195">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-196">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-196">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-197">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-197">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-198">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-198">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-199">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-199">Event</span></span>|<span data-ttu-id="ff4b4-200">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-200">Event ID</span></span>|<span data-ttu-id="ff4b4-201">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-201">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionFilterStart`|<span data-ttu-id="ff4b4-202">254</span><span class="sxs-lookup"><span data-stu-id="ff4b4-202">254</span></span>|<span data-ttu-id="ff4b4-203">托管异常筛选开始。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-203">A managed exception filtering begins.</span></span>|

|<span data-ttu-id="ff4b4-204">字段名称</span><span class="sxs-lookup"><span data-stu-id="ff4b4-204">Field name</span></span>|<span data-ttu-id="ff4b4-205">数据类型</span><span class="sxs-lookup"><span data-stu-id="ff4b4-205">Data type</span></span>|<span data-ttu-id="ff4b4-206">说明</span><span class="sxs-lookup"><span data-stu-id="ff4b4-206">Description</span></span>|
|----------------|---------------|-----------------|
|`EIPCodeThrow`|`win:Pointer`|<span data-ttu-id="ff4b4-207">指向异常发生位置的指令指针。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-207">Instruction pointer where exception occurred.</span></span>|
|`MethodID`|`win:Pointer`|<span data-ttu-id="ff4b4-208">一个指针，指向发生了异常的方法上的方法说明符。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-208">Pointer to the method descriptor on the method where exception occurred.</span></span>|
|`MethodName`|`win:UnicodeString`|<span data-ttu-id="ff4b4-209">发生异常的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-209">Name of the method where exception occurred.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="ff4b4-210">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-210">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="exceptionfilterstop-event"></a><span data-ttu-id="ff4b4-211">ExceptionFilterStop 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-211">ExceptionFilterStop event</span></span>

<span data-ttu-id="ff4b4-212">当托管异常筛选结束时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-212">This event is emitted when a managed exception filtering ends.</span></span>

|<span data-ttu-id="ff4b4-213">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-213">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-214">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-214">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-215">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-215">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-216">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-216">Informational (4)</span></span>|

 <span data-ttu-id="ff4b4-217">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-217">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-218">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-218">Event</span></span>|<span data-ttu-id="ff4b4-219">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-219">Event ID</span></span>|<span data-ttu-id="ff4b4-220">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-220">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionFilteringStart`|<span data-ttu-id="ff4b4-221">255</span><span class="sxs-lookup"><span data-stu-id="ff4b4-221">255</span></span>|<span data-ttu-id="ff4b4-222">托管异常筛选结束。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-222">A managed exception filtering ends.</span></span>|

## <a name="exceptionthrownstop-event"></a><span data-ttu-id="ff4b4-223">ExceptionThrownStop 事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-223">ExceptionThrownStop event</span></span>

<span data-ttu-id="ff4b4-224">当运行时处理引发的托管异常时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-224">This event is emitted when the runtime is done handling a managed exception that was thrown.</span></span>

|<span data-ttu-id="ff4b4-225">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ff4b4-225">Keyword for raising the event</span></span>|<span data-ttu-id="ff4b4-226">Level</span><span class="sxs-lookup"><span data-stu-id="ff4b4-226">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="ff4b4-227">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-227">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ff4b4-228">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="ff4b4-228">Informational (4)</span></span>|
  
 <span data-ttu-id="ff4b4-229">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-229">The following table shows event information.</span></span>

|<span data-ttu-id="ff4b4-230">事件</span><span class="sxs-lookup"><span data-stu-id="ff4b4-230">Event</span></span>|<span data-ttu-id="ff4b4-231">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ff4b4-231">Event ID</span></span>|<span data-ttu-id="ff4b4-232">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ff4b4-232">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ExceptionThrownStop`|<span data-ttu-id="ff4b4-233">256</span><span class="sxs-lookup"><span data-stu-id="ff4b4-233">256</span></span>|<span data-ttu-id="ff4b4-234">托管异常筛选结束。</span><span class="sxs-lookup"><span data-stu-id="ff4b4-234">A managed exception filtering ends.</span></span>|
