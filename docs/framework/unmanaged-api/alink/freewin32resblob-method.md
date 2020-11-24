---
title: FreeWin32ResBlob 方法
ms.date: 03/30/2017
api_name:
- IALink.FreeWin32ResBlob
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- FreeWin32ResBlob
helpviewer_keywords:
- FreeWin32ResBlob method
ms.assetid: d941102b-2679-4c49-b15e-c0fc9c53e11f
topic_type:
- apiref
ms.openlocfilehash: 44c5228f7ee467abd02a9ec09590d0352fc82036
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684754"
---
# <a name="freewin32resblob-method"></a><span data-ttu-id="71cbe-102">FreeWin32ResBlob 方法</span><span class="sxs-lookup"><span data-stu-id="71cbe-102">FreeWin32ResBlob Method</span></span>

<span data-ttu-id="71cbe-103">释放 Win32 资源 blob 和关联的资源。</span><span class="sxs-lookup"><span data-stu-id="71cbe-103">Releases the Win32 resource blob and associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71cbe-104">语法</span><span class="sxs-lookup"><span data-stu-id="71cbe-104">Syntax</span></span>  
  
```cpp  
HRESULT FreeWin32ResBlob(  
    const void** ppResBlob  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="71cbe-105">参数</span><span class="sxs-lookup"><span data-stu-id="71cbe-105">Parameters</span></span>  

 `ppResBlob`  
 <span data-ttu-id="71cbe-106">要释放的资源 blob。</span><span class="sxs-lookup"><span data-stu-id="71cbe-106">The resource blob to be released.</span></span> <span data-ttu-id="71cbe-107">此方法将 blob 指针赋给 NULL。</span><span class="sxs-lookup"><span data-stu-id="71cbe-107">This method assigns the blob pointer to NULL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="71cbe-108">返回值</span><span class="sxs-lookup"><span data-stu-id="71cbe-108">Return Value</span></span>  

 <span data-ttu-id="71cbe-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="71cbe-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="71cbe-110">要求</span><span class="sxs-lookup"><span data-stu-id="71cbe-110">Requirements</span></span>  

 <span data-ttu-id="71cbe-111">需要 alink</span><span class="sxs-lookup"><span data-stu-id="71cbe-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71cbe-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71cbe-112">See also</span></span>

- [<span data-ttu-id="71cbe-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="71cbe-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="71cbe-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="71cbe-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="71cbe-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="71cbe-115">ALink API</span></span>](index.md)
