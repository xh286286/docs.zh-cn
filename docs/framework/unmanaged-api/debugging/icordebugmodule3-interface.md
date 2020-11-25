---
title: ICorDebugModule3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModule3
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3
helpviewer_keywords:
- ICorDebugModule3 interface [.NET Framework debugging]
ms.assetid: 0b69f945-263a-4e11-8512-89d27f6ea296
topic_type:
- apiref
ms.openlocfilehash: 543a1a3c79b6cf3eb799da5844f35286dfa91940
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709552"
---
# <a name="icordebugmodule3-interface"></a><span data-ttu-id="6eb9d-102">ICorDebugModule3 接口</span><span class="sxs-lookup"><span data-stu-id="6eb9d-102">ICorDebugModule3 Interface</span></span>

<span data-ttu-id="6eb9d-103">为动态模块创建符号读取器。</span><span class="sxs-lookup"><span data-stu-id="6eb9d-103">Creates a symbol reader for a dynamic module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6eb9d-104">语法</span><span class="sxs-lookup"><span data-stu-id="6eb9d-104">Syntax</span></span>  
  
```cpp  
interface ICorDebugModule3 : IUnknown  
{  
    HRESULT CreateReaderForInMemorySymbols  
      (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **  ppObj  
      );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6eb9d-105">方法</span><span class="sxs-lookup"><span data-stu-id="6eb9d-105">Methods</span></span>  
  
|<span data-ttu-id="6eb9d-106">方法</span><span class="sxs-lookup"><span data-stu-id="6eb9d-106">Method</span></span>|<span data-ttu-id="6eb9d-107">说明</span><span class="sxs-lookup"><span data-stu-id="6eb9d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6eb9d-108">ICorDebugModule3::CreateReaderForInMemorySymbols 方法</span><span class="sxs-lookup"><span data-stu-id="6eb9d-108">ICorDebugModule3::CreateReaderForInMemorySymbols Method</span></span>](icordebugmodule3-createreaderforinmemorysymbols-method.md)|<span data-ttu-id="6eb9d-109"> (通常为动态模块的 [ISymUnmanagedReader 接口](../diagnostics/isymunmanagedreader-interface.md)) 创建符号读取器。</span><span class="sxs-lookup"><span data-stu-id="6eb9d-109">Creates a symbol reader (typically [ISymUnmanagedReader Interface](../diagnostics/isymunmanagedreader-interface.md)) for a dynamic module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6eb9d-110">注解</span><span class="sxs-lookup"><span data-stu-id="6eb9d-110">Remarks</span></span>  

 <span data-ttu-id="6eb9d-111">此接口以逻辑方式扩展了 "ICorDebugModule" 和 "ICorDebugModule2" 接口。</span><span class="sxs-lookup"><span data-stu-id="6eb9d-111">This interface logically extends the "ICorDebugModule" and "ICorDebugModule2" interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6eb9d-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="6eb9d-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6eb9d-113">要求</span><span class="sxs-lookup"><span data-stu-id="6eb9d-113">Requirements</span></span>  

 <span data-ttu-id="6eb9d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6eb9d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6eb9d-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6eb9d-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6eb9d-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6eb9d-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6eb9d-117">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="6eb9d-117">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6eb9d-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6eb9d-118">See also</span></span>

- [<span data-ttu-id="6eb9d-119">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="6eb9d-119">ICorDebugRemoteTarget Interface</span></span>](icordebugremotetarget-interface.md)
- [<span data-ttu-id="6eb9d-120">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="6eb9d-120">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="6eb9d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="6eb9d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
