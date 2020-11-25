---
title: ICLRRuntimeInfo::IsStarted 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsStarted
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsStarted
helpviewer_keywords:
- IsStarted method [.NET Framework hosting]
- ICLRRuntimeInfo::IsStarted method [.NET Framework hosting]
ms.assetid: ef6f2662-323b-4534-aa82-6d1afb7b9309
ms.openlocfilehash: 1dfeb6101a6b8e33ab2fe35f318087d7f1834b6a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714882"
---
# <a name="iclrruntimeinfoisstarted-method"></a><span data-ttu-id="df1e0-102">ICLRRuntimeInfo::IsStarted 方法</span><span class="sxs-lookup"><span data-stu-id="df1e0-102">ICLRRuntimeInfo::IsStarted Method</span></span>

<span data-ttu-id="df1e0-103">指示运行时是否已启动 (即是否已调用 [ICLRRuntimeHost：： Start 方法](iclrruntimehost-start-method.md) 并且已成功) 。</span><span class="sxs-lookup"><span data-stu-id="df1e0-103">Indicates whether the runtime has been started (that is, whether the [ICLRRuntimeHost::Start method](iclrruntimehost-start-method.md) has been called and has succeeded).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df1e0-104">语法</span><span class="sxs-lookup"><span data-stu-id="df1e0-104">Syntax</span></span>  
  
```cpp  
HRESULT IsStarted(  
        [out] BOOL     *pbStarted,  
        [out] DWORD    *pdwStartupFlags);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df1e0-105">参数</span><span class="sxs-lookup"><span data-stu-id="df1e0-105">Parameters</span></span>  

 `pbStarted`  
 <span data-ttu-id="df1e0-106">[out] `true` 如果此运行时已启动，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="df1e0-106">[out] `true` if this runtime is started; otherwise, `false`.</span></span>  
  
 `pdwStartupFlags`  
 <span data-ttu-id="df1e0-107">弄返回用于启动运行时的标志。</span><span class="sxs-lookup"><span data-stu-id="df1e0-107">[out] Returns the flags that were used to start the runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="df1e0-108">返回值</span><span class="sxs-lookup"><span data-stu-id="df1e0-108">Return Value</span></span>  

 <span data-ttu-id="df1e0-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="df1e0-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="df1e0-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="df1e0-110">HRESULT</span></span>|<span data-ttu-id="df1e0-111">说明</span><span class="sxs-lookup"><span data-stu-id="df1e0-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="df1e0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="df1e0-112">S_OK</span></span>|<span data-ttu-id="df1e0-113">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="df1e0-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="df1e0-114">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="df1e0-114">E_NOTIMPL</span></span>|<span data-ttu-id="df1e0-115">公共语言运行时 (CLR) 版本早于 .NET Framework 4 中的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="df1e0-115">The common language runtime (CLR) version is earlier than the CLR version in the .NET Framework 4.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="df1e0-116">注解</span><span class="sxs-lookup"><span data-stu-id="df1e0-116">Remarks</span></span>  

 <span data-ttu-id="df1e0-117">此方法不适用于 CLR 版本早于 .NET Framework 4 的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="df1e0-117">This method does not work with CLR versions earlier than the CLR version in the .NET Framework 4.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df1e0-118">要求</span><span class="sxs-lookup"><span data-stu-id="df1e0-118">Requirements</span></span>  

 <span data-ttu-id="df1e0-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df1e0-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df1e0-120">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="df1e0-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="df1e0-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="df1e0-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="df1e0-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df1e0-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df1e0-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df1e0-123">See also</span></span>

- [<span data-ttu-id="df1e0-124">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="df1e0-124">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="df1e0-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="df1e0-125">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="df1e0-126">承载</span><span class="sxs-lookup"><span data-stu-id="df1e0-126">Hosting</span></span>](index.md)
