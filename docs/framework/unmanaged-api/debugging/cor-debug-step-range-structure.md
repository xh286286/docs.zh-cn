---
title: COR_DEBUG_STEP_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_DEBUG_STEP_RANGE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_STEP_RANGE
helpviewer_keywords:
- COR_DEBUG_STEP_RANGE structure [.NET Framework debugging]
ms.assetid: 8809d00e-beaa-4dcf-b4e8-e89d0a5406b7
topic_type:
- apiref
ms.openlocfilehash: cd85ba2e6a907ff9546614e02b4da5f45e74b924
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726634"
---
# <a name="cor_debug_step_range-structure"></a><span data-ttu-id="a40b6-102">COR_DEBUG_STEP_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="a40b6-102">COR_DEBUG_STEP_RANGE Structure</span></span>

<span data-ttu-id="a40b6-103">包含代码区域的偏离量信息。</span><span class="sxs-lookup"><span data-stu-id="a40b6-103">Contains the offset information for a range of code.</span></span>  
  
 <span data-ttu-id="a40b6-104">此结构由 [ICorDebugStepper：： StepRange](icordebugstepper-steprange-method.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="a40b6-104">This structure is used by the [ICorDebugStepper::StepRange](icordebugstepper-steprange-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a40b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="a40b6-105">Syntax</span></span>  
  
```cpp  
typedef struct {  
    ULONG32 startOffset;  
    ULONG32 endOffset;  
} COR_DEBUG_STEP_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="a40b6-106">成员</span><span class="sxs-lookup"><span data-stu-id="a40b6-106">Members</span></span>  
  
|<span data-ttu-id="a40b6-107">成员</span><span class="sxs-lookup"><span data-stu-id="a40b6-107">Member</span></span>|<span data-ttu-id="a40b6-108">说明</span><span class="sxs-lookup"><span data-stu-id="a40b6-108">Description</span></span>|  
|------------|-----------------|  
|`startOffset`|<span data-ttu-id="a40b6-109">范围开始处的偏移量。</span><span class="sxs-lookup"><span data-stu-id="a40b6-109">The offset of the beginning of the range.</span></span>|  
|`endOffset`|<span data-ttu-id="a40b6-110">范围末尾的偏移量。</span><span class="sxs-lookup"><span data-stu-id="a40b6-110">The offset of the end of the range.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a40b6-111">要求</span><span class="sxs-lookup"><span data-stu-id="a40b6-111">Requirements</span></span>  

 <span data-ttu-id="a40b6-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a40b6-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a40b6-113">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="a40b6-113">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="a40b6-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a40b6-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a40b6-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a40b6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a40b6-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a40b6-116">See also</span></span>

- [<span data-ttu-id="a40b6-117">StepRange 方法</span><span class="sxs-lookup"><span data-stu-id="a40b6-117">StepRange Method</span></span>](icordebugstepper-steprange-method.md)
- [<span data-ttu-id="a40b6-118">调试结构</span><span class="sxs-lookup"><span data-stu-id="a40b6-118">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="a40b6-119">调试</span><span class="sxs-lookup"><span data-stu-id="a40b6-119">Debugging</span></span>](index.md)
