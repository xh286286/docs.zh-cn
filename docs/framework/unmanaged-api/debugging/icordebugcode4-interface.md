---
title: ICorDebugCode4 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCode4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode4
helpviewer_keywords:
- ICorDebugCode4 interface [.NET Framework debugging]
ms.assetid: a3fdf523-274a-449c-920b-9fcb0aed1d97
topic_type:
- apiref
ms.openlocfilehash: 8a373afdf41590ec44a7cbac7360719a12faa82e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720719"
---
# <a name="icordebugcode4-interface"></a><span data-ttu-id="ef887-102">ICorDebugCode4 接口</span><span class="sxs-lookup"><span data-stu-id="ef887-102">ICorDebugCode4 Interface</span></span>

<span data-ttu-id="ef887-103">提供一个方法，该方法使调试器可以枚举函数中的局部变量和参数。</span><span class="sxs-lookup"><span data-stu-id="ef887-103">Provides a method that enables a debugger to enumerate the local variables and arguments in a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ef887-104">方法</span><span class="sxs-lookup"><span data-stu-id="ef887-104">Methods</span></span>  
  
|<span data-ttu-id="ef887-105">方法</span><span class="sxs-lookup"><span data-stu-id="ef887-105">Method</span></span>|<span data-ttu-id="ef887-106">说明</span><span class="sxs-lookup"><span data-stu-id="ef887-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ef887-107">EnumerateVariableHomes 方法</span><span class="sxs-lookup"><span data-stu-id="ef887-107">EnumerateVariableHomes Method</span></span>](icordebugcode4-enumeratevariablehomes-method.md)|<span data-ttu-id="ef887-108">获取函数中局部变量和参数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="ef887-108">Gets an enumerator to the local variables and arguments in a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ef887-109">注解</span><span class="sxs-lookup"><span data-stu-id="ef887-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ef887-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="ef887-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef887-111">要求</span><span class="sxs-lookup"><span data-stu-id="ef887-111">Requirements</span></span>  

 <span data-ttu-id="ef887-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ef887-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef887-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ef887-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ef887-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ef887-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ef887-115">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef887-115">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef887-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef887-116">See also</span></span>

- [<span data-ttu-id="ef887-117">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="ef887-117">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)
- [<span data-ttu-id="ef887-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="ef887-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
