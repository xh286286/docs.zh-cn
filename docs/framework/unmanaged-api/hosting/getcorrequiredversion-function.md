---
title: GetCORRequiredVersion 函数
ms.date: 03/30/2017
api_name:
- GetCORRequiredVersion
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetCORRequiredVersion
helpviewer_keywords:
- GetCORRequiredVersion function [.NET Framework hosting]
ms.assetid: 1588fe7b-c378-4f4b-9c4b-48647f1119cc
topic_type:
- apiref
ms.openlocfilehash: 9590d19f4e5f5890af53a108492bd1b6d130fb72
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95704495"
---
# <a name="getcorrequiredversion-function"></a><span data-ttu-id="c4662-102">GetCORRequiredVersion 函数</span><span class="sxs-lookup"><span data-stu-id="c4662-102">GetCORRequiredVersion Function</span></span>

<span data-ttu-id="c4662-103">获取 CLR) 版本号 (所需的公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="c4662-103">Gets the required common language runtime (CLR) version number.</span></span>  
  
 <span data-ttu-id="c4662-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="c4662-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4662-105">语法</span><span class="sxs-lookup"><span data-stu-id="c4662-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCORRequiredVersion (  
    [out] LPWSTR   pbuffer,  
    [in]  DWORD    cchBuffer,  
    [out] DWORD   *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4662-106">参数</span><span class="sxs-lookup"><span data-stu-id="c4662-106">Parameters</span></span>  

 `pbuffer`  
 <span data-ttu-id="c4662-107">弄包含指定版本号的字符串的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="c4662-107">[out] A buffer containing a string that specifies the version number.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="c4662-108">中缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c4662-108">[in] The size, in bytes, of the buffer.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="c4662-109">弄缓冲区中返回的字节数。</span><span class="sxs-lookup"><span data-stu-id="c4662-109">[out] The number of bytes returned in the buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4662-110">要求</span><span class="sxs-lookup"><span data-stu-id="c4662-110">Requirements</span></span>  

 <span data-ttu-id="c4662-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4662-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4662-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c4662-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c4662-113">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c4662-113">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c4662-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4662-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4662-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4662-115">See also</span></span>

- [<span data-ttu-id="c4662-116">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="c4662-116">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
