---
title: ICorProfilerCallback::ModuleLoadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadFinished
helpviewer_keywords:
- ModuleLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadFinished method [.NET Framework profiling]
ms.assetid: 050649e5-ffc0-4458-a0a4-d9ee128a219e
topic_type:
- apiref
ms.openlocfilehash: 5a29507ca56cac4ab800845e3a88706dc7a25379
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683987"
---
# <a name="icorprofilercallbackmoduleloadfinished-method"></a><span data-ttu-id="f8818-102">ICorProfilerCallback::ModuleLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="f8818-102">ICorProfilerCallback::ModuleLoadFinished Method</span></span>

<span data-ttu-id="f8818-103">通知探查器模块已完成加载。</span><span class="sxs-lookup"><span data-stu-id="f8818-103">Notifies the profiler that a module has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8818-104">语法</span><span class="sxs-lookup"><span data-stu-id="f8818-104">Syntax</span></span>  
  
```cpp  
HRESULT ModuleLoadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f8818-105">参数</span><span class="sxs-lookup"><span data-stu-id="f8818-105">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="f8818-106">中已完成加载的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="f8818-106">[in] The ID of the module that has finished loading.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="f8818-107">中一个 HRESULT，指示是否已成功加载该模块。</span><span class="sxs-lookup"><span data-stu-id="f8818-107">[in] An HRESULT that indicates whether the module was loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8818-108">注解</span><span class="sxs-lookup"><span data-stu-id="f8818-108">Remarks</span></span>  

 <span data-ttu-id="f8818-109">在 `moduleId` 调用方法之前，的值对信息请求无效 `ModuleLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="f8818-109">The value of `moduleId` is not valid for an information request until the `ModuleLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="f8818-110">在回调后，加载模块的某些部分可能会继续 `ModuleLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="f8818-110">Some parts of loading the module might continue after the `ModuleLoadFinished` callback.</span></span> <span data-ttu-id="f8818-111">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="f8818-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="f8818-112">但是，中的成功 HRESULT `hrStatus` 仅指示加载模块的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="f8818-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8818-113">要求</span><span class="sxs-lookup"><span data-stu-id="f8818-113">Requirements</span></span>  

 <span data-ttu-id="f8818-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f8818-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8818-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f8818-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f8818-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f8818-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f8818-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8818-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8818-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8818-118">See also</span></span>

- [<span data-ttu-id="f8818-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="f8818-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="f8818-120">ModuleLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="f8818-120">ModuleLoadStarted Method</span></span>](icorprofilercallback-moduleloadstarted-method.md)
