---
title: ICorDebugVariableSymbol 接口
ms.date: 03/30/2017
ms.assetid: 0e58b85e-69bd-41ff-bedb-8cdc8be6a7a2
ms.openlocfilehash: 3d808fd49eb7767f1f48ad4e07d8ba7e47c8f34b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679476"
---
# <a name="icordebugvariablesymbol-interface"></a><span data-ttu-id="0071c-102">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="0071c-102">ICorDebugVariableSymbol Interface</span></span>

<span data-ttu-id="0071c-103">检索变量的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="0071c-103">Retrieves the debug symbol information for a variable.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0071c-104">方法</span><span class="sxs-lookup"><span data-stu-id="0071c-104">Methods</span></span>  
  
|<span data-ttu-id="0071c-105">方法</span><span class="sxs-lookup"><span data-stu-id="0071c-105">Method</span></span>|<span data-ttu-id="0071c-106">说明</span><span class="sxs-lookup"><span data-stu-id="0071c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0071c-107">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="0071c-107">GetName Method</span></span>](icordebugvariablesymbol-getname-method.md)|<span data-ttu-id="0071c-108">获取变量名。</span><span class="sxs-lookup"><span data-stu-id="0071c-108">Gets the name of a variable.</span></span>|  
|[<span data-ttu-id="0071c-109">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="0071c-109">GetSize Method</span></span>](icordebugvariablesymbol-getsize-method.md)|<span data-ttu-id="0071c-110">获取变量的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0071c-110">Gets the size of a variable in bytes.</span></span>|  
|[<span data-ttu-id="0071c-111">GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="0071c-111">GetSlotIndex Method</span></span>](icordebugvariablesymbol-getslotindex-method.md)|<span data-ttu-id="0071c-112">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="0071c-112">Gets the managed slot index of a local variable.</span></span>|  
|[<span data-ttu-id="0071c-113">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="0071c-113">GetValue Method</span></span>](icordebugvariablesymbol-getvalue-method.md)|<span data-ttu-id="0071c-114">获取作为字节数组的变量的值。</span><span class="sxs-lookup"><span data-stu-id="0071c-114">Gets the value of a variable as a byte array.</span></span>|  
|[<span data-ttu-id="0071c-115">SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="0071c-115">SetValue Method</span></span>](icordebugvariablesymbol-setvalue-method.md)|<span data-ttu-id="0071c-116">将字节数组的值分配给变量。</span><span class="sxs-lookup"><span data-stu-id="0071c-116">Assigns the value of a byte array to a variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0071c-117">注解</span><span class="sxs-lookup"><span data-stu-id="0071c-117">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0071c-118">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="0071c-118">This interface is available with .NET Native only.</span></span> <span data-ttu-id="0071c-119">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="0071c-119">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0071c-120">要求</span><span class="sxs-lookup"><span data-stu-id="0071c-120">Requirements</span></span>  

 <span data-ttu-id="0071c-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0071c-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0071c-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0071c-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0071c-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0071c-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0071c-124">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0071c-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0071c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0071c-125">See also</span></span>

- [<span data-ttu-id="0071c-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="0071c-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="0071c-127">调试</span><span class="sxs-lookup"><span data-stu-id="0071c-127">Debugging</span></span>](index.md)
