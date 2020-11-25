---
title: ICorDebugManagedCallback::EvalComplete 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalComplete
helpviewer_keywords:
- ICorDebugManagedCallback::EvalComplete method [.NET Framework debugging]
- EvalComplete method [.NET Framework debugging]
ms.assetid: f74ab4eb-cd1b-407c-a66d-8ec0d85647f3
topic_type:
- apiref
ms.openlocfilehash: e95874447528989af68f5c97825691532195889f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731795"
---
# <a name="icordebugmanagedcallbackevalcomplete-method"></a><span data-ttu-id="193d2-102">ICorDebugManagedCallback::EvalComplete 方法</span><span class="sxs-lookup"><span data-stu-id="193d2-102">ICorDebugManagedCallback::EvalComplete Method</span></span>

<span data-ttu-id="193d2-103">通知调试器已完成计算。</span><span class="sxs-lookup"><span data-stu-id="193d2-103">Notifies the debugger that an evaluation has been completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="193d2-104">语法</span><span class="sxs-lookup"><span data-stu-id="193d2-104">Syntax</span></span>  
  
```cpp  
HRESULT EvalComplete (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="193d2-105">参数</span><span class="sxs-lookup"><span data-stu-id="193d2-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="193d2-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示在其中执行计算的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="193d2-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation was performed.</span></span>  
  
 `pThread`  
 <span data-ttu-id="193d2-107">中指向 ICorDebugThread 对象的指针，该对象表示在其中执行计算的线程。</span><span class="sxs-lookup"><span data-stu-id="193d2-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation was performed.</span></span>  
  
 `pEval`  
 <span data-ttu-id="193d2-108">中指向 ICorDebugEval 对象的指针，该对象表示执行计算的代码。</span><span class="sxs-lookup"><span data-stu-id="193d2-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="193d2-109">要求</span><span class="sxs-lookup"><span data-stu-id="193d2-109">Requirements</span></span>  

 <span data-ttu-id="193d2-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="193d2-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="193d2-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="193d2-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="193d2-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="193d2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="193d2-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="193d2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="193d2-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="193d2-114">See also</span></span>

- [<span data-ttu-id="193d2-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="193d2-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
