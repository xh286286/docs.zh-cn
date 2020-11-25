---
title: ICLRPolicyManager::SetTimeout 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetTimeout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetTimeout
helpviewer_keywords:
- SetTimeout method [.NET Framework hosting]
- ICLRPolicyManager::SetTimeout method [.NET Framework hosting]
ms.assetid: 954404fd-d52d-4e68-b582-8692f3a5f608
topic_type:
- apiref
ms.openlocfilehash: 459c5bc0699487b62d5dcf76f1044faf53ebab8b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732458"
---
# <a name="iclrpolicymanagersettimeout-method"></a><span data-ttu-id="71b43-102">ICLRPolicyManager::SetTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="71b43-102">ICLRPolicyManager::SetTimeout Method</span></span>

<span data-ttu-id="71b43-103">设置指定操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="71b43-103">Sets a timeout value for the specified operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71b43-104">语法</span><span class="sxs-lookup"><span data-stu-id="71b43-104">Syntax</span></span>  
  
```cpp  
HRESULT SetTimeout (  
    [in] EClrOperation operation,  
    [in] DWORD dsMilliseconds  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="71b43-105">参数</span><span class="sxs-lookup"><span data-stu-id="71b43-105">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="71b43-106">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示公共语言运行时 (CLR) 操作设置超时。</span><span class="sxs-lookup"><span data-stu-id="71b43-106">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the common language runtime (CLR) operation for which to set a timeout.</span></span> <span data-ttu-id="71b43-107">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="71b43-107">The following values are supported:</span></span>  
  
- <span data-ttu-id="71b43-108">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="71b43-108">OPR_AppDomainUnload</span></span>  
  
- <span data-ttu-id="71b43-109">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="71b43-109">OPR_ProcessExit</span></span>  
  
- <span data-ttu-id="71b43-110">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="71b43-110">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
- <span data-ttu-id="71b43-111">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="71b43-111">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `dwMilliseconds`  
 <span data-ttu-id="71b43-112">中新的超时值（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="71b43-112">[in] The new timeout value, in milliseconds.</span></span> <span data-ttu-id="71b43-113">如果值为 "无限"，则操作永远不会超时。</span><span class="sxs-lookup"><span data-stu-id="71b43-113">A value of INFINITE causes the operation never to time out.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="71b43-114">返回值</span><span class="sxs-lookup"><span data-stu-id="71b43-114">Return Value</span></span>  
  
|<span data-ttu-id="71b43-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="71b43-115">HRESULT</span></span>|<span data-ttu-id="71b43-116">说明</span><span class="sxs-lookup"><span data-stu-id="71b43-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="71b43-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="71b43-117">S_OK</span></span>|<span data-ttu-id="71b43-118">`SetTimeout` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="71b43-118">`SetTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="71b43-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="71b43-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="71b43-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="71b43-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="71b43-121">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="71b43-121">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="71b43-122">调用超时。</span><span class="sxs-lookup"><span data-stu-id="71b43-122">The call timed out.</span></span>|  
|<span data-ttu-id="71b43-123">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="71b43-123">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="71b43-124">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="71b43-124">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="71b43-125">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="71b43-125">HOST_E_ABANDONED</span></span>|<span data-ttu-id="71b43-126">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="71b43-126">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="71b43-127">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="71b43-127">E_FAIL</span></span>|<span data-ttu-id="71b43-128">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="71b43-128">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="71b43-129">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="71b43-129">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="71b43-130">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="71b43-130">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="71b43-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="71b43-131">E_INVALIDARG</span></span>|<span data-ttu-id="71b43-132">无法为指定的设置超时 `operation` ，或者为提供的值无效 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="71b43-132">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="71b43-133">要求</span><span class="sxs-lookup"><span data-stu-id="71b43-133">Requirements</span></span>  

 <span data-ttu-id="71b43-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="71b43-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71b43-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="71b43-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="71b43-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="71b43-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="71b43-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71b43-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71b43-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71b43-138">See also</span></span>

- [<span data-ttu-id="71b43-139">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="71b43-139">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="71b43-140">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="71b43-140">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="71b43-141">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="71b43-141">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
