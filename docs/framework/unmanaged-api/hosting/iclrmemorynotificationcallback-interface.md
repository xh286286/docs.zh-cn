---
title: ICLRMemoryNotificationCallback 接口
ms.date: 03/30/2017
api_name:
- ICLRMemoryNotificationCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMemoryNotificationCallback
helpviewer_keywords:
- ICLRMemoryNotificationCallback interface [.NET Framework hosting]
ms.assetid: 873639e2-4837-4568-83b3-4493e67e4174
topic_type:
- apiref
ms.openlocfilehash: 5762a354bec485cb382b5460dfd2a337f79bee1a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689532"
---
# <a name="iclrmemorynotificationcallback-interface"></a><span data-ttu-id="eec4d-102">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="eec4d-102">ICLRMemoryNotificationCallback Interface</span></span>

<span data-ttu-id="eec4d-103">允许主机使用类似于 Win32 函数的方法来报告内存压力情况 `CreateMemoryResourceNotification` 。</span><span class="sxs-lookup"><span data-stu-id="eec4d-103">Allows the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="eec4d-104">方法</span><span class="sxs-lookup"><span data-stu-id="eec4d-104">Methods</span></span>  
  
|<span data-ttu-id="eec4d-105">方法</span><span class="sxs-lookup"><span data-stu-id="eec4d-105">Method</span></span>|<span data-ttu-id="eec4d-106">说明</span><span class="sxs-lookup"><span data-stu-id="eec4d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="eec4d-107">OnMemoryNotification 方法</span><span class="sxs-lookup"><span data-stu-id="eec4d-107">OnMemoryNotification Method</span></span>](iclrmemorynotificationcallback-onmemorynotification-method.md)|<span data-ttu-id="eec4d-108"> (CLR) 计算机上的内存负载通知公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="eec4d-108">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eec4d-109">注解</span><span class="sxs-lookup"><span data-stu-id="eec4d-109">Remarks</span></span>  

 <span data-ttu-id="eec4d-110">主机使用 `ICLRMemoryNotificationCallback` 接口请求 CLR 释放内存资源。</span><span class="sxs-lookup"><span data-stu-id="eec4d-110">The host uses the `ICLRMemoryNotificationCallback` interface to request that the CLR free memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eec4d-111">要求</span><span class="sxs-lookup"><span data-stu-id="eec4d-111">Requirements</span></span>  

 <span data-ttu-id="eec4d-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eec4d-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eec4d-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="eec4d-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="eec4d-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="eec4d-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="eec4d-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eec4d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eec4d-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eec4d-116">See also</span></span>

- [<span data-ttu-id="eec4d-117">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="eec4d-117">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="eec4d-118">承载接口</span><span class="sxs-lookup"><span data-stu-id="eec4d-118">Hosting Interfaces</span></span>](hosting-interfaces.md)
