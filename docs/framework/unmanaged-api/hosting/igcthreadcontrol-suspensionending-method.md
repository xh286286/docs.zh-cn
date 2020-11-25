---
title: IGCThreadControl::SuspensionEnding 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
ms.openlocfilehash: 4638672b1d64a9ea07618212cc514d00996470eb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721668"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="f3344-102">IGCThreadControl::SuspensionEnding 方法</span><span class="sxs-lookup"><span data-stu-id="f3344-102">IGCThreadControl::SuspensionEnding Method</span></span>

<span data-ttu-id="f3344-103">向宿主通知运行时在垃圾回收或其他挂起后正在恢复线程。</span><span class="sxs-lookup"><span data-stu-id="f3344-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3344-104">语法</span><span class="sxs-lookup"><span data-stu-id="f3344-104">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f3344-105">参数</span><span class="sxs-lookup"><span data-stu-id="f3344-105">Parameters</span></span>  

 `Generation`  
 <span data-ttu-id="f3344-106">中已对其执行垃圾回收的代。</span><span class="sxs-lookup"><span data-stu-id="f3344-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f3344-107">注解</span><span class="sxs-lookup"><span data-stu-id="f3344-107">Remarks</span></span>  

 <span data-ttu-id="f3344-108">不要在回调过程中重新计划任何线程 `SuspensionEnding` 。</span><span class="sxs-lookup"><span data-stu-id="f3344-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3344-109">要求</span><span class="sxs-lookup"><span data-stu-id="f3344-109">Requirements</span></span>  

 <span data-ttu-id="f3344-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f3344-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3344-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f3344-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3344-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3344-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3344-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3344-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3344-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3344-114">See also</span></span>

- [<span data-ttu-id="f3344-115">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="f3344-115">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)
