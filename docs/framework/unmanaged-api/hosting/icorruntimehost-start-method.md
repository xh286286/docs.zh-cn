---
title: ICorRuntimeHost::Start 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::Start
helpviewer_keywords:
- Start method, ICorRuntimeHost interface [.NET Framework hosting]
- ICorRuntimeHost::Start method [.NET Framework hosting]
ms.assetid: c66f3ac5-6489-484a-9bed-c31b711cee01
topic_type:
- apiref
ms.openlocfilehash: bc647ad025b5e22187b476383ed0128761cb632f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721031"
---
# <a name="icorruntimehoststart-method"></a><span data-ttu-id="c0d1f-102">ICorRuntimeHost::Start 方法</span><span class="sxs-lookup"><span data-stu-id="c0d1f-102">ICorRuntimeHost::Start Method</span></span>

<span data-ttu-id="c0d1f-103"> (CLR) 启动公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-103">Starts the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0d1f-104">语法</span><span class="sxs-lookup"><span data-stu-id="c0d1f-104">Syntax</span></span>  
  
```cpp  
HRESULT Start ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c0d1f-105">返回值</span><span class="sxs-lookup"><span data-stu-id="c0d1f-105">Return Value</span></span>  
  
|<span data-ttu-id="c0d1f-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c0d1f-106">HRESULT</span></span>|<span data-ttu-id="c0d1f-107">说明</span><span class="sxs-lookup"><span data-stu-id="c0d1f-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c0d1f-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0d1f-108">S_OK</span></span>|<span data-ttu-id="c0d1f-109">操作成功。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-109">The operation was successful.</span></span>|  
|<span data-ttu-id="c0d1f-110">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c0d1f-110">S_FALSE</span></span>|<span data-ttu-id="c0d1f-111">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-111">The operation failed to complete.</span></span>|  
|<span data-ttu-id="c0d1f-112">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c0d1f-112">E_FAIL</span></span>|<span data-ttu-id="c0d1f-113">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-113">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="c0d1f-114">如果某个方法返回 E_FAIL，则 CLR 将无法再在进程中使用。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-114">If a method returns E_FAIL, the CLR is no longer usable in the process.</span></span> <span data-ttu-id="c0d1f-115">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-115">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="c0d1f-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c0d1f-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c0d1f-117">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0d1f-118">注解</span><span class="sxs-lookup"><span data-stu-id="c0d1f-118">Remarks</span></span>  

 <span data-ttu-id="c0d1f-119">通常不需要调用 `Start` 方法，因为 CLR 会在首次运行托管代码请求时自动启动。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-119">It is typically not necessary to call the `Start` method, because the CLR starts automatically upon the first request to run managed code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0d1f-120">要求</span><span class="sxs-lookup"><span data-stu-id="c0d1f-120">Requirements</span></span>  

 <span data-ttu-id="c0d1f-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0d1f-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0d1f-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c0d1f-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c0d1f-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0d1f-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c0d1f-124">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="c0d1f-124">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0d1f-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0d1f-125">See also</span></span>

- [<span data-ttu-id="c0d1f-126">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="c0d1f-126">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
