---
title: CorMarkThreadInThreadPool 函数
ms.date: 03/30/2017
api_name:
- CorMarkThreadInThreadPool
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CorMarkThreadInThreadPool
helpviewer_keywords:
- CorMarkThreadInThreadPool function [.NET Framework hosting]
ms.assetid: 3f958d41-e82e-4ec3-ae6f-16c7b3b31e3e
topic_type:
- apiref
ms.openlocfilehash: 69508e1ccab2e7aa98f33bf048ccfca5e6f70811
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688011"
---
# <a name="cormarkthreadinthreadpool-function"></a><span data-ttu-id="112c4-102">CorMarkThreadInThreadPool 函数</span><span class="sxs-lookup"><span data-stu-id="112c4-102">CorMarkThreadInThreadPool Function</span></span>

<span data-ttu-id="112c4-103">标记当前正在执行的线程池线程以执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="112c4-103">Marks the currently executing thread-pool thread for the execution of managed code.</span></span> <span data-ttu-id="112c4-104">从 .NET Framework 版本2.0 开始，此函数不起作用。</span><span class="sxs-lookup"><span data-stu-id="112c4-104">Starting with the .NET Framework version 2.0, this function has no effect.</span></span> <span data-ttu-id="112c4-105">这不是必需的，并且可以从代码中删除。</span><span class="sxs-lookup"><span data-stu-id="112c4-105">It is not required, and can be removed from your code.</span></span> <span data-ttu-id="112c4-106">此函数在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="112c4-106">This function is deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="112c4-107">语法</span><span class="sxs-lookup"><span data-stu-id="112c4-107">Syntax</span></span>  
  
```cpp  
void CorMarkThreadInThreadPool ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="112c4-108">要求</span><span class="sxs-lookup"><span data-stu-id="112c4-108">Requirements</span></span>  

 <span data-ttu-id="112c4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="112c4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="112c4-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="112c4-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="112c4-111">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="112c4-111">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="112c4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="112c4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="112c4-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="112c4-113">See also</span></span>

- [<span data-ttu-id="112c4-114">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="112c4-114">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
