---
title: ICorDebugFrameEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFrameEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrameEnum
helpviewer_keywords:
- ICorDebugFrameEnum interface [.NET Framework debugging]
ms.assetid: ee3f85d3-044e-46b8-945c-93ebfa5d9e91
topic_type:
- apiref
ms.openlocfilehash: 4277a552d217ad7f601bfe72cae32a1f25dd6be4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696227"
---
# <a name="icordebugframeenum-interface"></a><span data-ttu-id="3ac95-102">ICorDebugFrameEnum 接口</span><span class="sxs-lookup"><span data-stu-id="3ac95-102">ICorDebugFrameEnum Interface</span></span>

<span data-ttu-id="3ac95-103">实现 ICorDebugEnum 方法，并枚举 ICorDebugFrame 数组。</span><span class="sxs-lookup"><span data-stu-id="3ac95-103">Implements ICorDebugEnum methods, and enumerates ICorDebugFrame arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3ac95-104">方法</span><span class="sxs-lookup"><span data-stu-id="3ac95-104">Methods</span></span>  
  
|<span data-ttu-id="3ac95-105">方法</span><span class="sxs-lookup"><span data-stu-id="3ac95-105">Method</span></span>|<span data-ttu-id="3ac95-106">说明</span><span class="sxs-lookup"><span data-stu-id="3ac95-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3ac95-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="3ac95-107">Next Method</span></span>](icordebugframeenum-next-method.md)|<span data-ttu-id="3ac95-108">`ICorDebugFrame`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="3ac95-108">Gets the specified number of `ICorDebugFrame` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3ac95-109">注解</span><span class="sxs-lookup"><span data-stu-id="3ac95-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3ac95-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3ac95-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ac95-111">要求</span><span class="sxs-lookup"><span data-stu-id="3ac95-111">Requirements</span></span>  

 <span data-ttu-id="3ac95-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3ac95-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ac95-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3ac95-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3ac95-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3ac95-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3ac95-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ac95-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ac95-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3ac95-116">See also</span></span>

- [<span data-ttu-id="3ac95-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="3ac95-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
