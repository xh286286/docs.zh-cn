---
title: IDebuggerThreadControl::StartBlockingForDebugger 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
ms.openlocfilehash: 1e0cb52a6b9f03209256e5398415b4ec632fb5e5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705496"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a><span data-ttu-id="4b869-102">IDebuggerThreadControl::StartBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="4b869-102">IDebuggerThreadControl::StartBlockingForDebugger Method</span></span>

<span data-ttu-id="4b869-103">通知宿主调试服务即将开始阻塞所有线程。</span><span class="sxs-lookup"><span data-stu-id="4b869-103">Notifies the host that the debugging services are about to start blocking all threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b869-104">语法</span><span class="sxs-lookup"><span data-stu-id="4b869-104">Syntax</span></span>  
  
```cpp  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b869-105">参数</span><span class="sxs-lookup"><span data-stu-id="4b869-105">Parameters</span></span>  

 `dwUnused`  
 <span data-ttu-id="4b869-106">中保留供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4b869-106">[in] Reserved for future use.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4b869-107">注解</span><span class="sxs-lookup"><span data-stu-id="4b869-107">Remarks</span></span>  

 <span data-ttu-id="4b869-108">`StartBlockingForDebugger`可以在运行时线程上调用方法。</span><span class="sxs-lookup"><span data-stu-id="4b869-108">The `StartBlockingForDebugger` method could be called on a runtime thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b869-109">要求</span><span class="sxs-lookup"><span data-stu-id="4b869-109">Requirements</span></span>  

 <span data-ttu-id="4b869-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4b869-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b869-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4b869-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4b869-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4b869-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4b869-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b869-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b869-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b869-114">See also</span></span>

- [<span data-ttu-id="4b869-115">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="4b869-115">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)
