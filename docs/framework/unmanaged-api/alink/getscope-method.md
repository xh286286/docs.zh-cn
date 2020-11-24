---
title: GetScope 方法
ms.date: 03/30/2017
api_name:
- IALink.GetScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope
helpviewer_keywords:
- GetScope method
ms.assetid: e1555328-2c71-4ece-b357-9eb6d3a8efc4
topic_type:
- apiref
ms.openlocfilehash: fd5ae6ef40cb171c33132df0f640acbef96d69b5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684664"
---
# <a name="getscope-method"></a><span data-ttu-id="04a6c-102">GetScope 方法</span><span class="sxs-lookup"><span data-stu-id="04a6c-102">GetScope Method</span></span>

<span data-ttu-id="04a6c-103">获取导入范围。</span><span class="sxs-lookup"><span data-stu-id="04a6c-103">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04a6c-104">语法</span><span class="sxs-lookup"><span data-stu-id="04a6c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetScope(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport** ppImportScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="04a6c-105">参数</span><span class="sxs-lookup"><span data-stu-id="04a6c-105">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="04a6c-106">要导入到的程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="04a6c-106">Unique ID of assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="04a6c-107">要从中导入的文件的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="04a6c-107">Unique ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="04a6c-108">要导入的从零开始的范围。</span><span class="sxs-lookup"><span data-stu-id="04a6c-108">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="04a6c-109">接收作用域的 [IMetaDataImport 接口](../metadata/imetadataimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="04a6c-109">Receives [IMetaDataImport Interface](../metadata/imetadataimport-interface.md) interface for the scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="04a6c-110">返回值</span><span class="sxs-lookup"><span data-stu-id="04a6c-110">Return Value</span></span>  

 <span data-ttu-id="04a6c-111">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="04a6c-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04a6c-112">要求</span><span class="sxs-lookup"><span data-stu-id="04a6c-112">Requirements</span></span>  

 <span data-ttu-id="04a6c-113">需要 alink</span><span class="sxs-lookup"><span data-stu-id="04a6c-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04a6c-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04a6c-114">See also</span></span>

- [<span data-ttu-id="04a6c-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="04a6c-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="04a6c-116">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="04a6c-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="04a6c-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="04a6c-117">ALink API</span></span>](index.md)
