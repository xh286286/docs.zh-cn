---
title: ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetReferencedAssembliesFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile
helpviewer_keywords:
- ICLRAssemblyIdentityManager::GetReferenceAssembliesFromFile method [.NET Framework hosting]
- GetReferenceAssembliesFromFile method [.NET Framework hosting]
ms.assetid: eed63d31-d977-4c7d-9443-f9d37a2a7d81
topic_type:
- apiref
ms.openlocfilehash: 6b67ba9d022d94f51d7cc6a4645855f6b6ac3e19
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679308"
---
# <a name="iclrassemblyidentitymanagergetreferencedassembliesfromfile-method"></a><span data-ttu-id="3773c-102">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="3773c-102">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile Method</span></span>

<span data-ttu-id="3773c-103">获取一个 [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) 实例，该实例包含程序集在指定文件路径处引用的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="3773c-103">Gets an [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) instance that contains a list of assemblies referenced by the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3773c-104">语法</span><span class="sxs-lookup"><span data-stu-id="3773c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetReferencedAssembliesFromFile (  
    [in]  LPCWSTR pwzFilePath,  
    [in]  DWORD   dwFlags,  
    [in]  ICLRAssemblyReferenceList   *pExcludeAssembliesList,  
    [out] ICLRReferenceAssemblyEnum  **ppReferenceEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3773c-105">参数</span><span class="sxs-lookup"><span data-stu-id="3773c-105">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="3773c-106">中要计算的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="3773c-106">[in] The path to the assembly to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="3773c-107">中提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="3773c-107">[in] Provided for future extensibility.</span></span> <span data-ttu-id="3773c-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时的当前版本 (CLR) 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="3773c-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pExcludeAssembliesList`  
 <span data-ttu-id="3773c-109">中指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 对象的指针，该对象表示应从中排除的程序集 `ppReferenceEnum` 。</span><span class="sxs-lookup"><span data-stu-id="3773c-109">[in] A pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) object that represents assemblies that should be excluded from `ppReferenceEnum`.</span></span>  
  
 `ppReferenceEnum`  
 <span data-ttu-id="3773c-110">弄指向对象地址的指针 `ICLRReferenceAssemblyEnum` ，该对象包含程序集引用的程序集的程序集标识数据，不包括由表示的程序集 `pwzFilePath` `pExcludeAssembliesList` 。</span><span class="sxs-lookup"><span data-stu-id="3773c-110">[out] A pointer to the address of an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly at `pwzFilePath`, excluding the assemblies represented by `pExcludeAssembliesList`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3773c-111">返回值</span><span class="sxs-lookup"><span data-stu-id="3773c-111">Return Value</span></span>  
  
|<span data-ttu-id="3773c-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3773c-112">HRESULT</span></span>|<span data-ttu-id="3773c-113">说明</span><span class="sxs-lookup"><span data-stu-id="3773c-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3773c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3773c-114">S_OK</span></span>|<span data-ttu-id="3773c-115">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3773c-115">The method returned successfully.</span></span>|  
|<span data-ttu-id="3773c-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3773c-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3773c-117">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="3773c-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3773c-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3773c-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3773c-119">调用超时。</span><span class="sxs-lookup"><span data-stu-id="3773c-119">The call timed out.</span></span>|  
|<span data-ttu-id="3773c-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3773c-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3773c-121">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="3773c-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3773c-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3773c-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3773c-123">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="3773c-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3773c-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3773c-124">E_FAIL</span></span>|<span data-ttu-id="3773c-125">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="3773c-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3773c-126">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="3773c-126">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3773c-127">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="3773c-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3773c-128">注解</span><span class="sxs-lookup"><span data-stu-id="3773c-128">Remarks</span></span>  

 <span data-ttu-id="3773c-129">调用方可以选择从返回的列表中排除一组已知的程序集引用。</span><span class="sxs-lookup"><span data-stu-id="3773c-129">The caller can choose to exclude a set of known assembly references from the returned list.</span></span> <span data-ttu-id="3773c-130">此集由 `pExcludeAssembliesList` 参数定义。</span><span class="sxs-lookup"><span data-stu-id="3773c-130">This set is defined by the `pExcludeAssembliesList` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3773c-131">要求</span><span class="sxs-lookup"><span data-stu-id="3773c-131">Requirements</span></span>  

 <span data-ttu-id="3773c-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3773c-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3773c-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3773c-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3773c-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3773c-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3773c-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3773c-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3773c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3773c-136">See also</span></span>

- [<span data-ttu-id="3773c-137">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="3773c-137">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="3773c-138">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="3773c-138">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="3773c-139">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="3773c-139">ICLRReferenceAssemblyEnum Interface</span></span>](iclrreferenceassemblyenum-interface.md)
