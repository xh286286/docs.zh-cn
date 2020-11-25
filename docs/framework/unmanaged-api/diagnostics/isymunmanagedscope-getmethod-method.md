---
title: ISymUnmanagedScope::GetMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetMethod method [.NET Framework debugging]
ms.assetid: a61866ee-221a-45b9-a1b7-395825b77872
topic_type:
- apiref
ms.openlocfilehash: 75d5638a6f01ba9569a03e5255a7217371c9d177
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725932"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="8a26d-102">ISymUnmanagedScope::GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="8a26d-102">ISymUnmanagedScope::GetMethod Method</span></span>

<span data-ttu-id="8a26d-103">获取包含此范围的方法。</span><span class="sxs-lookup"><span data-stu-id="8a26d-103">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a26d-104">语法</span><span class="sxs-lookup"><span data-stu-id="8a26d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a26d-105">参数</span><span class="sxs-lookup"><span data-stu-id="8a26d-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="8a26d-106">弄指向返回的 [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="8a26d-106">[out] A pointer to the returned [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8a26d-107">返回值</span><span class="sxs-lookup"><span data-stu-id="8a26d-107">Return Value</span></span>  

 <span data-ttu-id="8a26d-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="8a26d-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a26d-109">要求</span><span class="sxs-lookup"><span data-stu-id="8a26d-109">Requirements</span></span>  

 <span data-ttu-id="8a26d-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="8a26d-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a26d-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a26d-111">See also</span></span>

- [<span data-ttu-id="8a26d-112">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="8a26d-112">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
