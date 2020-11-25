---
title: IMetaDataError 接口
ms.date: 03/30/2017
api_name:
- IMetaDataError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError
helpviewer_keywords:
- IMetaDataError interface [.NET Framework metadata]
ms.assetid: 0020b62c-ea88-40c7-a9ee-16b064f81624
topic_type:
- apiref
ms.openlocfilehash: 5f5e04787ce0ab0e1c8ecf3c19ba37e76ba38bfe
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95701921"
---
# <a name="imetadataerror-interface"></a><span data-ttu-id="cff69-102">IMetaDataError 接口</span><span class="sxs-lookup"><span data-stu-id="cff69-102">IMetaDataError Interface</span></span>

<span data-ttu-id="cff69-103">提供用于在元数据合并期间报告错误的回调机制。</span><span class="sxs-lookup"><span data-stu-id="cff69-103">Provides a callback mechanism for reporting errors during the metadata merge.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cff69-104">`IMetaDataError`接口必须由客户端实现。</span><span class="sxs-lookup"><span data-stu-id="cff69-104">The `IMetaDataError` interface must be implemented by the client.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cff69-105">方法</span><span class="sxs-lookup"><span data-stu-id="cff69-105">Methods</span></span>  
  
|<span data-ttu-id="cff69-106">方法</span><span class="sxs-lookup"><span data-stu-id="cff69-106">Method</span></span>|<span data-ttu-id="cff69-107">说明</span><span class="sxs-lookup"><span data-stu-id="cff69-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cff69-108">OnError 方法</span><span class="sxs-lookup"><span data-stu-id="cff69-108">OnError Method</span></span>](imetadataerror-onerror-method.md)|<span data-ttu-id="cff69-109">提供在元数据合并期间发生的错误的通知。</span><span class="sxs-lookup"><span data-stu-id="cff69-109">Provides notification of errors that occur during the metadata merge.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cff69-110">要求</span><span class="sxs-lookup"><span data-stu-id="cff69-110">Requirements</span></span>  

 <span data-ttu-id="cff69-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cff69-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cff69-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="cff69-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cff69-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="cff69-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cff69-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cff69-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cff69-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cff69-115">See also</span></span>

- [<span data-ttu-id="cff69-116">元数据接口</span><span class="sxs-lookup"><span data-stu-id="cff69-116">Metadata Interfaces</span></span>](metadata-interfaces.md)
