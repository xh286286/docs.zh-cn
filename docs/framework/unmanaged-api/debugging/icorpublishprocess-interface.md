---
title: ICorPublishProcess 接口
ms.date: 03/30/2017
api_name:
- ICorPublishProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess
helpviewer_keywords:
- ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 6d1dc41b-8aa2-4889-bb00-1cbccc00c123
topic_type:
- apiref
ms.openlocfilehash: 8ee59e9d416d1c53312e4fccb6953f20b03b29b3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95693081"
---
# <a name="icorpublishprocess-interface"></a><span data-ttu-id="35475-102">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="35475-102">ICorPublishProcess Interface</span></span>

<span data-ttu-id="35475-103">提供用于访问要显示的有关进程的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="35475-103">Provides methods that access information to be displayed about a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="35475-104">方法</span><span class="sxs-lookup"><span data-stu-id="35475-104">Methods</span></span>  
  
|<span data-ttu-id="35475-105">方法</span><span class="sxs-lookup"><span data-stu-id="35475-105">Method</span></span>|<span data-ttu-id="35475-106">说明</span><span class="sxs-lookup"><span data-stu-id="35475-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="35475-107">EnumAppDomains 方法</span><span class="sxs-lookup"><span data-stu-id="35475-107">EnumAppDomains Method</span></span>](icorpublishprocess-enumappdomains-method.md)|<span data-ttu-id="35475-108">获取一个 [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) 实例，其中包含此所引用的进程中的应用程序域 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="35475-108">Gets an [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) instance that contains the application domains in the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="35475-109">GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="35475-109">GetDisplayName Method</span></span>](icorpublishprocess-getdisplayname-method.md)|<span data-ttu-id="35475-110">获取此引用的进程的可执行文件的完整路径 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="35475-110">Gets the full path of the executable for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="35475-111">GetProcessID 方法</span><span class="sxs-lookup"><span data-stu-id="35475-111">GetProcessID Method</span></span>](icorpublishprocess-getprocessid-method.md)|<span data-ttu-id="35475-112">获取此引用的进程的操作系统标识符 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="35475-112">Gets the operating system identifier for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="35475-113">IsManaged 方法</span><span class="sxs-lookup"><span data-stu-id="35475-113">IsManaged Method</span></span>](icorpublishprocess-ismanaged-method.md)|<span data-ttu-id="35475-114">获取一个值，该值指示由此引用的进程是否 `ICorPublishProcess` 已知正在运行托管代码。</span><span class="sxs-lookup"><span data-stu-id="35475-114">Gets a value that indicates whether the process referenced by this `ICorPublishProcess` is known to be running managed code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="35475-115">要求</span><span class="sxs-lookup"><span data-stu-id="35475-115">Requirements</span></span>  

 <span data-ttu-id="35475-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="35475-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35475-117">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="35475-117">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="35475-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="35475-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="35475-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35475-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35475-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35475-120">See also</span></span>

- [<span data-ttu-id="35475-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="35475-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="35475-122">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="35475-122">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
