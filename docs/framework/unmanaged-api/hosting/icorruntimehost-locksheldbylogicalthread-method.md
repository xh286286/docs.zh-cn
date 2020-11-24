---
title: ICorRuntimeHost::LocksHeldByLogicalThread 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.LocksHeldByLogicalThread
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread
helpviewer_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread method [.NET Framework hosting]
- LocksHeldByLogicalThread method [.NET Framework hosting]
ms.assetid: c3601255-d894-4d7c-b1df-c31334551700
topic_type:
- apiref
ms.openlocfilehash: 16f34d91861f9fcae51691ab13549bdf1ef333a7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671494"
---
# <a name="icorruntimehostlocksheldbylogicalthread-method"></a><span data-ttu-id="9f65c-102">ICorRuntimeHost::LocksHeldByLogicalThread 方法</span><span class="sxs-lookup"><span data-stu-id="9f65c-102">ICorRuntimeHost::LocksHeldByLogicalThread Method</span></span>

<span data-ttu-id="9f65c-103">检索当前线程所持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="9f65c-103">Retrieves the number of locks that current thread holds.</span></span>  
  
 <span data-ttu-id="9f65c-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="9f65c-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f65c-105">语法</span><span class="sxs-lookup"><span data-stu-id="9f65c-105">Syntax</span></span>  
  
```cpp  
HRESULT LocksHeldByLogicalThread(  
    [out] DWORD *pCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9f65c-106">参数</span><span class="sxs-lookup"><span data-stu-id="9f65c-106">Parameters</span></span>  

 `pCount`  
 <span data-ttu-id="9f65c-107">弄一个指针，指向当前线程所持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="9f65c-107">[out] A pointer to the number of locks that the current thread holds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f65c-108">要求</span><span class="sxs-lookup"><span data-stu-id="9f65c-108">Requirements</span></span>  

 <span data-ttu-id="9f65c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9f65c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f65c-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9f65c-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9f65c-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f65c-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9f65c-112">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="9f65c-112">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f65c-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9f65c-113">See also</span></span>

- [<span data-ttu-id="9f65c-114">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="9f65c-114">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
