---
title: CorExitProcess 函数
ms.date: 03/30/2017
api_name:
- CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CorExitProcess
helpviewer_keywords:
- CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type:
- apiref
ms.openlocfilehash: f6d8114732a3b7c15d0a0258a28a362d661b030a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673617"
---
# <a name="corexitprocess-function"></a><span data-ttu-id="eb02c-102">CorExitProcess 函数</span><span class="sxs-lookup"><span data-stu-id="eb02c-102">CorExitProcess Function</span></span>

<span data-ttu-id="eb02c-103">关闭当前的非托管进程。</span><span class="sxs-lookup"><span data-stu-id="eb02c-103">Shuts down the current unmanaged process.</span></span>  
  
 <span data-ttu-id="eb02c-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="eb02c-104">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="eb02c-105">改为使用 [ICLRMetaHost：： ExitProcess](iclrmetahost-exitprocess-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb02c-105">Use the [ICLRMetaHost::ExitProcess](iclrmetahost-exitprocess-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb02c-106">语法</span><span class="sxs-lookup"><span data-stu-id="eb02c-106">Syntax</span></span>  
  
```cpp  
void STDMETHODCALLTYPE CorExitProcess (
  int  exitCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb02c-107">参数</span><span class="sxs-lookup"><span data-stu-id="eb02c-107">Parameters</span></span>  

 `exitCode`  
 <span data-ttu-id="eb02c-108">一个整数，指定进程退出代码。</span><span class="sxs-lookup"><span data-stu-id="eb02c-108">An integer that specifies the process exit code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb02c-109">注解</span><span class="sxs-lookup"><span data-stu-id="eb02c-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="eb02c-110">从 .NET Framework 4 开始， `CorExitProcess` 退出进程中的每个已启动的运行时，而不只是旧 api 所绑定到的运行时。</span><span class="sxs-lookup"><span data-stu-id="eb02c-110">Beginning with the .NET Framework 4, `CorExitProcess` exits every started runtime in the process, not just the runtime to which the legacy APIs have been bound.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb02c-111">要求</span><span class="sxs-lookup"><span data-stu-id="eb02c-111">Requirements</span></span>  

 <span data-ttu-id="eb02c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eb02c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb02c-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="eb02c-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="eb02c-114">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="eb02c-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="eb02c-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb02c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb02c-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb02c-116">See also</span></span>

- [<span data-ttu-id="eb02c-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="eb02c-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
