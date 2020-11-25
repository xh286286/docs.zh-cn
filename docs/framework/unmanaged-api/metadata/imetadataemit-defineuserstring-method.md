---
title: IMetaDataEmit::DefineUserString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineUserString
helpviewer_keywords:
- DefineUserString method [.NET Framework metadata]
- IMetaDataEmit::DefineUserString method [.NET Framework metadata]
ms.assetid: 88fb7ef3-bbdf-429c-b678-c9c153456461
topic_type:
- apiref
ms.openlocfilehash: ed3c20fe8272ca3205079d26df0b7bde12e58307
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732692"
---
# <a name="imetadataemitdefineuserstring-method"></a><span data-ttu-id="5fce6-102">IMetaDataEmit::DefineUserString 方法</span><span class="sxs-lookup"><span data-stu-id="5fce6-102">IMetaDataEmit::DefineUserString Method</span></span>

<span data-ttu-id="5fce6-103">获取指定文本字符串的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="5fce6-103">Gets a metadata token for the specified literal string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fce6-104">语法</span><span class="sxs-lookup"><span data-stu-id="5fce6-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineUserString (
    [in]  LPCWSTR     szString,
    [in]  ULONG       cchString,
    [out] mdString    *pstk
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5fce6-105">参数</span><span class="sxs-lookup"><span data-stu-id="5fce6-105">Parameters</span></span>  

 `szString`  
 <span data-ttu-id="5fce6-106">中要存储的用户字符串。</span><span class="sxs-lookup"><span data-stu-id="5fce6-106">[in] The user string to store.</span></span>  
  
 `cchString`  
 <span data-ttu-id="5fce6-107">中中的宽字符数 `szString` 。</span><span class="sxs-lookup"><span data-stu-id="5fce6-107">[in] The count of wide characters in `szString`.</span></span>  
  
 `pstk`  
 <span data-ttu-id="5fce6-108">弄分配的字符串标记。</span><span class="sxs-lookup"><span data-stu-id="5fce6-108">[out] The string token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5fce6-109">要求</span><span class="sxs-lookup"><span data-stu-id="5fce6-109">Requirements</span></span>  

 <span data-ttu-id="5fce6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fce6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fce6-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5fce6-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5fce6-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5fce6-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5fce6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5fce6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fce6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5fce6-114">See also</span></span>

- [<span data-ttu-id="5fce6-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5fce6-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="5fce6-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="5fce6-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
