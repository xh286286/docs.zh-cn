---
title: ICLRErrorReportingManager::EndCustomDump 方法
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.EndCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::EndCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::EndCustomDump method [.NET Framework hosting]
- EndCustomDump method [.NET Framework hosting]
ms.assetid: 88a5da04-8729-4108-82c4-af206a7d483e
topic_type:
- apiref
ms.openlocfilehash: feaeba15fcc4e8264f7fde57d3b268a6b583ad83
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677825"
---
# <a name="iclrerrorreportingmanagerendcustomdump-method"></a><span data-ttu-id="ae887-102">ICLRErrorReportingManager::EndCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="ae887-102">ICLRErrorReportingManager::EndCustomDump Method</span></span>

<span data-ttu-id="ae887-103">删除在先前对 [ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 方法的调用中指定的自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="ae887-103">Removes the custom stack dump configuration that was specified in an earlier call to the [ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae887-104">语法</span><span class="sxs-lookup"><span data-stu-id="ae887-104">Syntax</span></span>  
  
```cpp  
HRESULT EndCustomDump ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ae887-105">返回值</span><span class="sxs-lookup"><span data-stu-id="ae887-105">Return Value</span></span>  
  
|<span data-ttu-id="ae887-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ae887-106">HRESULT</span></span>|<span data-ttu-id="ae887-107">说明</span><span class="sxs-lookup"><span data-stu-id="ae887-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ae887-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae887-108">S_OK</span></span>|<span data-ttu-id="ae887-109">`EndCustomDump` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ae887-109">`EndCustomDump` returned successfully.</span></span>|  
|<span data-ttu-id="ae887-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae887-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ae887-111"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ae887-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ae887-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ae887-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ae887-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ae887-113">The call timed out.</span></span>|  
|<span data-ttu-id="ae887-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ae887-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ae887-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ae887-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ae887-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ae887-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ae887-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ae887-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ae887-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae887-118">E_FAIL</span></span>|<span data-ttu-id="ae887-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ae887-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ae887-120">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ae887-120">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ae887-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ae887-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae887-122">注解</span><span class="sxs-lookup"><span data-stu-id="ae887-122">Remarks</span></span>  

 <span data-ttu-id="ae887-123">`EndCustomDump`方法通过对方法的更早调用来清除自定义堆栈转储配置 `BeginCustomDump` ，并释放任何关联的状态。</span><span class="sxs-lookup"><span data-stu-id="ae887-123">The `EndCustomDump` method clears the custom stack dump configuration set by an earlier call to the `BeginCustomDump` method and frees any associated state.</span></span> <span data-ttu-id="ae887-124">应在自定义堆栈转储完成后调用它。</span><span class="sxs-lookup"><span data-stu-id="ae887-124">It should be called after the custom stack dump is complete.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="ae887-125">调用失败 `EndCustomDump` 会导致内存泄露。</span><span class="sxs-lookup"><span data-stu-id="ae887-125">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae887-126">要求</span><span class="sxs-lookup"><span data-stu-id="ae887-126">Requirements</span></span>  

 <span data-ttu-id="ae887-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae887-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae887-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ae887-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ae887-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae887-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ae887-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae887-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae887-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae887-131">See also</span></span>

- [<span data-ttu-id="ae887-132">CustomDumpItem 结构</span><span class="sxs-lookup"><span data-stu-id="ae887-132">CustomDumpItem Structure</span></span>](customdumpitem-structure.md)
- [<span data-ttu-id="ae887-133">ECustomDumpFlavor 枚举</span><span class="sxs-lookup"><span data-stu-id="ae887-133">ECustomDumpFlavor Enumeration</span></span>](ecustomdumpflavor-enumeration.md)
- [<span data-ttu-id="ae887-134">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="ae887-134">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
