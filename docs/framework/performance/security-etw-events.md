---
title: 安全 ETW 事件
description: 了解在 .NET 中强名称验证和验证码验证期间引发的安全 ETW 事件。
ms.date: 03/30/2017
helpviewer_keywords:
- security events [.NET Framework]
- ETW, security events (CLR)
ms.assetid: 0ed69f73-5c01-4514-bd63-979c6e38d41d
ms.openlocfilehash: 4402bf5690a53ce518077268a3e20a95aeb14e8a
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96272509"
---
# <a name="security-etw-events"></a><span data-ttu-id="06a08-103">安全 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="06a08-103">Security ETW Events</span></span>

<span data-ttu-id="06a08-104">在强名称验证和验证码验证期间会引发安全事件。</span><span class="sxs-lookup"><span data-stu-id="06a08-104">Security events are raised during strong name verification and Authenticode verification.</span></span>  

## <a name="strongnameverificationstart_v1-and-strongnameverificationstop_v1-events"></a><span data-ttu-id="06a08-105">StrongNameVerificationStart_V1 和 StrongNameVerificationStop_V1 事件</span><span class="sxs-lookup"><span data-stu-id="06a08-105">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>  

 <span data-ttu-id="06a08-106">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="06a08-106">The following table shows the keyword and level.</span></span> <span data-ttu-id="06a08-107">（有关详细信息，请参阅 [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md)。）</span><span class="sxs-lookup"><span data-stu-id="06a08-107">(For more information, see [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="06a08-108">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="06a08-108">Keyword for raising the event</span></span>|<span data-ttu-id="06a08-109">Level</span><span class="sxs-lookup"><span data-stu-id="06a08-109">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="06a08-110">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="06a08-110">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="06a08-111">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="06a08-111">Informational(4)</span></span>|  
  
 <span data-ttu-id="06a08-112">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="06a08-112">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="06a08-113">事件</span><span class="sxs-lookup"><span data-stu-id="06a08-113">Event</span></span>|<span data-ttu-id="06a08-114">事件 ID</span><span class="sxs-lookup"><span data-stu-id="06a08-114">Event ID</span></span>|<span data-ttu-id="06a08-115">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="06a08-115">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`StrongNameVerificationStart_V1`|<span data-ttu-id="06a08-116">181</span><span class="sxs-lookup"><span data-stu-id="06a08-116">181</span></span>|<span data-ttu-id="06a08-117">强名称验证开始。</span><span class="sxs-lookup"><span data-stu-id="06a08-117">Start of strong name verification.</span></span>|  
|`StrongNameVerificationStop_V1`|<span data-ttu-id="06a08-118">182</span><span class="sxs-lookup"><span data-stu-id="06a08-118">182</span></span>|<span data-ttu-id="06a08-119">强名称验证结束。</span><span class="sxs-lookup"><span data-stu-id="06a08-119">End of strong name verification.</span></span>|  
  
 <span data-ttu-id="06a08-120">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="06a08-120">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="06a08-121">字段名称</span><span class="sxs-lookup"><span data-stu-id="06a08-121">Field name</span></span>|<span data-ttu-id="06a08-122">数据类型</span><span class="sxs-lookup"><span data-stu-id="06a08-122">Data type</span></span>|<span data-ttu-id="06a08-123">说明</span><span class="sxs-lookup"><span data-stu-id="06a08-123">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="06a08-124">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="06a08-124">VerificationFlags</span></span>|<span data-ttu-id="06a08-125">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="06a08-125">win:UInt32</span></span>|<span data-ttu-id="06a08-126">验证标志。</span><span class="sxs-lookup"><span data-stu-id="06a08-126">The verification flags.</span></span>|  
|<span data-ttu-id="06a08-127">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="06a08-127">ErrorCode</span></span>|<span data-ttu-id="06a08-128">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="06a08-128">win:UInt32</span></span>|<span data-ttu-id="06a08-129">HResult 错误代码。</span><span class="sxs-lookup"><span data-stu-id="06a08-129">The HResult error code.</span></span>|  
|<span data-ttu-id="06a08-130">FullyQualifiedAssemblyName</span><span class="sxs-lookup"><span data-stu-id="06a08-130">FullyQualifiedAssemblyName</span></span>|<span data-ttu-id="06a08-131">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="06a08-131">win:UnicodeString</span></span>|<span data-ttu-id="06a08-132">完全限定程序集名称。</span><span class="sxs-lookup"><span data-stu-id="06a08-132">The fully qualified assembly name.</span></span>|  
|<span data-ttu-id="06a08-133">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="06a08-133">ClrInstanceID</span></span>|<span data-ttu-id="06a08-134">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="06a08-134">win:UInt16</span></span>|<span data-ttu-id="06a08-135">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="06a08-135">Unique ID for the instance of CLR or CoreCLR.</span></span>|  

## <a name="authenticodeverificationstart_v1-and-authenticodeverificationstop_v1-events"></a><span data-ttu-id="06a08-136">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 事件</span><span class="sxs-lookup"><span data-stu-id="06a08-136">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>  

 <span data-ttu-id="06a08-137">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="06a08-137">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="06a08-138">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="06a08-138">Keyword for raising the event</span></span>|<span data-ttu-id="06a08-139">Level</span><span class="sxs-lookup"><span data-stu-id="06a08-139">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="06a08-140">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="06a08-140">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="06a08-141">信息性 (4)</span><span class="sxs-lookup"><span data-stu-id="06a08-141">Informational(4)</span></span>|  
  
 <span data-ttu-id="06a08-142">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="06a08-142">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="06a08-143">事件</span><span class="sxs-lookup"><span data-stu-id="06a08-143">Event</span></span>|<span data-ttu-id="06a08-144">事件 ID</span><span class="sxs-lookup"><span data-stu-id="06a08-144">Event ID</span></span>|<span data-ttu-id="06a08-145">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="06a08-145">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AuthenticodeVerificationStart_V1`|<span data-ttu-id="06a08-146">183</span><span class="sxs-lookup"><span data-stu-id="06a08-146">183</span></span>|<span data-ttu-id="06a08-147">验证码验证开始。</span><span class="sxs-lookup"><span data-stu-id="06a08-147">Start of Authenticode verification.</span></span>|  
|`AuthenticodeVerificationStop_V1`|<span data-ttu-id="06a08-148">184</span><span class="sxs-lookup"><span data-stu-id="06a08-148">184</span></span>|<span data-ttu-id="06a08-149">验证码验证结束。</span><span class="sxs-lookup"><span data-stu-id="06a08-149">End of Authenticode verification.</span></span>|  
  
 <span data-ttu-id="06a08-150">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="06a08-150">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="06a08-151">字段名称</span><span class="sxs-lookup"><span data-stu-id="06a08-151">Field name</span></span>|<span data-ttu-id="06a08-152">数据类型</span><span class="sxs-lookup"><span data-stu-id="06a08-152">Data type</span></span>|<span data-ttu-id="06a08-153">说明</span><span class="sxs-lookup"><span data-stu-id="06a08-153">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="06a08-154">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="06a08-154">VerificationFlags</span></span>|<span data-ttu-id="06a08-155">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="06a08-155">win:UInt32</span></span>|<span data-ttu-id="06a08-156">验证标志。</span><span class="sxs-lookup"><span data-stu-id="06a08-156">The verification flags.</span></span>|  
|<span data-ttu-id="06a08-157">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="06a08-157">ErrorCode</span></span>|<span data-ttu-id="06a08-158">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="06a08-158">win:UInt32</span></span>|<span data-ttu-id="06a08-159">HResult 错误代码。</span><span class="sxs-lookup"><span data-stu-id="06a08-159">The HResult error code.</span></span>|  
|<span data-ttu-id="06a08-160">ModulePath</span><span class="sxs-lookup"><span data-stu-id="06a08-160">ModulePath</span></span>|<span data-ttu-id="06a08-161">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="06a08-161">win:UnicodeString</span></span>|<span data-ttu-id="06a08-162">模块路径。</span><span class="sxs-lookup"><span data-stu-id="06a08-162">The module path.</span></span>|  
|<span data-ttu-id="06a08-163">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="06a08-163">ClrInstanceID</span></span>|<span data-ttu-id="06a08-164">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="06a08-164">win:UInt16</span></span>|<span data-ttu-id="06a08-165">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="06a08-165">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="06a08-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06a08-166">See also</span></span>

- [<span data-ttu-id="06a08-167">CLR ETW 事件</span><span class="sxs-lookup"><span data-stu-id="06a08-167">CLR ETW Events</span></span>](clr-etw-events.md)
