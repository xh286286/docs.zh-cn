---
title: ICorRuntimeHost::NextDomain 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.NextDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::NextDomain
helpviewer_keywords:
- ICorRuntimeHost::NextDomain method [.NET Framework hosting]
- NextDomain method [.NET Framework hosting]
ms.assetid: fe07a05b-f6d6-44b5-ab01-b9a6eb15c350
topic_type:
- apiref
ms.openlocfilehash: 598c46d50d7b4a67c1b2c0d844c9b12deb12a428
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671364"
---
# <a name="icorruntimehostnextdomain-method"></a><span data-ttu-id="581f5-102">ICorRuntimeHost::NextDomain 方法</span><span class="sxs-lookup"><span data-stu-id="581f5-102">ICorRuntimeHost::NextDomain Method</span></span>

<span data-ttu-id="581f5-103">获取一个接口指针，该指针指向枚举中的下一个域。</span><span class="sxs-lookup"><span data-stu-id="581f5-103">Gets an interface pointer to the next domain in the enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="581f5-104">语法</span><span class="sxs-lookup"><span data-stu-id="581f5-104">Syntax</span></span>  
  
```cpp  
HRESULT NextDomain (  
    [in] HCORENUM hEnum,  
    [out] void** pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="581f5-105">参数</span><span class="sxs-lookup"><span data-stu-id="581f5-105">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="581f5-106">中通过调用 [EnumDomains](icorruntimehost-enumdomains-method.md)获取的枚举器。</span><span class="sxs-lookup"><span data-stu-id="581f5-106">[in] The enumerator that was obtained through a call to [EnumDomains](icorruntimehost-enumdomains-method.md).</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="581f5-107">弄指向 <xref:System._AppDomain?displayProperty=nameWithType> 表示枚举中下一个域的类型的接口指针; 如果不存在其他域，则为 null。</span><span class="sxs-lookup"><span data-stu-id="581f5-107">[out] An interface pointer to the <xref:System._AppDomain?displayProperty=nameWithType> type that represents the next domain in the enumeration, or null, if no more domains exist.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="581f5-108">返回值</span><span class="sxs-lookup"><span data-stu-id="581f5-108">Return Value</span></span>  
  
|<span data-ttu-id="581f5-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="581f5-109">HRESULT</span></span>|<span data-ttu-id="581f5-110">说明</span><span class="sxs-lookup"><span data-stu-id="581f5-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="581f5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="581f5-111">S_OK</span></span>|<span data-ttu-id="581f5-112">操作成功。</span><span class="sxs-lookup"><span data-stu-id="581f5-112">The operation was successful.</span></span>|  
|<span data-ttu-id="581f5-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="581f5-113">S_FALSE</span></span>|<span data-ttu-id="581f5-114">操作未能完成，或者枚举中没有更多的域。</span><span class="sxs-lookup"><span data-stu-id="581f5-114">The operation failed to complete, or there are no more domains in the enumeration.</span></span>|  
|<span data-ttu-id="581f5-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="581f5-115">E_FAIL</span></span>|<span data-ttu-id="581f5-116">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="581f5-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="581f5-117">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="581f5-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="581f5-118">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="581f5-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="581f5-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="581f5-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="581f5-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="581f5-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="581f5-121">要求</span><span class="sxs-lookup"><span data-stu-id="581f5-121">Requirements</span></span>  

 <span data-ttu-id="581f5-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="581f5-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="581f5-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="581f5-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="581f5-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="581f5-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="581f5-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="581f5-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="581f5-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="581f5-126">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="581f5-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="581f5-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
