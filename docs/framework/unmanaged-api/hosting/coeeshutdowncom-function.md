---
title: CoEEShutDownCOM 函数
ms.date: 03/30/2017
api_name:
- CoEEShutDownCOM
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoEEShutDownCOM
helpviewer_keywords:
- CoEEShutDownCOM function [.NET Framework hosting]
ms.assetid: b634cae2-632f-4737-9be4-92d0652844d7
topic_type:
- apiref
ms.openlocfilehash: 774704698f92d546d6bafa61c65d18d083c65f89
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95716754"
---
# <a name="coeeshutdowncom-function"></a><span data-ttu-id="23c0d-102">CoEEShutDownCOM 函数</span><span class="sxs-lookup"><span data-stu-id="23c0d-102">CoEEShutDownCOM Function</span></span>

<span data-ttu-id="23c0d-103">强制公共语言运行时 (CLR) 释放它包含在运行时可调用包装器 (RCW) 中的所有接口指针。</span><span class="sxs-lookup"><span data-stu-id="23c0d-103">Forces the common language runtime (CLR) to release all interface pointers it holds inside runtime callable wrappers (RCW).</span></span> <span data-ttu-id="23c0d-104">这就产生了释放所有 RCW 缓存的效果。</span><span class="sxs-lookup"><span data-stu-id="23c0d-104">This has the effect of releasing all RCW caches.</span></span> <span data-ttu-id="23c0d-105">此全局函数在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="23c0d-105">This global function is deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="23c0d-106">相反，请使用特定运行时的入口点。</span><span class="sxs-lookup"><span data-stu-id="23c0d-106">Instead, use the entry point for a specific runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23c0d-107">语法</span><span class="sxs-lookup"><span data-stu-id="23c0d-107">Syntax</span></span>  
  
```cpp  
void CoEEShutDownCOM ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="23c0d-108">备注</span><span class="sxs-lookup"><span data-stu-id="23c0d-108">Remarks</span></span>  

 <span data-ttu-id="23c0d-109">`CoEEShutDownCOM`函数首先释放所有上下文和所有缓存中的所有 rcw，然后删除安装程序中的任何现有的弹出通知。</span><span class="sxs-lookup"><span data-stu-id="23c0d-109">The `CoEEShutDownCOM` function first releases all the RCWs in all contexts and in all caches, and then removes any tear-down notification existing in setup.</span></span> <span data-ttu-id="23c0d-110">不发生 DLL 卸载。</span><span class="sxs-lookup"><span data-stu-id="23c0d-110">No DLL unloading occurs.</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="23c0d-111">此函数影响加载到进程中的所有运行时。</span><span class="sxs-lookup"><span data-stu-id="23c0d-111">This function affects all runtimes that are loaded into the process.</span></span>  
  
 <span data-ttu-id="23c0d-112">从 .NET Framework 4 开始，在你想要影响的特定运行时上调用此函数的入口点。</span><span class="sxs-lookup"><span data-stu-id="23c0d-112">Beginning with the .NET Framework 4, call the entry point for this function on the specific runtime you want to affect.</span></span> <span data-ttu-id="23c0d-113">若要获取入口点，请调用 [ICLRRuntimeInfo：： GetProcAddress](iclrruntimeinfo-getprocaddress-method.md) 方法，并指定 "CoEEShutDownCOM"。</span><span class="sxs-lookup"><span data-stu-id="23c0d-113">To get the entry point, call the [ICLRRuntimeInfo::GetProcAddress](iclrruntimeinfo-getprocaddress-method.md) method and specify "CoEEShutDownCOM".</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="23c0d-114">要求</span><span class="sxs-lookup"><span data-stu-id="23c0d-114">Requirements</span></span>  

 <span data-ttu-id="23c0d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="23c0d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23c0d-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="23c0d-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="23c0d-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="23c0d-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="23c0d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="23c0d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23c0d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23c0d-119">See also</span></span>

- [<span data-ttu-id="23c0d-120">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="23c0d-120">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
