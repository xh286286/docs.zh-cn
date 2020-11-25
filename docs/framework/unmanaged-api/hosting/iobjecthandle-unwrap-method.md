---
title: IObjectHandle::Unwrap 方法
ms.date: 03/30/2017
api_name:
- IObjectHandle.Unwrap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Unwrap
helpviewer_keywords:
- Unwrap method [.NET Framework hosting]
- IObjectHandle::Unwrap method [.NET Framework hosting]
ms.assetid: 794c6f8e-ed58-416b-b756-e864f2c958f7
topic_type:
- apiref
ms.openlocfilehash: 32b6d2c05a96658ab2b8ec1df288d2be05bb947f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730657"
---
# <a name="iobjecthandleunwrap-method"></a><span data-ttu-id="e1236-102">IObjectHandle::Unwrap 方法</span><span class="sxs-lookup"><span data-stu-id="e1236-102">IObjectHandle::Unwrap Method</span></span>

<span data-ttu-id="e1236-103">从间接寻址将按值封送对象解包。</span><span class="sxs-lookup"><span data-stu-id="e1236-103">Unwraps a marshal-by-value object from indirection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1236-104">语法</span><span class="sxs-lookup"><span data-stu-id="e1236-104">Syntax</span></span>  
  
```cpp  
HRESULT Unwrap (  
    [out, retval] VARIANT *ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e1236-105">参数</span><span class="sxs-lookup"><span data-stu-id="e1236-105">Parameters</span></span>  

 `ppv`  
 <span data-ttu-id="e1236-106">弄指向要解包的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="e1236-106">[out] A pointer to the object to be unwrapped.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1236-107">要求</span><span class="sxs-lookup"><span data-stu-id="e1236-107">Requirements</span></span>  

 <span data-ttu-id="e1236-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e1236-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1236-109">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e1236-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e1236-110">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e1236-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e1236-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e1236-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
