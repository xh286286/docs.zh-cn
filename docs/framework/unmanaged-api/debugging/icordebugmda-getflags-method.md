---
title: ICorDebugMDA::GetFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetFlags
helpviewer_keywords:
- ICorDebugMDA::GetFlags method [.NET Framework debugging]
- GetFlags method [.NET Framework debugging]
ms.assetid: 87ce7c5b-fd82-453e-bf55-c8a32150b183
topic_type:
- apiref
ms.openlocfilehash: 38a5c2da900530b6bf78f24e224714496ceaa62c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710956"
---
# <a name="icordebugmdagetflags-method"></a><span data-ttu-id="13003-102">ICorDebugMDA::GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="13003-102">ICorDebugMDA::GetFlags Method</span></span>

<span data-ttu-id="13003-103">获取与托管调试助手关联的标志 (MDA) [ICorDebugMDA](icordebugmda-interface.md)表示。</span><span class="sxs-lookup"><span data-stu-id="13003-103">Gets the flags associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13003-104">语法</span><span class="sxs-lookup"><span data-stu-id="13003-104">Syntax</span></span>  
  
```cpp  
HRESULT GetFlags (  
    [in] CorDebugMDAFlags *pFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13003-105">参数</span><span class="sxs-lookup"><span data-stu-id="13003-105">Parameters</span></span>  

 `pFlags`  
 <span data-ttu-id="13003-106">中 [CorDebugMDAFlags](cordebugmdaflags-enumeration.md) 枚举值的按位组合，这些值指定此 MDA 的标志的设置。</span><span class="sxs-lookup"><span data-stu-id="13003-106">[in] A bitwise combination of the [CorDebugMDAFlags](cordebugmdaflags-enumeration.md) enumeration values that specify the settings of the flags for this MDA.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13003-107">要求</span><span class="sxs-lookup"><span data-stu-id="13003-107">Requirements</span></span>  

 <span data-ttu-id="13003-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13003-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13003-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="13003-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="13003-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13003-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13003-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13003-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13003-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="13003-112">See also</span></span>

- [<span data-ttu-id="13003-113">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="13003-113">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="13003-114">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="13003-114">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
