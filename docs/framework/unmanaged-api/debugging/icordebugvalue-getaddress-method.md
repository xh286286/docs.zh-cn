---
title: ICorDebugValue::GetAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetAddress
helpviewer_keywords:
- ICorDebugValue::GetAddress method [.NET Framework debugging]
- GetAddress method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: a247c792-45e1-4538-9e1f-b46acca4a463
topic_type:
- apiref
ms.openlocfilehash: 47c0c4dfa78e85bcc83f0bb2a333955c8e8666fa
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728363"
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="ee868-102">ICorDebugValue::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="ee868-102">ICorDebugValue::GetAddress Method</span></span>

<span data-ttu-id="ee868-103">获取此 "ICorDebugValue" 对象的地址，该对象处于调试过程中。</span><span class="sxs-lookup"><span data-stu-id="ee868-103">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee868-104">语法</span><span class="sxs-lookup"><span data-stu-id="ee868-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ee868-105">参数</span><span class="sxs-lookup"><span data-stu-id="ee868-105">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="ee868-106">弄指向 `CORDB_ADDRESS` 对象的指针，该对象指定此值对象的地址。</span><span class="sxs-lookup"><span data-stu-id="ee868-106">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ee868-107">注解</span><span class="sxs-lookup"><span data-stu-id="ee868-107">Remarks</span></span>  

 <span data-ttu-id="ee868-108">如果值不可用，则返回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="ee868-108">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="ee868-109">如果值至少出现在寄存器中或者存储在垃圾回收器句柄 () 中，则可能会发生这种情况 `GCHandle` 。</span><span class="sxs-lookup"><span data-stu-id="ee868-109">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee868-110">要求</span><span class="sxs-lookup"><span data-stu-id="ee868-110">Requirements</span></span>  

 <span data-ttu-id="ee868-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee868-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee868-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ee868-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ee868-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee868-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee868-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee868-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee868-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee868-115">See also</span></span>
