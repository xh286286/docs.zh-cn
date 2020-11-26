---
title: 堆栈 ETW 事件
description: 阅读有关 stack ETW 事件的信息，该事件应与其他事件结合使用，以在引发事件后生成堆栈跟踪。
ms.date: 03/30/2017
helpviewer_keywords:
- stack event [.NET Framework]
- ETW, stack event (CLR)
ms.assetid: f612fa5b-4b62-4593-a19e-85c9b1018dce
ms.openlocfilehash: 3b890e587abd5cb1b7315fe41897f24638fd4604
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96236203"
---
# <a name="stack-etw-event"></a><span data-ttu-id="470c9-103">堆栈 ETW 事件</span><span class="sxs-lookup"><span data-stu-id="470c9-103">Stack ETW Event</span></span>

<span data-ttu-id="470c9-104">堆栈事件应与其他事件结合使用，在引发事件后生成堆栈跟踪。</span><span class="sxs-lookup"><span data-stu-id="470c9-104">The stack event should be used in conjunction with other events to generate stack traces after an event is raised.</span></span> <span data-ttu-id="470c9-105">启用运行时提供程序时，记录该事件。</span><span class="sxs-lookup"><span data-stu-id="470c9-105">It is logged when the runtime provider is enabled.</span></span> <span data-ttu-id="470c9-106">这是一个发生频率非常高的事件，因为每当引发另一个运行时事件时，都将引发此事件。</span><span class="sxs-lookup"><span data-stu-id="470c9-106">This is a very high frequency event, because it is raised whenever another runtime event is raised.</span></span> <span data-ttu-id="470c9-107">因此，我们建议谨慎使用此事件。</span><span class="sxs-lookup"><span data-stu-id="470c9-107">For this reason, we recommend that you use this event with caution.</span></span>  
  
 <span data-ttu-id="470c9-108">下表显示了关键字和级别。</span><span class="sxs-lookup"><span data-stu-id="470c9-108">The following table shows the keyword and level.</span></span> <span data-ttu-id="470c9-109">（有关详细信息，请参阅 [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md)。）</span><span class="sxs-lookup"><span data-stu-id="470c9-109">(For more information, see [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="470c9-110">引发事件的关键字</span><span class="sxs-lookup"><span data-stu-id="470c9-110">Keyword for raising the event</span></span>|<span data-ttu-id="470c9-111">Level</span><span class="sxs-lookup"><span data-stu-id="470c9-111">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="470c9-112">`StackKeyword` (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="470c9-112">`StackKeyword` (0x40000000)</span></span>|<span data-ttu-id="470c9-113">LogAlways(0)</span><span class="sxs-lookup"><span data-stu-id="470c9-113">LogAlways(0)</span></span>|  
  
 <span data-ttu-id="470c9-114">下表显示了事件信息。</span><span class="sxs-lookup"><span data-stu-id="470c9-114">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="470c9-115">事件</span><span class="sxs-lookup"><span data-stu-id="470c9-115">Event</span></span>|<span data-ttu-id="470c9-116">事件 ID</span><span class="sxs-lookup"><span data-stu-id="470c9-116">Event ID</span></span>|<span data-ttu-id="470c9-117">在发生以下情况时引发</span><span class="sxs-lookup"><span data-stu-id="470c9-117">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`CLRStackWalk`|<span data-ttu-id="470c9-118">82</span><span class="sxs-lookup"><span data-stu-id="470c9-118">82</span></span>|<span data-ttu-id="470c9-119">与其他事件结合使用，在事件发生后生成堆栈跟踪。</span><span class="sxs-lookup"><span data-stu-id="470c9-119">In conjunction with other events to generate stack traces following an event.</span></span>|  
  
 <span data-ttu-id="470c9-120">下表显示了事件数据。</span><span class="sxs-lookup"><span data-stu-id="470c9-120">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="470c9-121">字段名称</span><span class="sxs-lookup"><span data-stu-id="470c9-121">Field name</span></span>|<span data-ttu-id="470c9-122">数据类型</span><span class="sxs-lookup"><span data-stu-id="470c9-122">Data Type</span></span>|<span data-ttu-id="470c9-123">说明</span><span class="sxs-lookup"><span data-stu-id="470c9-123">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="470c9-124">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="470c9-124">ClrInstanceID</span></span>|<span data-ttu-id="470c9-125">win:Uint16</span><span class="sxs-lookup"><span data-stu-id="470c9-125">win:Uint16</span></span>|<span data-ttu-id="470c9-126">唯一运行时标识符。</span><span class="sxs-lookup"><span data-stu-id="470c9-126">Unique runtime identifier.</span></span>|  
|<span data-ttu-id="470c9-127">Reserved1</span><span class="sxs-lookup"><span data-stu-id="470c9-127">Reserved1</span></span>|<span data-ttu-id="470c9-128">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="470c9-128">win:UInt8</span></span>|<span data-ttu-id="470c9-129">保留。</span><span class="sxs-lookup"><span data-stu-id="470c9-129">Reserved.</span></span>|  
|<span data-ttu-id="470c9-130">Reserved2</span><span class="sxs-lookup"><span data-stu-id="470c9-130">Reserved2</span></span>|<span data-ttu-id="470c9-131">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="470c9-131">win:UInt8</span></span>|<span data-ttu-id="470c9-132">保留。</span><span class="sxs-lookup"><span data-stu-id="470c9-132">Reserved.</span></span>|  
|<span data-ttu-id="470c9-133">FrameCount</span><span class="sxs-lookup"><span data-stu-id="470c9-133">FrameCount</span></span>|<span data-ttu-id="470c9-134">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="470c9-134">win:UInt32</span></span>|<span data-ttu-id="470c9-135">堆栈跟踪中的帧数。</span><span class="sxs-lookup"><span data-stu-id="470c9-135">The number of frames in the stack trace.</span></span>|  
|<span data-ttu-id="470c9-136">堆栈</span><span class="sxs-lookup"><span data-stu-id="470c9-136">Stack</span></span>|<span data-ttu-id="470c9-137">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="470c9-137">win:Pointer</span></span>|<span data-ttu-id="470c9-138">指令指针的列</span><span class="sxs-lookup"><span data-stu-id="470c9-138">Columns of instruction pointers.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="470c9-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="470c9-139">See also</span></span>

- [<span data-ttu-id="470c9-140">CLR ETW 事件</span><span class="sxs-lookup"><span data-stu-id="470c9-140">CLR ETW Events</span></span>](clr-etw-events.md)
