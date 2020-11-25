---
title: IMetaDataEmit::SetTypeDefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetTypeDefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetTypeDefProps
helpviewer_keywords:
- SetTypeDefProps method [.NET Framework metadata]
- IMetaDataEmit::SetTypeDefProps method [.NET Framework metadata]
ms.assetid: 480d596a-759f-4d29-ac1a-3dbff8f3544d
topic_type:
- apiref
ms.openlocfilehash: 2f572f66f16ff701350fde3b05be822b9e8c78b4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706822"
---
# <a name="imetadataemitsettypedefprops-method"></a><span data-ttu-id="daa61-102">IMetaDataEmit::SetTypeDefProps 方法</span><span class="sxs-lookup"><span data-stu-id="daa61-102">IMetaDataEmit::SetTypeDefProps Method</span></span>

<span data-ttu-id="daa61-103">设置由之前调用 [IMetaDataEmit：:D efinetypedef](imetadataemit-definetypedef-method.md)定义的类型的功能。</span><span class="sxs-lookup"><span data-stu-id="daa61-103">Sets features of a type defined by a prior call to [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="daa61-104">语法</span><span class="sxs-lookup"><span data-stu-id="daa61-104">Syntax</span></span>  
  
```cpp  
HRESULT SetTypeDefProps (  
    [in]  mdTypeDef   td,
    [in]  DWORD       dwTypeDefFlags,
    [in]  mdToken     tkExtends,
    [in]  mdToken     rtkImplements[]
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="daa61-105">参数</span><span class="sxs-lookup"><span data-stu-id="daa61-105">Parameters</span></span>  

 `td`  
 <span data-ttu-id="daa61-106">中 `mdTypeDef` 从对 IMetaDataEmit 的原始调用获取的标记 [：:D efinetypedef](imetadataemit-definetypedef-method.md)。</span><span class="sxs-lookup"><span data-stu-id="daa61-106">[in] An `mdTypeDef` token obtained from original call to [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md).</span></span>  
  
 `dwTypeDefFlags`  
 <span data-ttu-id="daa61-107">[in] `TypeDef` 属性.</span><span class="sxs-lookup"><span data-stu-id="daa61-107">[in] `TypeDef` attributes.</span></span> <span data-ttu-id="daa61-108">这是一个值的位掩码 `CorTypeAttr` 。</span><span class="sxs-lookup"><span data-stu-id="daa61-108">This is a bitmask of `CorTypeAttr` values.</span></span>  
  
 `tkExtends`  
 <span data-ttu-id="daa61-109">中 `mdToken` 基类的。</span><span class="sxs-lookup"><span data-stu-id="daa61-109">[in] The `mdToken` of the base class.</span></span> <span data-ttu-id="daa61-110">从之前对 IMetaDataEmit 的调用中获取 [：:D efineimporttype](imetadataemit-defineimporttype-method.md)或 `null` 。</span><span class="sxs-lookup"><span data-stu-id="daa61-110">Obtained from a previous call to [IMetaDataEmit::DefineImportType](imetadataemit-defineimporttype-method.md), or `null`.</span></span>  
  
 `rtkImplements[]`  
 <span data-ttu-id="daa61-111">中此类型实现的接口的标记数组。</span><span class="sxs-lookup"><span data-stu-id="daa61-111">[in] An array of tokens for the interfaces that this type implements.</span></span> <span data-ttu-id="daa61-112">`mdTypeRef`使用[IMetaDataEmit：:D efineimporttype](imetadataemit-defineimporttype-method.md)获取这些令牌。</span><span class="sxs-lookup"><span data-stu-id="daa61-112">These `mdTypeRef` tokens are obtained using [IMetaDataEmit::DefineImportType](imetadataemit-defineimporttype-method.md).</span></span> <span data-ttu-id="daa61-113">数组的最后一个元素必须是 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="daa61-113">The last element of the array is must be `mdTokenNil`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="daa61-114">要求</span><span class="sxs-lookup"><span data-stu-id="daa61-114">Requirements</span></span>  

 <span data-ttu-id="daa61-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="daa61-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="daa61-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="daa61-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="daa61-117">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="daa61-117">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="daa61-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="daa61-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="daa61-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="daa61-119">See also</span></span>

- [<span data-ttu-id="daa61-120">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="daa61-120">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="daa61-121">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="daa61-121">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
