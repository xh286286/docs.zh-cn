---
title: IMetaDataEmit::DefineProperty 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineProperty
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type:
- apiref
ms.openlocfilehash: d2a4a15126f34666a58021a59e9e193685b15a49
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719484"
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="2d96c-102">IMetaDataEmit::DefineProperty 方法</span><span class="sxs-lookup"><span data-stu-id="2d96c-102">IMetaDataEmit::DefineProperty Method</span></span>

<span data-ttu-id="2d96c-103">使用指定的和方法访问器创建指定类型的属性定义， `get` `set` 并获取该属性定义的标记。</span><span class="sxs-lookup"><span data-stu-id="2d96c-103">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d96c-104">语法</span><span class="sxs-lookup"><span data-stu-id="2d96c-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineProperty (
    [in]  mdTypeDef          td,
    [in]  LPCWSTR            szProperty,
    [in]  DWORD              dwPropFlags,
    [in]  PCCOR_SIGNATURE    pvSig,
    [in]  ULONG              cbSig,
    [in]  DWORD              dwCPlusTypeFlag,
    [in]  void const         *pValue,
    [in]  ULONG              cchValue,
    [in]  mdMethodDef        mdSetter,
    [in]  mdMethodDef        mdGetter,
    [in]  mdMethodDef        rmdOtherMethods[],
    [out] mdProperty         *pmdProp
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d96c-105">参数</span><span class="sxs-lookup"><span data-stu-id="2d96c-105">Parameters</span></span>  

 `td`  
 <span data-ttu-id="2d96c-106">中正在为其定义属性的类或接口的标记。</span><span class="sxs-lookup"><span data-stu-id="2d96c-106">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="2d96c-107">中属性的名称。</span><span class="sxs-lookup"><span data-stu-id="2d96c-107">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="2d96c-108">中属性标志。</span><span class="sxs-lookup"><span data-stu-id="2d96c-108">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="2d96c-109">中属性签名。</span><span class="sxs-lookup"><span data-stu-id="2d96c-109">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="2d96c-110">中中的字节数 `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="2d96c-110">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="2d96c-111">中属性的默认值的类型。</span><span class="sxs-lookup"><span data-stu-id="2d96c-111">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="2d96c-112">中属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="2d96c-112">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="2d96c-113">中中 (Unicode) 字符的计数 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="2d96c-113">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="2d96c-114">中用于设置属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="2d96c-114">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="2d96c-115">中获取属性值的方法。</span><span class="sxs-lookup"><span data-stu-id="2d96c-115">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="2d96c-116">中与属性关联的其他方法的数组。</span><span class="sxs-lookup"><span data-stu-id="2d96c-116">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="2d96c-117">使用终止数组 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="2d96c-117">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="2d96c-118">弄 `mdProperty` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="2d96c-118">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d96c-119">要求</span><span class="sxs-lookup"><span data-stu-id="2d96c-119">Requirements</span></span>  

 <span data-ttu-id="2d96c-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d96c-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d96c-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="2d96c-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2d96c-122">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="2d96c-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2d96c-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d96c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d96c-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d96c-124">See also</span></span>

- [<span data-ttu-id="2d96c-125">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="2d96c-125">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="2d96c-126">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="2d96c-126">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
