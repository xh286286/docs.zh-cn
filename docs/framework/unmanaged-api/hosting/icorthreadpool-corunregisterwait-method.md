---
title: ICorThreadpool::CorUnregisterWait 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorUnregisterWait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorUnregisterWait
helpviewer_keywords:
- CorUnregisterWait method [.NET Framework hosting]
- ICorThreadpool::CorUnregisterWait method [.NET Framework hosting]
ms.assetid: 42c933f1-30a8-4011-bdea-e117f3c3265e
topic_type:
- apiref
ms.openlocfilehash: 38b3655da75750ffc3ea1c7983ce3b549d76f087
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733966"
---
# <a name="icorthreadpoolcorunregisterwait-method"></a><span data-ttu-id="3898c-102">ICorThreadpool::CorUnregisterWait 方法</span><span class="sxs-lookup"><span data-stu-id="3898c-102">ICorThreadpool::CorUnregisterWait Method</span></span>

<span data-ttu-id="3898c-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="3898c-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3898c-104">语法</span><span class="sxs-lookup"><span data-stu-id="3898c-104">Syntax</span></span>  
  
```cpp  
HRESULT CorUnregisterWait (  
    [in] HANDLE hWaitObject,  
    [in] HANDLE CompletionEvent,  
    [out] BOOL* result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="3898c-105">要求</span><span class="sxs-lookup"><span data-stu-id="3898c-105">Requirements</span></span>  

 <span data-ttu-id="3898c-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3898c-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3898c-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3898c-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3898c-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3898c-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3898c-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3898c-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3898c-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3898c-110">See also</span></span>

- [<span data-ttu-id="3898c-111">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="3898c-111">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
