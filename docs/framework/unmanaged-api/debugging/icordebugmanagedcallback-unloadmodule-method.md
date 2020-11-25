---
title: ICorDebugManagedCallback::UnloadModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadModule
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadModule method [.NET Framework debugging]
- UnloadModule method [.NET Framework debugging]
ms.assetid: b12bfcd9-1e29-48bf-9a3d-44bfae5df5e8
topic_type:
- apiref
ms.openlocfilehash: f24d49189ee81a80397b94ee4113c9514c083dbc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723982"
---
# <a name="icordebugmanagedcallbackunloadmodule-method"></a><span data-ttu-id="8d157-102">ICorDebugManagedCallback::UnloadModule 方法</span><span class="sxs-lookup"><span data-stu-id="8d157-102">ICorDebugManagedCallback::UnloadModule Method</span></span>

<span data-ttu-id="8d157-103">通知调试器已卸载了公共语言运行时模块 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="8d157-103">Notifies the debugger that a common language runtime module (DLL) has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d157-104">语法</span><span class="sxs-lookup"><span data-stu-id="8d157-104">Syntax</span></span>  
  
```cpp  
HRESULT UnloadModule (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugModule     *pModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8d157-105">参数</span><span class="sxs-lookup"><span data-stu-id="8d157-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="8d157-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含模块的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="8d157-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the module.</span></span>  
  
 `pModule`  
 <span data-ttu-id="8d157-107">中指向表示模块的 ICorDebugModule 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="8d157-107">[in] A pointer to an ICorDebugModule object that represents the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d157-108">注解</span><span class="sxs-lookup"><span data-stu-id="8d157-108">Remarks</span></span>  

 <span data-ttu-id="8d157-109">此调用之后不应使用该模块。</span><span class="sxs-lookup"><span data-stu-id="8d157-109">The module should not be used after this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d157-110">要求</span><span class="sxs-lookup"><span data-stu-id="8d157-110">Requirements</span></span>  

 <span data-ttu-id="8d157-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d157-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d157-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8d157-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8d157-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d157-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8d157-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d157-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d157-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d157-115">See also</span></span>

- [<span data-ttu-id="8d157-116">LoadModule 方法</span><span class="sxs-lookup"><span data-stu-id="8d157-116">LoadModule Method</span></span>](icordebugmanagedcallback-loadmodule-method.md)
- [<span data-ttu-id="8d157-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="8d157-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
