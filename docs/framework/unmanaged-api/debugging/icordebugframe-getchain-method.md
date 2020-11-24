---
title: ICorDebugFrame::GetChain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetChain
helpviewer_keywords:
- ICorDebugFrame::GetChain method [.NET Framework debugging]
- GetChain method [.NET Framework debugging]
ms.assetid: e28e51d3-8f73-494f-bcd4-48bac239fbe1
topic_type:
- apiref
ms.openlocfilehash: d605ac36c17a815bf546819e331830f51142cfcd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690416"
---
# <a name="icordebugframegetchain-method"></a><span data-ttu-id="e4681-102">ICorDebugFrame::GetChain 方法</span><span class="sxs-lookup"><span data-stu-id="e4681-102">ICorDebugFrame::GetChain Method</span></span>

<span data-ttu-id="e4681-103">获取一个指针，该指针指向此帧所属的链。</span><span class="sxs-lookup"><span data-stu-id="e4681-103">Gets a pointer to the chain this frame is a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4681-104">语法</span><span class="sxs-lookup"><span data-stu-id="e4681-104">Syntax</span></span>  
  
```cpp  
HRESULT GetChain (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4681-105">参数</span><span class="sxs-lookup"><span data-stu-id="e4681-105">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="e4681-106">弄指向 ICorDebugChain 对象的地址的指针，该对象表示包含此帧的链。</span><span class="sxs-lookup"><span data-stu-id="e4681-106">[out] A pointer to the address of an ICorDebugChain object that represents the chain containing this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4681-107">要求</span><span class="sxs-lookup"><span data-stu-id="e4681-107">Requirements</span></span>  

 <span data-ttu-id="e4681-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4681-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4681-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4681-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4681-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4681-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4681-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4681-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
