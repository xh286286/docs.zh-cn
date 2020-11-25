---
title: ICLRRuntimeInfo::GetInterface 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetInterface
helpviewer_keywords:
- GetInterface method [.NET Framework hosting]
- ICLRRuntimeInfo::GetInterface method [.NET Framework hosting]
ms.assetid: cc7b0e5b-48c3-4509-8ebb-611ddb1f7ec2
topic_type:
- apiref
ms.openlocfilehash: 192163ed8af680e39f7f3a03aee3f46546bc7450
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732068"
---
# <a name="iclrruntimeinfogetinterface-method"></a><span data-ttu-id="faf4a-102">ICLRRuntimeInfo::GetInterface 方法</span><span class="sxs-lookup"><span data-stu-id="faf4a-102">ICLRRuntimeInfo::GetInterface Method</span></span>

<span data-ttu-id="faf4a-103">将 CLR 加载到当前进程并返回运行时接口指针，如 [ICLRRuntimeHost](iclrruntimehost-interface.md)、 [ICLRStrongName](iclrstrongname-interface.md)和 [IMetaDataDispenserEx](../metadata/imetadatadispenser-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="faf4a-103">Loads the CLR into the current process and returns runtime interface pointers, such as [ICLRRuntimeHost](iclrruntimehost-interface.md), [ICLRStrongName](iclrstrongname-interface.md), and [IMetaDataDispenserEx](../metadata/imetadatadispenser-interface.md).</span></span>  
  
 <span data-ttu-id="faf4a-104">此方法取代 `CorBindTo` [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md) 部分中的所有 \* 函数。</span><span class="sxs-lookup"><span data-stu-id="faf4a-104">This method supersedes all the `CorBindTo`\* functions in the [Deprecated CLR Hosting Functions](deprecated-clr-hosting-functions.md) section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="faf4a-105">语法</span><span class="sxs-lookup"><span data-stu-id="faf4a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetInterface(  
[in]  REFCLSID rclsid,  
[in]  REFIID   riid,  
[out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="faf4a-106">参数</span><span class="sxs-lookup"><span data-stu-id="faf4a-106">Parameters</span></span>  

 `rclsid`  
 <span data-ttu-id="faf4a-107">中Coclass 的 CLSID 接口。</span><span class="sxs-lookup"><span data-stu-id="faf4a-107">[in] The CLSID interface for the coclass.</span></span>  
  
 `riid`  
 <span data-ttu-id="faf4a-108">中所请求的接口的 IID `rclsid` 。</span><span class="sxs-lookup"><span data-stu-id="faf4a-108">[in] The IID of the requested `rclsid` interface.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="faf4a-109">弄指向查询的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="faf4a-109">[out] A pointer to the queried interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="faf4a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="faf4a-110">Return Value</span></span>  

 <span data-ttu-id="faf4a-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="faf4a-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="faf4a-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="faf4a-112">HRESULT</span></span>|<span data-ttu-id="faf4a-113">说明</span><span class="sxs-lookup"><span data-stu-id="faf4a-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="faf4a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="faf4a-114">S_OK</span></span>|<span data-ttu-id="faf4a-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="faf4a-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="faf4a-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="faf4a-116">E_POINTER</span></span>|<span data-ttu-id="faf4a-117">`ppUnk` 为 null。</span><span class="sxs-lookup"><span data-stu-id="faf4a-117">`ppUnk` is null.</span></span>|  
|<span data-ttu-id="faf4a-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="faf4a-118">E_OUTOFMEMORY</span></span>|<span data-ttu-id="faf4a-119">没有足够的内存可用来处理请求。</span><span class="sxs-lookup"><span data-stu-id="faf4a-119">Not enough memory is available to handle the request.</span></span>|  
|<span data-ttu-id="faf4a-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="faf4a-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="faf4a-121">已将其他运行时绑定到旧版 CLR 版本2激活策略。</span><span class="sxs-lookup"><span data-stu-id="faf4a-121">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="faf4a-122">注解</span><span class="sxs-lookup"><span data-stu-id="faf4a-122">Remarks</span></span>  

 <span data-ttu-id="faf4a-123">此方法导致加载但不初始化 CLR。</span><span class="sxs-lookup"><span data-stu-id="faf4a-123">This method causes the CLR to be loaded but not initialized.</span></span>  
  
 <span data-ttu-id="faf4a-124">下表显示了和支持的组合 `rclsid` `riid` 。</span><span class="sxs-lookup"><span data-stu-id="faf4a-124">The following table shows the supported combinations for `rclsid` and `riid`.</span></span>  
  
|`rclsid`|`riid`|  
|--------------|------------|  
|<span data-ttu-id="faf4a-125">CLSID_CorMetaDataDispenser</span><span class="sxs-lookup"><span data-stu-id="faf4a-125">CLSID_CorMetaDataDispenser</span></span>|<span data-ttu-id="faf4a-126">IID_IMetaDataDispenser，IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="faf4a-126">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="faf4a-127">CLSID_CorMetaDataDispenserRuntime</span><span class="sxs-lookup"><span data-stu-id="faf4a-127">CLSID_CorMetaDataDispenserRuntime</span></span>|<span data-ttu-id="faf4a-128">IID_IMetaDataDispenser，IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="faf4a-128">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="faf4a-129">CLSID_CorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="faf4a-129">CLSID_CorRuntimeHost</span></span>|<span data-ttu-id="faf4a-130">IID_ICorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="faf4a-130">IID_ICorRuntimeHost</span></span>|  
|<span data-ttu-id="faf4a-131">CLSID_CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="faf4a-131">CLSID_CLRRuntimeHost</span></span>|<span data-ttu-id="faf4a-132">IID_ICLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="faf4a-132">IID_ICLRRuntimeHost</span></span>|  
|<span data-ttu-id="faf4a-133">CLSID_TypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="faf4a-133">CLSID_TypeNameFactory</span></span>|<span data-ttu-id="faf4a-134">IID_ITypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="faf4a-134">IID_ITypeNameFactory</span></span>|  
|<span data-ttu-id="faf4a-135">CLSID_CLRDebuggingLegacy</span><span class="sxs-lookup"><span data-stu-id="faf4a-135">CLSID_CLRDebuggingLegacy</span></span>|<span data-ttu-id="faf4a-136">IID_ICorDebug</span><span class="sxs-lookup"><span data-stu-id="faf4a-136">IID_ICorDebug</span></span>|  
|||  
|<span data-ttu-id="faf4a-137">CLSID_CLRStrongName</span><span class="sxs-lookup"><span data-stu-id="faf4a-137">CLSID_CLRStrongName</span></span>|<span data-ttu-id="faf4a-138">IID_ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="faf4a-138">IID_ICLRStrongName</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="faf4a-139">要求</span><span class="sxs-lookup"><span data-stu-id="faf4a-139">Requirements</span></span>  

 <span data-ttu-id="faf4a-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="faf4a-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="faf4a-141">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="faf4a-141">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="faf4a-142">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="faf4a-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="faf4a-143">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="faf4a-143">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="faf4a-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="faf4a-144">See also</span></span>

- [<span data-ttu-id="faf4a-145">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="faf4a-145">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="faf4a-146">承载接口</span><span class="sxs-lookup"><span data-stu-id="faf4a-146">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="faf4a-147">承载</span><span class="sxs-lookup"><span data-stu-id="faf4a-147">Hosting</span></span>](index.md)
