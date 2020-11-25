---
title: ICorDebugValue3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3
helpviewer_keywords:
- ICorDebugValue3 interface [.NET Framework debugging]
ms.assetid: 7d5385d3-f4a5-47c4-8478-a3513b5e9406
topic_type:
- apiref
ms.openlocfilehash: 419efc7f21f4ac2e68657b2a4d69a8690a2938d4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722305"
---
# <a name="icordebugvalue3-interface"></a><span data-ttu-id="a88f2-102">ICorDebugValue3 接口</span><span class="sxs-lookup"><span data-stu-id="a88f2-102">ICorDebugValue3 Interface</span></span>

<span data-ttu-id="a88f2-103">扩展了 "ICorDebugValue" 和 "ICorDebugValue2" 接口，为大于 2 GB 的数组提供支持。</span><span class="sxs-lookup"><span data-stu-id="a88f2-103">Extends the "ICorDebugValue" and "ICorDebugValue2" interfaces to provide support for arrays that are larger than 2 GB.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a88f2-104">方法</span><span class="sxs-lookup"><span data-stu-id="a88f2-104">Methods</span></span>  
  
|<span data-ttu-id="a88f2-105">方法</span><span class="sxs-lookup"><span data-stu-id="a88f2-105">Method</span></span>|<span data-ttu-id="a88f2-106">说明</span><span class="sxs-lookup"><span data-stu-id="a88f2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a88f2-107">GetSize64 方法</span><span class="sxs-lookup"><span data-stu-id="a88f2-107">GetSize64 Method</span></span>](icordebugvalue3-getsize64-method.md)|<span data-ttu-id="a88f2-108">获取此对象的大小（以字节为单位） `ICorDebugValue3` 。</span><span class="sxs-lookup"><span data-stu-id="a88f2-108">Gets the size, in bytes, of this `ICorDebugValue3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a88f2-109">注解</span><span class="sxs-lookup"><span data-stu-id="a88f2-109">Remarks</span></span>  

 <span data-ttu-id="a88f2-110">[ICorDebugValue：： GetSize](icordebugvalue3-getsize64-method.md)方法返回的对象大小范围为0到2147483647字节。</span><span class="sxs-lookup"><span data-stu-id="a88f2-110">The [ICorDebugValue::GetSize](icordebugvalue3-getsize64-method.md) method returns an object size that ranges from 0 to 2,147,483,647 bytes.</span></span> <span data-ttu-id="a88f2-111">在 .NET Framework 4.5 中，数组的大小可超过 2 GB。</span><span class="sxs-lookup"><span data-stu-id="a88f2-111">In the .NET Framework 4.5, the size of arrays can exceed 2 GB.</span></span> <span data-ttu-id="a88f2-112">`ICorDebugValue3`接口使您能够确定这些数组的大小。</span><span class="sxs-lookup"><span data-stu-id="a88f2-112">The `ICorDebugValue3` interface enables you to determine the size of these arrays.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a88f2-113">要求</span><span class="sxs-lookup"><span data-stu-id="a88f2-113">Requirements</span></span>  

 <span data-ttu-id="a88f2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a88f2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a88f2-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a88f2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a88f2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a88f2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a88f2-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a88f2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a88f2-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a88f2-118">See also</span></span>

- [<span data-ttu-id="a88f2-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="a88f2-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="a88f2-120">调试</span><span class="sxs-lookup"><span data-stu-id="a88f2-120">Debugging</span></span>](index.md)
