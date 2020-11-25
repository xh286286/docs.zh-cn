---
title: ICorDebugBreakpointEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpointEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpointEnum
helpviewer_keywords:
- ICorDebugBreakpointEnum interface [.NET Framework debugging]
ms.assetid: 4c6f4f6e-52cc-402e-881b-7b8526544c90
topic_type:
- apiref
ms.openlocfilehash: 97e06a2f20dcc2bb3815b98ba29ff230e37ff29d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730157"
---
# <a name="icordebugbreakpointenum-interface"></a><span data-ttu-id="1fa9b-102">ICorDebugBreakpointEnum 接口</span><span class="sxs-lookup"><span data-stu-id="1fa9b-102">ICorDebugBreakpointEnum Interface</span></span>

<span data-ttu-id="1fa9b-103">实现 ICorDebugEnum 方法，并枚举 ICorDebugBreakpoint 数组。</span><span class="sxs-lookup"><span data-stu-id="1fa9b-103">Implements ICorDebugEnum methods, and enumerates ICorDebugBreakpoint arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1fa9b-104">方法</span><span class="sxs-lookup"><span data-stu-id="1fa9b-104">Methods</span></span>  
  
|<span data-ttu-id="1fa9b-105">方法</span><span class="sxs-lookup"><span data-stu-id="1fa9b-105">Method</span></span>|<span data-ttu-id="1fa9b-106">说明</span><span class="sxs-lookup"><span data-stu-id="1fa9b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1fa9b-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="1fa9b-107">Next Method</span></span>](icordebugbreakpointenum-next-method.md)|<span data-ttu-id="1fa9b-108">`ICorDebugBreakpoint`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="1fa9b-108">Gets the specified number of `ICorDebugBreakpoint` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fa9b-109">注解</span><span class="sxs-lookup"><span data-stu-id="1fa9b-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1fa9b-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="1fa9b-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fa9b-111">要求</span><span class="sxs-lookup"><span data-stu-id="1fa9b-111">Requirements</span></span>  

 <span data-ttu-id="1fa9b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fa9b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fa9b-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1fa9b-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fa9b-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fa9b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fa9b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fa9b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fa9b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1fa9b-116">See also</span></span>

- [<span data-ttu-id="1fa9b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="1fa9b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
