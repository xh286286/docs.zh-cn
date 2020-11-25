---
title: ITypeName::GetNames 方法
ms.date: 03/30/2017
api_name:
- ITypeName.GetNames
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetNames
helpviewer_keywords:
- ITypeName::GetNames method [.NET Framework hosting]
- GetNames method [.NET Framework hosting]
ms.assetid: e2a3637b-d1e9-4d93-9e9b-0555fbff793d
topic_type:
- apiref
ms.openlocfilehash: 91e73f8e3d2e3c372d3fe1c4fd4fccf6ff67b363
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727804"
---
# <a name="itypenamegetnames-method"></a><span data-ttu-id="fb2f1-102">ITypeName::GetNames 方法</span><span class="sxs-lookup"><span data-stu-id="fb2f1-102">ITypeName::GetNames Method</span></span>

<span data-ttu-id="fb2f1-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb2f1-104">语法</span><span class="sxs-lookup"><span data-stu-id="fb2f1-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNames (  
    [in] DWORD           count,  
    [out] BSTR*          rgbszNames,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="fb2f1-105">要求</span><span class="sxs-lookup"><span data-stu-id="fb2f1-105">Requirements</span></span>  

 <span data-ttu-id="fb2f1-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb2f1-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="fb2f1-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fb2f1-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fb2f1-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fb2f1-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fb2f1-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb2f1-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb2f1-110">See also</span></span>

- [<span data-ttu-id="fb2f1-111">承载接口</span><span class="sxs-lookup"><span data-stu-id="fb2f1-111">Hosting Interfaces</span></span>](hosting-interfaces.md)
