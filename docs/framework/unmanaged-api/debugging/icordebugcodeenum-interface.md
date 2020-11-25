---
title: ICorDebugCodeEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCodeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCodeEnum
helpviewer_keywords:
- ICorDebugCodeEnum interface [.NET Framework debugging]
ms.assetid: b5589171-a4a0-4c00-bbdc-6e0a42233b75
topic_type:
- apiref
ms.openlocfilehash: b611dcabc1e5cc36f5c6342f0a832cc81de8c1d5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720732"
---
# <a name="icordebugcodeenum-interface"></a><span data-ttu-id="b8097-102">ICorDebugCodeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="b8097-102">ICorDebugCodeEnum Interface</span></span>

<span data-ttu-id="b8097-103">实现 "ICorDebugEnum" 方法，并枚举 "ICorDebugCode" 数组。</span><span class="sxs-lookup"><span data-stu-id="b8097-103">Implements "ICorDebugEnum" methods, and enumerates "ICorDebugCode" arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b8097-104">方法</span><span class="sxs-lookup"><span data-stu-id="b8097-104">Methods</span></span>  
  
|<span data-ttu-id="b8097-105">方法</span><span class="sxs-lookup"><span data-stu-id="b8097-105">Method</span></span>|<span data-ttu-id="b8097-106">说明</span><span class="sxs-lookup"><span data-stu-id="b8097-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b8097-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="b8097-107">Next Method</span></span>](icordebugcodeenum-next-method.md)|<span data-ttu-id="b8097-108">`ICorDebugCode`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="b8097-108">Gets the specified number of `ICorDebugCode` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8097-109">注解</span><span class="sxs-lookup"><span data-stu-id="b8097-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b8097-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b8097-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8097-111">要求</span><span class="sxs-lookup"><span data-stu-id="b8097-111">Requirements</span></span>  

 <span data-ttu-id="b8097-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8097-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8097-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b8097-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b8097-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8097-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8097-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8097-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8097-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8097-116">See also</span></span>

- [<span data-ttu-id="b8097-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="b8097-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
