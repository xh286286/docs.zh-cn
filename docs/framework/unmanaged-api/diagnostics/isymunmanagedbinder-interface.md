---
title: ISymUnmanagedBinder 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder
helpviewer_keywords:
- ISymUnmanagedBinder interface [.NET Framework debugging]
ms.assetid: b22fbe19-b30f-4696-8175-e6b91da9edab
topic_type:
- apiref
ms.openlocfilehash: 554e59484f00626726f7f024c69e93a5e6647130
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727375"
---
# <a name="isymunmanagedbinder-interface"></a><span data-ttu-id="68ca2-102">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="68ca2-102">ISymUnmanagedBinder Interface</span></span>

<span data-ttu-id="68ca2-103">表示非托管代码的符号绑定器。</span><span class="sxs-lookup"><span data-stu-id="68ca2-103">Represents a symbol binder for unmanaged code.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="68ca2-104">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="68ca2-104">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="68ca2-105">方法</span><span class="sxs-lookup"><span data-stu-id="68ca2-105">Methods</span></span>  
  
|<span data-ttu-id="68ca2-106">方法</span><span class="sxs-lookup"><span data-stu-id="68ca2-106">Method</span></span>|<span data-ttu-id="68ca2-107">说明</span><span class="sxs-lookup"><span data-stu-id="68ca2-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="68ca2-108">GetReaderForFile 方法</span><span class="sxs-lookup"><span data-stu-id="68ca2-108">GetReaderForFile Method</span></span>](isymunmanagedbinder-getreaderforfile-method.md)|<span data-ttu-id="68ca2-109">给定元数据接口和文件名后，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将读取与模块关联的调试符号。</span><span class="sxs-lookup"><span data-stu-id="68ca2-109">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols associated with the module.</span></span>|  
|[<span data-ttu-id="68ca2-110">GetReaderFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="68ca2-110">GetReaderFromStream Method</span></span>](isymunmanagedbinder-getreaderfromstream-method.md)|<span data-ttu-id="68ca2-111">给定元数据接口和包含符号存储区的流时，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将从给定的符号存储区中读取调试符号。</span><span class="sxs-lookup"><span data-stu-id="68ca2-111">Given a metadata interface and a stream that contains the symbol store, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols from the given symbol store.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="68ca2-112">要求</span><span class="sxs-lookup"><span data-stu-id="68ca2-112">Requirements</span></span>  

 <span data-ttu-id="68ca2-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="68ca2-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68ca2-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="68ca2-114">See also</span></span>

- [<span data-ttu-id="68ca2-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="68ca2-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="68ca2-116">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="68ca2-116">ISymUnmanagedBinder2 Interface</span></span>](isymunmanagedbinder2-interface.md)
- [<span data-ttu-id="68ca2-117">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="68ca2-117">ISymUnmanagedBinder3 Interface</span></span>](isymunmanagedbinder3-interface.md)
