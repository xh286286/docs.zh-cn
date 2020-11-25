---
title: ICorProfilerCallback2::GarbageCollectionFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.GarbageCollectionFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::GarbageCollectionFinished
helpviewer_keywords:
- ICorProfilerCallback2::GarbageCollectionFinished method [.NET Framework profiling]
- GarbageCollectionFinished method [.NET Framework profiling]
ms.assetid: 1a5758ea-2354-43c0-92a3-32c9909d64e1
topic_type:
- apiref
ms.openlocfilehash: 84a71853ba2ccc8b95e4a8936005f2790d09a2c4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717301"
---
# <a name="icorprofilercallback2garbagecollectionfinished-method"></a><span data-ttu-id="014ed-102">ICorProfilerCallback2::GarbageCollectionFinished 方法</span><span class="sxs-lookup"><span data-stu-id="014ed-102">ICorProfilerCallback2::GarbageCollectionFinished Method</span></span>

<span data-ttu-id="014ed-103">通知探查器垃圾回收已完成，并为其发出了所有垃圾回收回调。</span><span class="sxs-lookup"><span data-stu-id="014ed-103">Notifies the profiler that garbage collection has completed and all garbage collection callbacks have been issued for it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="014ed-104">语法</span><span class="sxs-lookup"><span data-stu-id="014ed-104">Syntax</span></span>  
  
```cpp  
HRESULT GarbageCollectionFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="014ed-105">备注</span><span class="sxs-lookup"><span data-stu-id="014ed-105">Remarks</span></span>  

 <span data-ttu-id="014ed-106">调用方法时，探查器可以安全检查其最终位置中的对象 `GarbageCollectionFinished` 。</span><span class="sxs-lookup"><span data-stu-id="014ed-106">It is safe for the profiler to inspect objects in their final locations when the `GarbageCollectionFinished` method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="014ed-107">要求</span><span class="sxs-lookup"><span data-stu-id="014ed-107">Requirements</span></span>  

 <span data-ttu-id="014ed-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="014ed-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="014ed-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="014ed-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="014ed-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="014ed-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="014ed-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="014ed-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="014ed-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="014ed-112">See also</span></span>

- [<span data-ttu-id="014ed-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="014ed-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="014ed-114">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="014ed-114">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
