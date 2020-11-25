---
title: ImportFile 方法
ms.date: 03/30/2017
api_name:
- IALink.ImportFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile
helpviewer_keywords:
- ImportFile method
ms.assetid: bcbe321f-b83a-4e9a-9f10-8d913e244dc9
topic_type:
- apiref
ms.openlocfilehash: f30307884a268008fd4d1a8de31ec5a49b6ab92d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705236"
---
# <a name="importfile-method"></a><span data-ttu-id="6dd81-102">ImportFile 方法</span><span class="sxs-lookup"><span data-stu-id="6dd81-102">ImportFile Method</span></span>

<span data-ttu-id="6dd81-103">导入程序集和未绑定模块。</span><span class="sxs-lookup"><span data-stu-id="6dd81-103">Imports assemblies and unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6dd81-104">语法</span><span class="sxs-lookup"><span data-stu-id="6dd81-104">Syntax</span></span>  
  
```cpp  
HRESULT ImportFile(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="6dd81-105">参数</span><span class="sxs-lookup"><span data-stu-id="6dd81-105">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="6dd81-106">要导入的文件的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="6dd81-106">Fully qualified name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="6dd81-107">可选输出文件名，可用于在文件链接到程序集时对其进行重命名。</span><span class="sxs-lookup"><span data-stu-id="6dd81-107">Optional output file name that can be used to rename the file as it is linked into the assembly.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="6dd81-108">如果为 TRUE，则使用 ImportTypes，否则必须手动执行导入。</span><span class="sxs-lookup"><span data-stu-id="6dd81-108">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="6dd81-109">指向将存储唯一文件 ID 的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="6dd81-109">Pointer to token where a unique file ID will be stored.</span></span> <span data-ttu-id="6dd81-110">该文件可以是程序集或文件。</span><span class="sxs-lookup"><span data-stu-id="6dd81-110">The file can be an assembly or a file.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="6dd81-111">接收指向 [IMetaDataAssemblyImport 接口](../metadata/imetadataassemblyimport-interface.md)的指针。</span><span class="sxs-lookup"><span data-stu-id="6dd81-111">Receives pointer to [IMetaDataAssemblyImport Interface](../metadata/imetadataassemblyimport-interface.md).</span></span> <span data-ttu-id="6dd81-112">如果文件不是程序集，则可以为 NULL。</span><span class="sxs-lookup"><span data-stu-id="6dd81-112">Can be NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="6dd81-113">一个指针，指向已导入的文件和/或范围的计数。</span><span class="sxs-lookup"><span data-stu-id="6dd81-113">Pointer to the count of files and/or scopes that have been imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6dd81-114">返回值</span><span class="sxs-lookup"><span data-stu-id="6dd81-114">Return Value</span></span>  

 <span data-ttu-id="6dd81-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="6dd81-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6dd81-116">要求</span><span class="sxs-lookup"><span data-stu-id="6dd81-116">Requirements</span></span>  

 <span data-ttu-id="6dd81-117">需要 alink</span><span class="sxs-lookup"><span data-stu-id="6dd81-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dd81-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6dd81-118">See also</span></span>

- [<span data-ttu-id="6dd81-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="6dd81-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="6dd81-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="6dd81-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="6dd81-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="6dd81-121">ALink API</span></span>](index.md)
