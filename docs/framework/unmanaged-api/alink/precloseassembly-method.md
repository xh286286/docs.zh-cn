---
title: PreCloseAssembly 方法
ms.date: 03/30/2017
api_name:
- IALink.PreCloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- PreCloseAssembly
helpviewer_keywords:
- PreCloseAssembly method
ms.assetid: 6d23ac54-15ea-4027-a172-9ebef43e8f56
topic_type:
- apiref
ms.openlocfilehash: 31c0c5e23d1a985c2005693e25ca91379037482a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728675"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="ca9c0-102">PreCloseAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="ca9c0-102">PreCloseAssembly Method</span></span>

<span data-ttu-id="ca9c0-103">关闭程序集文件。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-103">Closes the assembly file.</span></span> <span data-ttu-id="ca9c0-104">在关闭所有其他文件之后但在关闭程序集文件之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="ca9c0-105">不要对未绑定的模块调用此方法。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca9c0-106">语法</span><span class="sxs-lookup"><span data-stu-id="ca9c0-106">Syntax</span></span>  
  
```cpp  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ca9c0-107">参数</span><span class="sxs-lookup"><span data-stu-id="ca9c0-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="ca9c0-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ca9c0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ca9c0-109">Return Value</span></span>  

 <span data-ttu-id="ca9c0-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca9c0-111">要求</span><span class="sxs-lookup"><span data-stu-id="ca9c0-111">Requirements</span></span>  

 <span data-ttu-id="ca9c0-112">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="ca9c0-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca9c0-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca9c0-113">See also</span></span>

- [<span data-ttu-id="ca9c0-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="ca9c0-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="ca9c0-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="ca9c0-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="ca9c0-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="ca9c0-116">ALink API</span></span>](index.md)
