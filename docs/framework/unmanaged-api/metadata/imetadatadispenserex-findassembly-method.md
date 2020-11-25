---
title: IMetaDataDispenserEx::FindAssembly 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssembly
helpviewer_keywords:
- FindAssembly method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssembly method [.NET Framework metadata]
ms.assetid: 3afe7252-5f28-48d9-a74d-1927566c404c
topic_type:
- apiref
ms.openlocfilehash: c11a4498610c3e82590a0ff9be1247173e70be76
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713387"
---
# <a name="imetadatadispenserexfindassembly-method"></a><span data-ttu-id="3489d-102">IMetaDataDispenserEx::FindAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="3489d-102">IMetaDataDispenserEx::FindAssembly Method</span></span>

<span data-ttu-id="3489d-103">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="3489d-103">This method is not implemented.</span></span> <span data-ttu-id="3489d-104">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="3489d-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3489d-105">语法</span><span class="sxs-lookup"><span data-stu-id="3489d-105">Syntax</span></span>  
  
```cpp  
HRESULT FindAssembly(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3489d-106">参数</span><span class="sxs-lookup"><span data-stu-id="3489d-106">Parameters</span></span>  

 `szAppBase`  
 <span data-ttu-id="3489d-107">中不使用。</span><span class="sxs-lookup"><span data-stu-id="3489d-107">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="3489d-108">中不使用。</span><span class="sxs-lookup"><span data-stu-id="3489d-108">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="3489d-109">中不使用。</span><span class="sxs-lookup"><span data-stu-id="3489d-109">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="3489d-110">中要查找的程序集。</span><span class="sxs-lookup"><span data-stu-id="3489d-110">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="3489d-111">弄程序集的简单名称。</span><span class="sxs-lookup"><span data-stu-id="3489d-111">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="3489d-112">中的大小（以字节为单位） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="3489d-112">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="3489d-113">弄中实际返回的字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="3489d-113">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3489d-114">要求</span><span class="sxs-lookup"><span data-stu-id="3489d-114">Requirements</span></span>  

 <span data-ttu-id="3489d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3489d-115">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3489d-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3489d-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3489d-117">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3489d-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3489d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3489d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3489d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3489d-119">See also</span></span>

- [<span data-ttu-id="3489d-120">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="3489d-120">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="3489d-121">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="3489d-121">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
