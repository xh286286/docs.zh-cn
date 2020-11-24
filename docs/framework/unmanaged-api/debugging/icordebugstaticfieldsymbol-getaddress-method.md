---
title: ICorDebugStaticFieldSymbol::GetAddress 方法
ms.date: 03/30/2017
ms.assetid: 5a6c9a5a-ec72-4c40-a9c3-cee7baa63687
ms.openlocfilehash: e9404b429ad4507acb5132a86af5f287dbcf07b3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677279"
---
# <a name="icordebugstaticfieldsymbolgetaddress-method"></a><span data-ttu-id="4d9e6-102">ICorDebugStaticFieldSymbol::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="4d9e6-102">ICorDebugStaticFieldSymbol::GetAddress Method</span></span>

<span data-ttu-id="4d9e6-103">获取静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="4d9e6-103">Gets the address of a static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d9e6-104">语法</span><span class="sxs-lookup"><span data-stu-id="4d9e6-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress(  
   [out] CORDB_ADDRESS *pRVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4d9e6-105">参数</span><span class="sxs-lookup"><span data-stu-id="4d9e6-105">Parameters</span></span>  

 <span data-ttu-id="4d9e6-106">pRVA</span><span class="sxs-lookup"><span data-stu-id="4d9e6-106">pRVA</span></span>  
 <span data-ttu-id="4d9e6-107">[out] 指向静态字段的相对虚拟地址 (RVA) 的指针。</span><span class="sxs-lookup"><span data-stu-id="4d9e6-107">[out] A pointer to the relative virtual address (RVA) of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4d9e6-108">注解</span><span class="sxs-lookup"><span data-stu-id="4d9e6-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4d9e6-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="4d9e6-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4d9e6-110">要求</span><span class="sxs-lookup"><span data-stu-id="4d9e6-110">Requirements</span></span>  

 <span data-ttu-id="4d9e6-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4d9e6-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4d9e6-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4d9e6-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4d9e6-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4d9e6-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4d9e6-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4d9e6-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d9e6-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d9e6-115">See also</span></span>

- [<span data-ttu-id="4d9e6-116">ICorDebugStaticFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="4d9e6-116">ICorDebugStaticFieldSymbol Interface</span></span>](icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="4d9e6-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="4d9e6-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
