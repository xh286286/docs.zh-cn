---
title: IMetaDataEmit::SetFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldMarshal
helpviewer_keywords:
- SetFieldMarshal method [.NET Framework metadata]
- IMetaDataEmit::SetFieldMarshal method [.NET Framework metadata]
ms.assetid: be232314-7f69-4855-bfab-63361bd22307
topic_type:
- apiref
ms.openlocfilehash: d479416f5f1cb4042f9b3fc112e22b67e37d3f78
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95672703"
---
# <a name="imetadataemitsetfieldmarshal-method"></a><span data-ttu-id="ac529-102">IMetaDataEmit::SetFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="ac529-102">IMetaDataEmit::SetFieldMarshal Method</span></span>

<span data-ttu-id="ac529-103">为指定的标记引用的字段、方法返回或方法参数设置 PInvoke 封送处理信息。</span><span class="sxs-lookup"><span data-stu-id="ac529-103">Sets the PInvoke marshaling information for the field, method return, or method parameter referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac529-104">语法</span><span class="sxs-lookup"><span data-stu-id="ac529-104">Syntax</span></span>  
  
```cpp  
HRESULT SetFieldMarshal (  
    [in]  mdToken          tk,
    [in]  PCCOR_SIGNATURE  pvNativeType,
    [in]  ULONG            cbNativeType
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac529-105">参数</span><span class="sxs-lookup"><span data-stu-id="ac529-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="ac529-106">中目标数据项的标记。</span><span class="sxs-lookup"><span data-stu-id="ac529-106">[in] The token for target data item.</span></span> <span data-ttu-id="ac529-107">这是 `mdFieldDef` 或 `mdParamDef` 令牌。</span><span class="sxs-lookup"><span data-stu-id="ac529-107">This is either a `mdFieldDef` or a `mdParamDef` token.</span></span>  
  
 `pvNativeType`  
 <span data-ttu-id="ac529-108">中非托管类型的签名。</span><span class="sxs-lookup"><span data-stu-id="ac529-108">[in] The signature for unmanaged type.</span></span>  
  
 `cbNativeType`  
 <span data-ttu-id="ac529-109">中中的字节数 `pvNativeType` 。</span><span class="sxs-lookup"><span data-stu-id="ac529-109">[in] The count of bytes in `pvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac529-110">要求</span><span class="sxs-lookup"><span data-stu-id="ac529-110">Requirements</span></span>  

 <span data-ttu-id="ac529-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ac529-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac529-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ac529-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ac529-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ac529-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ac529-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac529-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac529-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac529-115">See also</span></span>

- [<span data-ttu-id="ac529-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="ac529-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="ac529-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="ac529-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
