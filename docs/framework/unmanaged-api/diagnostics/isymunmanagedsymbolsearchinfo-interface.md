---
title: ISymUnmanagedSymbolSearchInfo 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: 30817373-0a21-49c1-a0c4-8e8daeecb8db
topic_type:
- apiref
ms.openlocfilehash: 95ad3cbea4269173f22e662d15772ff97f7ee900
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705444"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="ebe80-102">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="ebe80-102">ISymUnmanagedSymbolSearchInfo Interface</span></span>

<span data-ttu-id="ebe80-103">提供获取有关搜索路径的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="ebe80-103">Provides methods that get information about the search path.</span></span> <span data-ttu-id="ebe80-104">通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。</span><span class="sxs-lookup"><span data-stu-id="ebe80-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ebe80-105">方法</span><span class="sxs-lookup"><span data-stu-id="ebe80-105">Methods</span></span>  
  
|<span data-ttu-id="ebe80-106">方法</span><span class="sxs-lookup"><span data-stu-id="ebe80-106">Method</span></span>|<span data-ttu-id="ebe80-107">说明</span><span class="sxs-lookup"><span data-stu-id="ebe80-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ebe80-108">GetHRESULT 方法</span><span class="sxs-lookup"><span data-stu-id="ebe80-108">GetHRESULT Method</span></span>](isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="ebe80-109">获取 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="ebe80-109">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="ebe80-110">GetSearchPath 方法</span><span class="sxs-lookup"><span data-stu-id="ebe80-110">GetSearchPath Method</span></span>](isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="ebe80-111">获取搜索路径。</span><span class="sxs-lookup"><span data-stu-id="ebe80-111">Gets the search path.</span></span>|  
|[<span data-ttu-id="ebe80-112">GetSearchPathLength 方法</span><span class="sxs-lookup"><span data-stu-id="ebe80-112">GetSearchPathLength Method</span></span>](isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="ebe80-113">获取搜索路径长度。</span><span class="sxs-lookup"><span data-stu-id="ebe80-113">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ebe80-114">要求</span><span class="sxs-lookup"><span data-stu-id="ebe80-114">Requirements</span></span>  

 <span data-ttu-id="ebe80-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ebe80-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebe80-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ebe80-116">See also</span></span>

- [<span data-ttu-id="ebe80-117">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="ebe80-117">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
