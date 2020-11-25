---
title: AssemblyRefFlags 枚举
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
ms.openlocfilehash: 0a99d2f79645bdc46ff4db86d7280614eeb1faf5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732757"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="7df39-102">AssemblyRefFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="7df39-102">AssemblyRefFlags Enumeration</span></span>

<span data-ttu-id="7df39-103">包含用于描述程序集引用的功能的值。</span><span class="sxs-lookup"><span data-stu-id="7df39-103">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7df39-104">语法</span><span class="sxs-lookup"><span data-stu-id="7df39-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="7df39-105">成员</span><span class="sxs-lookup"><span data-stu-id="7df39-105">Members</span></span>  
  
|<span data-ttu-id="7df39-106">成员</span><span class="sxs-lookup"><span data-stu-id="7df39-106">Member</span></span>|<span data-ttu-id="7df39-107">说明</span><span class="sxs-lookup"><span data-stu-id="7df39-107">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="7df39-108">指定程序集引用包含有关程序集的发布服务器的完整的未哈哈希信息。</span><span class="sxs-lookup"><span data-stu-id="7df39-108">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7df39-109">要求</span><span class="sxs-lookup"><span data-stu-id="7df39-109">Requirements</span></span>  

 <span data-ttu-id="7df39-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7df39-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7df39-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="7df39-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7df39-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7df39-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7df39-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7df39-113">See also</span></span>

- [<span data-ttu-id="7df39-114">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="7df39-114">Metadata Enumerations</span></span>](metadata-enumerations.md)
- [<span data-ttu-id="7df39-115">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="7df39-115">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
- [<span data-ttu-id="7df39-116">DefineAssemblyRef 方法</span><span class="sxs-lookup"><span data-stu-id="7df39-116">DefineAssemblyRef Method</span></span>](imetadataassemblyemit-defineassemblyref-method.md)
