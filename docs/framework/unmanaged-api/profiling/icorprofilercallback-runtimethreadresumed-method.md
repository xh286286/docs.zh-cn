---
title: ICorProfilerCallback::RuntimeThreadResumed 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeThreadResumed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadResumed
helpviewer_keywords:
- ICorProfilerCallback::RuntimeThreadResumed method [.NET Framework profiling]
- RuntimeThreadResumed method [.NET Framework profiling]
ms.assetid: da984f89-4f53-4ab0-ae6f-3e2ee6085994
topic_type:
- apiref
ms.openlocfilehash: 0996d7eb5b7354a67106ec7aa8818d5e4d46232e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717220"
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="50f90-102">ICorProfilerCallback::RuntimeThreadResumed 方法</span><span class="sxs-lookup"><span data-stu-id="50f90-102">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>

<span data-ttu-id="50f90-103">通知探查器指定的线程在挂起后已恢复。</span><span class="sxs-lookup"><span data-stu-id="50f90-103">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50f90-104">语法</span><span class="sxs-lookup"><span data-stu-id="50f90-104">Syntax</span></span>  
  
```cpp  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="50f90-105">参数</span><span class="sxs-lookup"><span data-stu-id="50f90-105">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="50f90-106">中已恢复的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="50f90-106">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50f90-107">要求</span><span class="sxs-lookup"><span data-stu-id="50f90-107">Requirements</span></span>  

 <span data-ttu-id="50f90-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="50f90-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50f90-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="50f90-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="50f90-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50f90-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="50f90-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50f90-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50f90-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50f90-112">See also</span></span>

- [<span data-ttu-id="50f90-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="50f90-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="50f90-114">RuntimeThreadSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="50f90-114">RuntimeThreadSuspended Method</span></span>](icorprofilercallback-runtimethreadsuspended-method.md)
