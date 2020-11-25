---
title: ISymUnmanagedReader::GetGlobalVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetGlobalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetGlobalVariables
helpviewer_keywords:
- GetGlobalVariables method [.NET Framework debugging]
- ISymUnmanagedReader::GetGlobalVariables method [.NET Framework debugging]
ms.assetid: a2dd5098-3e58-4be5-b7a2-e4160b3b505a
topic_type:
- apiref
ms.openlocfilehash: 299787ea4eb8a5c25bdab64ad08445839c9f24d6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707537"
---
# <a name="isymunmanagedreadergetglobalvariables-method"></a><span data-ttu-id="6df2d-102">ISymUnmanagedReader::GetGlobalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="6df2d-102">ISymUnmanagedReader::GetGlobalVariables Method</span></span>

<span data-ttu-id="6df2d-103">返回所有全局变量。</span><span class="sxs-lookup"><span data-stu-id="6df2d-103">Returns all global variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6df2d-104">语法</span><span class="sxs-lookup"><span data-stu-id="6df2d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetGlobalVariables(  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is(cVars),  
        length_is(*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6df2d-105">参数</span><span class="sxs-lookup"><span data-stu-id="6df2d-105">Parameters</span></span>  

 `cVars`  
 <span data-ttu-id="6df2d-106">中所指向的缓冲区的长度 `pcVars` 。</span><span class="sxs-lookup"><span data-stu-id="6df2d-106">[in] The length of the buffer pointed to by `pcVars`.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="6df2d-107">弄指向的指针 `ULONG32` ，该指针接收包含变量所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="6df2d-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the variables.</span></span>  
  
 `pVars`  
 <span data-ttu-id="6df2d-108">弄包含变量的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="6df2d-108">[out] A buffer that contains the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6df2d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="6df2d-109">Return Value</span></span>  

 <span data-ttu-id="6df2d-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="6df2d-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6df2d-111">要求</span><span class="sxs-lookup"><span data-stu-id="6df2d-111">Requirements</span></span>  

 <span data-ttu-id="6df2d-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="6df2d-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6df2d-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6df2d-113">See also</span></span>

- [<span data-ttu-id="6df2d-114">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="6df2d-114">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
