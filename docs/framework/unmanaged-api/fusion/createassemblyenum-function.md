---
title: CreateAssemblyEnum 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyEnum
helpviewer_keywords:
- CreateAssemblyEnum function [.NET Framework fusion]
ms.assetid: 3506df38-6cea-42f6-946e-4287863bcfb3
topic_type:
- apiref
ms.openlocfilehash: b7e3696121475885f5061bd96eb6905d7ccae734
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683168"
---
# <a name="createassemblyenum-function"></a><span data-ttu-id="4103c-102">CreateAssemblyEnum 函数</span><span class="sxs-lookup"><span data-stu-id="4103c-102">CreateAssemblyEnum Function</span></span>

<span data-ttu-id="4103c-103">获取一个指针，该指针指向可使用指定的[IAssemblyName](iassemblyname-interface.md)枚举程序集中的对象的[IAssemblyEnum](iassemblyenum-interface.md)实例。</span><span class="sxs-lookup"><span data-stu-id="4103c-103">Gets a pointer to an [IAssemblyEnum](iassemblyenum-interface.md) instance that can enumerate the objects in the assembly with the specified [IAssemblyName](iassemblyname-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4103c-104">语法</span><span class="sxs-lookup"><span data-stu-id="4103c-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateAssemblyEnum (  
    [out] IAssemblyEnum  **pEnum,  
    [in]  IUnknown       *pUnkReserved,  
    [in]  IAssemblyName  *pName,  
    [in]  DWORD          dwFlags,  
    [in]  LPVOID         pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="4103c-105">参数</span><span class="sxs-lookup"><span data-stu-id="4103c-105">Parameters</span></span>  

 `pEnum`  
 <span data-ttu-id="4103c-106">弄指向包含所请求指针的内存位置的指针 `IAssemblyEnum` 。</span><span class="sxs-lookup"><span data-stu-id="4103c-106">[out] Pointer to a memory location that contains the requested `IAssemblyEnum` pointer.</span></span>  
  
 `pUnkReserved`  
 <span data-ttu-id="4103c-107">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="4103c-107">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="4103c-108">`pUnkReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="4103c-108">`pUnkReserved` must be a null reference.</span></span>  
  
 `pName`  
 <span data-ttu-id="4103c-109">中 `IAssemblyName` 请求的程序集的。</span><span class="sxs-lookup"><span data-stu-id="4103c-109">[in] The `IAssemblyName` of the requested assembly.</span></span> <span data-ttu-id="4103c-110">此名称用于筛选枚举。</span><span class="sxs-lookup"><span data-stu-id="4103c-110">This name is used to filter the enumeration.</span></span> <span data-ttu-id="4103c-111">它可以为 null，以枚举全局程序集缓存中的所有程序集。</span><span class="sxs-lookup"><span data-stu-id="4103c-111">It can be null to enumerate all assemblies in the global assembly cache.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="4103c-112">中用于修改枚举器的行为的标志。</span><span class="sxs-lookup"><span data-stu-id="4103c-112">[in] Flags for modifying the enumerator's behavior.</span></span> <span data-ttu-id="4103c-113">此参数仅包含 [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) 枚举中的一个位。</span><span class="sxs-lookup"><span data-stu-id="4103c-113">This parameter contains exactly one bit from the [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) enumeration.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="4103c-114">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="4103c-114">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="4103c-115">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="4103c-115">`pvReserved` must be a null reference.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4103c-116">注解</span><span class="sxs-lookup"><span data-stu-id="4103c-116">Remarks</span></span>  

 <span data-ttu-id="4103c-117">`dwFlags`参数只包含枚举中的一个位 `ASM_CACHE_FLAGS` 。</span><span class="sxs-lookup"><span data-stu-id="4103c-117">The `dwFlags` parameter contains exactly one bit from the `ASM_CACHE_FLAGS` enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4103c-118">要求</span><span class="sxs-lookup"><span data-stu-id="4103c-118">Requirements</span></span>  

 <span data-ttu-id="4103c-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4103c-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4103c-120">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="4103c-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="4103c-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4103c-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4103c-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4103c-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4103c-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4103c-123">See also</span></span>

- [<span data-ttu-id="4103c-124">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="4103c-124">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
- [<span data-ttu-id="4103c-125">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="4103c-125">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="4103c-126">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="4103c-126">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
