---
title: CLRRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CLRRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLRRuntimeHost
helpviewer_keywords:
- CLRRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 2ac9cbf5-8a2d-4e4f-8831-0dad8ef0a897
topic_type:
- apiref
ms.openlocfilehash: 7c77cb2e89cb8fd87bf219780b9460649de19c9d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731749"
---
# <a name="clrruntimehost-coclass"></a><span data-ttu-id="a8703-102">CLRRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="a8703-102">CLRRuntimeHost Coclass</span></span>

<span data-ttu-id="a8703-103">提供用于管理运行时执行的代码的接口。</span><span class="sxs-lookup"><span data-stu-id="a8703-103">Provides interfaces for managing code execution by the runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8703-104">语法</span><span class="sxs-lookup"><span data-stu-id="a8703-104">Syntax</span></span>  
  
```cpp  
coclass CLRRuntimeHost {  
    [default] interface  ICLRRuntimeHost;  
    interface            ICLRValidator;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="a8703-105">界面</span><span class="sxs-lookup"><span data-stu-id="a8703-105">Interfaces</span></span>  
  
|<span data-ttu-id="a8703-106">接口</span><span class="sxs-lookup"><span data-stu-id="a8703-106">Interface</span></span>|<span data-ttu-id="a8703-107">说明</span><span class="sxs-lookup"><span data-stu-id="a8703-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="a8703-108">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="a8703-108">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)|<span data-ttu-id="a8703-109">提供通过运行时控制应用程序执行的方法。</span><span class="sxs-lookup"><span data-stu-id="a8703-109">Provides methods for controlling the execution of applications by the runtime.</span></span>|  
|[<span data-ttu-id="a8703-110">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="a8703-110">ICLRValidator Interface</span></span>](iclrvalidator-interface.md)|<span data-ttu-id="a8703-111">提供可移植可执行映像的验证方法，并提供验证错误的详细报告。</span><span class="sxs-lookup"><span data-stu-id="a8703-111">Provides methods for validation of portable executable images and for detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a8703-112">要求</span><span class="sxs-lookup"><span data-stu-id="a8703-112">Requirements</span></span>  

 <span data-ttu-id="a8703-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a8703-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8703-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a8703-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="a8703-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a8703-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a8703-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8703-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8703-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8703-117">See also</span></span>

- [<span data-ttu-id="a8703-118">承载组件类</span><span class="sxs-lookup"><span data-stu-id="a8703-118">Hosting Coclasses</span></span>](hosting-coclasses.md)
