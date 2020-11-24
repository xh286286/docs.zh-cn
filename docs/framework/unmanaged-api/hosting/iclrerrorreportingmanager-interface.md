---
title: ICLRErrorReportingManager 接口
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
ms.openlocfilehash: d3816c8a3b6204b053505aa888eb28d696f8990b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677833"
---
# <a name="iclrerrorreportingmanager-interface"></a><span data-ttu-id="0632a-102">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="0632a-102">ICLRErrorReportingManager Interface</span></span>

<span data-ttu-id="0632a-103">提供允许主机配置自定义堆栈转储以用于错误报告的方法。</span><span class="sxs-lookup"><span data-stu-id="0632a-103">Provides methods that allow the host to configure custom stack dumps for error reporting.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0632a-104">方法</span><span class="sxs-lookup"><span data-stu-id="0632a-104">Methods</span></span>  
  
|<span data-ttu-id="0632a-105">方法</span><span class="sxs-lookup"><span data-stu-id="0632a-105">Method</span></span>|<span data-ttu-id="0632a-106">说明</span><span class="sxs-lookup"><span data-stu-id="0632a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0632a-107">BeginCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="0632a-107">BeginCustomDump Method</span></span>](iclrerrorreportingmanager-begincustomdump-method.md)|<span data-ttu-id="0632a-108">指定用于错误报告的自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="0632a-108">Specifies the configuration of custom stack dumps for error reporting.</span></span>|  
|[<span data-ttu-id="0632a-109">EndCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="0632a-109">EndCustomDump Method</span></span>](iclrerrorreportingmanager-endcustomdump-method.md)|<span data-ttu-id="0632a-110">清除由先前对的调用设置的自定义堆栈转储配置 `BeginCustomDump` 。</span><span class="sxs-lookup"><span data-stu-id="0632a-110">Clears the custom stack dump configuration that was set by an earlier call to `BeginCustomDump`.</span></span>|  
|[<span data-ttu-id="0632a-111">GetBucketParametersForCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="0632a-111">GetBucketParametersForCurrentException Method</span></span>](iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|<span data-ttu-id="0632a-112">获取调用线程上的当前异常的 Watson 存储桶。</span><span class="sxs-lookup"><span data-stu-id="0632a-112">Gets the Watson bucket for the current exception on the calling thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0632a-113">注解</span><span class="sxs-lookup"><span data-stu-id="0632a-113">Remarks</span></span>  

 <span data-ttu-id="0632a-114">`BeginCustomDump`方法设置自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="0632a-114">The `BeginCustomDump` method sets custom stack dump configuration.</span></span> <span data-ttu-id="0632a-115">`EndCustomDump`方法清除自定义堆栈转储配置并释放任何关联的状态。</span><span class="sxs-lookup"><span data-stu-id="0632a-115">The `EndCustomDump` method clears the custom stack dump configuration and frees any associated state.</span></span> <span data-ttu-id="0632a-116">应在自定义转储完成后调用它。</span><span class="sxs-lookup"><span data-stu-id="0632a-116">It should be called after the custom dump is complete.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="0632a-117">调用失败 `EndCustomDump` 会导致内存泄露。</span><span class="sxs-lookup"><span data-stu-id="0632a-117">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0632a-118">要求</span><span class="sxs-lookup"><span data-stu-id="0632a-118">Requirements</span></span>  

 <span data-ttu-id="0632a-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0632a-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0632a-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0632a-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0632a-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0632a-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0632a-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0632a-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0632a-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0632a-123">See also</span></span>

- [<span data-ttu-id="0632a-124">ECustomDumpItemKind 枚举</span><span class="sxs-lookup"><span data-stu-id="0632a-124">ECustomDumpItemKind Enumeration</span></span>](ecustomdumpitemkind-enumeration.md)
- [<span data-ttu-id="0632a-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="0632a-125">Hosting Interfaces</span></span>](hosting-interfaces.md)
