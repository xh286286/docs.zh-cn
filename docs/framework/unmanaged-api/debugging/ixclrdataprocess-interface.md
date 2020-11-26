---
title: IXCLRDataProcess 接口
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess Interface
helpviewer.keywords:
- IXCLRDataProcess Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 376ec2b840bc17c79ed1f27c17a8ddd22c37a0f4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96245336"
---
# <a name="ixclrdataprocess-interface"></a><span data-ttu-id="0211d-102">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="0211d-102">IXCLRDataProcess Interface</span></span>

<span data-ttu-id="0211d-103">提供用于查询有关进程的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0211d-103">Provides methods for querying information about a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="0211d-104">方法</span><span class="sxs-lookup"><span data-stu-id="0211d-104">Methods</span></span>

| <span data-ttu-id="0211d-105">方法</span><span class="sxs-lookup"><span data-stu-id="0211d-105">Method</span></span>                                                                                                                                               | <span data-ttu-id="0211d-106">描述</span><span class="sxs-lookup"><span data-stu-id="0211d-106">Description</span></span>                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="0211d-107">GetRuntimeNameByAddress</span><span class="sxs-lookup"><span data-stu-id="0211d-107">GetRuntimeNameByAddress</span></span>](ixclrdataprocess-getruntimenamebyaddress-method.md)                     | <span data-ttu-id="0211d-108">获取给定地址的名称。</span><span class="sxs-lookup"><span data-stu-id="0211d-108">Gets a name for the given address.</span></span>                                                               |
| [<span data-ttu-id="0211d-109">GetAppDomainByUniqueId</span><span class="sxs-lookup"><span data-stu-id="0211d-109">GetAppDomainByUniqueId</span></span>](ixclrdataprocess-getappdomainbyuniqueid-method.md)                       | <span data-ttu-id="0211d-110">`AppDomain`按其唯一 id 在进程中获取。</span><span class="sxs-lookup"><span data-stu-id="0211d-110">Gets an `AppDomain` in a process by its unique id.</span></span>                                              |
| [<span data-ttu-id="0211d-111">StartEnumModules</span><span class="sxs-lookup"><span data-stu-id="0211d-111">StartEnumModules</span></span>](ixclrdataprocess-startenummodules-method.md)                                   | <span data-ttu-id="0211d-112">提供枚举进程的模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="0211d-112">Provides a handle to enumerate the modules of a process.</span></span>                                        |
| [<span data-ttu-id="0211d-113">EnumModule</span><span class="sxs-lookup"><span data-stu-id="0211d-113">EnumModule</span></span>](ixclrdataprocess-enummodule-method.md)                                               | <span data-ttu-id="0211d-114">枚举此进程的模块。</span><span class="sxs-lookup"><span data-stu-id="0211d-114">Enumerates the modules of this process.</span></span>                                                         |
| [<span data-ttu-id="0211d-115">EndEnumModules</span><span class="sxs-lookup"><span data-stu-id="0211d-115">EndEnumModules</span></span>](ixclrdataprocess-endenummodules-method.md)                                       | <span data-ttu-id="0211d-116">释放模块枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="0211d-116">Releases the resources used by internal iterators used during module enumeration.</span></span>               |
| [<span data-ttu-id="0211d-117">StartEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="0211d-117">StartEnumMethodInstancesByAddress</span></span>](ixclrdataprocess-startenummethodinstancesbyaddress-method.md) | <span data-ttu-id="0211d-118">提供用于枚举 `AppDomain` 从给定地址开始的方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="0211d-118">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span> |
| [<span data-ttu-id="0211d-119">EnumMethodInstanceByAddress</span><span class="sxs-lookup"><span data-stu-id="0211d-119">EnumMethodInstanceByAddress</span></span>](ixclrdataprocess-enummethodinstancebyaddress-method.md)             | <span data-ttu-id="0211d-120">枚举此进程的方法实例（从地址偏移量开始）。</span><span class="sxs-lookup"><span data-stu-id="0211d-120">Enumerates the method instances of this process starting at an address offset.</span></span>                  |
| [<span data-ttu-id="0211d-121">EndEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="0211d-121">EndEnumMethodInstancesByAddress</span></span>](ixclrdataprocess-endenummethodinstancesbyaddress-method.md)     | <span data-ttu-id="0211d-122">释放实例枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="0211d-122">Releases the resources used by internal iterators used during instance enumeration.</span></span>             |

## <a name="remarks"></a><span data-ttu-id="0211d-123">备注</span><span class="sxs-lookup"><span data-stu-id="0211d-123">Remarks</span></span>

<span data-ttu-id="0211d-124">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="0211d-124">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="0211d-125">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="0211d-125">However, it's a COM interface that derives from `IUnknown` with GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="0211d-126">要求</span><span class="sxs-lookup"><span data-stu-id="0211d-126">Requirements</span></span>

<span data-ttu-id="0211d-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0211d-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>
<span data-ttu-id="0211d-128">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="0211d-128">**Header:** None</span></span>  
<span data-ttu-id="0211d-129">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="0211d-129">**Library:** None</span></span>  
<span data-ttu-id="0211d-130">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0211d-130">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="0211d-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0211d-131">See also</span></span>

- [<span data-ttu-id="0211d-132">调试</span><span class="sxs-lookup"><span data-stu-id="0211d-132">Debugging</span></span>](index.md)
- [<span data-ttu-id="0211d-133">调试接口</span><span class="sxs-lookup"><span data-stu-id="0211d-133">Debugging Interfaces</span></span>](debugging-interfaces.md)
