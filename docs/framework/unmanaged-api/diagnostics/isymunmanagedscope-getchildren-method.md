---
title: ISymUnmanagedScope::GetChildren 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetChildren
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetChildren
helpviewer_keywords:
- ISymUnmanagedScope::GetChildren method [.NET Framework debugging]
- GetChildren method [.NET Framework debugging]
ms.assetid: 0bed524e-cc48-4bf0-b9fa-25d665e63ddb
topic_type:
- apiref
ms.openlocfilehash: 8f3c83a7a89553ba600f3e0e368eec0ddd0350e9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727603"
---
# <a name="isymunmanagedscopegetchildren-method"></a><span data-ttu-id="61c65-102">ISymUnmanagedScope::GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="61c65-102">ISymUnmanagedScope::GetChildren Method</span></span>

<span data-ttu-id="61c65-103">获取此作用域的子级。</span><span class="sxs-lookup"><span data-stu-id="61c65-103">Gets the children of this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61c65-104">语法</span><span class="sxs-lookup"><span data-stu-id="61c65-104">Syntax</span></span>  
  
```cpp  
HRESULT GetChildren(  
    [in]  ULONG32  cChildren,  
    [out] ULONG32  *pcChildren,  
    [out, size_is(cChildren),  
        length_is(*pcChildren)] ISymUnmanagedScope* children[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61c65-105">参数</span><span class="sxs-lookup"><span data-stu-id="61c65-105">Parameters</span></span>  

 `cChildren`  
 <span data-ttu-id="61c65-106">中 `ULONG32` 指示数组大小的 `children` 。</span><span class="sxs-lookup"><span data-stu-id="61c65-106">[in] A `ULONG32` that indicates the size of the `children` array.</span></span>  
  
 `pcChildren`  
 <span data-ttu-id="61c65-107">弄指向的指针 `ULONG32` ，该指针接收包含子级所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="61c65-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the children.</span></span>  
  
 `children`  
 <span data-ttu-id="61c65-108">弄返回的子元素数组。</span><span class="sxs-lookup"><span data-stu-id="61c65-108">[out] The returned array of children.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="61c65-109">返回值</span><span class="sxs-lookup"><span data-stu-id="61c65-109">Return Value</span></span>  

 <span data-ttu-id="61c65-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="61c65-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61c65-111">要求</span><span class="sxs-lookup"><span data-stu-id="61c65-111">Requirements</span></span>  

 <span data-ttu-id="61c65-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="61c65-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61c65-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61c65-113">See also</span></span>

- [<span data-ttu-id="61c65-114">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="61c65-114">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="61c65-115">GetParent 方法</span><span class="sxs-lookup"><span data-stu-id="61c65-115">GetParent Method</span></span>](isymunmanagedscope-getparent-method.md)
