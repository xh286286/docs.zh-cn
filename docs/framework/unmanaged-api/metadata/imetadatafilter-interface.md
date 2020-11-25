---
title: IMetaDataFilter 接口
ms.date: 03/30/2017
api_name:
- IMetaDataFilter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter
helpviewer_keywords:
- IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: ec0856ef-8c56-40ba-bf60-86e0ce8b337f
topic_type:
- apiref
ms.openlocfilehash: 2c22e45ca3d33b0a81ff0ecd90bf7574c45676bd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95701843"
---
# <a name="imetadatafilter-interface"></a><span data-ttu-id="220d5-102">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="220d5-102">IMetaDataFilter Interface</span></span>

<span data-ttu-id="220d5-103">提供用于标记和筛选元数据标记以避免重复已进行的操作的方法。</span><span class="sxs-lookup"><span data-stu-id="220d5-103">Provides methods for marking and filtering metadata tokens to avoid repeating actions that have already been taken.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="220d5-104">方法</span><span class="sxs-lookup"><span data-stu-id="220d5-104">Methods</span></span>  
  
|<span data-ttu-id="220d5-105">方法</span><span class="sxs-lookup"><span data-stu-id="220d5-105">Method</span></span>|<span data-ttu-id="220d5-106">说明</span><span class="sxs-lookup"><span data-stu-id="220d5-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="220d5-107">IsTokenMarked 方法</span><span class="sxs-lookup"><span data-stu-id="220d5-107">IsTokenMarked Method</span></span>](imetadatafilter-istokenmarked-method.md)|<span data-ttu-id="220d5-108">获取一个值，该值指示是否已处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="220d5-108">Gets a value indicating whether the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="220d5-109">MarkToken 方法</span><span class="sxs-lookup"><span data-stu-id="220d5-109">MarkToken Method</span></span>](imetadatafilter-marktoken-method.md)|<span data-ttu-id="220d5-110">设置一个值，该值指示已处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="220d5-110">Sets a value indicating that the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="220d5-111">UnmarkAll 方法</span><span class="sxs-lookup"><span data-stu-id="220d5-111">UnmarkAll Method</span></span>](imetadatafilter-unmarkall-method.md)|<span data-ttu-id="220d5-112">从当前元数据范围内的所有标记中删除处理标记。</span><span class="sxs-lookup"><span data-stu-id="220d5-112">Removes the processing marks from all the tokens in the current metadata scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="220d5-113">要求</span><span class="sxs-lookup"><span data-stu-id="220d5-113">Requirements</span></span>  

 <span data-ttu-id="220d5-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="220d5-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="220d5-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="220d5-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="220d5-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="220d5-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="220d5-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="220d5-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="220d5-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="220d5-118">See also</span></span>

- [<span data-ttu-id="220d5-119">元数据接口</span><span class="sxs-lookup"><span data-stu-id="220d5-119">Metadata Interfaces</span></span>](metadata-interfaces.md)
