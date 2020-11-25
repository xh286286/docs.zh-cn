---
title: ICorDebugThread3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThread3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread3
helpviewer_keywords:
- ICorDebugThread3 interface [.NET Framework debugging]
ms.assetid: eb2860ef-06cb-4968-a6c3-6d048ecda2a4
topic_type:
- apiref
ms.openlocfilehash: 015d0061e5be5bbc212243ca06f1d165abe4496a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729299"
---
# <a name="icordebugthread3-interface"></a><span data-ttu-id="16123-102">ICorDebugThread3 接口</span><span class="sxs-lookup"><span data-stu-id="16123-102">ICorDebugThread3 Interface</span></span>

<span data-ttu-id="16123-103">提供 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 和相应接口的入口点。</span><span class="sxs-lookup"><span data-stu-id="16123-103">Provides the entry point to the [ICorDebugStackWalk](icordebugstackwalk-interface.md) and corresponding interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="16123-104">方法</span><span class="sxs-lookup"><span data-stu-id="16123-104">Methods</span></span>  
  
|<span data-ttu-id="16123-105">方法</span><span class="sxs-lookup"><span data-stu-id="16123-105">Method</span></span>|<span data-ttu-id="16123-106">说明</span><span class="sxs-lookup"><span data-stu-id="16123-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="16123-107">CreateStackWalk 方法</span><span class="sxs-lookup"><span data-stu-id="16123-107">CreateStackWalk Method</span></span>](icordebugthread3-createstackwalk-method.md)|<span data-ttu-id="16123-108">为要展开其堆栈的线程创建 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="16123-108">Creates an [ICorDebugStackWalk](icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>|  
|[<span data-ttu-id="16123-109">GetActiveInternalFrames 方法</span><span class="sxs-lookup"><span data-stu-id="16123-109">GetActiveInternalFrames Method</span></span>](icordebugthread3-getactiveinternalframes-method.md)|<span data-ttu-id="16123-110">返回堆栈 ([ICorDebugInternalFrame2](icordebuginternalframe2-interface.md) 对象) 内部帧的数组。</span><span class="sxs-lookup"><span data-stu-id="16123-110">Returns an array of internal frames ([ICorDebugInternalFrame2](icordebuginternalframe2-interface.md) objects) on the stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="16123-111">注解</span><span class="sxs-lookup"><span data-stu-id="16123-111">Remarks</span></span>  

 <span data-ttu-id="16123-112">`ICorDebugThread3` 是 ICorDebugThread 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="16123-112">`ICorDebugThread3` is a logical extension to the ICorDebugThread interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="16123-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="16123-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16123-114">要求</span><span class="sxs-lookup"><span data-stu-id="16123-114">Requirements</span></span>  

 <span data-ttu-id="16123-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="16123-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16123-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="16123-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="16123-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="16123-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="16123-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16123-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16123-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16123-119">See also</span></span>

- [<span data-ttu-id="16123-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="16123-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="16123-121">调试</span><span class="sxs-lookup"><span data-stu-id="16123-121">Debugging</span></span>](index.md)
