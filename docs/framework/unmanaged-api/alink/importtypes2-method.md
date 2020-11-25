---
title: ImportTypes2 方法
ms.date: 03/30/2017
api_name:
- IALink2.ImportTypes2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes2
helpviewer_keywords:
- ImportTypes2 method
ms.assetid: 32f3ba58-9695-41e9-ba58-fd19e45ed396
topic_type:
- apiref
ms.openlocfilehash: 2ec7708edd86b9f2656d0eee434992c3b73200ca
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705041"
---
# <a name="importtypes2-method"></a><span data-ttu-id="4bfea-102">ImportTypes2 方法</span><span class="sxs-lookup"><span data-stu-id="4bfea-102">ImportTypes2 Method</span></span>

<span data-ttu-id="4bfea-103">启动类型的导入。</span><span class="sxs-lookup"><span data-stu-id="4bfea-103">Initiates the import of types.</span></span> <span data-ttu-id="4bfea-104">调用此方法以开始从通过 [ImportFile 方法](importfile-method.md)导入的每个范围导入类型。</span><span class="sxs-lookup"><span data-stu-id="4bfea-104">Call this method to begin importing types from each scope imported via [ImportFile Method](importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bfea-105">语法</span><span class="sxs-lookup"><span data-stu-id="4bfea-105">Syntax</span></span>  
  
```cpp  
HRESULT ImportTypes2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport2** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="4bfea-106">参数</span><span class="sxs-lookup"><span data-stu-id="4bfea-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="4bfea-107">要导入的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="4bfea-107">ID of assembly into which to import.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="4bfea-108">要从其导入的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="4bfea-108">ID of file to from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="4bfea-109">要从中导入的从零开始的作用域。</span><span class="sxs-lookup"><span data-stu-id="4bfea-109">Zero-based scope from which to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="4bfea-110">接收给定范围内的类型的枚举器句柄。</span><span class="sxs-lookup"><span data-stu-id="4bfea-110">Receives enumerator handle for the types in the given scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="4bfea-111">可以选择接收 [IMetaDataImport2 接口](../metadata/imetadataimport2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="4bfea-111">Optionally receives [IMetaDataImport2 Interface](../metadata/imetadataimport2-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="4bfea-112">可以选择接收指定范围内的类型的计数。</span><span class="sxs-lookup"><span data-stu-id="4bfea-112">Optionally receives count of types in the specified scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4bfea-113">返回值</span><span class="sxs-lookup"><span data-stu-id="4bfea-113">Return Value</span></span>  

 <span data-ttu-id="4bfea-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="4bfea-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bfea-115">要求</span><span class="sxs-lookup"><span data-stu-id="4bfea-115">Requirements</span></span>  

 <span data-ttu-id="4bfea-116">需要 alink</span><span class="sxs-lookup"><span data-stu-id="4bfea-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bfea-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4bfea-117">See also</span></span>

- [<span data-ttu-id="4bfea-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="4bfea-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="4bfea-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="4bfea-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="4bfea-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="4bfea-120">ALink API</span></span>](index.md)
