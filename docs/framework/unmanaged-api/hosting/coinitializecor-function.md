---
title: CoInitializeCor 函数
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
ms.openlocfilehash: 9d077d5c5a414568b5643cad0171e101d7bb06f9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731704"
---
# <a name="coinitializecor-function"></a><span data-ttu-id="0fac7-102">CoInitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="0fac7-102">CoInitializeCor Function</span></span>

<span data-ttu-id="0fac7-103">`CoInitializeCor` 已过时。</span><span class="sxs-lookup"><span data-stu-id="0fac7-103">`CoInitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fac7-104">语法</span><span class="sxs-lookup"><span data-stu-id="0fac7-104">Syntax</span></span>  
  
```cpp  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="0fac7-105">备注</span><span class="sxs-lookup"><span data-stu-id="0fac7-105">Remarks</span></span>  

 <span data-ttu-id="0fac7-106">若要初始化公共语言运行时，请使用 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 或 [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md)。</span><span class="sxs-lookup"><span data-stu-id="0fac7-106">To initialize the common language runtime, use either [CorBindToRuntimeEx](corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fac7-107">要求</span><span class="sxs-lookup"><span data-stu-id="0fac7-107">Requirements</span></span>  

 <span data-ttu-id="0fac7-108">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0fac7-108">**Header:** Cor.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fac7-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0fac7-109">See also</span></span>

- [<span data-ttu-id="0fac7-110">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="0fac7-110">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
