---
title: FunctionLeave 函数
ms.date: 03/30/2017
api_name:
- FunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionLeave
helpviewer_keywords:
- FunctionLeave function [.NET Framework profiling]
ms.assetid: 18e89f45-e068-426a-be16-9f53a4346860
topic_type:
- apiref
ms.openlocfilehash: 13636da9c3e8ac4aa9e8dc1fa02b2e33afef4717
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722253"
---
# <a name="functionleave-function"></a><span data-ttu-id="d96f3-102">FunctionLeave 函数</span><span class="sxs-lookup"><span data-stu-id="d96f3-102">FunctionLeave Function</span></span>

<span data-ttu-id="d96f3-103">通知探查器某个函数将要返回到调用方。</span><span class="sxs-lookup"><span data-stu-id="d96f3-103">Notifies the profiler that a function is about to return to the caller.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d96f3-104">`FunctionLeave`.NET Framework 2.0 中不推荐使用该函数。</span><span class="sxs-lookup"><span data-stu-id="d96f3-104">The `FunctionLeave` function is deprecated in the .NET Framework 2.0.</span></span> <span data-ttu-id="d96f3-105">它将继续运行，但会导致性能下降。</span><span class="sxs-lookup"><span data-stu-id="d96f3-105">It will continue to work, but will incur a performance penalty.</span></span> <span data-ttu-id="d96f3-106">改为使用 [FunctionLeave2](functionleave2-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="d96f3-106">Use the [FunctionLeave2](functionleave2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d96f3-107">语法</span><span class="sxs-lookup"><span data-stu-id="d96f3-107">Syntax</span></span>  
  
```cpp  
void __stdcall FunctionLeave (  
    [in] FunctionID funcID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d96f3-108">参数</span><span class="sxs-lookup"><span data-stu-id="d96f3-108">Parameters</span></span>

- `funcID`

  <span data-ttu-id="d96f3-109">\[in] 返回的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="d96f3-109">\[in] The identifier of the function that is returning.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96f3-110">注解</span><span class="sxs-lookup"><span data-stu-id="d96f3-110">Remarks</span></span>  

 <span data-ttu-id="d96f3-111">`FunctionLeave`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="d96f3-111">The `FunctionLeave` function is a callback; you must implement it.</span></span> <span data-ttu-id="d96f3-112">实现必须使用 `__declspec` `naked`) 存储类特性的 (。</span><span class="sxs-lookup"><span data-stu-id="d96f3-112">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="d96f3-113">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="d96f3-113">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="d96f3-114">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="d96f3-114">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="d96f3-115">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="d96f3-115">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="d96f3-116">的实现 `FunctionLeave` 不应被阻止，因为它将延迟垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="d96f3-116">The implementation of `FunctionLeave` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="d96f3-117">实现不应尝试垃圾回收，因为堆栈可能不处于垃圾回收友好状态。</span><span class="sxs-lookup"><span data-stu-id="d96f3-117">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="d96f3-118">如果尝试垃圾回收，则运行时将被阻止，直到 `FunctionLeave` 返回。</span><span class="sxs-lookup"><span data-stu-id="d96f3-118">If a garbage collection is attempted, the runtime will block until `FunctionLeave` returns.</span></span>  
  
 <span data-ttu-id="d96f3-119">此外，该 `FunctionLeave` 函数不得调入托管代码或以任何方式导致托管的内存分配。</span><span class="sxs-lookup"><span data-stu-id="d96f3-119">Also, the `FunctionLeave` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d96f3-120">要求</span><span class="sxs-lookup"><span data-stu-id="d96f3-120">Requirements</span></span>  

 <span data-ttu-id="d96f3-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d96f3-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d96f3-122">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="d96f3-122">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="d96f3-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d96f3-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d96f3-124">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="d96f3-124">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d96f3-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d96f3-125">See also</span></span>

- [<span data-ttu-id="d96f3-126">FunctionEnter2 函数</span><span class="sxs-lookup"><span data-stu-id="d96f3-126">FunctionEnter2 Function</span></span>](functionenter2-function.md)
- [<span data-ttu-id="d96f3-127">FunctionLeave2 函数</span><span class="sxs-lookup"><span data-stu-id="d96f3-127">FunctionLeave2 Function</span></span>](functionleave2-function.md)
- [<span data-ttu-id="d96f3-128">FunctionTailcall2 函数</span><span class="sxs-lookup"><span data-stu-id="d96f3-128">FunctionTailcall2 Function</span></span>](functiontailcall2-function.md)
- [<span data-ttu-id="d96f3-129">SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="d96f3-129">SetEnterLeaveFunctionHooks2 Method</span></span>](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [<span data-ttu-id="d96f3-130">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="d96f3-130">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
