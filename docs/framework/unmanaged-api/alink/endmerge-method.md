---
title: EndMerge 方法
ms.date: 03/30/2017
api_name:
- IALink.EndMerge
- EndMerge
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EndMerge
helpviewer_keywords:
- EndMerge method
ms.assetid: 1d03bb15-a2c8-4a04-8fc6-b126c89c3778
topic_type:
- apiref
ms.openlocfilehash: ed4ac7b12caa0dd78b79554258de62b8752553e0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684923"
---
# <a name="endmerge-method"></a><span data-ttu-id="03cd7-102">EndMerge 方法</span><span class="sxs-lookup"><span data-stu-id="03cd7-102">EndMerge Method</span></span>

<span data-ttu-id="03cd7-103">指示所有自定义特性都已合并到发出范围中。</span><span class="sxs-lookup"><span data-stu-id="03cd7-103">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03cd7-104">语法</span><span class="sxs-lookup"><span data-stu-id="03cd7-104">Syntax</span></span>  
  
```cpp  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="03cd7-105">参数</span><span class="sxs-lookup"><span data-stu-id="03cd7-105">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="03cd7-106">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="03cd7-106">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="03cd7-107">返回值</span><span class="sxs-lookup"><span data-stu-id="03cd7-107">Return Value</span></span>  

 <span data-ttu-id="03cd7-108">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="03cd7-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="03cd7-109">要求</span><span class="sxs-lookup"><span data-stu-id="03cd7-109">Requirements</span></span>  

 <span data-ttu-id="03cd7-110">需要 alink</span><span class="sxs-lookup"><span data-stu-id="03cd7-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03cd7-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="03cd7-111">See also</span></span>

- [<span data-ttu-id="03cd7-112">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="03cd7-112">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="03cd7-113">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="03cd7-113">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="03cd7-114">ALink API</span><span class="sxs-lookup"><span data-stu-id="03cd7-114">ALink API</span></span>](index.md)
