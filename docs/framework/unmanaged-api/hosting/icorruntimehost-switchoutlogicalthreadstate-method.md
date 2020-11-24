---
title: ICorRuntimeHost::SwitchOutLogicalThreadState 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.SwitchOutLogicalThreadState
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState
helpviewer_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState method [.NET Framework hosting]
- SwitchOutLogicalThreadState method [.NET Framework hosting]
ms.assetid: e1968f0b-2675-4dc2-8507-46164e1df154
topic_type:
- apiref
ms.openlocfilehash: e41ead54b50b8b28ebd9ee9c97d15ca6c71e7313
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690117"
---
# <a name="icorruntimehostswitchoutlogicalthreadstate-method"></a><span data-ttu-id="94279-102">ICorRuntimeHost::SwitchOutLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="94279-102">ICorRuntimeHost::SwitchOutLogicalThreadState Method</span></span>

<span data-ttu-id="94279-103">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="94279-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94279-104">语法</span><span class="sxs-lookup"><span data-stu-id="94279-104">Syntax</span></span>  
  
```cpp  
HRESULT SwitchOutLogicalThreadState(  
    [out] DWORD **pFiberCookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94279-105">参数</span><span class="sxs-lookup"><span data-stu-id="94279-105">Parameters</span></span>  

 `pFiberCookie`  
 <span data-ttu-id="94279-106">弄指示要交换的纤程的 Cookie。</span><span class="sxs-lookup"><span data-stu-id="94279-106">[out] Cookie that indicates the fiber being switched out.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94279-107">要求</span><span class="sxs-lookup"><span data-stu-id="94279-107">Requirements</span></span>  

 <span data-ttu-id="94279-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94279-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94279-109">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="94279-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="94279-110">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="94279-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="94279-111">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="94279-111">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94279-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94279-112">See also</span></span>

- [<span data-ttu-id="94279-113">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="94279-113">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
