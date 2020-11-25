---
title: ICorDebugMemoryBuffer::GetSize 方法
ms.date: 03/30/2017
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
ms.openlocfilehash: 7f5458dd12ca83c1a5190bbf7fab0f8e5d06a0e1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710745"
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="2dc9e-102">ICorDebugMemoryBuffer::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="2dc9e-102">ICorDebugMemoryBuffer::GetSize Method</span></span>

<span data-ttu-id="2dc9e-103">获取内存缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="2dc9e-103">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dc9e-104">语法</span><span class="sxs-lookup"><span data-stu-id="2dc9e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2dc9e-105">参数</span><span class="sxs-lookup"><span data-stu-id="2dc9e-105">Parameters</span></span>  

 `pcbBufferLength`  
 <span data-ttu-id="2dc9e-106">[out] 指向内存缓冲区大小的指针。</span><span class="sxs-lookup"><span data-stu-id="2dc9e-106">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2dc9e-107">注解</span><span class="sxs-lookup"><span data-stu-id="2dc9e-107">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2dc9e-108">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="2dc9e-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2dc9e-109">要求</span><span class="sxs-lookup"><span data-stu-id="2dc9e-109">Requirements</span></span>  

 <span data-ttu-id="2dc9e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2dc9e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2dc9e-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2dc9e-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2dc9e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2dc9e-113">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2dc9e-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2dc9e-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2dc9e-114">See also</span></span>

- [<span data-ttu-id="2dc9e-115">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="2dc9e-115">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="2dc9e-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="2dc9e-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
