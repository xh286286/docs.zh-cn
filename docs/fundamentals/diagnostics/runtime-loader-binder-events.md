---
title: 加载器和联编程序运行时事件
description: 请参阅收集特定于加载程序的诊断信息和联编程序 ETW 事件的 .NET 运行时事件，这些事件收集有关程序集加载程序和联编程序的信息。
ms.date: 11/13/2020
ms.topic: reference
helpviewer_keywords:
- Assembly Loader events (CoreCLR)
- Assembly Binder events (CoreCLR)
- ETW, EventPipe, LTTng assembly loader and binder events (CoreCLR)
ms.openlocfilehash: 2284c580482f6b93a77f44649225ff7e5485666a
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96591079"
---
# <a name="net-runtime-loader-and-binder-events"></a><span data-ttu-id="d600a-103">.NET 运行时加载程序和联编程序事件</span><span class="sxs-lookup"><span data-stu-id="d600a-103">.NET runtime loader and binder events</span></span>

<span data-ttu-id="d600a-104">这些事件将收集与加载和卸载程序集和模块相关的信息。</span><span class="sxs-lookup"><span data-stu-id="d600a-104">These events collect information relating to loading and unloading assemblies and modules.</span></span> <span data-ttu-id="d600a-105">有关如何将这些事件用于诊断的详细信息，请参阅 [日志记录和跟踪 .net 应用程序](../../core/diagnostics/logging-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="d600a-105">For more information about how to use these events for diagnostic purposes, see [logging and tracing .NET applications](../../core/diagnostics/logging-tracing.md)</span></span>

|<span data-ttu-id="d600a-106">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-106">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-107">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-107">Event</span></span>|<span data-ttu-id="d600a-108">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-108">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-109">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-109">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-110">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-110">Informational (4)</span></span>|

|<span data-ttu-id="d600a-111">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-111">Event</span></span>|<span data-ttu-id="d600a-112">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-112">Event ID</span></span>|<span data-ttu-id="d600a-113">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-113">Description</span></span>|
|-----------|--------------|-----------------|
|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-114">151</span><span class="sxs-lookup"><span data-stu-id="d600a-114">151</span></span>|<span data-ttu-id="d600a-115">在为应用程序域加载模块时引发。</span><span class="sxs-lookup"><span data-stu-id="d600a-115">Raised when a module is loaded for an application domain.</span></span>|

## <a name="moduleload_v2-event"></a><span data-ttu-id="d600a-116">ModuleLoad_V2 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-116">ModuleLoad_V2 event</span></span>

|<span data-ttu-id="d600a-117">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-117">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-118">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-118">Event</span></span>|<span data-ttu-id="d600a-119">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-119">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-120">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-120">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-121">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-121">Informational (4)</span></span>|

|<span data-ttu-id="d600a-122">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-122">Event</span></span>|<span data-ttu-id="d600a-123">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-123">Event ID</span></span>|<span data-ttu-id="d600a-124">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-124">Description</span></span>|
|-----------|--------------|-----------------|
|`ModuleLoad_V2`|<span data-ttu-id="d600a-125">152</span><span class="sxs-lookup"><span data-stu-id="d600a-125">152</span></span>|<span data-ttu-id="d600a-126">在进程的生存期内加载模块时引发。</span><span class="sxs-lookup"><span data-stu-id="d600a-126">Raised when a module is loaded during the lifetime of a process.</span></span>|

|<span data-ttu-id="d600a-127">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-127">Field name</span></span>|<span data-ttu-id="d600a-128">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-128">Data type</span></span>|<span data-ttu-id="d600a-129">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-129">Description</span></span>|
|----------------|---------------|-----------------|
|`ModuleID`|`win:UInt64`|<span data-ttu-id="d600a-130">模块的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-130">Unique ID for the module.</span></span>|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-131">此模块所驻留的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-131">ID of the assembly in which this module resides.</span></span>|
|`ModuleFlags`|`win:UInt32`|<span data-ttu-id="d600a-132">0x1：非特定于域的模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-132">0x1: Domain neutral module.</span></span><br /><br /> <span data-ttu-id="d600a-133">0x2：模块具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-133">0x2: Module has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-134">0x4：动态模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-134">0x4: Dynamic module.</span></span><br /><br /> <span data-ttu-id="d600a-135">0x8：清单模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-135">0x8: Manifest module.</span></span>|
|`Reserved1`|`win:UInt32`|<span data-ttu-id="d600a-136">保留的字段。</span><span class="sxs-lookup"><span data-stu-id="d600a-136">Reserved field.</span></span>|
|`ModuleILPath`|`win:UnicodeString`|<span data-ttu-id="d600a-137">适用于模块的公共中间语言 (CIL) 图像的路径; 如果是动态程序集，则为动态模块名称 (以 null 终止) 。</span><span class="sxs-lookup"><span data-stu-id="d600a-137">Path of the Common Intermediate Language (CIL) image for the module, or dynamic module name if it is a dynamic assembly (null-terminated).</span></span>|
|`ModuleNativePath`|`win:UnicodeString`|<span data-ttu-id="d600a-138">如果存在（以 null 结尾），则为模块本机映像的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-138">Path of the module native image, if present (null-terminated).</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-139">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-139">Unique ID for the instance of CLR or CoreCLR.</span></span>|
|`ManagedPdbSignature`|`win:GUID`|<span data-ttu-id="d600a-140">匹配此模块的托管程序数据库 (PDB) 的 GUID 签名。</span><span class="sxs-lookup"><span data-stu-id="d600a-140">GUID signature of the managed program database (PDB) that matches this module.</span></span>|
|`ManagedPdbAge`|`win:UInt32`|<span data-ttu-id="d600a-141">写入匹配此模块的托管 PDB 的年限数。</span><span class="sxs-lookup"><span data-stu-id="d600a-141">Age number written to the managed PDB that matches this module.</span></span>|
|`ManagedPdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-142">生成匹配此模块的托管 PDB 的位置的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-142">Path to the location where the managed PDB that matches this module was built.</span></span> <span data-ttu-id="d600a-143">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-143">In some cases, this may just be a file name.</span></span>|
|`NativePdbSignature`|`win:GUID`|<span data-ttu-id="d600a-144">匹配此模块的本机映像生成器 (NGen) PDB 的 GUID 签名（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-144">GUID signature of the Native Image Generator (NGen) PDB that matches this module, if applicable.</span></span>|
|`NativePdbAge`|`win:UInt32`|<span data-ttu-id="d600a-145">写入匹配此模块的 NGen PDB 的年限数（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-145">Age number written to the NGen PDB that matches this module, if applicable.</span></span>|
|`NativePdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-146">生成匹配此模块的 NGen PDB 的位置的路径（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-146">Path to the location where the NGen PDB that matches this module was built, if applicable.</span></span> <span data-ttu-id="d600a-147">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-147">In some cases, this may just be a file name.</span></span>|

## <a name="moduleunload_v2-event"></a><span data-ttu-id="d600a-148">ModuleUnload_V2 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-148">ModuleUnload_V2 event</span></span>

|<span data-ttu-id="d600a-149">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-149">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-150">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-150">Event</span></span>|<span data-ttu-id="d600a-151">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-151">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-152">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-152">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-153">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-153">Informational (4)</span></span>|

|<span data-ttu-id="d600a-154">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-154">Event</span></span>|<span data-ttu-id="d600a-155">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-155">Event ID</span></span>|<span data-ttu-id="d600a-156">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-156">Description</span></span>|
|-----------|--------------|-----------------|
|`ModuleUnload_V2`|<span data-ttu-id="d600a-157">153</span><span class="sxs-lookup"><span data-stu-id="d600a-157">153</span></span>|<span data-ttu-id="d600a-158">在进程的生存期内卸载模块时引发。</span><span class="sxs-lookup"><span data-stu-id="d600a-158">Raised when a module is unloaded during the lifetime of a process.</span></span>|

|<span data-ttu-id="d600a-159">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-159">Field name</span></span>|<span data-ttu-id="d600a-160">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-160">Data type</span></span>|<span data-ttu-id="d600a-161">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-161">Description</span></span>|
|----------------|---------------|-----------------|
|`ModuleID`|`win:UInt64`|<span data-ttu-id="d600a-162">模块的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-162">Unique ID for the module.</span></span>|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-163">此模块所驻留的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-163">ID of the assembly in which this module resides.</span></span>|
|`ModuleFlags`|`win:UInt32`|<span data-ttu-id="d600a-164">0x1：非特定于域的模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-164">0x1: Domain neutral module.</span></span><br /><br /> <span data-ttu-id="d600a-165">0x2：模块具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-165">0x2: Module has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-166">0x4：动态模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-166">0x4: Dynamic module.</span></span><br /><br /> <span data-ttu-id="d600a-167">0x8：清单模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-167">0x8: Manifest module.</span></span>|
|`Reserved1`|`win:UInt32`|<span data-ttu-id="d600a-168">保留的字段。</span><span class="sxs-lookup"><span data-stu-id="d600a-168">Reserved field.</span></span>|
|`ModuleILPath`|`win:UnicodeString`|<span data-ttu-id="d600a-169">适用于模块的公共中间语言 (CIL) 图像的路径; 如果是动态程序集，则为动态模块名称 (以 null 终止) 。</span><span class="sxs-lookup"><span data-stu-id="d600a-169">Path of the Common Intermediate Language (CIL) image for the module, or dynamic module name if it is a dynamic assembly (null-terminated).</span></span>|
|`ModuleNativePath`|`win:UnicodeString`|<span data-ttu-id="d600a-170">如果存在（以 null 结尾），则为模块本机映像的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-170">Path of the module native image, if present (null-terminated).</span></span>|
|`ClrInstanceID`|``win:UInt16``|<span data-ttu-id="d600a-171">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-171">Unique ID for the instance of CLR or CoreCLR.</span></span>|
|`ManagedPdbSignature`|`win:GUID`|<span data-ttu-id="d600a-172">匹配此模块的托管程序数据库 (PDB) 的 GUID 签名。</span><span class="sxs-lookup"><span data-stu-id="d600a-172">GUID signature of the managed program database (PDB) that matches this module.</span></span>|
|`ManagedPdbAge`|`win:UInt32`|<span data-ttu-id="d600a-173">写入匹配此模块的托管 PDB 的年限数。</span><span class="sxs-lookup"><span data-stu-id="d600a-173">Age number written to the managed PDB that matches this module.</span></span>|
|`ManagedPdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-174">生成匹配此模块的托管 PDB 的位置的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-174">Path to the location where the managed PDB that matches this module was built.</span></span> <span data-ttu-id="d600a-175">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-175">In some cases, this may just be a file name.</span></span>|
|`NativePdbSignature`|`win:GUID`|<span data-ttu-id="d600a-176">匹配此模块的本机映像生成器 (NGen) PDB 的 GUID 签名（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-176">GUID signature of the Native Image Generator (NGen) PDB that matches this module, if applicable.</span></span>|
|`NativePdbAge`|`win:UInt32`|<span data-ttu-id="d600a-177">写入匹配此模块的 NGen PDB 的年限数（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-177">Age number written to the NGen PDB that matches this module, if applicable.</span></span>|
|`NativePdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-178">生成匹配此模块的 NGen PDB 的位置的路径（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-178">Path to the location where the NGen PDB that matches this module was built, if applicable.</span></span> <span data-ttu-id="d600a-179">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-179">In some cases, this may just be a file name.</span></span>|

## <a name="moduledcstart_v2-event"></a><span data-ttu-id="d600a-180">ModuleDCStart_V2 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-180">ModuleDCStart_V2 event</span></span>

|<span data-ttu-id="d600a-181">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-181">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-182">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-182">Event</span></span>|<span data-ttu-id="d600a-183">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-183">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-184">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-184">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-185">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-185">Informational (4)</span></span>

|<span data-ttu-id="d600a-186">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-186">Event</span></span>|<span data-ttu-id="d600a-187">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-187">Event ID</span></span>|<span data-ttu-id="d600a-188">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-188">Description</span></span>
|-----------|--------------|-----------------|
|`ModuleDCStart_V2`|<span data-ttu-id="d600a-189">153</span><span class="sxs-lookup"><span data-stu-id="d600a-189">153</span></span>|<span data-ttu-id="d600a-190">在启动断开期间枚举模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-190">Enumerates modules during a start rundown.</span></span>|

|<span data-ttu-id="d600a-191">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-191">Field name</span></span>|<span data-ttu-id="d600a-192">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-192">Data type</span></span>|<span data-ttu-id="d600a-193">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-193">Description</span></span>|
|----------------|---------------|-----------------|
|`ModuleID`|`win:UInt64`|<span data-ttu-id="d600a-194">模块的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-194">Unique ID for the module.</span></span>|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-195">此模块所驻留的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-195">ID of the assembly in which this module resides.</span></span>|
|`ModuleFlags`|`win:UInt32`|<span data-ttu-id="d600a-196">0x1：非特定于域的模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-196">0x1: Domain neutral module.</span></span><br /><br /> <span data-ttu-id="d600a-197">0x2：模块具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-197">0x2: Module has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-198">0x4：动态模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-198">0x4: Dynamic module.</span></span><br /><br /> <span data-ttu-id="d600a-199">0x8：清单模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-199">0x8: Manifest module.</span></span>|
|`Reserved1`|`win:UInt32`|<span data-ttu-id="d600a-200">保留的字段。</span><span class="sxs-lookup"><span data-stu-id="d600a-200">Reserved field.</span></span>|
|`ModuleILPath`|`win:UnicodeString`|<span data-ttu-id="d600a-201">适用于模块的公共中间语言 (CIL) 图像的路径; 如果是动态程序集，则为动态模块名称 (以 null 终止) 。</span><span class="sxs-lookup"><span data-stu-id="d600a-201">Path of the Common Intermediate Language (CIL) image for the module, or dynamic module name if it is a dynamic assembly (null-terminated).</span></span>|
|`ModuleNativePath`|`win:UnicodeString`|<span data-ttu-id="d600a-202">如果存在（以 null 结尾），则为模块本机映像的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-202">Path of the module native image, if present (null-terminated).</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-203">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-203">Unique ID for the instance of CLR or CoreCLR.</span></span>|
|`ManagedPdbSignature`|`win:GUID`|<span data-ttu-id="d600a-204">匹配此模块的托管程序数据库 (PDB) 的 GUID 签名。</span><span class="sxs-lookup"><span data-stu-id="d600a-204">GUID signature of the managed program database (PDB) that matches this module.</span></span>|
|`ManagedPdbAge`|`win:UInt32`|<span data-ttu-id="d600a-205">写入匹配此模块的托管 PDB 的年限数。</span><span class="sxs-lookup"><span data-stu-id="d600a-205">Age number written to the managed PDB that matches this module.</span></span>|
|`ManagedPdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-206">生成匹配此模块的托管 PDB 的位置的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-206">Path to the location where the managed PDB that matches this module was built.</span></span> <span data-ttu-id="d600a-207">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-207">In some cases, this may just be a file name.</span></span>|
|`NativePdbSignature`|`win:GUID`|<span data-ttu-id="d600a-208">匹配此模块的本机映像生成器 (NGen) PDB 的 GUID 签名（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-208">GUID signature of the Native Image Generator (NGen) PDB that matches this module, if applicable.</span></span>|
|`NativePdbAge`|`win:UInt32`|<span data-ttu-id="d600a-209">写入匹配此模块的 NGen PDB 的年限数（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-209">Age number written to the NGen PDB that matches this module, if applicable.</span></span>|
|`NativePdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-210">生成匹配此模块的 NGen PDB 的位置的路径（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-210">Path to the location where the NGen PDB that matches this module was built, if applicable.</span></span> <span data-ttu-id="d600a-211">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-211">In some cases, this may just be a file name.</span></span>|

## <a name="moduledcend_v2-event"></a><span data-ttu-id="d600a-212">ModuleDCEnd_V2 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-212">ModuleDCEnd_V2 event</span></span>

|<span data-ttu-id="d600a-213">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-213">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-214">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-214">Event</span></span>|<span data-ttu-id="d600a-215">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-215">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-216">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-216">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-217">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-217">Informational (4)</span></span>|

|<span data-ttu-id="d600a-218">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-218">Event</span></span>|<span data-ttu-id="d600a-219">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-219">Event ID</span></span>|<span data-ttu-id="d600a-220">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-220">Description</span></span>|
|-----------|--------------|-----------------|
|`ModuleDCEnd_V2`|<span data-ttu-id="d600a-221">154</span><span class="sxs-lookup"><span data-stu-id="d600a-221">154</span></span>|<span data-ttu-id="d600a-222">在结束断开期间枚举模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-222">Enumerates modules during an end rundown.</span></span>|

|<span data-ttu-id="d600a-223">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-223">Field name</span></span>|<span data-ttu-id="d600a-224">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-224">Data type</span></span>|<span data-ttu-id="d600a-225">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-225">Description</span></span>|
|----------------|---------------|-----------------|
|`ModuleID`|`win:UInt64`|<span data-ttu-id="d600a-226">模块的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-226">Unique ID for the module.</span></span>|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-227">此模块所驻留的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-227">ID of the assembly in which this module resides.</span></span>|
|`ModuleFlags`|`win:UInt32`|<span data-ttu-id="d600a-228">0x1：非特定于域的模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-228">0x1: Domain neutral module.</span></span><br /><br /> <span data-ttu-id="d600a-229">0x2：模块具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-229">0x2: Module has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-230">0x4：动态模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-230">0x4: Dynamic module.</span></span><br /><br /> <span data-ttu-id="d600a-231">0x8：清单模块。</span><span class="sxs-lookup"><span data-stu-id="d600a-231">0x8: Manifest module.</span></span>|
|`Reserved1`|`win:UInt32`|<span data-ttu-id="d600a-232">保留的字段。</span><span class="sxs-lookup"><span data-stu-id="d600a-232">Reserved field.</span></span>|
|`ModuleILPath`|`win:UnicodeString`|<span data-ttu-id="d600a-233">适用于模块的公共中间语言 (CIL) 图像的路径; 如果是动态程序集，则为动态模块名称 (以 null 终止) 。</span><span class="sxs-lookup"><span data-stu-id="d600a-233">Path of the Common Intermediate Language (CIL) image for the module, or dynamic module name if it is a dynamic assembly (null-terminated).</span></span>|
|`ModuleNativePath`|`win:UnicodeString`|<span data-ttu-id="d600a-234">如果存在（以 null 结尾），则为模块本机映像的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-234">Path of the module native image, if present (null-terminated).</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-235">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-235">Unique ID for the instance of CLR or CoreCLR.</span></span>|
|`ManagedPdbSignature`|`win:GUID`|<span data-ttu-id="d600a-236">匹配此模块的托管程序数据库 (PDB) 的 GUID 签名。</span><span class="sxs-lookup"><span data-stu-id="d600a-236">GUID signature of the managed program database (PDB) that matches this module.</span></span>|
|`ManagedPdbAge`|`win:UInt32`|<span data-ttu-id="d600a-237">写入匹配此模块的托管 PDB 的年限数。</span><span class="sxs-lookup"><span data-stu-id="d600a-237">Age number written to the managed PDB that matches this module.</span></span>|
|`ManagedPdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-238">生成匹配此模块的托管 PDB 的位置的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-238">Path to the location where the managed PDB that matches this module was built.</span></span> <span data-ttu-id="d600a-239">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-239">In some cases, this may just be a file name.</span></span>|
|`NativePdbSignature`|`win:GUID`|<span data-ttu-id="d600a-240">匹配此模块的本机映像生成器 (NGen) PDB 的 GUID 签名（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-240">GUID signature of the Native Image Generator (NGen) PDB that matches this module, if applicable.</span></span>|
|`NativePdbAge`|`win:UInt32`|<span data-ttu-id="d600a-241">写入匹配此模块的 NGen PDB 的年限数（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-241">Age number written to the NGen PDB that matches this module, if applicable.</span></span>|
|`NativePdbBuildPath`|`win:UnicodeString`|<span data-ttu-id="d600a-242">生成匹配此模块的 NGen PDB 的位置的路径（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d600a-242">Path to the location where the NGen PDB that matches this module was built, if applicable.</span></span> <span data-ttu-id="d600a-243">在某些情况下，这可能只是一个文件名。</span><span class="sxs-lookup"><span data-stu-id="d600a-243">In some cases, this may just be a file name.</span></span>|

## <a name="assemblyload_v1-event"></a><span data-ttu-id="d600a-244">AssemblyLoad_V1 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-244">AssemblyLoad_V1 event</span></span>

|<span data-ttu-id="d600a-245">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-245">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-246">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-246">Event</span></span>|<span data-ttu-id="d600a-247">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-247">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-248">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-248">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-249">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-249">Informational (4)</span></span>|

|<span data-ttu-id="d600a-250">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-250">Event</span></span>|<span data-ttu-id="d600a-251">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-251">Event ID</span></span>|<span data-ttu-id="d600a-252">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-252">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyLoad_V1`|<span data-ttu-id="d600a-253">154</span><span class="sxs-lookup"><span data-stu-id="d600a-253">154</span></span>|<span data-ttu-id="d600a-254">在加载程序集时引发。</span><span class="sxs-lookup"><span data-stu-id="d600a-254">Raised when an assembly is loaded.</span></span>|

|<span data-ttu-id="d600a-255">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-255">Field name</span></span>|<span data-ttu-id="d600a-256">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-256">Data type</span></span>|<span data-ttu-id="d600a-257">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-257">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-258">程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-258">Unique ID for the assembly.</span></span>|
|`AppDomainID`|`win:UInt64`|<span data-ttu-id="d600a-259">此程序集的域的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-259">ID of the domain of this assembly.</span></span>|
|`BindingID`|`win:UInt64`|<span data-ttu-id="d600a-260">唯一地标识程序集绑定的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-260">ID that uniquely identifies the assembly binding.</span></span>|
|`AssemblyFlags`|`win:UInt32`|<span data-ttu-id="d600a-261">0x1：非特定于域的程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-261">0x1: Domain neutral assembly.</span></span><br /><br /> <span data-ttu-id="d600a-262">0x2：动态程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-262">0x2: Dynamic assembly.</span></span><br /><br /> <span data-ttu-id="d600a-263">0x4：程序集具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-263">0x4: Assembly has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-264">0x8：可回收程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-264">0x8: Collectible assembly.</span></span>|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-265">完全限定程序集名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-265">Fully qualified assembly name.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-266">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-266">Unique ID for the instance of CoreCLR.</span></span>

## <a name="assemblyunload_v1-event"></a><span data-ttu-id="d600a-267">AssemblyUnload_V1 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-267">AssemblyUnload_V1 event</span></span>

|<span data-ttu-id="d600a-268">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-268">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-269">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-269">Event</span></span>|<span data-ttu-id="d600a-270">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-270">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-271">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-271">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-272">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-272">Informational (4)</span></span>|

|<span data-ttu-id="d600a-273">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-273">Event</span></span>|<span data-ttu-id="d600a-274">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-274">Event ID</span></span>|<span data-ttu-id="d600a-275">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-275">Description</span></span>|
|-----------|--------------|-----------------|
|`FireAssemblyUnload_V1`|<span data-ttu-id="d600a-276">155</span><span class="sxs-lookup"><span data-stu-id="d600a-276">155</span></span>|<span data-ttu-id="d600a-277">在加载程序集时引发。</span><span class="sxs-lookup"><span data-stu-id="d600a-277">Raised when an assembly is loaded.</span></span>|

|<span data-ttu-id="d600a-278">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-278">Field name</span></span>|<span data-ttu-id="d600a-279">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-279">Data type</span></span>|<span data-ttu-id="d600a-280">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-280">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-281">程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-281">Unique ID for the assembly.</span></span>|
|`AppDomainID`|`win:UInt64`|<span data-ttu-id="d600a-282">此程序集的域的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-282">ID of the domain of this assembly.</span></span>|
|`BindingID`|`win:UInt64`|<span data-ttu-id="d600a-283">唯一地标识程序集绑定的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-283">ID that uniquely identifies the assembly binding.</span></span>|
|`AssemblyFlags`|`win:UInt32`|<span data-ttu-id="d600a-284">0x1：非特定于域的程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-284">0x1: Domain neutral assembly.</span></span><br /><br /> <span data-ttu-id="d600a-285">0x2：动态程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-285">0x2: Dynamic assembly.</span></span><br /><br /> <span data-ttu-id="d600a-286">0x4：程序集具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-286">0x4: Assembly has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-287">0x8：可回收程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-287">0x8: Collectible assembly.</span></span>|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-288">完全限定程序集名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-288">Fully qualified assembly name.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-289">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-289">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="assemblydcstart_v1-event"></a><span data-ttu-id="d600a-290">AssemblyDCStart_V1 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-290">AssemblyDCStart_V1 event</span></span>

|<span data-ttu-id="d600a-291">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-291">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-292">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-292">Event</span></span>|<span data-ttu-id="d600a-293">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-293">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-294">`LoaderKeyword` (0x8)</span><span class="sxs-lookup"><span data-stu-id="d600a-294">`LoaderKeyword` (0x8)</span></span>|`DomainModuleLoad_V1`|<span data-ttu-id="d600a-295">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-295">Informational (4)</span></span>|

|<span data-ttu-id="d600a-296">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-296">Event</span></span>|<span data-ttu-id="d600a-297">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-297">Event ID</span></span>|<span data-ttu-id="d600a-298">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-298">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyDCStart_V1`|<span data-ttu-id="d600a-299">155</span><span class="sxs-lookup"><span data-stu-id="d600a-299">155</span></span>|<span data-ttu-id="d600a-300">在启动断开期间枚举程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-300">Enumerates assemblies during a start rundown.</span></span>|

|<span data-ttu-id="d600a-301">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-301">Field name</span></span>|<span data-ttu-id="d600a-302">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-302">Data type</span></span>|<span data-ttu-id="d600a-303">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-303">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyID`|`win:UInt64`|<span data-ttu-id="d600a-304">程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-304">Unique ID for the assembly.</span></span>|
|`AppDomainID`|`win:UInt64`|<span data-ttu-id="d600a-305">此程序集的域的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-305">ID of the domain of this assembly.</span></span>|
|`BindingID`|`win:UInt64`|<span data-ttu-id="d600a-306">唯一地标识程序集绑定的 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-306">ID that uniquely identifies the assembly binding.</span></span>|
|`AssemblyFlags`|`win:UInt32`|<span data-ttu-id="d600a-307">0x1：非特定于域的程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-307">0x1: Domain neutral assembly.</span></span><br /><br /> <span data-ttu-id="d600a-308">0x2：动态程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-308">0x2: Dynamic assembly.</span></span><br /><br /> <span data-ttu-id="d600a-309">0x4：程序集具有本机映像。</span><span class="sxs-lookup"><span data-stu-id="d600a-309">0x4: Assembly has a native image.</span></span><br /><br /> <span data-ttu-id="d600a-310">0x8：可回收程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-310">0x8: Collectible assembly.</span></span>|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-311">完全限定程序集名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-311">Fully qualified assembly name.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-312">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-312">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="assemblyloadstart-event"></a><span data-ttu-id="d600a-313">AssemblyLoadStart 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-313">AssemblyLoadStart event</span></span>

|<span data-ttu-id="d600a-314">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-314">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-315">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-315">Event</span></span>|<span data-ttu-id="d600a-316">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-316">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-317">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-317">`Binder` (0x4)</span></span>|`AssemblyLoadStart`|<span data-ttu-id="d600a-318">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-318">Informational (4)</span></span>|

|<span data-ttu-id="d600a-319">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-319">Event</span></span>|<span data-ttu-id="d600a-320">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-320">Event ID</span></span>|<span data-ttu-id="d600a-321">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-321">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyLoadStart`|<span data-ttu-id="d600a-322">290</span><span class="sxs-lookup"><span data-stu-id="d600a-322">290</span></span>|<span data-ttu-id="d600a-323">已请求程序集加载。</span><span class="sxs-lookup"><span data-stu-id="d600a-323">An assembly load has been requested.</span></span>

|<span data-ttu-id="d600a-324">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-324">Field name</span></span>|<span data-ttu-id="d600a-325">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-325">Data type</span></span>|<span data-ttu-id="d600a-326">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-326">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-327">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-327">Name of assembly name.</span></span>|
|`AssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-328">程序集名称的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-328">Path of assembly name.</span></span>|
|`RequestingAssembly`|`win:UnicodeString`|<span data-ttu-id="d600a-329">请求 ( "parent" ) 程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-329">Name of the requesting ("parent") assembly.</span></span>|
|`AssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-330">加载程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-330">Load context of the assembly.</span></span>|
|`RequestingAssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-331">加载请求 ( "parent" ) 程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-331">Load context of the requesting ("parent") assembly.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-332">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-332">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="assemblyloadstop-event"></a><span data-ttu-id="d600a-333">AssemblyLoadStop 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-333">AssemblyLoadStop event</span></span>

|<span data-ttu-id="d600a-334">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-334">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-335">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-335">Event</span></span>|<span data-ttu-id="d600a-336">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-336">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-337">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-337">`Binder` (0x4)</span></span>|`AssemblyLoadStart`|<span data-ttu-id="d600a-338">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-338">Informational (4)</span></span>|

|<span data-ttu-id="d600a-339">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-339">Event</span></span>|<span data-ttu-id="d600a-340">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-340">Event ID</span></span>|<span data-ttu-id="d600a-341">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-341">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyLoadStart`|<span data-ttu-id="d600a-342">291</span><span class="sxs-lookup"><span data-stu-id="d600a-342">291</span></span>|<span data-ttu-id="d600a-343">已请求程序集加载。</span><span class="sxs-lookup"><span data-stu-id="d600a-343">An assembly load has been requested.</span></span>

|<span data-ttu-id="d600a-344">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-344">Field name</span></span>|<span data-ttu-id="d600a-345">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-345">Data type</span></span>|<span data-ttu-id="d600a-346">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-346">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-347">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-347">Name of assembly name.</span></span>|
|`AssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-348">程序集名称的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-348">Path of assembly name.</span></span>|
|`RequestingAssembly`|`win:UnicodeString`|<span data-ttu-id="d600a-349">请求 ( "parent" ) 程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-349">Name of the requesting ("parent") assembly.</span></span>|
|`AssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-350">加载程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-350">Load context of the assembly.</span></span>|
|`RequestingAssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-351">加载请求 ( "parent" ) 程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-351">Load context of the requesting ("parent") assembly.</span></span>|
|`Success`|`win:Boolean`|<span data-ttu-id="d600a-352">程序集加载是否成功。</span><span class="sxs-lookup"><span data-stu-id="d600a-352">Whether the assembly load succeeded.</span></span>|
|`ResultAssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-353">已加载的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-353">The name of assembly that was loaded.</span></span>|
|`ResultAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-354">从加载的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-354">The path of the assembly that was loaded from.</span></span>|
|`Cached`|`win:UnicodeString`|<span data-ttu-id="d600a-355">是否缓存了负载。</span><span class="sxs-lookup"><span data-stu-id="d600a-355">Whether the load was cached.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-356">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-356">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="resolutionattempted-event"></a><span data-ttu-id="d600a-357">ResolutionAttempted 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-357">ResolutionAttempted event</span></span>

|<span data-ttu-id="d600a-358">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-358">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-359">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-359">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-360">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-360">`Binder` (0x4)</span></span>|<span data-ttu-id="d600a-361">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-361">Informational (4)</span></span>|

|<span data-ttu-id="d600a-362">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-362">Event</span></span>|<span data-ttu-id="d600a-363">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-363">Event ID</span></span>|<span data-ttu-id="d600a-364">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-364">Description</span></span>|
|-----------|--------------|-----------------|
|`ResolutionAttempted`|<span data-ttu-id="d600a-365">292</span><span class="sxs-lookup"><span data-stu-id="d600a-365">292</span></span>|<span data-ttu-id="d600a-366">已请求程序集加载。</span><span class="sxs-lookup"><span data-stu-id="d600a-366">An assembly load has been requested.</span></span>

|<span data-ttu-id="d600a-367">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-367">Field name</span></span>|<span data-ttu-id="d600a-368">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-368">Data type</span></span>|<span data-ttu-id="d600a-369">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-369">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-370">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-370">Name of assembly name.</span></span>|
|`Stage`|`win:UInt16`|<span data-ttu-id="d600a-371">解决阶段。</span><span class="sxs-lookup"><span data-stu-id="d600a-371">The resolution stage.</span></span><br/><br/><span data-ttu-id="d600a-372">0：在加载中查找。</span><span class="sxs-lookup"><span data-stu-id="d600a-372">0: Find in load.</span></span><br/><br/><span data-ttu-id="d600a-373">1：程序集加载上下文</span><span class="sxs-lookup"><span data-stu-id="d600a-373">1: Assembly Load Context</span></span></br><br/><span data-ttu-id="d600a-374">2：应用程序程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-374">2: Application assemblies.</span></span><br/><br/><span data-ttu-id="d600a-375">3：默认程序集加载上下文回退。</span><span class="sxs-lookup"><span data-stu-id="d600a-375">3: Default assembly load context fallback.</span></span> <br/><br/><span data-ttu-id="d600a-376">4：解析附属程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-376">4: Resolve satellite assembly.</span></span> <br/><br/><span data-ttu-id="d600a-377">5：程序集加载上下文正在解析。</span><span class="sxs-lookup"><span data-stu-id="d600a-377">5: Assembly load context resolving.</span></span><br/><br/><span data-ttu-id="d600a-378">6： AppDomain 程序集正在解析。</span><span class="sxs-lookup"><span data-stu-id="d600a-378">6: AppDomain assembly resolving.</span></span>
|`AssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-379">加载程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-379">Load context of the assembly.</span></span>|
|`Result`|`win:UInt16`|<span data-ttu-id="d600a-380">解析尝试的结果。</span><span class="sxs-lookup"><span data-stu-id="d600a-380">The result of resolution attempt.</span></span><br/><br/><span data-ttu-id="d600a-381">0：成功</span><span class="sxs-lookup"><span data-stu-id="d600a-381">0: Success</span></span><br/><br/><span data-ttu-id="d600a-382">1：程序集 NotFound</span><span class="sxs-lookup"><span data-stu-id="d600a-382">1: Assembly NotFound</span></span><br/><br/><span data-ttu-id="d600a-383">2：版本不兼容</span><span class="sxs-lookup"><span data-stu-id="d600a-383">2: Incompatible Version</span></span><br/><br/><span data-ttu-id="d600a-384">3：程序集名称不匹配</span><span class="sxs-lookup"><span data-stu-id="d600a-384">3: Mismatched Assembly Name</span></span><br/><br/><span data-ttu-id="d600a-385">4：失败</span><span class="sxs-lookup"><span data-stu-id="d600a-385">4: Failure</span></span><br/><br/><span data-ttu-id="d600a-386">5：异常</span><span class="sxs-lookup"><span data-stu-id="d600a-386">5: Exception</span></span>|
|`ResultAssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-387">已解析的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-387">The name of assembly that was resolved.</span></span>|
|`ResultAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-388">从中解析的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-388">The path of the assembly that was resolved from.</span></span>|
|`ErrorMessage`|`win:UnicodeString`|<span data-ttu-id="d600a-389">发生异常时的错误消息。</span><span class="sxs-lookup"><span data-stu-id="d600a-389">Error message if there is an exception.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-390">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-390">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="assemblyloadcontextresolvinghandlerinvoked-event"></a><span data-ttu-id="d600a-391">AssemblyLoadContextResolvingHandlerInvoked 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-391">AssemblyLoadContextResolvingHandlerInvoked event</span></span>

|<span data-ttu-id="d600a-392">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-392">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-393">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-393">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-394">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-394">`Binder` (0x4)</span></span>|<span data-ttu-id="d600a-395">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-395">Informational (4)</span></span>|

|<span data-ttu-id="d600a-396">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-396">Event</span></span>|<span data-ttu-id="d600a-397">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-397">Event ID</span></span>|<span data-ttu-id="d600a-398">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-398">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyLoadContextResolvingHandlerInvoked`|<span data-ttu-id="d600a-399">293</span><span class="sxs-lookup"><span data-stu-id="d600a-399">293</span></span>|<span data-ttu-id="d600a-400">已调用 [AssemblyLoadContext](xref:System.Runtime.Loader.AssemblyLoadContext.Resolving) 处理程序。</span><span class="sxs-lookup"><span data-stu-id="d600a-400">An [AssemblyLoadContext.Resolving](xref:System.Runtime.Loader.AssemblyLoadContext.Resolving) handler has been invoked.</span></span>|

|<span data-ttu-id="d600a-401">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-401">Field name</span></span>|<span data-ttu-id="d600a-402">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-402">Data type</span></span>|<span data-ttu-id="d600a-403">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-403">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-404">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-404">Name of assembly name.</span></span>|
|`HandlerName`|`win:UnicodeString`|<span data-ttu-id="d600a-405">调用的处理程序的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-405">Name of the handler invoked.</span></span>|
|`AssemblyLoadContext`|`win:UnicodeString`|<span data-ttu-id="d600a-406">加载程序集的上下文。</span><span class="sxs-lookup"><span data-stu-id="d600a-406">Load context of the assembly.</span></span>|
|`ResultAssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-407">已解析的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-407">The name of assembly that was resolved.</span></span>|
|`ResultAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-408">从中解析的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-408">The path of the assembly that was resolved from.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-409">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-409">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="appdomainassemblyresolvehandlerinvoked-event"></a><span data-ttu-id="d600a-410">AppDomainAssemblyResolveHandlerInvoked 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-410">AppDomainAssemblyResolveHandlerInvoked event</span></span>

|<span data-ttu-id="d600a-411">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-411">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-412">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-412">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-413">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-413">`Binder` (0x4)</span></span>|<span data-ttu-id="d600a-414">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-414">Informational (4)</span></span>|

|<span data-ttu-id="d600a-415">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-415">Event</span></span>|<span data-ttu-id="d600a-416">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-416">Event ID</span></span>|<span data-ttu-id="d600a-417">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-417">Description</span></span>|
|-----------|--------------|-----------------|
|`AppDomainAssemblyResolveHandlerInvoked`|<span data-ttu-id="d600a-418">294</span><span class="sxs-lookup"><span data-stu-id="d600a-418">294</span></span>|<span data-ttu-id="d600a-419">已 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 调用处理程序。</span><span class="sxs-lookup"><span data-stu-id="d600a-419">An <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> handler has been invoked.</span></span>|

|<span data-ttu-id="d600a-420">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-420">Field name</span></span>|<span data-ttu-id="d600a-421">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-421">Data type</span></span>|<span data-ttu-id="d600a-422">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-422">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-423">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-423">Name of assembly name.</span></span>|
|`HandlerName`|`win:UnicodeString`|<span data-ttu-id="d600a-424">调用的处理程序的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-424">Name of the handler invoked.</span></span>|
|`ResultAssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-425">已解析的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-425">The name of assembly that was resolved.</span></span>|
|`ResultAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-426">从中解析的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-426">The path of the assembly that was resolved from.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-427">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-427">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="assemblyloadfromresolvehandlerinvoked-event"></a><span data-ttu-id="d600a-428">AssemblyLoadFromResolveHandlerInvoked 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-428">AssemblyLoadFromResolveHandlerInvoked event</span></span>

|<span data-ttu-id="d600a-429">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-429">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-430">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-430">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-431">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-431">`Binder` (0x4)</span></span>|<span data-ttu-id="d600a-432">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-432">Informational (4)</span></span>|

|<span data-ttu-id="d600a-433">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-433">Event</span></span>|<span data-ttu-id="d600a-434">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-434">Event ID</span></span>|<span data-ttu-id="d600a-435">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-435">Description</span></span>|
|-----------|--------------|-----------------|
|`AssemblyLoadFromResolveHandlerInvoked`|<span data-ttu-id="d600a-436">295</span><span class="sxs-lookup"><span data-stu-id="d600a-436">295</span></span>|<span data-ttu-id="d600a-437">已 <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> 调用处理程序。</span><span class="sxs-lookup"><span data-stu-id="d600a-437">An <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> handler has been invoked.</span></span>|

|<span data-ttu-id="d600a-438">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-438">Field name</span></span>|<span data-ttu-id="d600a-439">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-439">Data type</span></span>|<span data-ttu-id="d600a-440">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-440">Description</span></span>|
|----------------|---------------|-----------------|
|`AssemblyName`|`win:UnicodeString`|<span data-ttu-id="d600a-441">程序集名称的名称。</span><span class="sxs-lookup"><span data-stu-id="d600a-441">Name of assembly name.</span></span>|
|`IsTrackedLoad`|`win:Boolean`|<span data-ttu-id="d600a-442">是否跟踪程序集加载。</span><span class="sxs-lookup"><span data-stu-id="d600a-442">Whether the assembly load is tracked.</span></span>|
|`RequestingAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-443">请求的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-443">The path of the requesting assembly.</span></span>|
|`ComputedRequestedAssemblyPath`|`win:UnicodeString`|<span data-ttu-id="d600a-444">请求的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-444">The path of the assembly that was requested.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-445">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-445">Unique ID for the instance of CoreCLR.</span></span>|

## <a name="knownpathprobed-event"></a><span data-ttu-id="d600a-446">KnownPathProbed 事件</span><span class="sxs-lookup"><span data-stu-id="d600a-446">KnownPathProbed event</span></span>

|<span data-ttu-id="d600a-447">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="d600a-447">Keyword for raising the event</span></span>|<span data-ttu-id="d600a-448">Level</span><span class="sxs-lookup"><span data-stu-id="d600a-448">Level</span></span>|
|-----------------------------------|-----------|-----------|
|<span data-ttu-id="d600a-449">`Binder` (0x4) </span><span class="sxs-lookup"><span data-stu-id="d600a-449">`Binder` (0x4)</span></span>|<span data-ttu-id="d600a-450">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="d600a-450">Informational (4)</span></span>|

|<span data-ttu-id="d600a-451">事件</span><span class="sxs-lookup"><span data-stu-id="d600a-451">Event</span></span>|<span data-ttu-id="d600a-452">事件 ID</span><span class="sxs-lookup"><span data-stu-id="d600a-452">Event ID</span></span>|<span data-ttu-id="d600a-453">描述</span><span class="sxs-lookup"><span data-stu-id="d600a-453">Description</span></span>|
|-----------|--------------|-----------------|
|`KnownPathProbed`|<span data-ttu-id="d600a-454">296</span><span class="sxs-lookup"><span data-stu-id="d600a-454">296</span></span>|<span data-ttu-id="d600a-455">为程序集探测了已知路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-455">A known path was probed for an assembly.</span></span>|

|<span data-ttu-id="d600a-456">字段名称</span><span class="sxs-lookup"><span data-stu-id="d600a-456">Field Name</span></span>|<span data-ttu-id="d600a-457">数据类型</span><span class="sxs-lookup"><span data-stu-id="d600a-457">Data Type</span></span>|<span data-ttu-id="d600a-458">说明</span><span class="sxs-lookup"><span data-stu-id="d600a-458">Description</span></span>|
|----------------|---------------|-----------------|
|`FilePath`|`win:UnicodeString`|<span data-ttu-id="d600a-459">已探测路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-459">Path probed.</span></span>|
|`Source`|`win:UInt16`|<span data-ttu-id="d600a-460">已探测路径的源。</span><span class="sxs-lookup"><span data-stu-id="d600a-460">Source of the path probed.</span></span><br/><br/><span data-ttu-id="d600a-461">0x0：应用程序程序集。</span><span class="sxs-lookup"><span data-stu-id="d600a-461">0x0:Application Assemblies.</span></span><br/><br/><span data-ttu-id="d600a-462">0x1：应用本机映像路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-462">0x1:App native image path.</span></span><br/><br/><span data-ttu-id="d600a-463">0x2：应用路径。</span><span class="sxs-lookup"><span data-stu-id="d600a-463">0x2:App path.</span></span></br><br/><span data-ttu-id="d600a-464">0x3：平台资源根。</span><span class="sxs-lookup"><span data-stu-id="d600a-464">0x3:Platform resource roots.</span></span><br/><br/><span data-ttu-id="d600a-465">0x4：附属子目录。</span><span class="sxs-lookup"><span data-stu-id="d600a-465">0x4:Satellite Subdirectory.</span></span></br>|
|`Result`|`win:UInt32`|<span data-ttu-id="d600a-466">探测器的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d600a-466">HRESULT for the probe.</span></span>|
|`ClrInstanceID`|`win:UInt16`|<span data-ttu-id="d600a-467">CoreCLR 实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="d600a-467">Unique ID for the instance of CoreCLR.</span></span>|
