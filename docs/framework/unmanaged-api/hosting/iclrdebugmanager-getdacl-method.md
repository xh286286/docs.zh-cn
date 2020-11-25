---
title: ICLRDebugManager::GetDacl 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.GetDacl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::GetDacl
helpviewer_keywords:
- GetDacl method [.NET Framework hosting]
- ICLRDebugManager::GetDacl method [.NET Framework hosting]
ms.assetid: 7115e920-aaff-440a-824e-39497139c6f6
topic_type:
- apiref
ms.openlocfilehash: 8a7de5a900bc1af219924b6a83f83cf7e2ef6150
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726140"
---
# <a name="iclrdebugmanagergetdacl-method"></a><span data-ttu-id="9d747-102">ICLRDebugManager::GetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="9d747-102">ICLRDebugManager::GetDacl Method</span></span>

<span data-ttu-id="9d747-103">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="9d747-103">This method is not implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d747-104">语法</span><span class="sxs-lookup"><span data-stu-id="9d747-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDacl (  
    [out] PACL* ppacl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9d747-105">参数</span><span class="sxs-lookup"><span data-stu-id="9d747-105">Parameters</span></span>  

 `ppacl`  
 <span data-ttu-id="9d747-106">弄指向访问控制列表 (ACL) 的接口指针。</span><span class="sxs-lookup"><span data-stu-id="9d747-106">[out] An interface pointer to the Access Control List (ACL).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9d747-107">返回值</span><span class="sxs-lookup"><span data-stu-id="9d747-107">Return Value</span></span>  
  
|<span data-ttu-id="9d747-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d747-108">HRESULT</span></span>|<span data-ttu-id="9d747-109">说明</span><span class="sxs-lookup"><span data-stu-id="9d747-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9d747-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9d747-110">E_NOTIMPL</span></span>|<span data-ttu-id="9d747-111">该方法未实现。</span><span class="sxs-lookup"><span data-stu-id="9d747-111">The method is not implemented.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9d747-112">要求</span><span class="sxs-lookup"><span data-stu-id="9d747-112">Requirements</span></span>  

 <span data-ttu-id="9d747-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9d747-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d747-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9d747-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9d747-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d747-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9d747-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d747-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d747-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9d747-117">See also</span></span>

- [<span data-ttu-id="9d747-118">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="9d747-118">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="9d747-119">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="9d747-119">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="9d747-120">SetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="9d747-120">SetDacl Method</span></span>](iclrdebugmanager-setdacl-method.md)
- [<span data-ttu-id="9d747-121">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="9d747-121">IHostControl Interface</span></span>](ihostcontrol-interface.md)
