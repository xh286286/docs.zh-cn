---
title: ICorDebugSymbolProvider::GetMergedAssemblyRecords 方法
ms.date: 03/30/2017
ms.assetid: cc4c510d-550d-4941-af34-81987caf3425
ms.openlocfilehash: 10bbcf2e6a536eeb4ab8141c10c177a53faa1c95
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730872"
---
# <a name="icordebugsymbolprovidergetmergedassemblyrecords-method"></a><span data-ttu-id="e0c10-102">ICorDebugSymbolProvider::GetMergedAssemblyRecords 方法</span><span class="sxs-lookup"><span data-stu-id="e0c10-102">ICorDebugSymbolProvider::GetMergedAssemblyRecords Method</span></span>

<span data-ttu-id="e0c10-103">获取所有合并程序集的符号记录。</span><span class="sxs-lookup"><span data-stu-id="e0c10-103">Gets the symbol records for all the merged assemblies.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0c10-104">语法</span><span class="sxs-lookup"><span data-stu-id="e0c10-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMergedAssemblyRecords(  
   [in] ULONG32 cRequestedRecords,  
   [out] ULONG32 *pcFetchedRecords,  
   [out, size_is(cRequestedRecords), length_is(*pcFetchedRecords)] ICorDebugMergedAssemblyRecord *pRecords[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e0c10-105">参数</span><span class="sxs-lookup"><span data-stu-id="e0c10-105">Parameters</span></span>  

 `cRequestedRecords`  
 <span data-ttu-id="e0c10-106">[in] 请求的符号记录数。</span><span class="sxs-lookup"><span data-stu-id="e0c10-106">[in] The number of symbol records requested.</span></span>  
  
 `pcFetchedRecords`  
 <span data-ttu-id="e0c10-107">[out] 指向由方法检索的符号记录数的指针。</span><span class="sxs-lookup"><span data-stu-id="e0c10-107">[out] A pointer to the number of symbol records retrieved by the method.</span></span>  
  
 `pRecords`  
 <span data-ttu-id="e0c10-108">指向 [ICorDebugMergedAssemblyRecord](icordebugmergedassemblyrecord-interface.md) 对象数组的指针。</span><span class="sxs-lookup"><span data-stu-id="e0c10-108">A pointer to an array of [ICorDebugMergedAssemblyRecord](icordebugmergedassemblyrecord-interface.md) objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e0c10-109">注解</span><span class="sxs-lookup"><span data-stu-id="e0c10-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e0c10-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="e0c10-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0c10-111">要求</span><span class="sxs-lookup"><span data-stu-id="e0c10-111">Requirements</span></span>  

 <span data-ttu-id="e0c10-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e0c10-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0c10-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e0c10-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e0c10-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e0c10-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e0c10-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0c10-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0c10-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0c10-116">See also</span></span>

- [<span data-ttu-id="e0c10-117">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="e0c10-117">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="e0c10-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="e0c10-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
