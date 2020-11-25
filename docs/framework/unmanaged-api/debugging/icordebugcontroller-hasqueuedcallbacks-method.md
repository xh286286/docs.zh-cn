---
title: ICorDebugController::HasQueuedCallbacks 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.HasQueuedCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::HasQueuedCallbacks
helpviewer_keywords:
- HasQueuedCallbacks method [.NET Framework debugging]
- ICorDebugController::HasQueuedCallbacks method [.NET Framework debugging]
ms.assetid: 0d6a1cd9-370b-4462-adbf-e3980e897ea7
topic_type:
- apiref
ms.openlocfilehash: bd623f8bee2feafebe80c0c7513bcfb33d6ad367
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707888"
---
# <a name="icordebugcontrollerhasqueuedcallbacks-method"></a><span data-ttu-id="66511-102">ICorDebugController::HasQueuedCallbacks 方法</span><span class="sxs-lookup"><span data-stu-id="66511-102">ICorDebugController::HasQueuedCallbacks Method</span></span>

<span data-ttu-id="66511-103">获取一个值，该值指示当前是否为指定线程排队任何托管回调。</span><span class="sxs-lookup"><span data-stu-id="66511-103">Gets a value that indicates whether any managed callbacks are currently queued for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66511-104">语法</span><span class="sxs-lookup"><span data-stu-id="66511-104">Syntax</span></span>  
  
```cpp  
HRESULT HasQueuedCallbacks (  
    [in] ICorDebugThread *pThread,  
    [out] BOOL           *pbQueued  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="66511-105">参数</span><span class="sxs-lookup"><span data-stu-id="66511-105">Parameters</span></span>  

 `pThread`  
 <span data-ttu-id="66511-106">中指向表示线程的 "ICorDebugThread" 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="66511-106">[in] A pointer to an "ICorDebugThread" object that represents the thread.</span></span>  
  
 `pbQueued`  
 <span data-ttu-id="66511-107">弄一个指向值的指针，该值为 `true` ; 如果当前为指定线程排队，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="66511-107">[out] A pointer to a value that is `true` if any managed callbacks are currently queued for the specified thread; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="66511-108">如果为该参数指定了 null `pThread` ，则 `HasQueuedCallbacks` 将返回， `true` 如果当前有托管的回调排队等候任何线程。</span><span class="sxs-lookup"><span data-stu-id="66511-108">If null is specified for the `pThread` parameter, `HasQueuedCallbacks` will return `true` if there are currently managed callbacks queued for any thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="66511-109">注解</span><span class="sxs-lookup"><span data-stu-id="66511-109">Remarks</span></span>  

 <span data-ttu-id="66511-110">每次都将调度一个回调，每次调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="66511-110">Callbacks will be dispatched one at a time, each time [ICorDebugController::Continue](icordebugcontroller-continue-method.md) is called.</span></span> <span data-ttu-id="66511-111">如果要报告同时发生的多个调试事件，则调试器可以检查此标志。</span><span class="sxs-lookup"><span data-stu-id="66511-111">The debugger can check this flag if it wants to report multiple debugging events that occur simultaneously.</span></span>  
  
 <span data-ttu-id="66511-112">调试事件排队后，它们已发生，因此调试器必须释放整个队列，才能确保调试对象的状态。</span><span class="sxs-lookup"><span data-stu-id="66511-112">When debugging events are queued, they have already occurred, so the debugger must drain the entire queue to be sure of the state of the debuggee.</span></span> <span data-ttu-id="66511-113">`ICorDebugController::Continue`用于排出队列的 (调用 ) 。例如，如果队列在线程 *x* 上包含两个调试事件，并且调试器在第一个调试事件之后挂起线程 *x* ，然后调用 `ICorDebugController::Continue` ，则线程 *x* 的第二个调试事件会在线程已挂起的情况下进行调度。</span><span class="sxs-lookup"><span data-stu-id="66511-113">(Call `ICorDebugController::Continue` to drain the queue.) For example, if the queue contains two debugging events on thread *X*, and the debugger suspends thread *X* after the first debugging event and then calls `ICorDebugController::Continue`, the second debugging event for thread *X* will be dispatched although the thread has been suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66511-114">要求</span><span class="sxs-lookup"><span data-stu-id="66511-114">Requirements</span></span>  

 <span data-ttu-id="66511-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="66511-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66511-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="66511-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66511-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="66511-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="66511-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66511-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66511-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66511-119">See also</span></span>
