---
title: ICorDebugAssembly 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
ms.openlocfilehash: 821eae8ea5b4147408e9fe60d1e5b70c7936959e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696240"
---
# <a name="icordebugassembly-interface"></a><span data-ttu-id="b15a7-102">ICorDebugAssembly 接口</span><span class="sxs-lookup"><span data-stu-id="b15a7-102">ICorDebugAssembly Interface</span></span>

<span data-ttu-id="b15a7-103">表示一个程序集。</span><span class="sxs-lookup"><span data-stu-id="b15a7-103">Represents an assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b15a7-104">方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-104">Methods</span></span>  
  
|<span data-ttu-id="b15a7-105">方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-105">Method</span></span>|<span data-ttu-id="b15a7-106">说明</span><span class="sxs-lookup"><span data-stu-id="b15a7-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b15a7-107">EnumerateModules 方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-107">EnumerateModules Method</span></span>](icordebugassembly-enumeratemodules-method.md)|<span data-ttu-id="b15a7-108">获取包含在程序集中的模块的枚举器。</span><span class="sxs-lookup"><span data-stu-id="b15a7-108">Gets an enumerator for the modules contained in the assembly.</span></span>|  
|[<span data-ttu-id="b15a7-109">GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-109">GetAppDomain Method</span></span>](icordebugassembly-getappdomain-method.md)|<span data-ttu-id="b15a7-110">获取一个接口指针，该指针指向包含此实例的应用程序域 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="b15a7-110">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>|  
|[<span data-ttu-id="b15a7-111">GetCodeBase 方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-111">GetCodeBase Method</span></span>](icordebugassembly-getcodebase-method.md)|<span data-ttu-id="b15a7-112">未在 .NET Framework 的当前版本中实现。</span><span class="sxs-lookup"><span data-stu-id="b15a7-112">Not implemented in the current version of the .NET Framework.</span></span>|  
|[<span data-ttu-id="b15a7-113">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-113">GetName Method</span></span>](icordebugassembly-getname-method.md)|<span data-ttu-id="b15a7-114">获取程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="b15a7-114">Gets the name of the assembly.</span></span>|  
|[<span data-ttu-id="b15a7-115">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="b15a7-115">GetProcess Method</span></span>](icordebugassembly-getprocess-method.md)|<span data-ttu-id="b15a7-116">获取在其中运行程序集的 ICorDebugProcess 实例。</span><span class="sxs-lookup"><span data-stu-id="b15a7-116">Gets the ICorDebugProcess instance in which the assembly is running.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b15a7-117">注解</span><span class="sxs-lookup"><span data-stu-id="b15a7-117">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b15a7-118">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b15a7-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b15a7-119">要求</span><span class="sxs-lookup"><span data-stu-id="b15a7-119">Requirements</span></span>  

 <span data-ttu-id="b15a7-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b15a7-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b15a7-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b15a7-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b15a7-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b15a7-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b15a7-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b15a7-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b15a7-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b15a7-124">See also</span></span>

- [<span data-ttu-id="b15a7-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="b15a7-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
