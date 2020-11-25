---
title: ICorProfilerInfo2::GetObjectGeneration 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetObjectGeneration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetObjectGeneration
helpviewer_keywords:
- GetObjectGeneration method [.NET Framework profiling]
- ICorProfilerInfo2::GetObjectGeneration method [.NET Framework profiling]
ms.assetid: b0d25f76-0bd5-4aa6-96cf-bfec0e1de28b
topic_type:
- apiref
ms.openlocfilehash: 4ba404692bef84c0522a799c61f07eac341eaab4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95703838"
---
# <a name="icorprofilerinfo2getobjectgeneration-method"></a><span data-ttu-id="2a63e-102">ICorProfilerInfo2::GetObjectGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="2a63e-102">ICorProfilerInfo2::GetObjectGeneration Method</span></span>

<span data-ttu-id="2a63e-103">获取包含指定对象的堆段。</span><span class="sxs-lookup"><span data-stu-id="2a63e-103">Gets the segment of the heap that contains the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a63e-104">语法</span><span class="sxs-lookup"><span data-stu-id="2a63e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectGeneration(  
    [in] ObjectID objectId,  
    [out] COR_PRF_GC_GENERATION_RANGE *range);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2a63e-105">参数</span><span class="sxs-lookup"><span data-stu-id="2a63e-105">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="2a63e-106">中对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="2a63e-106">[in] The ID of the object.</span></span>  
  
 `range`  
 <span data-ttu-id="2a63e-107">弄指向 [COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md) 结构的指针，该结构描述一个范围 (即，生成中正在进行垃圾回收的内存块) 。</span><span class="sxs-lookup"><span data-stu-id="2a63e-107">[out] A pointer to a [COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md) structure, which describes a range (that is, a block) of memory within the generation that is undergoing garbage collection.</span></span> <span data-ttu-id="2a63e-108">此范围包含指定的对象。</span><span class="sxs-lookup"><span data-stu-id="2a63e-108">This range contains the specified object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a63e-109">注解</span><span class="sxs-lookup"><span data-stu-id="2a63e-109">Remarks</span></span>  

 <span data-ttu-id="2a63e-110">`GetObjectGeneration`如果垃圾回收未进行，则可以从任何探查器回调调用方法。</span><span class="sxs-lookup"><span data-stu-id="2a63e-110">The `GetObjectGeneration` method may be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="2a63e-111">也就是说，它可从任何回调调用， [ICorProfilerCallback2：： GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) 和 [ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)之间发生的回调除外。</span><span class="sxs-lookup"><span data-stu-id="2a63e-111">That is, it may be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a63e-112">要求</span><span class="sxs-lookup"><span data-stu-id="2a63e-112">Requirements</span></span>  

 <span data-ttu-id="2a63e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2a63e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a63e-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2a63e-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2a63e-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a63e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a63e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a63e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a63e-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a63e-117">See also</span></span>

- [<span data-ttu-id="2a63e-118">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2a63e-118">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="2a63e-119">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="2a63e-119">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
