---
title: ICorPublishAppDomainEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum::Next
helpviewer_keywords:
- Next method, ICorPublishAppDomainEnum interface [.NET Framework debugging]
- ICorPublishAppDomainEnum::Next method [.NET Framework debugging]
ms.assetid: ad37cd10-0339-4d08-9b0e-4b3428bb4dc3
topic_type:
- apiref
ms.openlocfilehash: 00aff9ab4edbbebe4b924d335fa12f92e9840737
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95693692"
---
# <a name="icorpublishappdomainenumnext-method"></a><span data-ttu-id="0074b-102">ICorPublishAppDomainEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="0074b-102">ICorPublishAppDomainEnum::Next Method</span></span>

<span data-ttu-id="0074b-103">从当前位置开始，获取进程中当前存在的指定数量的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="0074b-103">Gets the specified number of application domains that currently exist in the process, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0074b-104">语法</span><span class="sxs-lookup"><span data-stu-id="0074b-104">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]
        ICorPublishAppDomain **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0074b-105">参数</span><span class="sxs-lookup"><span data-stu-id="0074b-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="0074b-106">中要检索的元素的数目。</span><span class="sxs-lookup"><span data-stu-id="0074b-106">[in] The number of elements to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="0074b-107">弄一个指针，指向检索到的 [ICorPublishAppDomain](icorpublishappdomain-interface.md) 对象的数组，其中每个对象都表示一个应用程序域。</span><span class="sxs-lookup"><span data-stu-id="0074b-107">[out] A pointer to the array of retrieved [ICorPublishAppDomain](icorpublishappdomain-interface.md) objects, each of which represents an application domain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="0074b-108">弄一个指针，指向实际返回的应用程序域的数量。</span><span class="sxs-lookup"><span data-stu-id="0074b-108">[out] Pointer to the number of application domains actually returned.</span></span> <span data-ttu-id="0074b-109">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="0074b-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0074b-110">要求</span><span class="sxs-lookup"><span data-stu-id="0074b-110">Requirements</span></span>  

 <span data-ttu-id="0074b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0074b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0074b-112">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="0074b-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="0074b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0074b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0074b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0074b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0074b-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0074b-115">See also</span></span>

- [<span data-ttu-id="0074b-116">ICorPublishAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="0074b-116">ICorPublishAppDomainEnum Interface</span></span>](icorpublishappdomainenum-interface.md)
