---
title: ICorDebugEval2::RudeAbort 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.RudeAbort
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::RudeAbort
helpviewer_keywords:
- ICorDebugEval2::RudeAbort method [.NET Framework debugging]
- RudeAbort method, ICorDebugEval2 interface [.NET Framework debugging]
ms.assetid: 02468edf-d32b-4cb3-aaa8-3dd2abfc8b25
topic_type:
- apiref
ms.openlocfilehash: 478772925dfb7ca7389b5267433f9b06ace3d5a3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729611"
---
# <a name="icordebugeval2rudeabort-method"></a><span data-ttu-id="c3e54-102">ICorDebugEval2::RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="c3e54-102">ICorDebugEval2::RudeAbort Method</span></span>

<span data-ttu-id="c3e54-103">中止此当前正在执行的计算 `ICorDebugEval2` 。</span><span class="sxs-lookup"><span data-stu-id="c3e54-103">Aborts the computation that this `ICorDebugEval2` is currently performing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3e54-104">语法</span><span class="sxs-lookup"><span data-stu-id="c3e54-104">Syntax</span></span>  
  
```cpp  
HRESULT RudeAbort ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="c3e54-105">备注</span><span class="sxs-lookup"><span data-stu-id="c3e54-105">Remarks</span></span>  

 <span data-ttu-id="c3e54-106">`RudeAbort` 不会释放该计算器持有的任何锁，因此会使调试会话处于不安全状态。</span><span class="sxs-lookup"><span data-stu-id="c3e54-106">`RudeAbort` does not release any locks that the evaluator holds, so it leaves the debugging session in an unsafe state.</span></span> <span data-ttu-id="c3e54-107">请特别小心调用此方法。</span><span class="sxs-lookup"><span data-stu-id="c3e54-107">Call this method with extreme caution.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3e54-108">要求</span><span class="sxs-lookup"><span data-stu-id="c3e54-108">Requirements</span></span>  

 <span data-ttu-id="c3e54-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c3e54-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3e54-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c3e54-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c3e54-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c3e54-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c3e54-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3e54-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
