---
title: IGCThreadControl::SuspensionStarting 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionStarting
helpviewer_keywords:
- IGCThreadControl::SuspensionStarting method [.NET Framework hosting]
- SuspensionStarting method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 0af312af-98e9-415e-b182-42e80a1aee51
topic_type:
- apiref
ms.openlocfilehash: 9d39ee79f7734f7dd099a07640ecb06f4f8dcbb3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721655"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="710f9-102">IGCThreadControl::SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="710f9-102">IGCThreadControl::SuspensionStarting Method</span></span>

<span data-ttu-id="710f9-103">通知宿主运行时正在为垃圾回收或其他挂起开始线程挂起。</span><span class="sxs-lookup"><span data-stu-id="710f9-103">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="710f9-104">语法</span><span class="sxs-lookup"><span data-stu-id="710f9-104">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="710f9-105">备注</span><span class="sxs-lookup"><span data-stu-id="710f9-105">Remarks</span></span>  

 <span data-ttu-id="710f9-106">不要在回调过程中重新计划任何线程 `SuspensionStarting` 。</span><span class="sxs-lookup"><span data-stu-id="710f9-106">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="710f9-107">要求</span><span class="sxs-lookup"><span data-stu-id="710f9-107">Requirements</span></span>  

 <span data-ttu-id="710f9-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="710f9-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="710f9-109">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="710f9-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="710f9-110">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="710f9-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="710f9-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="710f9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="710f9-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="710f9-112">See also</span></span>

- [<span data-ttu-id="710f9-113">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="710f9-113">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)
