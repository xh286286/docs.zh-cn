---
title: IMetaDataImport::EnumUnresolvedMethods 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUnresolvedMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUnresolvedMethods
helpviewer_keywords:
- EnumUnresolvedMethods method [.NET Framework metadata]
- IMetaDataImport::EnumUnresolvedMethods method [.NET Framework metadata]
ms.assetid: eb3187d7-74cf-44b1-aeeb-7a8d2b60e3b7
topic_type:
- apiref
ms.openlocfilehash: 6b5e7bbe2303a200d7829fea12e228a513595f97
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95716546"
---
# <a name="imetadataimportenumunresolvedmethods-method"></a><span data-ttu-id="090cd-102">IMetaDataImport::EnumUnresolvedMethods 方法</span><span class="sxs-lookup"><span data-stu-id="090cd-102">IMetaDataImport::EnumUnresolvedMethods Method</span></span>

<span data-ttu-id="090cd-103">枚举表示当前元数据范围内未解析的方法的 MemberDef 标记。</span><span class="sxs-lookup"><span data-stu-id="090cd-103">Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="090cd-104">语法</span><span class="sxs-lookup"><span data-stu-id="090cd-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumUnresolvedMethods (  
   [in, out] HCORENUM    *phEnum,  
   [out]     mdToken     rMethods[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="090cd-105">参数</span><span class="sxs-lookup"><span data-stu-id="090cd-105">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="090cd-106">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="090cd-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="090cd-107">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="090cd-107">This must be NULL for the first call of this method.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="090cd-108">弄用于存储 MemberDef 标记的数组。</span><span class="sxs-lookup"><span data-stu-id="090cd-108">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="090cd-109">[in] `rMethods` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="090cd-109">[in] The maximum size of the `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="090cd-110">弄中返回的 MemberDef 令牌数 `rMethods` 。</span><span class="sxs-lookup"><span data-stu-id="090cd-110">[out] The number of MemberDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="090cd-111">返回值</span><span class="sxs-lookup"><span data-stu-id="090cd-111">Return Value</span></span>  
  
|<span data-ttu-id="090cd-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="090cd-112">HRESULT</span></span>|<span data-ttu-id="090cd-113">说明</span><span class="sxs-lookup"><span data-stu-id="090cd-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="090cd-114">`EnumUnresolvedMethods` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="090cd-114">`EnumUnresolvedMethods` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="090cd-115">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="090cd-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="090cd-116">在这种情况下， `pcTokens` 为零。</span><span class="sxs-lookup"><span data-stu-id="090cd-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="090cd-117">注解</span><span class="sxs-lookup"><span data-stu-id="090cd-117">Remarks</span></span>  

 <span data-ttu-id="090cd-118">未解析的方法是已声明但未实现的方法。</span><span class="sxs-lookup"><span data-stu-id="090cd-118">An unresolved method is one that has been declared but not implemented.</span></span> <span data-ttu-id="090cd-119">如果方法已标记 `miForwardRef` 并且 `mdPinvokeImpl` 或 `miRuntime` 设置为零，则枚举中将包含方法。</span><span class="sxs-lookup"><span data-stu-id="090cd-119">A method is included in the enumeration if the method is marked `miForwardRef` and either `mdPinvokeImpl` or `miRuntime` is set to zero.</span></span> <span data-ttu-id="090cd-120">换句话说，未解析的方法是已标记 `miForwardRef` 但未在非托管代码中实现的类方法 (通过 PInvoke) 或由运行时本身内部实现</span><span class="sxs-lookup"><span data-stu-id="090cd-120">In other words, an unresolved method is a class method that is marked `miForwardRef` but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself</span></span>  
  
 <span data-ttu-id="090cd-121">枚举排除在模块范围 (全局) 或接口或抽象类中定义的所有方法。</span><span class="sxs-lookup"><span data-stu-id="090cd-121">The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="090cd-122">要求</span><span class="sxs-lookup"><span data-stu-id="090cd-122">Requirements</span></span>  

 <span data-ttu-id="090cd-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="090cd-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="090cd-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="090cd-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="090cd-125">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="090cd-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="090cd-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="090cd-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="090cd-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="090cd-127">See also</span></span>

- [<span data-ttu-id="090cd-128">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="090cd-128">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="090cd-129">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="090cd-129">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
