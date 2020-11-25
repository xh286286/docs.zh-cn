---
title: ComCallUnmarshal Coclass
ms.date: 03/30/2017
api_name:
- ComCallUnmarshal Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ComCallUnmarshal
helpviewer_keywords:
- ComCallUnmarshal coclass [.NET Framework hosting]
ms.assetid: 2adb5827-2268-4914-a1c6-f62b61880a45
topic_type:
- apiref
ms.openlocfilehash: 90bcf4f37631e0246e58cc14bfcd331d981e4713
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731717"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="7e1e9-102">ComCallUnmarshal Coclass</span><span class="sxs-lookup"><span data-stu-id="7e1e9-102">ComCallUnmarshal Coclass</span></span>

<span data-ttu-id="7e1e9-103">提供用于管理接口指针的封送处理的接口。</span><span class="sxs-lookup"><span data-stu-id="7e1e9-103">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e1e9-104">语法</span><span class="sxs-lookup"><span data-stu-id="7e1e9-104">Syntax</span></span>  
  
```cpp  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="7e1e9-105">界面</span><span class="sxs-lookup"><span data-stu-id="7e1e9-105">Interfaces</span></span>  
  
|<span data-ttu-id="7e1e9-106">接口</span><span class="sxs-lookup"><span data-stu-id="7e1e9-106">Interface</span></span>|<span data-ttu-id="7e1e9-107">说明</span><span class="sxs-lookup"><span data-stu-id="7e1e9-107">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="7e1e9-108">提供用于在客户端进程中创建、初始化和管理代理的方法。</span><span class="sxs-lookup"><span data-stu-id="7e1e9-108">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7e1e9-109">要求</span><span class="sxs-lookup"><span data-stu-id="7e1e9-109">Requirements</span></span>  

 <span data-ttu-id="7e1e9-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7e1e9-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e1e9-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7e1e9-111">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="7e1e9-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7e1e9-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7e1e9-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e1e9-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e1e9-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e1e9-114">See also</span></span>

- [<span data-ttu-id="7e1e9-115">承载组件类</span><span class="sxs-lookup"><span data-stu-id="7e1e9-115">Hosting Coclasses</span></span>](hosting-coclasses.md)
