---
title: ICorDebugStringValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue
helpviewer_keywords:
- ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type:
- apiref
ms.openlocfilehash: cd6c5726b9a938d04cf4eb018ec9851c81d9c745
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697044"
---
# <a name="icordebugstringvalue-interface"></a><span data-ttu-id="e8126-102">ICorDebugStringValue 接口</span><span class="sxs-lookup"><span data-stu-id="e8126-102">ICorDebugStringValue Interface</span></span>

<span data-ttu-id="e8126-103">应用于字符串值的 ICorDebugHeapValue 的子类。</span><span class="sxs-lookup"><span data-stu-id="e8126-103">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e8126-104">方法</span><span class="sxs-lookup"><span data-stu-id="e8126-104">Methods</span></span>  
  
|<span data-ttu-id="e8126-105">方法</span><span class="sxs-lookup"><span data-stu-id="e8126-105">Method</span></span>|<span data-ttu-id="e8126-106">说明</span><span class="sxs-lookup"><span data-stu-id="e8126-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e8126-107">GetLength 方法</span><span class="sxs-lookup"><span data-stu-id="e8126-107">GetLength Method</span></span>](icordebugstringvalue-getlength-method.md)|<span data-ttu-id="e8126-108">获取此引用的字符串中的字符数 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="e8126-108">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="e8126-109">GetString 方法</span><span class="sxs-lookup"><span data-stu-id="e8126-109">GetString Method</span></span>](icordebugstringvalue-getstring-method.md)|<span data-ttu-id="e8126-110">获取此引用的字符串 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="e8126-110">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8126-111">注解</span><span class="sxs-lookup"><span data-stu-id="e8126-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e8126-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="e8126-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8126-113">要求</span><span class="sxs-lookup"><span data-stu-id="e8126-113">Requirements</span></span>  

 <span data-ttu-id="e8126-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8126-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8126-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e8126-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e8126-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8126-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8126-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8126-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8126-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8126-118">See also</span></span>

- [<span data-ttu-id="e8126-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="e8126-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
