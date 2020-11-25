---
title: ICorProfilerCallback::AssemblyUnloadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyUnloadFinished
helpviewer_keywords:
- AssemblyUnloadFinished method [.NET Framework profiling]
- ICorProfilerCallback::AssemblyUnloadFinished method [.NET Framework profiling]
ms.assetid: 53fca564-84b1-44d4-9e21-17a492d2aae7
topic_type:
- apiref
ms.openlocfilehash: 3f2b4a64b3f17b043f193e054c56601d706a10e1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700367"
---
# <a name="icorprofilercallbackassemblyunloadfinished-method"></a><span data-ttu-id="61a8f-102">ICorProfilerCallback::AssemblyUnloadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="61a8f-102">ICorProfilerCallback::AssemblyUnloadFinished Method</span></span>

<span data-ttu-id="61a8f-103">通知探查器已卸载程序集。</span><span class="sxs-lookup"><span data-stu-id="61a8f-103">Notifies the profiler that an assembly has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61a8f-104">语法</span><span class="sxs-lookup"><span data-stu-id="61a8f-104">Syntax</span></span>  
  
```cpp  
HRESULT AssemblyUnloadFinished(  
    [in] AssemblyID assemblyId,  
    [in] HRESULT    hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61a8f-105">参数</span><span class="sxs-lookup"><span data-stu-id="61a8f-105">Parameters</span></span>

- `assemblyId`

  <span data-ttu-id="61a8f-106">\[in] 标识正在卸载的程序集。</span><span class="sxs-lookup"><span data-stu-id="61a8f-106">\[in] Identifies the assembly that is being unloaded.</span></span>

- `hrStatus`

  <span data-ttu-id="61a8f-107">\[in] 一个 HRESULT，指示程序集是否已成功卸载。</span><span class="sxs-lookup"><span data-stu-id="61a8f-107">\[in] An HRESULT that indicates whether the assembly was unloaded successfully.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a8f-108">注解</span><span class="sxs-lookup"><span data-stu-id="61a8f-108">Remarks</span></span>  

 <span data-ttu-id="61a8f-109">在 `assemblyId` [ICorProfilerCallback：： AssemblyUnloadStarted](icorprofilercallback-assemblyunloadstarted-method.md) 方法返回后，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="61a8f-109">The value of `assemblyId` is not valid for an information request after the [ICorProfilerCallback::AssemblyUnloadStarted](icorprofilercallback-assemblyunloadstarted-method.md) method returns.</span></span>  
  
 <span data-ttu-id="61a8f-110">在回调后，卸载程序集的某些部分可能会继续 `AssemblyUnloadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="61a8f-110">Some parts of unloading the assembly might continue after the `AssemblyUnloadFinished` callback.</span></span> <span data-ttu-id="61a8f-111">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="61a8f-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="61a8f-112">但是，中的成功 HRESULT `hrStatus` 仅指示卸载程序集的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="61a8f-112">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the assembly has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61a8f-113">要求</span><span class="sxs-lookup"><span data-stu-id="61a8f-113">Requirements</span></span>  

 <span data-ttu-id="61a8f-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61a8f-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61a8f-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="61a8f-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="61a8f-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="61a8f-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="61a8f-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61a8f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61a8f-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61a8f-118">See also</span></span>

- [<span data-ttu-id="61a8f-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="61a8f-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
