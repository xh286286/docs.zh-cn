---
title: ICorDebugFunction::GetToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetToken
helpviewer_keywords:
- ICorDebugFunction::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: c6bbf479-062e-48e9-9c70-0f92e293e36a
topic_type:
- apiref
ms.openlocfilehash: 9aee95c554afad5b2ea3cf157fc9e62c9b7e40e9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696110"
---
# <a name="icordebugfunctiongettoken-method"></a><span data-ttu-id="36387-102">ICorDebugFunction::GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="36387-102">ICorDebugFunction::GetToken Method</span></span>

<span data-ttu-id="36387-103">获取此函数的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="36387-103">Gets the metadata token for this function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36387-104">语法</span><span class="sxs-lookup"><span data-stu-id="36387-104">Syntax</span></span>  
  
```cpp  
HRESULT GetToken (  
    [out] mdMethodDef *pMethodDef  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="36387-105">参数</span><span class="sxs-lookup"><span data-stu-id="36387-105">Parameters</span></span>  

 `pMethodDef`  
 <span data-ttu-id="36387-106">弄指向 `mdMethodDef` 引用此函数的元数据的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="36387-106">[out] A pointer to an `mdMethodDef` token that references the metadata for this function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36387-107">要求</span><span class="sxs-lookup"><span data-stu-id="36387-107">Requirements</span></span>  

 <span data-ttu-id="36387-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="36387-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36387-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="36387-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="36387-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="36387-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="36387-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36387-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
