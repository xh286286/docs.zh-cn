---
title: ICorDebugAppDomain::EnumerateBreakpoints 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateBreakpoints
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints method [.NET Framework debugging]
- EnumerateBreakpoints method [.NET Framework debugging]
ms.assetid: 206069c5-25cb-4794-9d69-67c5aa7ed0af
topic_type:
- apiref
ms.openlocfilehash: 20c8a1987e48a88a3b8c92cf9f36fb58166cda9e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715974"
---
# <a name="icordebugappdomainenumeratebreakpoints-method"></a><span data-ttu-id="e5687-102">ICorDebugAppDomain::EnumerateBreakpoints 方法</span><span class="sxs-lookup"><span data-stu-id="e5687-102">ICorDebugAppDomain::EnumerateBreakpoints Method</span></span>

<span data-ttu-id="e5687-103">获取应用程序域中所有活动断点的枚举器。</span><span class="sxs-lookup"><span data-stu-id="e5687-103">Gets an enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5687-104">语法</span><span class="sxs-lookup"><span data-stu-id="e5687-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateBreakpoints (  
    [out] ICorDebugBreakpointEnum   **ppBreakpoints  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5687-105">参数</span><span class="sxs-lookup"><span data-stu-id="e5687-105">Parameters</span></span>  

 `ppBreakpoints`  
 <span data-ttu-id="e5687-106">弄指向 ICorDebugBreakpointEnum 对象地址的指针，该对象是应用程序域中所有活动断点的枚举器。</span><span class="sxs-lookup"><span data-stu-id="e5687-106">[out] A pointer to the address of an ICorDebugBreakpointEnum object that is the enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e5687-107">注解</span><span class="sxs-lookup"><span data-stu-id="e5687-107">Remarks</span></span>  

 <span data-ttu-id="e5687-108">枚举器包含所有类型的断点，包括函数断点和数据断点。</span><span class="sxs-lookup"><span data-stu-id="e5687-108">The enumerator includes all types of breakpoints, including function breakpoints and data breakpoints.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5687-109">要求</span><span class="sxs-lookup"><span data-stu-id="e5687-109">Requirements</span></span>  

 <span data-ttu-id="e5687-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e5687-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5687-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e5687-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e5687-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5687-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5687-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5687-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
