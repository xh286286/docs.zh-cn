---
title: IMetaDataEmit::SaveToMemory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SaveToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToMemory
helpviewer_keywords:
- IMetaDataEmit::SaveToMemory method [.NET Framework metadata]
- SaveToMemory method [.NET Framework metadata]
ms.assetid: d5237628-2675-45ed-a39e-65c0731b6a56
topic_type:
- apiref
ms.openlocfilehash: 1cd5e34d6afefab2fda7e20d4bf73b373ad42787
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688583"
---
# <a name="imetadataemitsavetomemory-method"></a><span data-ttu-id="5b4f9-102">IMetaDataEmit::SaveToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="5b4f9-102">IMetaDataEmit::SaveToMemory Method</span></span>

<span data-ttu-id="5b4f9-103">将当前范围中的所有元数据保存到指定的内存区域。</span><span class="sxs-lookup"><span data-stu-id="5b4f9-103">Saves all metadata in the current scope to the specified area of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b4f9-104">语法</span><span class="sxs-lookup"><span data-stu-id="5b4f9-104">Syntax</span></span>  
  
```cpp  
HRESULT SaveToMemory (
    [out]  void        *pbData,
    [in]   ULONG       cbData
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5b4f9-105">参数</span><span class="sxs-lookup"><span data-stu-id="5b4f9-105">Parameters</span></span>  

 `pbData`  
 <span data-ttu-id="5b4f9-106">弄开始写入元数据的地址。</span><span class="sxs-lookup"><span data-stu-id="5b4f9-106">[out] The address at which to begin writing metadata.</span></span>  
  
 `cbData`  
 <span data-ttu-id="5b4f9-107">中已分配内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5b4f9-107">[in] The size, in bytes, of the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b4f9-108">要求</span><span class="sxs-lookup"><span data-stu-id="5b4f9-108">Requirements</span></span>  

 <span data-ttu-id="5b4f9-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b4f9-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b4f9-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5b4f9-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5b4f9-111">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5b4f9-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5b4f9-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b4f9-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b4f9-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b4f9-113">See also</span></span>

- [<span data-ttu-id="5b4f9-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5b4f9-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="5b4f9-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="5b4f9-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
