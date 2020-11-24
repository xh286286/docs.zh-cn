---
title: ICorDebugReferenceValue::GetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::GetValue method [.NET Framework debugging]
ms.assetid: 5da07f99-6c70-46ec-b997-5ab6fb7106cd
topic_type:
- apiref
ms.openlocfilehash: cbdba623b02ccc85c6d4784a9539adf14fd256e7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95691183"
---
# <a name="icordebugreferencevaluegetvalue-method"></a><span data-ttu-id="5e44f-102">ICorDebugReferenceValue::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="5e44f-102">ICorDebugReferenceValue::GetValue Method</span></span>

<span data-ttu-id="5e44f-103">获取所引用对象的当前内存地址。</span><span class="sxs-lookup"><span data-stu-id="5e44f-103">Gets the current memory address of the referenced object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e44f-104">语法</span><span class="sxs-lookup"><span data-stu-id="5e44f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetValue (  
    [out] CORDB_ADDRESS   *pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5e44f-105">参数</span><span class="sxs-lookup"><span data-stu-id="5e44f-105">Parameters</span></span>  

 `pValue`  
 <span data-ttu-id="5e44f-106">弄一个指向 `CORDB_ADDRESS` 值的指针，该值指定此 ICorDebugReferenceValue 对象指向的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="5e44f-106">[out] A pointer to a `CORDB_ADDRESS` value that specifies the address of the object to which this ICorDebugReferenceValue object points.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e44f-107">要求</span><span class="sxs-lookup"><span data-stu-id="5e44f-107">Requirements</span></span>  

 <span data-ttu-id="5e44f-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e44f-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e44f-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5e44f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5e44f-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5e44f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5e44f-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e44f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
