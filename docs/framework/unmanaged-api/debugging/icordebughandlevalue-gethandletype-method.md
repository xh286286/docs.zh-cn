---
title: ICorDebugHandleValue::GetHandleType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue.GetHandleType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue::GetHandleType
helpviewer_keywords:
- GetHandleType method [.NET Framework debugging]
- ICorDebugHandleValue::GetHandleType method [.NET Framework debugging]
ms.assetid: d5e7b12d-835a-4e86-ae2f-d658d4f1c67c
topic_type:
- apiref
ms.openlocfilehash: 72ef9a0fe4cd08ce67594600375953c249243d4f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95734148"
---
# <a name="icordebughandlevaluegethandletype-method"></a><span data-ttu-id="a1d8f-102">ICorDebugHandleValue::GetHandleType 方法</span><span class="sxs-lookup"><span data-stu-id="a1d8f-102">ICorDebugHandleValue::GetHandleType Method</span></span>

<span data-ttu-id="a1d8f-103">获取一个值，该值指示此 ICorDebugHandleValue 对象所引用的句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="a1d8f-103">Gets a value that indicates the kind of handle referenced by this ICorDebugHandleValue object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1d8f-104">语法</span><span class="sxs-lookup"><span data-stu-id="a1d8f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetHandleType (  
    [out] CorDebugHandleType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1d8f-105">参数</span><span class="sxs-lookup"><span data-stu-id="a1d8f-105">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="a1d8f-106">弄指向 CorDebugHandleType 枚举的值的指针，该枚举指示此句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="a1d8f-106">[out] A pointer to a value of the CorDebugHandleType enumeration that indicates the type of this handle.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1d8f-107">要求</span><span class="sxs-lookup"><span data-stu-id="a1d8f-107">Requirements</span></span>  

 <span data-ttu-id="a1d8f-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1d8f-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1d8f-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a1d8f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a1d8f-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a1d8f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1d8f-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1d8f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
