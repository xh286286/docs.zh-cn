---
title: ICorDebugProcess::ThreadForFiberCookie 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ThreadForFiberCookie
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ThreadForFiberCookie
helpviewer_keywords:
- ICorDebugProcess::ThreadForFiberCookie method [.NET Framework debugging]
- ThreadForFiberCookie method [.NET Framework debugging]
ms.assetid: afe4e97f-bffc-47e1-adad-d6e842487f35
topic_type:
- apiref
ms.openlocfilehash: 74cad19d9fa681a6afb933f79ee7061590084509
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95694654"
---
# <a name="icordebugprocessthreadforfibercookie-method"></a><span data-ttu-id="1540f-102">ICorDebugProcess::ThreadForFiberCookie 方法</span><span class="sxs-lookup"><span data-stu-id="1540f-102">ICorDebugProcess::ThreadForFiberCookie Method</span></span>

<span data-ttu-id="1540f-103">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="1540f-103">This method is not implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1540f-104">语法</span><span class="sxs-lookup"><span data-stu-id="1540f-104">Syntax</span></span>  
  
```cpp  
HRESULT ThreadForFiberCookie (  
    [in] DWORD fiberCookie,  
    [out] ICorDebugThread **ppThread  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="1540f-105">要求</span><span class="sxs-lookup"><span data-stu-id="1540f-105">Requirements</span></span>  

 <span data-ttu-id="1540f-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1540f-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1540f-107">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1540f-107">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1540f-108">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1540f-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1540f-109">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1540f-109">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
