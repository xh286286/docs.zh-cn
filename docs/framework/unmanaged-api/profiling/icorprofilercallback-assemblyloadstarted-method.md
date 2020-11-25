---
title: ICorProfilerCallback::AssemblyLoadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadStarted method [.NET Framework profiling]
- AssemblyLoadStarted method [.NET Framework profiling]
ms.assetid: 67e8209d-a0ca-4118-a6e6-c1ee0abc2221
topic_type:
- apiref
ms.openlocfilehash: c2fbc0ae8cdeb79b65cbad9a055a8051acf67e50
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700413"
---
# <a name="icorprofilercallbackassemblyloadstarted-method"></a><span data-ttu-id="e49d8-102">ICorProfilerCallback::AssemblyLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="e49d8-102">ICorProfilerCallback::AssemblyLoadStarted Method</span></span>

<span data-ttu-id="e49d8-103">通知探查器正在加载程序集。</span><span class="sxs-lookup"><span data-stu-id="e49d8-103">Notifies the profiler that an assembly is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e49d8-104">语法</span><span class="sxs-lookup"><span data-stu-id="e49d8-104">Syntax</span></span>  
  
```cpp  
HRESULT AssemblyLoadStarted(  
    [in] AssemblyID assemblyId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e49d8-105">参数</span><span class="sxs-lookup"><span data-stu-id="e49d8-105">Parameters</span></span>

- `assemblyId`

  <span data-ttu-id="e49d8-106">\[in] 标识要加载的程序集。</span><span class="sxs-lookup"><span data-stu-id="e49d8-106">\[in] Identifies the assembly that is being loaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49d8-107">注解</span><span class="sxs-lookup"><span data-stu-id="e49d8-107">Remarks</span></span>  

 <span data-ttu-id="e49d8-108">在 `assemblyId` 调用 [ICorProfilerCallback：： AssemblyLoadFinished](icorprofilercallback-assemblyloadfinished-method.md) 方法之前，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="e49d8-108">The value of `assemblyId` is not valid for an information request until the [ICorProfilerCallback::AssemblyLoadFinished](icorprofilercallback-assemblyloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e49d8-109">要求</span><span class="sxs-lookup"><span data-stu-id="e49d8-109">Requirements</span></span>  

 <span data-ttu-id="e49d8-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e49d8-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e49d8-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e49d8-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e49d8-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e49d8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e49d8-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e49d8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e49d8-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e49d8-114">See also</span></span>

- [<span data-ttu-id="e49d8-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e49d8-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
