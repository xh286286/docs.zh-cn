---
title: ICorDebugVariableSymbol::GetSlotIndex 方法
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
ms.openlocfilehash: fc42517cb95dfc14c472b5bb9111ebd70639cee7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725984"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a><span data-ttu-id="34813-102">ICorDebugVariableSymbol::GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="34813-102">ICorDebugVariableSymbol::GetSlotIndex Method</span></span>

<span data-ttu-id="34813-103">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="34813-103">Gets the managed slot index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34813-104">语法</span><span class="sxs-lookup"><span data-stu-id="34813-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="34813-105">参数</span><span class="sxs-lookup"><span data-stu-id="34813-105">Parameters</span></span>  

 `pSlotIndex`  
 <span data-ttu-id="34813-106">[out] 指向本地变量的槽索引的指针。</span><span class="sxs-lookup"><span data-stu-id="34813-106">[out] A pointer to the local variable's slot index.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="34813-107">返回值</span><span class="sxs-lookup"><span data-stu-id="34813-107">Return Value</span></span>  

 <span data-ttu-id="34813-108">`S_OK` 如果成功。</span><span class="sxs-lookup"><span data-stu-id="34813-108">`S_OK` if successful.</span></span> <span data-ttu-id="34813-109">如果变量是一个函数自变量，则为 `E_FAIL`。</span><span class="sxs-lookup"><span data-stu-id="34813-109">`E_FAIL` if the variable is a function argument.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="34813-110">注解</span><span class="sxs-lookup"><span data-stu-id="34813-110">Remarks</span></span>  

 <span data-ttu-id="34813-111">本地变量的托管槽索引可用于检索变量的元数据信息</span><span class="sxs-lookup"><span data-stu-id="34813-111">The managed slot index of a local variable can be used to retrieve the variable's metadata information</span></span>  
  
> [!NOTE]
> <span data-ttu-id="34813-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="34813-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34813-113">要求</span><span class="sxs-lookup"><span data-stu-id="34813-113">Requirements</span></span>  

 <span data-ttu-id="34813-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="34813-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34813-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="34813-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="34813-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="34813-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="34813-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34813-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34813-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34813-118">See also</span></span>

- [<span data-ttu-id="34813-119">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="34813-119">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="34813-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="34813-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
