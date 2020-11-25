---
title: IHostSecurityManager::ImpersonateLoggedOnUser 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.ImpersonateLoggedOnUser
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::ImpersonateLoggedOnUser
helpviewer_keywords:
- ImpersonateLoggedOnUser method [.NET Framework hosting]
- IHostSecurityManager::ImpersonateLoggedOnUser method [.NET Framework hosting]
ms.assetid: acc49ba0-f1d9-45ad-871f-9d053a89dcbe
topic_type:
- apiref
ms.openlocfilehash: dd1d1af8072ac11e37bd2eb1a47d76b12685cb31
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724775"
---
# <a name="ihostsecuritymanagerimpersonateloggedonuser-method"></a><span data-ttu-id="6d51b-102">IHostSecurityManager::ImpersonateLoggedOnUser 方法</span><span class="sxs-lookup"><span data-stu-id="6d51b-102">IHostSecurityManager::ImpersonateLoggedOnUser Method</span></span>

<span data-ttu-id="6d51b-103">请求使用当前用户标识的凭据执行代码。</span><span class="sxs-lookup"><span data-stu-id="6d51b-103">Requests that code be executed using the credentials of the current user identity.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d51b-104">语法</span><span class="sxs-lookup"><span data-stu-id="6d51b-104">Syntax</span></span>  
  
```cpp  
HRESULT ImpersonateLoggedOnUser (  
    [in] HANDLE hToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6d51b-105">参数</span><span class="sxs-lookup"><span data-stu-id="6d51b-105">Parameters</span></span>  

 `hToken`  
 <span data-ttu-id="6d51b-106">中一个标记，表示要模拟的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="6d51b-106">[in] A token representing the credentials of the user to be impersonated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6d51b-107">返回值</span><span class="sxs-lookup"><span data-stu-id="6d51b-107">Return Value</span></span>  
  
|<span data-ttu-id="6d51b-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6d51b-108">HRESULT</span></span>|<span data-ttu-id="6d51b-109">说明</span><span class="sxs-lookup"><span data-stu-id="6d51b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6d51b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d51b-110">S_OK</span></span>|<span data-ttu-id="6d51b-111">`ImpersonateLoggedOnUser` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6d51b-111">`ImpersonateLoggedOnUser` returned successfully.</span></span>|  
|<span data-ttu-id="6d51b-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6d51b-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6d51b-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6d51b-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6d51b-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6d51b-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6d51b-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6d51b-115">The call timed out.</span></span>|  
|<span data-ttu-id="6d51b-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6d51b-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6d51b-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6d51b-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6d51b-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6d51b-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6d51b-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6d51b-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6d51b-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6d51b-120">E_FAIL</span></span>|<span data-ttu-id="6d51b-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6d51b-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6d51b-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6d51b-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6d51b-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6d51b-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6d51b-124">注解</span><span class="sxs-lookup"><span data-stu-id="6d51b-124">Remarks</span></span>  

 <span data-ttu-id="6d51b-125">调用 `LogonUser` 或相关的 Win32 函数获取当前用户标识的凭据的句柄。</span><span class="sxs-lookup"><span data-stu-id="6d51b-125">Call `LogonUser` or a related Win32 function to get a handle to the credentials of the current user identity.</span></span>  
  
 <span data-ttu-id="6d51b-126">`HANDLE`类型不符合 COM 要求，也就是说，其大小特定于操作系统，并需要自定义封送处理。</span><span class="sxs-lookup"><span data-stu-id="6d51b-126">The `HANDLE` type is not COM-compliant, that is, its size is specific to an operating system, and it requires custom marshaling.</span></span> <span data-ttu-id="6d51b-127">因此，此令牌仅在该进程内的 CLR 和主机之间使用。</span><span class="sxs-lookup"><span data-stu-id="6d51b-127">Thus, this token is for use only within the process, between the CLR and the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d51b-128">要求</span><span class="sxs-lookup"><span data-stu-id="6d51b-128">Requirements</span></span>  

 <span data-ttu-id="6d51b-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6d51b-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d51b-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6d51b-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6d51b-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6d51b-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6d51b-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d51b-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d51b-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6d51b-133">See also</span></span>

- [<span data-ttu-id="6d51b-134">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="6d51b-134">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="6d51b-135">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="6d51b-135">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="6d51b-136">RevertToSelf 方法</span><span class="sxs-lookup"><span data-stu-id="6d51b-136">RevertToSelf Method</span></span>](ihostsecuritymanager-reverttoself-method.md)
