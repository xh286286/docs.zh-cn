---
title: DestroyICeeFileGen 函数
ms.date: 03/30/2017
api_name:
- DestroyICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- DestroyICeeFileGen
helpviewer_keywords:
- DestroyICeeFileGen function [.NET Framework hosting]
ms.assetid: dc1e2235-e721-4cb2-a0b8-6b0c030d7bab
topic_type:
- apiref
ms.openlocfilehash: 495d84470c559df13ea64b63dd00582f4335d4e3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673171"
---
# <a name="destroyiceefilegen-function"></a><span data-ttu-id="c679a-102">DestroyICeeFileGen 函数</span><span class="sxs-lookup"><span data-stu-id="c679a-102">DestroyICeeFileGen Function</span></span>

<span data-ttu-id="c679a-103">销毁 [ICeeFileGen](iceefilegen-class.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="c679a-103">Destroys an [ICeeFileGen](iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="c679a-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="c679a-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c679a-105">语法</span><span class="sxs-lookup"><span data-stu-id="c679a-105">Syntax</span></span>  
  
```cpp  
HRESULT DestroyICeeFileGen (  
    [in] ICeeFileGen  **ceeFileGen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c679a-106">参数</span><span class="sxs-lookup"><span data-stu-id="c679a-106">Parameters</span></span>  

 `ceeFileGen`  
 <span data-ttu-id="c679a-107">中 `ICeeFileGen` 要销毁的对象。</span><span class="sxs-lookup"><span data-stu-id="c679a-107">[in] The `ICeeFileGen` object to destroy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c679a-108">返回值</span><span class="sxs-lookup"><span data-stu-id="c679a-108">Return Value</span></span>  

 <span data-ttu-id="c679a-109">此方法返回标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="c679a-109">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c679a-110">注解</span><span class="sxs-lookup"><span data-stu-id="c679a-110">Remarks</span></span>  

 <span data-ttu-id="c679a-111">`DestroyICeeFileGen` 销毁 `ICeeFileGen` [CreateICeeFileGen](createiceefilegen-function.md) 函数创建的对象。</span><span class="sxs-lookup"><span data-stu-id="c679a-111">`DestroyICeeFileGen` destroys the `ICeeFileGen` object created by the [CreateICeeFileGen](createiceefilegen-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c679a-112">要求</span><span class="sxs-lookup"><span data-stu-id="c679a-112">Requirements</span></span>  

 <span data-ttu-id="c679a-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c679a-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c679a-114">**标头：** ICeeFileGen</span><span class="sxs-lookup"><span data-stu-id="c679a-114">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="c679a-115">**库：** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="c679a-115">**Library:** MSCorPE.dll</span></span>  
  
 <span data-ttu-id="c679a-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c679a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c679a-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c679a-117">See also</span></span>

- [<span data-ttu-id="c679a-118">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="c679a-118">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
