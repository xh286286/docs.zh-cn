---
title: 'ResetSecurity 函数 (非托管 API 参考) '
description: ResetSecurity 函数将模拟标记分配给当前线程。
ms.date: 11/06/2017
api_name:
- ResetSecurity
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ResetSecurity
helpviewer_keywords:
- ResetSecurity function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 259bef74356f16221f1453dd4086e2fbb26faa83
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721109"
---
# <a name="resetsecurity-function"></a><span data-ttu-id="a9993-103">ResetSecurity 函数</span><span class="sxs-lookup"><span data-stu-id="a9993-103">ResetSecurity function</span></span>

<span data-ttu-id="a9993-104">将提供的模拟令牌分配给当前线程。</span><span class="sxs-lookup"><span data-stu-id="a9993-104">Assigns the supplied impersonation token to the current thread.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a9993-105">语法</span><span class="sxs-lookup"><span data-stu-id="a9993-105">Syntax</span></span>  
  
```cpp  
HRESULT ResetSecurity (
   [in] HANDLE token
);
```  

## <a name="parameters"></a><span data-ttu-id="a9993-106">参数</span><span class="sxs-lookup"><span data-stu-id="a9993-106">Parameters</span></span>

`token`  
<span data-ttu-id="a9993-107">中要与当前线程关联的模拟标记。</span><span class="sxs-lookup"><span data-stu-id="a9993-107">[in] The impersonation token to associate with the current thread.</span></span> <span data-ttu-id="a9993-108">其值可为 `null`。</span><span class="sxs-lookup"><span data-stu-id="a9993-108">Its value can be `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9993-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a9993-109">Return value</span></span>

<span data-ttu-id="a9993-110">如果该函数成功，则返回值为 `S_OK` (0) 。</span><span class="sxs-lookup"><span data-stu-id="a9993-110">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="a9993-111">如果函数失败，则返回值为非零错误代码。</span><span class="sxs-lookup"><span data-stu-id="a9993-111">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="a9993-112">若要获取扩展的错误信息，请调用 [GetErrorInfo](geterrorinfo.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="a9993-112">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="a9993-113">要求</span><span class="sxs-lookup"><span data-stu-id="a9993-113">Requirements</span></span>  

 <span data-ttu-id="a9993-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9993-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9993-115">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="a9993-115">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="a9993-116">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a9993-116">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9993-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9993-117">See also</span></span>

- [<span data-ttu-id="a9993-118">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="a9993-118">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
