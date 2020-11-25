---
title: FunctionTailcall3 函数
ms.date: 03/30/2017
api_name:
- FunctionTailcall3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionTailcall3
helpviewer_keywords:
- FunctionTailcall3 function [.NET Framework profiling]
ms.assetid: 1e48243f-5de6-4bd6-a1d0-e1d248bca4b8
topic_type:
- apiref
ms.openlocfilehash: dfe1a530ea009300e7cfbf002053d2e2b6034845
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719276"
---
# <a name="functiontailcall3-function"></a><span data-ttu-id="6c40c-102">FunctionTailcall3 函数</span><span class="sxs-lookup"><span data-stu-id="6c40c-102">FunctionTailcall3 Function</span></span>

<span data-ttu-id="6c40c-103">通知探查器，当前正在执行的函数即将对另一个函数执行尾调用。</span><span class="sxs-lookup"><span data-stu-id="6c40c-103">Notifies the profiler that the currently executing function is about to perform a tail call to another function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c40c-104">语法</span><span class="sxs-lookup"><span data-stu-id="6c40c-104">Syntax</span></span>  
  
```cpp  
void __stdcall FunctionTailcall3 (FunctionOrRemappedID functionOrRemappedID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c40c-105">参数</span><span class="sxs-lookup"><span data-stu-id="6c40c-105">Parameters</span></span>

- `functionOrRemappedID`

  <span data-ttu-id="6c40c-106">\[in] 要进行尾调用的当前正在执行的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="6c40c-106">\[in] The identifier of the currently executing function that is about to make a tail call.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c40c-107">注解</span><span class="sxs-lookup"><span data-stu-id="6c40c-107">Remarks</span></span>  

 <span data-ttu-id="6c40c-108">`FunctionTailcall3`回调函数将在调用函数时通知探查器。</span><span class="sxs-lookup"><span data-stu-id="6c40c-108">The `FunctionTailcall3` callback function notifies the profiler as functions are being called.</span></span> <span data-ttu-id="6c40c-109">使用 [ICorProfilerInfo3：： SetEnterLeaveFunctionHooks3 方法](icorprofilerinfo3-setenterleavefunctionhooks3-method.md) 注册此函数的实现。</span><span class="sxs-lookup"><span data-stu-id="6c40c-109">Use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method](icorprofilerinfo3-setenterleavefunctionhooks3-method.md) to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="6c40c-110">`FunctionTailcall3`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="6c40c-110">The `FunctionTailcall3` function is a callback; you must implement it.</span></span> <span data-ttu-id="6c40c-111">实现必须使用 `__declspec(naked)` 存储类特性。</span><span class="sxs-lookup"><span data-stu-id="6c40c-111">The implementation must use the `__declspec(naked)` storage-class attribute.</span></span>  
  
 <span data-ttu-id="6c40c-112">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="6c40c-112">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="6c40c-113">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="6c40c-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="6c40c-114">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="6c40c-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="6c40c-115">的实现 `FunctionTailcall3` 不应阻塞，因为它将延迟垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="6c40c-115">The implementation of `FunctionTailcall3` should not block, because it will delay garbage collection.</span></span> <span data-ttu-id="6c40c-116">实现不应尝试垃圾回收，因为堆栈可能不处于垃圾回收友好状态。</span><span class="sxs-lookup"><span data-stu-id="6c40c-116">The implementation should not attempt a garbage collection, because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="6c40c-117">如果尝试垃圾回收，则运行时将被阻止，直到 `FunctionTailcall3` 返回。</span><span class="sxs-lookup"><span data-stu-id="6c40c-117">If a garbage collection is attempted, the runtime will block until `FunctionTailcall3` returns.</span></span>  
  
 <span data-ttu-id="6c40c-118">`FunctionTailcall3`函数不得调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="6c40c-118">The `FunctionTailcall3` function must not call into managed code or cause a managed memory allocation in any way.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c40c-119">要求</span><span class="sxs-lookup"><span data-stu-id="6c40c-119">Requirements</span></span>  

 <span data-ttu-id="6c40c-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c40c-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c40c-121">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="6c40c-121">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="6c40c-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c40c-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6c40c-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c40c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c40c-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c40c-124">See also</span></span>

- [<span data-ttu-id="6c40c-125">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="6c40c-125">FunctionEnter3</span></span>](functionenter3-function.md)
- [<span data-ttu-id="6c40c-126">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="6c40c-126">FunctionLeave3</span></span>](functionleave3-function.md)
- [<span data-ttu-id="6c40c-127">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="6c40c-127">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="6c40c-128">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="6c40c-128">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="6c40c-129">FunctionTailcall3WithInfo 函数</span><span class="sxs-lookup"><span data-stu-id="6c40c-129">FunctionTailcall3WithInfo Function</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="6c40c-130">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="6c40c-130">SetEnterLeaveFunctionHooks3</span></span>](icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="6c40c-131">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="6c40c-131">SetEnterLeaveFunctionHooks3WithInfo</span></span>](icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="6c40c-132">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="6c40c-132">SetFunctionIDMapper</span></span>](icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="6c40c-133">SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="6c40c-133">SetFunctionIDMapper2</span></span>](icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="6c40c-134">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="6c40c-134">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
