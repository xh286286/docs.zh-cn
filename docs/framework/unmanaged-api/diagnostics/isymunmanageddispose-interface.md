---
title: ISymUnmanagedDispose 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDispose
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDispose
helpviewer_keywords:
- ISymUnmanagedDispose interface [.NET Framework debugging]
ms.assetid: b1d74e83-a200-4d00-8fbd-27918808616d
topic_type:
- apiref
ms.openlocfilehash: 932e76e73d5d40b36abcb17d8a53e6745927d873
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719601"
---
# <a name="isymunmanageddispose-interface"></a><span data-ttu-id="146fa-102">ISymUnmanagedDispose 接口</span><span class="sxs-lookup"><span data-stu-id="146fa-102">ISymUnmanagedDispose Interface</span></span>

<span data-ttu-id="146fa-103">释放非托管资源。</span><span class="sxs-lookup"><span data-stu-id="146fa-103">Disposes of unmanaged resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="146fa-104">方法</span><span class="sxs-lookup"><span data-stu-id="146fa-104">Methods</span></span>  
  
|<span data-ttu-id="146fa-105">方法</span><span class="sxs-lookup"><span data-stu-id="146fa-105">Method</span></span>|<span data-ttu-id="146fa-106">说明</span><span class="sxs-lookup"><span data-stu-id="146fa-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="146fa-107">Destroy 方法</span><span class="sxs-lookup"><span data-stu-id="146fa-107">Destroy Method</span></span>](isymunmanageddispose-destroy-method.md)|<span data-ttu-id="146fa-108">使基础对象释放所有内部引用，并在所有后续方法调用中返回失败。</span><span class="sxs-lookup"><span data-stu-id="146fa-108">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="146fa-109">要求</span><span class="sxs-lookup"><span data-stu-id="146fa-109">Requirements</span></span>  

 <span data-ttu-id="146fa-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="146fa-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="146fa-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="146fa-111">See also</span></span>

- [<span data-ttu-id="146fa-112">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="146fa-112">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
