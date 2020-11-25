---
title: INotifySource2::SetNotifyFilter 方法
ms.date: 03/30/2017
api_name:
- INotifySource2.SetNotifyFilter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySource2::SetNotifyFilter
helpviewer_keywords:
- INotifySource2::SetNotifyFilter method [.NET Framework debugging]
- SetNotifyFilter method [.NET Framework debugging]
ms.assetid: 6351fc92-b126-4af6-9bf3-0a8ce92845fc
topic_type:
- apiref
ms.openlocfilehash: 99bce831405d722f1f1ca0ae56e60f95f2d905e8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719926"
---
# <a name="inotifysource2setnotifyfilter-method"></a><span data-ttu-id="8c3d6-102">INotifySource2::SetNotifyFilter 方法</span><span class="sxs-lookup"><span data-stu-id="8c3d6-102">INotifySource2::SetNotifyFilter Method</span></span>

<span data-ttu-id="8c3d6-103">分配用于此源的通知筛选器。</span><span class="sxs-lookup"><span data-stu-id="8c3d6-103">Assigns a notification filter for use with this source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c3d6-104">语法</span><span class="sxs-lookup"><span data-stu-id="8c3d6-104">Syntax</span></span>  
  
```cpp  
HRESULT SetNotifyFilter  
(  
    [in]  NOTIFY_FILTER   in_NotifyFilter,  
    [in]  USER_THREAD*    in_pUserThreadFilter  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8c3d6-105">参数</span><span class="sxs-lookup"><span data-stu-id="8c3d6-105">Parameters</span></span>  

 `in_NotifyFilter`  
 <span data-ttu-id="8c3d6-106">中 [NOTIFY_FILTER](notify-filter-enumeration.md) 枚举值的按位组合，这些值用于标识调试器 API 的回调。</span><span class="sxs-lookup"><span data-stu-id="8c3d6-106">[in] A bitwise combination of the [NOTIFY_FILTER](notify-filter-enumeration.md) enumeration values that identify callbacks for the debugger API.</span></span>  
  
 `in_pUserThreadFilter`  
 <span data-ttu-id="8c3d6-107">中一个指针，指向用于标识调试器 API 的线程的 [USER_THREAD](user-thread-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="8c3d6-107">[in] A pointer to a [USER_THREAD](user-thread-structure.md) structure that identifies threads for the debugger API.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8c3d6-108">返回值</span><span class="sxs-lookup"><span data-stu-id="8c3d6-108">Return Value</span></span>  

 <span data-ttu-id="8c3d6-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="8c3d6-109">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8c3d6-110">要求</span><span class="sxs-lookup"><span data-stu-id="8c3d6-110">Requirements</span></span>  

 <span data-ttu-id="8c3d6-111">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="8c3d6-111">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c3d6-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c3d6-112">See also</span></span>

- [<span data-ttu-id="8c3d6-113">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="8c3d6-113">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="8c3d6-114">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="8c3d6-114">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
- [<span data-ttu-id="8c3d6-115">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="8c3d6-115">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
