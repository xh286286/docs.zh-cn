---
title: ICLRTaskManager::SetUILocale 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::SetUILocale
helpviewer_keywords:
- ICLRTaskManager::SetUILocale method [.NET Framework hosting]
- SetUILocale method, ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 03adaa9a-2beb-49b3-b2c4-6b4fc3f10715
topic_type:
- apiref
ms.openlocfilehash: a426fca1b7ca4bfb9cbb30a221859f7c114db682
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732419"
---
# <a name="iclrtaskmanagersetuilocale-method"></a><span data-ttu-id="d0322-102">ICLRTaskManager::SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="d0322-102">ICLRTaskManager::SetUILocale Method</span></span>

<span data-ttu-id="d0322-103">通知公共语言运行时 (CLR) 宿主已修改当前正在执行的任务的用户界面 (UI) 区域设置或区域性）。</span><span class="sxs-lookup"><span data-stu-id="d0322-103">Notifies the common language runtime (CLR) that the host has modified the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0322-104">语法</span><span class="sxs-lookup"><span data-stu-id="d0322-104">Syntax</span></span>  
  
```cpp  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0322-105">参数</span><span class="sxs-lookup"><span data-stu-id="d0322-105">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="d0322-106">中区域设置标识符值，用于映射到新分配的用户界面的地理区域和语言。</span><span class="sxs-lookup"><span data-stu-id="d0322-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language for the user interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d0322-107">返回值</span><span class="sxs-lookup"><span data-stu-id="d0322-107">Return Value</span></span>  
  
|<span data-ttu-id="d0322-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0322-108">HRESULT</span></span>|<span data-ttu-id="d0322-109">说明</span><span class="sxs-lookup"><span data-stu-id="d0322-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d0322-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0322-110">S_OK</span></span>|<span data-ttu-id="d0322-111">`SetUILocale` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d0322-111">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="d0322-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d0322-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d0322-113">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d0322-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d0322-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d0322-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d0322-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d0322-115">The call timed out.</span></span>|  
|<span data-ttu-id="d0322-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d0322-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d0322-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d0322-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d0322-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d0322-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d0322-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d0322-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d0322-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d0322-120">E_FAIL</span></span>|<span data-ttu-id="d0322-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d0322-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d0322-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d0322-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d0322-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d0322-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d0322-124">注解</span><span class="sxs-lookup"><span data-stu-id="d0322-124">Remarks</span></span>  

 <span data-ttu-id="d0322-125">`SetUILocale` 为宿主提供对区域设置同步所需的任何机制的机会。</span><span class="sxs-lookup"><span data-stu-id="d0322-125">`SetUILocale` provides an opportunity for the host to execute any mechanisms it might have for the synchronization of locales.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0322-126">要求</span><span class="sxs-lookup"><span data-stu-id="d0322-126">Requirements</span></span>  

 <span data-ttu-id="d0322-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0322-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0322-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d0322-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d0322-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d0322-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d0322-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0322-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0322-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0322-131">See also</span></span>

- [<span data-ttu-id="d0322-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="d0322-132">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="d0322-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d0322-133">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="d0322-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="d0322-134">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="d0322-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d0322-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
