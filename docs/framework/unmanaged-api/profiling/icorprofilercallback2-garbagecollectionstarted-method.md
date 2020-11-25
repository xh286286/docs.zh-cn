---
title: ICorProfilerCallback2::GarbageCollectionStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.GarbageCollectionStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::GarbageCollectionStarted
helpviewer_keywords:
- GarbageCollectionStarted method [.NET Framework profiling]
- ICorProfilerCallback2::GarbageCollectionStarted method [.NET Framework profiling]
ms.assetid: 44eef087-f21f-4fe2-b481-f8a0ee022e7d
topic_type:
- apiref
ms.openlocfilehash: 63a8d212a61bd73f44995f0e057eeff96f9a5554
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731938"
---
# <a name="icorprofilercallback2garbagecollectionstarted-method"></a><span data-ttu-id="dfaed-102">ICorProfilerCallback2::GarbageCollectionStarted 方法</span><span class="sxs-lookup"><span data-stu-id="dfaed-102">ICorProfilerCallback2::GarbageCollectionStarted Method</span></span>

<span data-ttu-id="dfaed-103">通知代码探查器垃圾回收已启动。</span><span class="sxs-lookup"><span data-stu-id="dfaed-103">Notifies the code profiler that garbage collection has started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfaed-104">语法</span><span class="sxs-lookup"><span data-stu-id="dfaed-104">Syntax</span></span>  
  
```cpp  
HRESULT GarbageCollectionStarted(  
    [in] int cGenerations,  
    [in, size_is(cGenerations), length_is(cGenerations)] BOOL generationCollected[],  
    [in] COR_PRF_GC_REASON reason);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfaed-105">参数</span><span class="sxs-lookup"><span data-stu-id="dfaed-105">Parameters</span></span>  

 `cGenerations`  
 <span data-ttu-id="dfaed-106">中数组中的总项数 `generationCollected` 。</span><span class="sxs-lookup"><span data-stu-id="dfaed-106">[in] The total number of entries in the `generationCollected` array.</span></span>  
  
 `generationCollected`  
 <span data-ttu-id="dfaed-107">中布尔值的数组， `true` 如果此垃圾回收正在收集与数组索引对应的生成，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="dfaed-107">[in] An array of Boolean values, which are `true` if the generation that corresponds to the array index is being collected by this garbage collection; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="dfaed-108">数组由 [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) 枚举的一个值进行索引，该枚举指示代。</span><span class="sxs-lookup"><span data-stu-id="dfaed-108">The array is indexed by a value of the [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) enumeration, which indicates the generation.</span></span>  
  
 `reason`  
 <span data-ttu-id="dfaed-109">中一个 [COR_PRF_GC_REASON](cor-prf-gc-reason-enumeration.md) 枚举的值，该值指示导致垃圾回收的原因。</span><span class="sxs-lookup"><span data-stu-id="dfaed-109">[in] A value of the [COR_PRF_GC_REASON](cor-prf-gc-reason-enumeration.md) enumeration that indicates the reason the garbage collection was induced.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dfaed-110">注解</span><span class="sxs-lookup"><span data-stu-id="dfaed-110">Remarks</span></span>  

 <span data-ttu-id="dfaed-111">与此垃圾回收相关的所有回调都将在 `GarbageCollectionStarted` 回调和相应的 [ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) 回调之间发生。</span><span class="sxs-lookup"><span data-stu-id="dfaed-111">All callbacks that pertain to this garbage collection will occur between the `GarbageCollectionStarted` callback and the corresponding [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) callback.</span></span> <span data-ttu-id="dfaed-112">这些回调不需要在同一线程上发生。</span><span class="sxs-lookup"><span data-stu-id="dfaed-112">These callbacks need not occur on the same thread.</span></span>  
  
 <span data-ttu-id="dfaed-113">探查器在回调过程中检查其原始位置的对象是安全的 `GarbageCollectionStarted` 。</span><span class="sxs-lookup"><span data-stu-id="dfaed-113">It is safe for the profiler to inspect objects in their original locations during the `GarbageCollectionStarted` callback.</span></span> <span data-ttu-id="dfaed-114">垃圾回收器将在返回后开始移动对象 `GarbageCollectionStarted` 。</span><span class="sxs-lookup"><span data-stu-id="dfaed-114">The garbage collector will begin moving objects after the return from `GarbageCollectionStarted`.</span></span> <span data-ttu-id="dfaed-115">在探查器从此回调返回后，探查器应在收到回调之前将所有对象 Id 视为无效 `ICorProfilerCallback2::GarbageCollectionFinished` 。</span><span class="sxs-lookup"><span data-stu-id="dfaed-115">After the profiler has returned from this callback, the profiler should consider all object IDs to be invalid until it receives a `ICorProfilerCallback2::GarbageCollectionFinished` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfaed-116">要求</span><span class="sxs-lookup"><span data-stu-id="dfaed-116">Requirements</span></span>  

 <span data-ttu-id="dfaed-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dfaed-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dfaed-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dfaed-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dfaed-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dfaed-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dfaed-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dfaed-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfaed-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfaed-121">See also</span></span>

- [<span data-ttu-id="dfaed-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="dfaed-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="dfaed-123">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="dfaed-123">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
