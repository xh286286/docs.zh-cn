---
title: ISymUnmanagedScope2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2
helpviewer_keywords:
- ISymUnmanagedScope2 interface [.NET Framework debugging]
ms.assetid: 2ed6a387-ba45-483e-9a1e-b0c69f67998b
topic_type:
- apiref
ms.openlocfilehash: 40c437e109eaa4352a83c5566185593cbc6b0eba
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725828"
---
# <a name="isymunmanagedscope2-interface"></a><span data-ttu-id="2c3c7-102">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="2c3c7-102">ISymUnmanagedScope2 Interface</span></span>

<span data-ttu-id="2c3c7-103">表示方法中的词法范围。</span><span class="sxs-lookup"><span data-stu-id="2c3c7-103">Represents a lexical scope within a method.</span></span> <span data-ttu-id="2c3c7-104">此接口扩展了 [ISymUnmanagedScope](isymunmanagedscope-interface.md) 接口，其中包含获取有关范围内定义的常量的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="2c3c7-104">This interface extends the [ISymUnmanagedScope](isymunmanagedscope-interface.md) interface with methods that get information about constants defined within the scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2c3c7-105">方法</span><span class="sxs-lookup"><span data-stu-id="2c3c7-105">Methods</span></span>  
  
|<span data-ttu-id="2c3c7-106">方法</span><span class="sxs-lookup"><span data-stu-id="2c3c7-106">Method</span></span>|<span data-ttu-id="2c3c7-107">说明</span><span class="sxs-lookup"><span data-stu-id="2c3c7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2c3c7-108">GetConstantCount 方法</span><span class="sxs-lookup"><span data-stu-id="2c3c7-108">GetConstantCount Method</span></span>](isymunmanagedscope2-getconstantcount-method.md)|<span data-ttu-id="2c3c7-109">获取在此范围中定义的常量的计数。</span><span class="sxs-lookup"><span data-stu-id="2c3c7-109">Gets a count of the constants defined within this scope.</span></span>|  
|[<span data-ttu-id="2c3c7-110">GetConstants 方法</span><span class="sxs-lookup"><span data-stu-id="2c3c7-110">GetConstants Method</span></span>](isymunmanagedscope2-getconstants-method.md)|<span data-ttu-id="2c3c7-111">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="2c3c7-111">Gets the local constants defined within this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2c3c7-112">要求</span><span class="sxs-lookup"><span data-stu-id="2c3c7-112">Requirements</span></span>  

 <span data-ttu-id="2c3c7-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="2c3c7-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c3c7-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c3c7-114">See also</span></span>

- [<span data-ttu-id="2c3c7-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="2c3c7-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="2c3c7-116">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="2c3c7-116">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
