---
title: 异常 Thrown_V1 ETW 事件
description: 查看有关 ExceptionThrown_V1 ETW 事件的详细信息。 将为引发的异常提供事件数据（如字段名称、数据类型和说明）。
ms.date: 03/30/2017
helpviewer_keywords:
- ExceptionThrown_V1 event [.NET Framework]
- ETW, ExceptionThrown_V1 event (CLR)
ms.assetid: 0d3da389-6b7b-40f6-a877-fac546d6019c
ms.openlocfilehash: c1ba994b291bd278a95e34beb0b02ed6581786e8
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96263472"
---
# <a name="exception-thrown_v1-etw-event"></a><span data-ttu-id="ae7f3-104">异常 Thrown_V1 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="ae7f3-104">Exception Thrown_V1 ETW Event</span></span>

<span data-ttu-id="ae7f3-105">该事件捕获有关引发的异常的信息。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-105">This event captures information about the exceptions that are thrown.</span></span>  
  
 <span data-ttu-id="ae7f3-106">下表显示了引发事件的关键字以及事件的级别。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-106">The following table shows the keyword under which the event is raised, and the level of the event.</span></span> <span data-ttu-id="ae7f3-107">（有关详细信息，请参阅 [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md)。）</span><span class="sxs-lookup"><span data-stu-id="ae7f3-107">(For more information, see [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="ae7f3-108">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="ae7f3-108">Keyword for raising the event</span></span>|<span data-ttu-id="ae7f3-109">Level</span><span class="sxs-lookup"><span data-stu-id="ae7f3-109">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="ae7f3-110">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ae7f3-110">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="ae7f3-111">警告 (2)</span><span class="sxs-lookup"><span data-stu-id="ae7f3-111">Warning (2)</span></span>|  
  
 <span data-ttu-id="ae7f3-112">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-112">The following table shows event information.</span></span>  
  
|<span data-ttu-id="ae7f3-113">事件</span><span class="sxs-lookup"><span data-stu-id="ae7f3-113">Event</span></span>|<span data-ttu-id="ae7f3-114">事件 ID</span><span class="sxs-lookup"><span data-stu-id="ae7f3-114">Event ID</span></span>|<span data-ttu-id="ae7f3-115">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="ae7f3-115">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ExceptionThrown_V1`|<span data-ttu-id="ae7f3-116">80</span><span class="sxs-lookup"><span data-stu-id="ae7f3-116">80</span></span>|<span data-ttu-id="ae7f3-117">引发托管异常。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-117">A managed exception is thrown.</span></span>|  
  
 <span data-ttu-id="ae7f3-118">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-118">The following table shows event data.</span></span>  
  
|<span data-ttu-id="ae7f3-119">字段名称</span><span class="sxs-lookup"><span data-stu-id="ae7f3-119">Field name</span></span>|<span data-ttu-id="ae7f3-120">数据类型</span><span class="sxs-lookup"><span data-stu-id="ae7f3-120">Data type</span></span>|<span data-ttu-id="ae7f3-121">说明</span><span class="sxs-lookup"><span data-stu-id="ae7f3-121">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="ae7f3-122">异常类型</span><span class="sxs-lookup"><span data-stu-id="ae7f3-122">Exception Type</span></span>|<span data-ttu-id="ae7f3-123">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="ae7f3-123">win:UnicodeString</span></span>|<span data-ttu-id="ae7f3-124">异常的类型，例如，`System.NullReferenceException`。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-124">Type of the exception; for example, `System.NullReferenceException`.</span></span>|  
|<span data-ttu-id="ae7f3-125">异常消息</span><span class="sxs-lookup"><span data-stu-id="ae7f3-125">Exception Message</span></span>|<span data-ttu-id="ae7f3-126">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="ae7f3-126">win:UnicodeString</span></span>|<span data-ttu-id="ae7f3-127">实际的异常消息。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-127">Actual exception message.</span></span>|  
|<span data-ttu-id="ae7f3-128">EIPCodeThrow</span><span class="sxs-lookup"><span data-stu-id="ae7f3-128">EIPCodeThrow</span></span>|<span data-ttu-id="ae7f3-129">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="ae7f3-129">win:Pointer</span></span>|<span data-ttu-id="ae7f3-130">指向异常发生位置的指令指针。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-130">Instruction pointer where exception occurred.</span></span>|  
|<span data-ttu-id="ae7f3-131">ExceptionHR</span><span class="sxs-lookup"><span data-stu-id="ae7f3-131">ExceptionHR</span></span>|<span data-ttu-id="ae7f3-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="ae7f3-132">win:UInt32</span></span>|<span data-ttu-id="ae7f3-133">异常 [HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-133">Exception [HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a).</span></span>|  
|<span data-ttu-id="ae7f3-134">ExceptionFlags</span><span class="sxs-lookup"><span data-stu-id="ae7f3-134">ExceptionFlags</span></span>|<span data-ttu-id="ae7f3-135">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="ae7f3-135">win:UInt16</span></span>|<span data-ttu-id="ae7f3-136">0x01: HasInnerException（参阅 Visual Basic 文档中的 [CLR ETW 事件](clr-etw-events.md)）。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-136">0x01: HasInnerException (see [CLR ETW Events](clr-etw-events.md) in the Visual Basic documentation).</span></span><br /><br /> <span data-ttu-id="ae7f3-137">0x02: IsNestedException。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-137">0x02: IsNestedException.</span></span><br /><br /> <span data-ttu-id="ae7f3-138">0x04: IsRethrownException。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-138">0x04: IsRethrownException.</span></span><br /><br /> <span data-ttu-id="ae7f3-139">0x08： IsCorruptedStateException (指示进程状态已损坏;请参阅 [处理损坏状态异常](/archive/msdn-magazine/2009/february/clr-inside-out-handling-corrupted-state-exceptions)) 。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-139">0x08: IsCorruptedStateException (indicates that the process state is corrupt; see [Handling Corrupted State Exceptions](/archive/msdn-magazine/2009/february/clr-inside-out-handling-corrupted-state-exceptions)).</span></span><br /><br /> <span data-ttu-id="ae7f3-140">0x10: IsCLSCompliant（从 <xref:System.Exception> 派生的异常符合 CLS，此外的其他异常均不符合 CLS）。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-140">0x10: IsCLSCompliant (an exception that derives from <xref:System.Exception> is CLS-compliant; otherwise, it is not CLS-compliant).</span></span>|  
|<span data-ttu-id="ae7f3-141">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="ae7f3-141">ClrInstanceID</span></span>|<span data-ttu-id="ae7f3-142">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="ae7f3-142">win:UInt16</span></span>|<span data-ttu-id="ae7f3-143">CLR 或 CoreCLR 的实例的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ae7f3-143">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ae7f3-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae7f3-144">See also</span></span>

- [<span data-ttu-id="ae7f3-145">CLR ETW 事件</span><span class="sxs-lookup"><span data-stu-id="ae7f3-145">CLR ETW Events</span></span>](clr-etw-events.md)
