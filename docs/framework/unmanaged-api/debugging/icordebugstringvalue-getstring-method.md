---
title: ICorDebugStringValue::GetString 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetString
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetString
helpviewer_keywords:
- ICorDebugStringValue::GetString method [.NET Framework debugging]
- GetString method, ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: 2b94bda7-09ee-435d-91b9-c4e31af1896c
topic_type:
- apiref
ms.openlocfilehash: 9051fa612bef3fbd817ff7bdadbd52c96ade5b7f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697085"
---
# <a name="icordebugstringvaluegetstring-method"></a><span data-ttu-id="7860f-102">ICorDebugStringValue::GetString 方法</span><span class="sxs-lookup"><span data-stu-id="7860f-102">ICorDebugStringValue::GetString Method</span></span>

<span data-ttu-id="7860f-103">获取此 ICorDebugStringValue 引用的字符串。</span><span class="sxs-lookup"><span data-stu-id="7860f-103">Gets the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7860f-104">语法</span><span class="sxs-lookup"><span data-stu-id="7860f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetString (  
    [in] ULONG32    cchString,  
    [out] ULONG32   *pcchString,  
    [out, size_is(cchString), length_is(*pcchString)]
        WCHAR       szString[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7860f-105">参数</span><span class="sxs-lookup"><span data-stu-id="7860f-105">Parameters</span></span>  

 `cchString`  
 <span data-ttu-id="7860f-106">[in] `szString` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="7860f-106">[in] The size of the `szString` array.</span></span>  
  
 `pcchString`  
 <span data-ttu-id="7860f-107">弄一个指针，指向数组中返回的字符数 `szString` 。</span><span class="sxs-lookup"><span data-stu-id="7860f-107">[out] A pointer to the number of characters returned in the `szString` array.</span></span>  
  
 `szString`  
 <span data-ttu-id="7860f-108">弄存储检索的字符串的数组。</span><span class="sxs-lookup"><span data-stu-id="7860f-108">[out] An array that stores the retrieved string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7860f-109">要求</span><span class="sxs-lookup"><span data-stu-id="7860f-109">Requirements</span></span>  

 <span data-ttu-id="7860f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7860f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7860f-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7860f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7860f-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7860f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7860f-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7860f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
