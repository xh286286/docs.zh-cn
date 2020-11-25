---
title: ICorDebugModuleEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum
helpviewer_keywords:
- ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 2fb93cd6-6d47-4fdc-a9a0-047726fd03a1
topic_type:
- apiref
ms.openlocfilehash: 08d16393a04888cd3f1a03fa209a1fceac28520b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724749"
---
# <a name="icordebugmoduleenum-interface"></a><span data-ttu-id="9304e-102">ICorDebugModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="9304e-102">ICorDebugModuleEnum Interface</span></span>

<span data-ttu-id="9304e-103">实现 ICorDebugEnum 方法，并枚举 ICorDebugModule 数组。</span><span class="sxs-lookup"><span data-stu-id="9304e-103">Implements ICorDebugEnum methods, and enumerates ICorDebugModule arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9304e-104">方法</span><span class="sxs-lookup"><span data-stu-id="9304e-104">Methods</span></span>  
  
|<span data-ttu-id="9304e-105">方法</span><span class="sxs-lookup"><span data-stu-id="9304e-105">Method</span></span>|<span data-ttu-id="9304e-106">说明</span><span class="sxs-lookup"><span data-stu-id="9304e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9304e-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="9304e-107">Next Method</span></span>](icordebugmoduleenum-next-method.md)|<span data-ttu-id="9304e-108">`ICorDebugModule`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="9304e-108">Gets the specified number of `ICorDebugModule` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9304e-109">注解</span><span class="sxs-lookup"><span data-stu-id="9304e-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9304e-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="9304e-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9304e-111">要求</span><span class="sxs-lookup"><span data-stu-id="9304e-111">Requirements</span></span>  

 <span data-ttu-id="9304e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9304e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9304e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9304e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9304e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9304e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9304e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9304e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9304e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9304e-116">See also</span></span>

- [<span data-ttu-id="9304e-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="9304e-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
