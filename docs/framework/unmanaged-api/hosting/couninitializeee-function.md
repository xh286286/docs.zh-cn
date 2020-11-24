---
title: CoUninitializeEE 函数
ms.date: 03/30/2017
api_name:
- CoUninitializeEE
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeEE
helpviewer_keywords:
- CoUninitializeEE function [.NET Framework hosting]
ms.assetid: 5f5a311a-839a-465f-89d9-ff1c74da9736
topic_type:
- apiref
ms.openlocfilehash: e6616392eaa23f8ba40247c5aabd12e4d530cea1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687842"
---
# <a name="couninitializeee-function"></a><span data-ttu-id="5d8be-102">CoUninitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="5d8be-102">CoUninitializeEE Function</span></span>

<span data-ttu-id="5d8be-103">`CoUninitializeEE` 已过时，不提供任何功能。</span><span class="sxs-lookup"><span data-stu-id="5d8be-103">`CoUninitializeEE` is obsolete and provides no functionality.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d8be-104">语法</span><span class="sxs-lookup"><span data-stu-id="5d8be-104">Syntax</span></span>  
  
```cpp  
void CoUninitializeEE (  
    BOOL fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="5d8be-105">备注</span><span class="sxs-lookup"><span data-stu-id="5d8be-105">Remarks</span></span>  

 <span data-ttu-id="5d8be-106">不能从进程中卸载公共语言运行时的执行引擎。</span><span class="sxs-lookup"><span data-stu-id="5d8be-106">The common language runtime execution engine cannot be unloaded from a process.</span></span> <span data-ttu-id="5d8be-107">若要关闭执行引擎，请调用 [CorExitProcess](corexitprocess-function.md)。</span><span class="sxs-lookup"><span data-stu-id="5d8be-107">To shut down the execution engine call [CorExitProcess](corexitprocess-function.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d8be-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d8be-108">See also</span></span>

- [<span data-ttu-id="5d8be-109">CoInitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="5d8be-109">CoInitializeEE Function</span></span>](coinitializeee-function.md)
- [<span data-ttu-id="5d8be-110">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="5d8be-110">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
