---
title: ICorProfilerCallback::ThreadCreated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadCreated
helpviewer_keywords:
- ICorProfilerCallback::ThreadCreated method [.NET Framework profiling]
- ThreadCreated method [.NET Framework profiling]
ms.assetid: cca0f799-09b8-4689-a33c-6d6537943a9b
topic_type:
- apiref
ms.openlocfilehash: 72b074d1794a6039060cbd84aabb0bc0155c154e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717231"
---
# <a name="icorprofilercallbackthreadcreated-method"></a><span data-ttu-id="3628a-102">ICorProfilerCallback::ThreadCreated 方法</span><span class="sxs-lookup"><span data-stu-id="3628a-102">ICorProfilerCallback::ThreadCreated Method</span></span>

<span data-ttu-id="3628a-103">通知探查器已创建一个线程。</span><span class="sxs-lookup"><span data-stu-id="3628a-103">Notifies the profiler that a thread has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3628a-104">语法</span><span class="sxs-lookup"><span data-stu-id="3628a-104">Syntax</span></span>  
  
```cpp  
HRESULT ThreadCreated(  
    [in] ThreadID threadId);
```  
  
## <a name="parameters"></a><span data-ttu-id="3628a-105">参数</span><span class="sxs-lookup"><span data-stu-id="3628a-105">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="3628a-106">中已创建的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="3628a-106">[in] The ID of the thread that has been created.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3628a-107">注解</span><span class="sxs-lookup"><span data-stu-id="3628a-107">Remarks</span></span>  

 <span data-ttu-id="3628a-108">`threadId`值立即有效。</span><span class="sxs-lookup"><span data-stu-id="3628a-108">The `threadId` value is immediately valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3628a-109">要求</span><span class="sxs-lookup"><span data-stu-id="3628a-109">Requirements</span></span>  

 <span data-ttu-id="3628a-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3628a-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3628a-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3628a-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3628a-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3628a-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3628a-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3628a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3628a-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3628a-114">See also</span></span>

- [<span data-ttu-id="3628a-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="3628a-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="3628a-116">ThreadDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="3628a-116">ThreadDestroyed Method</span></span>](icorprofilercallback-threaddestroyed-method.md)
