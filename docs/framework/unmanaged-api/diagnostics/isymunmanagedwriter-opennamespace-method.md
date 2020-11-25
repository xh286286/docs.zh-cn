---
title: ISymUnmanagedWriter::OpenNamespace 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenNamespace
helpviewer_keywords:
- ISymUnmanagedWriter::OpenNamespace method [.NET Framework debugging]
- OpenNamespace method [.NET Framework debugging]
ms.assetid: 426f4e4f-e60d-4ad1-b546-a10e3c55c283
topic_type:
- apiref
ms.openlocfilehash: 2f64f9f4bde3119f9f089becec5a36d69ed43596
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730056"
---
# <a name="isymunmanagedwriteropennamespace-method"></a><span data-ttu-id="adaba-102">ISymUnmanagedWriter::OpenNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="adaba-102">ISymUnmanagedWriter::OpenNamespace Method</span></span>

<span data-ttu-id="adaba-103">打开一个新的命名空间。</span><span class="sxs-lookup"><span data-stu-id="adaba-103">Opens a new namespace.</span></span> <span data-ttu-id="adaba-104">在定义占用命名空间的方法或变量之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="adaba-104">Call this method before defining methods or variables that occupy a namespace.</span></span> <span data-ttu-id="adaba-105">命名空间可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="adaba-105">Namespaces can be nested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adaba-106">语法</span><span class="sxs-lookup"><span data-stu-id="adaba-106">Syntax</span></span>  
  
```cpp  
HRESULT OpenNamespace(  
    [in] const WCHAR *name);  
```  
  
## <a name="parameters"></a><span data-ttu-id="adaba-107">参数</span><span class="sxs-lookup"><span data-stu-id="adaba-107">Parameters</span></span>  

 `name`  
 <span data-ttu-id="adaba-108">中指向新命名空间的名称的指针。</span><span class="sxs-lookup"><span data-stu-id="adaba-108">[in] A pointer to the name of the new namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="adaba-109">返回值</span><span class="sxs-lookup"><span data-stu-id="adaba-109">Return Value</span></span>  

 <span data-ttu-id="adaba-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="adaba-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="adaba-111">要求</span><span class="sxs-lookup"><span data-stu-id="adaba-111">Requirements</span></span>  

 <span data-ttu-id="adaba-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="adaba-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="adaba-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="adaba-113">See also</span></span>

- [<span data-ttu-id="adaba-114">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="adaba-114">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="adaba-115">CloseNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="adaba-115">CloseNamespace Method</span></span>](isymunmanagedwriter-closenamespace-method.md)
