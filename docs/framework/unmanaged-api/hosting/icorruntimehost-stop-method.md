---
title: ICorRuntimeHost::Stop 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.Stop
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::Stop
helpviewer_keywords:
- Stop method, ICorRuntimeHost interface [.NET Framework hosting]
- ICorRuntimeHost::Stop method [.NET Framework hosting]
ms.assetid: 46a0d450-b516-4bef-8b71-8d3bf265cbed
topic_type:
- apiref
ms.openlocfilehash: 9342233317535ebecbcddea48b9029b81868eb0c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690143"
---
# <a name="icorruntimehoststop-method"></a><span data-ttu-id="d1b9b-102">ICorRuntimeHost::Stop 方法</span><span class="sxs-lookup"><span data-stu-id="d1b9b-102">ICorRuntimeHost::Stop Method</span></span>

<span data-ttu-id="d1b9b-103">停止执行当前进程的运行时中的代码。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-103">Stops the execution of code in the runtime for the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1b9b-104">语法</span><span class="sxs-lookup"><span data-stu-id="d1b9b-104">Syntax</span></span>  
  
```cpp  
HRESULT Stop ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="d1b9b-105">返回值</span><span class="sxs-lookup"><span data-stu-id="d1b9b-105">Return Value</span></span>  
  
|<span data-ttu-id="d1b9b-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1b9b-106">HRESULT</span></span>|<span data-ttu-id="d1b9b-107">说明</span><span class="sxs-lookup"><span data-stu-id="d1b9b-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d1b9b-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1b9b-108">S_OK</span></span>|<span data-ttu-id="d1b9b-109">操作成功。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-109">The operation was successful.</span></span>|  
|<span data-ttu-id="d1b9b-110">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d1b9b-110">S_FALSE</span></span>|<span data-ttu-id="d1b9b-111">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-111">The operation failed to complete.</span></span>|  
|<span data-ttu-id="d1b9b-112">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d1b9b-112">E_FAIL</span></span>|<span data-ttu-id="d1b9b-113">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-113">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="d1b9b-114">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-114">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="d1b9b-115">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-115">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d1b9b-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d1b9b-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d1b9b-117">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1b9b-118">注解</span><span class="sxs-lookup"><span data-stu-id="d1b9b-118">Remarks</span></span>  

 <span data-ttu-id="d1b9b-119">通常不需要调用 `Stop` 方法，因为在进程退出时代码将停止执行。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-119">It is typically unnecessary to call the `Stop` method, because the code stops executing when the process exits.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d1b9b-120">调用后 `Stop` ，无法将 CLR 重新初始化为同一进程。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-120">After a call to `Stop`, the CLR cannot be reinitialized into the same process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1b9b-121">要求</span><span class="sxs-lookup"><span data-stu-id="d1b9b-121">Requirements</span></span>  

 <span data-ttu-id="d1b9b-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1b9b-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d1b9b-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d1b9b-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d1b9b-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d1b9b-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="d1b9b-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1b9b-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1b9b-126">See also</span></span>

- [<span data-ttu-id="d1b9b-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="d1b9b-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
