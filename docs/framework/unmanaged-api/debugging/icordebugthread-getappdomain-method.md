---
title: ICorDebugThread::GetAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetAppDomain
helpviewer_keywords:
- GetAppDomain method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetAppDomain method [.NET Framework debugging]
ms.assetid: 415b3d34-8b35-4b60-a318-140646cc83f8
topic_type:
- apiref
ms.openlocfilehash: 882176f381a7c5bc4a0297021b89a96948a1cea8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728064"
---
# <a name="icordebugthreadgetappdomain-method"></a><span data-ttu-id="f1aeb-102">ICorDebugThread::GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="f1aeb-102">ICorDebugThread::GetAppDomain Method</span></span>

<span data-ttu-id="f1aeb-103">获取一个接口指针，该指针指向此 ICorDebugThread 当前正在执行的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="f1aeb-103">Gets an interface pointer to the application domain in which this ICorDebugThread is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1aeb-104">语法</span><span class="sxs-lookup"><span data-stu-id="f1aeb-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1aeb-105">参数</span><span class="sxs-lookup"><span data-stu-id="f1aeb-105">Parameters</span></span>  

 `ppAppDomain`  
 <span data-ttu-id="f1aeb-106">弄指向 ICorDebugAppDomain 对象的指针，该对象表示此线程当前正在执行的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="f1aeb-106">[out] A pointer to an ICorDebugAppDomain object that represents the application domain in which this thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1aeb-107">要求</span><span class="sxs-lookup"><span data-stu-id="f1aeb-107">Requirements</span></span>  

 <span data-ttu-id="f1aeb-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1aeb-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1aeb-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f1aeb-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f1aeb-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f1aeb-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f1aeb-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1aeb-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
