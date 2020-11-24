---
title: IHostManualEvent 接口
ms.date: 03/30/2017
api_name:
- IHostManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent
helpviewer_keywords:
- IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type:
- apiref
ms.openlocfilehash: 50e37b770e3ee6e0a5cdfca61fc5b09749e5735f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673176"
---
# <a name="ihostmanualevent-interface"></a><span data-ttu-id="6c636-102">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="6c636-102">IHostManualEvent Interface</span></span>

<span data-ttu-id="6c636-103">提供宿主手动重置事件表示形式的实现。</span><span class="sxs-lookup"><span data-stu-id="6c636-103">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6c636-104">方法</span><span class="sxs-lookup"><span data-stu-id="6c636-104">Methods</span></span>  
  
|<span data-ttu-id="6c636-105">方法</span><span class="sxs-lookup"><span data-stu-id="6c636-105">Method</span></span>|<span data-ttu-id="6c636-106">说明</span><span class="sxs-lookup"><span data-stu-id="6c636-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6c636-107">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="6c636-107">Reset Method</span></span>](ihostmanualevent-reset-method.md)|<span data-ttu-id="6c636-108">将当前实例重置 `IHostManualEvent` 为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="6c636-108">Resets the current `IHostManualEvent` instance to a non-signaled state.</span></span>|  
|[<span data-ttu-id="6c636-109">Set 方法</span><span class="sxs-lookup"><span data-stu-id="6c636-109">Set Method</span></span>](ihostmanualevent-set-method.md)|<span data-ttu-id="6c636-110">将当前 `IHostManualEvent` 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="6c636-110">Sets the current `IHostManualEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="6c636-111">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="6c636-111">Wait Method</span></span>](ihostmanualevent-wait-method.md)|<span data-ttu-id="6c636-112">导致当前 `IHostManualEvent` 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="6c636-112">Causes the current `IHostManualEvent` instance to wait until it is owned, or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6c636-113">要求</span><span class="sxs-lookup"><span data-stu-id="6c636-113">Requirements</span></span>  

 <span data-ttu-id="6c636-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c636-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c636-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6c636-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6c636-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6c636-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6c636-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c636-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c636-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c636-118">See also</span></span>

- [<span data-ttu-id="6c636-119">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="6c636-119">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="6c636-120">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="6c636-120">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="6c636-121">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="6c636-121">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="6c636-122">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="6c636-122">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="6c636-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="6c636-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
