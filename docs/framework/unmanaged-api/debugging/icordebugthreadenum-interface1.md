---
title: ICorDebugThreadEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThreadEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThreadEnum
helpviewer_keywords:
- ICorDebugThreadEnum interface [.NET Framework debugging]
ms.assetid: 796de687-7dd4-4b7b-a10b-8bf22dc7779f
topic_type:
- apiref
ms.openlocfilehash: ca7668f23671721477c561774bab03279c4c18c8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95678550"
---
# <a name="icordebugthreadenum-interface"></a><span data-ttu-id="68f81-102">ICorDebugThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="68f81-102">ICorDebugThreadEnum Interface</span></span>

<span data-ttu-id="68f81-103">实现 ICorDebugEnum 方法并枚举 ICorDebugThread 数组。</span><span class="sxs-lookup"><span data-stu-id="68f81-103">Implements ICorDebugEnum methods and enumerates ICorDebugThread arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="68f81-104">方法</span><span class="sxs-lookup"><span data-stu-id="68f81-104">Methods</span></span>  
  
|<span data-ttu-id="68f81-105">方法</span><span class="sxs-lookup"><span data-stu-id="68f81-105">Method</span></span>|<span data-ttu-id="68f81-106">说明</span><span class="sxs-lookup"><span data-stu-id="68f81-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="68f81-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="68f81-107">Next Method</span></span>](icordebugthreadenum-next-method.md)|<span data-ttu-id="68f81-108">`ICorDebugThread`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="68f81-108">Gets the specified number of `ICorDebugThread` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="68f81-109">注解</span><span class="sxs-lookup"><span data-stu-id="68f81-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="68f81-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="68f81-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68f81-111">要求</span><span class="sxs-lookup"><span data-stu-id="68f81-111">Requirements</span></span>  

 <span data-ttu-id="68f81-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="68f81-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68f81-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="68f81-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="68f81-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68f81-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68f81-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68f81-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68f81-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="68f81-116">See also</span></span>

- [<span data-ttu-id="68f81-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="68f81-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
