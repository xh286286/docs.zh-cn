---
title: ICLRValidator 接口
ms.date: 03/30/2017
api_name:
- ICLRValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRValidator
helpviewer_keywords:
- ICLRValidator interface [.NET Framework hosting]
ms.assetid: 2edd0a10-77fb-4173-91eb-f2970cc364d0
topic_type:
- apiref
ms.openlocfilehash: d9ccd5c6c91b1ab2166ff40a0fb2048e15927d3a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723943"
---
# <a name="iclrvalidator-interface"></a><span data-ttu-id="e2644-102">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="e2644-102">ICLRValidator Interface</span></span>

<span data-ttu-id="e2644-103">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="e2644-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e2644-104">方法</span><span class="sxs-lookup"><span data-stu-id="e2644-104">Methods</span></span>  
  
|<span data-ttu-id="e2644-105">方法</span><span class="sxs-lookup"><span data-stu-id="e2644-105">Method</span></span>|<span data-ttu-id="e2644-106">说明</span><span class="sxs-lookup"><span data-stu-id="e2644-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e2644-107">FormatEventInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e2644-107">FormatEventInfo Method</span></span>](iclrvalidator-formateventinfo-method.md)|<span data-ttu-id="e2644-108">获取有关指定验证错误的详细消息。</span><span class="sxs-lookup"><span data-stu-id="e2644-108">Gets a detailed message about the specified validation error.</span></span>|  
|[<span data-ttu-id="e2644-109">Validate 方法</span><span class="sxs-lookup"><span data-stu-id="e2644-109">Validate Method</span></span>](iclrvalidator-validate-method.md)|<span data-ttu-id="e2644-110">验证指定文件中的可移植可执行文件或 Microsoft 中间语言 (MSIL) 。</span><span class="sxs-lookup"><span data-stu-id="e2644-110">Validates the portable executable or Microsoft intermediate language (MSIL) in the specified file.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e2644-111">要求</span><span class="sxs-lookup"><span data-stu-id="e2644-111">Requirements</span></span>  

 <span data-ttu-id="e2644-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e2644-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2644-113">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="e2644-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="e2644-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e2644-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e2644-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2644-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2644-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2644-116">See also</span></span>

- [<span data-ttu-id="e2644-117">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="e2644-117">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="e2644-118">承载接口</span><span class="sxs-lookup"><span data-stu-id="e2644-118">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="e2644-119">CLRRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="e2644-119">CLRRuntimeHost Coclass</span></span>](clrruntimehost-coclass.md)
