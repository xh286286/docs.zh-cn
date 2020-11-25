---
title: IValidator 接口
ms.date: 03/30/2017
api_name:
- IValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IValidator
helpviewer_keywords:
- IValidator interface [.NET Framework hosting]
ms.assetid: b297e3b0-20f9-478f-b707-5e2eecb2b5b2
topic_type:
- apiref
ms.openlocfilehash: ce417402231d03828243bfb8bb7543c0a644a882
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700985"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="16734-102">IValidator 接口</span><span class="sxs-lookup"><span data-stu-id="16734-102">IValidator Interface</span></span>

<span data-ttu-id="16734-103">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="16734-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="16734-104">方法</span><span class="sxs-lookup"><span data-stu-id="16734-104">Methods</span></span>  
  
|<span data-ttu-id="16734-105">方法</span><span class="sxs-lookup"><span data-stu-id="16734-105">Method</span></span>|<span data-ttu-id="16734-106">说明</span><span class="sxs-lookup"><span data-stu-id="16734-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="16734-107">验证</span><span class="sxs-lookup"><span data-stu-id="16734-107">Validate</span></span>|<span data-ttu-id="16734-108">验证指定的 PE 或 Microsoft 中间语言 (MSIL) 文件。</span><span class="sxs-lookup"><span data-stu-id="16734-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="16734-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="16734-109">FormatEventInfo</span></span>|<span data-ttu-id="16734-110">获取与指定的验证错误相对应的错误消息。</span><span class="sxs-lookup"><span data-stu-id="16734-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="16734-111">要求</span><span class="sxs-lookup"><span data-stu-id="16734-111">Requirements</span></span>  

 <span data-ttu-id="16734-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="16734-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16734-113">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="16734-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="16734-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="16734-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="16734-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16734-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16734-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16734-116">See also</span></span>

- [<span data-ttu-id="16734-117">承载接口</span><span class="sxs-lookup"><span data-stu-id="16734-117">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="16734-118">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="16734-118">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)
