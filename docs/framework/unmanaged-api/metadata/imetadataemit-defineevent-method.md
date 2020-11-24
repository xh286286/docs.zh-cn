---
title: IMetaDataEmit::DefineEvent 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineEvent
helpviewer_keywords:
- IMetaDataEmit::DefineEvent method [.NET Framework metadata]
- DefineEvent method [.NET Framework metadata]
ms.assetid: cf064bac-9a9f-41c5-9e1d-108ff7af3afe
topic_type:
- apiref
ms.openlocfilehash: 3c03497f48b8199da545d796637e5f8a5c532362
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675680"
---
# <a name="imetadataemitdefineevent-method"></a><span data-ttu-id="955c0-102">IMetaDataEmit::DefineEvent 方法</span><span class="sxs-lookup"><span data-stu-id="955c0-102">IMetaDataEmit::DefineEvent Method</span></span>

<span data-ttu-id="955c0-103">使用指定的元数据签名创建事件的定义，并获取该事件定义的标记。</span><span class="sxs-lookup"><span data-stu-id="955c0-103">Creates a definition for an event with the specified metadata signature, and gets a token to that event definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="955c0-104">语法</span><span class="sxs-lookup"><span data-stu-id="955c0-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineEvent (
    [in]  mdTypeDef    td,
    [in]  LPCWSTR      szEvent,
    [in]  DWORD        dwEventFlags,
    [in]  mdToken      tkEventType,
    [in]  mdMethodDef  mdAddOn,
    [in]  mdMethodDef  mdRemoveOn,
    [in]  mdMethodDef  mdFire,
    [in]  mdMethodDef  rmdOtherMethods[],
    [out] mdEvent      *pmdEvent
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="955c0-105">参数</span><span class="sxs-lookup"><span data-stu-id="955c0-105">Parameters</span></span>  

 `td`  
 <span data-ttu-id="955c0-106">中目标类或接口的标记。</span><span class="sxs-lookup"><span data-stu-id="955c0-106">[in] The token for the target class or interface.</span></span> <span data-ttu-id="955c0-107">这是 `mdTypeDef` 或 `mdTypeDefNil` 令牌。</span><span class="sxs-lookup"><span data-stu-id="955c0-107">This is either a `mdTypeDef` or `mdTypeDefNil` token.</span></span>  
  
 `szEvent`  
 <span data-ttu-id="955c0-108">中事件的名称。</span><span class="sxs-lookup"><span data-stu-id="955c0-108">[in] The name of the event.</span></span>  
  
 `dwEventFlags`  
 <span data-ttu-id="955c0-109">中事件标志。</span><span class="sxs-lookup"><span data-stu-id="955c0-109">[in] Event flags.</span></span>  
  
 `tkEventType`  
 <span data-ttu-id="955c0-110">中事件类的标记。</span><span class="sxs-lookup"><span data-stu-id="955c0-110">[in] The token for the event class.</span></span> <span data-ttu-id="955c0-111">这是 `mdTypeDef` 、 `mdTypeRef` 或 `mdTokenNil` 标记。</span><span class="sxs-lookup"><span data-stu-id="955c0-111">This is a `mdTypeDef`, a `mdTypeRef`, or a `mdTokenNil` token.</span></span>  
  
 `mdAddOn`  
 <span data-ttu-id="955c0-112">中用于订阅事件的方法，或为 null。</span><span class="sxs-lookup"><span data-stu-id="955c0-112">[in] The method used to subscribe to the event, or null.</span></span>  
  
 `mdRemoveOn`  
 <span data-ttu-id="955c0-113">中用于取消订阅事件的方法，或为 null。</span><span class="sxs-lookup"><span data-stu-id="955c0-113">[in] The method used to unsubscribe to the event, or null.</span></span>  
  
 `mdFire`  
 <span data-ttu-id="955c0-114">中派生类 (用来引发事件) 的方法。</span><span class="sxs-lookup"><span data-stu-id="955c0-114">[in] The method used (by a derived class) to raise the event.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="955c0-115">中与事件关联的其他方法的标记数组。</span><span class="sxs-lookup"><span data-stu-id="955c0-115">[in] An array of tokens for other methods associated with the event.</span></span> <span data-ttu-id="955c0-116">使用标记终止数组 `mdMethodDefNil` 。</span><span class="sxs-lookup"><span data-stu-id="955c0-116">The array is terminated with a `mdMethodDefNil` token.</span></span>  
  
 `pmdEvent`  
 <span data-ttu-id="955c0-117">弄分配给事件的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="955c0-117">[out] The metadata token assigned to the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="955c0-118">要求</span><span class="sxs-lookup"><span data-stu-id="955c0-118">Requirements</span></span>  

 <span data-ttu-id="955c0-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="955c0-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="955c0-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="955c0-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="955c0-121">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="955c0-121">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="955c0-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="955c0-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="955c0-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="955c0-123">See also</span></span>

- [<span data-ttu-id="955c0-124">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="955c0-124">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="955c0-125">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="955c0-125">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
