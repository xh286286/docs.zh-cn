---
title: ISymUnmanagedWriter3::OpenMethod2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.OpenMethod2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::OpenMethod2
helpviewer_keywords:
- ISymUnmanagedWriter3::OpenMethod2 method [.NET Framework debugging]
- OpenMethod2 method [.NET Framework debugging]
ms.assetid: 025e358c-448f-4423-a2f2-57acf437c8a5
topic_type:
- apiref
ms.openlocfilehash: 39235c5c26cb168dfc995de97f72b80dccb6b818
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720290"
---
# <a name="isymunmanagedwriter3openmethod2-method"></a><span data-ttu-id="3cba4-102">ISymUnmanagedWriter3::OpenMethod2 方法</span><span class="sxs-lookup"><span data-stu-id="3cba4-102">ISymUnmanagedWriter3::OpenMethod2 Method</span></span>

<span data-ttu-id="3cba4-103">打开方法并在图像中提供其实际节偏移量。</span><span class="sxs-lookup"><span data-stu-id="3cba4-103">Opens a method and provides its real section offset in the image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cba4-104">语法</span><span class="sxs-lookup"><span data-stu-id="3cba4-104">Syntax</span></span>  
  
```cpp  
HRESULT OpenMethod2(
    [in] mdMethodDef method,  
    [in] ULONG32 isect,  
    [in] ULONG32 offset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3cba4-105">参数</span><span class="sxs-lookup"><span data-stu-id="3cba4-105">Parameters</span></span>  

 `method`  
 <span data-ttu-id="3cba4-106">中要打开的方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="3cba4-106">[in] The metadata token for the method to be opened.</span></span>  
  
 `isect`  
 <span data-ttu-id="3cba4-107">中图像中的节偏移量。</span><span class="sxs-lookup"><span data-stu-id="3cba4-107">[in] The section offset in the image.</span></span>  
  
 `offset`  
 <span data-ttu-id="3cba4-108">中图像中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="3cba4-108">[in] The offset in the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3cba4-109">返回值</span><span class="sxs-lookup"><span data-stu-id="3cba4-109">Return Value</span></span>  

 <span data-ttu-id="3cba4-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3cba4-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3cba4-111">要求</span><span class="sxs-lookup"><span data-stu-id="3cba4-111">Requirements</span></span>  

 <span data-ttu-id="3cba4-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3cba4-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cba4-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3cba4-113">See also</span></span>

- [<span data-ttu-id="3cba4-114">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="3cba4-114">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)
- [<span data-ttu-id="3cba4-115">OpenMethod 方法</span><span class="sxs-lookup"><span data-stu-id="3cba4-115">OpenMethod Method</span></span>](isymunmanagedwriter-openmethod-method.md)
