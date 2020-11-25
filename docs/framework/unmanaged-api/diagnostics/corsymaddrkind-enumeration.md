---
title: CorSymAddrKind 枚举
ms.date: 03/30/2017
api_name:
- CorSymAddrKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymAddrKind
helpviewer_keywords:
- CorSymAddrKind enumeration [.NET Framework debugging]
ms.assetid: 3ef841c2-cade-42ee-ba34-2ef91d6d0879
topic_type:
- apiref
ms.openlocfilehash: f71d8956e8706cdc71b94b6e6e2e8210e5b9161e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725230"
---
# <a name="corsymaddrkind-enumeration"></a><span data-ttu-id="7b991-102">CorSymAddrKind 枚举</span><span class="sxs-lookup"><span data-stu-id="7b991-102">CorSymAddrKind Enumeration</span></span>

<span data-ttu-id="7b991-103">指示内存地址的类型。</span><span class="sxs-lookup"><span data-stu-id="7b991-103">Indicates the type of memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b991-104">语法</span><span class="sxs-lookup"><span data-stu-id="7b991-104">Syntax</span></span>  
  
```cpp  
typedef enum CorSymAddrKind  
{  
    ADDR_IL_OFFSET          = 1,  
    ADDR_NATIVE_RVA         = 2,  
    ADDR_NATIVE_REGISTER    = 3,  
    ADDR_NATIVE_REGREL      = 4,  
    ADDR_NATIVE_OFFSET      = 5,  
    ADDR_NATIVE_REGREG      = 6,  
    ADDR_NATIVE_REGSTK      = 7,  
    ADDR_NATIVE_STKREG      = 8,  
    ADDR_BITFIELD           = 9,  
    ADDR_NATIVE_ISECTOFFSET = 10  
} CorSymAddrKind;  
```  
  
## <a name="members"></a><span data-ttu-id="7b991-105">成员</span><span class="sxs-lookup"><span data-stu-id="7b991-105">Members</span></span>  
  
|<span data-ttu-id="7b991-106">成员</span><span class="sxs-lookup"><span data-stu-id="7b991-106">Member</span></span>|<span data-ttu-id="7b991-107">说明</span><span class="sxs-lookup"><span data-stu-id="7b991-107">Description</span></span>|  
|------------|-----------------|  
|`ADDR_IL_OFFSET`|<span data-ttu-id="7b991-108">指示 (MSIL) 本地变量或参数索引的 Microsoft 中间语言。</span><span class="sxs-lookup"><span data-stu-id="7b991-108">Indicates a Microsoft intermediate language (MSIL) local variable or parameter index.</span></span>|  
|`ADDR_NATIVE_RVA`|<span data-ttu-id="7b991-109">指示模块中的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="7b991-109">Indicates a relative virtual address into a module.</span></span>|  
|`ADDR_NATIVE_REGISTER`|<span data-ttu-id="7b991-110">指示 CPU 寄存器。</span><span class="sxs-lookup"><span data-stu-id="7b991-110">Indicates a CPU register.</span></span>|  
|`ADDR_NATIVE_REGREL`|<span data-ttu-id="7b991-111">指示第一个地址是寄存器，第二个地址是偏移量。</span><span class="sxs-lookup"><span data-stu-id="7b991-111">Indicates that the first address is a register and the second address is an offset.</span></span>|  
|`ADDR_NATIVE_OFFSET`|<span data-ttu-id="7b991-112">指示与基址的偏移量。</span><span class="sxs-lookup"><span data-stu-id="7b991-112">Indicates an offset from a base address.</span></span>|  
|`ADDR_NATIVE_REGREG`|<span data-ttu-id="7b991-113">指示第一个地址为寄存器的低部分，第二个地址为高部分。</span><span class="sxs-lookup"><span data-stu-id="7b991-113">Indicates that the first address is the low portion of a register, and the second address is the high portion.</span></span>|  
|`ADDR_NATIVE_REGSTK`|<span data-ttu-id="7b991-114">指示第一个地址是寄存器的低部分，第二个是高部分，第三个是偏移量。</span><span class="sxs-lookup"><span data-stu-id="7b991-114">Indicates that the first address is the low portion of a register, the second is the high portion, and the third is an offset.</span></span>|  
|`ADDR_NATIVE_STKREG`|<span data-ttu-id="7b991-115">指示第一个地址为寄存器，第二个为偏移量，第三个是寄存器的高位部分。</span><span class="sxs-lookup"><span data-stu-id="7b991-115">Indicates that the first address is a register, the second is an offset, and the third is the high portion of the register.</span></span>|  
|`ADDR_BITFIELD`|<span data-ttu-id="7b991-116">指示第一个地址是字段的开头，第二个地址是字段长度。</span><span class="sxs-lookup"><span data-stu-id="7b991-116">Indicates that the first address is the start of a field and the second address is the field length.</span></span>|  
|`ADDR_NATIVE_ISECTOFFSET`|<span data-ttu-id="7b991-117">指示第一个地址为节，第二个地址为偏移量。</span><span class="sxs-lookup"><span data-stu-id="7b991-117">Indicates that the first address is the section and the second address is an offset.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7b991-118">要求</span><span class="sxs-lookup"><span data-stu-id="7b991-118">Requirements</span></span>  

 <span data-ttu-id="7b991-119">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="7b991-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b991-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b991-120">See also</span></span>

- [<span data-ttu-id="7b991-121">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="7b991-121">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)
