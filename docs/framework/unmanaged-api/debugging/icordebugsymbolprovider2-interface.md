---
title: ICorDebugSymbolProvider2 接口
ms.date: 03/30/2017
ms.assetid: 1c9c3d92-f0de-4d4d-87f1-0c702a4808af
ms.openlocfilehash: 3bef03e9e85224058bc17e1f0ce8746e98aa30f6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688336"
---
# <a name="icordebugsymbolprovider2-interface"></a><span data-ttu-id="ed4c9-102">ICorDebugSymbolProvider2 接口</span><span class="sxs-lookup"><span data-stu-id="ed4c9-102">ICorDebugSymbolProvider2 Interface</span></span>

<span data-ttu-id="ed4c9-103">以逻辑方式扩展 [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) 接口以检索其他调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-103">Logically extends the [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) interface to retrieve additional debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ed4c9-104">方法</span><span class="sxs-lookup"><span data-stu-id="ed4c9-104">Methods</span></span>  
  
|<span data-ttu-id="ed4c9-105">方法</span><span class="sxs-lookup"><span data-stu-id="ed4c9-105">Method</span></span>|<span data-ttu-id="ed4c9-106">说明</span><span class="sxs-lookup"><span data-stu-id="ed4c9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ed4c9-107">GetFrameProps 方法</span><span class="sxs-lookup"><span data-stu-id="ed4c9-107">GetFrameProps Method</span></span>](icordebugsymbolprovider2-getframeprops-method.md)|<span data-ttu-id="ed4c9-108">返回启动方法相对虚拟地址的方法和具有代码相对虚拟地址的父框架。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-108">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>|  
|[<span data-ttu-id="ed4c9-109">GetGenericDictionaryInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ed4c9-109">GetGenericDictionaryInfo Method</span></span>](icordebugsymbolprovider2-getgenericdictionaryinfo-method.md)|<span data-ttu-id="ed4c9-110">检索泛型字典映射。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-110">Retrieves a generic dictionary map.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed4c9-111">注解</span><span class="sxs-lookup"><span data-stu-id="ed4c9-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed4c9-112">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="ed4c9-113">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed4c9-114">要求</span><span class="sxs-lookup"><span data-stu-id="ed4c9-114">Requirements</span></span>  

 <span data-ttu-id="ed4c9-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed4c9-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed4c9-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ed4c9-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ed4c9-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed4c9-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed4c9-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed4c9-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed4c9-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed4c9-119">See also</span></span>

- [<span data-ttu-id="ed4c9-120">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="ed4c9-120">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="ed4c9-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="ed4c9-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="ed4c9-122">调试</span><span class="sxs-lookup"><span data-stu-id="ed4c9-122">Debugging</span></span>](index.md)
