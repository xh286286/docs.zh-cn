---
title: ICorDebugModuleBreakpoint::GetModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint.GetModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint::GetModule
helpviewer_keywords:
- ICorDebugModuleBreakpoint::GetModule method [.NET Framework debugging]
- GetModule method, ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: ffd5d9ec-4564-4200-b625-b306eec0ebd7
topic_type:
- apiref
ms.openlocfilehash: b6363ef901d5297862ca46e685bb783aaaeb4123
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709591"
---
# <a name="icordebugmodulebreakpointgetmodule-method"></a><span data-ttu-id="4f401-102">ICorDebugModuleBreakpoint::GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="4f401-102">ICorDebugModuleBreakpoint::GetModule Method</span></span>

<span data-ttu-id="4f401-103">获取一个指向 "ICorDebugModule" 的接口指针，该指针引用设置此断点的模块。</span><span class="sxs-lookup"><span data-stu-id="4f401-103">Gets an interface pointer to an "ICorDebugModule" that references the module in which this breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f401-104">语法</span><span class="sxs-lookup"><span data-stu-id="4f401-104">Syntax</span></span>  
  
```cpp  
HRESULT GetModule (  
    [out] ICorDebugModule   **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4f401-105">参数</span><span class="sxs-lookup"><span data-stu-id="4f401-105">Parameters</span></span>  

 `ppModule`  
 <span data-ttu-id="4f401-106">弄指向接口的地址的指针 `ICorDebugModule` ，该接口引用在其中设置断点的模块。</span><span class="sxs-lookup"><span data-stu-id="4f401-106">[out] A pointer to the address of an `ICorDebugModule` interface that references the module in which the breakpoint is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f401-107">要求</span><span class="sxs-lookup"><span data-stu-id="4f401-107">Requirements</span></span>  

 <span data-ttu-id="4f401-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4f401-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4f401-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4f401-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4f401-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4f401-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4f401-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4f401-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f401-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f401-112">See also</span></span>
