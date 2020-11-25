---
title: ICorThreadpool::CorCreateTimer 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCreateTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCreateTimer
helpviewer_keywords:
- CorCreateTimer method [.NET Framework hosting]
- ICorThreadpool::CorCreateTimer method [.NET Framework hosting]
ms.assetid: 0d56ef25-30f1-4499-8a1f-76e7654ec614
topic_type:
- apiref
ms.openlocfilehash: 3eac575e18c7371754401da6498d85ba7ed6c8cf
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717603"
---
# <a name="icorthreadpoolcorcreatetimer-method"></a><span data-ttu-id="2d24a-102">ICorThreadpool::CorCreateTimer 方法</span><span class="sxs-lookup"><span data-stu-id="2d24a-102">ICorThreadpool::CorCreateTimer Method</span></span>

<span data-ttu-id="2d24a-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="2d24a-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d24a-104">语法</span><span class="sxs-lookup"><span data-stu-id="2d24a-104">Syntax</span></span>  
  
```cpp  
HRESULT CorCreateTimer (  
    [in]  HANDLE*             phNewTimer,  
    [in]  WAITORTIMERCALLBACK Callback,  
    [in]  PVOID               Parameter,  
    [in]  DWORD               DueTime,  
    [in]  DWORD               Period,  
    [out] BOOL*               result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="2d24a-105">要求</span><span class="sxs-lookup"><span data-stu-id="2d24a-105">Requirements</span></span>  

 <span data-ttu-id="2d24a-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d24a-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d24a-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2d24a-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2d24a-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2d24a-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2d24a-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d24a-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d24a-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d24a-110">See also</span></span>

- [<span data-ttu-id="2d24a-111">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="2d24a-111">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
