---
title: ICorDebugAppDomain::EnumerateSteppers 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateSteppers
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateSteppers
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateSteppers method [.NET Framework debugging]
- EnumerateSteppers method [.NET Framework debugging]
ms.assetid: 3f3c4503-570e-44c1-ae6a-a3c6b840c732
topic_type:
- apiref
ms.openlocfilehash: fd9243d9e0c12b572613694538661fd553e8a487
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715922"
---
# <a name="icordebugappdomainenumeratesteppers-method"></a><span data-ttu-id="c7771-102">ICorDebugAppDomain::EnumerateSteppers 方法</span><span class="sxs-lookup"><span data-stu-id="c7771-102">ICorDebugAppDomain::EnumerateSteppers Method</span></span>

<span data-ttu-id="c7771-103">获取应用程序域中所有活动 steppers 的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c7771-103">Gets an enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7771-104">语法</span><span class="sxs-lookup"><span data-stu-id="c7771-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateSteppers (  
    [out] ICorDebugStepperEnum   **ppSteppers  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c7771-105">参数</span><span class="sxs-lookup"><span data-stu-id="c7771-105">Parameters</span></span>  

 `ppSteppers`  
 <span data-ttu-id="c7771-106">弄指向 ICorDebugStepperEnum 对象地址的指针，该对象是应用程序域中所有活动 steppers 的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c7771-106">[out] A pointer to the address of an ICorDebugStepperEnum object that is the enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7771-107">要求</span><span class="sxs-lookup"><span data-stu-id="c7771-107">Requirements</span></span>  

 <span data-ttu-id="c7771-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7771-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7771-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7771-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7771-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7771-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7771-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7771-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
