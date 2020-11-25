---
title: SetNonAssemblyFlags 方法
ms.date: 03/30/2017
api_name:
- IALink.SetNonAssemblyFlags
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetNonAssemblyFlags
helpviewer_keywords:
- SetNonAssemblyFlags method
ms.assetid: f8ba6fc8-f5aa-4066-ac96-56332758f5ec
topic_type:
- apiref
ms.openlocfilehash: b7bcf530947c161decc9c01c07df310550d69738
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733758"
---
# <a name="setnonassemblyflags-method"></a><span data-ttu-id="2b7c8-102">SetNonAssemblyFlags 方法</span><span class="sxs-lookup"><span data-stu-id="2b7c8-102">SetNonAssemblyFlags Method</span></span>

<span data-ttu-id="2b7c8-103">设置不是程序集特定的标志。</span><span class="sxs-lookup"><span data-stu-id="2b7c8-103">Sets flags that are not assembly-specific.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b7c8-104">语法</span><span class="sxs-lookup"><span data-stu-id="2b7c8-104">Syntax</span></span>  
  
```cpp  
HRESULT SetNonAssemblyFlags(  
    AssemblyFlags afFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b7c8-105">参数</span><span class="sxs-lookup"><span data-stu-id="2b7c8-105">Parameters</span></span>  

 `afFlags`  
 <span data-ttu-id="2b7c8-106">ALink 标志。</span><span class="sxs-lookup"><span data-stu-id="2b7c8-106">ALink flags.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2b7c8-107">返回值</span><span class="sxs-lookup"><span data-stu-id="2b7c8-107">Return Value</span></span>  

 <span data-ttu-id="2b7c8-108">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="2b7c8-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b7c8-109">要求</span><span class="sxs-lookup"><span data-stu-id="2b7c8-109">Requirements</span></span>  

 <span data-ttu-id="2b7c8-110">需要 alink</span><span class="sxs-lookup"><span data-stu-id="2b7c8-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b7c8-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b7c8-111">See also</span></span>

- [<span data-ttu-id="2b7c8-112">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="2b7c8-112">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="2b7c8-113">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="2b7c8-113">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="2b7c8-114">ALink API</span><span class="sxs-lookup"><span data-stu-id="2b7c8-114">ALink API</span></span>](index.md)
