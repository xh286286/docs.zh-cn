---
title: IMetaDataEmit2 接口
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2
helpviewer_keywords:
- IMetaDataEmit2 interface [.NET Framework metadata]
ms.assetid: 866dc96b-bbfc-4c0f-80c2-38ce93072106
topic_type:
- apiref
ms.openlocfilehash: b8ad159dace734c343297b256092162f17ab829b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726478"
---
# <a name="imetadataemit2-interface"></a><span data-ttu-id="1edff-102">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="1edff-102">IMetaDataEmit2 Interface</span></span>

<span data-ttu-id="1edff-103">扩展 [IMetaDataEmit](imetadataemit-interface.md) 接口，主要用于提供使用泛型类型的能力。</span><span class="sxs-lookup"><span data-stu-id="1edff-103">Extends the [IMetaDataEmit](imetadataemit-interface.md) interface primarily to provide the ability to work with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1edff-104">方法</span><span class="sxs-lookup"><span data-stu-id="1edff-104">Methods</span></span>  
  
|<span data-ttu-id="1edff-105">方法</span><span class="sxs-lookup"><span data-stu-id="1edff-105">Method</span></span>|<span data-ttu-id="1edff-106">说明</span><span class="sxs-lookup"><span data-stu-id="1edff-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1edff-107">DefineGenericParam 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-107">DefineGenericParam Method</span></span>](imetadataemit2-definegenericparam-method.md)|<span data-ttu-id="1edff-108">创建泛型类型参数的定义，并获取该泛型类型参数的令牌。</span><span class="sxs-lookup"><span data-stu-id="1edff-108">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>|  
|[<span data-ttu-id="1edff-109">DefineMethodSpec 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-109">DefineMethodSpec Method</span></span>](imetadataemit2-definemethodspec-method.md)|<span data-ttu-id="1edff-110">创建方法的泛型实例，并获取定义的标记。</span><span class="sxs-lookup"><span data-stu-id="1edff-110">Creates a generic instance of a method, and gets a token to the definition.</span></span>|  
|[<span data-ttu-id="1edff-111">GetDeltaSaveSize 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-111">GetDeltaSaveSize Method</span></span>](imetadataemit2-getdeltasavesize-method.md)|<span data-ttu-id="1edff-112">获取一个值，该值指示为当前的 "编辑并继续" 会话表示更改所需的数据的大小差异。</span><span class="sxs-lookup"><span data-stu-id="1edff-112">Gets a value indicating the difference in size of the data that is required to express the changes for the current edit-and-continue session.</span></span>|  
|[<span data-ttu-id="1edff-113">ResetENCLog 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-113">ResetENCLog Method</span></span>](imetadataemit2-resetenclog-method.md)|<span data-ttu-id="1edff-114">重置编辑并继续日志并启动新的会话。</span><span class="sxs-lookup"><span data-stu-id="1edff-114">Resets the edit-and-continue log and starts a new session.</span></span>|  
|[<span data-ttu-id="1edff-115">SaveDelta 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-115">SaveDelta Method</span></span>](imetadataemit2-savedelta-method.md)|<span data-ttu-id="1edff-116">将当前的 "编辑并继续" 会话中的更改保存到指定的文件。</span><span class="sxs-lookup"><span data-stu-id="1edff-116">Saves changes from the current edit-and-continue session to the specified file.</span></span>|  
|[<span data-ttu-id="1edff-117">SaveDeltaToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-117">SaveDeltaToMemory Method</span></span>](imetadataemit2-savedeltatomemory-method.md)|<span data-ttu-id="1edff-118">将当前的 "编辑并继续" 会话中的更改保存到内存。</span><span class="sxs-lookup"><span data-stu-id="1edff-118">Saves changes from the current edit-and-continue session to memory.</span></span>|  
|[<span data-ttu-id="1edff-119">SaveDeltaToStream 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-119">SaveDeltaToStream Method</span></span>](imetadataemit2-savedeltatostream-method.md)|<span data-ttu-id="1edff-120">将当前的 "编辑并继续" 会话中的更改保存到指定的流。</span><span class="sxs-lookup"><span data-stu-id="1edff-120">Saves changes from the current edit-and-continue session to the specified stream.</span></span>|  
|[<span data-ttu-id="1edff-121">SetGenericParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="1edff-121">SetGenericParamProps Method</span></span>](imetadataemit2-setgenericparamprops-method.md)|<span data-ttu-id="1edff-122">设置指定的标记所引用的泛型参数定义的属性值。</span><span class="sxs-lookup"><span data-stu-id="1edff-122">Sets property values for the generic parameter definition referenced by the specified token.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1edff-123">要求</span><span class="sxs-lookup"><span data-stu-id="1edff-123">Requirements</span></span>  

 <span data-ttu-id="1edff-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1edff-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1edff-125">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1edff-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1edff-126">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1edff-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1edff-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1edff-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1edff-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1edff-128">See also</span></span>

- [<span data-ttu-id="1edff-129">元数据接口</span><span class="sxs-lookup"><span data-stu-id="1edff-129">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="1edff-130">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="1edff-130">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
