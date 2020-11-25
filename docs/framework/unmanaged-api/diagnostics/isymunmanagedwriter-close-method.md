---
title: ISymUnmanagedWriter::Close 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Close
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Close
helpviewer_keywords:
- Close method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::Close method [.NET Framework debugging]
ms.assetid: 4cce59e1-80b9-4fc4-b3aa-126f1c5876bc
topic_type:
- apiref
ms.openlocfilehash: 1d684c14f14fcc93040798ae4ee3b8bb1df5354d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733251"
---
# <a name="isymunmanagedwriterclose-method"></a><span data-ttu-id="3b54a-102">ISymUnmanagedWriter::Close 方法</span><span class="sxs-lookup"><span data-stu-id="3b54a-102">ISymUnmanagedWriter::Close Method</span></span>

<span data-ttu-id="3b54a-103">将符号提交到符号存储区后关闭符号编写器。</span><span class="sxs-lookup"><span data-stu-id="3b54a-103">Closes the symbol writer after committing the symbols to the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b54a-104">语法</span><span class="sxs-lookup"><span data-stu-id="3b54a-104">Syntax</span></span>  
  
```cpp  
HRESULT Close();  
```  
  
## <a name="return-value"></a><span data-ttu-id="3b54a-105">返回值</span><span class="sxs-lookup"><span data-stu-id="3b54a-105">Return Value</span></span>  

 <span data-ttu-id="3b54a-106">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3b54a-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b54a-107">注解</span><span class="sxs-lookup"><span data-stu-id="3b54a-107">Remarks</span></span>  

 <span data-ttu-id="3b54a-108">在此调用之后，符号编写器将变为无效以便进一步更新。</span><span class="sxs-lookup"><span data-stu-id="3b54a-108">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="3b54a-109">若要在不提交符号的情况下关闭符号编写器，请改用 [ISymUnmanagedWriter：： Abort](isymunmanagedwriter-abort-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3b54a-109">To close the symbol writer without committing the symbols, use the [ISymUnmanagedWriter::Abort](isymunmanagedwriter-abort-method.md) method instead.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b54a-110">要求</span><span class="sxs-lookup"><span data-stu-id="3b54a-110">Requirements</span></span>  

 <span data-ttu-id="3b54a-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3b54a-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b54a-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b54a-112">See also</span></span>

- [<span data-ttu-id="3b54a-113">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="3b54a-113">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
