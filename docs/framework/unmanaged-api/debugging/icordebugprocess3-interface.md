---
title: ICorDebugProcess3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3
helpviewer_keywords:
- ICorDebugProcess3 interface [.NET Framework debugging]
ms.assetid: ced9c82e-d7b0-4806-a151-98b6611d3097
topic_type:
- apiref
ms.openlocfilehash: ef8dbd5253c02355f85fba626fa7e68ed62df4bd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95686438"
---
# <a name="icordebugprocess3-interface"></a><span data-ttu-id="05ebd-102">ICorDebugProcess3 接口</span><span class="sxs-lookup"><span data-stu-id="05ebd-102">ICorDebugProcess3 Interface</span></span>

<span data-ttu-id="05ebd-103">控制自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="05ebd-103">Controls custom debugger notifications.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="05ebd-104">方法</span><span class="sxs-lookup"><span data-stu-id="05ebd-104">Methods</span></span>  
  
|<span data-ttu-id="05ebd-105">方法</span><span class="sxs-lookup"><span data-stu-id="05ebd-105">Method</span></span>|<span data-ttu-id="05ebd-106">说明</span><span class="sxs-lookup"><span data-stu-id="05ebd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="05ebd-107">SetEnableCustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="05ebd-107">SetEnableCustomNotification Method</span></span>](icordebugprocess3-setenablecustomnotification-method.md)|<span data-ttu-id="05ebd-108">启用和禁用指定类型的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="05ebd-108">Enables and disables custom debugger notifications of the specified type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="05ebd-109">注解</span><span class="sxs-lookup"><span data-stu-id="05ebd-109">Remarks</span></span>  

 <span data-ttu-id="05ebd-110">此接口以逻辑方式扩展 ICorDebugProcess 和 ICorDebugProcess2 接口。</span><span class="sxs-lookup"><span data-stu-id="05ebd-110">This interface logically extends the ICorDebugProcess and ICorDebugProcess2 interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="05ebd-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="05ebd-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05ebd-112">要求</span><span class="sxs-lookup"><span data-stu-id="05ebd-112">Requirements</span></span>  

 <span data-ttu-id="05ebd-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05ebd-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05ebd-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="05ebd-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="05ebd-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05ebd-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05ebd-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05ebd-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05ebd-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05ebd-117">See also</span></span>

- [<span data-ttu-id="05ebd-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="05ebd-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="05ebd-119">调试</span><span class="sxs-lookup"><span data-stu-id="05ebd-119">Debugging</span></span>](index.md)
