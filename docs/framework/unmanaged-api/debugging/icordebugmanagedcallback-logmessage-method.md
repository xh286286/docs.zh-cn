---
title: ICorDebugManagedCallback::LogMessage 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LogMessage
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LogMessage
helpviewer_keywords:
- ICorDebugManagedCallback::LogMessage method [.NET Framework debugging]
- LogMessage method [.NET Framework debugging]
ms.assetid: d218554a-bf42-4d88-833d-ede30de67a53
topic_type:
- apiref
ms.openlocfilehash: 92b2a7f7f1dd98f0d847119a6431e3816c16d5da
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679567"
---
# <a name="icordebugmanagedcallbacklogmessage-method"></a><span data-ttu-id="91c33-102">ICorDebugManagedCallback::LogMessage 方法</span><span class="sxs-lookup"><span data-stu-id="91c33-102">ICorDebugManagedCallback::LogMessage Method</span></span>

<span data-ttu-id="91c33-103">通知调试器公共语言运行时 (CLR) 托管线程在类中调用了方法 <xref:System.Diagnostics.EventLog> 来记录事件。</span><span class="sxs-lookup"><span data-stu-id="91c33-103">Notifies the debugger that a common language runtime (CLR) managed thread has called a method in the <xref:System.Diagnostics.EventLog> class to log an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91c33-104">语法</span><span class="sxs-lookup"><span data-stu-id="91c33-104">Syntax</span></span>  
  
```cpp  
HRESULT LogMessage (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] LONG                 lLevel,  
    [in] WCHAR               *pLogSwitchName,  
    [in] WCHAR               *pMessage  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="91c33-105">参数</span><span class="sxs-lookup"><span data-stu-id="91c33-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="91c33-106">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含记录事件的托管线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="91c33-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the managed thread that logged the event.</span></span>  
  
 `pThread`  
 <span data-ttu-id="91c33-107">中指向 ICorDebugThread 对象的指针，该对象表示托管线程。</span><span class="sxs-lookup"><span data-stu-id="91c33-107">[in] A pointer to an ICorDebugThread object that represents the managed thread.</span></span>  
  
 `lLevel`  
 <span data-ttu-id="91c33-108">中 [LoggingLevelEnum](logginglevelenum-enumeration.md) 枚举的一个值，该值指示写入事件日志的描述性消息的严重性级别。</span><span class="sxs-lookup"><span data-stu-id="91c33-108">[in] A value of the [LoggingLevelEnum](logginglevelenum-enumeration.md) enumeration that indicates the severity level of the descriptive message that was written to the event log.</span></span>  
  
 `pLogSwitchName`  
 <span data-ttu-id="91c33-109">中指向跟踪开关名称的指针。</span><span class="sxs-lookup"><span data-stu-id="91c33-109">[in] A pointer to the name of the tracing switch.</span></span>  
  
 `pMessage`  
 <span data-ttu-id="91c33-110">中指向写入事件日志的消息的指针。</span><span class="sxs-lookup"><span data-stu-id="91c33-110">[in] A pointer to the message that was written to the event log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91c33-111">要求</span><span class="sxs-lookup"><span data-stu-id="91c33-111">Requirements</span></span>  

 <span data-ttu-id="91c33-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91c33-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91c33-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="91c33-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="91c33-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91c33-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91c33-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91c33-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91c33-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91c33-116">See also</span></span>

- [<span data-ttu-id="91c33-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="91c33-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
