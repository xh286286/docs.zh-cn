---
title: IMetaDataEmit::DefineMethodImpl 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMethodImpl
helpviewer_keywords:
- DefineMethodImpl method [.NET Framework metadata]
- IMetaDataEmit::DefineMethodImpl method [.NET Framework metadata]
ms.assetid: 9dcc8b3d-33ee-4c7c-8d6f-322c57b94a0f
topic_type:
- apiref
ms.openlocfilehash: 24a7c5bca1287e55f3eb06d63e1fed8da37eb3b0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719562"
---
# <a name="imetadataemitdefinemethodimpl-method"></a><span data-ttu-id="a3cd0-102">IMetaDataEmit::DefineMethodImpl 方法</span><span class="sxs-lookup"><span data-stu-id="a3cd0-102">IMetaDataEmit::DefineMethodImpl Method</span></span>

<span data-ttu-id="a3cd0-103">创建一个定义，用于实现从接口继承的方法，并返回该方法实现定义的标记。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-103">Creates a definition for implementation of a method inherited from an interface, and returns a token to that method-implementation definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3cd0-104">语法</span><span class="sxs-lookup"><span data-stu-id="a3cd0-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineMethodImpl (
    [in]  mdTypeDef         td,
    [in]  mdToken           tkBody,
    [in]  mdToken           tkDecl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a3cd0-105">参数</span><span class="sxs-lookup"><span data-stu-id="a3cd0-105">Parameters</span></span>  

 `td`  
 <span data-ttu-id="a3cd0-106">中 `mdTypedef` 实现类的标记。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-106">[in] The `mdTypedef` token of the implementing class.</span></span>  
  
 `tkBody`  
 <span data-ttu-id="a3cd0-107">中 `mdMethodDef` `mdMemberRef` 代码主体的或标记。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-107">[in] The `mdMethodDef` or `mdMemberRef` token of the code body.</span></span>  
  
 `tkDecl`  
 <span data-ttu-id="a3cd0-108">中 `mdMethodDef` `mdMemberRef` 要实现的接口方法的或标记。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-108">[in] The `mdMethodDef` or `mdMemberRef` token of the interface method being implemented.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3cd0-109">要求</span><span class="sxs-lookup"><span data-stu-id="a3cd0-109">Requirements</span></span>  

 <span data-ttu-id="a3cd0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3cd0-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a3cd0-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a3cd0-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a3cd0-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3cd0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3cd0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3cd0-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3cd0-114">See also</span></span>

- [<span data-ttu-id="a3cd0-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="a3cd0-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="a3cd0-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="a3cd0-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
