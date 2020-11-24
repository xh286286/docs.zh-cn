---
title: GetCORVersion 函数
ms.date: 03/30/2017
api_name:
- GetCORVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetCORVersion
helpviewer_keywords:
- GetCORVersion function [.NET Framework hosting]
ms.assetid: 2f09cd37-bf3a-4cc5-87b0-adc42a7eed31
topic_type:
- apiref
ms.openlocfilehash: e7ef3f300c8cfa0c275d15913e171abe09385eea
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95681192"
---
# <a name="getcorversion-function"></a><span data-ttu-id="e355d-102">GetCORVersion 函数</span><span class="sxs-lookup"><span data-stu-id="e355d-102">GetCORVersion Function</span></span>

<span data-ttu-id="e355d-103">返回当前进程中运行 (CLR) 的公共语言运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="e355d-103">Returns the version number of the common language runtime (CLR) that is running in the current process.</span></span>  
  
 <span data-ttu-id="e355d-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="e355d-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e355d-105">语法</span><span class="sxs-lookup"><span data-stu-id="e355d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCORVersion (  
    [in] LPWSTR  pbuffer,  
    [in]  DWORD   cchBuffer,
    [out] DWORD*  dwlength  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="e355d-106">参数</span><span class="sxs-lookup"><span data-stu-id="e355d-106">Parameters</span></span>  

 `pbuffer`  
 <span data-ttu-id="e355d-107">指向缓冲区的指针，CLR 在此缓冲区中返回一个字符串，该字符串指定当前加载到进程中的运行时版本。</span><span class="sxs-lookup"><span data-stu-id="e355d-107">A pointer to a buffer in which the CLR returns a string specifying the version of the runtime that is currently loaded into the process.</span></span> <span data-ttu-id="e355d-108">返回的字符串采用与传递到 [CorBindToRuntimeEx](corbindtoruntimeex-function.md)的字符串相同的形式，例如 "v 1.0.1216"。</span><span class="sxs-lookup"><span data-stu-id="e355d-108">The returned string takes the same form as strings passed to [CorBindToRuntimeEx](corbindtoruntimeex-function.md), for example, "v1.0.1216".</span></span> <span data-ttu-id="e355d-109">如果运行时尚未加载到进程中，则该函数将为计算机上安装的最新版本的运行时返回相应的目录信息。</span><span class="sxs-lookup"><span data-stu-id="e355d-109">If the runtime has not yet been loaded into the process, the function returns the appropriate directory information for the latest version of the runtime installed on the computer.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="e355d-110">可以保存的)  (字符数 `WCHAR` `pbuffer` 。</span><span class="sxs-lookup"><span data-stu-id="e355d-110">The number of characters (`WCHAR`s) that can be held in `pbuffer`.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="e355d-111">一个指针，指向中实际返回的字符数 `pbuffer` 。</span><span class="sxs-lookup"><span data-stu-id="e355d-111">A pointer to the number of characters actually returned in `pbuffer`.</span></span> <span data-ttu-id="e355d-112">如果 `pbuffer` 为 null 指针，则运行时返回 E_POINTER。</span><span class="sxs-lookup"><span data-stu-id="e355d-112">If `pbuffer` is a null pointer, the runtime returns E_POINTER.</span></span> <span data-ttu-id="e355d-113">如果字符数超过了的长度 `pbuffer` ，则运行时返回 ERROR_INSUFFICIENT_BUFFER。</span><span class="sxs-lookup"><span data-stu-id="e355d-113">If the number of characters is greater then the length of `pbuffer` , the runtime returns ERROR_INSUFFICIENT_BUFFER.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e355d-114">要求</span><span class="sxs-lookup"><span data-stu-id="e355d-114">Requirements</span></span>  

 <span data-ttu-id="e355d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e355d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e355d-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e355d-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e355d-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e355d-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e355d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e355d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e355d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e355d-119">See also</span></span>

- [<span data-ttu-id="e355d-120">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="e355d-120">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
