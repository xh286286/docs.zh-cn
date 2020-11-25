---
title: IMetaDataEmit2::SaveDeltaToMemory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToMemory
helpviewer_keywords:
- SaveDeltaToMemory method [.NET Framework metadata]
- IMetaDataEmit2::SaveDeltaToMemory method [.NET Framework metadata]
ms.assetid: e2146726-0084-4c9e-a2d2-e8d461b13b21
topic_type:
- apiref
ms.openlocfilehash: a4dbe090987248ef77ce371b5bc6fb42d898f726
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705405"
---
# <a name="imetadataemit2savedeltatomemory-method"></a><span data-ttu-id="fe7d4-102">IMetaDataEmit2::SaveDeltaToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="fe7d4-102">IMetaDataEmit2::SaveDeltaToMemory Method</span></span>

<span data-ttu-id="fe7d4-103">将当前的 "编辑并继续" 会话中的更改保存到内存。</span><span class="sxs-lookup"><span data-stu-id="fe7d4-103">Saves changes from the current edit-and-continue session to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe7d4-104">语法</span><span class="sxs-lookup"><span data-stu-id="fe7d4-104">Syntax</span></span>  
  
```cpp  
HRESULT SaveDeltaToMemory (  
    [out] void        *pbData,
    [in]  ULONG       cbData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fe7d4-105">参数</span><span class="sxs-lookup"><span data-stu-id="fe7d4-105">Parameters</span></span>  

 `pbData`  
 <span data-ttu-id="fe7d4-106">弄开始写入元数据增量的地址。</span><span class="sxs-lookup"><span data-stu-id="fe7d4-106">[out] The address at which to begin writing the metadata delta.</span></span>  
  
 `cbData`  
 <span data-ttu-id="fe7d4-107">中更改的大小。</span><span class="sxs-lookup"><span data-stu-id="fe7d4-107">[in] The size of the changes.</span></span> <span data-ttu-id="fe7d4-108">使用 [IMetaDataEmit2：： GetDeltaSaveSize](imetadataemit2-getdeltasavesize-method.md) 确定大小。</span><span class="sxs-lookup"><span data-stu-id="fe7d4-108">Use [IMetaDataEmit2::GetDeltaSaveSize](imetadataemit2-getdeltasavesize-method.md) to determine the size.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe7d4-109">要求</span><span class="sxs-lookup"><span data-stu-id="fe7d4-109">Requirements</span></span>  

 <span data-ttu-id="fe7d4-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe7d4-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe7d4-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="fe7d4-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fe7d4-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="fe7d4-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fe7d4-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe7d4-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe7d4-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe7d4-114">See also</span></span>

- [<span data-ttu-id="fe7d4-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="fe7d4-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="fe7d4-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="fe7d4-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
