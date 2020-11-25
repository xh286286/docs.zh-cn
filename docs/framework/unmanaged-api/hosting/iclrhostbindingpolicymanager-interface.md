---
title: ICLRHostBindingPolicyManager 接口
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager
helpviewer_keywords:
- ICLRHostBindingPolicyManager interface [.NET Framework hosting]
ms.assetid: f9da168b-366b-4b2b-bdb9-330b6bad5a6b
topic_type:
- apiref
ms.openlocfilehash: 49d1ee4dd0965d4ae5b54b53208809cfbdf7e718
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725620"
---
# <a name="iclrhostbindingpolicymanager-interface"></a><span data-ttu-id="5b09b-102">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="5b09b-102">ICLRHostBindingPolicyManager Interface</span></span>

<span data-ttu-id="5b09b-103">为宿主提供方法，用于评估当前的绑定策略并传达指定程序集的策略更改。</span><span class="sxs-lookup"><span data-stu-id="5b09b-103">Provides methods for the host to evaluate current binding policy and communicate policy changes for a specified assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5b09b-104">方法</span><span class="sxs-lookup"><span data-stu-id="5b09b-104">Methods</span></span>  
  
|<span data-ttu-id="5b09b-105">方法</span><span class="sxs-lookup"><span data-stu-id="5b09b-105">Method</span></span>|<span data-ttu-id="5b09b-106">说明</span><span class="sxs-lookup"><span data-stu-id="5b09b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5b09b-107">EvaluatePolicy 方法</span><span class="sxs-lookup"><span data-stu-id="5b09b-107">EvaluatePolicy Method</span></span>](iclrhostbindingpolicymanager-evaluatepolicy-method.md)|<span data-ttu-id="5b09b-108">代表主机计算绑定策略。</span><span class="sxs-lookup"><span data-stu-id="5b09b-108">Evaluates binding policy on behalf of the host.</span></span>|  
|[<span data-ttu-id="5b09b-109">ModifyApplicationPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="5b09b-109">ModifyApplicationPolicy Method</span></span>](iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)|<span data-ttu-id="5b09b-110">修改指定程序集的绑定策略，并创建该策略的新版本。</span><span class="sxs-lookup"><span data-stu-id="5b09b-110">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5b09b-111">要求</span><span class="sxs-lookup"><span data-stu-id="5b09b-111">Requirements</span></span>  

 <span data-ttu-id="5b09b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b09b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b09b-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5b09b-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5b09b-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5b09b-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5b09b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b09b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b09b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b09b-116">See also</span></span>

- [<span data-ttu-id="5b09b-117">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="5b09b-117">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="5b09b-118">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="5b09b-118">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
- [<span data-ttu-id="5b09b-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="5b09b-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
