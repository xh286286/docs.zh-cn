---
title: ICorDebugValueBreakpoint::GetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugValueBreakpoint interface [.NET Framework debugging]
- ICorDebugValueBreakpoint::GetValue method [.NET Framework debugging]
ms.assetid: 52a73654-bc47-48b6-b2b1-a4456b10140c
topic_type:
- apiref
ms.openlocfilehash: 8b0ab22d4a782bb21e09d29c9121ef83782a4571
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722318"
---
# <a name="icordebugvaluebreakpointgetvalue-method"></a><span data-ttu-id="3416d-102">ICorDebugValueBreakpoint::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="3416d-102">ICorDebugValueBreakpoint::GetValue Method</span></span>

<span data-ttu-id="3416d-103">获取一个指向 "ICorDebugValue" 对象的接口指针，该对象表示在其上设置断点的对象的值。</span><span class="sxs-lookup"><span data-stu-id="3416d-103">Gets an interface pointer to an "ICorDebugValue" object that represents the value of the object on which the breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3416d-104">语法</span><span class="sxs-lookup"><span data-stu-id="3416d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetValue (  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3416d-105">参数</span><span class="sxs-lookup"><span data-stu-id="3416d-105">Parameters</span></span>  

 `ppValue`  
 <span data-ttu-id="3416d-106">弄指向对象地址的指针 `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="3416d-106">[out] A pointer to the address of an `ICorDebugValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3416d-107">要求</span><span class="sxs-lookup"><span data-stu-id="3416d-107">Requirements</span></span>  

 <span data-ttu-id="3416d-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3416d-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3416d-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3416d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3416d-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3416d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3416d-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3416d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3416d-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3416d-112">See also</span></span>
