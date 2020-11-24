---
title: EmbedResource 方法
ms.date: 03/30/2017
api_name:
- IALink.EmbedResource
- EmbedResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmbedResource
helpviewer_keywords:
- EmbedResource method
ms.assetid: 667bd954-6dc6-4020-a3cb-0e8224179993
topic_type:
- apiref
ms.openlocfilehash: 34439b7c01dee7d7789d989b58e8944c6282b71b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95676382"
---
# <a name="embedresource-method"></a><span data-ttu-id="04564-102">EmbedResource 方法</span><span class="sxs-lookup"><span data-stu-id="04564-102">EmbedResource Method</span></span>

<span data-ttu-id="04564-103">声明嵌入的资源。</span><span class="sxs-lookup"><span data-stu-id="04564-103">Declares an embedded resource.</span></span> <span data-ttu-id="04564-104">此方法并不实际嵌入资源。</span><span class="sxs-lookup"><span data-stu-id="04564-104">This method does not actually embed the resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04564-105">语法</span><span class="sxs-lookup"><span data-stu-id="04564-105">Syntax</span></span>  
  
```cpp  
HRESULT EmbedResource(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    LPCWSTR     pszResourceName,  
    DWORD       dwOffset,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="04564-106">参数</span><span class="sxs-lookup"><span data-stu-id="04564-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="04564-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="04564-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="04564-108">包含资源的文件的文件标记或程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="04564-108">File token or assembly ID of file that contains the resource.</span></span>  
  
 `pszResourceName`  
 <span data-ttu-id="04564-109">资源的名称。</span><span class="sxs-lookup"><span data-stu-id="04564-109">Name of the resource.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="04564-110">RVA 中资源的偏移量。</span><span class="sxs-lookup"><span data-stu-id="04564-110">Offset of resource from RVA.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="04564-111">辅助功能标志 `mrPublic` ，例如和 `mrPrivate` 。</span><span class="sxs-lookup"><span data-stu-id="04564-111">Accessibility flags such as `mrPublic` and `mrPrivate`.</span></span> <span data-ttu-id="04564-112">这些标志可能会传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="04564-112">These flags may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="04564-113">返回值</span><span class="sxs-lookup"><span data-stu-id="04564-113">Return Value</span></span>  

 <span data-ttu-id="04564-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="04564-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04564-115">要求</span><span class="sxs-lookup"><span data-stu-id="04564-115">Requirements</span></span>  

 <span data-ttu-id="04564-116">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="04564-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04564-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04564-117">See also</span></span>

- [<span data-ttu-id="04564-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="04564-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="04564-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="04564-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="04564-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="04564-120">ALink API</span></span>](index.md)
