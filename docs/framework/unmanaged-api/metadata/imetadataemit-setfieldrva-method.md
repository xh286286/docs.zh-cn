---
title: IMetaDataEmit::SetFieldRVA 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldRVA
helpviewer_keywords:
- IMetaDataEmit::SetFieldRVA method [.NET Framework metadata]
- SetFieldRVA method [.NET Framework metadata]
ms.assetid: 6dc37f9d-87ee-4cb3-9216-ced600184ce8
topic_type:
- apiref
ms.openlocfilehash: 8468b0e7faa520fe2d27e17674af5503871d3b62
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730378"
---
# <a name="imetadataemitsetfieldrva-method"></a><span data-ttu-id="3d1e1-102">IMetaDataEmit::SetFieldRVA 方法</span><span class="sxs-lookup"><span data-stu-id="3d1e1-102">IMetaDataEmit::SetFieldRVA Method</span></span>

<span data-ttu-id="3d1e1-103">为指定的标记所引用的字段的相对虚拟地址设置全局变量值。</span><span class="sxs-lookup"><span data-stu-id="3d1e1-103">Sets a global variable value for the relative virtual address of the field referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d1e1-104">语法</span><span class="sxs-lookup"><span data-stu-id="3d1e1-104">Syntax</span></span>  
  
```cpp  
HRESULT SetFieldRVA (
    [in]  mdFieldDef  fd,
    [in]  ULONG       ulRVA
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3d1e1-105">参数</span><span class="sxs-lookup"><span data-stu-id="3d1e1-105">Parameters</span></span>  

 `fd`  
 <span data-ttu-id="3d1e1-106">中目标字段的标记。</span><span class="sxs-lookup"><span data-stu-id="3d1e1-106">[in] The token for the target field.</span></span>  
  
 `ulRVA`  
 <span data-ttu-id="3d1e1-107">中代码或数据区域的地址。</span><span class="sxs-lookup"><span data-stu-id="3d1e1-107">[in] The address of a code or data area.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d1e1-108">要求</span><span class="sxs-lookup"><span data-stu-id="3d1e1-108">Requirements</span></span>  

 <span data-ttu-id="3d1e1-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e1-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d1e1-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3d1e1-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3d1e1-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3d1e1-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3d1e1-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d1e1-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d1e1-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d1e1-113">See also</span></span>

- [<span data-ttu-id="3d1e1-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="3d1e1-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="3d1e1-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="3d1e1-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
