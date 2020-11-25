---
title: IAssemblyCache 接口
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
ms.openlocfilehash: df4f0ba018b55202c22cb90b22b927a9c426c4ed
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696851"
---
# <a name="iassemblycache-interface"></a><span data-ttu-id="bae9e-102">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="bae9e-102">IAssemblyCache Interface</span></span>

<span data-ttu-id="bae9e-103">表示用于合成技术的全局程序集缓存。</span><span class="sxs-lookup"><span data-stu-id="bae9e-103">Represents the global assembly cache for use by the fusion technology.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bae9e-104">方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-104">Methods</span></span>  
  
|<span data-ttu-id="bae9e-105">方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-105">Method</span></span>|<span data-ttu-id="bae9e-106">说明</span><span class="sxs-lookup"><span data-stu-id="bae9e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bae9e-107">CreateAssemblyCacheItem 方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-107">CreateAssemblyCacheItem Method</span></span>](iassemblycache-createassemblycacheitem-method.md)|<span data-ttu-id="bae9e-108">获取对新 [IAssemblyCacheItem](iassemblycacheitem-interface.md)的引用。</span><span class="sxs-lookup"><span data-stu-id="bae9e-108">Gets a reference to a new [IAssemblyCacheItem](iassemblycacheitem-interface.md).</span></span>|  
|[<span data-ttu-id="bae9e-109">CreateAssemblyScavenger 方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-109">CreateAssemblyScavenger Method</span></span>](iassemblycache-createassemblyscavenger-method.md)|<span data-ttu-id="bae9e-110">保留供合成技术内部使用。</span><span class="sxs-lookup"><span data-stu-id="bae9e-110">Reserved for internal use by the fusion technology.</span></span>|  
|[<span data-ttu-id="bae9e-111">InstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-111">InstallAssembly Method</span></span>](iassemblycache-installassembly-method.md)|<span data-ttu-id="bae9e-112">在全局程序集缓存中安装指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="bae9e-112">Installs the specified assembly in the global assembly cache.</span></span>|  
|[<span data-ttu-id="bae9e-113">QueryAssemblyInfo 方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-113">QueryAssemblyInfo Method</span></span>](iassemblycache-queryassemblyinfo-method.md)|<span data-ttu-id="bae9e-114">获取有关指定程序集的请求的数据。</span><span class="sxs-lookup"><span data-stu-id="bae9e-114">Gets the requested data about the specified assembly.</span></span>|  
|[<span data-ttu-id="bae9e-115">UninstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="bae9e-115">UninstallAssembly Method</span></span>](iassemblycache-uninstallassembly-method.md)|<span data-ttu-id="bae9e-116">从全局程序集缓存中卸载指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="bae9e-116">Uninstalls the specified assembly from the global assembly cache.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bae9e-117">要求</span><span class="sxs-lookup"><span data-stu-id="bae9e-117">Requirements</span></span>  

 <span data-ttu-id="bae9e-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bae9e-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bae9e-119">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="bae9e-119">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="bae9e-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bae9e-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bae9e-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bae9e-121">See also</span></span>

- [<span data-ttu-id="bae9e-122">合成接口</span><span class="sxs-lookup"><span data-stu-id="bae9e-122">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="bae9e-123">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="bae9e-123">Global Assembly Cache</span></span>](../../app-domains/gac.md)
