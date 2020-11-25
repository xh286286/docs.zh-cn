---
title: ICorDebugManagedCallback::CreateThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateThread method
helpviewer_keywords:
- ICorDebugManagedCallback::CreateThread method [.NET Framework debugging]
- CreateThread method [.NET Framework debugging]
ms.assetid: 6b961728-21c4-4e8d-ae81-197458be62f4
topic_type:
- apiref
ms.openlocfilehash: 56ec7c56b167c29c9951638c5eee159e1d3c7ffb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721291"
---
# <a name="icordebugmanagedcallbackcreatethread-method"></a><span data-ttu-id="57a36-102">ICorDebugManagedCallback::CreateThread 方法</span><span class="sxs-lookup"><span data-stu-id="57a36-102">ICorDebugManagedCallback::CreateThread Method</span></span>

<span data-ttu-id="57a36-103">通知调试器线程已开始执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="57a36-103">Notifies the debugger that a thread has started executing managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57a36-104">语法</span><span class="sxs-lookup"><span data-stu-id="57a36-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57a36-105">参数</span><span class="sxs-lookup"><span data-stu-id="57a36-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="57a36-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="57a36-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="57a36-107">中指向表示线程的 ICorDebugThread 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="57a36-107">[in] A pointer to an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="57a36-108">注解</span><span class="sxs-lookup"><span data-stu-id="57a36-108">Remarks</span></span>  

 <span data-ttu-id="57a36-109">线程将定位在要执行的第一个托管代码指令上。</span><span class="sxs-lookup"><span data-stu-id="57a36-109">The thread will be positioned at the first managed code instruction to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57a36-110">要求</span><span class="sxs-lookup"><span data-stu-id="57a36-110">Requirements</span></span>  

 <span data-ttu-id="57a36-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="57a36-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57a36-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="57a36-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57a36-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57a36-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57a36-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57a36-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57a36-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57a36-115">See also</span></span>

- [<span data-ttu-id="57a36-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="57a36-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
