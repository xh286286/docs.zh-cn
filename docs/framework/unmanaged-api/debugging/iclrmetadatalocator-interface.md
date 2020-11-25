---
title: ICLRMetadataLocator 接口
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator
helpviewer_keywords:
- ICLRMetadataLocator interface [.NET Framework debugging]
ms.assetid: 43c944f4-406a-4df6-981e-0eabb33dd5d0
topic_type:
- apiref
ms.openlocfilehash: 69c52c13a4a0aca5094274de969ebed6e09651b2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723501"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="4012c-102">ICLRMetadataLocator 接口</span><span class="sxs-lookup"><span data-stu-id="4012c-102">ICLRMetadataLocator Interface</span></span>

<span data-ttu-id="4012c-103">由数据访问服务层用于在目标进程中查找程序集的元数据。</span><span class="sxs-lookup"><span data-stu-id="4012c-103">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4012c-104">方法</span><span class="sxs-lookup"><span data-stu-id="4012c-104">Methods</span></span>  
  
|<span data-ttu-id="4012c-105">方法</span><span class="sxs-lookup"><span data-stu-id="4012c-105">Method</span></span>|<span data-ttu-id="4012c-106">说明</span><span class="sxs-lookup"><span data-stu-id="4012c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4012c-107">GetMetadata 方法</span><span class="sxs-lookup"><span data-stu-id="4012c-107">GetMetadata Method</span></span>](iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="4012c-108">从目标进程中检索图像的元数据。</span><span class="sxs-lookup"><span data-stu-id="4012c-108">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4012c-109">注解</span><span class="sxs-lookup"><span data-stu-id="4012c-109">Remarks</span></span>  

 <span data-ttu-id="4012c-110">API 客户端（即调试器）必须针对特定的目标进程实现此接口。</span><span class="sxs-lookup"><span data-stu-id="4012c-110">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="4012c-111">例如，实时过程的实现与内存转储的实现不同。</span><span class="sxs-lookup"><span data-stu-id="4012c-111">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4012c-112">要求</span><span class="sxs-lookup"><span data-stu-id="4012c-112">Requirements</span></span>  

 <span data-ttu-id="4012c-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4012c-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4012c-114">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="4012c-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="4012c-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4012c-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4012c-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4012c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4012c-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4012c-117">See also</span></span>

- [<span data-ttu-id="4012c-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="4012c-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
