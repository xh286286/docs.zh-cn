---
title: CLRCreateInstance 函数
ms.date: 03/30/2017
api_name:
- CLRCreateInstance
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- COM
f1_keywords:
- CLRCreateInstance
helpviewer_keywords:
- CLRCreateInstance function [.NET Framework hosting]
ms.assetid: 5de13327-96c6-4697-a89e-b8bf40717855
topic_type:
- apiref
ms.openlocfilehash: 3c7a14f828e55310435a99693c1195f2f0dd40c6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95711671"
---
# <a name="clrcreateinstance-function"></a><span data-ttu-id="aa639-102">CLRCreateInstance 函数</span><span class="sxs-lookup"><span data-stu-id="aa639-102">CLRCreateInstance Function</span></span>

<span data-ttu-id="aa639-103">提供以下三个接口之一： [ICLRMetaHost](iclrmetahost-interface.md)、 [ICLRMetaHostPolicy](iclrmetahostpolicy-interface.md)或 [ICLRDebugging](../debugging/iclrdebugging-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="aa639-103">Provides one of three interfaces: [ICLRMetaHost](iclrmetahost-interface.md), [ICLRMetaHostPolicy](iclrmetahostpolicy-interface.md), or [ICLRDebugging](../debugging/iclrdebugging-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa639-104">语法</span><span class="sxs-lookup"><span data-stu-id="aa639-104">Syntax</span></span>  
  
```cpp  
HRESULT CLRCreateInstance(  
    [in]  REFCLSID  clsid,  
    [in]  REFIID     riid,  
    [out] LPVOID  * ppInterface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aa639-105">参数</span><span class="sxs-lookup"><span data-stu-id="aa639-105">Parameters</span></span>  

 `clsid`  
 <span data-ttu-id="aa639-106">中三个类标识符之一： CLSID_CLRMetaHost、CLSID_CLRMetaHostPolicy 或 CLSID_CLRDebugging。</span><span class="sxs-lookup"><span data-stu-id="aa639-106">[in] One of three class identifiers: CLSID_CLRMetaHost, CLSID_CLRMetaHostPolicy, or CLSID_CLRDebugging.</span></span>  
  
 `riid`  
 <span data-ttu-id="aa639-107">中三个接口标识符中的一个 (Iid) ： IID_ICLRMetaHost、IID_ICLRMetaHostPolicy 或 IID_ICLRDebugging。</span><span class="sxs-lookup"><span data-stu-id="aa639-107">[in] One of three interface identifiers (IIDs): IID_ICLRMetaHost, IID_ICLRMetaHostPolicy, or IID_ICLRDebugging.</span></span>  
  
 `ppInterface`  
 <span data-ttu-id="aa639-108">弄以下三个接口之一： [ICLRMetaHost](iclrmetahost-interface.md)、 [ICLRMetaHostPolicy](iclrmetahostpolicy-interface.md)或 [ICLRDebugging](../debugging/iclrdebugging-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="aa639-108">[out] One of three interfaces: [ICLRMetaHost](iclrmetahost-interface.md), [ICLRMetaHostPolicy](iclrmetahostpolicy-interface.md), or [ICLRDebugging](../debugging/iclrdebugging-interface.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aa639-109">返回值</span><span class="sxs-lookup"><span data-stu-id="aa639-109">Return Value</span></span>  

 <span data-ttu-id="aa639-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="aa639-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="aa639-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="aa639-111">HRESULT</span></span>|<span data-ttu-id="aa639-112">说明</span><span class="sxs-lookup"><span data-stu-id="aa639-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="aa639-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa639-113">S_OK</span></span>|<span data-ttu-id="aa639-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="aa639-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="aa639-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="aa639-115">E_POINTER</span></span>|<span data-ttu-id="aa639-116">`ppInterface` 为 null。</span><span class="sxs-lookup"><span data-stu-id="aa639-116">`ppInterface` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aa639-117">注解</span><span class="sxs-lookup"><span data-stu-id="aa639-117">Remarks</span></span>  

 <span data-ttu-id="aa639-118">下表显示了和支持的组合 `clsid` `riid` 。</span><span class="sxs-lookup"><span data-stu-id="aa639-118">The following table shows the supported combinations for `clsid` and `riid`.</span></span>  
  
|`clsid`|`riid`|  
|--------------|------------|  
|<span data-ttu-id="aa639-119">CLSID_CLRMetaHost</span><span class="sxs-lookup"><span data-stu-id="aa639-119">CLSID_CLRMetaHost</span></span>|<span data-ttu-id="aa639-120">IID_ICLRMetaHost</span><span class="sxs-lookup"><span data-stu-id="aa639-120">IID_ICLRMetaHost</span></span>|  
|<span data-ttu-id="aa639-121">CLSID_CLRMetaHostPolicy</span><span class="sxs-lookup"><span data-stu-id="aa639-121">CLSID_CLRMetaHostPolicy</span></span>|<span data-ttu-id="aa639-122">IID_ICLRMetaHostPolicy</span><span class="sxs-lookup"><span data-stu-id="aa639-122">IID_ICLRMetaHostPolicy</span></span>|  
|<span data-ttu-id="aa639-123">CLSID_CLRDebugging</span><span class="sxs-lookup"><span data-stu-id="aa639-123">CLSID_CLRDebugging</span></span>|<span data-ttu-id="aa639-124">IID_ICLRDebugging</span><span class="sxs-lookup"><span data-stu-id="aa639-124">IID_ICLRDebugging</span></span>|  
  
 <span data-ttu-id="aa639-125">下面的代码演示如何使用 `CLRCreateInstance` 获取所有三个接口：</span><span class="sxs-lookup"><span data-stu-id="aa639-125">The following code shows how to use `CLRCreateInstance` to get all three interfaces:</span></span>  
  
```cpp  
#include <metahost.h>  
#pragma comment(lib, "mscoree.lib")  
  
ICLRMetaHost       *pMetaHost       = NULL;  
ICLRMetaHostPolicy *pMetaHostPolicy = NULL;  
ICLRDebugging      *pCLRDebugging   = NULL;  
HRESULT hr;  
hr = CLRCreateInstance(CLSID_CLRMetaHost, IID_ICLRMetaHost,  
                    (LPVOID*)&pMetaHost);  
hr = CLRCreateInstance (CLSID_CLRMetaHostPolicy, IID_ICLRMetaHostPolicy,  
                    (LPVOID*)&pMetaHostPolicy);  
hr = CLRCreateInstance (CLSID_CLRDebugging, IID_ICLRDebugging,  
                    (LPVOID*)&pCLRDebugging);  
```  
  
## <a name="requirements"></a><span data-ttu-id="aa639-126">要求</span><span class="sxs-lookup"><span data-stu-id="aa639-126">Requirements</span></span>  

 <span data-ttu-id="aa639-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aa639-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa639-128">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="aa639-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="aa639-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aa639-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aa639-130">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa639-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa639-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa639-131">See also</span></span>

- [<span data-ttu-id="aa639-132">承载</span><span class="sxs-lookup"><span data-stu-id="aa639-132">Hosting</span></span>](index.md)
