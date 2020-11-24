---
title: ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList.IsStringAssemblyReferenceInList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList
helpviewer_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList method [.NET Framework hosting]
- IsStringAssemblyReferenceInList method [.NET Framework hosting]
ms.assetid: e6121cc3-2f11-42c7-bdae-47808581ff71
topic_type:
- apiref
ms.openlocfilehash: 74d47b3f55c10f65d47f726a2b96ba5e0b18b749
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679138"
---
# <a name="iclrassemblyreferencelistisstringassemblyreferenceinlist-method"></a><span data-ttu-id="42de9-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList 方法</span><span class="sxs-lookup"><span data-stu-id="42de9-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList Method</span></span>

<span data-ttu-id="42de9-103">获取一个值，该值指示所提供的名称是否与列表中的程序集的名称相匹配。</span><span class="sxs-lookup"><span data-stu-id="42de9-103">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42de9-104">语法</span><span class="sxs-lookup"><span data-stu-id="42de9-104">Syntax</span></span>  
  
```cpp  
HRESULT IsStringAssemblyReferenceInList (  
    [in] LPCWSTR pwzAssemblyName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42de9-105">参数</span><span class="sxs-lookup"><span data-stu-id="42de9-105">Parameters</span></span>  

 `pwzAssemblyName`  
 <span data-ttu-id="42de9-106">中要搜索的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="42de9-106">[in] The name of the assembly for which to search.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="42de9-107">返回值</span><span class="sxs-lookup"><span data-stu-id="42de9-107">Return Value</span></span>  
  
|<span data-ttu-id="42de9-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="42de9-108">HRESULT</span></span>|<span data-ttu-id="42de9-109">说明</span><span class="sxs-lookup"><span data-stu-id="42de9-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="42de9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="42de9-110">S_OK</span></span>|<span data-ttu-id="42de9-111">此字符串将显示在列表中。</span><span class="sxs-lookup"><span data-stu-id="42de9-111">The string appears in the list.</span></span>|  
|<span data-ttu-id="42de9-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="42de9-112">S_FALSE</span></span>|<span data-ttu-id="42de9-113">该字符串未出现在列表中。</span><span class="sxs-lookup"><span data-stu-id="42de9-113">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="42de9-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="42de9-114">E_FAIL</span></span>|<span data-ttu-id="42de9-115">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="42de9-115">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="42de9-116">方法返回 E_FAIL 后，公共语言运行时在进程中将不再可用。</span><span class="sxs-lookup"><span data-stu-id="42de9-116">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="42de9-117">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="42de9-117">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="42de9-118">要求</span><span class="sxs-lookup"><span data-stu-id="42de9-118">Requirements</span></span>  

 <span data-ttu-id="42de9-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42de9-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42de9-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="42de9-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="42de9-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="42de9-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="42de9-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42de9-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42de9-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42de9-123">See also</span></span>

- [<span data-ttu-id="42de9-124">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="42de9-124">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="42de9-125">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="42de9-125">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="42de9-126">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="42de9-126">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="42de9-127">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="42de9-127">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
