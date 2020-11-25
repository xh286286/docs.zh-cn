---
title: IMetaDataImport2::EnumGenericParams 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumGenericParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumGenericParams
helpviewer_keywords:
- EnumGenericParams method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParams method [.NET Framework metadata]
ms.assetid: b50488a5-3cf0-483c-82dc-2892a3ec61ac
topic_type:
- apiref
ms.openlocfilehash: 6b1a8e66eea6caec9dfc8d99e343c987cefa1b0c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702753"
---
# <a name="imetadataimport2enumgenericparams-method"></a><span data-ttu-id="138e2-102">IMetaDataImport2::EnumGenericParams 方法</span><span class="sxs-lookup"><span data-stu-id="138e2-102">IMetaDataImport2::EnumGenericParams Method</span></span>

<span data-ttu-id="138e2-103">获取与指定的 TypeDef 或 MethodDef 标记相关联的泛型参数标记数组的枚举器。</span><span class="sxs-lookup"><span data-stu-id="138e2-103">Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="138e2-104">语法</span><span class="sxs-lookup"><span data-stu-id="138e2-104">Syntax</span></span>  
  
```cpp
HRESULT EnumGenericParams (  
   [in, out] HCORENUM     *phEnum,
   [in]  mdToken          tk,  
   [out] mdGenericParam   rGenericParams[],
   [in]  ULONG            cMax,
   [out] ULONG            *pcGenericParams  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="138e2-105">参数</span><span class="sxs-lookup"><span data-stu-id="138e2-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="138e2-106">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="138e2-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="138e2-107">中要枚举其泛型参数的 TypeDef 或 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="138e2-107">[in] The TypeDef or MethodDef token whose generic parameters are to be enumerated.</span></span>  
  
 `rGenericParams`  
 <span data-ttu-id="138e2-108">弄要枚举的泛型参数的数组。</span><span class="sxs-lookup"><span data-stu-id="138e2-108">[out] The array of generic parameters to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="138e2-109">中要放入的请求的最大数量 `rGenericParams` 。</span><span class="sxs-lookup"><span data-stu-id="138e2-109">[in] The requested maximum number of tokens to place in `rGenericParams`.</span></span>  
  
 `pcGenericParams`  
 <span data-ttu-id="138e2-110">弄放入的标记数 `rGenericParams` 。</span><span class="sxs-lookup"><span data-stu-id="138e2-110">[out] The returned number of tokens placed in `rGenericParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="138e2-111">返回值</span><span class="sxs-lookup"><span data-stu-id="138e2-111">Return Value</span></span>  
  
|<span data-ttu-id="138e2-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="138e2-112">HRESULT</span></span>|<span data-ttu-id="138e2-113">说明</span><span class="sxs-lookup"><span data-stu-id="138e2-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="138e2-114">`EnumGenericParams` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="138e2-114">`EnumGenericParams` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="138e2-115">`phEnum` 没有成员元素。</span><span class="sxs-lookup"><span data-stu-id="138e2-115">`phEnum` has no member elements.</span></span> <span data-ttu-id="138e2-116">在这种情况下， `pcGenericParams` 设置为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="138e2-116">In this case, `pcGenericParams` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="138e2-117">要求</span><span class="sxs-lookup"><span data-stu-id="138e2-117">Requirements</span></span>  

 <span data-ttu-id="138e2-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="138e2-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="138e2-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="138e2-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="138e2-120">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="138e2-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="138e2-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="138e2-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="138e2-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="138e2-122">See also</span></span>

- [<span data-ttu-id="138e2-123">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="138e2-123">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="138e2-124">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="138e2-124">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
