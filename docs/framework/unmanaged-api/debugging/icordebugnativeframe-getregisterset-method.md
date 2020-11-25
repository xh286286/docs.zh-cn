---
title: ICorDebugNativeFrame::GetRegisterSet 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetRegisterSet
helpviewer_keywords:
- ICorDebugNativeFrame::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 6f309b5f-5556-4f1e-b1dd-4fe97fc81d01
topic_type:
- apiref
ms.openlocfilehash: 945a398d32b50efc81ba45e705ed9d4161ed1524
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709266"
---
# <a name="icordebugnativeframegetregisterset-method"></a><span data-ttu-id="97b48-102">ICorDebugNativeFrame::GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="97b48-102">ICorDebugNativeFrame::GetRegisterSet Method</span></span>

<span data-ttu-id="97b48-103">获取此堆栈帧的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="97b48-103">Gets the register set for this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97b48-104">语法</span><span class="sxs-lookup"><span data-stu-id="97b48-104">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="97b48-105">参数</span><span class="sxs-lookup"><span data-stu-id="97b48-105">Parameters</span></span>  

 `ppRegisters`  
 <span data-ttu-id="97b48-106">弄一个指向 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 对象地址的指针，该对象表示此堆栈帧的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="97b48-106">[out] A pointer to the address of an [ICorDebugRegisterSet](icordebugregisterset-interface.md) object that represents the register set for this stack frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97b48-107">要求</span><span class="sxs-lookup"><span data-stu-id="97b48-107">Requirements</span></span>  

 <span data-ttu-id="97b48-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="97b48-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97b48-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="97b48-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="97b48-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97b48-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="97b48-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97b48-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97b48-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97b48-112">See also</span></span>
