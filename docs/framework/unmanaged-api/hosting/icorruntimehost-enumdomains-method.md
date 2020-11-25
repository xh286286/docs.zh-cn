---
title: ICorRuntimeHost::EnumDomains 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.EnumDomains
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::EnumDomains
helpviewer_keywords:
- ICorRuntimeHost::EnumDomains method [.NET Framework hosting]
- EnumDomains method [.NET Framework hosting]
ms.assetid: 96b74995-0cde-4876-b6df-7fc164e6a5d1
topic_type:
- apiref
ms.openlocfilehash: f4338429dc24bf5196b92d3f18e73c98442f61e7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720657"
---
# <a name="icorruntimehostenumdomains-method"></a><span data-ttu-id="9024b-102">ICorRuntimeHost::EnumDomains 方法</span><span class="sxs-lookup"><span data-stu-id="9024b-102">ICorRuntimeHost::EnumDomains Method</span></span>

<span data-ttu-id="9024b-103">获取当前进程中的域的枚举数。</span><span class="sxs-lookup"><span data-stu-id="9024b-103">Gets an enumerator for the domains in the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9024b-104">语法</span><span class="sxs-lookup"><span data-stu-id="9024b-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumDomains (  
    [out] HCORENUM *hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9024b-105">参数</span><span class="sxs-lookup"><span data-stu-id="9024b-105">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="9024b-106">弄域的枚举数。</span><span class="sxs-lookup"><span data-stu-id="9024b-106">[out] An enumerator for the domains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9024b-107">返回值</span><span class="sxs-lookup"><span data-stu-id="9024b-107">Return Value</span></span>  
  
|<span data-ttu-id="9024b-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9024b-108">HRESULT</span></span>|<span data-ttu-id="9024b-109">说明</span><span class="sxs-lookup"><span data-stu-id="9024b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9024b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9024b-110">S_OK</span></span>|<span data-ttu-id="9024b-111">操作成功。</span><span class="sxs-lookup"><span data-stu-id="9024b-111">The operation was successful.</span></span>|  
|<span data-ttu-id="9024b-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9024b-112">S_FALSE</span></span>|<span data-ttu-id="9024b-113">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="9024b-113">The operation failed to complete.</span></span>|  
|<span data-ttu-id="9024b-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9024b-114">E_FAIL</span></span>|<span data-ttu-id="9024b-115">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="9024b-115">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="9024b-116">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="9024b-116">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="9024b-117">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="9024b-117">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="9024b-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9024b-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9024b-119">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="9024b-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9024b-120">要求</span><span class="sxs-lookup"><span data-stu-id="9024b-120">Requirements</span></span>  

 <span data-ttu-id="9024b-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9024b-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9024b-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9024b-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9024b-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9024b-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9024b-124">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="9024b-124">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9024b-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9024b-125">See also</span></span>

- [<span data-ttu-id="9024b-126">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="9024b-126">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
