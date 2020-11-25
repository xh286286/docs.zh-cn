---
title: ICorDebugObjectEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectEnum
helpviewer_keywords:
- ICorDebugObjectEnum interface [.NET Framework debugging]
ms.assetid: 9ffb4498-7719-49d3-8890-df2c22248a0c
topic_type:
- apiref
ms.openlocfilehash: 9400c4fa3ddcefef923d7bcfaae80e2cef62dc7d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95695460"
---
# <a name="icordebugobjectenum-interface"></a><span data-ttu-id="98b6e-102">ICorDebugObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="98b6e-102">ICorDebugObjectEnum Interface</span></span>

<span data-ttu-id="98b6e-103">实现 ICorDebugEnum 方法，并按它们相对虚拟地址 (Rva) 来枚举对象数组。</span><span class="sxs-lookup"><span data-stu-id="98b6e-103">Implements ICorDebugEnum methods, and enumerates arrays of objects by their relative virtual addresses (RVAs).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="98b6e-104">方法</span><span class="sxs-lookup"><span data-stu-id="98b6e-104">Methods</span></span>  
  
|<span data-ttu-id="98b6e-105">方法</span><span class="sxs-lookup"><span data-stu-id="98b6e-105">Method</span></span>|<span data-ttu-id="98b6e-106">说明</span><span class="sxs-lookup"><span data-stu-id="98b6e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="98b6e-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="98b6e-107">Next Method</span></span>](icordebugobjectenum-next-method.md)|<span data-ttu-id="98b6e-108">从当前位置开始，获取枚举中指定数量的对象的 Rva。</span><span class="sxs-lookup"><span data-stu-id="98b6e-108">Gets the RVAs of the specified number of objects from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="98b6e-109">注解</span><span class="sxs-lookup"><span data-stu-id="98b6e-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="98b6e-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="98b6e-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98b6e-111">要求</span><span class="sxs-lookup"><span data-stu-id="98b6e-111">Requirements</span></span>  

 <span data-ttu-id="98b6e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="98b6e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98b6e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="98b6e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="98b6e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="98b6e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="98b6e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="98b6e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98b6e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98b6e-116">See also</span></span>

- [<span data-ttu-id="98b6e-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="98b6e-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
