---
title: ICorConfiguration::SetGCThreadControl 方法
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCThreadControl
helpviewer_keywords:
- ICorConfiguration::SetGCThreadControl method [.NET Framework hosting]
- SetGCThreadControl method [.NET Framework hosting]
ms.assetid: 72e38e61-3d56-4ae3-b8f6-0ab7922aaf11
topic_type:
- apiref
ms.openlocfilehash: 28b012bbe3f8c11ecd0afb8b5905336bd99c349c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724021"
---
# <a name="icorconfigurationsetgcthreadcontrol-method"></a><span data-ttu-id="d9dde-102">ICorConfiguration::SetGCThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="d9dde-102">ICorConfiguration::SetGCThreadControl Method</span></span>

<span data-ttu-id="d9dde-103">设置回调接口，用于为非运行时任务计划线程，否则将阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="d9dde-103">Sets the callback interface for scheduling threads for non-runtime tasks that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9dde-104">语法</span><span class="sxs-lookup"><span data-stu-id="d9dde-104">Syntax</span></span>  
  
```cpp  
HRESULT SetGCThreadControl (  
    [in] IGCThreadControl* pGCThreadControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9dde-105">参数</span><span class="sxs-lookup"><span data-stu-id="d9dde-105">Parameters</span></span>  

 `pGCThreadControl`  
 <span data-ttu-id="d9dde-106">中指向 [IGCThreadControl](igcthreadcontrol-interface.md) 对象的指针，该对象向宿主通知非运行时任务的线程挂起。</span><span class="sxs-lookup"><span data-stu-id="d9dde-106">[in] A pointer to an [IGCThreadControl](igcthreadcontrol-interface.md) object that notifies the host about the suspension of threads for non-runtime tasks.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9dde-107">注解</span><span class="sxs-lookup"><span data-stu-id="d9dde-107">Remarks</span></span>  

 <span data-ttu-id="d9dde-108">宿主可以在 [IGCThreadControl：： ThreadIsBlockingForSuspension](igcthreadcontrol-threadisblockingforsuspension-method.md) 回调中选择是否重新计划线程。</span><span class="sxs-lookup"><span data-stu-id="d9dde-108">The host may choose within the [IGCThreadControl::ThreadIsBlockingForSuspension](igcthreadcontrol-threadisblockingforsuspension-method.md) callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9dde-109">要求</span><span class="sxs-lookup"><span data-stu-id="d9dde-109">Requirements</span></span>  

 <span data-ttu-id="d9dde-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9dde-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9dde-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d9dde-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d9dde-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d9dde-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d9dde-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9dde-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9dde-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9dde-114">See also</span></span>

- [<span data-ttu-id="d9dde-115">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="d9dde-115">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)
