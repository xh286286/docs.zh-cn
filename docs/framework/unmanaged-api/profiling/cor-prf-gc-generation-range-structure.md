---
title: COR_PRF_GC_GENERATION_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_GENERATION_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_GENERATION_RANGE
helpviewer_keywords:
- COR_PRF_GC_GENERATION_RANGE structure [.NET Framework profiling]
ms.assetid: e7e07273-8d10-4a68-807e-59634e3f8c5e
topic_type:
- apiref
ms.openlocfilehash: a0ee2c9ce38272caef4960bfe5949c11083c12dd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674926"
---
# <a name="cor_prf_gc_generation_range-structure"></a><span data-ttu-id="4826b-102">COR_PRF_GC_GENERATION_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="4826b-102">COR_PRF_GC_GENERATION_RANGE Structure</span></span>

<span data-ttu-id="4826b-103">描述一个正进行垃圾回收的内存范围（即块）。</span><span class="sxs-lookup"><span data-stu-id="4826b-103">Describes a range (that is, block) of memory that is undergoing garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4826b-104">语法</span><span class="sxs-lookup"><span data-stu-id="4826b-104">Syntax</span></span>  
  
```cpp  
typedef struct COR_PRF_GC_GENERATION_RANGE {  
    COR_PRF_GC_GENERATION generation;  
    ObjectID rangeStart;  
    UINT_PTR rangeLength;  
    UINT_PTR rangeLengthReserved;  
} COR_PRF_GC_GENERATION_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="4826b-105">成员</span><span class="sxs-lookup"><span data-stu-id="4826b-105">Members</span></span>  
  
|<span data-ttu-id="4826b-106">成员</span><span class="sxs-lookup"><span data-stu-id="4826b-106">Member</span></span>|<span data-ttu-id="4826b-107">说明</span><span class="sxs-lookup"><span data-stu-id="4826b-107">Description</span></span>|  
|------------|-----------------|  
|`generation`|<span data-ttu-id="4826b-108">一个 [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) 枚举的值，该值指定内存块所属的代。</span><span class="sxs-lookup"><span data-stu-id="4826b-108">A value of the [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) enumeration that specifies the generation to which the block of memory belongs.</span></span>|  
|`rangeStart`|<span data-ttu-id="4826b-109">对象的 ID，该对象指定内存块的起始位置。</span><span class="sxs-lookup"><span data-stu-id="4826b-109">The ID of an object that specifies the starting location of the block of memory.</span></span>|  
|`rangeLength`|<span data-ttu-id="4826b-110">一个指向整数的指针，该整数指定内存块的已使用部分的大小， (即块中使用的内存量) 。</span><span class="sxs-lookup"><span data-stu-id="4826b-110">A pointer to an integer that specifies the size of the used portion of the memory block (that is, the amount of memory used within the block).</span></span>|  
|`rangeLengthReserved`|<span data-ttu-id="4826b-111">指向一个整数的指针，该整数指定内存块的大小 (即，为块) 预留的内存量。</span><span class="sxs-lookup"><span data-stu-id="4826b-111">A pointer to an integer that specifies the size of the memory block (that is, the amount of memory reserved for the block).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4826b-112">注解</span><span class="sxs-lookup"><span data-stu-id="4826b-112">Remarks</span></span>  

 <span data-ttu-id="4826b-113">`rangeLength`仅当[ICorProfilerInfo2：： GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md)或[ICorProfilerInfo2：： GetObjectGeneration](icorprofilerinfo2-getobjectgeneration-method.md)（这两个均使用该 `COR_PRF_GC_GENERATION_RANGE` 结构）从[ICorProfilerCallback2：： GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md)或[ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)方法调用时，此值才是准确的。</span><span class="sxs-lookup"><span data-stu-id="4826b-113">The `rangeLength` value is guaranteed to be accurate only if [ICorProfilerInfo2::GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md) or [ICorProfilerInfo2::GetObjectGeneration](icorprofilerinfo2-getobjectgeneration-method.md), both of which use the `COR_PRF_GC_GENERATION_RANGE` structure, is called from the [ICorProfilerCallback2::GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) or the [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4826b-114">要求</span><span class="sxs-lookup"><span data-stu-id="4826b-114">Requirements</span></span>  

 <span data-ttu-id="4826b-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4826b-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4826b-116">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="4826b-116">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="4826b-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4826b-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4826b-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4826b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4826b-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4826b-119">See also</span></span>

- [<span data-ttu-id="4826b-120">分析结构</span><span class="sxs-lookup"><span data-stu-id="4826b-120">Profiling Structures</span></span>](profiling-structures.md)
