---
title: EContextType 枚举
ms.date: 03/30/2017
api_name:
- EContextType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EContextType
helpviewer_keywords:
- EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type:
- apiref
ms.openlocfilehash: c6d1ace12bd07fa1f14c8570eca1f950a5c22be9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95686327"
---
# <a name="econtexttype-enumeration"></a><span data-ttu-id="ae773-102">EContextType 枚举</span><span class="sxs-lookup"><span data-stu-id="ae773-102">EContextType Enumeration</span></span>

<span data-ttu-id="ae773-103">描述当前正在执行的线程的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="ae773-103">Describes the security context of the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae773-104">语法</span><span class="sxs-lookup"><span data-stu-id="ae773-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a><span data-ttu-id="ae773-105">成员</span><span class="sxs-lookup"><span data-stu-id="ae773-105">Members</span></span>  
  
|<span data-ttu-id="ae773-106">成员</span><span class="sxs-lookup"><span data-stu-id="ae773-106">Member</span></span>|<span data-ttu-id="ae773-107">说明</span><span class="sxs-lookup"><span data-stu-id="ae773-107">Description</span></span>|  
|------------|-----------------|  
|`eCurrentContext`|<span data-ttu-id="ae773-108">指示当公共语言运行时 (CLR) 在调用[IHostSecurityManager：： SetSecurityContext](ihostsecuritymanager-setsecuritycontext-method.md)方法的调用中调用[IHostSecurityManager：： GETSECURITYCONTEXT](ihostsecuritymanager-getsecuritycontext-method.md)方法或 CLR 请求的上下文时，当前线程上的上下文。</span><span class="sxs-lookup"><span data-stu-id="ae773-108">Indicates the context on the current thread at the time the common language runtime (CLR) calls the [IHostSecurityManager::GetSecurityContext](ihostsecuritymanager-getsecuritycontext-method.md) method, or the context requested by the CLR in a call to the [IHostSecurityManager::SetSecurityContext](ihostsecuritymanager-setsecuritycontext-method.md) method.</span></span>|  
|`eRestrictedContext`|<span data-ttu-id="ae773-109">指示宿主具有更低权限的上下文，如垃圾回收器或类或模块构造函数。</span><span class="sxs-lookup"><span data-stu-id="ae773-109">Indicates a context over which the host has lower privileges, such as the garbage collector, or class or module constructors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae773-110">注解</span><span class="sxs-lookup"><span data-stu-id="ae773-110">Remarks</span></span>  

 <span data-ttu-id="ae773-111">`EContextType`在对和方法的调用中，CLR 将值之一作为参数值 `IHostSecurityManager::GetSecurityContext` 提供 `IHostSecurityManager::SetSecurityContext` 。</span><span class="sxs-lookup"><span data-stu-id="ae773-111">The CLR supplies one of the `EContextType` values as a parameter value in calls to the `IHostSecurityManager::GetSecurityContext` and `IHostSecurityManager::SetSecurityContext` methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae773-112">要求</span><span class="sxs-lookup"><span data-stu-id="ae773-112">Requirements</span></span>  

 <span data-ttu-id="ae773-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae773-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae773-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ae773-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ae773-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae773-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ae773-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae773-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae773-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae773-117">See also</span></span>

- [<span data-ttu-id="ae773-118">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="ae773-118">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="ae773-119">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="ae773-119">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="ae773-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="ae773-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
