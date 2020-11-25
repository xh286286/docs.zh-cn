---
title: ICorDebugProcess::ClearCurrentException 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ClearCurrentException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ClearCurrentException
helpviewer_keywords:
- ClearCurrentException method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::ClearCurrentException method [.NET Framework debugging]
ms.assetid: 9e02ee1a-e495-4578-bfb5-b946274bede7
topic_type:
- apiref
ms.openlocfilehash: 0d36390a905561b64b3ca6ca95722f82158450be
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95695213"
---
# <a name="icordebugprocessclearcurrentexception-method"></a><span data-ttu-id="163d0-102">ICorDebugProcess::ClearCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="163d0-102">ICorDebugProcess::ClearCurrentException Method</span></span>

<span data-ttu-id="163d0-103">清除给定线程上的当前非托管异常。</span><span class="sxs-lookup"><span data-stu-id="163d0-103">Clears the current unmanaged exception on the given thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="163d0-104">语法</span><span class="sxs-lookup"><span data-stu-id="163d0-104">Syntax</span></span>  
  
```cpp  
HRESULT ClearCurrentException([in] DWORD threadID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="163d0-105">参数</span><span class="sxs-lookup"><span data-stu-id="163d0-105">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="163d0-106">中将清除当前非托管异常的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="163d0-106">[in] The ID of the thread on which the current unmanaged exception will be cleared.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="163d0-107">注解</span><span class="sxs-lookup"><span data-stu-id="163d0-107">Remarks</span></span>  

 <span data-ttu-id="163d0-108">在线程报告了应被调试对象忽略的非托管异常之前，请在调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="163d0-108">Call this method before calling [ICorDebugController::Continue](icordebugcontroller-continue-method.md) when a thread has reported an unmanaged exception that should be ignored by the debuggee.</span></span> <span data-ttu-id="163d0-109">这会清除给定线程上未完成的带外 (IB) 和带外 (OOB) 事件。</span><span class="sxs-lookup"><span data-stu-id="163d0-109">This will clear both the outstanding in-band (IB) and out-of-band (OOB) events on the given thread.</span></span> <span data-ttu-id="163d0-110">自动清除所有 OOB 断点和单步例外。</span><span class="sxs-lookup"><span data-stu-id="163d0-110">All OOB breakpoints and single-step exceptions are automatically cleared.</span></span>  
  
 <span data-ttu-id="163d0-111">使用 [ICorDebugThread2：： InterceptCurrentException](icordebugthread2-interceptcurrentexception-method.md) 来截获线程上的当前托管异常。</span><span class="sxs-lookup"><span data-stu-id="163d0-111">Use [ICorDebugThread2::InterceptCurrentException](icordebugthread2-interceptcurrentexception-method.md) to intercept the current managed exception on a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="163d0-112">要求</span><span class="sxs-lookup"><span data-stu-id="163d0-112">Requirements</span></span>  

 <span data-ttu-id="163d0-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="163d0-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="163d0-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="163d0-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="163d0-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="163d0-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="163d0-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="163d0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
