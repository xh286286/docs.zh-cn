---
title: ISymUnmanagedMethod::GetRootScope 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetRootScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetRootScope
helpviewer_keywords:
- ISymUnmanagedMethod::GetRootScope method [.NET Framework debugging]
- GetRootScope method [.NET Framework debugging]
ms.assetid: 7d58caac-2e75-4dfa-9249-32d8a624b247
topic_type:
- apiref
ms.openlocfilehash: 071738c8fb9b40457215e21172240aa7e77198cd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95699464"
---
# <a name="isymunmanagedmethodgetrootscope-method"></a><span data-ttu-id="c4ef1-102">ISymUnmanagedMethod::GetRootScope 方法</span><span class="sxs-lookup"><span data-stu-id="c4ef1-102">ISymUnmanagedMethod::GetRootScope Method</span></span>

<span data-ttu-id="c4ef1-103">获取此方法内的根词法范围。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-103">Gets the root lexical scope within this method.</span></span> <span data-ttu-id="c4ef1-104">此范围包括整个方法。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-104">This scope encloses the entire method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4ef1-105">语法</span><span class="sxs-lookup"><span data-stu-id="c4ef1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRootScope(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4ef1-106">参数</span><span class="sxs-lookup"><span data-stu-id="c4ef1-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="c4ef1-107">弄设置为返回的 [ISymUnmanagedScope](isymunmanagedscope-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-107">[out] A pointer that is set to the returned [ISymUnmanagedScope](isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c4ef1-108">返回值</span><span class="sxs-lookup"><span data-stu-id="c4ef1-108">Return Value</span></span>  

 <span data-ttu-id="c4ef1-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4ef1-110">要求</span><span class="sxs-lookup"><span data-stu-id="c4ef1-110">Requirements</span></span>  

 <span data-ttu-id="c4ef1-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c4ef1-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4ef1-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4ef1-112">See also</span></span>

- [<span data-ttu-id="c4ef1-113">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="c4ef1-113">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
