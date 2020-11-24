---
title: ISymUnmanagedWriter::SetMethodSourceRange 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetMethodSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetMethodSourceRange
helpviewer_keywords:
- SetMethodSourceRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetMethodSourceRange method [.NET Framework debugging]
ms.assetid: c698b86e-ace7-4b21-9549-f52d6a034959
topic_type:
- apiref
ms.openlocfilehash: a918b5c2334683348adc6a7382527faedb52d7b6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683532"
---
# <a name="isymunmanagedwritersetmethodsourcerange-method"></a><span data-ttu-id="46235-102">ISymUnmanagedWriter::SetMethodSourceRange 方法</span><span class="sxs-lookup"><span data-stu-id="46235-102">ISymUnmanagedWriter::SetMethodSourceRange Method</span></span>

<span data-ttu-id="46235-103">指定源文件内方法的真正开始和结尾。</span><span class="sxs-lookup"><span data-stu-id="46235-103">Specifies the true start and end of a method within a source file.</span></span> <span data-ttu-id="46235-104">使用此方法可以独立于方法中存在的序列点来指定方法的范围。</span><span class="sxs-lookup"><span data-stu-id="46235-104">Use this method to specify the extent of a method independently of the sequence points that exist within the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46235-105">语法</span><span class="sxs-lookup"><span data-stu-id="46235-105">Syntax</span></span>  
  
```cpp  
HRESULT SetMethodSourceRange(  
    [in] ISymUnmanagedDocumentWriter  *startDoc,  
    [in] ULONG32                      startLine,  
    [in] ULONG32                      startColumn,  
    [in] ISymUnmanagedDocumentWriter  *endDoc,  
    [in] ULONG32                      endLine,  
    [in] ULONG32                      endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="46235-106">参数</span><span class="sxs-lookup"><span data-stu-id="46235-106">Parameters</span></span>  

 `startDoc`  
 <span data-ttu-id="46235-107">中指向包含起始位置的文档的指针。</span><span class="sxs-lookup"><span data-stu-id="46235-107">[in] A pointer to the document containing the starting position.</span></span>  
  
 `startLine`  
 <span data-ttu-id="46235-108">中起始行号。</span><span class="sxs-lookup"><span data-stu-id="46235-108">[in] The starting line number.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="46235-109">中起始列。</span><span class="sxs-lookup"><span data-stu-id="46235-109">[in] The starting column.</span></span>  
  
 `endDoc`  
 <span data-ttu-id="46235-110">中指向包含结束位置的文档的指针。</span><span class="sxs-lookup"><span data-stu-id="46235-110">[in] A pointer to the document containing the ending position.</span></span>  
  
 `endLine`  
 <span data-ttu-id="46235-111">中结束行号。</span><span class="sxs-lookup"><span data-stu-id="46235-111">[in] The ending line number.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="46235-112">中结束列号。</span><span class="sxs-lookup"><span data-stu-id="46235-112">[in] The ending column number.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="46235-113">返回值</span><span class="sxs-lookup"><span data-stu-id="46235-113">Return Value</span></span>  

 <span data-ttu-id="46235-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="46235-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46235-115">要求</span><span class="sxs-lookup"><span data-stu-id="46235-115">Requirements</span></span>  

 <span data-ttu-id="46235-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="46235-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46235-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46235-117">See also</span></span>

- [<span data-ttu-id="46235-118">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="46235-118">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
