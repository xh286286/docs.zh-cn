---
title: IHostSemaphore 接口
ms.date: 03/30/2017
api_name:
- IHostSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore
helpviewer_keywords:
- IHostSemaphore interface [.NET Framework hosting]
ms.assetid: c0765321-656c-441e-bab5-58176292be1e
topic_type:
- apiref
ms.openlocfilehash: cccbf9a28b16ffee14b3fd3ec43c376109d6ccec
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683051"
---
# <a name="ihostsemaphore-interface"></a><span data-ttu-id="79db7-102">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="79db7-102">IHostSemaphore Interface</span></span>

<span data-ttu-id="79db7-103">表示线程的信号量的主机实现。</span><span class="sxs-lookup"><span data-stu-id="79db7-103">Represents the host's implementation of a semaphore for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="79db7-104">方法</span><span class="sxs-lookup"><span data-stu-id="79db7-104">Methods</span></span>  
  
|<span data-ttu-id="79db7-105">方法</span><span class="sxs-lookup"><span data-stu-id="79db7-105">Method</span></span>|<span data-ttu-id="79db7-106">说明</span><span class="sxs-lookup"><span data-stu-id="79db7-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="79db7-107">ReleaseSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="79db7-107">ReleaseSemaphore Method</span></span>](ihostsemaphore-releasesemaphore-method.md)|<span data-ttu-id="79db7-108">`IHostSemaphore`按指定量增加当前实例的计数。</span><span class="sxs-lookup"><span data-stu-id="79db7-108">Increases the count of the current `IHostSemaphore` instance by the specified amount.</span></span>|  
|[<span data-ttu-id="79db7-109">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="79db7-109">Wait Method</span></span>](ihostsemaphore-wait-method.md)|<span data-ttu-id="79db7-110">使当前 `IHostSemaphore` 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="79db7-110">Causes the current `IHostSemaphore` instance to wait until it is owned or the specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="79db7-111">要求</span><span class="sxs-lookup"><span data-stu-id="79db7-111">Requirements</span></span>  

 <span data-ttu-id="79db7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79db7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79db7-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="79db7-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="79db7-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="79db7-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="79db7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79db7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79db7-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79db7-116">See also</span></span>

- [<span data-ttu-id="79db7-117">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="79db7-117">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="79db7-118">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="79db7-118">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="79db7-119">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="79db7-119">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="79db7-120">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="79db7-120">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="79db7-121">承载接口</span><span class="sxs-lookup"><span data-stu-id="79db7-121">Hosting Interfaces</span></span>](hosting-interfaces.md)
