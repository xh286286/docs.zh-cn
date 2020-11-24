---
title: CorRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CorRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRuntimeHost
helpviewer_keywords:
- CoRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 5833740b-7d67-44b4-865c-b5bf45e291e3
topic_type:
- apiref
ms.openlocfilehash: cd4e675b4ba50b47146428d204c28cc943c23c69
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687998"
---
# <a name="corruntimehost-coclass"></a><span data-ttu-id="0d070-102">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="0d070-102">CorRuntimeHost Coclass</span></span>

<span data-ttu-id="0d070-103">提供用于管理由公共语言运行时执行的应用程序的接口。</span><span class="sxs-lookup"><span data-stu-id="0d070-103">Provides interfaces for managing applications that are being executed by the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d070-104">语法</span><span class="sxs-lookup"><span data-stu-id="0d070-104">Syntax</span></span>  
  
```cpp  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="0d070-105">界面</span><span class="sxs-lookup"><span data-stu-id="0d070-105">Interfaces</span></span>  
  
|<span data-ttu-id="0d070-106">接口</span><span class="sxs-lookup"><span data-stu-id="0d070-106">Interface</span></span>|<span data-ttu-id="0d070-107">说明</span><span class="sxs-lookup"><span data-stu-id="0d070-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="0d070-108">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="0d070-108">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)|<span data-ttu-id="0d070-109">提供 (CLR) 配置公共语言运行时的方法。</span><span class="sxs-lookup"><span data-stu-id="0d070-109">Provides methods for configuring the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="0d070-110">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="0d070-110">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)|<span data-ttu-id="0d070-111">提供使宿主可以显式启动和停止公共语言运行时、创建和配置应用程序域、访问默认域和枚举进程中运行的所有域的方法。</span><span class="sxs-lookup"><span data-stu-id="0d070-111">Provides methods that enable the host to start and stop the common language runtime explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>|  
|[<span data-ttu-id="0d070-112">IDebuggerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="0d070-112">IDebuggerInfo Interface</span></span>](idebuggerinfo-interface.md)|<span data-ttu-id="0d070-113">提供用于获取有关调试服务状态的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0d070-113">Provides methods for obtaining information about the state of the debugging services.</span></span>|  
|[<span data-ttu-id="0d070-114">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="0d070-114">IGCHost Interface</span></span>](igchost-interface.md)|<span data-ttu-id="0d070-115">提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。</span><span class="sxs-lookup"><span data-stu-id="0d070-115">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>|  
|<span data-ttu-id="0d070-116">IValidator</span><span class="sxs-lookup"><span data-stu-id="0d070-116">"IValidator"</span></span>|<span data-ttu-id="0d070-117">提供可移植可执行映像的验证和验证错误的详细报告的方法。</span><span class="sxs-lookup"><span data-stu-id="0d070-117">Provides methods for validation of portable executable images and detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0d070-118">要求</span><span class="sxs-lookup"><span data-stu-id="0d070-118">Requirements</span></span>  

 <span data-ttu-id="0d070-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d070-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d070-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0d070-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="0d070-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0d070-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0d070-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d070-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d070-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d070-123">See also</span></span>

- [<span data-ttu-id="0d070-124">承载组件类</span><span class="sxs-lookup"><span data-stu-id="0d070-124">Hosting Coclasses</span></span>](hosting-coclasses.md)
