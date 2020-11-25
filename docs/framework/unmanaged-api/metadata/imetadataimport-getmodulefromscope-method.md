---
title: IMetaDataImport::GetModuleFromScope 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetModuleFromScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetModuleFromScope
helpviewer_keywords:
- GetModuleFromScope method [.NET Framework metadata]
- IMetaDataImport::GetModuleFromScope method [.NET Framework metadata]
ms.assetid: add68d3f-45fd-4bef-af94-eb5273f26b11
topic_type:
- apiref
ms.openlocfilehash: 2eddd7a80c2b9c1b71f3e7fc5b1e4686ba11bccd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733160"
---
# <a name="imetadataimportgetmodulefromscope-method"></a><span data-ttu-id="f6cef-102">IMetaDataImport::GetModuleFromScope 方法</span><span class="sxs-lookup"><span data-stu-id="f6cef-102">IMetaDataImport::GetModuleFromScope Method</span></span>

<span data-ttu-id="f6cef-103">获取当前元数据范围内引用的模块的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f6cef-103">Gets a metadata token for the module referenced in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6cef-104">语法</span><span class="sxs-lookup"><span data-stu-id="f6cef-104">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleFromScope (  
   [out] mdModule    *pmd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6cef-105">参数</span><span class="sxs-lookup"><span data-stu-id="f6cef-105">Parameters</span></span>  

 `pmd`  
 <span data-ttu-id="f6cef-106">弄一个指针，指向表示当前元数据范围内引用的模块的标记。</span><span class="sxs-lookup"><span data-stu-id="f6cef-106">[out] A pointer to the token representing the module referenced in the current metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6cef-107">要求</span><span class="sxs-lookup"><span data-stu-id="f6cef-107">Requirements</span></span>  

 <span data-ttu-id="f6cef-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6cef-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6cef-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f6cef-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f6cef-110">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6cef-110">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f6cef-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6cef-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6cef-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f6cef-112">See also</span></span>

- [<span data-ttu-id="f6cef-113">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f6cef-113">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f6cef-114">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f6cef-114">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
