---
title: ICorDebugLoadedModule::GetName 方法
ms.date: 03/30/2017
ms.assetid: 88c304d5-edaa-4c0e-a8e1-144e8a76877e
ms.openlocfilehash: c18af45184f5a9485e13b9d4789bff2c570834cc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731847"
---
# <a name="icordebugloadedmodulegetname-method"></a><span data-ttu-id="1038e-102">ICorDebugLoadedModule::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="1038e-102">ICorDebugLoadedModule::GetName Method</span></span>

<span data-ttu-id="1038e-103">获取加载模块的名称。</span><span class="sxs-lookup"><span data-stu-id="1038e-103">Gets the name of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1038e-104">语法</span><span class="sxs-lookup"><span data-stu-id="1038e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
   [in] ULONG32 cchName,  
   [out] ULONG32 *pcchName,  
   [out, size_is(cchName),  
   length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1038e-105">参数</span><span class="sxs-lookup"><span data-stu-id="1038e-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="1038e-106">[in] `szName` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="1038e-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="1038e-107">[out] 指向实际写入 `szName` 缓冲区的字符数。缓冲区的字符数的指针。</span><span class="sxs-lookup"><span data-stu-id="1038e-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="1038e-108">[out] 包含加载模块名称的字符数组。</span><span class="sxs-lookup"><span data-stu-id="1038e-108">[out] An array of characters that contain the name of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1038e-109">注解</span><span class="sxs-lookup"><span data-stu-id="1038e-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1038e-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="1038e-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1038e-111">要求</span><span class="sxs-lookup"><span data-stu-id="1038e-111">Requirements</span></span>  

 <span data-ttu-id="1038e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1038e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1038e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1038e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1038e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1038e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1038e-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1038e-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1038e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1038e-116">See also</span></span>

- [<span data-ttu-id="1038e-117">ICorDebugLoadedModule 接口</span><span class="sxs-lookup"><span data-stu-id="1038e-117">ICorDebugLoadedModule Interface</span></span>](icordebugloadedmodule-interface.md)
- [<span data-ttu-id="1038e-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="1038e-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
