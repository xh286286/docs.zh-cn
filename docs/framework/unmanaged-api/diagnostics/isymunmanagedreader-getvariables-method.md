---
title: ISymUnmanagedReader::GetVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetVariables
helpviewer_keywords:
- ISymUnmanagedReader::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 16dc49cb-2c60-4ac8-9c35-020e9afba3f8
topic_type:
- apiref
ms.openlocfilehash: c4341a5ffe557694473ae505590b57d39a27a721
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675888"
---
# <a name="isymunmanagedreadergetvariables-method"></a><span data-ttu-id="a6610-102">ISymUnmanagedReader::GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="a6610-102">ISymUnmanagedReader::GetVariables Method</span></span>

<span data-ttu-id="a6610-103">在给定父和名称的情况下，返回非局部变量。</span><span class="sxs-lookup"><span data-stu-id="a6610-103">Returns a non-local variable, given its parent and name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6610-104">语法</span><span class="sxs-lookup"><span data-stu-id="a6610-104">Syntax</span></span>  
  
```cpp  
HRESULT GetVariables (  
    [in]  mdToken  parent,  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is (cVars),  
        length_is (*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a6610-105">参数</span><span class="sxs-lookup"><span data-stu-id="a6610-105">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="a6610-106">中变量的父级。</span><span class="sxs-lookup"><span data-stu-id="a6610-106">[in] The parent of the variable.</span></span>  
  
 `cVars`  
 <span data-ttu-id="a6610-107">[in] `pVars` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="a6610-107">[in] The size of the `pVars` array.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="a6610-108">弄指向一个变量的指针，该变量接收返回的变量数 `pVars` 。</span><span class="sxs-lookup"><span data-stu-id="a6610-108">[out] A pointer to the variable that receives the number of variables returned in `pVars`.</span></span>  
  
 `pVars`  
 <span data-ttu-id="a6610-109">弄指向接收变量的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="a6610-109">[out] A pointer to the variable that receives the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a6610-110">返回值</span><span class="sxs-lookup"><span data-stu-id="a6610-110">Return Value</span></span>  

 <span data-ttu-id="a6610-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a6610-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6610-112">要求</span><span class="sxs-lookup"><span data-stu-id="a6610-112">Requirements</span></span>  

 <span data-ttu-id="a6610-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a6610-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6610-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6610-114">See also</span></span>

- [<span data-ttu-id="a6610-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="a6610-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
