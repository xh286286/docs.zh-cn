---
title: ISymUnmanagedScope::GetStartOffset 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetStartOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetStartOffset
helpviewer_keywords:
- GetStartOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetStartOffset method [.NET Framework debugging]
ms.assetid: da6bbc75-94d1-4354-9722-0d455b4428fb
topic_type:
- apiref
ms.openlocfilehash: 69b72ce66a203f403fcfe0fd4b4e728ece7397e4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725867"
---
# <a name="isymunmanagedscopegetstartoffset-method"></a><span data-ttu-id="f302e-102">ISymUnmanagedScope::GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="f302e-102">ISymUnmanagedScope::GetStartOffset Method</span></span>

<span data-ttu-id="f302e-103">获取此范围的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="f302e-103">Gets the start offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f302e-104">语法</span><span class="sxs-lookup"><span data-stu-id="f302e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetStartOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f302e-105">参数</span><span class="sxs-lookup"><span data-stu-id="f302e-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="f302e-106">弄指向的指针 `ULONG32` ，该指针包含起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="f302e-106">[out] A pointer to a `ULONG32` that contains the starting offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f302e-107">返回值</span><span class="sxs-lookup"><span data-stu-id="f302e-107">Return Value</span></span>  

 <span data-ttu-id="f302e-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f302e-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f302e-109">要求</span><span class="sxs-lookup"><span data-stu-id="f302e-109">Requirements</span></span>  

 <span data-ttu-id="f302e-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f302e-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f302e-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f302e-111">See also</span></span>

- [<span data-ttu-id="f302e-112">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="f302e-112">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="f302e-113">GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="f302e-113">GetEndOffset Method</span></span>](isymunmanagedscope-getendoffset-method.md)
