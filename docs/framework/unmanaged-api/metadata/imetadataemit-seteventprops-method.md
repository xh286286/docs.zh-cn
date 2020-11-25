---
title: IMetaDataEmit::SetEventProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetEventProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetEventProps
helpviewer_keywords:
- IMetaDataEmit::SetEventProps method [.NET Framework metadata]
- SetEventProps method [.NET Framework metadata]
ms.assetid: 3b039e50-63ec-4730-99ff-2327408de477
topic_type:
- apiref
ms.openlocfilehash: 5c2880ac07f0317bc36ff4bbde68cd3a25febf52
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721980"
---
# <a name="imetadataemitseteventprops-method"></a><span data-ttu-id="fbf63-102">IMetaDataEmit::SetEventProps 方法</span><span class="sxs-lookup"><span data-stu-id="fbf63-102">IMetaDataEmit::SetEventProps Method</span></span>

<span data-ttu-id="fbf63-103">设置或更新通过之前对 IMetaDataEmit 的调用定义的事件的指定功能 [：:D efineevent](imetadataemit-defineevent-method.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf63-103">Sets or updates the specified feature of an event defined by a prior call to [IMetaDataEmit::DefineEvent](imetadataemit-defineevent-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbf63-104">语法</span><span class="sxs-lookup"><span data-stu-id="fbf63-104">Syntax</span></span>  
  
```cpp  
HRESULT SetEventProps (  
    [in]  mdEvent     ev,
    [in]  DWORD       dwEventFlags,
    [in]  mdToken     tkEventType,
    [in]  mdMethodDef mdAddOn,
    [in]  mdMethodDef mdRemoveOn,
    [in]  mdMethodDef mdFire,
    [in]  mdMethodDef rmdOtherMethods[]
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fbf63-105">参数</span><span class="sxs-lookup"><span data-stu-id="fbf63-105">Parameters</span></span>  

 `ev`  
 <span data-ttu-id="fbf63-106">中事件标记。</span><span class="sxs-lookup"><span data-stu-id="fbf63-106">[in] The event token.</span></span>  
  
 `dwEventFlags`  
 <span data-ttu-id="fbf63-107">中事件标志。</span><span class="sxs-lookup"><span data-stu-id="fbf63-107">[in] Event flags.</span></span> <span data-ttu-id="fbf63-108">这是一个值的位掩码 `CorEventAttr` 。</span><span class="sxs-lookup"><span data-stu-id="fbf63-108">This is a bitmask of `CorEventAttr` values.</span></span>  
  
 `tkEventType`  
 <span data-ttu-id="fbf63-109">中事件类的标记。</span><span class="sxs-lookup"><span data-stu-id="fbf63-109">[in] The token for the event class.</span></span> <span data-ttu-id="fbf63-110">这是 `mdTypeDef` 或 `mdTypeRef` 令牌。</span><span class="sxs-lookup"><span data-stu-id="fbf63-110">This is either a `mdTypeDef` or a `mdTypeRef` token.</span></span>  
  
 `mdAddOn`  
 <span data-ttu-id="fbf63-111">中用于订阅事件的方法，或为 null。</span><span class="sxs-lookup"><span data-stu-id="fbf63-111">[in] The method used to subscribe to the event, or null.</span></span>  
  
 `mdRemoveOn`  
 <span data-ttu-id="fbf63-112">中用于取消订阅事件的方法，或为 null。</span><span class="sxs-lookup"><span data-stu-id="fbf63-112">[in] The method used to unsubscribe to the event, or null.</span></span>  
  
 `mdFire`  
 <span data-ttu-id="fbf63-113">中派生类 (用来引发事件) 的方法。</span><span class="sxs-lookup"><span data-stu-id="fbf63-113">[in] The method used (by a derived class) to raise the event.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="fbf63-114">中与事件关联的其他方法的标记数组。</span><span class="sxs-lookup"><span data-stu-id="fbf63-114">[in] An array of tokens for other methods associated with the event.</span></span> <span data-ttu-id="fbf63-115">数组的最后一个元素必须是 `mdMethodDefNil` 。</span><span class="sxs-lookup"><span data-stu-id="fbf63-115">The last element of the array must be `mdMethodDefNil`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fbf63-116">要求</span><span class="sxs-lookup"><span data-stu-id="fbf63-116">Requirements</span></span>  

 <span data-ttu-id="fbf63-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf63-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fbf63-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="fbf63-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fbf63-119">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="fbf63-119">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fbf63-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fbf63-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbf63-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fbf63-121">See also</span></span>

- [<span data-ttu-id="fbf63-122">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="fbf63-122">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="fbf63-123">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="fbf63-123">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
