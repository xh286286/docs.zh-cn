---
title: IHostCrst::Enter 方法
ms.date: 03/30/2017
api_name:
- IHostCrst.Enter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::Enter
helpviewer_keywords:
- Enter method [.NET Framework hosting]
- IHostCrst::Enter method [.NET Framework hosting]
ms.assetid: 100dd7eb-7053-4295-9bb3-32ba47f6ec79
topic_type:
- apiref
ms.openlocfilehash: a5c2646d7c9dbf8a7aea4a7fb9bd0a6b8c1d5d66
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680542"
---
# <a name="ihostcrstenter-method"></a><span data-ttu-id="34b22-102">IHostCrst::Enter 方法</span><span class="sxs-lookup"><span data-stu-id="34b22-102">IHostCrst::Enter Method</span></span>

<span data-ttu-id="34b22-103">输入当前 [IHostCrst](ihostcrst-interface.md) 实例所表示的临界区。</span><span class="sxs-lookup"><span data-stu-id="34b22-103">Enters the critical section that is represented by the current [IHostCrst](ihostcrst-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34b22-104">语法</span><span class="sxs-lookup"><span data-stu-id="34b22-104">Syntax</span></span>  
  
```cpp  
HRESULT Enter (  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="34b22-105">参数</span><span class="sxs-lookup"><span data-stu-id="34b22-105">Parameters</span></span>  

 `option`  
 <span data-ttu-id="34b22-106">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指示在操作阻止时主机应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="34b22-106">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, indicating what action the host should take if the operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="34b22-107">返回值</span><span class="sxs-lookup"><span data-stu-id="34b22-107">Return Value</span></span>  
  
|<span data-ttu-id="34b22-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="34b22-108">HRESULT</span></span>|<span data-ttu-id="34b22-109">说明</span><span class="sxs-lookup"><span data-stu-id="34b22-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="34b22-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="34b22-110">S_OK</span></span>|<span data-ttu-id="34b22-111">`Enter` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="34b22-111">`Enter` returned successfully.</span></span>|  
|<span data-ttu-id="34b22-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="34b22-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="34b22-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="34b22-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="34b22-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="34b22-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="34b22-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="34b22-115">The call timed out.</span></span>|  
|<span data-ttu-id="34b22-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="34b22-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="34b22-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="34b22-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="34b22-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="34b22-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="34b22-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="34b22-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="34b22-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="34b22-120">E_FAIL</span></span>|<span data-ttu-id="34b22-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="34b22-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="34b22-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="34b22-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="34b22-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="34b22-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="34b22-124">注解</span><span class="sxs-lookup"><span data-stu-id="34b22-124">Remarks</span></span>  

 <span data-ttu-id="34b22-125">`Enter` 对 Win32 函数进行镜像 `EnterCriticalSection` 。</span><span class="sxs-lookup"><span data-stu-id="34b22-125">`Enter` mirrors the Win32 `EnterCriticalSection` function.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="34b22-126">直到进入临界区，此方法才会返回。</span><span class="sxs-lookup"><span data-stu-id="34b22-126">This method does not return until the critical section is entered.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34b22-127">要求</span><span class="sxs-lookup"><span data-stu-id="34b22-127">Requirements</span></span>  

 <span data-ttu-id="34b22-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="34b22-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34b22-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="34b22-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="34b22-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="34b22-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="34b22-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34b22-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34b22-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34b22-132">See also</span></span>

- [<span data-ttu-id="34b22-133">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="34b22-133">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="34b22-134">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="34b22-134">IHostCrst Interface</span></span>](ihostcrst-interface.md)
- [<span data-ttu-id="34b22-135">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="34b22-135">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
