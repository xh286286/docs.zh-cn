---
title: ICorProfilerCallback9 接口
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.openlocfilehash: 23b91a2a58c6e76b31b94e0fa3661dfbc8e18e33
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712763"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="840d6-102">ICorProfilerCallback9 接口</span><span class="sxs-lookup"><span data-stu-id="840d6-102">ICorProfilerCallback9 Interface</span></span>

<span data-ttu-id="840d6-103">[.NET Framework 4.7.2 和更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="840d6-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="840d6-104">提供回调方法的 [ICorProfilerCallback8](icorprofilercallback8-interface.md) 的子类，公共语言运行时使用该方法通知探查器动态方法已被垃圾回收并随后卸载。</span><span class="sxs-lookup"><span data-stu-id="840d6-104">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="840d6-105">方法</span><span class="sxs-lookup"><span data-stu-id="840d6-105">Methods</span></span>  
  
|<span data-ttu-id="840d6-106">方法</span><span class="sxs-lookup"><span data-stu-id="840d6-106">Method</span></span>|<span data-ttu-id="840d6-107">说明</span><span class="sxs-lookup"><span data-stu-id="840d6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="840d6-108">DynamicMethodUnloaded 方法</span><span class="sxs-lookup"><span data-stu-id="840d6-108">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="840d6-109">通知探查器已对动态方法进行了垃圾回收并随后将其卸载。</span><span class="sxs-lookup"><span data-stu-id="840d6-109">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="840d6-110">要求</span><span class="sxs-lookup"><span data-stu-id="840d6-110">Requirements</span></span>  

 <span data-ttu-id="840d6-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="840d6-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="840d6-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="840d6-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="840d6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="840d6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="840d6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="840d6-114">See also</span></span>

- [<span data-ttu-id="840d6-115">分析接口</span><span class="sxs-lookup"><span data-stu-id="840d6-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="840d6-116">ICorProfilerCallback8 接口</span><span class="sxs-lookup"><span data-stu-id="840d6-116">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="840d6-117">ICorProfilerCallback8. DynamicMethodJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="840d6-117">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="840d6-118">ICorProfilerCallback8. DynamicMethodJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="840d6-118">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
