---
title: ExportType 方法
ms.date: 03/30/2017
api_name:
- IALink.ExportType
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportType
helpviewer_keywords:
- ExportType method
ms.assetid: 91a7ce63-f5b8-4f16-b2c4-e1d0baa88944
topic_type:
- apiref
ms.openlocfilehash: b8db08b22765bac0ed2fe058db49d6882b8d22df
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684793"
---
# <a name="exporttype-method"></a><span data-ttu-id="dc75a-102">ExportType 方法</span><span class="sxs-lookup"><span data-stu-id="dc75a-102">ExportType Method</span></span>

<span data-ttu-id="dc75a-103">指定类型可导出。</span><span class="sxs-lookup"><span data-stu-id="dc75a-103">Specifies that a type is exportable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc75a-104">语法</span><span class="sxs-lookup"><span data-stu-id="dc75a-104">Syntax</span></span>  
  
```cpp  
HRESULT ExportType(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc75a-105">参数</span><span class="sxs-lookup"><span data-stu-id="dc75a-105">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="dc75a-106">要从中导出的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="dc75a-106">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="dc75a-107">定义可导出类型的文件的文件标记或程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="dc75a-107">File token or assembly ID of file that defines the exportable type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="dc75a-108">要使其可导出的类型的标记。</span><span class="sxs-lookup"><span data-stu-id="dc75a-108">Token of type to be made exportable.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="dc75a-109">要使其可导出的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="dc75a-109">Fully qualified type name to be made exportable.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="dc75a-110">`ComType` 标志，如 `tdPublic` 或 `tdNested` 。</span><span class="sxs-lookup"><span data-stu-id="dc75a-110">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="dc75a-111">此参数可传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="dc75a-111">This parameter may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="dc75a-112">接收导出类型的令牌。</span><span class="sxs-lookup"><span data-stu-id="dc75a-112">Receives token for exported type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dc75a-113">返回值</span><span class="sxs-lookup"><span data-stu-id="dc75a-113">Return Value</span></span>  

 <span data-ttu-id="dc75a-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="dc75a-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc75a-115">要求</span><span class="sxs-lookup"><span data-stu-id="dc75a-115">Requirements</span></span>  

 <span data-ttu-id="dc75a-116">需要 alink</span><span class="sxs-lookup"><span data-stu-id="dc75a-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc75a-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc75a-117">See also</span></span>

- [<span data-ttu-id="dc75a-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="dc75a-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="dc75a-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="dc75a-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="dc75a-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="dc75a-120">ALink API</span></span>](index.md)
