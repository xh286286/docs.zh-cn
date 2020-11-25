---
title: FunctionEnter 函数
ms.date: 03/30/2017
api_name:
- FunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionEnter
helpviewer_keywords:
- FunctionEnter function [.NET Framework profiling]
ms.assetid: bf4ffa50-4506-4dd4-aa13-a0457b47ca74
topic_type:
- apiref
ms.openlocfilehash: 9bc88d7dd5b00213da634dc9f511cfe0d39b42f1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729832"
---
# <a name="functionenter-function"></a><span data-ttu-id="c9cc0-102">FunctionEnter 函数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-102">FunctionEnter Function</span></span>

<span data-ttu-id="c9cc0-103">通知探查器控制正在传递到函数。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-103">Notifies the profiler that control is being passed to a function.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c9cc0-104">此 `FunctionEnter` 函数在 .NET Framework 版本2.0 中已弃用，其使用将导致性能下降。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-104">The `FunctionEnter` function is deprecated in the .NET Framework version 2.0, and its use will incur a performance penalty.</span></span> <span data-ttu-id="c9cc0-105">改为使用 [FunctionEnter2](functionenter2-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-105">Use the [FunctionEnter2](functionenter2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9cc0-106">语法</span><span class="sxs-lookup"><span data-stu-id="c9cc0-106">Syntax</span></span>  
  
```cpp  
void __stdcall FunctionEnter (  
    [in]  FunctionID funcID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9cc0-107">参数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-107">Parameters</span></span>

- `funcID`

  <span data-ttu-id="c9cc0-108">\[in] 控件传递到的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-108">\[in] The identifier of the function to which control is passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9cc0-109">注解</span><span class="sxs-lookup"><span data-stu-id="c9cc0-109">Remarks</span></span>  

 <span data-ttu-id="c9cc0-110">`FunctionEnter`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-110">The `FunctionEnter` function is a callback; you must implement it.</span></span> <span data-ttu-id="c9cc0-111">实现必须使用 `__declspec` `naked`) 存储类特性的 (。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-111">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="c9cc0-112">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-112">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="c9cc0-113">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="c9cc0-114">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="c9cc0-115">的实现 `FunctionEnter` 不应被阻止，因为它将延迟垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-115">The implementation of `FunctionEnter` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="c9cc0-116">实现不应尝试垃圾回收，因为堆栈可能不处于垃圾回收友好状态。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-116">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="c9cc0-117">如果尝试垃圾回收，则运行时将被阻止，直到 `FunctionEnter` 返回。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-117">If a garbage collection is attempted, the runtime will block until `FunctionEnter` returns.</span></span>  
  
 <span data-ttu-id="c9cc0-118">此外，该 `FunctionEnter` 函数不得调入托管代码或以任何方式导致托管的内存分配。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-118">Also, the `FunctionEnter` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9cc0-119">要求</span><span class="sxs-lookup"><span data-stu-id="c9cc0-119">Requirements</span></span>  

 <span data-ttu-id="c9cc0-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9cc0-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9cc0-121">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="c9cc0-121">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="c9cc0-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9cc0-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9cc0-123">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="c9cc0-123">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9cc0-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9cc0-124">See also</span></span>

- [<span data-ttu-id="c9cc0-125">FunctionEnter2 函数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-125">FunctionEnter2 Function</span></span>](functionenter2-function.md)
- [<span data-ttu-id="c9cc0-126">FunctionLeave2 函数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-126">FunctionLeave2 Function</span></span>](functionleave2-function.md)
- [<span data-ttu-id="c9cc0-127">FunctionTailcall2 函数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-127">FunctionTailcall2 Function</span></span>](functiontailcall2-function.md)
- [<span data-ttu-id="c9cc0-128">SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="c9cc0-128">SetEnterLeaveFunctionHooks2 Method</span></span>](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [<span data-ttu-id="c9cc0-129">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="c9cc0-129">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
