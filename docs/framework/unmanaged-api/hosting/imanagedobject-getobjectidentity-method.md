---
title: IManagedObject::GetObjectIdentity 方法
ms.date: 03/30/2017
api_name:
- IManagedObject.GetObjectIdentity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetObjectIdentity
helpviewer_keywords:
- GetObjectIdentity method [.NET Framework hosting]
- IManagedObject::GetObjectIdentity method [.NET Framework hosting]
ms.assetid: b862ff3e-e480-4cdf-84e2-e1013334a467
topic_type:
- apiref
ms.openlocfilehash: fc74b84bccceb1772bf3642e51ec88c562ce5dce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730704"
---
# <a name="imanagedobjectgetobjectidentity-method"></a><span data-ttu-id="b9491-102">IManagedObject::GetObjectIdentity 方法</span><span class="sxs-lookup"><span data-stu-id="b9491-102">IManagedObject::GetObjectIdentity Method</span></span>

<span data-ttu-id="b9491-103">获取此托管对象的标识。</span><span class="sxs-lookup"><span data-stu-id="b9491-103">Gets the identity of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9491-104">语法</span><span class="sxs-lookup"><span data-stu-id="b9491-104">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9491-105">参数</span><span class="sxs-lookup"><span data-stu-id="b9491-105">Parameters</span></span>  

 `pBSTRGUID`  
 <span data-ttu-id="b9491-106">弄指向对象所在的进程的 GUID 的指针。</span><span class="sxs-lookup"><span data-stu-id="b9491-106">[out] A pointer to the GUID of the process in which the object resides.</span></span>  
  
 `AppDomainID`  
 <span data-ttu-id="b9491-107">弄指向对象的应用程序域的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="b9491-107">[out] A pointer to the ID of the object's application domain.</span></span>  
  
 `pCCW`  
 <span data-ttu-id="b9491-108">弄指向 COM 经典 v 表中对象索引的指针。</span><span class="sxs-lookup"><span data-stu-id="b9491-108">[out] A pointer to object's index in the COM classic v-table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9491-109">注解</span><span class="sxs-lookup"><span data-stu-id="b9491-109">Remarks</span></span>  

 <span data-ttu-id="b9491-110">托管对象的标识包括进程 GUID、应用程序域 ID 以及 COM 经典 v 表中对象的索引。</span><span class="sxs-lookup"><span data-stu-id="b9491-110">The identity of a managed object includes process GUID, application domain ID, and the object's index in the COM classic v-table.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9491-111">要求</span><span class="sxs-lookup"><span data-stu-id="b9491-111">Requirements</span></span>  

 <span data-ttu-id="b9491-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b9491-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9491-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b9491-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b9491-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b9491-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b9491-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9491-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9491-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9491-116">See also</span></span>

- [<span data-ttu-id="b9491-117">IManagedObject 接口</span><span class="sxs-lookup"><span data-stu-id="b9491-117">IManagedObject Interface</span></span>](imanagedobject-interface.md)
