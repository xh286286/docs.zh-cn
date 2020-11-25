---
title: ICorDebugRegisterSet::GetRegistersAvailable 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable
helpviewer_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable method [.NET Framework debugging]
- GetRegistersAvailable method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 4ba08ffa-55a2-4662-9d6d-4738f1db60c9
topic_type:
- apiref
ms.openlocfilehash: d28c130e55cbebf29348752780c03b03c1b8f358
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95716988"
---
# <a name="icordebugregistersetgetregistersavailable-method"></a><span data-ttu-id="15adc-102">ICorDebugRegisterSet::GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="15adc-102">ICorDebugRegisterSet::GetRegistersAvailable Method</span></span>

<span data-ttu-id="15adc-103">获取指示此 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 中的哪些寄存器当前可用的位掩码。</span><span class="sxs-lookup"><span data-stu-id="15adc-103">Gets a bit mask indicating which registers in this [ICorDebugRegisterSet](icordebugregisterset-interface.md) are currently available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15adc-104">语法</span><span class="sxs-lookup"><span data-stu-id="15adc-104">Syntax</span></span>  
  
```cpp  
HRESULT GetRegistersAvailable (  
    [out] ULONG64   *pAvailable  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="15adc-105">参数</span><span class="sxs-lookup"><span data-stu-id="15adc-105">Parameters</span></span>  

 `pAvailable`  
 <span data-ttu-id="15adc-106">弄一个位掩码，用于指示当前可用的注册。</span><span class="sxs-lookup"><span data-stu-id="15adc-106">[out] A bit mask that indicates which registers are currently available.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="15adc-107">注解</span><span class="sxs-lookup"><span data-stu-id="15adc-107">Remarks</span></span>  

 <span data-ttu-id="15adc-108">如果无法为给定情况确定其值，则寄存器可能不可用。</span><span class="sxs-lookup"><span data-stu-id="15adc-108">A register may be unavailable if its value cannot be determined for the given situation.</span></span>  
  
 <span data-ttu-id="15adc-109">对于每个寄存器 (1 << 注册索引) ，返回的掩码包含一个位。</span><span class="sxs-lookup"><span data-stu-id="15adc-109">The returned mask contains a bit for each register (1 << the register index).</span></span> <span data-ttu-id="15adc-110">如果寄存器可用，则位值为 1; 否则为0。</span><span class="sxs-lookup"><span data-stu-id="15adc-110">The bit value is 1 if the register is available, or 0 if it is not available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15adc-111">要求</span><span class="sxs-lookup"><span data-stu-id="15adc-111">Requirements</span></span>  

 <span data-ttu-id="15adc-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="15adc-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15adc-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="15adc-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="15adc-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15adc-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15adc-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15adc-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15adc-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15adc-116">See also</span></span>

- [<span data-ttu-id="15adc-117">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="15adc-117">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="15adc-118">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="15adc-118">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
