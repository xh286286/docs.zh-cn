---
title: ICorProfilerCallback5 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback5
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback5
helpviewer_keywords:
- ICorProfilerCallback5 interface [.NET Framework profiling]
ms.assetid: 61d2e9ef-5f1f-4771-8847-239616e35d84
topic_type:
- apiref
ms.openlocfilehash: 8e94aebc489fff1c81593e54b17c471e7228d810
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689285"
---
# <a name="icorprofilercallback5-interface"></a><span data-ttu-id="2a6aa-102">ICorProfilerCallback5 接口</span><span class="sxs-lookup"><span data-stu-id="2a6aa-102">ICorProfilerCallback5 Interface</span></span>

<span data-ttu-id="2a6aa-103">当与 [ICorProfilerCallback：： RootReferences](icorprofilercallback-rootreferences-method.md) 或 [ICorProfilerCallback2：： RootReferences2](icorprofilercallback2-rootreferences2-method.md) 方法一起使用来帮助探查器识别完整的实时对象闭包和 [ICorProfilerCallback：： ObjectReferences](icorprofilercallback-objectreferences-method.md) 和 [ConditionalWeakTableElementReferences](icorprofilercallback5-conditionalweaktableelementreferences-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2a6aa-103">Supplements information to help a profiler identify the full closure of live objects, when used with either the [ICorProfilerCallback::RootReferences](icorprofilercallback-rootreferences-method.md) or [ICorProfilerCallback2::RootReferences2](icorprofilercallback2-rootreferences2-method.md) method together with the [ICorProfilerCallback::ObjectReferences](icorprofilercallback-objectreferences-method.md) and [ConditionalWeakTableElementReferences](icorprofilercallback5-conditionalweaktableelementreferences-method.md) methods.</span></span>  
  
 <span data-ttu-id="2a6aa-104">`ICorProfilerCallback5` 必须由托管的内存探查器实现，才能订阅与依赖句柄相关的通知。</span><span class="sxs-lookup"><span data-stu-id="2a6aa-104">`ICorProfilerCallback5` must be implemented by a managed memory profiler to subscribe to notifications related to dependent handles.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a6aa-105">注解</span><span class="sxs-lookup"><span data-stu-id="2a6aa-105">Remarks</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2a6aa-106">方法</span><span class="sxs-lookup"><span data-stu-id="2a6aa-106">Methods</span></span>  
  
|<span data-ttu-id="2a6aa-107">方法</span><span class="sxs-lookup"><span data-stu-id="2a6aa-107">Method</span></span>|<span data-ttu-id="2a6aa-108">说明</span><span class="sxs-lookup"><span data-stu-id="2a6aa-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2a6aa-109">ConditionalWeakTableElementReferences 方法</span><span class="sxs-lookup"><span data-stu-id="2a6aa-109">ConditionalWeakTableElementReferences Method</span></span>](icorprofilercallback5-conditionalweaktableelementreferences-method.md)|<span data-ttu-id="2a6aa-110">标识这些根通过直接成员字段引用和 `ConditionalWeakTable` 依赖关系引用的对象的传递闭包。</span><span class="sxs-lookup"><span data-stu-id="2a6aa-110">Identifies the transitive closure of objects referenced by those roots through both direct member field references and through `ConditionalWeakTable` dependencies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2a6aa-111">要求</span><span class="sxs-lookup"><span data-stu-id="2a6aa-111">Requirements</span></span>  

 <span data-ttu-id="2a6aa-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2a6aa-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a6aa-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2a6aa-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2a6aa-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a6aa-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a6aa-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a6aa-115">See also</span></span>

- [<span data-ttu-id="2a6aa-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="2a6aa-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="2a6aa-117">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="2a6aa-117">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
