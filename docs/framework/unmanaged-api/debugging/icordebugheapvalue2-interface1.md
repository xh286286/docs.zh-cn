---
title: ICorDebugHeapValue2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue2
helpviewer_keywords:
- ICorDebugHeapValue2 interface [.NET Framework debugging]
ms.assetid: 87360a52-90b1-4ada-80c0-589a556116d8
topic_type:
- apiref
ms.openlocfilehash: c959856e8c019f95d38cac9bc4d8d03bc31ef195
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726543"
---
# <a name="icordebugheapvalue2-interface"></a><span data-ttu-id="5fdb2-102">ICorDebugHeapValue2 接口</span><span class="sxs-lookup"><span data-stu-id="5fdb2-102">ICorDebugHeapValue2 Interface</span></span>

<span data-ttu-id="5fdb2-103">ICorDebugHeapValue 的扩展，它为公共语言运行时 (CLR) 句柄提供支持。</span><span class="sxs-lookup"><span data-stu-id="5fdb2-103">An extension of ICorDebugHeapValue that provides support for common language runtime (CLR) handles.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5fdb2-104">方法</span><span class="sxs-lookup"><span data-stu-id="5fdb2-104">Methods</span></span>  
  
|<span data-ttu-id="5fdb2-105">方法</span><span class="sxs-lookup"><span data-stu-id="5fdb2-105">Method</span></span>|<span data-ttu-id="5fdb2-106">说明</span><span class="sxs-lookup"><span data-stu-id="5fdb2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5fdb2-107">CreateHandle 方法</span><span class="sxs-lookup"><span data-stu-id="5fdb2-107">CreateHandle Method</span></span>](icordebugheapvalue2-createhandle-method.md)|<span data-ttu-id="5fdb2-108">为此对象创建指定类型的句柄 `ICorDebugHeapValue2` 。</span><span class="sxs-lookup"><span data-stu-id="5fdb2-108">Creates a handle of the specified type for this `ICorDebugHeapValue2` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5fdb2-109">注解</span><span class="sxs-lookup"><span data-stu-id="5fdb2-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="5fdb2-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="5fdb2-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5fdb2-111">要求</span><span class="sxs-lookup"><span data-stu-id="5fdb2-111">Requirements</span></span>  

 <span data-ttu-id="5fdb2-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fdb2-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fdb2-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5fdb2-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5fdb2-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5fdb2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5fdb2-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5fdb2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fdb2-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5fdb2-116">See also</span></span>

- [<span data-ttu-id="5fdb2-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="5fdb2-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
