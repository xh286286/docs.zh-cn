---
title: ICorDebugHandleValue::Dispose 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue.Dispose
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue::Dispose
helpviewer_keywords:
- ICorDebugHandleValue::Dispose method [.NET Framework debugging]
- Dispose method [.NET Framework debugging]
ms.assetid: c1542811-0a7f-4235-bcfd-b24370d6f24b
topic_type:
- apiref
ms.openlocfilehash: dc24afd8f78a900ea52539bf9dcb522287223c4c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705626"
---
# <a name="icordebughandlevaluedispose-method"></a><span data-ttu-id="6cfac-102">ICorDebugHandleValue::Dispose 方法</span><span class="sxs-lookup"><span data-stu-id="6cfac-102">ICorDebugHandleValue::Dispose Method</span></span>

<span data-ttu-id="6cfac-103">释放此 ICorDebugHandleValue 对象引用的句柄，无需显式释放接口指针。</span><span class="sxs-lookup"><span data-stu-id="6cfac-103">Releases the handle referenced by this ICorDebugHandleValue object without explicitly releasing the interface pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cfac-104">语法</span><span class="sxs-lookup"><span data-stu-id="6cfac-104">Syntax</span></span>  
  
```cpp  
HRESULT Dispose ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="6cfac-105">要求</span><span class="sxs-lookup"><span data-stu-id="6cfac-105">Requirements</span></span>  

 <span data-ttu-id="6cfac-106">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6cfac-106">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6cfac-107">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6cfac-107">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6cfac-108">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6cfac-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6cfac-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6cfac-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
