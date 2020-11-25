---
title: IAssemblyName 接口
ms.date: 03/30/2017
api_name:
- IAssemblyName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName
helpviewer_keywords:
- IAssemblyName interface [.NET Framework fusion]
ms.assetid: f7f8e605-6b67-4151-936f-f04ecd671d90
topic_type:
- apiref
ms.openlocfilehash: f6feed9f59715f9a2801cd3a2a99a087957d4377
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715064"
---
# <a name="iassemblyname-interface"></a><span data-ttu-id="b9074-102">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="b9074-102">IAssemblyName Interface</span></span>

<span data-ttu-id="b9074-103">提供用于描述和处理程序集的唯一标识的方法。</span><span class="sxs-lookup"><span data-stu-id="b9074-103">Provides methods for describing and working with an assembly's unique identity.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b9074-104">方法</span><span class="sxs-lookup"><span data-stu-id="b9074-104">Methods</span></span>  
  
|<span data-ttu-id="b9074-105">方法</span><span class="sxs-lookup"><span data-stu-id="b9074-105">Method</span></span>|<span data-ttu-id="b9074-106">说明</span><span class="sxs-lookup"><span data-stu-id="b9074-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b9074-107">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-107">Clone Method</span></span>](iassemblyname-clone-method.md)|<span data-ttu-id="b9074-108">创建此对象的浅表副本 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-108">Creates a shallow copy of this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="b9074-109">Finalize 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-109">Finalize Method</span></span>](iassemblyname-finalize-method.md)|<span data-ttu-id="b9074-110">允许此 `IAssemblyName` 对象在调用其析构函数之前释放资源并执行其他清理操作。</span><span class="sxs-lookup"><span data-stu-id="b9074-110">Allows this `IAssemblyName` object to release resources and perform other cleanup operations before its destructor is called.</span></span>|  
|[<span data-ttu-id="b9074-111">GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-111">GetDisplayName Method</span></span>](iassemblyname-getdisplayname-method.md)|<span data-ttu-id="b9074-112">获取此对象引用的程序集的可读名称 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-112">Gets the human-readable name of the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="b9074-113">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-113">GetName Method</span></span>](iassemblyname-getname-method.md)|<span data-ttu-id="b9074-114">获取此对象引用的程序集的简单、未加密名称 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-114">Gets the simple, unencrypted name of the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="b9074-115">GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-115">GetProperty Method</span></span>](iassemblyname-getproperty-method.md)|<span data-ttu-id="b9074-116">获取一个指针，该指针指向由指定的引用的属性 `PropertyId` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-116">Gets a pointer to the property referenced by the specified `PropertyId`.</span></span>|  
|[<span data-ttu-id="b9074-117">GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-117">GetVersion Method</span></span>](iassemblyname-getversion-method.md)|<span data-ttu-id="b9074-118">获取此对象引用的程序集的版本信息 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-118">Gets the version information for the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="b9074-119">IsEqual 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-119">IsEqual Method</span></span>](iassemblyname-isequal-method.md)|<span data-ttu-id="b9074-120">`IAssemblyName` `IAssemblyName` 根据指定的比较标志，确定指定的对象是否与此相等。</span><span class="sxs-lookup"><span data-stu-id="b9074-120">Determines whether a specified `IAssemblyName` object is equal to this `IAssemblyName`, based on the specified comparison flags.</span></span>|  
|[<span data-ttu-id="b9074-121">SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="b9074-121">SetProperty Method</span></span>](iassemblyname-setproperty-method.md)|<span data-ttu-id="b9074-122">设置由指定的引用的属性的值 `PropertyId` 。</span><span class="sxs-lookup"><span data-stu-id="b9074-122">Sets the value of the property referenced by the specified `PropertyId`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b9074-123">要求</span><span class="sxs-lookup"><span data-stu-id="b9074-123">Requirements</span></span>  

 <span data-ttu-id="b9074-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b9074-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9074-125">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="b9074-125">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="b9074-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9074-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9074-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9074-127">See also</span></span>

- [<span data-ttu-id="b9074-128">合成接口</span><span class="sxs-lookup"><span data-stu-id="b9074-128">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="b9074-129">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="b9074-129">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
