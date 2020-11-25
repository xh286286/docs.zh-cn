---
title: ICorDebugHeapValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue
helpviewer_keywords:
- ICorDebugHeapValue interface [.NET Framework debugging]
ms.assetid: 1bca66db-0359-4ae8-846e-e35f7e547e8b
topic_type:
- apiref
ms.openlocfilehash: ee3ea319360bba1a113c15daf8cf143ea512e5cd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733316"
---
# <a name="icordebugheapvalue-interface"></a><span data-ttu-id="7a092-102">ICorDebugHeapValue 接口</span><span class="sxs-lookup"><span data-stu-id="7a092-102">ICorDebugHeapValue Interface</span></span>

<span data-ttu-id="7a092-103">"ICorDebugValue" 的子类，它表示公共语言运行时 (CLR) 垃圾回收器收集的对象。</span><span class="sxs-lookup"><span data-stu-id="7a092-103">A subclass of "ICorDebugValue" that represents an object that has been collected by the common language runtime (CLR) garbage collector.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7a092-104">方法</span><span class="sxs-lookup"><span data-stu-id="7a092-104">Methods</span></span>  
  
|<span data-ttu-id="7a092-105">方法</span><span class="sxs-lookup"><span data-stu-id="7a092-105">Method</span></span>|<span data-ttu-id="7a092-106">说明</span><span class="sxs-lookup"><span data-stu-id="7a092-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7a092-107">CreateRelocBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="7a092-107">CreateRelocBreakpoint Method</span></span>](icordebugheapvalue-createrelocbreakpoint-method.md)|<span data-ttu-id="7a092-108">未实现。</span><span class="sxs-lookup"><span data-stu-id="7a092-108">Not implemented.</span></span>|  
|[<span data-ttu-id="7a092-109">IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="7a092-109">IsValid Method</span></span>](icordebugheapvalue-isvalid-method.md)|<span data-ttu-id="7a092-110">获取一个值，该值指示由此表示的对象是否 `ICorDebugHeapValue` 有效，或者是否已被垃圾回收器回收。</span><span class="sxs-lookup"><span data-stu-id="7a092-110">Gets a value that indicates whether the object represented by this `ICorDebugHeapValue` is valid, or has been reclaimed by the garbage collector.</span></span> <span data-ttu-id="7a092-111">此方法在 .NET Framework 版本2.0 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="7a092-111">This method has been deprecated in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a092-112">注解</span><span class="sxs-lookup"><span data-stu-id="7a092-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7a092-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="7a092-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a092-114">要求</span><span class="sxs-lookup"><span data-stu-id="7a092-114">Requirements</span></span>  

 <span data-ttu-id="7a092-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a092-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a092-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7a092-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7a092-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a092-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a092-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a092-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a092-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a092-119">See also</span></span>

- [<span data-ttu-id="7a092-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="7a092-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
