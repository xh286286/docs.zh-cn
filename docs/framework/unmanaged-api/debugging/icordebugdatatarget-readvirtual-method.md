---
title: ICorDebugDataTarget::ReadVirtual 方法
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.ReadVirtual Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::ReadVirtual
helpviewer_keywords:
- ICorDebugDataTarget::ReadVirtual method [.NET Framework debugging]
- ReadVirtual method, ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: 55e57640-b3d2-413d-b4f4-fbc27fb8e37c
topic_type:
- apiref
ms.openlocfilehash: 8fb0cfc72867653eaff65f3183dacf9191604290
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679723"
---
# <a name="icordebugdatatargetreadvirtual-method"></a><span data-ttu-id="e54a1-102">ICorDebugDataTarget::ReadVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="e54a1-102">ICorDebugDataTarget::ReadVirtual Method</span></span>

<span data-ttu-id="e54a1-103">获取从指定地址开始的连续内存块，并将其返回到提供的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="e54a1-103">Gets a block of contiguous memory starting at the specified address, and returns it in the supplied buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e54a1-104">语法</span><span class="sxs-lookup"><span data-stu-id="e54a1-104">Syntax</span></span>  
  
```cpp  
HRESULT ReadVirtual(  
    [in] CORDB_ADDRESS   address,  
    [out, size_is(bytesRequested), length_is(*pBytesRead)]  
          BYTE *     pBuffer,  
    [in]  ULONG32    bytesRequested,  
    [out] ULONG32 *  pBytesRead);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e54a1-105">参数</span><span class="sxs-lookup"><span data-stu-id="e54a1-105">Parameters</span></span>  

 `address`  
 <span data-ttu-id="e54a1-106">中请求的内存的开始地址。</span><span class="sxs-lookup"><span data-stu-id="e54a1-106">[in] The start address of requested memory.</span></span>  
  
 `pbuffer`  
 <span data-ttu-id="e54a1-107">弄内存将存储到的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e54a1-107">[out] The buffer where the memory will be stored.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="e54a1-108">中要从目标地址获取的字节数。</span><span class="sxs-lookup"><span data-stu-id="e54a1-108">[in] The number of bytes to get from the target address.</span></span>  
  
 `pBytesRead`  
 <span data-ttu-id="e54a1-109">弄实际从目标地址中读取的字节数。</span><span class="sxs-lookup"><span data-stu-id="e54a1-109">[out] The number of bytes actually read from the target address.</span></span> <span data-ttu-id="e54a1-110">该值可以少于 `bytesRequested` 。</span><span class="sxs-lookup"><span data-stu-id="e54a1-110">This can be fewer than `bytesRequested`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e54a1-111">注解</span><span class="sxs-lookup"><span data-stu-id="e54a1-111">Remarks</span></span>  

 <span data-ttu-id="e54a1-112">如果可以读取指定开始地址处的第一个字节 () ，则调用应返回成功 (，以支持通过自描述长度有效读取数据结构，如) 以 null 结尾的字符串。</span><span class="sxs-lookup"><span data-stu-id="e54a1-112">If the first byte (at the specified start address) can be read, the call should return success (to support efficient reading of data structures with self-describing length, like null-terminated strings).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e54a1-113">要求</span><span class="sxs-lookup"><span data-stu-id="e54a1-113">Requirements</span></span>  

 <span data-ttu-id="e54a1-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e54a1-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e54a1-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e54a1-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e54a1-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e54a1-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e54a1-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e54a1-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e54a1-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e54a1-118">See also</span></span>

- [<span data-ttu-id="e54a1-119">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="e54a1-119">ICorDebugDataTarget Interface</span></span>](icordebugdatatarget-interface.md)
- [<span data-ttu-id="e54a1-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="e54a1-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e54a1-121">调试</span><span class="sxs-lookup"><span data-stu-id="e54a1-121">Debugging</span></span>](index.md)
