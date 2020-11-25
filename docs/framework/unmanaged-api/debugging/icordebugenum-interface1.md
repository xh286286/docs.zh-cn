---
title: ICorDebugEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum
helpviewer_keywords:
- ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 80be7efe-2c32-4b9f-8c52-40c6f6268219
topic_type:
- apiref
ms.openlocfilehash: b208444de3b427329988f27b9d252b54143b7240
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698788"
---
# <a name="icordebugenum-interface"></a><span data-ttu-id="b2bcc-102">ICorDebugEnum 接口</span><span class="sxs-lookup"><span data-stu-id="b2bcc-102">ICorDebugEnum Interface</span></span>

<span data-ttu-id="b2bcc-103">用作调试应用程序所使用的枚举器的抽象基接口。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-103">Serves as the abstract base interface for the enumerators that are used by a debugging application.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b2bcc-104">方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-104">Methods</span></span>  
  
|<span data-ttu-id="b2bcc-105">方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-105">Method</span></span>|<span data-ttu-id="b2bcc-106">说明</span><span class="sxs-lookup"><span data-stu-id="b2bcc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b2bcc-107">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-107">Clone Method</span></span>](icordebugenum-clone-method.md)|<span data-ttu-id="b2bcc-108">创建此 `ICorDebugEnum` 对象的一个副本。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-108">Creates a copy of this `ICorDebugEnum` object.</span></span>|  
|[<span data-ttu-id="b2bcc-109">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-109">GetCount Method</span></span>](icordebugenum-getcount-method.md)|<span data-ttu-id="b2bcc-110">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-110">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="b2bcc-111">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-111">Reset Method</span></span>](icordebugenum-reset-method.md)|<span data-ttu-id="b2bcc-112">将光标移到枚举的开头。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-112">Moves the cursor to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="b2bcc-113">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="b2bcc-113">Skip Method</span></span>](icordebugenum-skip-method.md)|<span data-ttu-id="b2bcc-114">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-114">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b2bcc-115">注解</span><span class="sxs-lookup"><span data-stu-id="b2bcc-115">Remarks</span></span>  

 <span data-ttu-id="b2bcc-116">以下枚举器派生自 `ICorDebugEnum` ：</span><span class="sxs-lookup"><span data-stu-id="b2bcc-116">The following enumerators derive from `ICorDebugEnum`:</span></span>  
  
- <span data-ttu-id="b2bcc-117">ICorDebugAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-117">"ICorDebugAppDomainEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-118">ICorDebugAssemblyEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-118">"ICorDebugAssemblyEnum"</span></span>  
  
- [<span data-ttu-id="b2bcc-119">ICorDebugBlockingObjectEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-119">ICorDebugBlockingObjectEnum</span></span>](icordebugblockingobjectenum-interface.md)  
  
- <span data-ttu-id="b2bcc-120">ICorDebugBreakpointEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-120">"ICorDebugBreakpointEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-121">ICorDebugChainEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-121">"ICorDebugChainEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-122">ICorDebugCodeEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-122">"ICorDebugCodeEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-123">ICorDebugErrorInfoEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-123">"ICorDebugErrorInfoEnum"</span></span>  
  
- [<span data-ttu-id="b2bcc-124">ICorDebugExceptionObjectCallStackEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-124">ICorDebugExceptionObjectCallStackEnum</span></span>](icordebugexceptionobjectcallstackenum-interface.md)  
  
- <span data-ttu-id="b2bcc-125">ICorDebugFrameEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-125">"ICorDebugFrameEnum"</span></span>  
  
- [<span data-ttu-id="b2bcc-126">ICorDebugGCReferenceEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-126">ICorDebugGCReferenceEnum</span></span>](icordebuggcreferenceenum-interface.md)  
  
- [<span data-ttu-id="b2bcc-127">ICorDebugGuidToTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-127">ICorDebugGuidToTypeEnum</span></span>](icordebugguidtotypeenum-interface.md)  
  
- [<span data-ttu-id="b2bcc-128">ICorDebugHeapEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-128">ICorDebugHeapEnum</span></span>](icordebugheapenum-interface.md)  
  
- [<span data-ttu-id="b2bcc-129">ICorDebugHeapSegmentEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-129">ICorDebugHeapSegmentEnum</span></span>](icordebugheapsegmentenum-interface.md)  
  
- <span data-ttu-id="b2bcc-130">ICorDebugModuleEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-130">"ICorDebugModuleEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-131">ICorDebugObjectEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-131">"ICorDebugObjectEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-132">ICorDebugProcessEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-132">"ICorDebugProcessEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-133">ICorDebugStepperEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-133">"ICorDebugStepperEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-134">ICorDebugThreadEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-134">"ICorDebugThreadEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-135">ICorDebugTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-135">"ICorDebugTypeEnum"</span></span>  
  
- <span data-ttu-id="b2bcc-136">ICorDebugValueEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-136">"ICorDebugValueEnum"</span></span>  
  
- [<span data-ttu-id="b2bcc-137">ICorDebugVariableHomeEnum</span><span class="sxs-lookup"><span data-stu-id="b2bcc-137">ICorDebugVariableHomeEnum</span></span>](icordebugvariablehomeenum-interface.md)  
  
> [!NOTE]
> <span data-ttu-id="b2bcc-138">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-138">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b2bcc-139">要求</span><span class="sxs-lookup"><span data-stu-id="b2bcc-139">Requirements</span></span>  

 <span data-ttu-id="b2bcc-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b2bcc-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b2bcc-141">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b2bcc-141">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b2bcc-142">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b2bcc-142">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b2bcc-143">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2bcc-143">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2bcc-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2bcc-144">See also</span></span>

- [<span data-ttu-id="b2bcc-145">调试接口</span><span class="sxs-lookup"><span data-stu-id="b2bcc-145">Debugging Interfaces</span></span>](debugging-interfaces.md)
