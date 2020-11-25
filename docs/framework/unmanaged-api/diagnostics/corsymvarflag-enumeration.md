---
title: CorSymVarFlag 枚举
ms.date: 03/30/2017
api_name:
- CorSymVarFlag
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymVarFlag
helpviewer_keywords:
- CorSymVarFlag enumeration [.NET Framework debugging]
ms.assetid: c3f7d307-4047-4f9a-be8c-f152fca42fd0
topic_type:
- apiref
ms.openlocfilehash: ed08d9f818f6fc180dbd655243488bf8a527ae11
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725282"
---
# <a name="corsymvarflag-enumeration"></a><span data-ttu-id="3c171-102">CorSymVarFlag 枚举</span><span class="sxs-lookup"><span data-stu-id="3c171-102">CorSymVarFlag Enumeration</span></span>

<span data-ttu-id="3c171-103">指示变量是否是编译器生成的。</span><span class="sxs-lookup"><span data-stu-id="3c171-103">Indicates whether a variable is compiler-generated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c171-104">语法</span><span class="sxs-lookup"><span data-stu-id="3c171-104">Syntax</span></span>  
  
```cpp  
typedef enum CorSymVarFlag
{  
    VAR_IS_COMP_GEN = 1  
} CorSymVarFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="3c171-105">成员</span><span class="sxs-lookup"><span data-stu-id="3c171-105">Members</span></span>  
  
|<span data-ttu-id="3c171-106">成员</span><span class="sxs-lookup"><span data-stu-id="3c171-106">Member</span></span>|<span data-ttu-id="3c171-107">说明</span><span class="sxs-lookup"><span data-stu-id="3c171-107">Description</span></span>|  
|------------|-----------------|  
|`VAR_IS_COMP_GEN`|<span data-ttu-id="3c171-108">指示给定变量是编译器生成的。</span><span class="sxs-lookup"><span data-stu-id="3c171-108">Indicates that the given variable is compiler-generated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3c171-109">要求</span><span class="sxs-lookup"><span data-stu-id="3c171-109">Requirements</span></span>  

 <span data-ttu-id="3c171-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3c171-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c171-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c171-111">See also</span></span>

- [<span data-ttu-id="3c171-112">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="3c171-112">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)
