---
title: ICorDebugChain::GetRegisterSet 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetRegisterSet
helpviewer_keywords:
- ICorDebugChain::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: bc4288b6-3331-4ae3-990d-e1d6e62ecb67
topic_type:
- apiref
ms.openlocfilehash: a3f02af1a0de9fcd7b3db1e49ef0d78af3395d2f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719653"
---
# <a name="icordebugchaingetregisterset-method"></a><span data-ttu-id="70f3c-102">ICorDebugChain::GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="70f3c-102">ICorDebugChain::GetRegisterSet Method</span></span>

<span data-ttu-id="70f3c-103">获取此链的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="70f3c-103">Gets the register set for the active part of this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70f3c-104">语法</span><span class="sxs-lookup"><span data-stu-id="70f3c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="70f3c-105">参数</span><span class="sxs-lookup"><span data-stu-id="70f3c-105">Parameters</span></span>  

 `ppRegisters`  
 <span data-ttu-id="70f3c-106">弄指向 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 对象的地址的指针，该对象表示此链的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="70f3c-106">[out] A pointer to the address of an [ICorDebugRegisterSet](icordebugregisterset-interface.md) object that represents the register set for the active part of this chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70f3c-107">要求</span><span class="sxs-lookup"><span data-stu-id="70f3c-107">Requirements</span></span>  

 <span data-ttu-id="70f3c-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="70f3c-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70f3c-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="70f3c-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="70f3c-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="70f3c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="70f3c-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70f3c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
