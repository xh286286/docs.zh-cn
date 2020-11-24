---
title: ICorDebugManagedCallback::ExitThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitThread
helpviewer_keywords:
- ExitThread method [.NET Framework debugging]
- ICorDebugManagedCallback::ExitThread method [.NET Framework debugging]
ms.assetid: 62db708b-6cf0-45c5-b897-4b5c75bd2505
topic_type:
- apiref
ms.openlocfilehash: 2ccb06b974cb17dff987ba42b647224cdc4c4ff2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688921"
---
# <a name="icordebugmanagedcallbackexitthread-method"></a><span data-ttu-id="fe90c-102">ICorDebugManagedCallback::ExitThread 方法</span><span class="sxs-lookup"><span data-stu-id="fe90c-102">ICorDebugManagedCallback::ExitThread Method</span></span>

<span data-ttu-id="fe90c-103">通知调试器已退出正在执行的托管代码的线程。</span><span class="sxs-lookup"><span data-stu-id="fe90c-103">Notifies the debugger that a thread that was executing managed code has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe90c-104">语法</span><span class="sxs-lookup"><span data-stu-id="fe90c-104">Syntax</span></span>  
  
```cpp  
HRESULT ExitThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fe90c-105">参数</span><span class="sxs-lookup"><span data-stu-id="fe90c-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="fe90c-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含托管线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="fe90c-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the managed thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="fe90c-107">中指向 ICorDebugThread 对象的指针，该对象表示托管线程。</span><span class="sxs-lookup"><span data-stu-id="fe90c-107">[in] A pointer to an ICorDebugThread object that represents the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe90c-108">注解</span><span class="sxs-lookup"><span data-stu-id="fe90c-108">Remarks</span></span>  

 <span data-ttu-id="fe90c-109">`ExitThread`引发回调后，线程将不再出现在线程枚举中。</span><span class="sxs-lookup"><span data-stu-id="fe90c-109">Once the `ExitThread` callback is fired, the thread will no longer appear in thread enumerations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe90c-110">要求</span><span class="sxs-lookup"><span data-stu-id="fe90c-110">Requirements</span></span>  

 <span data-ttu-id="fe90c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe90c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe90c-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fe90c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fe90c-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe90c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe90c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe90c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe90c-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe90c-115">See also</span></span>

- [<span data-ttu-id="fe90c-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="fe90c-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
