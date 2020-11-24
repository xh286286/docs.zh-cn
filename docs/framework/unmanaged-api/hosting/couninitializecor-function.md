---
title: CoUninitializeCor 函数
ms.date: 03/30/2017
api_name:
- CoUninitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeCor
helpviewer_keywords:
- CoUninitializeCor function [.NET Framework hosting]
ms.assetid: 50a95b8b-9766-470e-bb29-2c7ecddfd4a1
topic_type:
- apiref
ms.openlocfilehash: 7d39c6fda6f159bfc937f62dc45d0d7ce37657f3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687876"
---
# <a name="couninitializecor-function"></a><span data-ttu-id="5a805-102">CoUninitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="5a805-102">CoUninitializeCor Function</span></span>

<span data-ttu-id="5a805-103">`CoUninitializeCor` 已过时。</span><span class="sxs-lookup"><span data-stu-id="5a805-103">`CoUninitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a805-104">语法</span><span class="sxs-lookup"><span data-stu-id="5a805-104">Syntax</span></span>  
  
```cpp  
STDAPI_(void) CoUninitializeCor(void);  
```  
  
## <a name="remarks"></a><span data-ttu-id="5a805-105">备注</span><span class="sxs-lookup"><span data-stu-id="5a805-105">Remarks</span></span>  

 <span data-ttu-id="5a805-106">公共语言运行时无法从进程中卸载。</span><span class="sxs-lookup"><span data-stu-id="5a805-106">The common language runtime cannot be unloaded from a process.</span></span> <span data-ttu-id="5a805-107">若要从正在运行的进程中完全删除运行时，则必须关闭该进程。</span><span class="sxs-lookup"><span data-stu-id="5a805-107">To completely remove the runtime from a running process, you must shut down that process.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a805-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5a805-108">See also</span></span>

- [<span data-ttu-id="5a805-109">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="5a805-109">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
