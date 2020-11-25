---
title: ITypeName::GetAssemblyName 方法
ms.date: 03/30/2017
api_name:
- ITypeName.GetAssemblyName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetAssemblyName
helpviewer_keywords:
- ITypeName::GetAssemblyName method [.NET Framework hosting]
- GetAssemblyName method [.NET Framework hosting]
ms.assetid: 97801d99-f5f1-4a30-882f-959827093fac
topic_type:
- apiref
ms.openlocfilehash: 256c0ccf7a39992ebb14adfd820729f8351e1990
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725113"
---
# <a name="itypenamegetassemblyname-method"></a><span data-ttu-id="66eea-102">ITypeName::GetAssemblyName 方法</span><span class="sxs-lookup"><span data-stu-id="66eea-102">ITypeName::GetAssemblyName Method</span></span>

<span data-ttu-id="66eea-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="66eea-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66eea-104">语法</span><span class="sxs-lookup"><span data-stu-id="66eea-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyName (  
    [out, retval] BSTR* rgbszAssemblyNames  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="66eea-105">要求</span><span class="sxs-lookup"><span data-stu-id="66eea-105">Requirements</span></span>  

 <span data-ttu-id="66eea-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="66eea-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66eea-107">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="66eea-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="66eea-108">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="66eea-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="66eea-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66eea-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66eea-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66eea-110">See also</span></span>

- [<span data-ttu-id="66eea-111">承载接口</span><span class="sxs-lookup"><span data-stu-id="66eea-111">Hosting Interfaces</span></span>](hosting-interfaces.md)
