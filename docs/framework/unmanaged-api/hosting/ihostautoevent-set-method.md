---
title: IHostAutoEvent::Set 方法
ms.date: 03/30/2017
api_name:
- IHostAutoEvent.Set
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent::Set
helpviewer_keywords:
- Set method, IHostAutoEvent interface [.NET Framework hosting]
- IHostAutoEvent::Set method [.NET Framework hosting]
ms.assetid: 46becf3e-bc0e-4338-85c0-9ab0df76a1d0
topic_type:
- apiref
ms.openlocfilehash: facfbb85645f444b010cb1fe1c34bbe94011ac50
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680819"
---
# <a name="ihostautoeventset-method"></a><span data-ttu-id="f3e3e-102">IHostAutoEvent::Set 方法</span><span class="sxs-lookup"><span data-stu-id="f3e3e-102">IHostAutoEvent::Set Method</span></span>

<span data-ttu-id="f3e3e-103">将当前的 [IHostAutoEvent](ihostautoevent-interface.md) 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-103">Sets the current [IHostAutoEvent](ihostautoevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3e3e-104">语法</span><span class="sxs-lookup"><span data-stu-id="f3e3e-104">Syntax</span></span>  
  
```cpp  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="f3e3e-105">返回值</span><span class="sxs-lookup"><span data-stu-id="f3e3e-105">Return Value</span></span>  
  
|<span data-ttu-id="f3e3e-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f3e3e-106">HRESULT</span></span>|<span data-ttu-id="f3e3e-107">说明</span><span class="sxs-lookup"><span data-stu-id="f3e3e-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f3e3e-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3e3e-108">S_OK</span></span>|<span data-ttu-id="f3e3e-109">`Set` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-109">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="f3e3e-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3e3e-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f3e3e-111"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f3e3e-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f3e3e-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f3e3e-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-113">The call timed out.</span></span>|  
|<span data-ttu-id="f3e3e-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f3e3e-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f3e3e-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f3e3e-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f3e3e-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f3e3e-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f3e3e-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3e3e-118">E_FAIL</span></span>|<span data-ttu-id="f3e3e-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f3e3e-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f3e3e-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f3e3e-122">要求</span><span class="sxs-lookup"><span data-stu-id="f3e3e-122">Requirements</span></span>  

 <span data-ttu-id="f3e3e-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f3e3e-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3e3e-124">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f3e3e-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3e3e-125">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3e3e-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3e3e-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3e3e-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3e3e-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3e3e-127">See also</span></span>

- [<span data-ttu-id="f3e3e-128">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f3e3e-128">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="f3e3e-129">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="f3e3e-129">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="f3e3e-130">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="f3e3e-130">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="f3e3e-131">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f3e3e-131">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
