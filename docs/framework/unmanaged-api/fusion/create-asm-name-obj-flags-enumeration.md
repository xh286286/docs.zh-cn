---
title: CREATE_ASM_NAME_OBJ_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- CREATE_ASM_NAME_OBJ_FLAGS
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- CREATE_ASM_NAME_OBJ_FLAGS
helpviewer_keywords:
- CREATE_ASM_NAME_OBJ_FLAGS enumeration [.NET Framework fusion]
ms.assetid: a5ed2fd0-c7d2-4603-aaca-5d0caad92675
topic_type:
- apiref
ms.openlocfilehash: 52d5ad3a18c102422e90621c7d1e23b2692c0000
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683222"
---
# <a name="create_asm_name_obj_flags-enumeration"></a><span data-ttu-id="e5259-102">CREATE_ASM_NAME_OBJ_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="e5259-102">CREATE_ASM_NAME_OBJ_FLAGS Enumeration</span></span>

<span data-ttu-id="e5259-103">指定 [IAssemblyName 接口](iassemblyname-interface.md) 对象在由 [CreateAssemblyNameObject](createassemblynameobject-function.md) 函数构建时的特性。</span><span class="sxs-lookup"><span data-stu-id="e5259-103">Specifies the attributes of an [IAssemblyName Interface](iassemblyname-interface.md) object when it is constructed by the [CreateAssemblyNameObject](createassemblynameobject-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5259-104">语法</span><span class="sxs-lookup"><span data-stu-id="e5259-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
  
    CANOF_PARSE_DISPLAY_NAME            = 0x1,  
    CANOF_SET_DEFAULT_VALUES            = 0x2,  
    CANOF_VERIFY_FRIEND_ASSEMBLYNAME    = 0x4,  
    CANOF_PARSE_FRIEND_DISPLAY_NAME     =
        CANOF_PARSE_DISPLAY_NAME | CANOF_VERIFY_FRIEND_ASSEMBLYNAME  
  
} CREATE_ASM_NAME_OBJ_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="e5259-105">成员</span><span class="sxs-lookup"><span data-stu-id="e5259-105">Members</span></span>  
  
|<span data-ttu-id="e5259-106">成员</span><span class="sxs-lookup"><span data-stu-id="e5259-106">Member</span></span>|<span data-ttu-id="e5259-107">说明</span><span class="sxs-lookup"><span data-stu-id="e5259-107">Description</span></span>|  
|------------|-----------------|  
|`CANOF_PARSE_DISPLAY_NAME`|<span data-ttu-id="e5259-108">指示传递的参数是文本标识。</span><span class="sxs-lookup"><span data-stu-id="e5259-108">Indicates that the parameter passed is a textual identity.</span></span>|  
|`CANOF_SET_DEFAULT_VALUES`|<span data-ttu-id="e5259-109">设置几个默认值。</span><span class="sxs-lookup"><span data-stu-id="e5259-109">Sets a few default values.</span></span>|  
|`CANOF_VERIFY_FRIEND_ASSEMBLYNAME`|<span data-ttu-id="e5259-110">验证友元程序集规则 (仅名称和公钥) 。</span><span class="sxs-lookup"><span data-stu-id="e5259-110">Verifies the friend assembly rule (only name and public key).</span></span> <span data-ttu-id="e5259-111">此成员仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="e5259-111">This member is for internal use only.</span></span>|  
|`CANOF_PARSE_FRIEND_DISPLAY_NAME`|<span data-ttu-id="e5259-112">和标志的组合 `CANOF_PARSE_DISPLAY_NAME` `CANOF_VERIFY_FRIEND_ASSEMBLYNAME` 。</span><span class="sxs-lookup"><span data-stu-id="e5259-112">A combination of the `CANOF_PARSE_DISPLAY_NAME` and `CANOF_VERIFY_FRIEND_ASSEMBLYNAME` flags.</span></span> <span data-ttu-id="e5259-113">此成员仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="e5259-113">This member is for internal use only.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e5259-114">要求</span><span class="sxs-lookup"><span data-stu-id="e5259-114">Requirements</span></span>  

 <span data-ttu-id="e5259-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e5259-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5259-116">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="e5259-116">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="e5259-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5259-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5259-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5259-118">See also</span></span>

- [<span data-ttu-id="e5259-119">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="e5259-119">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="e5259-120">CreateAssemblyNameObject 函数</span><span class="sxs-lookup"><span data-stu-id="e5259-120">CreateAssemblyNameObject Function</span></span>](createassemblynameobject-function.md)
- [<span data-ttu-id="e5259-121">合成枚举</span><span class="sxs-lookup"><span data-stu-id="e5259-121">Fusion Enumerations</span></span>](fusion-enumerations.md)
