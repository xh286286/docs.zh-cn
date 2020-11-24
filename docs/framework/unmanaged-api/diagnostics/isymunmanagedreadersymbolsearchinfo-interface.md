---
title: ISymUnmanagedReaderSymbolSearchInfo 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedReaderSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: fde7e21d-1169-4bed-a34d-792e69652bf9
topic_type:
- apiref
ms.openlocfilehash: af4124aed823a0a2475a181efe3fa68e1fae0bfe
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95678384"
---
# <a name="isymunmanagedreadersymbolsearchinfo-interface"></a><span data-ttu-id="5b878-102">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="5b878-102">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>

<span data-ttu-id="5b878-103">提供用于获取符号搜索信息的方法。</span><span class="sxs-lookup"><span data-stu-id="5b878-103">Provides methods that get symbol search information.</span></span> <span data-ttu-id="5b878-104">通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。</span><span class="sxs-lookup"><span data-stu-id="5b878-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5b878-105">方法</span><span class="sxs-lookup"><span data-stu-id="5b878-105">Methods</span></span>  
  
|<span data-ttu-id="5b878-106">方法</span><span class="sxs-lookup"><span data-stu-id="5b878-106">Method</span></span>|<span data-ttu-id="5b878-107">说明</span><span class="sxs-lookup"><span data-stu-id="5b878-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5b878-108">GetSymbolSearchInfo 方法</span><span class="sxs-lookup"><span data-stu-id="5b878-108">GetSymbolSearchInfo Method</span></span>](isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfo-method.md)|<span data-ttu-id="5b878-109">获取符号搜索信息。</span><span class="sxs-lookup"><span data-stu-id="5b878-109">Gets symbol search information.</span></span>|  
|[<span data-ttu-id="5b878-110">GetSymbolSearchInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="5b878-110">GetSymbolSearchInfoCount Method</span></span>](isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfocount-method.md)|<span data-ttu-id="5b878-111">获取符号搜索信息的计数。</span><span class="sxs-lookup"><span data-stu-id="5b878-111">Gets a count of symbol search information.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5b878-112">要求</span><span class="sxs-lookup"><span data-stu-id="5b878-112">Requirements</span></span>  

 <span data-ttu-id="5b878-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="5b878-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b878-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b878-114">See also</span></span>

- [<span data-ttu-id="5b878-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="5b878-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
