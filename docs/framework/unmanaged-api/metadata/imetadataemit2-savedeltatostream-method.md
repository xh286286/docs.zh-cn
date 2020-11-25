---
title: IMetaDataEmit2::SaveDeltaToStream 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToStream
helpviewer_keywords:
- IMetaDataEmit2::SaveDeltaToStream method [.NET Framework metadata]
- SaveDeltaToStream method [.NET Framework metadata]
ms.assetid: ecd786e8-f9a4-4190-a6ef-af18e8c6d654
topic_type:
- apiref
ms.openlocfilehash: dad916d74c4e754d8fd3ffb62024e49617f5de05
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702012"
---
# <a name="imetadataemit2savedeltatostream-method"></a><span data-ttu-id="c68e6-102">IMetaDataEmit2::SaveDeltaToStream 方法</span><span class="sxs-lookup"><span data-stu-id="c68e6-102">IMetaDataEmit2::SaveDeltaToStream Method</span></span>

<span data-ttu-id="c68e6-103">将当前的 "编辑并继续" 会话中的更改保存到指定的流。</span><span class="sxs-lookup"><span data-stu-id="c68e6-103">Saves changes from the current edit-and-continue session to the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c68e6-104">语法</span><span class="sxs-lookup"><span data-stu-id="c68e6-104">Syntax</span></span>  
  
```cpp  
HRESULT SaveDeltaToStream (  
    [in] IStream     *pIStream,
    [in] DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c68e6-105">参数</span><span class="sxs-lookup"><span data-stu-id="c68e6-105">Parameters</span></span>  

 `pIStream`  
 <span data-ttu-id="c68e6-106">中一个接口指针，指向要将更改保存到的可写流。</span><span class="sxs-lookup"><span data-stu-id="c68e6-106">[in] An interface pointer to the writable stream to which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="c68e6-107">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="c68e6-107">[in] Reserved.</span></span> <span data-ttu-id="c68e6-108">此值必须为零。</span><span class="sxs-lookup"><span data-stu-id="c68e6-108">This value must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c68e6-109">要求</span><span class="sxs-lookup"><span data-stu-id="c68e6-109">Requirements</span></span>  

 <span data-ttu-id="c68e6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c68e6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c68e6-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c68e6-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c68e6-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c68e6-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c68e6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c68e6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c68e6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c68e6-114">See also</span></span>

- [<span data-ttu-id="c68e6-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="c68e6-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="c68e6-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c68e6-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
