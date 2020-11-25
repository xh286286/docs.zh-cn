---
title: IMetaDataEmit::DeletePinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeletePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeletePinvokeMap
helpviewer_keywords:
- IMetaDataEmit::DeletePinvokeMap method [.NET Framework metadata]
- DeletePinvokeMap method [.NET Framework metadata]
ms.assetid: 3c4f6b54-5ce7-4a2a-83e1-6dec16441f50
topic_type:
- apiref
ms.openlocfilehash: 6fc6cf9b7333dd4caad3c5a4b081fecb060c8f86
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722084"
---
# <a name="imetadataemitdeletepinvokemap-method"></a><span data-ttu-id="d139f-102">IMetaDataEmit::DeletePinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="d139f-102">IMetaDataEmit::DeletePinvokeMap Method</span></span>

<span data-ttu-id="d139f-103">销毁指定标记所引用的对象的 PInvoke 映射元数据。</span><span class="sxs-lookup"><span data-stu-id="d139f-103">Destroys the PInvoke mapping metadata for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d139f-104">语法</span><span class="sxs-lookup"><span data-stu-id="d139f-104">Syntax</span></span>  
  
```cpp  
HRESULT DeletePinvokeMap (
    [in]  mdToken     tk
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d139f-105">参数</span><span class="sxs-lookup"><span data-stu-id="d139f-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="d139f-106">中 `mdFieldDef` 或 `mdMethodDef` 标记，它表示要为其删除 PInvoke 映射元数据的对象。</span><span class="sxs-lookup"><span data-stu-id="d139f-106">[in] An `mdFieldDef` or `mdMethodDef` token that represents the object for which to delete the PInvoke mapping metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d139f-107">要求</span><span class="sxs-lookup"><span data-stu-id="d139f-107">Requirements</span></span>  

 <span data-ttu-id="d139f-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d139f-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d139f-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d139f-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d139f-110">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d139f-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d139f-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d139f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d139f-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d139f-112">See also</span></span>

- [<span data-ttu-id="d139f-113">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="d139f-113">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="d139f-114">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="d139f-114">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
