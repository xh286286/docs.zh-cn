---
title: IMetaDataEmit::DeleteFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
ms.openlocfilehash: 5989c45782b4f83ecfa285cb305080320abf6a3c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700543"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="dc55c-102">IMetaDataEmit::DeleteFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="dc55c-102">IMetaDataEmit::DeleteFieldMarshal Method</span></span>

<span data-ttu-id="dc55c-103">销毁指定标记所引用的对象的 PInvoke 封送元数据签名。</span><span class="sxs-lookup"><span data-stu-id="dc55c-103">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc55c-104">语法</span><span class="sxs-lookup"><span data-stu-id="dc55c-104">Syntax</span></span>  
  
```cpp  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc55c-105">参数</span><span class="sxs-lookup"><span data-stu-id="dc55c-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="dc55c-106">中 `mdFieldDef` 或 `mdParamDef` 标记，它表示要删除封送处理元数据签名的字段或参数。</span><span class="sxs-lookup"><span data-stu-id="dc55c-106">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc55c-107">要求</span><span class="sxs-lookup"><span data-stu-id="dc55c-107">Requirements</span></span>  

 <span data-ttu-id="dc55c-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dc55c-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc55c-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="dc55c-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dc55c-110">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="dc55c-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dc55c-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc55c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc55c-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc55c-112">See also</span></span>

- [<span data-ttu-id="dc55c-113">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="dc55c-113">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="dc55c-114">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="dc55c-114">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
