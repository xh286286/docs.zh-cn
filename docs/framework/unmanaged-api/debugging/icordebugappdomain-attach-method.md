---
title: ICorDebugAppDomain::Attach 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.Attach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::Attach
helpviewer_keywords:
- ICorDebugAppDomain::Attach method [.NET Framework debugging]
- Attach method [.NET Framework debugging]
ms.assetid: 0358b84a-4236-4c34-945b-4babff7df570
topic_type:
- apiref
ms.openlocfilehash: d133cacb611a1c7bd03d7653f46c2e5fb1acc043
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723345"
---
# <a name="icordebugappdomainattach-method"></a><span data-ttu-id="f2f65-102">ICorDebugAppDomain::Attach 方法</span><span class="sxs-lookup"><span data-stu-id="f2f65-102">ICorDebugAppDomain::Attach Method</span></span>

<span data-ttu-id="f2f65-103">将调试器附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="f2f65-103">Attaches the debugger to the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2f65-104">语法</span><span class="sxs-lookup"><span data-stu-id="f2f65-104">Syntax</span></span>  
  
```cpp  
HRESULT Attach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="f2f65-105">备注</span><span class="sxs-lookup"><span data-stu-id="f2f65-105">Remarks</span></span>  

 <span data-ttu-id="f2f65-106">调试器必须附加到应用程序域，才能接收事件和启用应用程序域的调试。</span><span class="sxs-lookup"><span data-stu-id="f2f65-106">The debugger must be attached to the application domain to receive events and to enable debugging of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2f65-107">要求</span><span class="sxs-lookup"><span data-stu-id="f2f65-107">Requirements</span></span>  

 <span data-ttu-id="f2f65-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2f65-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2f65-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f2f65-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f2f65-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f2f65-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f2f65-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2f65-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
