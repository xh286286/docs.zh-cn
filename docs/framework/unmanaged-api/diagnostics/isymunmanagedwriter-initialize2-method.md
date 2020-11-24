---
title: ISymUnmanagedWriter::Initialize2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Initialize2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Initialize2
helpviewer_keywords:
- ISymUnmanagedWriter::Initialize2 method [.NET Framework debugging]
- Initialize2 method [.NET Framework debugging]
ms.assetid: 93de56b6-4ae8-4cca-acdc-25a434623509
topic_type:
- apiref
ms.openlocfilehash: 93a96a5da3342f4beff611de1d448dc199dd39dd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687125"
---
# <a name="isymunmanagedwriterinitialize2-method"></a><span data-ttu-id="d908d-102">ISymUnmanagedWriter::Initialize2 方法</span><span class="sxs-lookup"><span data-stu-id="d908d-102">ISymUnmanagedWriter::Initialize2 Method</span></span>

<span data-ttu-id="d908d-103">设置此编写器将与之关联的元数据发射器接口，并设置调试符号将写入的输出文件名。</span><span class="sxs-lookup"><span data-stu-id="d908d-103">Sets the metadata emitter interface with which this writer will be associated, and sets the output file name to which the debugging symbols will be written.</span></span> <span data-ttu-id="d908d-104">此方法还允许您设置程序数据库 (PDB) 文件的最终位置。</span><span class="sxs-lookup"><span data-stu-id="d908d-104">This method also lets you set the final location of the program database (PDB) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d908d-105">语法</span><span class="sxs-lookup"><span data-stu-id="d908d-105">Syntax</span></span>  
  
```cpp  
HRESULT Initialize2(  
    [in] IUnknown     *emitter,  
    [in] const WCHAR  *tempfilename,  
    [in] IStream      *pIStream,  
    [in] BOOL         fFullBuild,  
    [in] const WCHAR  *finalfilename);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d908d-106">参数</span><span class="sxs-lookup"><span data-stu-id="d908d-106">Parameters</span></span>  

 `emitter`  
 <span data-ttu-id="d908d-107">中指向元数据发射器接口的指针。</span><span class="sxs-lookup"><span data-stu-id="d908d-107">[in] A pointer to the metadata emitter interface.</span></span>  
  
 `tempfilename`  
 <span data-ttu-id="d908d-108">中指向的指针 `WCHAR` ，该指针包含向其中写入调试符号的文件名。</span><span class="sxs-lookup"><span data-stu-id="d908d-108">[in] A pointer to a `WCHAR` that contains the file name to which the debugging symbols are written.</span></span> <span data-ttu-id="d908d-109">如果为不使用文件名的编写器指定文件名，则忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="d908d-109">If a file name is specified for a writer that does not use file names, this parameter is ignored.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="d908d-110">中如果已指定，则符号编写器会将符号发送到给定的 <xref:System.Runtime.InteropServices.ComTypes.IStream> （而不是参数中指定的文件） `filename` 。</span><span class="sxs-lookup"><span data-stu-id="d908d-110">[in] If specified, the symbol writer emits the symbols into the given <xref:System.Runtime.InteropServices.ComTypes.IStream> rather than to the file specified in the `filename` parameter.</span></span> <span data-ttu-id="d908d-111">`pIStream` 参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="d908d-111">The `pIStream` parameter is optional.</span></span>  
  
 `fFullBuild`  
 <span data-ttu-id="d908d-112">[in] `true` 如果这是完全重新生成，则为; `false` 如果这是增量编译，则为。</span><span class="sxs-lookup"><span data-stu-id="d908d-112">[in] `true` if this is a full rebuild; `false` if this is an incremental compilation.</span></span>  
  
 `finalfilename`  
 <span data-ttu-id="d908d-113">中指向的指针 `WCHAR` ，它是 PDB 文件的最终位置的路径字符串。</span><span class="sxs-lookup"><span data-stu-id="d908d-113">[in] A pointer to a `WCHAR` that is the path string to the final location of the PDB file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d908d-114">返回值</span><span class="sxs-lookup"><span data-stu-id="d908d-114">Return Value</span></span>  

 <span data-ttu-id="d908d-115">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d908d-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d908d-116">要求</span><span class="sxs-lookup"><span data-stu-id="d908d-116">Requirements</span></span>  

 <span data-ttu-id="d908d-117">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d908d-117">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d908d-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d908d-118">See also</span></span>

- [<span data-ttu-id="d908d-119">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="d908d-119">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="d908d-120">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="d908d-120">Initialize Method</span></span>](isymunmanagedwriter-initialize-method.md)
