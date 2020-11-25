---
title: ICorDebugHeapValue3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3
helpviewer_keywords:
- ICorDebugHeapValue3 interface [.NET Framework debugging]
ms.assetid: 9c421bb0-e647-4b2d-a986-f3d578cc7f20
topic_type:
- apiref
ms.openlocfilehash: a1f4964c89aa3b658c57946d4b5a0327797118f1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728701"
---
# <a name="icordebugheapvalue3-interface"></a><span data-ttu-id="c4f7a-102">ICorDebugHeapValue3 接口</span><span class="sxs-lookup"><span data-stu-id="c4f7a-102">ICorDebugHeapValue3 Interface</span></span>

<span data-ttu-id="c4f7a-103">公开对象的监视器锁属性。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-103">Exposes the monitor lock properties of objects.</span></span> <span data-ttu-id="c4f7a-104">此接口扩展 ICorDebugHeapValue 和 ICorDebugHeapValue2 接口。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-104">This interface extends the ICorDebugHeapValue and ICorDebugHeapValue2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c4f7a-105">方法</span><span class="sxs-lookup"><span data-stu-id="c4f7a-105">Methods</span></span>  
  
|<span data-ttu-id="c4f7a-106">方法</span><span class="sxs-lookup"><span data-stu-id="c4f7a-106">Method</span></span>|<span data-ttu-id="c4f7a-107">说明</span><span class="sxs-lookup"><span data-stu-id="c4f7a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c4f7a-108">GetThreadOwningMonitorLock 方法</span><span class="sxs-lookup"><span data-stu-id="c4f7a-108">GetThreadOwningMonitorLock Method</span></span>](icordebugheapvalue3-getthreadowningmonitorlock-method.md)|<span data-ttu-id="c4f7a-109">返回拥有此对象的监视器锁的托管线程。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-109">Returns the managed thread that owns the monitor lock on this object.</span></span>|  
|[<span data-ttu-id="c4f7a-110">GetMonitorEventWaitList 方法</span><span class="sxs-lookup"><span data-stu-id="c4f7a-110">GetMonitorEventWaitList Method</span></span>](icordebugheapvalue3-getmonitoreventwaitlist-method.md)|<span data-ttu-id="c4f7a-111">提供在与监视器锁关联的事件上排队的线程的排序列表。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-111">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4f7a-112">注解</span><span class="sxs-lookup"><span data-stu-id="c4f7a-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c4f7a-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4f7a-114">要求</span><span class="sxs-lookup"><span data-stu-id="c4f7a-114">Requirements</span></span>  

 <span data-ttu-id="c4f7a-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4f7a-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c4f7a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c4f7a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c4f7a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c4f7a-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4f7a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4f7a-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4f7a-119">See also</span></span>

- [<span data-ttu-id="c4f7a-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="c4f7a-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="c4f7a-121">调试</span><span class="sxs-lookup"><span data-stu-id="c4f7a-121">Debugging</span></span>](index.md)
