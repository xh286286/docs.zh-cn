---
title: ICorDebugObjectValue::GetClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue::GetClass
helpviewer_keywords:
- ICorDebugObjectValue::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 5be25292-8357-445f-a09b-f997c0de761c
topic_type:
- apiref
ms.openlocfilehash: 42e5ffeeb81bc5e9a99c8ada8d58296fc9f610d3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95695395"
---
# <a name="icordebugobjectvaluegetclass-method"></a><span data-ttu-id="260a6-102">ICorDebugObjectValue::GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="260a6-102">ICorDebugObjectValue::GetClass Method</span></span>

<span data-ttu-id="260a6-103">获取此对象值的类。</span><span class="sxs-lookup"><span data-stu-id="260a6-103">Gets the class of this object value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="260a6-104">语法</span><span class="sxs-lookup"><span data-stu-id="260a6-104">Syntax</span></span>  
  
```cpp  
HRESULT GetClass (  
    [out] ICorDebugClass     **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="260a6-105">参数</span><span class="sxs-lookup"><span data-stu-id="260a6-105">Parameters</span></span>  

 `ppClass`  
 <span data-ttu-id="260a6-106">弄一个指向 "ICorDebugClass" 对象地址的指针，该对象表示由此 "ICorDebugObjectValue" 对象表示的对象值的类。</span><span class="sxs-lookup"><span data-stu-id="260a6-106">[out] A pointer to the address of an "ICorDebugClass" object that represents the class of the object value represented by this "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="260a6-107">注解</span><span class="sxs-lookup"><span data-stu-id="260a6-107">Remarks</span></span>  

 <span data-ttu-id="260a6-108">`GetClass`和[ICorDebugValue：： GetType](icordebugvalue-gettype-method.md)方法各自返回有关值类型的信息; 它们都被一般感知的[ICorDebugValue2：： GetExactType](icordebugvalue2-getexacttype-method.md)取代。</span><span class="sxs-lookup"><span data-stu-id="260a6-108">The `GetClass` and [ICorDebugValue::GetType](icordebugvalue-gettype-method.md) methods each return information about the type of a value; they are both superseded by the generics-aware [ICorDebugValue2::GetExactType](icordebugvalue2-getexacttype-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="260a6-109">要求</span><span class="sxs-lookup"><span data-stu-id="260a6-109">Requirements</span></span>  

 <span data-ttu-id="260a6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="260a6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="260a6-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="260a6-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="260a6-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="260a6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="260a6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="260a6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="260a6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="260a6-114">See also</span></span>
