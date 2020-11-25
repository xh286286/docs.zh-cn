---
title: ICorDebugModule2::GetJITCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.GetJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::GetJITCompilerFlags
helpviewer_keywords:
- GetJITCompilerFlags method [.NET Framework debugging]
- ICorDebugModule2::GetJITCompilerFlags method [.NET Framework debugging]
ms.assetid: 7212d9f4-989b-44e3-b8d4-ffc35922f6a0
topic_type:
- apiref
ms.openlocfilehash: c443fba711a3d122ed5f8f1566a220c79211631e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709669"
---
# <a name="icordebugmodule2getjitcompilerflags-method"></a><span data-ttu-id="e4911-102">ICorDebugModule2::GetJITCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="e4911-102">ICorDebugModule2::GetJITCompilerFlags Method</span></span>

<span data-ttu-id="e4911-103">获取用于控制此 ICorDebugModule2 的实时 (JIT) 编译的标志。</span><span class="sxs-lookup"><span data-stu-id="e4911-103">Gets the flags that control the just-in-time (JIT) compilation of this ICorDebugModule2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4911-104">语法</span><span class="sxs-lookup"><span data-stu-id="e4911-104">Syntax</span></span>  
  
```cpp  
HRESULT GetJITCompilerFlags (  
    [out] DWORD   *pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4911-105">参数</span><span class="sxs-lookup"><span data-stu-id="e4911-105">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="e4911-106">弄指向控制 JIT 编译的 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的值的指针。</span><span class="sxs-lookup"><span data-stu-id="e4911-106">[out] A pointer to a value of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration that controls the JIT compilation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4911-107">要求</span><span class="sxs-lookup"><span data-stu-id="e4911-107">Requirements</span></span>  

 <span data-ttu-id="e4911-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4911-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4911-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4911-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4911-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4911-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4911-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4911-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
