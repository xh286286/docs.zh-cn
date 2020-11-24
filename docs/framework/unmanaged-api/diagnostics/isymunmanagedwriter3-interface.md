---
title: ISymUnmanagedWriter3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3
helpviewer_keywords:
- ISymUnmanagedWriter3 interface [.NET Framework debugging]
ms.assetid: a034c21e-e371-4360-b470-29e88288948f
topic_type:
- apiref
ms.openlocfilehash: dfc2e39a6a39e7386bd7358d422d5c6978ec42ec
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683285"
---
# <a name="isymunmanagedwriter3-interface"></a><span data-ttu-id="62f4e-102">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="62f4e-102">ISymUnmanagedWriter3 Interface</span></span>

<span data-ttu-id="62f4e-103">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="62f4e-103">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="62f4e-104">此接口扩展 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="62f4e-104">This interface extends the [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="62f4e-105">方法</span><span class="sxs-lookup"><span data-stu-id="62f4e-105">Methods</span></span>  
  
|<span data-ttu-id="62f4e-106">方法</span><span class="sxs-lookup"><span data-stu-id="62f4e-106">Method</span></span>|<span data-ttu-id="62f4e-107">说明</span><span class="sxs-lookup"><span data-stu-id="62f4e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="62f4e-108">Commit 方法</span><span class="sxs-lookup"><span data-stu-id="62f4e-108">Commit Method</span></span>](isymunmanagedwriter3-commit-method.md)|<span data-ttu-id="62f4e-109">将迄今为止写入的更改提交到流。</span><span class="sxs-lookup"><span data-stu-id="62f4e-109">Commits the changes written so far to the stream.</span></span>|  
|[<span data-ttu-id="62f4e-110">OpenMethod2 方法</span><span class="sxs-lookup"><span data-stu-id="62f4e-110">OpenMethod2 Method</span></span>](isymunmanagedwriter3-openmethod2-method.md)|<span data-ttu-id="62f4e-111">打开方法并在图像中提供其实际节偏移量。</span><span class="sxs-lookup"><span data-stu-id="62f4e-111">Opens a method and provides its real section offset in the image.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="62f4e-112">要求</span><span class="sxs-lookup"><span data-stu-id="62f4e-112">Requirements</span></span>  

 <span data-ttu-id="62f4e-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="62f4e-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62f4e-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62f4e-114">See also</span></span>

- [<span data-ttu-id="62f4e-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="62f4e-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="62f4e-116">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="62f4e-116">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="62f4e-117">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="62f4e-117">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
