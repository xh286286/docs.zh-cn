---
title: IMetaDataEmit::DefineSecurityAttributeSet 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineSecurityAttributeSet
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet
helpviewer_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet method [.NET Framework metadata]
- DefineSecurityAttributeSet method [.NET Framework metadata]
ms.assetid: 27064ca2-4186-4433-90a7-3b297785e891
topic_type:
- apiref
ms.openlocfilehash: 5caf07414c9e64169f272eb11169c4d4ee399c6b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719458"
---
# <a name="imetadataemitdefinesecurityattributeset-method"></a><span data-ttu-id="b8bce-102">IMetaDataEmit::DefineSecurityAttributeSet 方法</span><span class="sxs-lookup"><span data-stu-id="b8bce-102">IMetaDataEmit::DefineSecurityAttributeSet Method</span></span>

<span data-ttu-id="b8bce-103">创建一组安全权限，以附加到指定标记所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="b8bce-103">Creates a set of security permissions to attach to the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8bce-104">语法</span><span class="sxs-lookup"><span data-stu-id="b8bce-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineSecurityAttributeSet (
    [in]  mdToken       tkObj,
    [in]  COR_SECATTR   rSecAttrs[],
    [in]  ULONG         cSecAttrs,
    [out] ULONG         *pulErrorAttr
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8bce-105">参数</span><span class="sxs-lookup"><span data-stu-id="b8bce-105">Parameters</span></span>  

 `tkObj`  
 <span data-ttu-id="b8bce-106">中安全信息附加到的令牌。</span><span class="sxs-lookup"><span data-stu-id="b8bce-106">[in] The token to which the security information is attached.</span></span>  
  
 `rSecAttrs`  
 <span data-ttu-id="b8bce-107">中结构的数组 `COR_SECATTR` 。</span><span class="sxs-lookup"><span data-stu-id="b8bce-107">[in] An array of `COR_SECATTR` structures.</span></span>  
  
 `cSecAttrs`  
 <span data-ttu-id="b8bce-108">中中的元素数目 `rSecAttrs` 。</span><span class="sxs-lookup"><span data-stu-id="b8bce-108">[in] The number of elements in `rSecAttrs`.</span></span>  
  
 `pulErrorAttr`  
 <span data-ttu-id="b8bce-109">弄如果该方法失败，则指定 `rSecAttrs` 引起问题的元素在中的索引。</span><span class="sxs-lookup"><span data-stu-id="b8bce-109">[out] If the method fails, specifies the index in `rSecAttrs` of the element that caused the problem.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8bce-110">要求</span><span class="sxs-lookup"><span data-stu-id="b8bce-110">Requirements</span></span>  

 <span data-ttu-id="b8bce-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8bce-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8bce-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b8bce-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b8bce-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b8bce-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b8bce-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8bce-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8bce-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8bce-115">See also</span></span>

- [<span data-ttu-id="b8bce-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="b8bce-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="b8bce-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="b8bce-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
