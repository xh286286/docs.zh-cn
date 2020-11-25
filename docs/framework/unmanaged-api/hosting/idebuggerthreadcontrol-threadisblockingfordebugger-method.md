---
title: IDebuggerThreadControl::ThreadIsBlockingForDebugger 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ThreadIsBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForDebugger
helpviewer_keywords:
- ThreadIsBlockingForDebugger method [.NET Framework hosting]
- IDebuggerThreadControl::ThreadIsBlockingForDebugger method [.NET Framework hosting]
ms.assetid: d4d7cb2d-69da-48b3-879a-1a8a68c9bfa8
topic_type:
- apiref
ms.openlocfilehash: 8c2741d7db60781fef12293f3be0b515a55b7885
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705499"
---
# <a name="idebuggerthreadcontrolthreadisblockingfordebugger-method"></a><span data-ttu-id="a6212-102">IDebuggerThreadControl::ThreadIsBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="a6212-102">IDebuggerThreadControl::ThreadIsBlockingForDebugger Method</span></span>

<span data-ttu-id="a6212-103">向宿主通知发送此回调的线程即将在调试服务中阻止。</span><span class="sxs-lookup"><span data-stu-id="a6212-103">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6212-104">语法</span><span class="sxs-lookup"><span data-stu-id="a6212-104">Syntax</span></span>  
  
```cpp  
HRESULT ThreadIsBlockingForDebugger ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="a6212-105">备注</span><span class="sxs-lookup"><span data-stu-id="a6212-105">Remarks</span></span>  

 <span data-ttu-id="a6212-106">在 `ThreadIsBlockingForDebugger` 运行时线程上将始终调用方法。</span><span class="sxs-lookup"><span data-stu-id="a6212-106">The `ThreadIsBlockingForDebugger` method will always be called on a runtime thread.</span></span>  
  
 <span data-ttu-id="a6212-107">`ThreadIsBlockingForDebugger`方法使宿主有机会在线程阻塞时执行另一个操作。</span><span class="sxs-lookup"><span data-stu-id="a6212-107">The `ThreadIsBlockingForDebugger` method gives the host an opportunity to perform another action while the thread blocks.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6212-108">要求</span><span class="sxs-lookup"><span data-stu-id="a6212-108">Requirements</span></span>  

 <span data-ttu-id="a6212-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6212-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6212-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a6212-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a6212-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a6212-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a6212-112">**NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6212-112">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6212-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6212-113">See also</span></span>

- [<span data-ttu-id="a6212-114">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="a6212-114">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)
