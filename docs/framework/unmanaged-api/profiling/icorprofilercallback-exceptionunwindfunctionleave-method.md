---
title: ICorProfilerCallback::ExceptionUnwindFunctionLeave 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionUnwindFunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionLeave
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionLeave method [.NET Framework profiling]
- ExceptionUnwindFunctionLeave method [.NET Framework profiling]
ms.assetid: ebaad1d5-ee0a-4cb0-96bc-8ba5d371b747
topic_type:
- apiref
ms.openlocfilehash: 9f88a3fde7d7cb5941e3a7f44a7d94056a959ab8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733914"
---
# <a name="icorprofilercallbackexceptionunwindfunctionleave-method"></a><span data-ttu-id="7186e-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave 方法</span><span class="sxs-lookup"><span data-stu-id="7186e-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave Method</span></span>

<span data-ttu-id="7186e-103">通知探查器异常处理的展开阶段已完成展开某个函数。</span><span class="sxs-lookup"><span data-stu-id="7186e-103">Notifies the profiler that the unwind phase of exception handling has finished unwinding a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7186e-104">语法</span><span class="sxs-lookup"><span data-stu-id="7186e-104">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionUnwindFunctionLeave();  
```  
  
## <a name="remarks"></a><span data-ttu-id="7186e-105">备注</span><span class="sxs-lookup"><span data-stu-id="7186e-105">Remarks</span></span>  

 <span data-ttu-id="7186e-106">`ExceptionUnwindFunctionLeave`调用方法时，将从堆栈中移除函数实例及其堆栈数据。</span><span class="sxs-lookup"><span data-stu-id="7186e-106">When the `ExceptionUnwindFunctionLeave` method is called, the function instance and its stack data are removed from the stack.</span></span>  
  
 <span data-ttu-id="7186e-107">探查器不应在此调用期间被阻止，因为堆栈可能不处于允许垃圾回收的状态，因此无法启用抢先垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="7186e-107">The profiler should not block during this call because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="7186e-108">如果探查器在此处阻止并且试图进行垃圾回收，则运行时将被阻止，直到此回调返回。</span><span class="sxs-lookup"><span data-stu-id="7186e-108">If the profiler blocks here and a garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="7186e-109">此外，在此调用期间，探查器不得调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="7186e-109">Also, during this call, the profiler must not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7186e-110">要求</span><span class="sxs-lookup"><span data-stu-id="7186e-110">Requirements</span></span>  

 <span data-ttu-id="7186e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7186e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7186e-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7186e-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7186e-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7186e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7186e-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7186e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7186e-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7186e-115">See also</span></span>

- [<span data-ttu-id="7186e-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7186e-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="7186e-117">ExceptionUnwindFunctionEnter 方法</span><span class="sxs-lookup"><span data-stu-id="7186e-117">ExceptionUnwindFunctionEnter Method</span></span>](icorprofilercallback-exceptionunwindfunctionenter-method.md)
