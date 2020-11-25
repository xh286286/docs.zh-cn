---
title: CorDebugSetContextFlag 枚举
ms.date: 03/30/2017
api_name:
- CorDebugSetContextFlag
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugSetContextFlag
helpviewer_keywords:
- CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type:
- apiref
ms.openlocfilehash: 078dfefc70704eaadb9cf3c06cfe58f276f7dfce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726010"
---
# <a name="cordebugsetcontextflag-enumeration"></a><span data-ttu-id="e8096-102">CorDebugSetContextFlag 枚举</span><span class="sxs-lookup"><span data-stu-id="e8096-102">CorDebugSetContextFlag Enumeration</span></span>

<span data-ttu-id="e8096-103">指示上下文是来自堆栈上的活动（或叶）帧，还是已通过从另一个帧展开来进行计算。</span><span class="sxs-lookup"><span data-stu-id="e8096-103">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8096-104">语法</span><span class="sxs-lookup"><span data-stu-id="e8096-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="e8096-105">成员</span><span class="sxs-lookup"><span data-stu-id="e8096-105">Members</span></span>  
  
|<span data-ttu-id="e8096-106">成员</span><span class="sxs-lookup"><span data-stu-id="e8096-106">Member</span></span>|<span data-ttu-id="e8096-107">说明</span><span class="sxs-lookup"><span data-stu-id="e8096-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="e8096-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span><span class="sxs-lookup"><span data-stu-id="e8096-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span></span>|<span data-ttu-id="e8096-109">上下文是线程的活动上下文。</span><span class="sxs-lookup"><span data-stu-id="e8096-109">The context is the thread’s active context.</span></span>|  
|<span data-ttu-id="e8096-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span><span class="sxs-lookup"><span data-stu-id="e8096-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span></span>|<span data-ttu-id="e8096-111">已通过从另一个帧展开上下文来计算上下文。</span><span class="sxs-lookup"><span data-stu-id="e8096-111">The context has been computed by unwinding from another frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8096-112">注解</span><span class="sxs-lookup"><span data-stu-id="e8096-112">Remarks</span></span>  

 <span data-ttu-id="e8096-113">`CorDebugSetContextFlag` 提供 [ICorDebugStackWalk：： SetContext](icordebugstackwalk-setcontext-method.md) 方法使用的值。</span><span class="sxs-lookup"><span data-stu-id="e8096-113">`CorDebugSetContextFlag` provides values that are used by the [ICorDebugStackWalk::SetContext](icordebugstackwalk-setcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8096-114">要求</span><span class="sxs-lookup"><span data-stu-id="e8096-114">Requirements</span></span>  

 <span data-ttu-id="e8096-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8096-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8096-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e8096-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e8096-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8096-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8096-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8096-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8096-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8096-119">See also</span></span>

- [<span data-ttu-id="e8096-120">调试枚举</span><span class="sxs-lookup"><span data-stu-id="e8096-120">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="e8096-121">调试</span><span class="sxs-lookup"><span data-stu-id="e8096-121">Debugging</span></span>](index.md)
