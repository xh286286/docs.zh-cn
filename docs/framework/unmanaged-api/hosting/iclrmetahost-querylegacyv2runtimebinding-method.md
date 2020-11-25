---
title: ICLRMetaHost::QueryLegacyV2RuntimeBinding 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.RequestRuntimeLoadedNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::QueryLegacyV2RuntimeBinding
helpviewer_keywords:
- QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
- ICLRMetaHost::QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
ms.assetid: 9929817e-acc9-40b7-960c-598664e04b60
topic_type:
- apiref
ms.openlocfilehash: d65191e515db9c302cef669a824ffd08327faf34
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713985"
---
# <a name="iclrmetahostquerylegacyv2runtimebinding-method"></a><span data-ttu-id="10800-102">ICLRMetaHost::QueryLegacyV2RuntimeBinding 方法</span><span class="sxs-lookup"><span data-stu-id="10800-102">ICLRMetaHost::QueryLegacyV2RuntimeBinding Method</span></span>

<span data-ttu-id="10800-103">返回一个接口，该接口表示已绑定旧式激活策略的运行时，例如，通过使用 `useLegacyV2RuntimeActivationPolicy` [ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)配置文件项上的特性、直接使用旧的激活 Api 或通过调用[ICLRRuntimeInfo：： BindAsLegacyV2Runtime](iclrruntimeinfo-bindaslegacyv2runtime-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="10800-103">Returns an interface that represents a runtime to which legacy activation policy has been bound, for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../configure-apps/file-schema/startup/startup-element.md) configuration file entry, by direct use of the legacy activation APIs, or by calling the [ICLRRuntimeInfo::BindAsLegacyV2Runtime](iclrruntimeinfo-bindaslegacyv2runtime-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10800-104">语法</span><span class="sxs-lookup"><span data-stu-id="10800-104">Syntax</span></span>  
  
```cpp  
HRESULT QueryLegacyV2RuntimeBinding (  
    [in] REFIID riid,  
    [out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="10800-105">参数</span><span class="sxs-lookup"><span data-stu-id="10800-105">Parameters</span></span>  

 `riid`  
 <span data-ttu-id="10800-106">中必需。当前此参数的有效值为 `IID_ICLRRuntimeInfo` 。</span><span class="sxs-lookup"><span data-stu-id="10800-106">[in] Required.Currently the only valid value for this parameter is `IID_ICLRRuntimeInfo`.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="10800-107">[out] 必需。</span><span class="sxs-lookup"><span data-stu-id="10800-107">[out] Required.</span></span> <span data-ttu-id="10800-108">此方法返回时，包含一个指向 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口的指针，该接口表示已绑定到旧版激活策略的运行时。</span><span class="sxs-lookup"><span data-stu-id="10800-108">When this method returns, contains a pointer to the [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface that represents a runtime that has been bound to legacy activation policy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="10800-109">返回值</span><span class="sxs-lookup"><span data-stu-id="10800-109">Return Value</span></span>  

 <span data-ttu-id="10800-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="10800-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="10800-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="10800-111">HRESULT</span></span>|<span data-ttu-id="10800-112">说明</span><span class="sxs-lookup"><span data-stu-id="10800-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="10800-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="10800-113">S_OK</span></span>|<span data-ttu-id="10800-114">该方法已成功完成，并返回一个绑定到旧式激活策略的运行时。</span><span class="sxs-lookup"><span data-stu-id="10800-114">The method completed successfully and returned a runtime that was bound to legacy activation policy.</span></span>|  
|<span data-ttu-id="10800-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="10800-115">S_FALSE</span></span>|<span data-ttu-id="10800-116">该方法已成功完成，但尚未绑定旧式运行时。</span><span class="sxs-lookup"><span data-stu-id="10800-116">The method completed successfully, but a legacy runtime has not yet been bound.</span></span>|  
|<span data-ttu-id="10800-117">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="10800-117">E_NOINTERFACE</span></span>|<span data-ttu-id="10800-118">该方法找到了绑定到旧式激活策略的运行时，但该运行时不支持 `riid`。</span><span class="sxs-lookup"><span data-stu-id="10800-118">The method found a runtime that was bound to legacy activation policy, but `riid` is not supported by that runtime.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="10800-119">备注</span><span class="sxs-lookup"><span data-stu-id="10800-119">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10800-120">要求</span><span class="sxs-lookup"><span data-stu-id="10800-120">Requirements</span></span>  

 <span data-ttu-id="10800-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="10800-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10800-122">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="10800-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="10800-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="10800-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="10800-124">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10800-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10800-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10800-125">See also</span></span>

- [<span data-ttu-id="10800-126">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="10800-126">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="10800-127">承载</span><span class="sxs-lookup"><span data-stu-id="10800-127">Hosting</span></span>](index.md)
