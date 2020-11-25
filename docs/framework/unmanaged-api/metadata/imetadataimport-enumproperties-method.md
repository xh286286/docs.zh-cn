---
title: IMetaDataImport::EnumProperties 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumProperties
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumProperties
helpviewer_keywords:
- IMetaDataImport::EnumProperties method [.NET Framework metadata]
- EnumProperties method [.NET Framework metadata]
ms.assetid: 60573ad7-8821-4721-a068-3f7a6d25926a
topic_type:
- apiref
ms.openlocfilehash: 24ee37a36e34c74258e1c750ba424640c0496f0a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728246"
---
# <a name="imetadataimportenumproperties-method"></a><span data-ttu-id="d1e24-102">IMetaDataImport::EnumProperties 方法</span><span class="sxs-lookup"><span data-stu-id="d1e24-102">IMetaDataImport::EnumProperties Method</span></span>

<span data-ttu-id="d1e24-103">枚举 PropertyDef 标记，这些标记表示指定的 TypeDef 标记所引用的类型的属性。</span><span class="sxs-lookup"><span data-stu-id="d1e24-103">Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1e24-104">语法</span><span class="sxs-lookup"><span data-stu-id="d1e24-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumProperties (  
   [in, out] HCORENUM    *phEnum,  
   [in]      mdTypeDef   td,  
   [out]     mdProperty  rProperties[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcProperties  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d1e24-105">参数</span><span class="sxs-lookup"><span data-stu-id="d1e24-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="d1e24-106">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="d1e24-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="d1e24-107">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="d1e24-107">This must be NULL for the first call of this method.</span></span>  
  
 `td`  
 <span data-ttu-id="d1e24-108">中一个 TypeDef 标记，它表示具有要枚举的属性的类型。</span><span class="sxs-lookup"><span data-stu-id="d1e24-108">[in] A TypeDef token representing the type with properties to enumerate.</span></span>  
  
 `rProperties`  
 <span data-ttu-id="d1e24-109">弄用于存储 PropertyDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="d1e24-109">[out] The array used to store the PropertyDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d1e24-110">[in] `rProperties` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="d1e24-110">[in] The maximum size of the `rProperties` array.</span></span>  
  
 `pcProperties`  
 <span data-ttu-id="d1e24-111">弄中返回的 PropertyDef 令牌数 `rProperties` 。</span><span class="sxs-lookup"><span data-stu-id="d1e24-111">[out] The number of PropertyDef tokens returned in `rProperties`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1e24-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d1e24-112">Return Value</span></span>  
  
|<span data-ttu-id="d1e24-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1e24-113">HRESULT</span></span>|<span data-ttu-id="d1e24-114">说明</span><span class="sxs-lookup"><span data-stu-id="d1e24-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="d1e24-115">`EnumProperties` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d1e24-115">`EnumProperties` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="d1e24-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="d1e24-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="d1e24-117">在这种情况下， `pcProperties` 为零。</span><span class="sxs-lookup"><span data-stu-id="d1e24-117">In that case, `pcProperties` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d1e24-118">要求</span><span class="sxs-lookup"><span data-stu-id="d1e24-118">Requirements</span></span>  

 <span data-ttu-id="d1e24-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d1e24-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1e24-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d1e24-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d1e24-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d1e24-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d1e24-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1e24-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1e24-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1e24-123">See also</span></span>

- [<span data-ttu-id="d1e24-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="d1e24-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="d1e24-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="d1e24-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
