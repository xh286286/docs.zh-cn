---
title: ICorProfilerCallback9：:D ynamicMethodUnloaded 方法
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9.DynamicMethodUnloaded
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.openlocfilehash: 0e6fe3430696c16405d4ae414436bb12882c08a5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732342"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="4f988-102">ICorProfilerCallback9：:D ynamicMethodUnloaded 方法</span><span class="sxs-lookup"><span data-stu-id="4f988-102">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>

<span data-ttu-id="4f988-103">[.NET Framework 4.7.2 和更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="4f988-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="4f988-104">每当对动态方法进行垃圾回收并随后卸载时，通知探查器。</span><span class="sxs-lookup"><span data-stu-id="4f988-104">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f988-105">语法</span><span class="sxs-lookup"><span data-stu-id="4f988-105">Syntax</span></span>  
  
```cpp  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4f988-106">参数</span><span class="sxs-lookup"><span data-stu-id="4f988-106">Parameters</span></span>  

<span data-ttu-id="4f988-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="4f988-107">[in] `functionId`</span></span>  
<span data-ttu-id="4f988-108">已被垃圾回收和卸载的内存中函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="4f988-108">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f988-109">要求</span><span class="sxs-lookup"><span data-stu-id="4f988-109">Requirements</span></span>  

 <span data-ttu-id="4f988-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4f988-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4f988-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4f988-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4f988-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4f988-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4f988-113">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4f988-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f988-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f988-114">See also</span></span>

- [<span data-ttu-id="4f988-115">ICorProfilerCallback8. DynamicMethodJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="4f988-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="4f988-116">ICorProfilerCallback8. DynamicMethodJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="4f988-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [<span data-ttu-id="4f988-117">ICorProfilerCallback9 接口</span><span class="sxs-lookup"><span data-stu-id="4f988-117">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="4f988-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="4f988-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
