---
title: IMetaDataEmit::SetMethodProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetMethodProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetMethodProps
helpviewer_keywords:
- SetMethodProps method [.NET Framework metadata]
- IMetaDataEmit::SetMethodProps method [.NET Framework metadata]
ms.assetid: e0c6ac12-22ea-43f5-b799-8cda0faf3336
topic_type:
- apiref
ms.openlocfilehash: c461582cc22f7185ee2707db91be83bc1aa0ba4c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706828"
---
# <a name="imetadataemitsetmethodprops-method"></a><span data-ttu-id="8f277-102">IMetaDataEmit::SetMethodProps 方法</span><span class="sxs-lookup"><span data-stu-id="8f277-102">IMetaDataEmit::SetMethodProps Method</span></span>

<span data-ttu-id="8f277-103">设置或更新在指定的相对虚拟地址上存储的功能，该方法由之前对 IMetaDataEmit 的调用定义的方法 [：:D efinemethod](imetadataemit-definemethod-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8f277-103">Sets or updates the feature, stored at the specified relative virtual address, of a method defined by a prior call to [IMetaDataEmit::DefineMethod](imetadataemit-definemethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f277-104">语法</span><span class="sxs-lookup"><span data-stu-id="8f277-104">Syntax</span></span>  
  
```cpp  
HRESULT SetMethodProps (
    [in]  mdMethodDef md,
    [in]  DWORD       dwMethodFlags,  
    [in]  ULONG       ulCodeRVA,
    [in]  DWORD       dwImplFlags
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f277-105">参数</span><span class="sxs-lookup"><span data-stu-id="8f277-105">Parameters</span></span>  

 `md`  
 <span data-ttu-id="8f277-106">中要更改的方法的标记。</span><span class="sxs-lookup"><span data-stu-id="8f277-106">[in] The token for the method to be changed.</span></span>  
  
 `dwMethodFlags`  
 <span data-ttu-id="8f277-107">中成员特性。</span><span class="sxs-lookup"><span data-stu-id="8f277-107">[in] The member attributes.</span></span>  
  
 `ulCodeRVA`  
 <span data-ttu-id="8f277-108">中代码的地址。</span><span class="sxs-lookup"><span data-stu-id="8f277-108">[in] The address of the code.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="8f277-109">中方法的实现标志。</span><span class="sxs-lookup"><span data-stu-id="8f277-109">[in] The implementation flags for the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f277-110">要求</span><span class="sxs-lookup"><span data-stu-id="8f277-110">Requirements</span></span>  

 <span data-ttu-id="8f277-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f277-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f277-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8f277-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8f277-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8f277-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f277-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f277-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f277-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f277-115">See also</span></span>

- [<span data-ttu-id="8f277-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8f277-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8f277-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8f277-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
