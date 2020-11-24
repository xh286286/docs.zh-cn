---
title: ISymUnmanagedReader::GetMethodFromDocumentPosition 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodFromDocumentPosition
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodFromDocumentPosition
helpviewer_keywords:
- GetMethodFromDocumentPosition method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodFromDocumentPosition method [.NET Framework debugging]
ms.assetid: 55773dbc-9053-46e3-8a3c-86caa9d91fb4
topic_type:
- apiref
ms.openlocfilehash: 417644e5d0c7af802d5266bd1825efa83c181597
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689597"
---
# <a name="isymunmanagedreadergetmethodfromdocumentposition-method"></a><span data-ttu-id="e4bcc-102">ISymUnmanagedReader::GetMethodFromDocumentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="e4bcc-102">ISymUnmanagedReader::GetMethodFromDocumentPosition Method</span></span>

<span data-ttu-id="e4bcc-103">返回包含文档中给定位置处的断点的方法。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-103">Returns the method that contains the breakpoint at the given position in a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4bcc-104">语法</span><span class="sxs-lookup"><span data-stu-id="e4bcc-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodFromDocumentPosition (  
    [in]  ISymUnmanagedDocument*  document,  
    [in]  ULONG32  line,  
    [in]  ULONG32  column,  
    [out, retval] ISymUnmanagedMethod**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4bcc-105">参数</span><span class="sxs-lookup"><span data-stu-id="e4bcc-105">Parameters</span></span>  

 `document`  
 <span data-ttu-id="e4bcc-106">中指定的文档。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-106">[in] The specified document.</span></span>  
  
 `line`  
 <span data-ttu-id="e4bcc-107">中指定文档的行。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-107">[in] The line of the specified document.</span></span>  
  
 `column`  
 <span data-ttu-id="e4bcc-108">中指定文档的列。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-108">[in] The column of the specified document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="e4bcc-109">弄指向表示包含断点的方法的 [ISymUnmanagedMethod 接口](isymunmanagedmethod-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-109">[out] A pointer to the address of a [ISymUnmanagedMethod Interface](isymunmanagedmethod-interface.md) object that represents the method containing the breakpoint.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4bcc-110">返回值</span><span class="sxs-lookup"><span data-stu-id="e4bcc-110">Return Value</span></span>  

 <span data-ttu-id="e4bcc-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="e4bcc-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4bcc-112">要求</span><span class="sxs-lookup"><span data-stu-id="e4bcc-112">Requirements</span></span>  

 <span data-ttu-id="e4bcc-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="e4bcc-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4bcc-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e4bcc-114">See also</span></span>

- [<span data-ttu-id="e4bcc-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="e4bcc-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
