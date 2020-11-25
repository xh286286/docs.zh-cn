---
title: RunDll32ShimW 函数
ms.date: 03/30/2017
api_name:
- RunDll32ShimW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- RunDll32ShimW
helpviewer_keywords:
- RunDll32ShimW function [.NET Framework hosting]
ms.assetid: 9ea07b57-96e2-44df-8711-8fe6c119087f
topic_type:
- apiref
ms.openlocfilehash: dd053134792b80a006849e465bc0025cf77a9ad8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729949"
---
# <a name="rundll32shimw-function"></a><span data-ttu-id="445c2-102">RunDll32ShimW 函数</span><span class="sxs-lookup"><span data-stu-id="445c2-102">RunDll32ShimW Function</span></span>

<span data-ttu-id="445c2-103">执行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="445c2-103">Executes the specified command.</span></span>  
  
 <span data-ttu-id="445c2-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="445c2-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="445c2-105">语法</span><span class="sxs-lookup"><span data-stu-id="445c2-105">Syntax</span></span>  
  
```cpp  
HRESULT RunDll32ShimW (  
    [in] HWND        hwnd,  
    [in] HINSTANCE   hinst,  
    [in] LPCWSTR     lpszCmdLine,  
    [in] int         nCmdShow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="445c2-106">参数</span><span class="sxs-lookup"><span data-stu-id="445c2-106">Parameters</span></span>  

 `hwnd`  
 <span data-ttu-id="445c2-107">中将在其中显示命令输出的窗口的句柄。</span><span class="sxs-lookup"><span data-stu-id="445c2-107">[in] A handle to a window in which the command output will be displayed.</span></span>  
  
 `hinst`  
 <span data-ttu-id="445c2-108">中包含命令的库的句柄。</span><span class="sxs-lookup"><span data-stu-id="445c2-108">[in] A handle to the library that contains the command.</span></span>  
  
 `lpszCmdLine`  
 <span data-ttu-id="445c2-109">中一个字符串，指定要执行的命令。</span><span class="sxs-lookup"><span data-stu-id="445c2-109">[in] A string that specifies the command to be executed.</span></span>  
  
 `nCmdShow`  
 <span data-ttu-id="445c2-110">中一个整数，指定 "输出" 窗口的显示模式。</span><span class="sxs-lookup"><span data-stu-id="445c2-110">[in] An integer that specifies the display mode for the output window.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="445c2-111">要求</span><span class="sxs-lookup"><span data-stu-id="445c2-111">Requirements</span></span>  

 <span data-ttu-id="445c2-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="445c2-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="445c2-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="445c2-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="445c2-114">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="445c2-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="445c2-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="445c2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="445c2-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="445c2-116">See also</span></span>

- [<span data-ttu-id="445c2-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="445c2-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
