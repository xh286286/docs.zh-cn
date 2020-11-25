---
title: CloseAssembly 方法
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
ms.openlocfilehash: 4e8aeef3520c4d5c9735b2c8975ac1e39470ba93
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717014"
---
# <a name="closeassembly-method"></a><span data-ttu-id="2edbe-102">CloseAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="2edbe-102">CloseAssembly Method</span></span>

<span data-ttu-id="2edbe-103">终结程序集操作。</span><span class="sxs-lookup"><span data-stu-id="2edbe-103">Finalizes assembly operations.</span></span> <span data-ttu-id="2edbe-104">在开始新的程序集或未绑定的模块之前，请调用此方法。</span><span class="sxs-lookup"><span data-stu-id="2edbe-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2edbe-105">语法</span><span class="sxs-lookup"><span data-stu-id="2edbe-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="2edbe-106">参数</span><span class="sxs-lookup"><span data-stu-id="2edbe-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="2edbe-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="2edbe-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2edbe-108">返回值</span><span class="sxs-lookup"><span data-stu-id="2edbe-108">Return Value</span></span>  

 <span data-ttu-id="2edbe-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="2edbe-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2edbe-110">要求</span><span class="sxs-lookup"><span data-stu-id="2edbe-110">Requirements</span></span>  

 <span data-ttu-id="2edbe-111">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="2edbe-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2edbe-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2edbe-112">See also</span></span>

- [<span data-ttu-id="2edbe-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="2edbe-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="2edbe-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="2edbe-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="2edbe-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="2edbe-115">ALink API</span></span>](index.md)
