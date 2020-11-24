---
title: IMetaDataEmit2::GetDeltaSaveSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.GetDeltaSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::GetDeltaSaveSize
helpviewer_keywords:
- IMetaDataEmit2::GetDeltaSaveSize method [.NET Framework metadata]
- GetDeltaSaveSize method [.NET Framework metadata]
ms.assetid: 036db5e7-8211-4645-9a34-03d1a89be955
topic_type:
- apiref
ms.openlocfilehash: 36021333c1efb61e23c16782d8ad721de62c2643
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674308"
---
# <a name="imetadataemit2getdeltasavesize-method"></a><span data-ttu-id="79b24-102">IMetaDataEmit2::GetDeltaSaveSize 方法</span><span class="sxs-lookup"><span data-stu-id="79b24-102">IMetaDataEmit2::GetDeltaSaveSize Method</span></span>

<span data-ttu-id="79b24-103">获取一个值，该值指示当前的 "编辑并继续" 会话导致的元数据大小的任何更改。</span><span class="sxs-lookup"><span data-stu-id="79b24-103">Gets a value indicating any change in metadata size that results from the current edit-and-continue session.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79b24-104">语法</span><span class="sxs-lookup"><span data-stu-id="79b24-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDeltaSaveSize (  
    [in]  CorSaveSize  fSave,  
    [out] DWORD        *pdwSaveSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79b24-105">参数</span><span class="sxs-lookup"><span data-stu-id="79b24-105">Parameters</span></span>  

 `fSave`  
 <span data-ttu-id="79b24-106">中 [CorSaveSize](corsavesize-enumeration.md) 值之一，指示所需的精度级别。</span><span class="sxs-lookup"><span data-stu-id="79b24-106">[in] One of the [CorSaveSize](corsavesize-enumeration.md) values, indicating the level of precision desired.</span></span> <span data-ttu-id="79b24-107">对于 .NET Framework 版本2.0，将忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="79b24-107">For the .NET Framework version 2.0, this parameter is ignored.</span></span>  
  
 `pdwSaveSize`  
 <span data-ttu-id="79b24-108">弄元数据的大小更改。</span><span class="sxs-lookup"><span data-stu-id="79b24-108">[out] The change in the size of the metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79b24-109">要求</span><span class="sxs-lookup"><span data-stu-id="79b24-109">Requirements</span></span>  

 <span data-ttu-id="79b24-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79b24-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79b24-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="79b24-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79b24-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="79b24-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="79b24-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79b24-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79b24-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79b24-114">See also</span></span>

- [<span data-ttu-id="79b24-115">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="79b24-115">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="79b24-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="79b24-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
