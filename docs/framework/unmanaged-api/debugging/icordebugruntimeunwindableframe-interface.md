---
title: ICorDebugRuntimeUnwindableFrame 接口
ms.date: 03/30/2017
api_name:
- ICorDebugUnwindableFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnwindableFrame
helpviewer_keywords:
- ICorDebugUnwindableFrame interface [.NET Framework debugging]
ms.assetid: cd6a3982-6ed3-4909-808d-a66055e813e0
topic_type:
- apiref
ms.openlocfilehash: 6619b8888588341f23a93b83865cd2e75cc9b3db
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712009"
---
# <a name="icordebugruntimeunwindableframe-interface"></a><span data-ttu-id="314d1-102">ICorDebugRuntimeUnwindableFrame 接口</span><span class="sxs-lookup"><span data-stu-id="314d1-102">ICorDebugRuntimeUnwindableFrame Interface</span></span>

<span data-ttu-id="314d1-103">提供对非托管方法的支持，这些方法需要公共语言运行时 (CLR) 来展开帧。</span><span class="sxs-lookup"><span data-stu-id="314d1-103">Provides support for unmanaged methods that require the common language runtime (CLR) to unwind a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="314d1-104">注解</span><span class="sxs-lookup"><span data-stu-id="314d1-104">Remarks</span></span>  

 <span data-ttu-id="314d1-105">`ICorDebugRuntimeUnwindableFrame` 是 ICorDebugFrame 接口的专用版本。</span><span class="sxs-lookup"><span data-stu-id="314d1-105">`ICorDebugRuntimeUnwindableFrame` is a specialized version of the ICorDebugFrame interface.</span></span> <span data-ttu-id="314d1-106">它由需要运行时展开当前堆栈上的帧的非托管方法使用。</span><span class="sxs-lookup"><span data-stu-id="314d1-106">It is used by unmanaged methods that require the runtime to unwind a frame on the current stack.</span></span> <span data-ttu-id="314d1-107">现有的展开约定不起作用，因为它们不使用 JIT 编译代码。</span><span class="sxs-lookup"><span data-stu-id="314d1-107">Existing unwinding conventions do not work, because they do not use JIT-compiled code.</span></span> <span data-ttu-id="314d1-108">当调试器发现不可展开帧时，它应使用 [ICorDebugStackWalk：： Next](icordebugstackwalk-next-method.md) 方法展开它，但它应执行检查。</span><span class="sxs-lookup"><span data-stu-id="314d1-108">When the debugger sees an unwindable frame, it should use the [ICorDebugStackWalk::Next](icordebugstackwalk-next-method.md) method to unwind it, but it should perform inspection itself.</span></span> <span data-ttu-id="314d1-109">当调试器收到时 `ICorDebugRuntimeUnwindableFrame` ，它可以调用 [ICorDebugStackWalk：： GetContext](icordebugstackwalk-getcontext-method.md) 方法来检索该帧的上下文。</span><span class="sxs-lookup"><span data-stu-id="314d1-109">When the debugger receives an `ICorDebugRuntimeUnwindableFrame`, it can call the [ICorDebugStackWalk::GetContext](icordebugstackwalk-getcontext-method.md) method to retrieve the context of the frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="314d1-110">要求</span><span class="sxs-lookup"><span data-stu-id="314d1-110">Requirements</span></span>  

 <span data-ttu-id="314d1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="314d1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="314d1-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="314d1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="314d1-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="314d1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="314d1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="314d1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="314d1-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="314d1-115">See also</span></span>

- [<span data-ttu-id="314d1-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="314d1-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="314d1-117">调试</span><span class="sxs-lookup"><span data-stu-id="314d1-117">Debugging</span></span>](index.md)
