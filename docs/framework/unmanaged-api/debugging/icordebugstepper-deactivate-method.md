---
title: ICorDebugStepper::Deactivate 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.Deactivate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::Deactivate
helpviewer_keywords:
- Deactivate method [.NET Framework debugging]
- ICorDebugStepper::Deactivate method [.NET Framework debugging]
ms.assetid: 855f4199-b62d-40ce-998e-1eb4a1772142
topic_type:
- apiref
ms.openlocfilehash: 0d7d5e7e6c9bc1a68feda85c5214f3ae95df9b97
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730560"
---
# <a name="icordebugstepperdeactivate-method"></a><span data-ttu-id="74bf9-102">ICorDebugStepper::Deactivate 方法</span><span class="sxs-lookup"><span data-stu-id="74bf9-102">ICorDebugStepper::Deactivate Method</span></span>

<span data-ttu-id="74bf9-103">使此 ICorDebugStepper 取消其收到的最后一个步骤命令。</span><span class="sxs-lookup"><span data-stu-id="74bf9-103">Causes this ICorDebugStepper to cancel the last step command that it received.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74bf9-104">语法</span><span class="sxs-lookup"><span data-stu-id="74bf9-104">Syntax</span></span>  
  
```cpp  
HRESULT Deactivate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="74bf9-105">备注</span><span class="sxs-lookup"><span data-stu-id="74bf9-105">Remarks</span></span>  

 <span data-ttu-id="74bf9-106">在取消最近收到的步骤命令后，可能会发出新的单步执行命令。</span><span class="sxs-lookup"><span data-stu-id="74bf9-106">A new stepping command may be issued after the most recently received step command has been canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74bf9-107">要求</span><span class="sxs-lookup"><span data-stu-id="74bf9-107">Requirements</span></span>  

 <span data-ttu-id="74bf9-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="74bf9-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74bf9-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="74bf9-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="74bf9-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="74bf9-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="74bf9-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74bf9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
