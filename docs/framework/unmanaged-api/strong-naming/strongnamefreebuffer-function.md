---
title: StrongNameFreeBuffer 函数
ms.date: 03/30/2017
api_name:
- StrongNameFreeBuffer
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameFreeBuffer
helpviewer_keywords:
- StrongNameFreeBuffer function [.NET Framework strong naming]
ms.assetid: eda21ecf-4734-4f92-aaba-9f34884385db
topic_type:
- apiref
ms.openlocfilehash: d93bda046a79dbdec2195eee48fefc1e5538b2e4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732250"
---
# <a name="strongnamefreebuffer-function"></a><span data-ttu-id="76850-102">StrongNameFreeBuffer 函数</span><span class="sxs-lookup"><span data-stu-id="76850-102">StrongNameFreeBuffer Function</span></span>

<span data-ttu-id="76850-103">释放先前调用 [StrongNameGetPublicKey](strongnamegetpublickey-function.md)、[StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md) 或 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md) 强名称函数分配的内存。</span><span class="sxs-lookup"><span data-stu-id="76850-103">Frees memory that was allocated with a previous call to a strong name function such as [StrongNameGetPublicKey](strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md), or [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md).</span></span>  
  
 <span data-ttu-id="76850-104">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="76850-104">This function has been deprecated.</span></span> <span data-ttu-id="76850-105">改为使用 [ICLRStrongName：： StrongNameFreeBuffer](../hosting/iclrstrongname-strongnamefreebuffer-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="76850-105">Use the [ICLRStrongName::StrongNameFreeBuffer](../hosting/iclrstrongname-strongnamefreebuffer-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76850-106">语法</span><span class="sxs-lookup"><span data-stu-id="76850-106">Syntax</span></span>  
  
```cpp  
VOID StrongNameFreeBuffer (
   [in] BYTE   *pbMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="76850-107">参数</span><span class="sxs-lookup"><span data-stu-id="76850-107">Parameters</span></span>  

 `pbMemory`  
 <span data-ttu-id="76850-108">中指向要释放的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="76850-108">[in] A pointer to the memory to free.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76850-109">要求</span><span class="sxs-lookup"><span data-stu-id="76850-109">Requirements</span></span>  

 <span data-ttu-id="76850-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="76850-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76850-111">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="76850-111">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="76850-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="76850-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="76850-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76850-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76850-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76850-114">See also</span></span>

- [<span data-ttu-id="76850-115">StrongNameFreeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="76850-115">StrongNameFreeBuffer Method</span></span>](../hosting/iclrstrongname-strongnamefreebuffer-method.md)
- [<span data-ttu-id="76850-116">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="76850-116">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
