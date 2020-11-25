---
title: IHostMemoryManager::ReleasedVirtualAddressSpace 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.ReleasedVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::ReleasedVirtualAddressSpace
helpviewer_keywords:
- ReleasedVirtualAddressSpace method [.NET Framework hosting]
- IHostMemoryManager::ReleasedVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: d1876601-6ab9-48e1-8ebd-184af1d0cd76
topic_type:
- apiref
ms.openlocfilehash: 8a875d59d270f087ce22079830818a9205309cc5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731288"
---
# <a name="ihostmemorymanagerreleasedvirtualaddressspace-method"></a><span data-ttu-id="c10dd-102">IHostMemoryManager::ReleasedVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="c10dd-102">IHostMemoryManager::ReleasedVirtualAddressSpace Method</span></span>

<span data-ttu-id="c10dd-103">向宿主通知公共语言运行时 (CLR) 已使用指定内存完成。</span><span class="sxs-lookup"><span data-stu-id="c10dd-103">Notifies the host that the common language runtime (CLR) has finished using the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c10dd-104">语法</span><span class="sxs-lookup"><span data-stu-id="c10dd-104">Syntax</span></span>  
  
```cpp  
HRESULT ReleasedVirtualAddressSpace(  
    [in] LPVOID startAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c10dd-105">参数</span><span class="sxs-lookup"><span data-stu-id="c10dd-105">Parameters</span></span>  

 `startAddress`  
 <span data-ttu-id="c10dd-106">中指向要释放的内存的起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="c10dd-106">[in] Pointer to the starting address of the memory to be released.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c10dd-107">注解</span><span class="sxs-lookup"><span data-stu-id="c10dd-107">Remarks</span></span>  

 <span data-ttu-id="c10dd-108">`ReleasedVirtualAddressSpace`方法是一个回调方法，必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="c10dd-108">The `ReleasedVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="c10dd-109">它由 CLR 调用。</span><span class="sxs-lookup"><span data-stu-id="c10dd-109">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c10dd-110">要求</span><span class="sxs-lookup"><span data-stu-id="c10dd-110">Requirements</span></span>  

 <span data-ttu-id="c10dd-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c10dd-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c10dd-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c10dd-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c10dd-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c10dd-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c10dd-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c10dd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c10dd-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c10dd-115">See also</span></span>

- [<span data-ttu-id="c10dd-116">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="c10dd-116">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
