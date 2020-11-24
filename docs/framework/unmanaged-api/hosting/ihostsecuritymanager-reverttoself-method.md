---
title: IHostSecurityManager::RevertToSelf 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.RevertToSelf
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::RevertToSelf
helpviewer_keywords:
- RevertToSelf method [.NET Framework hosting]
- IHostSecurityManager::RevertToSelf method [.NET Framework hosting]
ms.assetid: 189f28f8-f9a1-4192-aedc-91084e4f8b99
topic_type:
- apiref
ms.openlocfilehash: a54c25cb0cae906dc2d030900b9a1e1dbbbb2f1e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680516"
---
# <a name="ihostsecuritymanagerreverttoself-method"></a><span data-ttu-id="c3cf0-102">IHostSecurityManager::RevertToSelf 方法</span><span class="sxs-lookup"><span data-stu-id="c3cf0-102">IHostSecurityManager::RevertToSelf Method</span></span>

<span data-ttu-id="c3cf0-103">终止当前用户标识的模拟并返回原始线程标记。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-103">Terminates impersonation of the current user identity and returns the original thread token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3cf0-104">语法</span><span class="sxs-lookup"><span data-stu-id="c3cf0-104">Syntax</span></span>  
  
```cpp  
HRESULT RevertToSelf ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c3cf0-105">返回值</span><span class="sxs-lookup"><span data-stu-id="c3cf0-105">Return Value</span></span>  
  
|<span data-ttu-id="c3cf0-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c3cf0-106">HRESULT</span></span>|<span data-ttu-id="c3cf0-107">说明</span><span class="sxs-lookup"><span data-stu-id="c3cf0-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c3cf0-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3cf0-108">S_OK</span></span>|<span data-ttu-id="c3cf0-109">`RevertToSelf` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-109">`RevertToSelf` returned successfully.</span></span>|  
|<span data-ttu-id="c3cf0-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c3cf0-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c3cf0-111"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c3cf0-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c3cf0-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c3cf0-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-113">The call timed out.</span></span>|  
|<span data-ttu-id="c3cf0-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c3cf0-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c3cf0-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c3cf0-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c3cf0-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c3cf0-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c3cf0-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c3cf0-118">E_FAIL</span></span>|<span data-ttu-id="c3cf0-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c3cf0-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c3cf0-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c3cf0-122">注解</span><span class="sxs-lookup"><span data-stu-id="c3cf0-122">Remarks</span></span>  

 <span data-ttu-id="c3cf0-123">`RevertToSelf` 调用 [ImpersonateLoggedOnUser](ihostsecuritymanager-impersonateloggedonuser-method.md) 方法后，将调用以返回到原始线程标记。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-123">`RevertToSelf` is called to return to the original thread token, after an earlier call to the [ImpersonateLoggedOnUser](ihostsecuritymanager-impersonateloggedonuser-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3cf0-124">要求</span><span class="sxs-lookup"><span data-stu-id="c3cf0-124">Requirements</span></span>  

 <span data-ttu-id="c3cf0-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3cf0-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c3cf0-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c3cf0-127">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c3cf0-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c3cf0-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3cf0-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3cf0-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c3cf0-129">See also</span></span>

- [<span data-ttu-id="c3cf0-130">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="c3cf0-130">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="c3cf0-131">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="c3cf0-131">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="c3cf0-132">ImpersonateLoggedOnUser 方法</span><span class="sxs-lookup"><span data-stu-id="c3cf0-132">ImpersonateLoggedOnUser Method</span></span>](ihostsecuritymanager-impersonateloggedonuser-method.md)
