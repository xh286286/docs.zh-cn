---
title: IMetaDataEmit::SetParamProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetParamProps
helpviewer_keywords:
- IMetaDataEmit::SetParamProps method [.NET Framework metadata]
- SetParamProps method [.NET Framework metadata]
ms.assetid: a95a3908-9f87-4084-937e-8e01ef03ad63
topic_type:
- apiref
ms.openlocfilehash: b0cc28807938bcfb9b2465093ff4cfb94066ee98
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675056"
---
# <a name="imetadataemitsetparamprops-method"></a><span data-ttu-id="0beb2-102">IMetaDataEmit::SetParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="0beb2-102">IMetaDataEmit::SetParamProps Method</span></span>

<span data-ttu-id="0beb2-103">设置或更改之前调用 [IMetaDataEmit：:D efineparam](imetadataemit-defineparam-method.md)时定义的方法参数的功能。</span><span class="sxs-lookup"><span data-stu-id="0beb2-103">Sets or changes features of a method parameter that was defined by a prior call to [IMetaDataEmit::DefineParam](imetadataemit-defineparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0beb2-104">语法</span><span class="sxs-lookup"><span data-stu-id="0beb2-104">Syntax</span></span>  
  
```cpp  
HRESULT SetParamProps (
    [in]  mdParamDef  pd,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwParamFlags,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,
    [in]  ULONG       cchValue
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0beb2-105">参数</span><span class="sxs-lookup"><span data-stu-id="0beb2-105">Parameters</span></span>  

 `pd`  
 <span data-ttu-id="0beb2-106">中目标参数的标记。</span><span class="sxs-lookup"><span data-stu-id="0beb2-106">[in] The token for the target parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="0beb2-107">中Unicode 中参数的名称。</span><span class="sxs-lookup"><span data-stu-id="0beb2-107">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="0beb2-108">中参数的标志。</span><span class="sxs-lookup"><span data-stu-id="0beb2-108">[in] The flags for the parameter.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="0beb2-109">中常量值的 ELEMENT_TYPE_ \*。</span><span class="sxs-lookup"><span data-stu-id="0beb2-109">[in] The ELEMENT_TYPE_\* for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="0beb2-110">中参数的常数值。</span><span class="sxs-lookup"><span data-stu-id="0beb2-110">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="0beb2-111">中 (Unicode) 字符的大小 `pValue` 。</span><span class="sxs-lookup"><span data-stu-id="0beb2-111">[in] The size in (Unicode) characters of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0beb2-112">要求</span><span class="sxs-lookup"><span data-stu-id="0beb2-112">Requirements</span></span>  

 <span data-ttu-id="0beb2-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0beb2-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0beb2-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0beb2-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0beb2-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0beb2-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0beb2-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0beb2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0beb2-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0beb2-117">See also</span></span>

- [<span data-ttu-id="0beb2-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="0beb2-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="0beb2-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="0beb2-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
