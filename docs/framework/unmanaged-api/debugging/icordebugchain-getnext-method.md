---
title: ICorDebugChain::GetNext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetNext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetNext
helpviewer_keywords:
- GetNext method [.NET Framework debugging]
- ICorDebugChain::GetNext method [.NET Framework debugging]
ms.assetid: 8d9744a5-e08b-4ab2-9855-5c22711cc1e6
topic_type:
- apiref
ms.openlocfilehash: 75b97f4333f3e81533b1f10b8c3c7ba6197ac94a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730079"
---
# <a name="icordebugchaingetnext-method"></a><span data-ttu-id="bafb0-102">ICorDebugChain::GetNext 方法</span><span class="sxs-lookup"><span data-stu-id="bafb0-102">ICorDebugChain::GetNext Method</span></span>

<span data-ttu-id="bafb0-103">获取线程的下一个帧链。</span><span class="sxs-lookup"><span data-stu-id="bafb0-103">Gets the next chain of frames for the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bafb0-104">语法</span><span class="sxs-lookup"><span data-stu-id="bafb0-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNext (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bafb0-105">参数</span><span class="sxs-lookup"><span data-stu-id="bafb0-105">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="bafb0-106">弄指向 ICorDebugChain 对象的地址的指针，该对象表示线程的下一个帧链。</span><span class="sxs-lookup"><span data-stu-id="bafb0-106">[out] A pointer to the address of an ICorDebugChain object that represents the next chain of frames for the thread.</span></span> <span data-ttu-id="bafb0-107">如果此链是最后一个链， `ppChain` 则为 null。</span><span class="sxs-lookup"><span data-stu-id="bafb0-107">If this chain is the last chain, `ppChain` is null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bafb0-108">要求</span><span class="sxs-lookup"><span data-stu-id="bafb0-108">Requirements</span></span>  

 <span data-ttu-id="bafb0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bafb0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bafb0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bafb0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bafb0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bafb0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bafb0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bafb0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
