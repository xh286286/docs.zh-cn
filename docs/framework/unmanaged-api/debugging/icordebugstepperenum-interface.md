---
title: ICorDebugStepperEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum
helpviewer_keywords:
- ICorDebugStepperEnum interface [.NET Framework debugging]
ms.assetid: 988718c1-1a4a-40f2-a04c-7d67e5cfe1e2
topic_type:
- apiref
ms.openlocfilehash: facea5cd7f0b0e0e6c0b1049e87a2355f1d3965a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697163"
---
# <a name="icordebugstepperenum-interface"></a><span data-ttu-id="d955b-102">ICorDebugStepperEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d955b-102">ICorDebugStepperEnum Interface</span></span>

<span data-ttu-id="d955b-103">实现 ICorDebugEnum 方法，并枚举 ICorDebugStepper 数组。</span><span class="sxs-lookup"><span data-stu-id="d955b-103">Implements ICorDebugEnum methods, and enumerates ICorDebugStepper arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d955b-104">方法</span><span class="sxs-lookup"><span data-stu-id="d955b-104">Methods</span></span>  
  
|<span data-ttu-id="d955b-105">方法</span><span class="sxs-lookup"><span data-stu-id="d955b-105">Method</span></span>|<span data-ttu-id="d955b-106">说明</span><span class="sxs-lookup"><span data-stu-id="d955b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d955b-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="d955b-107">Next Method</span></span>](icordebugstepperenum-next-method.md)|<span data-ttu-id="d955b-108">`ICorDebugStepper`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="d955b-108">Gets the specified number of `ICorDebugStepper` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d955b-109">注解</span><span class="sxs-lookup"><span data-stu-id="d955b-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d955b-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="d955b-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d955b-111">要求</span><span class="sxs-lookup"><span data-stu-id="d955b-111">Requirements</span></span>  

 <span data-ttu-id="d955b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d955b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d955b-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d955b-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d955b-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d955b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d955b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d955b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d955b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d955b-116">See also</span></span>

- [<span data-ttu-id="d955b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="d955b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
