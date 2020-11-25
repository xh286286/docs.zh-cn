---
title: ICorDebugManagedCallback3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback3
helpviewer_keywords:
- ICorDebugManagedCallback3 interface [.NET Framework debugging]
ms.assetid: a95389d3-cf2e-47a4-9805-61426acc6b65
topic_type:
- apiref
ms.openlocfilehash: e04f5be6d2612b26bf7d71807753d170e6a5a7a0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723293"
---
# <a name="icordebugmanagedcallback3-interface"></a><span data-ttu-id="28173-102">ICorDebugManagedCallback3 接口</span><span class="sxs-lookup"><span data-stu-id="28173-102">ICorDebugManagedCallback3 Interface</span></span>

<span data-ttu-id="28173-103">提供一个回调方法，该方法指示已发出启用的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="28173-103">Provides a callback method that indicates that an enabled custom debugger notification has been raised.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="28173-104">方法</span><span class="sxs-lookup"><span data-stu-id="28173-104">Methods</span></span>  
  
|<span data-ttu-id="28173-105">方法</span><span class="sxs-lookup"><span data-stu-id="28173-105">Method</span></span>|<span data-ttu-id="28173-106">说明</span><span class="sxs-lookup"><span data-stu-id="28173-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="28173-107">CustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="28173-107">CustomNotification Method</span></span>](icordebugmanagedcallback3-customnotification-method.md)|<span data-ttu-id="28173-108">指示已引发启用的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="28173-108">Indicates that an enabled custom debugger notification has been raised.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28173-109">注解</span><span class="sxs-lookup"><span data-stu-id="28173-109">Remarks</span></span>  

 <span data-ttu-id="28173-110">此接口是 [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) 和 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="28173-110">This interface is a logical extension of the [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) and [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="28173-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="28173-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28173-112">要求</span><span class="sxs-lookup"><span data-stu-id="28173-112">Requirements</span></span>  

 <span data-ttu-id="28173-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28173-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28173-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="28173-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="28173-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28173-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="28173-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28173-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28173-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28173-117">See also</span></span>

- [<span data-ttu-id="28173-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="28173-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
- [<span data-ttu-id="28173-119">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="28173-119">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="28173-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="28173-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="28173-121">调试</span><span class="sxs-lookup"><span data-stu-id="28173-121">Debugging</span></span>](index.md)
