---
title: LogSwitchCallReason 枚举
ms.date: 03/30/2017
api_name:
- LogSwitchCallReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- LogSwitchCallReason
helpviewer_keywords:
- LogSwitchCallReason enumeration [.NET Framework debugging]
ms.assetid: 5bbb8d1b-bbc4-47b0-b1b1-2d54cc0be291
topic_type:
- apiref
ms.openlocfilehash: dfb34595530a47b74762610f5824b68ea00a8a69
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671936"
---
# <a name="logswitchcallreason-enumeration"></a><span data-ttu-id="72548-102">LogSwitchCallReason 枚举</span><span class="sxs-lookup"><span data-stu-id="72548-102">LogSwitchCallReason Enumeration</span></span>

<span data-ttu-id="72548-103">指示已对调试/跟踪开关执行的操作。</span><span class="sxs-lookup"><span data-stu-id="72548-103">Indicates the operation that was performed on a debugging/tracing switch.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72548-104">语法</span><span class="sxs-lookup"><span data-stu-id="72548-104">Syntax</span></span>  
  
```cpp  
typedef enum LogSwitchCallReason {  
    SWITCH_CREATE,  
    SWITCH_MODIFY,  
    SWITCH_DELETE  
} LogSwitchCallReason;  
```  
  
## <a name="members"></a><span data-ttu-id="72548-105">成员</span><span class="sxs-lookup"><span data-stu-id="72548-105">Members</span></span>  
  
|<span data-ttu-id="72548-106">成员</span><span class="sxs-lookup"><span data-stu-id="72548-106">Member</span></span>|<span data-ttu-id="72548-107">说明</span><span class="sxs-lookup"><span data-stu-id="72548-107">Description</span></span>|  
|------------|-----------------|  
|`SWITCH_CREATE`|<span data-ttu-id="72548-108">已创建调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="72548-108">A debugging/tracing switch was created.</span></span>|  
|`SWITCH_MODIFY`|<span data-ttu-id="72548-109">已修改调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="72548-109">A debugging/tracing switch was modified.</span></span>|  
|`SWITCH_DELETE`|<span data-ttu-id="72548-110">已删除调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="72548-110">A debugging/tracing switch was deleted.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="72548-111">要求</span><span class="sxs-lookup"><span data-stu-id="72548-111">Requirements</span></span>  

 <span data-ttu-id="72548-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="72548-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72548-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="72548-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="72548-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72548-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72548-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72548-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72548-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="72548-116">See also</span></span>

- [<span data-ttu-id="72548-117">调试枚举</span><span class="sxs-lookup"><span data-stu-id="72548-117">Debugging Enumerations</span></span>](debugging-enumerations.md)
