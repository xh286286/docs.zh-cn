---
title: ICorPublish::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorPublish.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish::GetProcess
helpviewer_keywords:
- ICorPublish::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorPublish interface [.NET Framework debugging]
ms.assetid: c5143805-2eb7-45b8-85ed-c8fb34df1084
topic_type:
- apiref
ms.openlocfilehash: a45f613b7547e2e80abdbd8ac85cb0b2b6a499e5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95716884"
---
# <a name="icorpublishgetprocess-method"></a><span data-ttu-id="9ad0d-102">ICorPublish::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="9ad0d-102">ICorPublish::GetProcess Method</span></span>

<span data-ttu-id="9ad0d-103">获取一个表示具有指定标识符的进程的 [ICorPublishProcess](icorpublishprocess-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="9ad0d-103">Gets an [ICorPublishProcess](icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ad0d-104">语法</span><span class="sxs-lookup"><span data-stu-id="9ad0d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess(  
    [in] unsigned              pid,
    [out] ICorPublishProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ad0d-105">参数</span><span class="sxs-lookup"><span data-stu-id="9ad0d-105">Parameters</span></span>  

 `pid`  
 <span data-ttu-id="9ad0d-106">中进程的标识符。</span><span class="sxs-lookup"><span data-stu-id="9ad0d-106">[in] The identifier of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="9ad0d-107">弄一个指针，指向 `ICorPublishProcess` 表示进程的实例的地址。</span><span class="sxs-lookup"><span data-stu-id="9ad0d-107">[out] A pointer to the address of an `ICorPublishProcess` instance that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9ad0d-108">注解</span><span class="sxs-lookup"><span data-stu-id="9ad0d-108">Remarks</span></span>  

 <span data-ttu-id="9ad0d-109">`GetProcess` 如果进程不存在，或者不是可由当前用户调试的托管进程，则会失败。</span><span class="sxs-lookup"><span data-stu-id="9ad0d-109">`GetProcess` fails if the process doesn't exist, or isn't a managed process that can be debugged by the current user.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ad0d-110">要求</span><span class="sxs-lookup"><span data-stu-id="9ad0d-110">Requirements</span></span>  

 <span data-ttu-id="9ad0d-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad0d-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ad0d-112">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="9ad0d-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="9ad0d-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ad0d-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ad0d-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ad0d-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ad0d-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ad0d-115">See also</span></span>

- [<span data-ttu-id="9ad0d-116">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="9ad0d-116">ICorPublish Interface</span></span>](icorpublish-interface.md)
