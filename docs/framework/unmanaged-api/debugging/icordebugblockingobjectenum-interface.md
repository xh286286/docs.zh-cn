---
title: ICorDebugBlockingObjectEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBlockingObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBlockingObjectEnum
helpviewer_keywords:
- ICorDebugBlockingObjectEnum interface [.NET Framework debugging]
ms.assetid: 208e5c2d-3f3f-404e-8b3c-7cccc14ddb16
topic_type:
- apiref
ms.openlocfilehash: 221acf9bea714728a81b9f15c8165c1f9eba16a8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719198"
---
# <a name="icordebugblockingobjectenum-interface"></a><span data-ttu-id="7a914-102">ICorDebugBlockingObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7a914-102">ICorDebugBlockingObjectEnum Interface</span></span>

<span data-ttu-id="7a914-103">为 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的列表提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="7a914-103">Provides an enumerator for a list of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures.</span></span> <span data-ttu-id="7a914-104">此接口是 ICorDebugEnum 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="7a914-104">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7a914-105">方法</span><span class="sxs-lookup"><span data-stu-id="7a914-105">Methods</span></span>  
  
|<span data-ttu-id="7a914-106">方法</span><span class="sxs-lookup"><span data-stu-id="7a914-106">Method</span></span>|<span data-ttu-id="7a914-107">说明</span><span class="sxs-lookup"><span data-stu-id="7a914-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7a914-108">Next 方法</span><span class="sxs-lookup"><span data-stu-id="7a914-108">Next Method</span></span>](icordebugblockingobjectenum-next-method.md)|<span data-ttu-id="7a914-109">枚举 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的列表。</span><span class="sxs-lookup"><span data-stu-id="7a914-109">Enumerates through a list of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a914-110">注解</span><span class="sxs-lookup"><span data-stu-id="7a914-110">Remarks</span></span>  

 <span data-ttu-id="7a914-111">每个 `CorDebugBlockingObject` 结构均表示一个阻塞线程的对象。</span><span class="sxs-lookup"><span data-stu-id="7a914-111">Each `CorDebugBlockingObject` structure represents an object that is blocking a thread.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7a914-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="7a914-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a914-113">要求</span><span class="sxs-lookup"><span data-stu-id="7a914-113">Requirements</span></span>  

 <span data-ttu-id="7a914-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a914-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a914-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7a914-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7a914-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a914-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a914-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a914-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a914-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a914-118">See also</span></span>

- [<span data-ttu-id="7a914-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="7a914-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="7a914-120">调试</span><span class="sxs-lookup"><span data-stu-id="7a914-120">Debugging</span></span>](index.md)
