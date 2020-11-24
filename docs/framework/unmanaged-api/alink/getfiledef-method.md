---
title: GetFileDef 方法
ms.date: 03/30/2017
api_name:
- IALink2.GetFileDef
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetFileDef
helpviewer_keywords:
- GetFileDef method
ms.assetid: 4e3fbe6c-b82a-4181-ab17-7faa1263f5b3
topic_type:
- apiref
ms.openlocfilehash: 42935813579d7f1d55a9f1daf9d8c6c1241f85be
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684702"
---
# <a name="getfiledef-method"></a><span data-ttu-id="5c7b2-102">GetFileDef 方法</span><span class="sxs-lookup"><span data-stu-id="5c7b2-102">GetFileDef Method</span></span>

<span data-ttu-id="5c7b2-103">检索元数据 (中使用的实际 FileDef 标记，而不是由 ALink) 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="5c7b2-103">Retrieves the actual FileDef token used in metadata (as opposed to the token assigned by ALink).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c7b2-104">语法</span><span class="sxs-lookup"><span data-stu-id="5c7b2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetFileDef(  
    mdAssembly AssemblyID,  
    mdFile TargetFile,  
    mdFile* pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c7b2-105">参数</span><span class="sxs-lookup"><span data-stu-id="5c7b2-105">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="5c7b2-106">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="5c7b2-106">ID of the assembly.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="5c7b2-107">从 AddFile 方法或 AddImport 方法检索到的已添加文件的标记。</span><span class="sxs-lookup"><span data-stu-id="5c7b2-107">Token of the added file as retrieved from AddFile Method or AddImport Method.</span></span>  
  
 `pScope`  
 <span data-ttu-id="5c7b2-108">接收 FileDef 标记。</span><span class="sxs-lookup"><span data-stu-id="5c7b2-108">Receives the FileDef token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5c7b2-109">返回值</span><span class="sxs-lookup"><span data-stu-id="5c7b2-109">Return Value</span></span>  

 <span data-ttu-id="5c7b2-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="5c7b2-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c7b2-111">要求</span><span class="sxs-lookup"><span data-stu-id="5c7b2-111">Requirements</span></span>  

 <span data-ttu-id="5c7b2-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="5c7b2-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c7b2-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c7b2-113">See also</span></span>

- [<span data-ttu-id="5c7b2-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="5c7b2-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="5c7b2-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="5c7b2-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="5c7b2-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="5c7b2-116">ALink API</span></span>](index.md)
