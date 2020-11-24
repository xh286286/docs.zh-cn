---
title: EmitAssembly 方法
ms.date: 03/30/2017
api_name:
- IALink2.EmitAssembly
- EmitAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssembly
helpviewer_keywords:
- EmitAssembly method
ms.assetid: 605ff39e-e5cc-4bff-8196-e8d68a9715b9
topic_type:
- apiref
ms.openlocfilehash: b85b2576660f77eb901c504d398e8bc7909882f7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95676369"
---
# <a name="emitassembly-method"></a><span data-ttu-id="4dc7e-102">EmitAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="4dc7e-102">EmitAssembly Method</span></span>

<span data-ttu-id="4dc7e-103">创建程序集。</span><span class="sxs-lookup"><span data-stu-id="4dc7e-103">Creates the assembly.</span></span> <span data-ttu-id="4dc7e-104">除程序集文件以外的所有其他文件关闭后，调用此方法。</span><span class="sxs-lookup"><span data-stu-id="4dc7e-104">Call this method after all other files are closed except for the assembly file.</span></span> <span data-ttu-id="4dc7e-105">在生成未绑定的模块时不要调用此方法。</span><span class="sxs-lookup"><span data-stu-id="4dc7e-105">Do not call this method when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4dc7e-106">语法</span><span class="sxs-lookup"><span data-stu-id="4dc7e-106">Syntax</span></span>  
  
```cpp  
HRESULT EmitAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="4dc7e-107">参数</span><span class="sxs-lookup"><span data-stu-id="4dc7e-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="4dc7e-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="4dc7e-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4dc7e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="4dc7e-109">Return Value</span></span>  

 <span data-ttu-id="4dc7e-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="4dc7e-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4dc7e-111">要求</span><span class="sxs-lookup"><span data-stu-id="4dc7e-111">Requirements</span></span>  

 <span data-ttu-id="4dc7e-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="4dc7e-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4dc7e-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4dc7e-113">See also</span></span>

- [<span data-ttu-id="4dc7e-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="4dc7e-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="4dc7e-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="4dc7e-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="4dc7e-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="4dc7e-116">ALink API</span></span>](index.md)
