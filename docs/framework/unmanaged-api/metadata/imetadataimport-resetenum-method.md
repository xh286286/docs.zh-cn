---
title: IMetaDataImport::ResetEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.ResetEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::ResetEnum
helpviewer_keywords:
- ResetEnum method [.NET Framework metadata]
- IMetaDataImport::ResetEnum method [.NET Framework metadata]
ms.assetid: dda867b5-1050-49ba-b01c-fcc83b7a5617
topic_type:
- apiref
ms.openlocfilehash: 52c35b3bd726d4c83c6745bf99940faa44ea7338
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702844"
---
# <a name="imetadataimportresetenum-method"></a><span data-ttu-id="f5355-102">IMetaDataImport::ResetEnum 方法</span><span class="sxs-lookup"><span data-stu-id="f5355-102">IMetaDataImport::ResetEnum Method</span></span>

<span data-ttu-id="f5355-103">将指定的枚举器重置到指定位置。</span><span class="sxs-lookup"><span data-stu-id="f5355-103">Resets the specified enumerator to the specified position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5355-104">语法</span><span class="sxs-lookup"><span data-stu-id="f5355-104">Syntax</span></span>  
  
```cpp  
HRESULT ResetEnum (  
   [in] HCORENUM    hEnum,
   [in] ULONG       ulPos  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5355-105">参数</span><span class="sxs-lookup"><span data-stu-id="f5355-105">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="f5355-106">中要重置的枚举数。</span><span class="sxs-lookup"><span data-stu-id="f5355-106">[in] The enumerator to reset.</span></span>  
  
 `ulPos`  
 <span data-ttu-id="f5355-107">中要放置枚举器的新位置。</span><span class="sxs-lookup"><span data-stu-id="f5355-107">[in] The new position at which to place the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5355-108">要求</span><span class="sxs-lookup"><span data-stu-id="f5355-108">Requirements</span></span>  

 <span data-ttu-id="f5355-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f5355-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5355-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f5355-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f5355-111">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f5355-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f5355-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5355-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5355-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5355-113">See also</span></span>

- [<span data-ttu-id="f5355-114">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f5355-114">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f5355-115">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f5355-115">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
