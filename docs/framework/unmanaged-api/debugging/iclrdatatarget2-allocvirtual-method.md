---
title: ICLRDataTarget2::AllocVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.AllocVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::AllocVirtual
helpviewer_keywords:
- ICLRDataTarget2::AllocVirtual method [.NET Framework debugging]
- AllocVirtual method [.NET Framework debugging]
ms.assetid: e3226230-964b-47fb-9f53-d6fdbeda1e9e
topic_type:
- apiref
ms.openlocfilehash: 6d3985919ea7e766db7d07e4ed81484851156ca5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723657"
---
# <a name="iclrdatatarget2allocvirtual-method"></a><span data-ttu-id="6604b-102">ICLRDataTarget2::AllocVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="6604b-102">ICLRDataTarget2::AllocVirtual Method</span></span>

<span data-ttu-id="6604b-103">由公共语言运行时 (CLR) 数据访问服务调用以在此目标进程的地址空间中分配内存。</span><span class="sxs-lookup"><span data-stu-id="6604b-103">Called by the common language runtime (CLR) data access services to allocate memory in the address space of this target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6604b-104">语法</span><span class="sxs-lookup"><span data-stu-id="6604b-104">Syntax</span></span>  
  
```cpp  
HRESULT AllocVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags,  
    [in] ULONG32 protectFlags,  
    [out] CLRDATA_ADDRESS* virt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6604b-105">参数</span><span class="sxs-lookup"><span data-stu-id="6604b-105">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="6604b-106">中一个 `CLRDATA_ADDRESS` 值，该值指定要分配的内存的起始地址。</span><span class="sxs-lookup"><span data-stu-id="6604b-106">[in] A `CLRDATA_ADDRESS` value that specifies the requested starting address of the memory to be allocated.</span></span>  
  
 `size`  
 <span data-ttu-id="6604b-107">中要分配的内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6604b-107">[in] The size, in bytes, of the memory to be allocated.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="6604b-108">中控制内存分配的标志。</span><span class="sxs-lookup"><span data-stu-id="6604b-108">[in] Flags that control the allocation of memory.</span></span> <span data-ttu-id="6604b-109">请参阅 Win32 `VirtualAlloc` 函数。</span><span class="sxs-lookup"><span data-stu-id="6604b-109">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `protectFlags`  
 <span data-ttu-id="6604b-110">中已分配内存的保护特性。</span><span class="sxs-lookup"><span data-stu-id="6604b-110">[in] The protection attributes for the allocated memory.</span></span> <span data-ttu-id="6604b-111">请参阅 Win32 `VirtualAlloc` 函数。</span><span class="sxs-lookup"><span data-stu-id="6604b-111">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `virt`  
 <span data-ttu-id="6604b-112">弄一个指向值的指针，该 `CLRDATA_ADDRESS` 值指定分配的内存的实际起始地址。</span><span class="sxs-lookup"><span data-stu-id="6604b-112">[out] A pointer to a `CLRDATA_ADDRESS` value that specifies the actual starting address of the allocated memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6604b-113">注解</span><span class="sxs-lookup"><span data-stu-id="6604b-113">Remarks</span></span>  

 <span data-ttu-id="6604b-114">`AllocVirtual`方法用作 Win32 函数的逻辑包装 `VirtualAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="6604b-114">The `AllocVirtual` method serves as a logical wrapper for the Win32 `VirtualAlloc` function.</span></span>  
  
 <span data-ttu-id="6604b-115">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="6604b-115">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6604b-116">要求</span><span class="sxs-lookup"><span data-stu-id="6604b-116">Requirements</span></span>  

 <span data-ttu-id="6604b-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6604b-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6604b-118">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="6604b-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6604b-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6604b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6604b-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6604b-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6604b-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6604b-121">See also</span></span>

- [<span data-ttu-id="6604b-122">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="6604b-122">ICLRDataTarget2 Interface</span></span>](iclrdatatarget2-interface.md)
- [<span data-ttu-id="6604b-123">FreeVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="6604b-123">FreeVirtual Method</span></span>](iclrdatatarget2-freevirtual-method.md)
