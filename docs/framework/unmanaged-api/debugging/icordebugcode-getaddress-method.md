---
title: ICorDebugCode::GetAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetAddress
helpviewer_keywords:
- GetAddress method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetAddress method [.NET Framework debugging]
ms.assetid: cc507cb0-df2e-49c2-b32e-0c3271a8df9a
topic_type:
- apiref
ms.openlocfilehash: c796e3782a498c798c9b47f028ef05c2de00f54d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717662"
---
# <a name="icordebugcodegetaddress-method"></a><span data-ttu-id="babf2-102">ICorDebugCode::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="babf2-102">ICorDebugCode::GetAddress Method</span></span>

<span data-ttu-id="babf2-103">获取此 "ICorDebugCode" 接口表示的代码段 (RVA) 的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="babf2-103">Gets the relative virtual address (RVA) of the code segment that this "ICorDebugCode" interface represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="babf2-104">语法</span><span class="sxs-lookup"><span data-stu-id="babf2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS *pStart  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="babf2-105">参数</span><span class="sxs-lookup"><span data-stu-id="babf2-105">Parameters</span></span>  

 `pStart`  
 <span data-ttu-id="babf2-106">弄指向代码段的 RVA 的指针。</span><span class="sxs-lookup"><span data-stu-id="babf2-106">[out] A pointer to the RVA of the code segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="babf2-107">要求</span><span class="sxs-lookup"><span data-stu-id="babf2-107">Requirements</span></span>  

 <span data-ttu-id="babf2-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="babf2-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="babf2-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="babf2-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="babf2-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="babf2-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="babf2-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="babf2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
