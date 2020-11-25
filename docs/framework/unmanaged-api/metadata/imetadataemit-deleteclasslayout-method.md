---
title: IMetaDataEmit::DeleteClassLayout 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteClassLayout
helpviewer_keywords:
- DeleteClassLayout method [.NET Framework metadata]
- IMetaDataEmit::DeleteClassLayout method [.NET Framework metadata]
ms.assetid: 65a4ad49-fa49-4b36-8ed1-76dd6a185ab4
topic_type:
- apiref
ms.openlocfilehash: d355e0e3b2461932384ca11d83d46fd1dc63b80e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732679"
---
# <a name="imetadataemitdeleteclasslayout-method"></a><span data-ttu-id="3cb58-102">IMetaDataEmit::DeleteClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="3cb58-102">IMetaDataEmit::DeleteClassLayout Method</span></span>

<span data-ttu-id="3cb58-103">销毁由指定标记表示的类型的类布局元数据签名。</span><span class="sxs-lookup"><span data-stu-id="3cb58-103">Destroys the class layout metadata signature for the type represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cb58-104">语法</span><span class="sxs-lookup"><span data-stu-id="3cb58-104">Syntax</span></span>  
  
```cpp  
HRESULT DeleteClassLayout (  
    [in]  mdTypeDef   td  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3cb58-105">参数</span><span class="sxs-lookup"><span data-stu-id="3cb58-105">Parameters</span></span>  

 `td`  
 <span data-ttu-id="3cb58-106">中一个 `mdTypeDef` 元数据标记，它表示将删除类布局的类型。</span><span class="sxs-lookup"><span data-stu-id="3cb58-106">[in] An `mdTypeDef` metadata token that represents the type for which the class layout will be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3cb58-107">要求</span><span class="sxs-lookup"><span data-stu-id="3cb58-107">Requirements</span></span>  

 <span data-ttu-id="3cb58-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3cb58-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3cb58-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3cb58-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3cb58-110">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3cb58-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3cb58-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3cb58-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cb58-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3cb58-112">See also</span></span>

- [<span data-ttu-id="3cb58-113">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="3cb58-113">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="3cb58-114">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="3cb58-114">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
