---
title: ISymUnmanagedScope 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope
helpviewer_keywords:
- ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 3db7a220-cfe9-4810-8ca8-a094bb8e0f5b
topic_type:
- apiref
ms.openlocfilehash: 9256342ad3a91e6770d6fd19d9d2f94fab267d3e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725880"
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="4aaee-102">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="4aaee-102">ISymUnmanagedScope Interface</span></span>

<span data-ttu-id="4aaee-103">表示方法中的词法范围。</span><span class="sxs-lookup"><span data-stu-id="4aaee-103">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4aaee-104">方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-104">Methods</span></span>  
  
|<span data-ttu-id="4aaee-105">方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-105">Method</span></span>|<span data-ttu-id="4aaee-106">说明</span><span class="sxs-lookup"><span data-stu-id="4aaee-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4aaee-107">GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-107">GetChildren Method</span></span>](isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="4aaee-108">获取此作用域的子级。</span><span class="sxs-lookup"><span data-stu-id="4aaee-108">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="4aaee-109">GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-109">GetEndOffset Method</span></span>](isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="4aaee-110">获取此范围的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="4aaee-110">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="4aaee-111">GetLocalCount 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-111">GetLocalCount Method</span></span>](isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="4aaee-112">获取在此范围内定义的局部变量的计数。</span><span class="sxs-lookup"><span data-stu-id="4aaee-112">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="4aaee-113">GetLocals 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-113">GetLocals Method</span></span>](isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="4aaee-114">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="4aaee-114">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="4aaee-115">GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-115">GetMethod Method</span></span>](isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="4aaee-116">获取包含此范围的方法。</span><span class="sxs-lookup"><span data-stu-id="4aaee-116">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="4aaee-117">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-117">GetNamespaces Method</span></span>](isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="4aaee-118">获取正在此范围内使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="4aaee-118">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="4aaee-119">GetParent 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-119">GetParent Method</span></span>](isymunmanagedscope-getparent-method.md)|<span data-ttu-id="4aaee-120">获取此范围的父范围。</span><span class="sxs-lookup"><span data-stu-id="4aaee-120">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="4aaee-121">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="4aaee-121">GetStartOffset Method</span></span>](isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="4aaee-122">获取此范围的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="4aaee-122">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4aaee-123">要求</span><span class="sxs-lookup"><span data-stu-id="4aaee-123">Requirements</span></span>  

 <span data-ttu-id="4aaee-124">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="4aaee-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4aaee-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4aaee-125">See also</span></span>

- [<span data-ttu-id="4aaee-126">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="4aaee-126">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="4aaee-127">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="4aaee-127">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)
