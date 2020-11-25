---
title: IAssemblyName::GetVersion 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetVersion
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetVersion
helpviewer_keywords:
- IAssemblyName::GetVersion method [.NET Framework fusion]
- GetVersion method, IAssemblyName interface [.NET Framework fusion]
ms.assetid: 42230928-2c33-41fd-9519-d96efef6c7af
topic_type:
- apiref
ms.openlocfilehash: 6f37979c7a4873a7751db0296dc7d485c3444561
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715896"
---
# <a name="iassemblynamegetversion-method"></a><span data-ttu-id="613ad-102">IAssemblyName::GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="613ad-102">IAssemblyName::GetVersion Method</span></span>

<span data-ttu-id="613ad-103">获取此 [IAssemblyName](iassemblyname-interface.md) 对象所引用的程序集的版本信息。</span><span class="sxs-lookup"><span data-stu-id="613ad-103">Gets the version information for the assembly referenced by this [IAssemblyName](iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="613ad-104">语法</span><span class="sxs-lookup"><span data-stu-id="613ad-104">Syntax</span></span>  
  
```cpp  
HRESULT GetVersion (  
    [out] LPDWORD pdwVersionHi,  
    [out] LPDWORD pdwVersionLow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="613ad-105">参数</span><span class="sxs-lookup"><span data-stu-id="613ad-105">Parameters</span></span>  

 `pdwVersionHi`  
 <span data-ttu-id="613ad-106">弄版本的高32位。</span><span class="sxs-lookup"><span data-stu-id="613ad-106">[out] The high 32 bits of the version.</span></span>  
  
 `pdwVersionLow`  
 <span data-ttu-id="613ad-107">弄版本的低32位。</span><span class="sxs-lookup"><span data-stu-id="613ad-107">[out] The low 32 bits of the version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="613ad-108">要求</span><span class="sxs-lookup"><span data-stu-id="613ad-108">Requirements</span></span>  

 <span data-ttu-id="613ad-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="613ad-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="613ad-110">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="613ad-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="613ad-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="613ad-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="613ad-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="613ad-112">See also</span></span>

- [<span data-ttu-id="613ad-113">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="613ad-113">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
