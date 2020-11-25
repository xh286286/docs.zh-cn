---
title: CorDebugExceptionObjectStackFrame 结构
ms.date: 03/30/2017
api_name:
- CorDebugExceptionObjectStackFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionObjectStackFrame
helpviewer_keywords:
- CorDebugExceptionObjectStackFrame structure [.NET Framework debugging]
ms.assetid: 542cdd81-5ae7-4361-b0ef-1ae4775df258
topic_type:
- apiref
ms.openlocfilehash: 9b904596ed1cce4c4cf2676676508dfb3851e8ce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712672"
---
# <a name="cordebugexceptionobjectstackframe-structure"></a><span data-ttu-id="fe775-102">CorDebugExceptionObjectStackFrame 结构</span><span class="sxs-lookup"><span data-stu-id="fe775-102">CorDebugExceptionObjectStackFrame Structure</span></span>

<span data-ttu-id="fe775-103">表示异常对象中的堆栈帧信息。</span><span class="sxs-lookup"><span data-stu-id="fe775-103">Represents stack frame information from an exception object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe775-104">语法</span><span class="sxs-lookup"><span data-stu-id="fe775-104">Syntax</span></span>  
  
```cpp  
typedef struct CorDebugExceptionObjectStackFrame {  
    ICorDebugModule* pModule;  
    CORDB_ADDRESS ip;  
    mdMethodDef methodDef;  
    BOOL isLastForeignExceptionFrame;  
} CorDebugExceptionObjectStackFrame;  
```  
  
## <a name="members"></a><span data-ttu-id="fe775-105">成员</span><span class="sxs-lookup"><span data-stu-id="fe775-105">Members</span></span>  
  
|<span data-ttu-id="fe775-106">成员</span><span class="sxs-lookup"><span data-stu-id="fe775-106">Member</span></span>|<span data-ttu-id="fe775-107">说明</span><span class="sxs-lookup"><span data-stu-id="fe775-107">Description</span></span>|  
|------------|-----------------|  
|`pModule`|<span data-ttu-id="fe775-108">指向当前帧的 ICorDebugModule 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="fe775-108">A pointer to the ICorDebugModule object for the current frame.</span></span>|  
|`ip`|<span data-ttu-id="fe775-109">指令指针的值 (当前帧的 EIP/裂缝) 。</span><span class="sxs-lookup"><span data-stu-id="fe775-109">The value of the instruction pointer (EIP/RIP) for the current frame.</span></span>|  
|`methodDef`|<span data-ttu-id="fe775-110">当前帧的方法标记。</span><span class="sxs-lookup"><span data-stu-id="fe775-110">The method token for the current frame.</span></span>|  
|`isLastForeignExceptionFrame`|<span data-ttu-id="fe775-111">一个值，该值指示帧是否为外部异常中的最后一个帧。</span><span class="sxs-lookup"><span data-stu-id="fe775-111">A value that indicates whether the frame is the last frame in a foreign exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe775-112">注解</span><span class="sxs-lookup"><span data-stu-id="fe775-112">Remarks</span></span>  

 <span data-ttu-id="fe775-113">当不再使用 ICorDebugModule 对象时，调用方必须释放指向该对象的指针。</span><span class="sxs-lookup"><span data-stu-id="fe775-113">The caller must release the pointer to the ICorDebugModule object once it is no longer in use.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe775-114">要求</span><span class="sxs-lookup"><span data-stu-id="fe775-114">Requirements</span></span>  

 <span data-ttu-id="fe775-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe775-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe775-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fe775-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fe775-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe775-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe775-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe775-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe775-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe775-119">See also</span></span>

- [<span data-ttu-id="fe775-120">调试结构</span><span class="sxs-lookup"><span data-stu-id="fe775-120">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="fe775-121">调试</span><span class="sxs-lookup"><span data-stu-id="fe775-121">Debugging</span></span>](index.md)
