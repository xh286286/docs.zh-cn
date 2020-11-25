---
title: COR_ACTIVE_FUNCTION 结构
ms.date: 03/30/2017
api_name:
- COR_ACTIVE_FUNCTION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_ACTIVE_FUNCTION
helpviewer_keywords:
- COR_ACTIVE_FUNCTION structure [.NET Framework debugging]
ms.assetid: ed86185f-2152-459c-961f-10c06d62e83f
topic_type:
- apiref
ms.openlocfilehash: c50ba530d78296ebb956329b2f34b4f1e5cae94c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727414"
---
# <a name="cor_active_function-structure"></a><span data-ttu-id="42f88-102">COR_ACTIVE_FUNCTION 结构</span><span class="sxs-lookup"><span data-stu-id="42f88-102">COR_ACTIVE_FUNCTION Structure</span></span>

<span data-ttu-id="42f88-103">包含有关在线程框架中当前处于活动状态的函数的信息。</span><span class="sxs-lookup"><span data-stu-id="42f88-103">Contains information about the functions that are currently active in a thread's frames.</span></span> <span data-ttu-id="42f88-104">此结构由 [ICorDebugThread2：： GetActiveFunctions](icordebugthread2-getactivefunctions-method.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="42f88-104">This structure is used by the [ICorDebugThread2::GetActiveFunctions](icordebugthread2-getactivefunctions-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42f88-105">语法</span><span class="sxs-lookup"><span data-stu-id="42f88-105">Syntax</span></span>  
  
```cpp  
typedef struct  _COR_ACTIVE_FUNCTION {  
    ICorDebugAppDomain   *pAppDomain;  
    ICorDebugModule      *pModule;  
    ICorDebugFunction2   *pFunction;  
    ULONG32              ilOffset;  
    ULONG32              flags;  
} COR_ACTIVE_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="42f88-106">成员</span><span class="sxs-lookup"><span data-stu-id="42f88-106">Members</span></span>  
  
|<span data-ttu-id="42f88-107">成员</span><span class="sxs-lookup"><span data-stu-id="42f88-107">Member</span></span>|<span data-ttu-id="42f88-108">说明</span><span class="sxs-lookup"><span data-stu-id="42f88-108">Description</span></span>|  
|------------|-----------------|  
|`pAppDomain`|<span data-ttu-id="42f88-109">指向字段的应用程序域所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="42f88-109">Pointer to the application domain owner of the `ilOffset` field.</span></span>|  
|`pModule`|<span data-ttu-id="42f88-110">指向字段的模块所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="42f88-110">Pointer to the module owner of the `ilOffset` field.</span></span>|  
|`pFunction`|<span data-ttu-id="42f88-111">指向字段的函数所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="42f88-111">Pointer to the function owner of the `ilOffset` field.</span></span>|  
|`ilOffset`|<span data-ttu-id="42f88-112">Microsoft 中间语言 (MSIL) 帧偏移量。</span><span class="sxs-lookup"><span data-stu-id="42f88-112">The Microsoft intermediate language (MSIL) offset of the frame.</span></span>|  
|`flags`|<span data-ttu-id="42f88-113">保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="42f88-113">Reserved for future extensibility.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="42f88-114">要求</span><span class="sxs-lookup"><span data-stu-id="42f88-114">Requirements</span></span>  

 <span data-ttu-id="42f88-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42f88-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42f88-116">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="42f88-116">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="42f88-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="42f88-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="42f88-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42f88-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42f88-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42f88-119">See also</span></span>

- [<span data-ttu-id="42f88-120">调试结构</span><span class="sxs-lookup"><span data-stu-id="42f88-120">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="42f88-121">调试</span><span class="sxs-lookup"><span data-stu-id="42f88-121">Debugging</span></span>](index.md)
