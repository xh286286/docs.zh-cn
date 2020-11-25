---
title: ICLRTaskManager::GetCurrentTaskType 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTaskType
helpviewer_keywords:
- GetCurrentTaskType method [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTaskType method [.NET Framework hosting]
ms.assetid: 6b0d9259-dbe2-45bb-b34d-990f60c73424
topic_type:
- apiref
ms.openlocfilehash: 684b94471c53701c5ebe1dc7e7593eae16ad50fd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728779"
---
# <a name="iclrtaskmanagergetcurrenttasktype-method"></a><span data-ttu-id="b8b0e-102">ICLRTaskManager::GetCurrentTaskType 方法</span><span class="sxs-lookup"><span data-stu-id="b8b0e-102">ICLRTaskManager::GetCurrentTaskType Method</span></span>

<span data-ttu-id="b8b0e-103">获取当前正在执行的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="b8b0e-103">Gets the type of the task that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8b0e-104">语法</span><span class="sxs-lookup"><span data-stu-id="b8b0e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentTaskType(  
    [out] ETaskType *pTaskType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8b0e-105">参数</span><span class="sxs-lookup"><span data-stu-id="b8b0e-105">Parameters</span></span>  

 `pTaskType`  
 <span data-ttu-id="b8b0e-106">弄一个指针，指向 [ETaskType](etasktype-enumeration.md) 枚举的值，该值指示当前正在执行的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="b8b0e-106">[out] A pointer to a value of the [ETaskType](etasktype-enumeration.md) enumeration that indicates the type of task that is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8b0e-107">要求</span><span class="sxs-lookup"><span data-stu-id="b8b0e-107">Requirements</span></span>  

 <span data-ttu-id="b8b0e-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b0e-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8b0e-109">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b8b0e-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b8b0e-110">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b8b0e-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b8b0e-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8b0e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8b0e-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8b0e-112">See also</span></span>

- [<span data-ttu-id="b8b0e-113">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="b8b0e-113">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
