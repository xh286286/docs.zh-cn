---
title: IMetaDataImport::EnumCustomAttributes 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumCustomAttributes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumCustomAttributes
helpviewer_keywords:
- EnumCustomAttributes method [.NET Framework metadata]
- IMetaDataImport::EnumCustomAttributes method [.NET Framework metadata]
ms.assetid: 798513a0-68b1-4d04-bc5b-782a4445ea68
topic_type:
- apiref
ms.openlocfilehash: 3b12200dae23a7b6a2f6e1654e46fdf74dc90968
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700530"
---
# <a name="imetadataimportenumcustomattributes-method"></a><span data-ttu-id="12638-102">IMetaDataImport::EnumCustomAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="12638-102">IMetaDataImport::EnumCustomAttributes Method</span></span>

<span data-ttu-id="12638-103">枚举与指定的类型或成员关联的自定义属性定义标记。</span><span class="sxs-lookup"><span data-stu-id="12638-103">Enumerates custom attribute-definition tokens associated with the specified type or member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12638-104">语法</span><span class="sxs-lookup"><span data-stu-id="12638-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumCustomAttributes (
   [in, out] HCORENUM      *phEnum,  
   [in]  mdToken            tk,
   [in]  mdToken            tkType,
   [out] mdCustomAttribute  rCustomAttributes[],
   [in]  ULONG              cMax,  
   [out, optional] ULONG   *pcCustomAttributes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12638-105">参数</span><span class="sxs-lookup"><span data-stu-id="12638-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="12638-106">[in，out]指向返回的枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="12638-106">[in, out] A pointer to the returned enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="12638-107">中枚举的范围的标记，对于所有自定义特性，则为零。</span><span class="sxs-lookup"><span data-stu-id="12638-107">[in] A token for the scope of the enumeration, or zero for all custom attributes.</span></span>  
  
 `tkType`  
 <span data-ttu-id="12638-108">中要枚举的属性类型或所有类型的构造函数的标记 `null` 。</span><span class="sxs-lookup"><span data-stu-id="12638-108">[in] A token for the constructor of the type of the attributes to be enumerated, or `null` for all types.</span></span>  
  
 `rCustomAttributes`  
 <span data-ttu-id="12638-109">弄自定义特性标记的数组。</span><span class="sxs-lookup"><span data-stu-id="12638-109">[out] An array of custom attribute tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="12638-110">[in] `rCustomAttributes` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="12638-110">[in] The maximum size of the `rCustomAttributes` array.</span></span>  
  
 `pcCustomAttributes`  
 <span data-ttu-id="12638-111">[out，optional]返回的令牌值的实际数量 `rCustomAttributes` 。</span><span class="sxs-lookup"><span data-stu-id="12638-111">[out, optional] The actual number of token values returned in `rCustomAttributes`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="12638-112">返回值</span><span class="sxs-lookup"><span data-stu-id="12638-112">Return Value</span></span>  
  
|<span data-ttu-id="12638-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="12638-113">HRESULT</span></span>|<span data-ttu-id="12638-114">说明</span><span class="sxs-lookup"><span data-stu-id="12638-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="12638-115">`EnumCustomAttributes` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="12638-115">`EnumCustomAttributes` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="12638-116">没有要枚举的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="12638-116">There are no custom attributes to enumerate.</span></span> <span data-ttu-id="12638-117">在这种情况下， `pcCustomAttributes` 为零。</span><span class="sxs-lookup"><span data-stu-id="12638-117">In that case, `pcCustomAttributes` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="12638-118">要求</span><span class="sxs-lookup"><span data-stu-id="12638-118">Requirements</span></span>  

 <span data-ttu-id="12638-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="12638-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12638-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="12638-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="12638-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="12638-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="12638-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12638-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12638-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12638-123">See also</span></span>

- [<span data-ttu-id="12638-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="12638-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="12638-125">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="12638-125">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
