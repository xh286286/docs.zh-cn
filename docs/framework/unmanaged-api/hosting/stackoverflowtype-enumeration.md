---
title: StackOverflowType 枚举
ms.date: 03/30/2017
api_name:
- StackOverflowType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowType
helpviewer_keywords:
- StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type:
- apiref
ms.openlocfilehash: bbdc68721378e6bbb09f5e4eade08e2e6e03b097
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729902"
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="babc8-102">StackOverflowType 枚举</span><span class="sxs-lookup"><span data-stu-id="babc8-102">StackOverflowType Enumeration</span></span>

<span data-ttu-id="babc8-103">包含指示堆栈溢出事件的根本原因的值。</span><span class="sxs-lookup"><span data-stu-id="babc8-103">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="babc8-104">语法</span><span class="sxs-lookup"><span data-stu-id="babc8-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="babc8-105">成员</span><span class="sxs-lookup"><span data-stu-id="babc8-105">Members</span></span>  
  
|<span data-ttu-id="babc8-106">成员</span><span class="sxs-lookup"><span data-stu-id="babc8-106">Member</span></span>|<span data-ttu-id="babc8-107">说明</span><span class="sxs-lookup"><span data-stu-id="babc8-107">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="babc8-108">堆栈溢出由执行引擎引起。</span><span class="sxs-lookup"><span data-stu-id="babc8-108">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="babc8-109">堆栈溢出由托管代码引起。</span><span class="sxs-lookup"><span data-stu-id="babc8-109">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="babc8-110">堆栈溢出由非托管代码引起。</span><span class="sxs-lookup"><span data-stu-id="babc8-110">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="babc8-111">注解</span><span class="sxs-lookup"><span data-stu-id="babc8-111">Remarks</span></span>  

 <span data-ttu-id="babc8-112">此信息通过调用 [IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md) 方法传递到主机。</span><span class="sxs-lookup"><span data-stu-id="babc8-112">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="babc8-113">要求</span><span class="sxs-lookup"><span data-stu-id="babc8-113">Requirements</span></span>  

 <span data-ttu-id="babc8-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="babc8-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="babc8-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="babc8-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="babc8-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="babc8-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="babc8-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="babc8-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="babc8-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="babc8-118">See also</span></span>

- [<span data-ttu-id="babc8-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="babc8-119">Hosting Enumerations</span></span>](hosting-enumerations.md)
