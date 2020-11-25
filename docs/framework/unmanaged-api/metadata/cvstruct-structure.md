---
title: CVStruct 结构
ms.date: 03/30/2017
api_name:
- CVStruct
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CVStruct
helpviewer_keywords:
- CVStruct structure [.NET Framework metadata]
ms.assetid: e9e4e497-d5fb-464b-991c-3bdd824664fd
topic_type:
- apiref
ms.openlocfilehash: db36b94fafe20b58b9bcbb886b8d285326960f67
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715571"
---
# <a name="cvstruct-structure"></a><span data-ttu-id="3536d-102">CVStruct 结构</span><span class="sxs-lookup"><span data-stu-id="3536d-102">CVStruct Structure</span></span>

<span data-ttu-id="3536d-103">包含在安装模块或复合图像时所使用的信息。</span><span class="sxs-lookup"><span data-stu-id="3536d-103">Contains information that is used when installing a module or a composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3536d-104">语法</span><span class="sxs-lookup"><span data-stu-id="3536d-104">Syntax</span></span>  
  
```cpp  
typedef struct {  
    short Major;  
    short Minor;  
    short Sub;  
    short Build;  
} CVStruct;  
```  
  
## <a name="members"></a><span data-ttu-id="3536d-105">成员</span><span class="sxs-lookup"><span data-stu-id="3536d-105">Members</span></span>  
  
|<span data-ttu-id="3536d-106">成员</span><span class="sxs-lookup"><span data-stu-id="3536d-106">Member</span></span>|<span data-ttu-id="3536d-107">说明</span><span class="sxs-lookup"><span data-stu-id="3536d-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="3536d-108">主要</span><span class="sxs-lookup"><span data-stu-id="3536d-108">Major</span></span>|<span data-ttu-id="3536d-109">主版本的内部版本号。</span><span class="sxs-lookup"><span data-stu-id="3536d-109">Major version build number.</span></span>|  
|<span data-ttu-id="3536d-110">次要</span><span class="sxs-lookup"><span data-stu-id="3536d-110">Minor</span></span>|<span data-ttu-id="3536d-111">次版本号。</span><span class="sxs-lookup"><span data-stu-id="3536d-111">Minor version build number.</span></span>|  
|<span data-ttu-id="3536d-112">Sub</span><span class="sxs-lookup"><span data-stu-id="3536d-112">Sub</span></span>|<span data-ttu-id="3536d-113">子生成号。</span><span class="sxs-lookup"><span data-stu-id="3536d-113">Sub-build number.</span></span>|  
|<span data-ttu-id="3536d-114">生成</span><span class="sxs-lookup"><span data-stu-id="3536d-114">Build</span></span>|<span data-ttu-id="3536d-115">内部版本号。</span><span class="sxs-lookup"><span data-stu-id="3536d-115">Build number.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3536d-116">要求</span><span class="sxs-lookup"><span data-stu-id="3536d-116">Requirements</span></span>  

 <span data-ttu-id="3536d-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3536d-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3536d-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3536d-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3536d-119">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3536d-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3536d-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3536d-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3536d-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3536d-121">See also</span></span>

- [<span data-ttu-id="3536d-122">元数据结构</span><span class="sxs-lookup"><span data-stu-id="3536d-122">Metadata Structures</span></span>](metadata-structures.md)
