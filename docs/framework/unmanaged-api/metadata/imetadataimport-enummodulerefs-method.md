---
title: IMetaDataImport::EnumModuleRefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumModuleRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumModuleRefs
helpviewer_keywords:
- EnumModuleRefs method [.NET Framework metadata]
- IMetaDataImport::EnumModuleRefs method [.NET Framework metadata]
ms.assetid: 53441f3a-68d2-477c-906e-37c55dfcfb4d
topic_type:
- apiref
ms.openlocfilehash: 788fd1815415bf8bcfa20d431a5451679d2025bd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728272"
---
# <a name="imetadataimportenummodulerefs-method"></a><span data-ttu-id="758de-102">IMetaDataImport::EnumModuleRefs 方法</span><span class="sxs-lookup"><span data-stu-id="758de-102">IMetaDataImport::EnumModuleRefs Method</span></span>

<span data-ttu-id="758de-103">枚举表示导入的模块的 ModuleRef 标记。</span><span class="sxs-lookup"><span data-stu-id="758de-103">Enumerates ModuleRef tokens that represent imported modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="758de-104">语法</span><span class="sxs-lookup"><span data-stu-id="758de-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumModuleRefs (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdModuleRef  rModuleRefs[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcModuleRefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="758de-105">参数</span><span class="sxs-lookup"><span data-stu-id="758de-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="758de-106">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="758de-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="758de-107">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="758de-107">This must be NULL for the first call of this method.</span></span>  
  
 `rModuleRefs`  
 <span data-ttu-id="758de-108">弄用于存储 ModuleRef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="758de-108">[out] The array used to store the ModuleRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="758de-109">[in] `rModuleRefs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="758de-109">[in] The maximum size of the `rModuleRefs` array.</span></span>  
  
 `pcModuleRefs`  
 <span data-ttu-id="758de-110">弄中返回的 ModuleRef 令牌数 `rModuleRefs` 。</span><span class="sxs-lookup"><span data-stu-id="758de-110">[out] The number of ModuleRef tokens returned in `rModuleRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="758de-111">返回值</span><span class="sxs-lookup"><span data-stu-id="758de-111">Return Value</span></span>  
  
|<span data-ttu-id="758de-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="758de-112">HRESULT</span></span>|<span data-ttu-id="758de-113">说明</span><span class="sxs-lookup"><span data-stu-id="758de-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="758de-114">`EnumModuleRefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="758de-114">`EnumModuleRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="758de-115">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="758de-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="758de-116">在这种情况下， `pcModuleRefs` 为零。</span><span class="sxs-lookup"><span data-stu-id="758de-116">In that case, `pcModuleRefs` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="758de-117">要求</span><span class="sxs-lookup"><span data-stu-id="758de-117">Requirements</span></span>  

 <span data-ttu-id="758de-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="758de-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="758de-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="758de-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="758de-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="758de-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="758de-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="758de-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="758de-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="758de-122">See also</span></span>

- [<span data-ttu-id="758de-123">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="758de-123">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="758de-124">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="758de-124">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
