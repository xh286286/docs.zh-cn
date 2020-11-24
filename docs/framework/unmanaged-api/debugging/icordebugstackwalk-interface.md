---
title: ICorDebugStackWalk 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk
helpviewer_keywords:
- ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 16d695e8-975d-431b-8421-e9e6c3e3f476
topic_type:
- apiref
ms.openlocfilehash: b37a89c0a86df49c894dc43676f8feafb80f5c95
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687510"
---
# <a name="icordebugstackwalk-interface"></a><span data-ttu-id="bb3a4-102">ICorDebugStackWalk 接口</span><span class="sxs-lookup"><span data-stu-id="bb3a4-102">ICorDebugStackWalk Interface</span></span>

<span data-ttu-id="bb3a4-103">提供用于获取线程堆栈上的托管方法或帧的方法。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-103">Provides methods for getting the managed methods, or frames, on a thread’s stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bb3a4-104">方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-104">Methods</span></span>  
  
|<span data-ttu-id="bb3a4-105">方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-105">Method</span></span>|<span data-ttu-id="bb3a4-106">说明</span><span class="sxs-lookup"><span data-stu-id="bb3a4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bb3a4-107">GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-107">GetContext Method</span></span>](icordebugstackwalk-getcontext-method.md)|<span data-ttu-id="bb3a4-108">返回对象中当前帧的上下文 `ICorDebugStackWalk` 。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-108">Returns the context for the current frame in the `ICorDebugStackWalk` object.</span></span>|  
|[<span data-ttu-id="bb3a4-109">SetContext 方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-109">SetContext Method</span></span>](icordebugstackwalk-setcontext-method.md)|<span data-ttu-id="bb3a4-110">将 `ICorDebugStackWalk` 对象的当前上下文设置为线程的有效上下文。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-110">Sets the `ICorDebugStackWalk` object’s current context to a valid context for the thread.</span></span>|  
|[<span data-ttu-id="bb3a4-111">Next 方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-111">Next Method</span></span>](icordebugstackwalk-next-method.md)|<span data-ttu-id="bb3a4-112">将 `ICorDebugStackWalk` 对象移动到下一帧。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-112">Moves the `ICorDebugStackWalk` object to the next frame.</span></span>|  
|[<span data-ttu-id="bb3a4-113">GetFrame 方法</span><span class="sxs-lookup"><span data-stu-id="bb3a4-113">GetFrame Method</span></span>](icordebugstackwalk-getframe-method.md)|<span data-ttu-id="bb3a4-114">获取对象中的当前帧 `ICorDebugStackWalk` 。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-114">Gets the current frame in the `ICorDebugStackWalk` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bb3a4-115">注解</span><span class="sxs-lookup"><span data-stu-id="bb3a4-115">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bb3a4-116">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb3a4-117">要求</span><span class="sxs-lookup"><span data-stu-id="bb3a4-117">Requirements</span></span>  

 <span data-ttu-id="bb3a4-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb3a4-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb3a4-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bb3a4-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bb3a4-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb3a4-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb3a4-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb3a4-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb3a4-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb3a4-122">See also</span></span>

- [<span data-ttu-id="bb3a4-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="bb3a4-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="bb3a4-124">调试</span><span class="sxs-lookup"><span data-stu-id="bb3a4-124">Debugging</span></span>](index.md)
