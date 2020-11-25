---
title: ICorThreadpool::CorDeleteTimer 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorDeleteTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorDeleteTimer
helpviewer_keywords:
- ICorThreadpool::CorDeleteTimer method [.NET Framework hosting]
- CorDeleteTimer method [.NET Framework hosting]
ms.assetid: 74847c35-7ca1-466a-b750-b25e7b03d100
topic_type:
- apiref
ms.openlocfilehash: 97658d5418ac3c04abd423ffff86324acf0e99c8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720527"
---
# <a name="icorthreadpoolcordeletetimer-method"></a><span data-ttu-id="65574-102">ICorThreadpool::CorDeleteTimer 方法</span><span class="sxs-lookup"><span data-stu-id="65574-102">ICorThreadpool::CorDeleteTimer Method</span></span>

<span data-ttu-id="65574-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="65574-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65574-104">语法</span><span class="sxs-lookup"><span data-stu-id="65574-104">Syntax</span></span>  
  
```cpp  
HRESULT CorDeleteTimer (  
    [in]  HANDLE Timer,  
    [in]  HANDLE CompletionEvent,  
    [out] BOOL*  result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="65574-105">要求</span><span class="sxs-lookup"><span data-stu-id="65574-105">Requirements</span></span>  

 <span data-ttu-id="65574-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="65574-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65574-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="65574-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="65574-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="65574-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="65574-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65574-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65574-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65574-110">See also</span></span>

- [<span data-ttu-id="65574-111">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="65574-111">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
