---
title: IMetaDataAssemblyImport::EnumAssemblyRefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumAssemblyRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs method [.NET Framework metadata]
- EnumAssemblyRefs method [.NET Framework metadata]
ms.assetid: 8844d0dd-730e-4592-8a7b-c1462d312c70
topic_type:
- apiref
ms.openlocfilehash: 18cd9dd14e615a7e76bfff30c9ae584305bd1907
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708924"
---
# <a name="imetadataassemblyimportenumassemblyrefs-method"></a><span data-ttu-id="bdece-102">IMetaDataAssemblyImport::EnumAssemblyRefs 方法</span><span class="sxs-lookup"><span data-stu-id="bdece-102">IMetaDataAssemblyImport::EnumAssemblyRefs Method</span></span>

<span data-ttu-id="bdece-103">枚举 `mdAssemblyRef` 在程序集清单中定义的实例。</span><span class="sxs-lookup"><span data-stu-id="bdece-103">Enumerates the `mdAssemblyRef` instances that are defined in the assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdece-104">语法</span><span class="sxs-lookup"><span data-stu-id="bdece-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumAssemblyRefs (  
    [in, out] HCORENUM        *phEnum,
    [out]     mdAssemblyRef   rAssemblyRefs[],
    [in]      ULONG           cMax,
    [out]     ULONG           *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bdece-105">参数</span><span class="sxs-lookup"><span data-stu-id="bdece-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="bdece-106">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="bdece-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="bdece-107">第一次调用方法时，此值必须为 null 值 `EnumAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="bdece-107">This must be a null value when the `EnumAssemblyRefs` method is called for the first time.</span></span>  
  
 `rAssemblyRefs`  
 <span data-ttu-id="bdece-108">弄 `mdAssemblyRef` 元数据标记的枚举。</span><span class="sxs-lookup"><span data-stu-id="bdece-108">[out] The enumeration of `mdAssemblyRef` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="bdece-109">中可置于数组中的最大标记数 `rAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="bdece-109">[in] The maximum number of tokens that can be placed in the `rAssemblyRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="bdece-110">弄实际置于中的标记数 `rAssemblyRefs` 。</span><span class="sxs-lookup"><span data-stu-id="bdece-110">[out] The number of tokens actually placed in `rAssemblyRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bdece-111">返回值</span><span class="sxs-lookup"><span data-stu-id="bdece-111">Return Value</span></span>  
  
|<span data-ttu-id="bdece-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bdece-112">HRESULT</span></span>|<span data-ttu-id="bdece-113">说明</span><span class="sxs-lookup"><span data-stu-id="bdece-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="bdece-114">`EnumAssemblyRefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bdece-114">`EnumAssemblyRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="bdece-115">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="bdece-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="bdece-116">在这种情况下， `pcTokens` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="bdece-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bdece-117">要求</span><span class="sxs-lookup"><span data-stu-id="bdece-117">Requirements</span></span>  

 <span data-ttu-id="bdece-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bdece-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdece-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="bdece-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bdece-120">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="bdece-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bdece-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdece-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdece-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdece-122">See also</span></span>

- [<span data-ttu-id="bdece-123">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="bdece-123">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
