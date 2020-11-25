---
title: ICorThreadpool::CorSetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorSetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSetMaxThreads
helpviewer_keywords:
- ICorThreadpool::CorSetMaxThreads method [.NET Framework hosting]
- CorSetMaxThreads method [.NET Framework hosting]
ms.assetid: 4a846238-df4e-4060-ba3b-5173f6a51e85
topic_type:
- apiref
ms.openlocfilehash: f7d9d3d059abcf58fe0f4b35ce41046efb9c2400
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733977"
---
# <a name="icorthreadpoolcorsetmaxthreads-method"></a><span data-ttu-id="3c372-102">ICorThreadpool::CorSetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="3c372-102">ICorThreadpool::CorSetMaxThreads Method</span></span>

<span data-ttu-id="3c372-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="3c372-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c372-104">语法</span><span class="sxs-lookup"><span data-stu-id="3c372-104">Syntax</span></span>  
  
```cpp  
HRESULT CorSetMaxThreads (  
    [in] DWORD MaxWorkerThreads,  
    [in] DWORD MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="3c372-105">要求</span><span class="sxs-lookup"><span data-stu-id="3c372-105">Requirements</span></span>  

 <span data-ttu-id="3c372-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c372-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c372-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3c372-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3c372-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3c372-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3c372-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c372-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c372-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c372-110">See also</span></span>

- [<span data-ttu-id="3c372-111">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="3c372-111">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
