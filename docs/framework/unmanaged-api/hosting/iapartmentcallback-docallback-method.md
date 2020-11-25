---
title: IApartmentCallback::DoCallback 方法
ms.date: 03/30/2017
api_name:
- IApartmentCallback.DoCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- DoCallback
helpviewer_keywords:
- IApartmentCallback::DoCallback method [.NET Framework hosting]
- DoCallback method [.NET Framework hosting]
ms.assetid: 8edad30c-30ff-4bee-813c-75525a82fc93
topic_type:
- apiref
ms.openlocfilehash: e3031bf123ff9107b4cebc0723f1be0d423bdaec
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721746"
---
# <a name="iapartmentcallbackdocallback-method"></a><span data-ttu-id="77780-102">IApartmentCallback::DoCallback 方法</span><span class="sxs-lookup"><span data-stu-id="77780-102">IApartmentCallback::DoCallback Method</span></span>

<span data-ttu-id="77780-103">在单元内执行指定的函数。</span><span class="sxs-lookup"><span data-stu-id="77780-103">Executes the specified function within an apartment.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77780-104">语法</span><span class="sxs-lookup"><span data-stu-id="77780-104">Syntax</span></span>  
  
```cpp  
HRESULT _stdcall DoCallback(  
    [in] SIZE_T pFunc,  
    [in] SIZE_T pData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77780-105">参数</span><span class="sxs-lookup"><span data-stu-id="77780-105">Parameters</span></span>  

 `pFunc`  
 <span data-ttu-id="77780-106">中指向要在单元中执行的函数的指针。</span><span class="sxs-lookup"><span data-stu-id="77780-106">[in] A pointer to the function to be executed within the apartment.</span></span>  
  
 `pData`  
 <span data-ttu-id="77780-107">中指向函数的自变量的指针。</span><span class="sxs-lookup"><span data-stu-id="77780-107">[in] A pointer to the function's argument.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77780-108">要求</span><span class="sxs-lookup"><span data-stu-id="77780-108">Requirements</span></span>  

 <span data-ttu-id="77780-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77780-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77780-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="77780-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="77780-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="77780-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="77780-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77780-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77780-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77780-113">See also</span></span>

- [<span data-ttu-id="77780-114">IApartmentCallback 接口</span><span class="sxs-lookup"><span data-stu-id="77780-114">IApartmentCallback Interface</span></span>](iapartmentcallback-interface.md)
