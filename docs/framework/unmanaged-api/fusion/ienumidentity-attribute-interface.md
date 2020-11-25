---
title: IEnumIDENTITY_ATTRIBUTE 接口
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
ms.openlocfilehash: 71a6ea9f593da093985a4420e690f1bdd7f9d139
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728987"
---
# <a name="ienumidentity_attribute-interface"></a><span data-ttu-id="a6403-102">IEnumIDENTITY_ATTRIBUTE 接口</span><span class="sxs-lookup"><span data-stu-id="a6403-102">IEnumIDENTITY_ATTRIBUTE Interface</span></span>

<span data-ttu-id="a6403-103">用作当前范围中代码对象的特性的枚举数。</span><span class="sxs-lookup"><span data-stu-id="a6403-103">Serves as an enumerator for the attributes of the code object in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a6403-104">方法</span><span class="sxs-lookup"><span data-stu-id="a6403-104">Methods</span></span>  
  
|<span data-ttu-id="a6403-105">方法</span><span class="sxs-lookup"><span data-stu-id="a6403-105">Method</span></span>|<span data-ttu-id="a6403-106">说明</span><span class="sxs-lookup"><span data-stu-id="a6403-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|<span data-ttu-id="a6403-107">获取一个接口指针，该指针指向 `IEnumIDENTITY_ATTRIBUTE` 包含与此相同的成员的新 `IEnumIDENTITY_ATTRIBUTE` 。</span><span class="sxs-lookup"><span data-stu-id="a6403-107">Gets an interface pointer to a new `IEnumIDENTITY_ATTRIBUTE` that contains the same members as this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|<span data-ttu-id="a6403-108">将此中包含的数据写入 `IEnumIDENTITY_ATTRIBUTE` 指定的数据缓冲区。</span><span class="sxs-lookup"><span data-stu-id="a6403-108">Writes the data contained in the elements of this `IEnumIDENTITY_ATTRIBUTE` to the specified data buffer.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|<span data-ttu-id="a6403-109">从当前位置开始，获取指定数目的属性。</span><span class="sxs-lookup"><span data-stu-id="a6403-109">Gets the specified number of attributes, starting at the current position.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|<span data-ttu-id="a6403-110">将指令指针移到此的开头 `IEnumIDENTITY_ATTRIBUTE` 。</span><span class="sxs-lookup"><span data-stu-id="a6403-110">Moves the instruction pointer to the beginning of this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|<span data-ttu-id="a6403-111">从当前位置开始，将指令指针向前移动指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="a6403-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a6403-112">要求</span><span class="sxs-lookup"><span data-stu-id="a6403-112">Requirements</span></span>  

 <span data-ttu-id="a6403-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6403-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6403-114">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="a6403-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="a6403-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6403-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6403-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6403-116">See also</span></span>

- [<span data-ttu-id="a6403-117">合成接口</span><span class="sxs-lookup"><span data-stu-id="a6403-117">Fusion Interfaces</span></span>](fusion-interfaces.md)
