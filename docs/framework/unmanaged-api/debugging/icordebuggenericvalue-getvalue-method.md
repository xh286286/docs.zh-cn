---
title: ICorDebugGenericValue::GetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue::GetValue
helpviewer_keywords:
- ICorDebugGenericValue::GetValue method [.NET Framework debugging]
- GetValue method, ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: 4e95d7cb-144d-4ccf-8a69-d605f4744be2
topic_type:
- apiref
ms.openlocfilehash: dd1c1ba4a976a10d0c38c5295fff838faf072f51
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728103"
---
# <a name="icordebuggenericvaluegetvalue-method"></a><span data-ttu-id="88a75-102">ICorDebugGenericValue::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="88a75-102">ICorDebugGenericValue::GetValue Method</span></span>

<span data-ttu-id="88a75-103">将此泛型的值复制到指定的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="88a75-103">Copies the value of this generic into the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88a75-104">语法</span><span class="sxs-lookup"><span data-stu-id="88a75-104">Syntax</span></span>  
  
```cpp  
HRESULT GetValue (  
    [out] void     *pTo  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="88a75-105">参数</span><span class="sxs-lookup"><span data-stu-id="88a75-105">Parameters</span></span>  

 `pTo`  
 <span data-ttu-id="88a75-106">弄一个指针，指向由此 ICorDebugGenericValue 对象表示的值。</span><span class="sxs-lookup"><span data-stu-id="88a75-106">[out] A pointer to the value that is represented by this ICorDebugGenericValue object.</span></span> <span data-ttu-id="88a75-107">此值可以是简单类型，也可以是引用类型 (即，指针) 。</span><span class="sxs-lookup"><span data-stu-id="88a75-107">The value may be a simple type or a reference type (that is, a pointer).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88a75-108">要求</span><span class="sxs-lookup"><span data-stu-id="88a75-108">Requirements</span></span>  

 <span data-ttu-id="88a75-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="88a75-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88a75-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="88a75-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="88a75-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88a75-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="88a75-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88a75-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
