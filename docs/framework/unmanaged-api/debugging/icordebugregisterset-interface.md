---
title: ICorDebugRegisterSet 接口
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet
helpviewer_keywords:
- ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: d3d9676d-0b87-4bc3-b679-7bbc7a186c88
topic_type:
- apiref
ms.openlocfilehash: 940810288b72be0d4dfc5366176663c22c369ebb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712373"
---
# <a name="icordebugregisterset-interface"></a><span data-ttu-id="79c93-102">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="79c93-102">ICorDebugRegisterSet Interface</span></span>

<span data-ttu-id="79c93-103">表示在当前正在执行代码的计算机上可用的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="79c93-103">Represents the set of registers available on the computer that is currently executing code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="79c93-104">方法</span><span class="sxs-lookup"><span data-stu-id="79c93-104">Methods</span></span>  
  
|<span data-ttu-id="79c93-105">方法</span><span class="sxs-lookup"><span data-stu-id="79c93-105">Method</span></span>|<span data-ttu-id="79c93-106">说明</span><span class="sxs-lookup"><span data-stu-id="79c93-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="79c93-107">GetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="79c93-107">GetRegisters Method</span></span>](icordebugregisterset-getregisters-method.md)|<span data-ttu-id="79c93-108">获取计算机上每个寄存器 (的值，该计算机当前正在执行位掩码指定的代码) 。</span><span class="sxs-lookup"><span data-stu-id="79c93-108">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="79c93-109">GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="79c93-109">GetRegistersAvailable Method</span></span>](icordebugregisterset-getregistersavailable-method.md)|<span data-ttu-id="79c93-110">获取一个位掩码，指示此中的哪些寄存器 `ICorDebugRegisterSet` 当前可用。</span><span class="sxs-lookup"><span data-stu-id="79c93-110">Gets a bit mask indicating which registers in this `ICorDebugRegisterSet` are currently available.</span></span>|  
|[<span data-ttu-id="79c93-111">GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="79c93-111">GetThreadContext Method</span></span>](icordebugregisterset-getthreadcontext-method.md)|<span data-ttu-id="79c93-112">获取当前线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="79c93-112">Gets the context of the current thread.</span></span>|  
|[<span data-ttu-id="79c93-113">SetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="79c93-113">SetRegisters Method</span></span>](icordebugregisterset-setregisters-method.md)|<span data-ttu-id="79c93-114">未实现 .NET Framework 版本2.0。</span><span class="sxs-lookup"><span data-stu-id="79c93-114">Not implemented for the .NET Framework version 2.0.</span></span>|  
|[<span data-ttu-id="79c93-115">SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="79c93-115">SetThreadContext Method</span></span>](icordebugregisterset-setthreadcontext-method.md)|<span data-ttu-id="79c93-116">未实现 2.0 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="79c93-116">Not implemented for the .NET Framework 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="79c93-117">注解</span><span class="sxs-lookup"><span data-stu-id="79c93-117">Remarks</span></span>  

 <span data-ttu-id="79c93-118">`ICorDebugRegisterSet`接口仅支持32位寄存器。</span><span class="sxs-lookup"><span data-stu-id="79c93-118">The `ICorDebugRegisterSet` interface supports only 32-bit registers.</span></span> <span data-ttu-id="79c93-119">使用需要额外注册的平台（如 IA-64）上的 [ICorDebugRegisterSet2](icordebugregisterset2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="79c93-119">Use the [ICorDebugRegisterSet2](icordebugregisterset2-interface.md) interface on platforms such as IA-64 that require additional registers.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="79c93-120">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="79c93-120">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79c93-121">要求</span><span class="sxs-lookup"><span data-stu-id="79c93-121">Requirements</span></span>  

 <span data-ttu-id="79c93-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79c93-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79c93-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="79c93-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="79c93-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79c93-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79c93-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79c93-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79c93-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79c93-126">See also</span></span>

- [<span data-ttu-id="79c93-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="79c93-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="79c93-128">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="79c93-128">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
