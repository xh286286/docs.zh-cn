---
title: ICorDebugModule::GetAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetAssembly
helpviewer_keywords:
- ICorDebugModule::GetAssembly method [.NET Framework debugging]
- GetAssembly method [.NET Framework debugging]
ms.assetid: 989762c4-3d15-4485-b8ee-69e0fa8ec895
topic_type:
- apiref
ms.openlocfilehash: e0ae11ee24a5e25fb439d5c502c4cda5bcb6a80e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710254"
---
# <a name="icordebugmodulegetassembly-method"></a><span data-ttu-id="9ae2d-102">ICorDebugModule::GetAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="9ae2d-102">ICorDebugModule::GetAssembly Method</span></span>

<span data-ttu-id="9ae2d-103">获取包含此模块的程序集。</span><span class="sxs-lookup"><span data-stu-id="9ae2d-103">Gets the containing assembly for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ae2d-104">语法</span><span class="sxs-lookup"><span data-stu-id="9ae2d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAssembly(  
    [out] ICorDebugAssembly **ppAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ae2d-105">参数</span><span class="sxs-lookup"><span data-stu-id="9ae2d-105">Parameters</span></span>  

 `ppAssembly`  
 <span data-ttu-id="9ae2d-106">弄指向 ICorDebugAssembly 对象的指针，该对象表示包含此模块的程序集。</span><span class="sxs-lookup"><span data-stu-id="9ae2d-106">[out] A pointer to an ICorDebugAssembly object that represents the assembly containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ae2d-107">要求</span><span class="sxs-lookup"><span data-stu-id="9ae2d-107">Requirements</span></span>  

 <span data-ttu-id="9ae2d-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae2d-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ae2d-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ae2d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ae2d-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ae2d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ae2d-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ae2d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
