---
title: ICorDebugManagedCallback::CreateProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateProcess
helpviewer_keywords:
- ICorDebugManagedCallback::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: 8e89d5ee-e4e3-4738-8302-0b7d1cf4846e
topic_type:
- apiref
ms.openlocfilehash: cd24e672c65769586dc618c21503dbb344566974
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731808"
---
# <a name="icordebugmanagedcallbackcreateprocess-method"></a><span data-ttu-id="5d745-102">ICorDebugManagedCallback::CreateProcess 方法</span><span class="sxs-lookup"><span data-stu-id="5d745-102">ICorDebugManagedCallback::CreateProcess Method</span></span>

<span data-ttu-id="5d745-103">第一次附加或启动进程时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="5d745-103">Notifies the debugger when a process has been attached or started for the first time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d745-104">语法</span><span class="sxs-lookup"><span data-stu-id="5d745-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5d745-105">参数</span><span class="sxs-lookup"><span data-stu-id="5d745-105">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="5d745-106">中指向 ICorDebugProcess 对象的指针，该对象表示已附加或已启动的进程。</span><span class="sxs-lookup"><span data-stu-id="5d745-106">[in] A pointer to an ICorDebugProcess object that represents the process that has been attached or started.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5d745-107">注解</span><span class="sxs-lookup"><span data-stu-id="5d745-107">Remarks</span></span>  

 <span data-ttu-id="5d745-108">在公共语言运行时初始化之前，不会调用此方法。</span><span class="sxs-lookup"><span data-stu-id="5d745-108">This method is not called until the common language runtime is initialized.</span></span> <span data-ttu-id="5d745-109">大多数 [ICorDebug](icordebug-interface.md) 方法将在回调之前返回 CORDBG_E_NOTREADY `CreateProcess` 。</span><span class="sxs-lookup"><span data-stu-id="5d745-109">Most of the [ICorDebug](icordebug-interface.md) methods will return CORDBG_E_NOTREADY before the `CreateProcess` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d745-110">要求</span><span class="sxs-lookup"><span data-stu-id="5d745-110">Requirements</span></span>  

 <span data-ttu-id="5d745-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5d745-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d745-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5d745-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5d745-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5d745-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5d745-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d745-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d745-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d745-115">See also</span></span>

- [<span data-ttu-id="5d745-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5d745-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
