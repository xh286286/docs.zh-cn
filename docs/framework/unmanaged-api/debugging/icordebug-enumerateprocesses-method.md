---
title: ICorDebug::EnumerateProcesses 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.EnumerateProcesses
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- EnumerateProcesses
helpviewer_keywords:
- EnumerateProcesses method [.NET Framework debugging]
- ICorDebug::EnumerateProcesses method [.NET Framework debugging]
ms.assetid: ba25d166-1d28-4f1d-aca2-de298bbca669
topic_type:
- apiref
ms.openlocfilehash: bf672c90cdbb9e9fb66105820a264a49601b38d7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723449"
---
# <a name="icordebugenumerateprocesses-method"></a><span data-ttu-id="29297-102">ICorDebug::EnumerateProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="29297-102">ICorDebug::EnumerateProcesses Method</span></span>

<span data-ttu-id="29297-103">获取正在调试的进程的枚举器。</span><span class="sxs-lookup"><span data-stu-id="29297-103">Gets an enumerator for the processes that are being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29297-104">语法</span><span class="sxs-lookup"><span data-stu-id="29297-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateProcesses (  
    [out] ICorDebugProcessEnum      **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="29297-105">参数</span><span class="sxs-lookup"><span data-stu-id="29297-105">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="29297-106">指向 ICorDebugProcessEnum 对象地址的指针，该对象是正在调试的进程的枚举器。</span><span class="sxs-lookup"><span data-stu-id="29297-106">A pointer to the address of an ICorDebugProcessEnum object that is the enumerator for the processes being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29297-107">要求</span><span class="sxs-lookup"><span data-stu-id="29297-107">Requirements</span></span>  

 <span data-ttu-id="29297-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="29297-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29297-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="29297-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="29297-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="29297-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="29297-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29297-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29297-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="29297-112">See also</span></span>

- [<span data-ttu-id="29297-113">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="29297-113">ICorDebug Interface</span></span>](icordebug-interface.md)
