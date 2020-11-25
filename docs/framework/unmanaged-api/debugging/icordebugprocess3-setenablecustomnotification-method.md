---
title: ICorDebugProcess3::SetEnableCustomNotification 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3.SetEnableCustomNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3::SetEnableCustomNotification
helpviewer_keywords:
- ICorDebugProcess3::SetEnableCustomNotification method [.NET Framework debugging]
- SetEnableCustomNotification method [.NET Framework debugging]
ms.assetid: afd88ee9-2589-4461-a75a-9b6fe55a2525
topic_type:
- apiref
ms.openlocfilehash: 078e5cb03848564b42e30a079101d5a61e0074bd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95734018"
---
# <a name="icordebugprocess3setenablecustomnotification-method"></a><span data-ttu-id="5c223-102">ICorDebugProcess3::SetEnableCustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="5c223-102">ICorDebugProcess3::SetEnableCustomNotification Method</span></span>

<span data-ttu-id="5c223-103">启用和禁用指定类型的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="5c223-103">Enables and disables custom debugger notifications of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c223-104">语法</span><span class="sxs-lookup"><span data-stu-id="5c223-104">Syntax</span></span>  
  
```cpp  
HRESULT SetEnableCustomNotification(ICorDebugClass * pClass,  
                                    BOOL fEnable);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c223-105">参数</span><span class="sxs-lookup"><span data-stu-id="5c223-105">Parameters</span></span>  

 `pClass`  
 <span data-ttu-id="5c223-106">中指定自定义调试器通知的类型。</span><span class="sxs-lookup"><span data-stu-id="5c223-106">[in] The type that specifies custom debugger notifications.</span></span>  
  
 `fEnable`  
 <span data-ttu-id="5c223-107">[in] `true` 启用自定义调试器通知; `false` 禁用通知。</span><span class="sxs-lookup"><span data-stu-id="5c223-107">[in] `true` to enable custom debugger notifications; `false` to disable notifications.</span></span> <span data-ttu-id="5c223-108">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="5c223-108">The default value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5c223-109">备注</span><span class="sxs-lookup"><span data-stu-id="5c223-109">Remarks</span></span>  

 <span data-ttu-id="5c223-110">当 `fEnable` 设置为时 `true` ，对方法的调用会 <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> 触发 [ICorDebugManagedCallback3：： CustomNotification](icordebugmanagedcallback3-customnotification-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="5c223-110">When `fEnable` is set to `true`, calls to the <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> method trigger an [ICorDebugManagedCallback3::CustomNotification](icordebugmanagedcallback3-customnotification-method.md) callback.</span></span> <span data-ttu-id="5c223-111">默认情况下禁用通知;因此，调试器必须指定它知道的任何通知类型并想要处理。</span><span class="sxs-lookup"><span data-stu-id="5c223-111">Notifications are disabled by default; therefore, the debugger must specify any notification types it knows about and wants to handle.</span></span> <span data-ttu-id="5c223-112">由于 [ICorDebugClass](icordebug-interface.md) 类的作用域是应用程序域，因此，如果要在 `SetEnableCustomNotification` 整个过程中接收通知，则调试器必须为进程中的每个应用程序域调用。</span><span class="sxs-lookup"><span data-stu-id="5c223-112">Because the [ICorDebugClass](icordebug-interface.md) class is scoped by application domain, the debugger must call `SetEnableCustomNotification` for every application domain in the process if it wants to receive the notification across the entire process.</span></span>  
  
 <span data-ttu-id="5c223-113">从 .NET Framework 4 开始，唯一受支持的通知是跨线程依赖项通知。</span><span class="sxs-lookup"><span data-stu-id="5c223-113">Starting with the .NET Framework 4, the only supported notification is a cross-thread dependency notification.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c223-114">要求</span><span class="sxs-lookup"><span data-stu-id="5c223-114">Requirements</span></span>  

 <span data-ttu-id="5c223-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5c223-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5c223-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5c223-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5c223-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5c223-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5c223-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5c223-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c223-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c223-119">See also</span></span>

- [<span data-ttu-id="5c223-120">ICorDebugProcess3 接口</span><span class="sxs-lookup"><span data-stu-id="5c223-120">ICorDebugProcess3 Interface</span></span>](icordebugprocess3-interface.md)
- [<span data-ttu-id="5c223-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="5c223-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="5c223-122">调试</span><span class="sxs-lookup"><span data-stu-id="5c223-122">Debugging</span></span>](index.md)
