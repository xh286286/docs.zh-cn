---
title: CorLaunchApplication 函数
ms.date: 03/30/2017
api_name:
- CorLaunchApplication
api_location:
- mscoree.dll
- clr.dll
api_type:
- COM
f1_keywords:
- CorLaunchApplication
helpviewer_keywords:
- CorLaunchApplication function [.NET Framework hosting]
ms.assetid: 71f362a9-8fe2-47ce-9302-05a645cf3d7d
topic_type:
- apiref
ms.openlocfilehash: ca427439f03d92b20e7714b9724d90b240e9cecb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95704066"
---
# <a name="corlaunchapplication-function"></a><span data-ttu-id="c2d17-102">CorLaunchApplication 函数</span><span class="sxs-lookup"><span data-stu-id="c2d17-102">CorLaunchApplication Function</span></span>

<span data-ttu-id="c2d17-103">使用指定的清单和其他应用程序数据，在指定的网络路径下启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="c2d17-103">Starts the application at the specified network path, using the specified manifests and other application data.</span></span>  
  
 <span data-ttu-id="c2d17-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="c2d17-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2d17-105">语法</span><span class="sxs-lookup"><span data-stu-id="c2d17-105">Syntax</span></span>  
  
```cpp  
HRESULT CorLaunchApplication (  
    [in]  HOST_TYPE                dwClickOnceHost,  
    [in]  LPCWSTR                  pwzAppFullName,  
    [in]  DWORD                    dwManifestPaths,  
    [in]  LPCWSTR                 *ppwzManifestPaths,  
    [in]  DWORD                    dwActivationData,  
    [in]  LPCWSTR                 *ppwzActivationData,  
    [out] LPPROCESS_INFORMATION    lpProcessInformation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2d17-106">参数</span><span class="sxs-lookup"><span data-stu-id="c2d17-106">Parameters</span></span>  

 `dwClickOnceHost`  
 <span data-ttu-id="c2d17-107">中一个 [HOST_TYPE](host-type-enumeration.md) 枚举的值，该值指定启动应用程序的主机的类型。</span><span class="sxs-lookup"><span data-stu-id="c2d17-107">[in] A value of the [HOST_TYPE](host-type-enumeration.md) enumeration that specifies the type of host that is launching the application.</span></span>  
  
 `pwzAppFullName`  
 <span data-ttu-id="c2d17-108">中正在启动的应用程序的完整名称。</span><span class="sxs-lookup"><span data-stu-id="c2d17-108">[in] The full name of the application that is being launched.</span></span>  
  
 `dwManifestPaths`  
 <span data-ttu-id="c2d17-109">中应用程序的清单路径数。</span><span class="sxs-lookup"><span data-stu-id="c2d17-109">[in] The number of manifest paths for the application.</span></span>  
  
 `ppwzManifestPaths`  
 <span data-ttu-id="c2d17-110">中一个字符串数组，其中每个字符串指定要启动的应用程序的清单的路径。</span><span class="sxs-lookup"><span data-stu-id="c2d17-110">[in] An array of strings, each of which specifies a path to a manifest for the application that is being launched.</span></span>  
  
 `dwActivationData`  
 <span data-ttu-id="c2d17-111">中正在启动的应用程序的激活数据项的数目。</span><span class="sxs-lookup"><span data-stu-id="c2d17-111">[in] The number of activation data items for the application that is being launched.</span></span>  
  
 `ppwzActivationData`  
 <span data-ttu-id="c2d17-112">中一个字符串数组，其中每个字符串都是要启动的应用程序的激活数据项。</span><span class="sxs-lookup"><span data-stu-id="c2d17-112">[in] An array of strings, each of which is an activation data item for the application that is being launched.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="c2d17-113">弄一个指针，指向有关已加载应用程序的进程的信息。</span><span class="sxs-lookup"><span data-stu-id="c2d17-113">[out] A pointer to information about the process in which the application has been loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2d17-114">要求</span><span class="sxs-lookup"><span data-stu-id="c2d17-114">Requirements</span></span>  

 <span data-ttu-id="c2d17-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d17-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2d17-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c2d17-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c2d17-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2d17-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2d17-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2d17-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2d17-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2d17-119">See also</span></span>

- [<span data-ttu-id="c2d17-120">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="c2d17-120">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
