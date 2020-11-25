---
title: 'VerifyClientKey 函数 (非托管 API 参考) '
description: VerifyClientKey 函数可确保客户端密钥具有正确的安全性。
ms.date: 11/06/2017
api_name:
- VerifyClientKey
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- VerifyClientKey
helpviewer_keywords:
- VerifyClientKey function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 26cffe9936f2e01078b6f54e8499b58519f1018e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729416"
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="4ac1f-103">VerifyClientKey 函数</span><span class="sxs-lookup"><span data-stu-id="4ac1f-103">VerifyClientKey function</span></span>

<span data-ttu-id="4ac1f-104">确保客户端密钥具有正确的安全性。</span><span class="sxs-lookup"><span data-stu-id="4ac1f-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="4ac1f-105">语法</span><span class="sxs-lookup"><span data-stu-id="4ac1f-105">Syntax</span></span>  
  
```cpp  
LONG VerifyClientKey();
```  

## <a name="return-value"></a><span data-ttu-id="4ac1f-106">返回值</span><span class="sxs-lookup"><span data-stu-id="4ac1f-106">Return value</span></span>

<span data-ttu-id="4ac1f-107">如果该函数成功，则返回值为 `ERROR_SUCCESS` (0) 。</span><span class="sxs-lookup"><span data-stu-id="4ac1f-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="4ac1f-108">如果函数失败，则返回值为 *winerror.h* 中定义的非零错误代码。</span><span class="sxs-lookup"><span data-stu-id="4ac1f-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac1f-109">要求</span><span class="sxs-lookup"><span data-stu-id="4ac1f-109">Requirements</span></span>  

 <span data-ttu-id="4ac1f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4ac1f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ac1f-111">**标头：** WMINet_Utils .def</span><span class="sxs-lookup"><span data-stu-id="4ac1f-111">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="4ac1f-112">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4ac1f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ac1f-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4ac1f-113">See also</span></span>

- [<span data-ttu-id="4ac1f-114">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="4ac1f-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
