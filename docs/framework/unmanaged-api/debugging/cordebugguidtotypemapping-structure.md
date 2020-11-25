---
title: CorDebugGuidToTypeMapping 结构
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugGuidToTypeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGuidToTypeMapping
helpviewer_keywords:
- CorDebugGuidToTypeMapping structure [.NET Framework debugging]
ms.assetid: 57dbccd9-b16d-4da3-ae25-7a2cf9adf679
topic_type:
- apiref
ms.openlocfilehash: 859853521b741f42f1de7921de813941d2501173
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729091"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="2bdd3-102">CorDebugGuidToTypeMapping 结构</span><span class="sxs-lookup"><span data-stu-id="2bdd3-102">CorDebugGuidToTypeMapping Structure</span></span>

<span data-ttu-id="2bdd3-103">将 Windows 运行时 GUID 映射到其对应的 ICorDebugType 对象。</span><span class="sxs-lookup"><span data-stu-id="2bdd3-103">Maps a Windows Runtime GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bdd3-104">语法</span><span class="sxs-lookup"><span data-stu-id="2bdd3-104">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="2bdd3-105">成员</span><span class="sxs-lookup"><span data-stu-id="2bdd3-105">Members</span></span>  
  
|<span data-ttu-id="2bdd3-106">成员</span><span class="sxs-lookup"><span data-stu-id="2bdd3-106">Member</span></span>|<span data-ttu-id="2bdd3-107">说明</span><span class="sxs-lookup"><span data-stu-id="2bdd3-107">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="2bdd3-108">缓存的 Windows 运行时类型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2bdd3-108">The GUID of the cached Windows Runtime type.</span></span>|  
|`pType`|<span data-ttu-id="2bdd3-109">指向 ICorDebugType 对象的指针，该对象提供有关缓存类型的信息。</span><span class="sxs-lookup"><span data-stu-id="2bdd3-109">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2bdd3-110">要求</span><span class="sxs-lookup"><span data-stu-id="2bdd3-110">Requirements</span></span>  

 <span data-ttu-id="2bdd3-111">**平台：** Windows 运行时。</span><span class="sxs-lookup"><span data-stu-id="2bdd3-111">**Platforms:** Windows Runtime.</span></span>  
  
 <span data-ttu-id="2bdd3-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2bdd3-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2bdd3-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2bdd3-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2bdd3-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2bdd3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bdd3-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2bdd3-115">See also</span></span>

- [<span data-ttu-id="2bdd3-116">调试结构</span><span class="sxs-lookup"><span data-stu-id="2bdd3-116">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="2bdd3-117">调试</span><span class="sxs-lookup"><span data-stu-id="2bdd3-117">Debugging</span></span>](index.md)
