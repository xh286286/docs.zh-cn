---
title: NukeDownloadedCache 函数
ms.date: 03/30/2017
api_name:
- NukeDownloadedCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- NukeDownloadedCache
helpviewer_keywords:
- NukeDownloadedCache function [.NET Framework fusion]
ms.assetid: fac2b1c6-6fa3-4818-805b-b63972024c86
topic_type:
- apiref
ms.openlocfilehash: 5ae0a887d666a150b717d495848c8a411d030a09
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728571"
---
# <a name="nukedownloadedcache-function"></a><span data-ttu-id="dd064-102">NukeDownloadedCache 函数</span><span class="sxs-lookup"><span data-stu-id="dd064-102">NukeDownloadedCache Function</span></span>

<span data-ttu-id="dd064-103">删除公共语言运行时 (CLR) 下载缓存。</span><span class="sxs-lookup"><span data-stu-id="dd064-103">Deletes the common language runtime (CLR) download cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd064-104">语法</span><span class="sxs-lookup"><span data-stu-id="dd064-104">Syntax</span></span>  
  
```cpp  
HRESULT NukeDownloadedCache();  
```  
  
## <a name="return-value"></a><span data-ttu-id="dd064-105">返回值</span><span class="sxs-lookup"><span data-stu-id="dd064-105">Return Value</span></span>  

 <span data-ttu-id="dd064-106">此方法返回 Winerror.h 中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="dd064-106">This method returns standard COM error codes, as defined in WinError.h.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd064-107">注解</span><span class="sxs-lookup"><span data-stu-id="dd064-107">Remarks</span></span>  

 <span data-ttu-id="dd064-108">CLR 下载缓存是存储从 URL 下载的具有强名称的程序集以便可以重复使用的区域。</span><span class="sxs-lookup"><span data-stu-id="dd064-108">The CLR download cache is the area where strong-named assemblies that are downloaded from a URL are stored for possible reuse.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd064-109">要求</span><span class="sxs-lookup"><span data-stu-id="dd064-109">Requirements</span></span>  

 <span data-ttu-id="dd064-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dd064-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd064-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="dd064-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="dd064-112">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="dd064-112">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="dd064-113">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="dd064-113">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="dd064-114">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd064-114">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd064-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dd064-115">See also</span></span>

- [<span data-ttu-id="dd064-116">CreateHistoryReader 函数</span><span class="sxs-lookup"><span data-stu-id="dd064-116">CreateHistoryReader Function</span></span>](createhistoryreader-function.md)
- [<span data-ttu-id="dd064-117">GetHistoryFileDirectory 函数</span><span class="sxs-lookup"><span data-stu-id="dd064-117">GetHistoryFileDirectory Function</span></span>](gethistoryfiledirectory-function.md)
- [<span data-ttu-id="dd064-118">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="dd064-118">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
