---
title: ICLRIoCompletionManager 接口
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
ms.openlocfilehash: e23675351e1fd0de510243c9ee8b3a6dd6f29cec
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714115"
---
# <a name="iclriocompletionmanager-interface"></a><span data-ttu-id="a39a8-102">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="a39a8-102">ICLRIoCompletionManager Interface</span></span>

<span data-ttu-id="a39a8-103">实现一个回调方法，该方法允许宿主通知公共语言运行时 (CLR) 指定 i/o 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="a39a8-103">Implements a callback method that allows the host to notify the common language runtime (CLR) of the status of specified I/O requests.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a39a8-104">方法</span><span class="sxs-lookup"><span data-stu-id="a39a8-104">Methods</span></span>  
  
|<span data-ttu-id="a39a8-105">方法</span><span class="sxs-lookup"><span data-stu-id="a39a8-105">Method</span></span>|<span data-ttu-id="a39a8-106">说明</span><span class="sxs-lookup"><span data-stu-id="a39a8-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a39a8-107">OnComplete 方法</span><span class="sxs-lookup"><span data-stu-id="a39a8-107">OnComplete Method</span></span>](iclriocompletionmanager-oncomplete-method.md)|<span data-ttu-id="a39a8-108">使用对 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法的调用，将发出的 i/o 请求状态通知给 CLR。</span><span class="sxs-lookup"><span data-stu-id="a39a8-108">Notifies the CLR of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](ihostiocompletionmanager-bind-method.md) method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a39a8-109">注解</span><span class="sxs-lookup"><span data-stu-id="a39a8-109">Remarks</span></span>  

 <span data-ttu-id="a39a8-110">宿主通过使用 [IHostIoCompletionManager](ihostiocompletionmanager-interface.md) 接口实现 i/o 完成抽象。</span><span class="sxs-lookup"><span data-stu-id="a39a8-110">The host implements the I/O completion abstraction by using the [IHostIoCompletionManager](ihostiocompletionmanager-interface.md) interface.</span></span> <span data-ttu-id="a39a8-111">CLR 通过此接口发出 i/o 请求，主机使用接口通知运行时此类请求的结果 `ICLRIoCompletionManager` 。</span><span class="sxs-lookup"><span data-stu-id="a39a8-111">The CLR makes I/O requests through this interface, and the host notifies the runtime of the outcome of such requests by using the `ICLRIoCompletionManager` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a39a8-112">要求</span><span class="sxs-lookup"><span data-stu-id="a39a8-112">Requirements</span></span>  

 <span data-ttu-id="a39a8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a39a8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a39a8-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a39a8-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a39a8-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a39a8-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a39a8-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a39a8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a39a8-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a39a8-117">See also</span></span>

- [<span data-ttu-id="a39a8-118">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="a39a8-118">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="a39a8-119">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="a39a8-119">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
- [<span data-ttu-id="a39a8-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="a39a8-120">Hosting Interfaces</span></span>](hosting-interfaces.md)
