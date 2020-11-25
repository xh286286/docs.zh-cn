---
title: IMetaDataImport::EnumTypeDefs 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeDefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeDefs
helpviewer_keywords:
- EnumTypeDefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeDefs method [.NET Framework metadata]
ms.assetid: 4e508711-da92-4381-aaf8-6803075cdaa2
topic_type:
- apiref
ms.openlocfilehash: 4545f5f8d78e588c655a72340210a785b0feb619
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720407"
---
# <a name="imetadataimportenumtypedefs-method"></a><span data-ttu-id="30c0f-102">IMetaDataImport::EnumTypeDefs 方法</span><span class="sxs-lookup"><span data-stu-id="30c0f-102">IMetaDataImport::EnumTypeDefs Method</span></span>

<span data-ttu-id="30c0f-103">枚举表示当前范围内的所有类型的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="30c0f-103">Enumerates TypeDef tokens representing all types within the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30c0f-104">语法</span><span class="sxs-lookup"><span data-stu-id="30c0f-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumTypeDefs (  
   [out] HCORENUM   *phEnum,
   [in]  mdTypeDef  rTypeDefs[],  
   [in]  ULONG      cMax,
   [out] ULONG      *pcTypeDefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30c0f-105">参数</span><span class="sxs-lookup"><span data-stu-id="30c0f-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="30c0f-106">弄指向新枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="30c0f-106">[out] A pointer to the new enumerator.</span></span> <span data-ttu-id="30c0f-107">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="30c0f-107">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeDefs`  
 <span data-ttu-id="30c0f-108">中用于存储 TypeDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="30c0f-108">[in] The array used to store the TypeDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="30c0f-109">[in] `rTypeDefs` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="30c0f-109">[in] The maximum size of the `rTypeDefs` array.</span></span>  
  
 `pcTypeDefs`  
 <span data-ttu-id="30c0f-110">弄中返回的 TypeDef 标记的数目 `rTypeDefs` 。</span><span class="sxs-lookup"><span data-stu-id="30c0f-110">[out] The number of TypeDef tokens returned in `rTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="30c0f-111">返回值</span><span class="sxs-lookup"><span data-stu-id="30c0f-111">Return Value</span></span>  
  
|<span data-ttu-id="30c0f-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="30c0f-112">HRESULT</span></span>|<span data-ttu-id="30c0f-113">说明</span><span class="sxs-lookup"><span data-stu-id="30c0f-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="30c0f-114">`EnumTypeDefs` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="30c0f-114">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="30c0f-115">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="30c0f-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="30c0f-116">在这种情况下， `pcTypeDefs` 为零。</span><span class="sxs-lookup"><span data-stu-id="30c0f-116">In that case, `pcTypeDefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="30c0f-117">注解</span><span class="sxs-lookup"><span data-stu-id="30c0f-117">Remarks</span></span>  

 <span data-ttu-id="30c0f-118">TypeDef 标记表示一种类型，如类或接口，以及通过扩展性机制添加的任何类型。</span><span class="sxs-lookup"><span data-stu-id="30c0f-118">The TypeDef token represents a type such as a class or an interface, as well as any type added via an extensibility mechanism.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30c0f-119">要求</span><span class="sxs-lookup"><span data-stu-id="30c0f-119">Requirements</span></span>  

 <span data-ttu-id="30c0f-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30c0f-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30c0f-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="30c0f-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="30c0f-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="30c0f-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="30c0f-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30c0f-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30c0f-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30c0f-124">See also</span></span>

- [<span data-ttu-id="30c0f-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="30c0f-125">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="30c0f-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="30c0f-126">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
