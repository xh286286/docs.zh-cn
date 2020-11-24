---
title: IHostCrst 接口
ms.date: 03/30/2017
api_name:
- IHostCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst
helpviewer_keywords:
- IHostCrst interface [.NET Framework hosting]
ms.assetid: ac298ebd-0815-47e4-a823-30b31baab903
topic_type:
- apiref
ms.openlocfilehash: 350af708456914c73929d2b8887173cf784d4294
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680548"
---
# <a name="ihostcrst-interface"></a><span data-ttu-id="b36f1-102">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="b36f1-102">IHostCrst Interface</span></span>

<span data-ttu-id="b36f1-103">用作线程的关键部分的宿主表示形式。</span><span class="sxs-lookup"><span data-stu-id="b36f1-103">Serves as the host's representation of a critical section for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b36f1-104">方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-104">Methods</span></span>  
  
|<span data-ttu-id="b36f1-105">方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-105">Method</span></span>|<span data-ttu-id="b36f1-106">说明</span><span class="sxs-lookup"><span data-stu-id="b36f1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b36f1-107">Enter 方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-107">Enter Method</span></span>](ihostcrst-enter-method.md)|<span data-ttu-id="b36f1-108">输入临界区。</span><span class="sxs-lookup"><span data-stu-id="b36f1-108">Enters the critical section.</span></span>|  
|[<span data-ttu-id="b36f1-109">Leave 方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-109">Leave Method</span></span>](ihostcrst-leave-method.md)|<span data-ttu-id="b36f1-110">离开临界区。</span><span class="sxs-lookup"><span data-stu-id="b36f1-110">Leaves the critical section.</span></span>|  
|[<span data-ttu-id="b36f1-111">SetSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-111">SetSpinCount Method</span></span>](ihostcrst-setspincount-method.md)|<span data-ttu-id="b36f1-112">设置临界区的旋转计数。</span><span class="sxs-lookup"><span data-stu-id="b36f1-112">Sets the spin count for the critical section.</span></span>|  
|[<span data-ttu-id="b36f1-113">TryEnter 方法</span><span class="sxs-lookup"><span data-stu-id="b36f1-113">TryEnter Method</span></span>](ihostcrst-tryenter-method.md)|<span data-ttu-id="b36f1-114">尝试输入临界区，并立即报告成功或失败。</span><span class="sxs-lookup"><span data-stu-id="b36f1-114">Attempts to enter the critical section, and reports success or failure immediately.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b36f1-115">注解</span><span class="sxs-lookup"><span data-stu-id="b36f1-115">Remarks</span></span>  

 <span data-ttu-id="b36f1-116">`IHostCrst` 允许公共语言运行时 (CLR) 直接与关键节的主机表示形式进行通信，而不是使用或等 Win32 函数 `EnterCriticalSection` `LeaveCriticalSection` 。</span><span class="sxs-lookup"><span data-stu-id="b36f1-116">`IHostCrst` allows the common language runtime (CLR) to communicate directly with the host's representation of a critical section, rather than using Win32 functions such as `EnterCriticalSection` or `LeaveCriticalSection`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b36f1-117">要求</span><span class="sxs-lookup"><span data-stu-id="b36f1-117">Requirements</span></span>  

 <span data-ttu-id="b36f1-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b36f1-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b36f1-119">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b36f1-119">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b36f1-120">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b36f1-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b36f1-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b36f1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b36f1-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b36f1-122">See also</span></span>

- [<span data-ttu-id="b36f1-123">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b36f1-123">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="b36f1-124">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b36f1-124">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="b36f1-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="b36f1-125">Hosting Interfaces</span></span>](hosting-interfaces.md)
