---
title: ICLRTaskManager 接口
ms.date: 03/30/2017
api_name:
- ICLRTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager
helpviewer_keywords:
- ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 2bd55e0c-001b-41fd-b29d-f01670fe8216
topic_type:
- apiref
ms.openlocfilehash: 1170b29c01275b108a6ccdf6e324c96d97c10c82
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732445"
---
# <a name="iclrtaskmanager-interface"></a><span data-ttu-id="74c91-102">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="74c91-102">ICLRTaskManager Interface</span></span>

<span data-ttu-id="74c91-103">提供一些方法，这些方法允许主机显式请求公共语言运行时 (CLR) 创建新任务、获取当前正在执行的任务，并设置任务的地理语言和区域性。</span><span class="sxs-lookup"><span data-stu-id="74c91-103">Provides methods that allow the host to request explicitly that the common language runtime (CLR) create a new task, get the currently executing task, and set the geographic language and culture for the task.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="74c91-104">方法</span><span class="sxs-lookup"><span data-stu-id="74c91-104">Methods</span></span>  
  
|<span data-ttu-id="74c91-105">方法</span><span class="sxs-lookup"><span data-stu-id="74c91-105">Method</span></span>|<span data-ttu-id="74c91-106">说明</span><span class="sxs-lookup"><span data-stu-id="74c91-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="74c91-107">CreateTask 方法</span><span class="sxs-lookup"><span data-stu-id="74c91-107">CreateTask Method</span></span>](iclrtaskmanager-createtask-method.md)|<span data-ttu-id="74c91-108">显式请求 CLR 创建新的 [ICLRTask](iclrtask-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="74c91-108">Requests explicitly that the CLR create a new [ICLRTask](iclrtask-interface.md) instance.</span></span>|  
|[<span data-ttu-id="74c91-109">GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="74c91-109">GetCurrentTask Method</span></span>](iclrtaskmanager-getcurrenttask-method.md)|<span data-ttu-id="74c91-110">获取 `ICLRTask` 表示当前正在执行的任务的实例。</span><span class="sxs-lookup"><span data-stu-id="74c91-110">Gets the `ICLRTask` instance that represents the task that is currently executing.</span></span>|  
|[<span data-ttu-id="74c91-111">GetCurrentTaskType 方法</span><span class="sxs-lookup"><span data-stu-id="74c91-111">GetCurrentTaskType Method</span></span>](iclrtaskmanager-getcurrenttasktype-method.md)|<span data-ttu-id="74c91-112">获取当前正在执行的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="74c91-112">Gets the type of the task that is currently executing.</span></span>|  
|[<span data-ttu-id="74c91-113">SetLocale 方法</span><span class="sxs-lookup"><span data-stu-id="74c91-113">SetLocale Method</span></span>](iclrtaskmanager-setlocale-method.md)|<span data-ttu-id="74c91-114">通知 CLR 宿主已经修改了当前正在执行的任务的区域设置标识符。</span><span class="sxs-lookup"><span data-stu-id="74c91-114">Notifies the CLR that the host has modified the locale identifier on the currently executing task.</span></span>|  
|[<span data-ttu-id="74c91-115">SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="74c91-115">SetUILocale Method</span></span>](iclrtaskmanager-setuilocale-method.md)|<span data-ttu-id="74c91-116">通知公共语言运行时宿主已经修改了当前正在执行的任务的用户界面区域设置标识符。</span><span class="sxs-lookup"><span data-stu-id="74c91-116">Notifies the common language runtime that the host has modified the user interface locale identifier on the currently executing task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="74c91-117">注解</span><span class="sxs-lookup"><span data-stu-id="74c91-117">Remarks</span></span>  

 <span data-ttu-id="74c91-118">宿主环境中运行的每个任务都在宿主端 (一个实例，该实例在 [IHostTask](ihosttask-interface.md)) 的实例和 CLR 端 [ () 的](iclrtask-interface.md) 实例上。</span><span class="sxs-lookup"><span data-stu-id="74c91-118">Each task that is running in a hosted environment has representations both on the host side (an instance of [IHostTask](ihosttask-interface.md)) and on the CLR side (an instance of [ICLRTask](iclrtask-interface.md)).</span></span> <span data-ttu-id="74c91-119">宿主或 CLR 可以启动任务创建，但宿主端表示形式必须与相应的 CLR 端表示形式相关联，以确保主机与 CLR 之间的有关任务的通信成功。</span><span class="sxs-lookup"><span data-stu-id="74c91-119">Either the host or the CLR can initiate the creation of a task, but the host-side representation must be associated with a corresponding CLR-side representation to ensure successful communication between the host and the CLR regarding the task.</span></span> <span data-ttu-id="74c91-120">必须先创建并实例化两个对象，然后托管代码才能在操作系统线程上执行。</span><span class="sxs-lookup"><span data-stu-id="74c91-120">The two objects must be created and instantiated before managed code can execute on an operating system thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74c91-121">要求</span><span class="sxs-lookup"><span data-stu-id="74c91-121">Requirements</span></span>  

 <span data-ttu-id="74c91-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="74c91-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74c91-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="74c91-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="74c91-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="74c91-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="74c91-125">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74c91-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74c91-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="74c91-126">See also</span></span>

- [<span data-ttu-id="74c91-127">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="74c91-127">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="74c91-128">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="74c91-128">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="74c91-129">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="74c91-129">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="74c91-130">承载接口</span><span class="sxs-lookup"><span data-stu-id="74c91-130">Hosting Interfaces</span></span>](hosting-interfaces.md)
