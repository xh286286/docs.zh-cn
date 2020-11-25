---
title: IMetaDataDispenserEx 接口
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx
helpviewer_keywords:
- IMetaDataDispenserEx interface [.NET Framework metadata]
ms.assetid: 78b3629e-77a2-4406-89c3-56b5cc2c4594
topic_type:
- apiref
ms.openlocfilehash: 60d321c1a87a5da433437c9d4587fa9f8947acf4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713374"
---
# <a name="imetadatadispenserex-interface"></a><span data-ttu-id="7d3f0-102">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="7d3f0-102">IMetaDataDispenserEx Interface</span></span>

<span data-ttu-id="7d3f0-103">扩展 [IMetaDataDispenser 接口](imetadatadispenser-interface.md) 接口，以提供控制元数据 api 对当前元数据范围的操作方式的功能。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-103">Extends the [IMetaDataDispenser Interface](imetadatadispenser-interface.md) interface to provide the capability to control how the metadata APIs operate on the current metadata scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7d3f0-104">方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-104">Methods</span></span>  
  
|<span data-ttu-id="7d3f0-105">方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-105">Method</span></span>|<span data-ttu-id="7d3f0-106">说明</span><span class="sxs-lookup"><span data-stu-id="7d3f0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7d3f0-107">FindAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-107">FindAssembly Method</span></span>](imetadatadispenserex-findassembly-method.md)|<span data-ttu-id="7d3f0-108">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-108">This method is not implemented.</span></span> <span data-ttu-id="7d3f0-109">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-109">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="7d3f0-110">FindAssemblyModule 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-110">FindAssemblyModule Method</span></span>](imetadatadispenserex-findassemblymodule-method.md)|<span data-ttu-id="7d3f0-111">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-111">This method is not implemented.</span></span> <span data-ttu-id="7d3f0-112">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-112">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="7d3f0-113">GetCORSystemDirectory 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-113">GetCORSystemDirectory Method</span></span>](imetadatadispenserex-getcorsystemdirectory-method.md)|<span data-ttu-id="7d3f0-114">获取 (CLR) 保存当前公共语言运行时的目录。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-114">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="7d3f0-115">此方法仅支持在进程外调试器中使用。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-115">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="7d3f0-116">如果从另一个组件调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-116">If called from another component, it will return E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="7d3f0-117">GetOption 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-117">GetOption Method</span></span>](imetadatadispenserex-getoption-method.md)|<span data-ttu-id="7d3f0-118">为当前元数据范围获取指定选项的值。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-118">Gets the value of the specified option for the current metadata scope.</span></span> <span data-ttu-id="7d3f0-119">选项控制如何处理对当前元数据范围的调用。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-119">The option controls how calls to the current metadata scope are handled.</span></span>|  
|[<span data-ttu-id="7d3f0-120">OpenScopeOnITypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-120">OpenScopeOnITypeInfo Method</span></span>](imetadatadispenserex-openscopeonitypeinfo-method.md)|<span data-ttu-id="7d3f0-121">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-121">This method is not implemented.</span></span> <span data-ttu-id="7d3f0-122">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-122">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="7d3f0-123">SetOption 方法</span><span class="sxs-lookup"><span data-stu-id="7d3f0-123">SetOption Method</span></span>](imetadatadispenserex-setoption-method.md)|<span data-ttu-id="7d3f0-124">为当前元数据范围将指定的选项设置为给定的值。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-124">Sets the specified option to a given value for the current metadata scope.</span></span> <span data-ttu-id="7d3f0-125">选项控制如何处理对当前元数据范围的调用。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-125">The option controls how calls to the current metadata scope are handled.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7d3f0-126">要求</span><span class="sxs-lookup"><span data-stu-id="7d3f0-126">Requirements</span></span>  

 <span data-ttu-id="7d3f0-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d3f0-127">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d3f0-128">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="7d3f0-128">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7d3f0-129">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="7d3f0-129">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7d3f0-130">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d3f0-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d3f0-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d3f0-131">See also</span></span>

- [<span data-ttu-id="7d3f0-132">元数据接口</span><span class="sxs-lookup"><span data-stu-id="7d3f0-132">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="7d3f0-133">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="7d3f0-133">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
- [<span data-ttu-id="7d3f0-134">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="7d3f0-134">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="7d3f0-135">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="7d3f0-135">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
