---
title: HOST_TYPE 枚举
ms.date: 03/30/2017
api_name:
- HOST_TYPE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- HOST_TYPE
helpviewer_keywords:
- HOST_TYPE enumeration [.NET Framework hosting]
ms.assetid: 51f848be-84c5-4036-9839-c762c576bbf5
topic_type:
- apiref
ms.openlocfilehash: 31640ada28af8e35554b91d5931d427fbaa8dcbe
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721850"
---
# <a name="host_type-enumeration"></a><span data-ttu-id="f66dd-102">HOST_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="f66dd-102">HOST_TYPE Enumeration</span></span>

<span data-ttu-id="f66dd-103">包含的值用于指定启动应用程序的主机的类型。</span><span class="sxs-lookup"><span data-stu-id="f66dd-103">Contains values that specify the type of host that is launching an application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f66dd-104">语法</span><span class="sxs-lookup"><span data-stu-id="f66dd-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    HOST_TYPE_DEFAULT     = 0x0,  
    HOST_TYPE_APPLAUNCH   = 0x1,  
    HOST_TYPE_CORFLAG     = 0x2  
} HOST_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="f66dd-105">成员</span><span class="sxs-lookup"><span data-stu-id="f66dd-105">Members</span></span>  
  
|<span data-ttu-id="f66dd-106">成员</span><span class="sxs-lookup"><span data-stu-id="f66dd-106">Member</span></span>|<span data-ttu-id="f66dd-107">说明</span><span class="sxs-lookup"><span data-stu-id="f66dd-107">Description</span></span>|  
|------------|-----------------|  
|`HOST_TYPE_APPLAUNCH`|<span data-ttu-id="f66dd-108">启动 AppLaunch.exe 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f66dd-108">Launch the application from AppLaunch.exe.</span></span><br /><br /> <span data-ttu-id="f66dd-109">将此值用于部分受信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f66dd-109">Use this value for partially-trusted applications.</span></span>|  
|`HOST_TYPE_CORFLAG`|<span data-ttu-id="f66dd-110">直接启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="f66dd-110">Launch the application directly.</span></span> <span data-ttu-id="f66dd-111">也就是说，从它自己的 .exe 文件启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="f66dd-111">That is, launch the application from its own .exe file.</span></span><br /><br /> <span data-ttu-id="f66dd-112">将此值用于完全受信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f66dd-112">Use this value for fully-trusted applications.</span></span>|  
|`HOST_TYPE_DEFAULT`|<span data-ttu-id="f66dd-113">与 HOST_TYPE_APPLAUNCH 相同。</span><span class="sxs-lookup"><span data-stu-id="f66dd-113">Same as HOST_TYPE_APPLAUNCH.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f66dd-114">要求</span><span class="sxs-lookup"><span data-stu-id="f66dd-114">Requirements</span></span>  

 <span data-ttu-id="f66dd-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f66dd-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f66dd-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f66dd-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f66dd-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f66dd-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f66dd-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f66dd-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f66dd-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f66dd-119">See also</span></span>

- [<span data-ttu-id="f66dd-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="f66dd-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
