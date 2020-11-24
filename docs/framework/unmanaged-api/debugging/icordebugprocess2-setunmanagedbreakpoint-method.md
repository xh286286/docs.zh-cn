---
title: ICorDebugProcess2::SetUnmanagedBreakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.SetUnmanagedBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::SetUnmanagedBreakpoint
helpviewer_keywords:
- ICorDebugProcess2::SetUnmanagedBreakpoint method [.NET Framework debugging]
- SetUnmanagedBreakpoint method [.NET Framework debugging]
ms.assetid: 93829d15-d942-4e2d-b7a4-dfc9d7fb96be
topic_type:
- apiref
ms.openlocfilehash: 1a883878107569145b97d5793f0628efefb13545
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675238"
---
# <a name="icordebugprocess2setunmanagedbreakpoint-method"></a><span data-ttu-id="323ea-102">ICorDebugProcess2::SetUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="323ea-102">ICorDebugProcess2::SetUnmanagedBreakpoint Method</span></span>

<span data-ttu-id="323ea-103">在指定的本机映像偏移量处设置非托管断点。</span><span class="sxs-lookup"><span data-stu-id="323ea-103">Sets an unmanaged breakpoint at the specified native image offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="323ea-104">语法</span><span class="sxs-lookup"><span data-stu-id="323ea-104">Syntax</span></span>  
  
```cpp  
HRESULT SetUnmanagedBreakpoint (  
    [in]  CORDB_ADDRESS    address,  
    [in]  ULONG32          bufsize,  
    [out, size_is(bufsize), length_is(*bufLen)]
        BYTE               buffer[],  
    [out] ULONG32          *bufLen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="323ea-105">参数</span><span class="sxs-lookup"><span data-stu-id="323ea-105">Parameters</span></span>  

 `address`  
 <span data-ttu-id="323ea-106">中一个 `CORDB_ADDRESS` 对象，该对象指定本机映像偏移量。</span><span class="sxs-lookup"><span data-stu-id="323ea-106">[in] A `CORDB_ADDRESS` object that specifies the native image offset.</span></span>  
  
 `bufsize`  
 <span data-ttu-id="323ea-107">中数组的大小（以字节为单位） `buffer` 。</span><span class="sxs-lookup"><span data-stu-id="323ea-107">[in] The size, in bytes, of the `buffer` array.</span></span>  
  
 `buffer`  
 <span data-ttu-id="323ea-108">弄一个数组，其中包含由断点替换的操作码。</span><span class="sxs-lookup"><span data-stu-id="323ea-108">[out] An array that contains the opcode that is replaced by the breakpoint.</span></span>  
  
 `bufLen`  
 <span data-ttu-id="323ea-109">弄指向数组中返回的字节数的指针 `buffer` 。</span><span class="sxs-lookup"><span data-stu-id="323ea-109">[out] A pointer to the number of bytes returned in the `buffer` array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="323ea-110">注解</span><span class="sxs-lookup"><span data-stu-id="323ea-110">Remarks</span></span>  

 <span data-ttu-id="323ea-111">如果本机映像偏移量在公共语言运行时 (CLR) 中，则将忽略该断点。</span><span class="sxs-lookup"><span data-stu-id="323ea-111">If the native image offset is within the common language runtime (CLR), the breakpoint will be ignored.</span></span> <span data-ttu-id="323ea-112">当调试器设置断点时，这允许 CLR 避免调度带外断点。</span><span class="sxs-lookup"><span data-stu-id="323ea-112">This allows the CLR to avoid dispatching an out-of-band breakpoint, when the breakpoint is set by the debugger.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="323ea-113">要求</span><span class="sxs-lookup"><span data-stu-id="323ea-113">Requirements</span></span>  

 <span data-ttu-id="323ea-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="323ea-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="323ea-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="323ea-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="323ea-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="323ea-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="323ea-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="323ea-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
