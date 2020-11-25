---
title: ISymUnmanagedBinder3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3 Interface
helpviewer_keywords:
- ISymUnmanagedBinder3 interface [.NET Framework debugging]
ms.assetid: 37527a84-4b03-4f08-8135-94d898599089
topic_type:
- apiref
ms.openlocfilehash: 0cb0b91f2dca8203c37599400b3b61f84eb7d282
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727310"
---
# <a name="isymunmanagedbinder3-interface"></a><span data-ttu-id="f4f3d-102">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="f4f3d-102">ISymUnmanagedBinder3 Interface</span></span>

<span data-ttu-id="f4f3d-103">扩展符号联编程序接口。</span><span class="sxs-lookup"><span data-stu-id="f4f3d-103">Extends the symbol binder interface.</span></span> <span data-ttu-id="f4f3d-104">通过对实现接口的对象调用来获取此接口 `QueryInterface` `ISymUnmanagedBinder` 。</span><span class="sxs-lookup"><span data-stu-id="f4f3d-104">Obtain this interface by calling `QueryInterface` on an object that implements the `ISymUnmanagedBinder` interface.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="f4f3d-105">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="f4f3d-105">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f4f3d-106">方法</span><span class="sxs-lookup"><span data-stu-id="f4f3d-106">Methods</span></span>  
  
|<span data-ttu-id="f4f3d-107">方法</span><span class="sxs-lookup"><span data-stu-id="f4f3d-107">Method</span></span>|<span data-ttu-id="f4f3d-108">说明</span><span class="sxs-lookup"><span data-stu-id="f4f3d-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f4f3d-109">GetReaderFromCallback 方法</span><span class="sxs-lookup"><span data-stu-id="f4f3d-109">GetReaderFromCallback Method</span></span>](isymunmanagedbinder3-getreaderfromcallback-method.md)|<span data-ttu-id="f4f3d-110">允许用户通过回调来实现或提供， `IID_IDiaReadExeAtRVACallback` `IID_IDiaReadExeAtOffsetCallback` 以从内存中获取调试目录信息</span><span class="sxs-lookup"><span data-stu-id="f4f3d-110">Allows the user to implement or supply via callback either an `IID_IDiaReadExeAtRVACallback` or `IID_IDiaReadExeAtOffsetCallback` to obtain the Debug directory information from memory</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f4f3d-111">要求</span><span class="sxs-lookup"><span data-stu-id="f4f3d-111">Requirements</span></span>  

 <span data-ttu-id="f4f3d-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f4f3d-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4f3d-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4f3d-113">See also</span></span>

- [<span data-ttu-id="f4f3d-114">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="f4f3d-114">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="f4f3d-115">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="f4f3d-115">ISymUnmanagedBinder Interface</span></span>](isymunmanagedbinder-interface.md)
- [<span data-ttu-id="f4f3d-116">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="f4f3d-116">ISymUnmanagedBinder2 Interface</span></span>](isymunmanagedbinder2-interface.md)
