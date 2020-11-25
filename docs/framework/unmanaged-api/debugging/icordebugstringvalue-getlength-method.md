---
title: ICorDebugStringValue::GetLength 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetLength
helpviewer_keywords:
- ICorDebugStringValue::GetLength method [.NET Framework debugging]
- GetLength method [.NET Framework debugging]
ms.assetid: a1ebfc69-46a6-4225-8788-b7cfb2f15e1d
topic_type:
- apiref
ms.openlocfilehash: 74a4b42be09c577cc80f1a73e077694e5a4a8d5f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697111"
---
# <a name="icordebugstringvaluegetlength-method"></a><span data-ttu-id="a001a-102">ICorDebugStringValue::GetLength 方法</span><span class="sxs-lookup"><span data-stu-id="a001a-102">ICorDebugStringValue::GetLength Method</span></span>

<span data-ttu-id="a001a-103">获取此 ICorDebugStringValue 引用的字符串中的字符数。</span><span class="sxs-lookup"><span data-stu-id="a001a-103">Gets the number of characters in the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a001a-104">语法</span><span class="sxs-lookup"><span data-stu-id="a001a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetLength (  
    [out] ULONG32   *pcchString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a001a-105">参数</span><span class="sxs-lookup"><span data-stu-id="a001a-105">Parameters</span></span>  

 `pcchString`  
 <span data-ttu-id="a001a-106">弄一个指向值的指针，该值指定此对象所引用的字符串的长度 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="a001a-106">[out] A pointer to a value that specifies the length of the string referenced by this `ICorDebugStringValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a001a-107">要求</span><span class="sxs-lookup"><span data-stu-id="a001a-107">Requirements</span></span>  

 <span data-ttu-id="a001a-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a001a-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a001a-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a001a-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a001a-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a001a-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a001a-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a001a-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
