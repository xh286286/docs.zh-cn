---
title: ICorDebugThread::GetDebugState 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetDebugState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetDebugState
helpviewer_keywords:
- GetDebugState method [.NET Framework debugging]
- ICorDebugThread::GetDebugState method [.NET Framework debugging]
ms.assetid: 9be27b0c-1d99-4722-b0d4-40cf6753ce5c
topic_type:
- apiref
ms.openlocfilehash: 746fef3629e6573d7dfe47d5a3fcf9ee9a1d4250
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728038"
---
# <a name="icordebugthreadgetdebugstate-method"></a><span data-ttu-id="19bb8-102">ICorDebugThread::GetDebugState 方法</span><span class="sxs-lookup"><span data-stu-id="19bb8-102">ICorDebugThread::GetDebugState Method</span></span>

<span data-ttu-id="19bb8-103">获取此 ICorDebugThread 对象的当前调试状态。</span><span class="sxs-lookup"><span data-stu-id="19bb8-103">Gets the current debug state of this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19bb8-104">语法</span><span class="sxs-lookup"><span data-stu-id="19bb8-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDebugState (  
    [out] CorDebugThreadState   *pState  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="19bb8-105">参数</span><span class="sxs-lookup"><span data-stu-id="19bb8-105">Parameters</span></span>  

 `pState`  
 <span data-ttu-id="19bb8-106">弄一个指针，指向用于描述此线程当前调试状态的 CorDebugThreadState 枚举值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="19bb8-106">[out] A pointer to a bitwise combination of CorDebugThreadState enumeration values that describes the current debug state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="19bb8-107">注解</span><span class="sxs-lookup"><span data-stu-id="19bb8-107">Remarks</span></span>  

 <span data-ttu-id="19bb8-108">如果进程当前已停止，则 `pState` 表示此线程的调试状态（如果进程继续），而不是此线程的实际当前状态。</span><span class="sxs-lookup"><span data-stu-id="19bb8-108">If the process is currently stopped, `pState` represents the debug state that would exist for this thread if the process were to be continued, not the actual current state of this thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19bb8-109">要求</span><span class="sxs-lookup"><span data-stu-id="19bb8-109">Requirements</span></span>  

 <span data-ttu-id="19bb8-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="19bb8-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19bb8-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="19bb8-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="19bb8-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="19bb8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="19bb8-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19bb8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
