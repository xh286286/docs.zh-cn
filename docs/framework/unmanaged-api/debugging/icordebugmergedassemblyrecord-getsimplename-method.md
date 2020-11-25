---
title: ICorDebugMergedAssemblyRecord::GetSimpleName 方法
ms.date: 03/30/2017
ms.assetid: bc3410f6-ebca-4bca-9b45-fc38c74fa9cb
ms.openlocfilehash: 11e43846f7b119933fb53bdf21423e28bbb792ac
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710540"
---
# <a name="icordebugmergedassemblyrecordgetsimplename-method"></a><span data-ttu-id="70764-102">ICorDebugMergedAssemblyRecord::GetSimpleName 方法</span><span class="sxs-lookup"><span data-stu-id="70764-102">ICorDebugMergedAssemblyRecord::GetSimpleName Method</span></span>

<span data-ttu-id="70764-103">获取程序集的简单名。</span><span class="sxs-lookup"><span data-stu-id="70764-103">Gets the simple name of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70764-104">语法</span><span class="sxs-lookup"><span data-stu-id="70764-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSimpleName(  
   [in] ULONG32 cchName,
   [out] ULONG32 *pcchName,
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="70764-105">参数</span><span class="sxs-lookup"><span data-stu-id="70764-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="70764-106">[in] `szName` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="70764-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="70764-107">[out] 指向实际写入 `szName` 缓冲区的字符数。缓冲区的字符数的指针。</span><span class="sxs-lookup"><span data-stu-id="70764-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="70764-108">指向字符数组的指针。</span><span class="sxs-lookup"><span data-stu-id="70764-108">A pointer to a character array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="70764-109">注解</span><span class="sxs-lookup"><span data-stu-id="70764-109">Remarks</span></span>  

 <span data-ttu-id="70764-110">此方法检索程序集的简单名（例如“System.Collections”），该名称不带文件扩展名、版本、区域性或公钥标记。</span><span class="sxs-lookup"><span data-stu-id="70764-110">This method retrieves the simple name of an assembly (such as "System.Collections"), without a file extension, version, culture, or public key token.</span></span> <span data-ttu-id="70764-111">它对应托管代码中的 <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="70764-111">It corresponds to the <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> property in managed code.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="70764-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="70764-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70764-113">要求</span><span class="sxs-lookup"><span data-stu-id="70764-113">Requirements</span></span>  

 <span data-ttu-id="70764-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="70764-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70764-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="70764-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="70764-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="70764-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="70764-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70764-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70764-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70764-118">See also</span></span>

- [<span data-ttu-id="70764-119">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="70764-119">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="70764-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="70764-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
