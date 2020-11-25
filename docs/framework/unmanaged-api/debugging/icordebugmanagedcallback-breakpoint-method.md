---
title: ICorDebugManagedCallback::Breakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Breakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Breakpoint
helpviewer_keywords:
- ICorDebugManagedCallback::Breakpoint method [.NET Framework debugging]
- Breakpoint method [.NET Framework debugging]
ms.assetid: 60b279b0-a726-46d2-8c53-76986a007ebb
topic_type:
- apiref
ms.openlocfilehash: d7cf966f407572cc681f641b63791906a5c015f3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731860"
---
# <a name="icordebugmanagedcallbackbreakpoint-method"></a><span data-ttu-id="0b1b7-102">ICorDebugManagedCallback::Breakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="0b1b7-102">ICorDebugManagedCallback::Breakpoint Method</span></span>

<span data-ttu-id="0b1b7-103">遇到断点时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="0b1b7-103">Notifies the debugger when a breakpoint is encountered.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b1b7-104">语法</span><span class="sxs-lookup"><span data-stu-id="0b1b7-104">Syntax</span></span>  
  
```cpp  
HRESULT Breakpoint (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b1b7-105">参数</span><span class="sxs-lookup"><span data-stu-id="0b1b7-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="0b1b7-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含断点的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="0b1b7-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the breakpoint.</span></span>  
  
 `pThread`  
 <span data-ttu-id="0b1b7-107">中指向 ICorDebugThread 对象的指针，该对象表示包含断点的线程。</span><span class="sxs-lookup"><span data-stu-id="0b1b7-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the breakpoint.</span></span>  
  
 `pBreakpoint`  
 <span data-ttu-id="0b1b7-108">中指向表示断点的 ICorDebugBreakpoint 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="0b1b7-108">[in] A pointer to an ICorDebugBreakpoint object that represents the breakpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b1b7-109">要求</span><span class="sxs-lookup"><span data-stu-id="0b1b7-109">Requirements</span></span>  

 <span data-ttu-id="0b1b7-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0b1b7-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b1b7-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0b1b7-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0b1b7-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0b1b7-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0b1b7-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b1b7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b1b7-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b1b7-114">See also</span></span>

- [<span data-ttu-id="0b1b7-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="0b1b7-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
