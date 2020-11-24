---
title: GetResolutionScope 方法
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
ms.openlocfilehash: 6318890dd6f0259d8d6a7675380684a129c14c8b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684665"
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="5c96c-102">GetResolutionScope 方法</span><span class="sxs-lookup"><span data-stu-id="5c96c-102">GetResolutionScope Method</span></span>

<span data-ttu-id="5c96c-103">检索给定类型的作用域。</span><span class="sxs-lookup"><span data-stu-id="5c96c-103">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c96c-104">语法</span><span class="sxs-lookup"><span data-stu-id="5c96c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c96c-105">参数</span><span class="sxs-lookup"><span data-stu-id="5c96c-105">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="5c96c-106">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="5c96c-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="5c96c-107">需要引用的文件。</span><span class="sxs-lookup"><span data-stu-id="5c96c-107">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="5c96c-108">在中定义类型的文件的标记，通常用 [ImportFile 方法](importfile-method.md)进行检索。</span><span class="sxs-lookup"><span data-stu-id="5c96c-108">Token of file that type is defined in, usually retrieved with [ImportFile Method](importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="5c96c-109">接收程序集或模块引用。</span><span class="sxs-lookup"><span data-stu-id="5c96c-109">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5c96c-110">返回值</span><span class="sxs-lookup"><span data-stu-id="5c96c-110">Return Value</span></span>  

 <span data-ttu-id="5c96c-111">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="5c96c-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c96c-112">要求</span><span class="sxs-lookup"><span data-stu-id="5c96c-112">Requirements</span></span>  

 <span data-ttu-id="5c96c-113">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="5c96c-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c96c-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c96c-114">See also</span></span>

- [<span data-ttu-id="5c96c-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="5c96c-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="5c96c-116">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="5c96c-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="5c96c-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="5c96c-117">ALink API</span></span>](index.md)
