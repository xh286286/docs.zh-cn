---
title: ICorProfilerCallback::RemotingServerInvocationStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationStarted
helpviewer_keywords:
- RemotingServerInvocationStarted method [.NET Framework profiling]
- ICorProfilerCallback::RemotingServerInvocationStarted method [.NET Framework profiling]
ms.assetid: 86051a11-ad8e-4ace-9a11-ff0f982a5e11
topic_type:
- apiref
ms.openlocfilehash: 630efefde2a90eca0b40643ea8d7ffe08efdc763
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95676824"
---
# <a name="icorprofilercallbackremotingserverinvocationstarted-method"></a><span data-ttu-id="b73b6-102">ICorProfilerCallback::RemotingServerInvocationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="b73b6-102">ICorProfilerCallback::RemotingServerInvocationStarted Method</span></span>

<span data-ttu-id="b73b6-103">通知探查器进程正在调用方法以响应远程方法调用请求。</span><span class="sxs-lookup"><span data-stu-id="b73b6-103">Notifies the profiler that the process is invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b73b6-104">语法</span><span class="sxs-lookup"><span data-stu-id="b73b6-104">Syntax</span></span>  
  
```cpp  
HRESULT RemotingServerInvocationStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="b73b6-105">要求</span><span class="sxs-lookup"><span data-stu-id="b73b6-105">Requirements</span></span>  

 <span data-ttu-id="b73b6-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b73b6-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b73b6-107">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b73b6-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b73b6-108">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b73b6-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b73b6-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b73b6-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b73b6-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b73b6-110">See also</span></span>

- [<span data-ttu-id="b73b6-111">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b73b6-111">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
