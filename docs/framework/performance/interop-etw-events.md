---
title: 互操作 ETW 事件
description: 查看互操作 ETW (Windows) 事件的事件跟踪，这些事件在 .NET 中捕获有关 Microsoft 中间语言 (MSIL) 存根生成 & 缓存的信息。
ms.date: 03/30/2017
helpviewer_keywords:
- interop events [.NET Framework]
- ETW, interop events (CLR)
ms.assetid: eb6eac2e-45f4-4923-a32c-38f203da66df
ms.openlocfilehash: 8e92a1492d0295fb71473843752cb4c6184d3604
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96242183"
---
# <a name="interop-etw-events"></a><span data-ttu-id="77d53-103">互操作 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="77d53-103">Interop ETW Events</span></span>

<span data-ttu-id="77d53-104">互操作事件捕获有关 Microsoft 中间语言 (MSIL) 存根生成和缓存的信息。</span><span class="sxs-lookup"><span data-stu-id="77d53-104">Interop events capture information about Microsoft intermediate language (MSIL) stub generation and caching.</span></span>  

## <a name="ilstubgenerated-event"></a><span data-ttu-id="77d53-105">ILStubGenerated 事件</span><span class="sxs-lookup"><span data-stu-id="77d53-105">ILStubGenerated Event</span></span>

<span data-ttu-id="77d53-106">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="77d53-106">The following table shows the keyword and level.</span></span> <span data-ttu-id="77d53-107">（有关详细信息，请参阅 [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md)。）</span><span class="sxs-lookup"><span data-stu-id="77d53-107">(For more information, see [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="77d53-108">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="77d53-108">Keyword for raising the event</span></span>|<span data-ttu-id="77d53-109">Level</span><span class="sxs-lookup"><span data-stu-id="77d53-109">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="77d53-110">`InteropKeyword` (0x2000)</span><span class="sxs-lookup"><span data-stu-id="77d53-110">`InteropKeyword` (0x2000)</span></span>|<span data-ttu-id="77d53-111">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="77d53-111">Informational(4)</span></span>|  
  
 <span data-ttu-id="77d53-112">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="77d53-112">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="77d53-113">事件</span><span class="sxs-lookup"><span data-stu-id="77d53-113">Event</span></span>|<span data-ttu-id="77d53-114">事件 ID</span><span class="sxs-lookup"><span data-stu-id="77d53-114">Event ID</span></span>|<span data-ttu-id="77d53-115">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="77d53-115">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ILStubGenerated`|<span data-ttu-id="77d53-116">88</span><span class="sxs-lookup"><span data-stu-id="77d53-116">88</span></span>|<span data-ttu-id="77d53-117">已生成 MSIL 存根。</span><span class="sxs-lookup"><span data-stu-id="77d53-117">The MSIL stub has been generated.</span></span>|  
  
 <span data-ttu-id="77d53-118">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="77d53-118">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="77d53-119">字段名称</span><span class="sxs-lookup"><span data-stu-id="77d53-119">Field name</span></span>|<span data-ttu-id="77d53-120">数据类型</span><span class="sxs-lookup"><span data-stu-id="77d53-120">Data type</span></span>|<span data-ttu-id="77d53-121">说明</span><span class="sxs-lookup"><span data-stu-id="77d53-121">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="77d53-122">ModuleID</span><span class="sxs-lookup"><span data-stu-id="77d53-122">ModuleID</span></span>|<span data-ttu-id="77d53-123">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="77d53-123">win:UInt16</span></span>|<span data-ttu-id="77d53-124">模块标识符。</span><span class="sxs-lookup"><span data-stu-id="77d53-124">The module identifier.</span></span>|  
|<span data-ttu-id="77d53-125">StubMethodID</span><span class="sxs-lookup"><span data-stu-id="77d53-125">StubMethodID</span></span>|<span data-ttu-id="77d53-126">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="77d53-126">win:UInt64</span></span>|<span data-ttu-id="77d53-127">存根方法标识符。</span><span class="sxs-lookup"><span data-stu-id="77d53-127">The stub method identifier.</span></span>|  
|<span data-ttu-id="77d53-128">StubFlags</span><span class="sxs-lookup"><span data-stu-id="77d53-128">StubFlags</span></span>|<span data-ttu-id="77d53-129">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="77d53-129">win:UInt64</span></span>|<span data-ttu-id="77d53-130">存根标志：</span><span class="sxs-lookup"><span data-stu-id="77d53-130">The flags for the stub:</span></span><br /><br /> <span data-ttu-id="77d53-131">0x1 - 反向互操作。</span><span class="sxs-lookup"><span data-stu-id="77d53-131">0x1 - Reverse interop.</span></span><br /><br /> <span data-ttu-id="77d53-132">0x2 - COM 互操作。</span><span class="sxs-lookup"><span data-stu-id="77d53-132">0x2 - COM interop.</span></span><br /><br /> <span data-ttu-id="77d53-133">0x4 - 由 NGen.exe 生成的存根。</span><span class="sxs-lookup"><span data-stu-id="77d53-133">0x4 - Stub generated by NGen.exe.</span></span><br /><br /> <span data-ttu-id="77d53-134">0x8 - 委托。</span><span class="sxs-lookup"><span data-stu-id="77d53-134">0x8 - Delegate.</span></span><br /><br /> <span data-ttu-id="77d53-135">0x10-可变参数。</span><span class="sxs-lookup"><span data-stu-id="77d53-135">0x10 - Variable argument.</span></span><br /><br /> <span data-ttu-id="77d53-136">0x20 - 非托管被调用方。</span><span class="sxs-lookup"><span data-stu-id="77d53-136">0x20 - Unmanaged callee.</span></span>|  
|<span data-ttu-id="77d53-137">ManagedInteropMethodToken</span><span class="sxs-lookup"><span data-stu-id="77d53-137">ManagedInteropMethodToken</span></span>|<span data-ttu-id="77d53-138">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="77d53-138">win:UInt32</span></span>|<span data-ttu-id="77d53-139">托管互操作方法的标记。</span><span class="sxs-lookup"><span data-stu-id="77d53-139">The token for the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-140">ManagedInteropMethodNameSpace</span><span class="sxs-lookup"><span data-stu-id="77d53-140">ManagedInteropMethodNameSpace</span></span>|<span data-ttu-id="77d53-141">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-141">win:UnicodeString</span></span>|<span data-ttu-id="77d53-142">托管互操作方法的命名空间。</span><span class="sxs-lookup"><span data-stu-id="77d53-142">The namespace of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-143">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="77d53-143">ManagedInteropMethodName</span></span>|<span data-ttu-id="77d53-144">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-144">win:UnicodeString</span></span>|<span data-ttu-id="77d53-145">托管互操作方法的名称。</span><span class="sxs-lookup"><span data-stu-id="77d53-145">The name of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-146">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="77d53-146">ManagedInteropMethodSignature</span></span>|<span data-ttu-id="77d53-147">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-147">win:UnicodeString</span></span>|<span data-ttu-id="77d53-148">托管互操作方法的签名。</span><span class="sxs-lookup"><span data-stu-id="77d53-148">The signature of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-149">NativeMethodSignature</span><span class="sxs-lookup"><span data-stu-id="77d53-149">NativeMethodSignature</span></span>|<span data-ttu-id="77d53-150">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-150">win:UnicodeString</span></span>|<span data-ttu-id="77d53-151">本机方法签名。</span><span class="sxs-lookup"><span data-stu-id="77d53-151">The native method signature.</span></span>|  
|<span data-ttu-id="77d53-152">StubMethodSignature</span><span class="sxs-lookup"><span data-stu-id="77d53-152">StubMethodSignature</span></span>|<span data-ttu-id="77d53-153">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-153">win:UnicodeString</span></span>|<span data-ttu-id="77d53-154">存根方法签名。</span><span class="sxs-lookup"><span data-stu-id="77d53-154">The stub method signature.</span></span>|  
|<span data-ttu-id="77d53-155">StubMethodILCode</span><span class="sxs-lookup"><span data-stu-id="77d53-155">StubMethodILCode</span></span>|<span data-ttu-id="77d53-156">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-156">win:UnicodeString</span></span>|<span data-ttu-id="77d53-157">存根方法的 MSIL 代码。</span><span class="sxs-lookup"><span data-stu-id="77d53-157">The MSIL code for the stub method.</span></span>|  
|<span data-ttu-id="77d53-158">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="77d53-158">ClrInstanceID</span></span>|<span data-ttu-id="77d53-159">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="77d53-159">win:UInt16</span></span>|<span data-ttu-id="77d53-160">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="77d53-160">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="ilstubcachehit-event"></a><span data-ttu-id="77d53-161">ILStubCacheHit 事件</span><span class="sxs-lookup"><span data-stu-id="77d53-161">ILStubCacheHit Event</span></span>  

<span data-ttu-id="77d53-162">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="77d53-162">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="77d53-163">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="77d53-163">Keyword for raising the event</span></span>|<span data-ttu-id="77d53-164">Level</span><span class="sxs-lookup"><span data-stu-id="77d53-164">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="77d53-165">`InteropKeyword` (0x2000)</span><span class="sxs-lookup"><span data-stu-id="77d53-165">`InteropKeyword` (0x2000)</span></span>|<span data-ttu-id="77d53-166">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="77d53-166">Informational(4)</span></span>|  
  
 <span data-ttu-id="77d53-167">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="77d53-167">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="77d53-168">事件</span><span class="sxs-lookup"><span data-stu-id="77d53-168">Event</span></span>|<span data-ttu-id="77d53-169">事件 ID</span><span class="sxs-lookup"><span data-stu-id="77d53-169">Event ID</span></span>|<span data-ttu-id="77d53-170">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="77d53-170">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ILStubCacheHit`|<span data-ttu-id="77d53-171">89</span><span class="sxs-lookup"><span data-stu-id="77d53-171">89</span></span>|<span data-ttu-id="77d53-172">已访问 MSIL 缓存。</span><span class="sxs-lookup"><span data-stu-id="77d53-172">The MSIL cache has been accessed.</span></span>|  
  
 <span data-ttu-id="77d53-173">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="77d53-173">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="77d53-174">字段名称</span><span class="sxs-lookup"><span data-stu-id="77d53-174">Field name</span></span>|<span data-ttu-id="77d53-175">数据类型</span><span class="sxs-lookup"><span data-stu-id="77d53-175">Data type</span></span>|<span data-ttu-id="77d53-176">说明</span><span class="sxs-lookup"><span data-stu-id="77d53-176">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="77d53-177">ModuleID</span><span class="sxs-lookup"><span data-stu-id="77d53-177">ModuleID</span></span>|<span data-ttu-id="77d53-178">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="77d53-178">win:UInt16</span></span>|<span data-ttu-id="77d53-179">模块标识符。</span><span class="sxs-lookup"><span data-stu-id="77d53-179">The module identifier.</span></span>|  
|<span data-ttu-id="77d53-180">StubMethodID</span><span class="sxs-lookup"><span data-stu-id="77d53-180">StubMethodID</span></span>|<span data-ttu-id="77d53-181">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="77d53-181">win:UInt64</span></span>|<span data-ttu-id="77d53-182">存根方法标识符。</span><span class="sxs-lookup"><span data-stu-id="77d53-182">The stub method identifier.</span></span>|  
|<span data-ttu-id="77d53-183">ManagedInteropMethodToken</span><span class="sxs-lookup"><span data-stu-id="77d53-183">ManagedInteropMethodToken</span></span>|<span data-ttu-id="77d53-184">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="77d53-184">win:UInt32</span></span>|<span data-ttu-id="77d53-185">托管互操作方法的标记。</span><span class="sxs-lookup"><span data-stu-id="77d53-185">The token for the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-186">ManagedInteropMethodNameSpace</span><span class="sxs-lookup"><span data-stu-id="77d53-186">ManagedInteropMethodNameSpace</span></span>|<span data-ttu-id="77d53-187">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-187">win:UnicodeString</span></span>|<span data-ttu-id="77d53-188">托管互操作方法的命名空间。</span><span class="sxs-lookup"><span data-stu-id="77d53-188">The namespace of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-189">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="77d53-189">ManagedInteropMethodName</span></span>|<span data-ttu-id="77d53-190">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-190">win:UnicodeString</span></span>|<span data-ttu-id="77d53-191">托管互操作方法的名称。</span><span class="sxs-lookup"><span data-stu-id="77d53-191">The name of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-192">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="77d53-192">ManagedInteropMethodSignature</span></span>|<span data-ttu-id="77d53-193">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="77d53-193">win:UnicodeString</span></span>|<span data-ttu-id="77d53-194">托管互操作方法的签名。</span><span class="sxs-lookup"><span data-stu-id="77d53-194">The signature of the managed interop method.</span></span>|  
|<span data-ttu-id="77d53-195">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="77d53-195">ClrInstanceID</span></span>|<span data-ttu-id="77d53-196">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="77d53-196">win:UInt16</span></span>|<span data-ttu-id="77d53-197">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="77d53-197">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="77d53-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77d53-198">See also</span></span>

- [<span data-ttu-id="77d53-199">CLR ETW 事件</span><span class="sxs-lookup"><span data-stu-id="77d53-199">CLR ETW Events</span></span>](clr-etw-events.md)
