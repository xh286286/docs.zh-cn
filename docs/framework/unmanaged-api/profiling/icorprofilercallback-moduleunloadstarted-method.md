---
title: ICorProfilerCallback::ModuleUnloadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleUnloadStarted
helpviewer_keywords:
- ModuleUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleUnloadStarted method [.NET Framework profiling]
ms.assetid: 2debcaab-6005-4245-afdb-4268bb7e74bd
topic_type:
- apiref
ms.openlocfilehash: 12d5f7e073337af6034b8f313a2e0161620a65ea
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720948"
---
# <a name="icorprofilercallbackmoduleunloadstarted-method"></a><span data-ttu-id="9db0c-102">ICorProfilerCallback::ModuleUnloadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="9db0c-102">ICorProfilerCallback::ModuleUnloadStarted Method</span></span>

<span data-ttu-id="9db0c-103">通知探查器正在卸载模块。</span><span class="sxs-lookup"><span data-stu-id="9db0c-103">Notifies the profiler that a module is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9db0c-104">语法</span><span class="sxs-lookup"><span data-stu-id="9db0c-104">Syntax</span></span>  
  
```cpp  
HRESULT ModuleUnloadStarted(  
    [in] ModuleID moduleId);
```  
  
## <a name="parameters"></a><span data-ttu-id="9db0c-105">参数</span><span class="sxs-lookup"><span data-stu-id="9db0c-105">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="9db0c-106">中正在卸载的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="9db0c-106">[in] The ID of the module that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9db0c-107">注解</span><span class="sxs-lookup"><span data-stu-id="9db0c-107">Remarks</span></span>  

 <span data-ttu-id="9db0c-108">在 `moduleId` 方法返回后，的值对信息请求无效 `ModuleUnloadStarted` -这是探查器获取有关此模块的信息的最后机会。</span><span class="sxs-lookup"><span data-stu-id="9db0c-108">The value of `moduleId` is not valid for an information request after the `ModuleUnloadStarted` method returns — this is the profiler's last chance to get information about this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9db0c-109">要求</span><span class="sxs-lookup"><span data-stu-id="9db0c-109">Requirements</span></span>  

 <span data-ttu-id="9db0c-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9db0c-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9db0c-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9db0c-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9db0c-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9db0c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9db0c-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9db0c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9db0c-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9db0c-114">See also</span></span>

- [<span data-ttu-id="9db0c-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="9db0c-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="9db0c-116">ModuleUnloadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="9db0c-116">ModuleUnloadFinished Method</span></span>](icorprofilercallback-moduleunloadfinished-method.md)
