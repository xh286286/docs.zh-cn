---
title: ICorDebugManagedCallback::UnloadAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadAssembly
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadAssembly method [.NET Framework debugging]
- UnloadAssembly method [.NET Framework debugging]
ms.assetid: 6734321c-c8a9-401f-a558-cad715ec4a77
topic_type:
- apiref
ms.openlocfilehash: e89b425afb63de8ef496fe545873ce33e5ff828c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724008"
---
# <a name="icordebugmanagedcallbackunloadassembly-method"></a><span data-ttu-id="be87a-102">ICorDebugManagedCallback::UnloadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="be87a-102">ICorDebugManagedCallback::UnloadAssembly Method</span></span>

<span data-ttu-id="be87a-103">通知调试器已卸载了公共语言运行时程序集。</span><span class="sxs-lookup"><span data-stu-id="be87a-103">Notifies the debugger that a common language runtime assembly has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be87a-104">语法</span><span class="sxs-lookup"><span data-stu-id="be87a-104">Syntax</span></span>  
  
```cpp  
HRESULT UnloadAssembly (  
    [in] IcorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugAssembly   *pAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be87a-105">参数</span><span class="sxs-lookup"><span data-stu-id="be87a-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="be87a-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含程序集的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="be87a-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the assembly.</span></span>  
  
 `pAssembly`  
 <span data-ttu-id="be87a-107">中指向表示程序集的 ICorDebugAssembly 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="be87a-107">[in] A pointer to an ICorDebugAssembly object that represents the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="be87a-108">注解</span><span class="sxs-lookup"><span data-stu-id="be87a-108">Remarks</span></span>  

 <span data-ttu-id="be87a-109">不应在此回调后使用该程序集。</span><span class="sxs-lookup"><span data-stu-id="be87a-109">The assembly should not be used after this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be87a-110">要求</span><span class="sxs-lookup"><span data-stu-id="be87a-110">Requirements</span></span>  

 <span data-ttu-id="be87a-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be87a-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be87a-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="be87a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="be87a-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be87a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be87a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be87a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be87a-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be87a-115">See also</span></span>

- [<span data-ttu-id="be87a-116">LoadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="be87a-116">LoadAssembly Method</span></span>](icordebugmanagedcallback-loadassembly-method.md)
- [<span data-ttu-id="be87a-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="be87a-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
