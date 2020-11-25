---
title: ICorDebugMergedAssemblyRecord::GetIndex 方法
ms.date: 03/30/2017
ms.assetid: 98701444-b9bc-4978-9548-89ac3394147d
ms.openlocfilehash: 3056d22f5ddc1b11b79ee072aba68ce3ad40e8da
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710631"
---
# <a name="icordebugmergedassemblyrecordgetindex-method"></a><span data-ttu-id="7d1e9-102">ICorDebugMergedAssemblyRecord::GetIndex 方法</span><span class="sxs-lookup"><span data-stu-id="7d1e9-102">ICorDebugMergedAssemblyRecord::GetIndex Method</span></span>

<span data-ttu-id="7d1e9-103">获取程序集的前缀索引。</span><span class="sxs-lookup"><span data-stu-id="7d1e9-103">Gets the assembly's prefix index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d1e9-104">语法</span><span class="sxs-lookup"><span data-stu-id="7d1e9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetIndex(  
   [out] ULONG32 *pIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d1e9-105">参数</span><span class="sxs-lookup"><span data-stu-id="7d1e9-105">Parameters</span></span>  

 `pIndex`  
 <span data-ttu-id="7d1e9-106">[out] 指向前缀索引的指针。</span><span class="sxs-lookup"><span data-stu-id="7d1e9-106">[out] A pointer to the prefix index.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7d1e9-107">注解</span><span class="sxs-lookup"><span data-stu-id="7d1e9-107">Remarks</span></span>  

 <span data-ttu-id="7d1e9-108">前缀索引用于防止合并的元数据类型名称出现名称冲突。</span><span class="sxs-lookup"><span data-stu-id="7d1e9-108">The prefix index is used to prevent name collisions in the merged metadata type names.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7d1e9-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="7d1e9-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d1e9-110">要求</span><span class="sxs-lookup"><span data-stu-id="7d1e9-110">Requirements</span></span>  

 <span data-ttu-id="7d1e9-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d1e9-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d1e9-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7d1e9-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7d1e9-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7d1e9-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7d1e9-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d1e9-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d1e9-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d1e9-115">See also</span></span>

- [<span data-ttu-id="7d1e9-116">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="7d1e9-116">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="7d1e9-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="7d1e9-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
