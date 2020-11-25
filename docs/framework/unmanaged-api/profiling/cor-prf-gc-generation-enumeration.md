---
title: COR_PRF_GC_GENERATION 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_GENERATION
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_GENERATION
helpviewer_keywords:
- COR_GC_GENERATION_FLAGS enumeration [.NET Framework profiling]
ms.assetid: d6ece160-26ad-4d39-abd7-05acd6f78c48
topic_type:
- apiref
ms.openlocfilehash: 1d7489e997868a9486f77d176580cee18213a99d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95718536"
---
# <a name="cor_prf_gc_generation-enumeration"></a><span data-ttu-id="42599-102">COR_PRF_GC_GENERATION 枚举</span><span class="sxs-lookup"><span data-stu-id="42599-102">COR_PRF_GC_GENERATION Enumeration</span></span>

<span data-ttu-id="42599-103">标识垃圾回收生成。</span><span class="sxs-lookup"><span data-stu-id="42599-103">Identifies a garbage-collection generation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42599-104">语法</span><span class="sxs-lookup"><span data-stu-id="42599-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_GC_GEN_0 = 0,  
    COR_PRF_GC_GEN_1 = 1,  
    COR_PRF_GC_GEN_2 = 2,  
    COR_PRF_GC_LARGE_OBJECT_HEAP = 3,
    COR_PRF_GC_PINNED_OBJECT_HEAP= 4
} COR_PRF_GC_GENERATION;  
```  
  
## <a name="members"></a><span data-ttu-id="42599-105">成员</span><span class="sxs-lookup"><span data-stu-id="42599-105">Members</span></span>  
  
|<span data-ttu-id="42599-106">成员</span><span class="sxs-lookup"><span data-stu-id="42599-106">Member</span></span>|<span data-ttu-id="42599-107">说明</span><span class="sxs-lookup"><span data-stu-id="42599-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_GEN_0`|<span data-ttu-id="42599-108">对象存储为第0代。</span><span class="sxs-lookup"><span data-stu-id="42599-108">The object is stored as generation 0.</span></span>|  
|`COR_PRF_GC_GEN_1`|<span data-ttu-id="42599-109">对象存储为第1代。</span><span class="sxs-lookup"><span data-stu-id="42599-109">The object is stored as generation 1.</span></span>|  
|`COR_PRF_GC_GEN_2`|<span data-ttu-id="42599-110">对象存储为第2代。</span><span class="sxs-lookup"><span data-stu-id="42599-110">The object is stored as generation 2.</span></span>|  
|`COR_PRF_GC_LARGE_OBJECT_HEAP`|<span data-ttu-id="42599-111">对象存储在大型对象堆中。</span><span class="sxs-lookup"><span data-stu-id="42599-111">The object is stored in the large-object heap.</span></span>|  
|`COR_PRF_GC_PINNED_OBJECT_HEAP`|<span data-ttu-id="42599-112">对象存储在固定对象堆中。</span><span class="sxs-lookup"><span data-stu-id="42599-112">The object is stored in the pinned-object heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="42599-113">注解</span><span class="sxs-lookup"><span data-stu-id="42599-113">Remarks</span></span>  

 <span data-ttu-id="42599-114">垃圾回收器通过将对象划分为基于年龄的代来改善内存管理性能。</span><span class="sxs-lookup"><span data-stu-id="42599-114">The garbage collector improves memory management performance by dividing objects into generations based on age.</span></span> <span data-ttu-id="42599-115">垃圾回收器当前使用三个代，编号为0、1和2，以及两个特殊堆段，一个用于大型对象，一个用于固定的对象。</span><span class="sxs-lookup"><span data-stu-id="42599-115">The garbage collector currently uses three generations, numbered 0, 1, and 2, and two special heap segments, one for large objects and one for pinned objects.</span></span>
  
 <span data-ttu-id="42599-116">大小大于阈值的对象存储在大对象堆中。</span><span class="sxs-lookup"><span data-stu-id="42599-116">Objects whose size is larger than a threshold value are stored in the large-object heap.</span></span> <span data-ttu-id="42599-117">固定的对象可以分配给固定对象堆，以避免在正常堆上分配这些对象的性能成本。</span><span class="sxs-lookup"><span data-stu-id="42599-117">Pinned objects can be allocated to the pinned-object heap to avoid the performance cost of allocating them on the normal heaps.</span></span> <span data-ttu-id="42599-118">其他已分配对象开始属于0代。</span><span class="sxs-lookup"><span data-stu-id="42599-118">Other allocated objects start out belonging to generation 0.</span></span> <span data-ttu-id="42599-119">发生垃圾回收后存在的所有对象都将升级到第1代。</span><span class="sxs-lookup"><span data-stu-id="42599-119">All objects that exist after garbage collection occurs in generation 0 are promoted to generation 1.</span></span> <span data-ttu-id="42599-120">在第1代中发生垃圾回收后存在的对象将移入第2代。</span><span class="sxs-lookup"><span data-stu-id="42599-120">Objects that exist after garbage collection occurs in generation 1 move into generation 2.</span></span>  
  
 <span data-ttu-id="42599-121">代的使用意味着垃圾回收器在任一时间只需要处理已分配对象的子集。</span><span class="sxs-lookup"><span data-stu-id="42599-121">The use of generations means that the garbage collector has to work with only a subset of the allocated objects at any one time.</span></span>  
  
 <span data-ttu-id="42599-122">`COR_PRF_GC_GENERATION`枚举由[COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md)结构使用。</span><span class="sxs-lookup"><span data-stu-id="42599-122">The `COR_PRF_GC_GENERATION` enumeration is used by the [COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42599-123">要求</span><span class="sxs-lookup"><span data-stu-id="42599-123">Requirements</span></span>  

 <span data-ttu-id="42599-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42599-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42599-125">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="42599-125">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="42599-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="42599-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="42599-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42599-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42599-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42599-128">See also</span></span>

- [<span data-ttu-id="42599-129">分析枚举</span><span class="sxs-lookup"><span data-stu-id="42599-129">Profiling Enumerations</span></span>](profiling-enumerations.md)
