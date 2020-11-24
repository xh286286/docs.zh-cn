---
title: ICorProfilerCallback::AppDomainCreationStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AppDomainCreationStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AppDomainCreationStarted
helpviewer_keywords:
- AppDomainCreationStarted method [.NET Framework profiling]
- ICorProfilerCallback::AppDomainCreationStarted method [.NET Framework profiling]
ms.assetid: b2a8240b-07fe-4859-bb2b-7d3adbfa0a9f
topic_type:
- apiref
ms.openlocfilehash: 901546c80c3bee32afddfa8e8cffbd2b679bc43b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95685378"
---
# <a name="icorprofilercallbackappdomaincreationstarted-method"></a><span data-ttu-id="bf1fb-102">ICorProfilerCallback::AppDomainCreationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="bf1fb-102">ICorProfilerCallback::AppDomainCreationStarted Method</span></span>

<span data-ttu-id="bf1fb-103">通知探查器正在创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="bf1fb-103">Notifies the profiler that an application domain is being created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf1fb-104">语法</span><span class="sxs-lookup"><span data-stu-id="bf1fb-104">Syntax</span></span>  
  
```cpp  
HRESULT AppDomainCreationStarted(  
    [in] AppDomainID appDomainId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bf1fb-105">参数</span><span class="sxs-lookup"><span data-stu-id="bf1fb-105">Parameters</span></span>

- `appDomainId`

  <span data-ttu-id="bf1fb-106">\[in] 标识正在创建的域。</span><span class="sxs-lookup"><span data-stu-id="bf1fb-106">\[in] Identifies the domain which is being created.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf1fb-107">注解</span><span class="sxs-lookup"><span data-stu-id="bf1fb-107">Remarks</span></span>  

 <span data-ttu-id="bf1fb-108">在调用 [ICorProfilerCallback：： AppDomainCreationFinished](icorprofilercallback-appdomaincreationfinished-method.md) 方法之前，ID 对任何信息请求都无效。</span><span class="sxs-lookup"><span data-stu-id="bf1fb-108">The ID is not valid for any information request until the [ICorProfilerCallback::AppDomainCreationFinished](icorprofilercallback-appdomaincreationfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf1fb-109">要求</span><span class="sxs-lookup"><span data-stu-id="bf1fb-109">Requirements</span></span>  

 <span data-ttu-id="bf1fb-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bf1fb-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf1fb-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="bf1fb-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="bf1fb-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bf1fb-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bf1fb-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bf1fb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf1fb-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf1fb-114">See also</span></span>

- [<span data-ttu-id="bf1fb-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="bf1fb-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
