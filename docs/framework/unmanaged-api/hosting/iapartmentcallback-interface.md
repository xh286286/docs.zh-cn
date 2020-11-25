---
title: IApartmentCallback 接口
ms.date: 03/30/2017
api_name:
- IApartmentCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IApartmentCallback
helpviewer_keywords:
- IApartmentCallback interface [.NET Framework hosting]
ms.assetid: 57c33c58-bf0b-4533-b569-e6a682d02cba
topic_type:
- apiref
ms.openlocfilehash: 0f38314df766b74164bf5e98d9b2153d2dddbcc1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721733"
---
# <a name="iapartmentcallback-interface"></a><span data-ttu-id="972dd-102">IApartmentCallback 接口</span><span class="sxs-lookup"><span data-stu-id="972dd-102">IApartmentCallback Interface</span></span>

<span data-ttu-id="972dd-103">提供用于在单元中进行回调的方法。</span><span class="sxs-lookup"><span data-stu-id="972dd-103">Provides methods for making callbacks within an apartment.</span></span> <span data-ttu-id="972dd-104">*单元* 是进程内共享相同线程访问要求的对象的逻辑容器。</span><span class="sxs-lookup"><span data-stu-id="972dd-104">An *apartment* is a logical container within a process for objects that share the same thread access requirements.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="972dd-105">方法</span><span class="sxs-lookup"><span data-stu-id="972dd-105">Methods</span></span>  
  
|<span data-ttu-id="972dd-106">方法</span><span class="sxs-lookup"><span data-stu-id="972dd-106">Method</span></span>|<span data-ttu-id="972dd-107">说明</span><span class="sxs-lookup"><span data-stu-id="972dd-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="972dd-108">DoCallback 方法</span><span class="sxs-lookup"><span data-stu-id="972dd-108">DoCallback Method</span></span>](iapartmentcallback-docallback-method.md)|<span data-ttu-id="972dd-109">在单元内执行指定的函数。</span><span class="sxs-lookup"><span data-stu-id="972dd-109">Executes the specified function within an apartment.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="972dd-110">要求</span><span class="sxs-lookup"><span data-stu-id="972dd-110">Requirements</span></span>  

 <span data-ttu-id="972dd-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="972dd-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="972dd-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="972dd-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="972dd-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="972dd-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="972dd-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="972dd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="972dd-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="972dd-115">See also</span></span>

- [<span data-ttu-id="972dd-116">承载接口</span><span class="sxs-lookup"><span data-stu-id="972dd-116">Hosting Interfaces</span></span>](hosting-interfaces.md)
