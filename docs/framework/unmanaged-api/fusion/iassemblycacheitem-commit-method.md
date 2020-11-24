---
title: IAssemblyCacheItem::Commit 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.Commit
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::Commit
helpviewer_keywords:
- IAssemblyCacheItem::Commit method [.NET Framework fusion]
- Commit method, IAssemblyCacheItem interface [.NET Framework fusion]
ms.assetid: c2321f17-f46f-4815-ae41-b28678753613
topic_type:
- apiref
ms.openlocfilehash: 2b7c10e82aca2b2ece7ea4d7209c1f3c9a456434
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95670402"
---
# <a name="iassemblycacheitemcommit-method"></a><span data-ttu-id="f68c9-102">IAssemblyCacheItem::Commit 方法</span><span class="sxs-lookup"><span data-stu-id="f68c9-102">IAssemblyCacheItem::Commit Method</span></span>

<span data-ttu-id="f68c9-103">将缓存的程序集引用提交到内存。</span><span class="sxs-lookup"><span data-stu-id="f68c9-103">Commits the cached assembly reference to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f68c9-104">语法</span><span class="sxs-lookup"><span data-stu-id="f68c9-104">Syntax</span></span>  
  
```cpp  
HRESULT Commit (  
    [in] DWORD dwFlags,
    [out, optional] ULONG *pulDisposition  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f68c9-105">参数</span><span class="sxs-lookup"><span data-stu-id="f68c9-105">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="f68c9-106">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="f68c9-106">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pulDisposition`  
 <span data-ttu-id="f68c9-107">[out，optional]一个指示操作结果的值。</span><span class="sxs-lookup"><span data-stu-id="f68c9-107">[out, optional] A value that indicates the result of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f68c9-108">要求</span><span class="sxs-lookup"><span data-stu-id="f68c9-108">Requirements</span></span>  

 <span data-ttu-id="f68c9-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f68c9-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f68c9-110">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="f68c9-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f68c9-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f68c9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f68c9-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f68c9-112">See also</span></span>

- [<span data-ttu-id="f68c9-113">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="f68c9-113">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)
